# Networking

## Basic Networking Concepts

Pop!_OS conforms to TCP/IP and other standards for network interconnectivity. In order to have a working internet connection, your computer must have:

- **Physical connection:** A wired (usually RJ-45 Ethernet) or wireless (usually 802.11 WiFi) connection to a network.
- **MAC address:** A physical address for the network card.
    - A MAC address is physically programmed into the network card, and generally can't be changed.
    - Other computers on the same network use MAC addresses to communicate directly with each other.
- **IP address:** A logical address for the network connection.
    - An IP address may be automatically assigned or manually configured.
    - The router uses IP addresses to identify where to send traffic after it crosses into or out of a network. (Other computers on the same network can also identify each other by IP address, but they will translate it into a MAC address behind-the-scenes.)
- **DNS:** A domain name system to translate domain names into IP addresses.
    - One or more DNS servers may be automatically discovered or manually configured.

### Domain Name System (DNS)

DNS translates domain names (e.g. `system76.com`) into IP addresses (e.g. `18.64.183.102`). The DNS services on your computer perform this translation every time you use a domain name. If your system has internet connection but no working DNS, you may be able to ping IP addresses, but you won't be able to navigate to websites using their names.

DNS in Pop!_OS utilizes the following sources, in order:

1. `/etc/hosts`: A local file where DNS overrides can be manually configured.
    - By default, `localhost` is configured to resolve to `127.0.0.1` for IPv4 and `::1` for IPv6 in this file.
2. `libnss-myhostname`: A module that resolves your computer's hostname (e.g. `pop-os` or `S1m0n-Laptop`) to `127.0.0.2`.
    - If the `localhost` entires are removed from `/etc/hosts`, then this module will also translate `localhost` to `127.0.0.2` for IPv4 and `::1` for IPv6.
3. `systemd-resolved`: A local service that handles general domain name resolution by sending queries to your configured DNS servers and returning the responses.
    - This service will cache the most recent 4096 responses for up to 2 hours. The cache can be cleared by running `resolvectl flush-caches` in a terminal.
    - If `libnss-myhostname` isn't present, this service will also perform the same functions that it would.
    
## Configuring Networking (GUI)

To configure networking using a graphical interface, see the appropriate section of the COSMIC documentation.

## Configuring Networking Manually

### NetworkManager

### DNS Configuration