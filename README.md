# ⏱️ Ultimate Timer V4 (Countdown + stabile Basis)

[![Open in Home Assistant](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https://raw.githubusercontent.com/rockbaer2007/ha-ultimate-timer-v4/main/blueprints/automation/ultimate_timer_v4.yaml)

![GitHub release](https://img.shields.io/github/v/release/rockbaer2007/ha-ultimate-timer-v4)
![GitHub stars](https://img.shields.io/github/stars/rockbaer2007/ha-ultimate-timer-v4?style=social)

🇬🇧 [English Version](README.md)

> Erweiterter Timer Blueprint für Home Assistant mit integriertem Countdown und stabiler Kernlogik.

---

## 🚀 Features

- ⏱️ Timer im Format `hh:mm:ss`  
- ▶️ Start-Trigger (Taster)  
- ⏹️ zuverlässiger STOP  
- 📡 Running Status  
- 🎯 DONE bleibt aktiv bis Reset  
- 🌙 täglicher Reset  
- 🔁 Multi-Instance fähig  
- 🛡️ keine Race Conditions  
- ⏳ **integrierter Countdown (NEU in V4)**  

---

## 🔄 Upgrade von V3

### V3 → V4

- Countdown hinzugefügt  
- Startzeit + Dauer Speicherung  
- neue Architektur (Logik + Anzeige getrennt)  

👉 V3 bleibt stabil – V4 ist die Weiterentwicklung

---

## 📦 Installation

### Manuell

```
config/blueprints/automation/
```

---

### Direkt importieren

[![Open in Home Assistant](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https://raw.githubusercontent.com/rockbaer2007/ha-ultimate-timer-v4/main/blueprints/automation/ultimate_timer_v4.yaml)

---

## ⚙️ Konfiguration

| Feld | Beschreibung |
|------|------------|
| Start | Timer starten |
| Stop | Timer stoppen |
| Dauer | hh:mm:ss |
| Running | Aktiv |
| Done | Fertig |
| Start Time Helper | speichert Startzeit |
| Duration Helper | speichert Dauer |
| Reset | täglicher Reset |

---

## 🧠 Funktionsweise

1. Start → Timer läuft  
2. Running → EIN  
3. Countdown startet automatisch  
4. Stop → sofort AUS  
5. Ablauf → Done = EIN  
6. Reset → alles AUS  

---

## 🖥️ UI (Optional)

See UI setup:
👉 docs/UI_README_DE.md
👉 docs/UI_README_EN.md

## 🎥 Demo

![Demo](docs/demo.gif)

---

## 📸 Blueprint Konfiguration

![Blueprint](docs/preview_blueprint.png)

---

## 📸 Vorschau

| Idle | Running | Done |
|------|--------|------|
| ![Idle](docs/preview_idle.png) | ![Running](docs/preview_running.png) | ![Done](docs/preview_done.png) |

---

## 💡 Einsatz

- Teich / Pool Pumpen  
- Bewässerung  
- Watchdog  
- Verzögerungen  
- Countdown Anzeige  

---

## 📜 Lizenz

MIT Lizenz

---

## ⭐ Support

Wenn dir das Projekt gefällt, gib ihm ein ⭐
