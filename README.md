# ⏱️ Ultimate Timer V4 (HH+MM Edition)

Advanced timer blueprint for Home Assistant with **stable HH + MM inputs**, countdown and clean UI.

## 🚀 Features

- ⏱️ Timer using **hours + minutes helpers**
- ▶️ Start / ⏹️ Stop
- 📡 Running + Done states
- 🎯 DONE stays active until reset
- 🔁 Multi-instance capable
- ⏳ Countdown sensor support
- 🧠 No template parsing issues (stable core)

---

## ⚙️ Configuration

| Field | Description |
|------|------------|
| Start | Start timer |
| Stop | Stop timer |
| Hours | input_number (0–10) |
| Minutes | input_number (0–59, step 5 recommended) |
| Running | Timer active |
| Done | Timer finished |
| Start Time | stores start time |
| Duration (sec) | calculated automatically |

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

1. Set **hours + minutes**
2. Press Start
3. Duration is calculated automatically
4. Countdown runs
5. Stop = immediate stop
6. Finished = DONE = ON

---

## 🖥️ UI (Mushroom)

- Start / Stop buttons
- Countdown display
- Hour + Minute controls
- Presets (10 min, 30 min, 1h, etc.)
- Uses `input_number.increment/decrement` (PRO)

---

## 💡 Use Cases

- Pool / pond pump
- Irrigation
- Delays
- Watchdog
- Countdown display

---

## 📜 License

MIT
