# 🌙 Nightreign Relic Editor

A powerful and user-friendly save editor for **Nightreign**, focused on full control over **Relics**, save data, and character progression for PC/PS4.



---

## ✨ Features

### 🔧 Relic Management
- Edit existing Relics  
- Replace Relics  
- Modify Relic effect IDs and values  
- Delete Relics  
- Export & import Relics via **Excel**  
- One-click fix illegal Relics if fixable 

### 💎 Save Editing
- Edit **Murks** and **Sigs**
- Import full save files or individual characters
- Improved **illegal relic detection**
- Multi-language support

### 🛡️ Automatic Backup System
To ensure data safety, the editor performs an automatic backup every time a save file is opened.

* **Cycle Backups**: The system automatically stores backups in the `/backup` folder within the application directory. It maintains the **5 most recent versions** on a rolling basis.
* **Root Backup (Protected)**: 
    * The system creates a one-time **"Root" backup** that will never be overwritten.
    * **For new users**: This serves as a permanent copy of your "Pure" (unmodified) save.
    * **For existing users**: This acts as a "Last Resort" recovery point to prevent permanent save corruption.

### ⚙️ Vessel and Preset Management

* **Relic Configuration**: Customize and edit Relic combinations for both Vessels and Presets.
* **Save as Preset**: Quickly save your current Vessel configuration as a Preset.
* **Loadout Export**: Export the specific loadout of a selected character for backup or sharing.
* **Selective Loadout Import**: Import specific loadouts with a flexible selection tool.
* **Safe Relic Auto-Addition**: When importing a loadout containing Relics not present in your save, the system will automatically add them (excluding **Unique Relics**).
* **Vessel Unlock Detection**: Automatically detects the unlock status of various Vessels.
    > **Note**: Character unlock parsing is currently a work in progress. By default, the initial Vessels for all characters are marked as "Unlocked."

#### 🔍 Definition: Unique Relics
To **avoid violation detection**, the system will not auto-generate **Unique Relics**. These are defined as:
* Relics obtained by **defeating Bosses**.
* Relics purchased from the **'Small Jar Bazaar'** or the **'Collector Signboard'**.

#### ⚠️ Important Usage Notes
* **Deep Mode & Deep Relics**: There is currently no complete detection mechanism for Deep Mode/Deep Relic unlock status. 
* **Recommendation**: It is highly recommended to **manually unlock Deep Mode in-game** before importing other players' loadouts to ensure compatibility.
---

## 💻 Running Editor manually

1. Install [uv](https://docs.astral.sh/uv/getting-started/installation)
2. Clone the repo with: `git clone https://github.com/alfizari/Elden-Ring-Nightreign-Save-Editor`
3. Run the editor with: `uv run src/Final.py`

## 🖥️ How to Use

### PC (Steam / Seamless Co-op)

#### Windows
1. Locate your save file:
   ```text
   C:\Users\%YourUsername%\AppData\Roaming\Nightreign\<User-ID>\
   NR0000.sl2
   ```
2. If using Seamless Co-op, ensure the save file name is NR0000.sl2.
3. Open the save file using the editor.
4. Edit the data as desired.
5. Save the changes and replace the original file.

#### macOS
1. Locate your save file:
   ```bash
   ~/Library/Application Support/Nightreign/<User-ID>/
   NR0000.sl2
   ```
2. If using Seamless Co-op, ensure the save file name is NR0000.sl2.
3. Open the save file using the editor.
4. Edit the data as desired.
5. Save the changes and replace the original file.

#### Linux
1. Locate your save file (check both common locations):
   ```bash
   ~/.config/Nightreign/<User-ID>/
   # or
   ~/.local/share/Nightreign/<User-ID>/
   ```
   or follow Proton prefix path if using Proton
2. If using Seamless Co-op, ensure the save file name is NR0000.sl2.
3. Open the save file using the editor.
4. Edit the data as desired.
5. Save the changes and replace the original file.

### PS4/PS5 (PS4 Version)
1. Decrypt your save file
   (see the YouTube decryption guide).
2. Open memory.dat with the editor.
3. Edit and save your changes.
4. Re-encrypt the modified data.
5. Transfer the save back to your console.



---
## 📥 Download

You can download the latest builds from the releases page:

🔗 https://github.com/alfizari/Elden-Ring-Nightreign-Save-Editor/releases


---

## 🧩 Requirements

### Platform Support
- **Windows** - Fully supported
- **macOS** - Fully supported (Intel & Apple Silicon)
- **Linux** - Fully supported (any distribution with Python 3.12+)

### Python
- **Python 3.12 or newer**

### Dependencies
The following Python packages are required:

```text
cryptography >= 46.0.3
lxml >= 6.0.2
openpyxl >= 3.1.5
orjson >= 3.11.5
pandas >= 2.3.3
pillow>=12.1.0
```
```bash
pip install cryptography lxml openpyxl orjson pandas pillow
```
or sync with [uv](https://docs.astral.sh/uv/getting-started/installation)

```bash
uv sync
```


---

## ⚠️ Disclaimer
- Always **backup your save files** before editing.
- Improper edits may cause save corruption.
- Using modified saves online may result in bans.
- Use this tool **at your own risk**.

---

## 🤝 Contributors

| Name | Contribution |
|------|--------------|
|    [ip1259](https://github.com/ip1259)  | Maintainer/Illegal relic detection/Multi Languge Support             |
|   [Vanesro](https://github.com/Vanesro)   | Illegal Relic Detection Improvments/Bug Fixes             |
|   [thewerthon](https://github.com/thewerthon)   |Relics and Effect list/QoL improvement              |
|   [msurkein](https://github.com/msurkein)   |Export Relic/QoL improvement              |
|   [nacitar](https://github.com/nacitar)   |Relic List             |

Thanks to everyone who contributed.



---

## 🤝 How to Contribute
Contributions are welcome and appreciated!

You can help by:
- Adding Relic IDs
- Adding Effect IDs
- Improving illegal relic detection
- Adding translations
- Improving documentation

Feel free to submit a pull request or share data via the project page.

---

## 📌 Notes
This project is actively developed.  
Feedback, bug reports, and suggestions are welcome.
