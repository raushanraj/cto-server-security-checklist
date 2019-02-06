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
