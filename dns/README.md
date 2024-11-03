# DNS Configuration with dnsmasq

This folder contains configuration files for [dnsmasq](https://thekelleys.org.uk/dnsmasq/doc.html), a lightweight DNS and DHCP server.

## Configuration File

The main configuration file for dnsmasq is `dnsmasq.conf`, which is typically located at: `/etc/dnsmasq.conf`


This file can be modified to customize dnsmasq's DNS and DHCP behavior as needed.

## Adding New DNS Records

To add new DNS records, simply edit the `/etc/hosts` file. Entries in `/etc/hosts` will be resolved by dnsmasq, allowing you to define custom DNS mappings. For example:

```
192.168.0.10 my-local-service 
192.168.0.144 another-service.local
```

After making changes to `/etc/hosts`, restart dnsmasq to apply the updates:

```bash
sudo systemctl restart dnsmasq
```

For more details on configuration options and capabilities, refer to the [dnsmasq documentation](https://thekelleys.org.uk/dnsmasq/doc.html).
