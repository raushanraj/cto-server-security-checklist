# cto-server-security-checklist

Minimal checklist to secure your linux cloud servers. (AWS/Digitalocean/Linode)

## Vulnerability Management
- [ ] Check and Update vulnerable .deb or .rpm packages. Use Vulners audit [dashboard](https://vulners.com/audit).

- [ ] Remove/Update backdoored/outdated pip packages.
```bash
$ pip install safety
$ safety check
```

## IT Compliance
- [ ]  Scan server for GDPR, PCI DSS, HIPPA compliance. [cisofy](https://cisofy.com/lynis/)


## Practices

- [ ] Encrypt primary disk. [LUKS](https://www.linode.com/docs/security/encryption/use-luks-for-full-disk-encryption/)

- [ ] Regulary monitor open ports. (nmap)

- [ ] Enable iptables.

- [ ] Install light weight HIDS agent. [osquery](http://osquery.io)

- [ ] Enable SELinux. 
```
$ setenforce enforcing
```


## Intrusions and Malwares

- [ ] Enable rootkit check and monitor logs. [osquery](https://github.com/facebook/osquery/blob/experimental/packs/ossec-rootkit.conf)

- [ ] Scan important directory with [ClamAV](https://www.clamav.net/)

- [ ] Monitor processes and sockets for [Threat Detection.](https://blog.rapid7.com/2016/05/09/introduction-to-osquery-for-threat-detection-dfir/)
