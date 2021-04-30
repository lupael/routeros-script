# Upload backup to Mikrotik cloud

[◀ Go back to main README](../)

## Description

This script uploads [binary backup to Mikrotik cloud](https://wiki.mikrotik.com/wiki/Manual:IP/Cloud#Backup).

## Requirements and installation

Just install the script:

```text
$ScriptInstallUpdate cloud-backup;
```

## Configuration

The configuration goes to `global-config-overlay`, this is the only parameter:

* `BackupPassword`: password to encrypt the backup with

Also notification settings are required for e-mail and telegram.

## Usage and invocation

Just run the script:

```text
/ system script run cloud-backup;
```

Creating a scheduler may be an option:

```text
/ system scheduler add interval=1w name=cloud-backup on-event="/ system script run cloud-backup;" start-time=09:20:00;
```

## See also

* [Send backup via e-mail](email-backup.md)
* [Upload backup to server](upload-backup.md)

[◀ Go back to main README](../)  
[▲ Go back to top](cloud-backup.md#top)

