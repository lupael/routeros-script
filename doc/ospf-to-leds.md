# Visualize OSPF state via LEDs

[◀ Go back to main README](../)

## Description

Physical interfaces have their state LEDs, software-defined connectivity does not. This script helps to visualize whether or not an OSPF instance is running.

## Requirements and installation

Just install the script:

```text
$ScriptInstallUpdate ospf-to-leds;
```

... and add a scheduler to run the script periodically:

```text
/ system scheduler add interval=20s name=ospf-to-leds on-event="/ system script run ospf-to-leds;" start-time=startup;
```

## Configuration

The configuration goes to OSPF instance's comment. To visualize state for instance `default` via LED `user-led` set this:

```text
/ routing ospf instance set default comment="ospf-to-leds, leds=user-led";
```

[◀ Go back to main README](../)  
[▲ Go back to top](ospf-to-leds.md#top)

