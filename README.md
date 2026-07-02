# SquadSeed Monitor

A Python-based desktop application designed to help populate Squad servers. Instead of sitting at your PC waiting for a server to seed, this tool monitors the player count via the BattleMetrics API and automatically triggers a system action (like closing the game or shutting down your PC) once the target population is reached.

Originally built for the 20R Gaming community.

## 🚀 Features
* **Live Monitoring:** Polls the BattleMetrics API every 60 seconds to check current server population.
* **Automated System Actions:** Choose to "Do Nothing", "Kill Process" (closes SquadGame.exe), or "Shutdown PC" when the target is hit.
* **Clean UI:** Built with Tkinter for a lightweight, easy-to-read dashboard without needing to use the command line.

## 📥 For Regular Users (No Code Required)
If you just want to use the tool, you don't need to install Python. 
1. Go to the **[Releases](../../releases)** page on the right side of this repository.
2. Download the latest `Squad seed monitor.exe` file.
3. Run the program and select your desired action!

## 💻 For Developers & Server Admins
If you want to run the raw Python code or configure this tool for your own community's server, follow these steps:

**Requirements:**
* Python 3.x
* `requests` library

**Installation:**
1. Clone this repository:
   `git clone https://github.com/YOUR-USERNAME/squad-seed-monitor.git`
2. Install the required dependency:
   `pip install -r requirements.txt`
3. Run the script:
   `python "Squad seed monitor.py"`

**Customizing for Your Server:**
Open the Python file and edit the variables at the top of the script to match your community:
* `API_URL`: Replace with your server's BattleMetrics API link.
* `JOIN_URL`: Replace with your community's direct connect link.
* `TARGET_PLAYERS`: Change the default threshold.
