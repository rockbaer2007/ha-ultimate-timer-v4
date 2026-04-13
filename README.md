# ⏱️ Ultimate Timer V4 (Countdown + Stable Core)

[![Open in Home
Assistant](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https://raw.githubusercontent.com/rockbaer2007/ha-ultimate-timer-v4/main/blueprints/automation/ultimate_timer_v4.yaml)

![GitHub
release](https://img.shields.io/github/v/release/rockbaer2007/ha-ultimate-timer-v4)
![GitHub
stars](https://img.shields.io/github/stars/rockbaer2007/ha-ultimate-timer-v4?style=social)

> Advanced timer blueprint for Home Assistant with integrated countdown
> and stable core logic.

------------------------------------------------------------------------

## 🚀 Features

-   ⏱️ Timer in `hh:mm:ss` format\
-   ▶️ Start trigger (button)\
-   ⏹️ Reliable STOP\
-   📡 Running status\
-   🎯 DONE stays active until reset\
-   🌙 Daily reset\
-   🔁 Multi-instance capable\
-   🛡️ No race conditions\
-   ⏳ Integrated countdown (NEW in V4)

------------------------------------------------------------------------

## 🔄 Upgrade from V3

### V3 → V4

-   Added countdown\
-   Start time + duration storage\
-   New architecture (logic + UI separated)

👉 V3 remains stable -- V4 is the evolution

------------------------------------------------------------------------

## 📦 Installation

### Manual

    config/blueprints/automation/

------------------------------------------------------------------------

### Direct import

[Open in Home
Assistant](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https://raw.githubusercontent.com/rockbaer2007/ha-ultimate-timer-v4/main/blueprints/automation/ultimate_timer_v4.yaml)

------------------------------------------------------------------------

## ⚙️ Configuration

  Field               Description
  ------------------- -------------------
  Start               Start timer
  Stop                Stop timer
  Duration            hh:mm:ss
  Running             Active
  Done                Finished
  Start Time Helper   stores start time
  Duration Helper     stores duration
  Reset               daily reset

------------------------------------------------------------------------

## ⚙️ Required Helpers

    input_boolean:
      timer_start:
      timer_stop:
      timer_running:
      timer_done:

    input_datetime:
      timer_start_time:
        has_date: false
        has_time: true

    input_number:
      timer_duration_sec:
        min: 0
        max: 86400
        step: 1

------------------------------------------------------------------------

## 🧠 How it works

1.  Start → Timer runs\
2.  Running → ON\
3.  Countdown starts automatically\
4.  Stop → immediately OFF\
5.  Finished → DONE = ON\
6.  Reset → everything OFF

------------------------------------------------------------------------

## 💡 Use Cases

-   Pool / pond pumps\
-   Irrigation\
-   Watchdog\
-   Delays\
-   Countdown display

------------------------------------------------------------------------

## 📜 License

MIT License

------------------------------------------------------------------------

## ⭐ Support

If you like this project, give it a ⭐
