# ⏱️ Ultimate Timer V4 (HH+MM Version)

Erweiterter Timer Blueprint für Home Assistant mit **Stunden + Minuten Eingabe**, Countdown und stabiler Logik.

## 🚀 Features

- ⏱️ Timer mit **Stunden + Minuten**
- ▶️ Start / ⏹️ Stop
- 📡 Running + Done Status
- 🎯 DONE bleibt aktiv bis Reset
- 🔁 Multi-Instance fähig
- ⏳ Countdown Anzeige
- 🧠 keine Template Probleme (stabil)

---

## ⚙️ Konfiguration

| Feld | Beschreibung |
|------|------------|
| Start | Timer starten |
| Stop | Timer stoppen |
| Stunden | input_number (0–10) |
| Minuten | input_number (0–59, Schritt 5 empfohlen) |
| Running | Aktiv |
| Done | Fertig |
| Startzeit | wird gespeichert |
| Dauer | automatisch berechnet |

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
3. Dauer wird automatisch berechnet
4. Countdown läuft
5. Stop = sofort AUS
6. Ablauf = DONE = EIN

---

## 🖥️ UI (Mushroom)

- Start / Stop Buttons
- Countdown Anzeige
- Stunden + Minuten Steuerung
- Presets
- nutzt `increment/decrement` (Profi-Lösung)

---

## 💡 Einsatz

- Pool / Teich
- Bewässerung
- Verzögerungen
- Watchdog
- Countdown Anzeige

---

## 📜 Lizenz

MIT
