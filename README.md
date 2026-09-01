# EdgeTX Script Builder

A playful, no-code builder for EdgeTX Lua telemetry scripts. Stack **display blocks** (Text, Value, Gauge, Battery Icon, Divider) and **action blocks** (Sound Alarm, Link Alarm, Switch Sound, Voice Timer, Random Sound, Greeting Sound) one below another, tweak their properties, and get a ready-to-use `.lua` script for your radio — no programming knowledge required.

Open [`index.html`](index.html) in a browser to use it.

## How it works

1. Tap a block on the left to add it to your script.
2. Configure it — telemetry source, thresholds, sounds, text, size, alignment.
3. Reorder blocks with the arrows or by dragging the handle; the on-screen order matches the list order.
4. The mock LCD preview and the generated Lua code update live.
5. Copy the code (or download it) and save it as a `.lua` file.
6. Copy it to `/SCRIPTS/TELEMETRY/` on your radio's SD card, add the sound files under `/SOUNDS/`, and assign it as a telemetry screen (Screens → Add telemetry screen → type "Script").

A generated screen only runs its logic — including any Sound/Link/Timer blocks placed on it — while it is the telemetry screen currently shown on the radio. Set it as your default/home screen if its alarms should always be active.

**Always test a new script on the ground, without power to the motor/propellers, before flying with it.**

## Status

This is a community tool and not an official EdgeTX project. It targets the standard EdgeTX Lua telemetry-script API (`getValue`, `playFile`, `lcd.*`, …) and has been checked for correctness against that API, but EdgeTX versions differ — verify behavior on your own radio before relying on it in flight.
