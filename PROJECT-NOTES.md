# Project notes — ESPHome weather station

(Assembled 2026-10-22 from the project's goal notes for
publication. This is all that exists for this project so far.)

An ESPHome-based weather station integrated with Home Assistant,
running always-on without deep sleep. The open problem is battery:
battery life is not visible in Home Assistant, and the options
being weighed are a voltage-divider wiring addition (battery+ →
100k + 100k divider → GPIO2, ADC multiply 2.0), a deep-sleep
configuration (wake ~30 s / sleep ~10 min), and a cheap solar
panel for charging.

Measured/estimated runtime on the 2600 mAh cell, always-on:
~2–4 days per charge; a small solar panel alone would stretch
that to roughly a week in good weather.
