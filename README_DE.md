# ⏱️ Ultimate Timer V4 (Countdown + stabile Basis)

🇬🇧 [English Version](README.md)

> Erweiterter Timer Blueprint für Home Assistant mit integriertem Countdown und stabiler Kernlogik.

---

## 🚀 Features

- ⏱️ Timer (NEU: Stunden + Minuten)
- ▶️ Start-Trigger
- ⏹️ zuverlässiger STOP
- 📡 Running Status
- 🎯 DONE bleibt aktiv bis Reset
- 🌙 täglicher Reset
- 🔁 Multi-Instance fähig
- ⏳ Countdown

---

## 🆕 NEU (HH+MM Version)

- Verwendung von input_number (Stunden + Minuten)
- keine Probleme mit duration Format
- stabiler als hh:mm:ss

---

## ⚙️ Konfiguration

| Feld | Beschreibung |
|------|------------|
| Start | Timer starten |
| Stop | Timer stoppen |
| Stunden | input_number |
| Minuten | input_number |

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

## 🧠 Funktionsweise

1. Stunden + Minuten einstellen
2. Start drücken
3. Countdown läuft
4. Stop → sofort AUS
5. Ablauf → DONE = EIN

---

## 📜 Lizenz

MIT
