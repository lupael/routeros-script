# Run scripts on ppp connection

[◀ Go back to main README](../)

## Description

This script is supposed to run on established ppp connection. Currently it does:

* release IPv6 dhcp leases \(and thus force a renew\)
* run [update-tunnelbroker](update-tunnelbroker.md)

## Requirements and installation

Just install the script:

```text
$ScriptInstallUpdate ppp-on-up;
```

... and make it the `on-up` script for ppp profile:

```text
/ ppp profile set on-up=ppp-on-up [ find ];
```

## See also

* [Update configuration on IPv6 prefix change](ipv6-update.md)
* [Update tunnelbroker configuration](update-tunnelbroker.md)

[◀ Go back to main README](../)  
[▲ Go back to top](ppp-on-up.md#top)

