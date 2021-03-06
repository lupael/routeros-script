# Update tunnelbroker configuration

[◀ Go back to main README](../)

## Description

Connecting to [tunnelbroker.net](https://github.com/lupael/Mikrotik-scripts/tree/6cea5a9f9b7f331ef0dcc7eb494887eef2441a62/tunnelbroker.net) from dynamic public ip address requires the address to be sent to the remote, and to be set locally. This script does both.

## Requirements and installation

Just install the script:

```text
$ScriptInstallUpdate update-tunnelbroker;
```

Installing [ppp-on-up](ppp-on-up.md) makes this script run when ever a ppp connection is established.

## Configuration

The configuration goes to interface's comment:

```text
/ interface 6to4 set comment="tunnelbroker, user=user, pass=s3cr3t, id=12345" tunnelbroker;
```

Also enabling dynamic DNS in Mikrotik cloud is required:

```text
/ ip cloud set ddns-enabled=yes;
```

## See also

* [Run scripts on ppp connection](ppp-on-up.md)

[◀ Go back to main README](../)  
[▲ Go back to top](update-tunnelbroker.md#top)

