# Installation

1. Install Unbound
```bash
sudo apt install unbound -y
```

2. Download Root Hints File (Recommended to run every 6 months*)
   
   This file helps Unbound find the root DNS server.
```bash
sudo curl -o /var/lib/unbound/root.hints https://www.internic.net/domain/named.root
```

3. Create Unbound config file for Pi-Hole

   Create a config file at /etc/unbound/unbound.conf.d/pi-hole/conf
```bash
sudo nano /etc/unbound/unbound.conf.d/pi-hole.conf
```
Paste this configuration:
```bash
server:
    verbosity: 0
    interface: 127.0.0.1
    port: 5335
    do-ip4: yes
    do-udp: yes
    do-tcp: yes
    root-hints: "/var/lib/unbound/root.hints"
    hide-identity: yes
    hide-version: yes
    harden-glue: yes
    harden-dnssec-stripped: yes
    use-caps-for-id: yes
    edns-buffer-size: 1232
    prefetch: yes
    qname-minimisation: yes
    cache-min-ttl: 3600
    cache-max-ttl: 86400
    num-threads: 1
    so-rcvbuf: 1m
```
Save and Exit.

4. Restart Service
```bash
sudo service unbound restart
```

5. Point Pi-hole to Unbound

   Go to the Pi-hole admin Interface:
   - Navigate to settings > DNS
   - Uncheck any current upstream DNS servers
   - In the Custom 1 (IPv4) field, enter:
```bash
127.0.0.1#5335
```
- Click Save

![DNS Settings](/configs/unbound/images/dnssettings.png)

6. Test the Setup

In terminal input:
```bash
dig example.com @127.0.0.1 -p 5335
```
If you get a response Unbound is working.

Also test through Pi-hole:
```bash
dig example.com @127.0.0.1
```