# Renew certificates and notify on expiration

[◀ Go back to main README](../)

## Description

This script tries to download and renew certificates, then notifies about certificates that are still about to expire.

## Requirements and installation

Just install the script:

```text
$ScriptInstallUpdate check-certificates;
```

## Configuration

The expiry notifications just require notification settings for e-mail and telegram.

For automatic download and renewal of certificates you need configuration in `global-config-overlay`, these are the parameters:

* `CertRenewPass`: an array of passphrases to try
* `CertRenewUrl`: the url to download certificates from

Certificates on the web server should be named `CN.pem` \(`PEM` format\) or `CN.p12` \(`PKCS#12` format\).

## Usage and invocation

Just run the script:

```text
/ system script run check-certificates;
```

... or create a scheduler for periodic execution:

```text
/ system scheduler add interval=1d name=check-certificates on-event="/ system script run check-certificates;" start-time=startup;
```

Alternatively running on startup may be desired:

```text
/ system scheduler add name=check-certificates-startup on-event="/ system script { run global-wait; run check-certificates; }" start-time=startup;
```

## See also

* [Renew locally issued certificates](certificate-renew-issued.md)

[◀ Go back to main README](../)  
[▲ Go back to top](check-certificates.md#top)

