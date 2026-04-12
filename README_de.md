# ⏱️ Ultimate Timer V4 (Countdown + stabile Basis)

🇬🇧 [English Version](README.md)

> Erweiterter Timer Blueprint mit integriertem Countdown.

---

## 🚀 Features

- Stabiler START / STOP
- RUNNING bleibt korrekt
- DONE bleibt aktiv bis Reset
- Multi-Instance fähig
- ⏳ Countdown Unterstützung

---

## 📦 Installation

Blueprint nach:

config/blueprints/automation/

kopieren.

---

## ⚙️ Benötigte Helper

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

## 🧠 Funktionsweise

1. Start → Timer startet
2. Running → EIN
3. Countdown läuft
4. Stop → AUS
5. Ablauf → Done EIN
6. Reset → AUS

---

## ⭐ Support

Wenn dir das Projekt gefällt, gib ihm ein ⭐
