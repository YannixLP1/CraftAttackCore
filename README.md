# CraftAttackSpawn 🚀

**CraftAttackSpawn** ist ein leichtgewichtiges, aber umfangreiches Minecraft-Plugin (Paper/Spigot), das klassische Features aus bekannten CraftAttack-Projekten auf deinen Server bringt.

---

## 📋 Features

* **Elytra Boost System:** Ermöglicht Raketen-Boosts beim Fliegen mit konfigurierbarer Stärke und temporärem Fallschaden-Schutz.
* **Status-System:** Spieler können ihren eigenen Status im Chat und in der Tabliste anzeigen lassen (`/status`).
* **Custom Rezepte:**
  * **Unsichtbare Item Frames:** Crafting-Rezept für unsichtbare Rahmen.
  * **Spielerköpfe:** Crafting-Rezept für den eigenen Kopf.
* **Schutzbereiche (Areas):** Lege geschützte Zonen fest, in denen nur Administratoren oder Spieler mit Bypass-Rechten bauen können.
* **Multiplayer Sleep:** Anpassbarer Prozentsatz an Schläfern, die benötigt werden, um die Nacht zu überspringen (standardmäßig ca. 33%).

---

## ⚙️ Befehle & Rechte

### Befehle

| Befehl | Beschreibung | Syntax |
| :--- | :--- | :--- |
| `/ca` | Hauptbefehl zur Verwaltung des Plugins | `/ca info` |
| `/status` | Setzt oder löscht deinen Chat-/Tab-Status | `/status <Text> <Farbe>` \| `/status clear` |
| `/kopf` | Zeigt das Rezept für deinen Spielerkopf | `/kopf` |
| `/itemframe` | Zeigt das Rezept für unsichtbare Item Frames | `/itemframe` |

### Ingame-Rezeptverwaltung
* `/ca recipe itemframe` – Rezept für unsichtbare Item Frames im Spiel bearbeiten
* `/ca recipe kopf` – Rezept für Spielerköpfe im Spiel bearbeiten

### Berechtigungen (Permissions)

* `craftattack.admin`: Voller Zugriff auf die Verwaltung von Areas und Todeszahlen *(Standard: OP)*
* `craftattack.bypass`: Erlaubt das Bauen innerhalb geschützter Areas *(Standard: OP)*

---

## 🔧 Konfiguration (`config.yml`)

```yaml
settings:
  status-max-length: 16
  boosts-per-flight: 2
  boost-strength: 1.6
  no-fall-damage-seconds: 3
  # Prozentsatz der Spieler, die schlafen müssen (0.34 = ca. 1/3)
  sleep-required-fraction: 0.34

crafting:
  itemframe-enabled: true
  head-enabled: true

area:
  world: ""
  pos1: {}
  pos2: {}

players: {}
recipes: {}
