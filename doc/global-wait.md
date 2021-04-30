# Wait for configuration und functions

[◀ Go back to main README](../)

## Description

The global scripts `global-config`, `global-config-overlay` and `global-functions` are run by scheduler at system startup. Running another script at system startup may result in race condition where configuration and/or function are not yet available. This script is supposed to wait for everything being prepared.

Do **not** add this script `global-wait` to the `global-scripts` scheduler! It would inhibit the initialization of configuration and functions.

## Requirements and installation

Just install the script:

```text
$ScriptInstallUpdate global-wait;
```

... and add it to your scheduler, for example in combination with [bridge-port](bridge-port.md):

```text
/ system scheduler add name=bridge-port-to-default on-event="/ system script { run global-wait; run bridge-port-to-default; }" start-time=startup;
```

## See also

* [Manage ports in bridge](bridge-port.md)
* [Download packages for CAP upgrade from CAPsMAN](capsman-download-packages.md)
* [Renew certificates and notify on expiration](check-certificates.md)
* [Use wireless network with daily psk](daily-psk.md)

[◀ Go back to main README](../)  
[▲ Go back to top](global-wait.md#top)

