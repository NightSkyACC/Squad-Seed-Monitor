# SquadSeed Monitor

A Python-based Windows desktop application designed to completely automate the process of populating Squad servers. Instead of sitting at your PC waiting for a server to seed, this tool applies low-resource settings, launches the game, mutes the menu audio, connects to the server, and automatically triggers a system action (like closing the game or shutting down your PC) once the target population is reached. 

Originally built for the 20R Gaming community.

## 🚀 Features
* **1-Click Auto-Seed Sequence:** Automatically backs up your graphics settings, applies ultra-low seeding configs, launches Squad, mutes the main menu audio, and joins the server.
* **Seeding Optimization:** Choose custom resolutions and FPS limits (down to 5 FPS) to free up almost all of your PC's resources while AFK seeding. 
* **Auto-Restore Settings:** The exact second the app closes or kills the game, your original high-quality graphics settings are instantly restored behind the scenes.
* **Smart Config Search:** Automatically tracks down your hidden `GameUserSettings.ini` file, regardless of what drive you installed the game on.
* **Live Monitoring:** Polls the BattleMetrics API every 60 seconds to check current server population.
* **Automated System Actions:** Choose to "Do Nothing", "Kill Process" (closes SquadGame), or "Shutdown PC" when the target population threshold is hit.

## 📥 For Regular Users (No Code Required)
If you just want to use the tool, you don't need to install Python or know how to code. 
1. Go to the **[Releases](../../releases)** page on the right side of this repository.
2. Download the latest `Squad seed monitor.exe` file (V2.0.0 or newer).
3. Run the program, select your target FPS, and click the big green **1-Click Auto-Seed** button!

## 💻 For Developers & Server Admins
If you want to run the raw Python code or configure this tool for your own community's server, follow these steps:

**Requirements:**
* Python 3.x
* Windows OS (Required for `pycaw` audio muting and `ctypes` UI scaling)
* `requests` library
* `pycaw` library
* `pyinstaller` (If you want to compile your own `.exe`)

**Installation & Building:**
1. Clone this repository:
   ```bash
   git clone [https://github.com/NightSkyACC/squad-seed-monitor.git](https://github.com/NightSkyACC/squad-seed-monitor.git)


**Installation:**
1. Clone this repository:
   `git clone https://github.com/NightSkyACC/squad-seed-monitor.git`
2. Install the required dependency:
   `pip install -r requirements.txt`
3. Run the script:
   `python "Squad seed monitor.py"`
4. To compile your own .exe (ensure 20r_logo.ico/YOUR_LOGO is in the same folder):
 `python -m PyInstaller --clean --onefile --windowed --icon="20r_logo.ico" ".\squad_seed_monitor"`

**Customizing for Your Server:**
Open the Python file and edit the variables at the top of the script to match your community:
* `API_URL`: Replace with your server's BattleMetrics API link.
* `JOIN_URL`: Replace with your community's direct connect link.
* `DISCORD_URL`:: Replace with your community Discord invite.
* `TARGET_PLAYERS`: Change the default threshold.

## Screenshot of the program
<img width="542" height="682" alt="image" src="https://github.com/user-attachments/assets/aa2221fd-1b80-42e6-b580-2d346d716a6b" />
 <img width="542" height="702" alt="image" src="https://github.com/user-attachments/assets/86b65744-985a-443e-95f3-7ac3b360bbfd" />



