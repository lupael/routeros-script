# Manage LEDs dark mode

[◀ Go back to main README](../)

## Description

These scripts control LEDs mode and allow to run your device completely dark. Hardware support for dark mode is required.

## Requirements and installation

Just install the scripts:

```text
$ScriptInstallUpdate leds-day-mode,leds-night-mode,leds-toggle-mode;
```

## Usage and invocation

To switch the device to dark mode:

```text
/ system script run leds-night-mode;
```

... and back to normal mode:

```text
/ system script run leds-day-mode;
```

To toggle between the two modes:

```text
/ system script run leds-toggle-mode;
```

Add these schedulers to switch to dark mode in the evening and back to normal mode in the morning:

```text
/ system scheduler add interval=1d name=leds-day-mode on-event="/ system script run leds-day-mode;" start-time=07:00:00;
/ system scheduler add interval=1d name=leds-night-mode on-event="/ system script run leds-night-mode;" start-time=21:00:00;
```

The script `leds-toggle-mode` can be used from [mode button](mode-button.md) to toggle mode.

## See also

* [Mode button with multiple presses](mode-button.md)

[◀ Go back to main README](../)  
[▲ Go back to top](leds-mode.md#top)

