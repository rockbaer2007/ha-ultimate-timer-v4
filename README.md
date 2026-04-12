# ⏱️ Ultimate Timer V4 (Countdown + Stable Core)

[![Open in Home Assistant](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https://raw.githubusercontent.com/rockbaer2007/ha-ultimate-timer-v4/main/blueprints/automation/ultimate_timer_v4.yaml)

🇩🇪 [German Version](README_de.md)

> Advanced timer blueprint with integrated countdown support.

---

## 🚀 Features

- Reliable START / STOP
- Stable RUNNING state
- DONE stays ON until reset
- Multi-instance safe
- ⏳ Countdown support (via template sensor)

---

## 📦 Installation

Copy blueprint to:

config/blueprints/automation/

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
  timer_duration_sec:
    min: 0
    max: 86400
    step: 1
```

---

## ⏳ Countdown Sensor

```yaml
template:
  - sensor:
      - name: "Timer Countdown"
        icon: mdi:timer-outline
        state: >
          {% set start = states('input_datetime.timer_start_time') %}
          {% set duration = states('input_number.timer_duration_sec') | int %}

          {% if start not in ['unknown','unavailable',''] and duration > 0 %}
            {% set start_ts = strptime(start, '%H:%M:%S') %}
            {% set now_ts = now() %}

            {% set elapsed =
              (now_ts.hour*3600 + now_ts.minute*60 + now_ts.second) -
              (start_ts.hour*3600 + start_ts.minute*60 + start_ts.second)
            %}

            {% set remaining = duration - elapsed %}
            {% set r = remaining if remaining > 0 else 0 %}

            {{ '%02d:%02d:%02d' | format(r//3600, (r%3600)//60, r%60) }}
          {% else %}
            00:00:00
          {% endif %}
```

---

## 🧠 How It Works

1. Start → Timer starts
2. Running → ON
3. Countdown → active
4. Stop → OFF
5. Timeout → Done ON
6. Reset → OFF

---

## ⭐ Support

If you like this project, give it a star ⭐
