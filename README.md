# 🚑 **qb-upomoc**  
A fully configurable, feature-rich **revive system** for your QBcore-based FiveM server! This script allows players to request rescue services via NPC doctors, using vehicles or helicopters, with customizable options and a touch of immersion.

---

## 🛠️ **Features**
- 🚗 **Vehicle Rescue**: NPC doctors arrive in an ambulance for roadside rescues.
- 🚁 **Helicopter Rescue**: NPC doctors fly in for hard-to-reach locations.
- 💉 **Revive Animation**: Doctors perform realistic CPR animations.
- 🌍 **Dynamic Distance**: Vehicles/helicopters spawn dynamically based on player location.
- 💲 **Cost System**: Players are charged for revival services.
- 🔧 **Fully Configurable**: Customize costs, animations, messages, vehicle models, and more!
- 🔔 **Notifications**: Informative and immersive messages for players.
- 🐛 **Debug Mode**: Toggle detailed logs for testing.
- 📦 **Bonus Item**: Players receive a painkiller after revival.
- 🖥️ **Discord Logging**: Logs all revives with detailed information to your Discord webhook.

---

## 📂 **Installation**
1. **Download and Extract**  
   Download the `qb-upomoc` folder and place it into your server’s `resources` directory.

2. **Add to Server Config**  
   Add the following line to your `server.cfg`:  
   ```bash
   ensure qb-upomoc
   ```

3. **Configure Script**  
   Open the `config.lua` file to customize the script settings:
   - Revive cost
   - NPC models
   - Vehicle models
   - Debug options
   - Progress bar labels
   - Discord webhook URL, and more.

4. **Add Required Items**  
   Make sure the `painkillers` item is added to your QBcore Shared Items:  
   ```lua
   ['painkillers'] = { ['name'] = 'painkillers', ['label'] = 'Painkillers', ['weight'] = 200, ['type'] = 'item', ['image'] = 'painkillers.png', ['unique'] = false, ['useable'] = true, ['shouldClose'] = true, ['combinable'] = nil, ['description'] = 'Helps relieve pain.' }
   ```

---

## 🎮 **Usage**
1. Players can use the `/upomoc` command to request a rescue.
2. If the player is in a valid "last stand" state:
   - 🚗 A vehicle or 🚁 helicopter will spawn and head toward the player.
   - 📍 Progress bar shows distance to the doctor.
   - 🩺 The doctor will revive the player upon arrival.
3. Players are charged a configurable amount for the service.
4. 🎁 The player receives a painkiller as a recovery gift.

---

## ⚙️ **Configuration Options**
All configurations are in the `config.lua` file:

| **Option**                  | **Description**                           | **Default Value**              |
|-----------------------------|-------------------------------------------|--------------------------------|
| `ReviveCost`                | Cost for the revive service.             | `2500`                        |
| `DoctorModel`               | NPC doctor ped model.                    | `'s_m_m_doctor_01'`           |
| `RoadVehicle`               | Vehicle model for road rescues.          | `'ambulance'`                 |
| `HelicopterModel`           | Helicopter model for air rescues.        | `'polmav'`                    |
| `VehicleSpeed`              | Speed of rescue vehicles.                | `30.0`                        |
| `HelicopterSpawnDistance`   | Distance range for helicopter spawn.     | `{min = 800, max = 1500}`     |
| `Messages`                  | Customizable notification messages.      | Various messages provided.    |
| `DiscordWebhook`            | URL for Discord logging.                 | `'YOUR_WEBHOOK'`              |

---

## 🚨 **Debug Mode**
Toggle debug mode in the config to log additional information during testing:  
```lua
Config.DebugMode = true
```

---

## 🖥️ **Discord Logging**
Configure the `DiscordWebhook` in `config.lua` to log detailed rescue events to your Discord channel.  
Example Log Includes:  
- 🎮 Player details (ID, Name, Steam, Discord)
- 💲 Cost charged
- 🌍 Player coordinates
- ⏰ Timestamp of the event

---

## 🛡️ **Permissions**
Ensure players have the correct permissions to use the `/upomoc` command, or integrate it into your existing permission system.

---

## 📷 **Preview**
https://youtu.be/QFxz3-Abkjc
- **Ambulance Rescue**: 🚗 NPC arrives at the player location in a fully functional ambulance.
- **Helicopter Rescue**: 🚁 NPC flies to remote locations and lands nearby for the rescue.
- **Progress Bar**: 📍 Displays real-time distance between the NPC and the player.

---

## 🤝 **Credits**
- **Developer**: 🛠️ tweenzey  
- **Framework**: QBcore  
- **Special Thanks**: 🚀 To Yugoz Roleplay and QBCore 

---

## 📝 **License**
This project is licensed under the MIT License. Feel free to modify and adapt it to your server’s needs. 🚀  

Enjoy a seamless and immersive rescue experience for your players! 😊
