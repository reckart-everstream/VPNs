# VPN & datacenter IPs
This is a list of common VPN providers. There are lots of lists of open proxies and tor nodes on the web, but surprisingly few usable ones dedicated to VPN providers and datacenters. This list combines:

  - Known VPN hostnames
  - ASNs owned by datacenters and VPN providers

This list doesn't list _all_ VPNs, but should list the vast majority of common ones.

Because this list gets its data directly from BGP & DNS hostname lookups, false positives are extremely unlikely.

# Use cases
There are lots of legitimate reasons to use VPNs, including perfectly valid concerns around censorship, privacy, and security. Still, to name some examples, you might want to block VPNs or treat them differently if:

  - You are a game server (especially one that can only ban players by easily changable IPs)
  - You run a commercial application with a very high fraud risk, i.e. ecommerce
  - You are trying to filter some types of DDoS or spam
  - You are required to do so for legal reasons

Because this list indiscriminately lists datacenters, it's unlikely to be useful to oppressive governments or ISPs.

# How to use
Feed the vpn-ipv4.txt file and/or the vpn-ipv6.txt file to your firewall or application.

For extra effectiveness, consider supplementing this list with blocklists for recently abusive IPs, as these invariably include many VPNs, and lists of open proxies/tor nodes. You should be able to find everything you need in that regard at http://iplists.firehol.org. At the very least, consider using _firehol_level1_, _firehol_level2_, _firehol_abusers_1d_, and _firehol_proxies_ with this list, depending on your needs.

Before implementing, consider that this list probably includes your own server's IP range, that of your DNS server, the server you get your software updates from, and the servers common search engines live on. Take a moment to make sure you don't accidentally use it to block network traffic you need. In a web application, you might want these IPs to GET, but not POST. In a firewall, you might want to block access to a specific port, but allow these IPs otherwise.

# How to contribute
Please open an issue if you know a VPN provider not listed here _and_ have a list of their DNS hostnames, or in the extremely unlikely case that you find a false positive entry in this list, or if you have any other suggestions or problems related to this list. 

Being mostly datacenter IPs, all IPs in this list change infrequently. The list is usually updated every 2 months.
