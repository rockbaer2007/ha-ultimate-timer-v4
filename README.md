# ⏱️ Ultimate Timer V4 (Countdown + Stable Core)

[![Open in Home Assistant](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https://raw.githubusercontent.com/rockbaer2007/ha-ultimate-timer-v4/main/blueprints/automation/ultimate_timer_v4.yaml)

![GitHub release](https://img.shields.io/github/v/release/rockbaer2007/ha-ultimate-timer-v4)
![GitHub stars](https://img.shields.io/github/stars/rockbaer2007/ha-ultimate-timer-v4?style=social)

> Advanced timer blueprint for Home Assistant with integrated countdown and stable core logic.

---

## 🚀 Features

- ⏱️ Timer (NEW: HH + MM helper based)
- ▶️ Start trigger (button)
- ⏹️ Reliable STOP
- 📡 Running status
- 🎯 DONE stays active until reset
- 🌙 Daily reset
- 🔁 Multi-instance capable
- 🛡️ No race conditions
- ⏳ Integrated countdown (V4)

---

## 🆕 NEW (HH+MM Version)

- Uses input_number (hours + minutes)
- No template parsing issues
- No duration selector problems
- More stable and HA-native approach

---

## ⚙️ Configuration

| Field | Description |
|------|------------|
| Start | Start timer |
| Stop | Stop timer |
| Hours | input_number |
| Minutes | input_number |
| Running | Active |
| Done | Finished |

---

## ⚙️ Required Helpers

```yaml
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
  timer_hours:
    min: 0
    max: 10
    step: 1

  timer_minutes:
    min: 0
    max: 59
    step: 5

  timer_duration_sec:
    min: 0
    max: 86400
    step: 1
```

---

## 🧠 How it works

1. Set hours + minutes
2. Press Start
3. Countdown runs
4. Stop → immediate OFF
5. Finished → DONE = ON

---

## 📜 License

MIT
