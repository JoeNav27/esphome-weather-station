# ESPHome Weather Station

An ESPHome-based weather station integrated with Home Assistant.

Built by JoeNav27.

## Status — notes only, for now

This repo is currently just the project notes (see
`PROJECT-NOTES.md`). The station itself is set up and running, but
its live ESPHome YAML was never exported into a file here, so there
is no config to publish yet. The notes record what's known: the
setup, the battery situation, and the options on the table for
fixing battery visibility and runtime.

## The setup

- ESPHome device reporting to Home Assistant
- Runs always-on (no deep sleep)
- Battery powered from a 2600 mAh cell — roughly 2–4 days per
  charge at the current always-on draw

## Open items

- No battery level visible in Home Assistant yet. Planned fix:
  voltage divider (battery+ through 100k + 100k resistors to
  GPIO2, ADC multiply 2.0) plus an ESPHome battery sensor.
- Deep-sleep option (wake ~30 s, sleep ~10 min) would stretch a
  charge to months, at the cost of continuous readings.
- A small cheap solar panel is being considered to keep the cell
  topped up; in good weather it would stretch a charge to roughly
  a week. Not purchased yet.
