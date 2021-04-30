# Install LTE firmware upgrade

[◀ Go back to main README](../)

## Description

This script upgrades LTE firmware on compatible devices:

* R11e-LTE
* R11e-LTE-US
* R11e-4G
* R11e-LTE6

A temporary scheduler is created to be independent from terminal. Thus starting the upgrade process over the broadband connection is supported.

## Requirements and installation

Just install the script:

```text
$ScriptInstallUpdate unattended-lte-firmware-upgrade;
```

## Usage and invocation

Run the script if an upgrade for your LTE hardware is available:

```text
/ system script run unattended-lte-firmware-upgrade;
```

Then be patient, go for a coffee and wait for the upgrade process to finish.

## See also

* [Notify on LTE firmware upgrade](check-lte-firmware-upgrade.md)

[◀ Go back to main README](../)  
[▲ Go back to top](unattended-lte-firmware-upgrade.md#top)

