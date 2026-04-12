# ⏱️ Ultimate Timer V4

[![Open in Home Assistant](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https://raw.githubusercontent.com/rockbaer2007/ha-ultimate-timer-blueprint/main/blueprints/automation/ultimate_timer_v3_2_4.yaml)

![GitHub release](https://img.shields.io/github/v/release/rockbaer2007/ha-ultimate-timer-blueprint)
![GitHub stars](https://img.shields.io/github/stars/rockbaer2007/ha-ultimate-timer-blueprint?style=social)
![HACS](https://img.shields.io/badge/HACS-Custom-blue)

🇩🇪 [German Version](README_de.md)

> A powerful hybrid timer blueprint for Home Assistant with reliable STOP handling, persistent DONE state and MQTT support.

---

## 🚀 Features

- ⏱️ Timer with `hh:mm:ss` format  
- ▶️ Start trigger (button behavior)  
- ⏹️ Reliable stop trigger (instant OFF)  
- 📡 Running state indicator  
- 🎯 Done state (persistent until reset)  
- 🌙 Daily reset time  
- 🔁 Multi-instance safe  
- 🔀 Hybrid mode (Helper or MQTT)  
- 🛡️ No race conditions  

---

## 🔄 Upgrade Notice

### V3.2 → V3.2.4 FINAL CLEAN

- Fixed RUNNING state issues  
- Fixed STOP reliability  
- DONE now stays ON until reset  

👉 Strongly recommended to update

---

## 📦 Installation

### Option 1: Manual

Copy to:

```
config/blueprints/automation/
```

---

### Option 2: Import

[![Open in Home Assistant](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https://raw.githubusercontent.com/rockbaer2007/ha-ultimate-timer-blueprint/main/blueprints/automation/ultimate_timer_v3_2_4.yaml)

---

## ⚙️ Configuration

| Field | Description |
|------|------------|
| Start Trigger | Starts timer |
| Stop Trigger | Stops timer |
| Duration | hh:mm:ss |
| Running | Active state |
| Done | Finished state |
| Reset Time | Daily reset |

---

## 🧠 How It Works

1. Start → Timer starts  
2. Running → ON  
3. Stop → Running OFF immediately  
4. Timeout → Done = ON  
5. Reset → everything OFF  

---
## 📸 Blueprint Configuration

![Blueprint](docs/preview_blueprint.png)

## 🎥 Demo

![Demo](docs/demo.gif)

## 📸 Preview

| Idle | Running | Done |
|------|--------|------|
| ![Idle](docs/preview_idle1.png) | ![Running](docs/preview_runing1.png) | ![Done](docs/preview_done1.png) |
| ![Idle](docs/preview_idle2.png) | ![Running](docs/preview_runing2.png) | ![Done](docs/preview_done2.png) |
---

## 💡 Use Cases

- Pump runtime limiter  
- Irrigation  
- Watchdog automation  
- Delayed shutdown  

---

## 📜 License

MIT License

---

## ⭐ Support

If you like this project, give it a star ⭐
