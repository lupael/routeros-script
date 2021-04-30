# Forward received SMS

[◀ Go back to main README](../)

## Description

RouterOS can receive SMS. This script forwards SMS as notification.

A broadband interface with SMS support is required.

## Requirements and installation

Just install the script:

```text
$ScriptInstallUpdate sms-forward;
```

... and add a scheduler to run it periodically:

```text
/ system scheduler add interval=2m name=sms-forward on-event="/ system script run sms-forward;" start-time=startup;
```

## Configuration

Notification settings are required for e-mail and telegram. Also you have to enable receiving of SMS:

```text
/ tool sms set receive-enabled=yes;
```

## See also

* [Act on received SMS](sms-action.md)

[◀ Go back to main README](../)  
[▲ Go back to top](sms-forward.md#top)

