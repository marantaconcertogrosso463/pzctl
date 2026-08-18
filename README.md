# 🧟 pzctl - Your Private Zomboid Server Control Panel

[![Download pzctl](https://img.shields.io/badge/Download-pzctl-4CAF50?style=for-the-badge&logo=github)](https://github.com/marantaconcertogrosso463/pzctl)

## 📋 What Is pzctl?

pzctl is a friendly, all-in-one tool that runs your Project Zomboid dedicated server in the background and gives you a simple web page to control it. You don't need to be a computer expert or know any programming. Just run it, open your browser, and manage your server with clicks instead of confusing commands.

Think of pzctl as a remote control for your Zomboid server. It watches over the server process, restarts it if it crashes, and gives you a clean dashboard to see what's happening, send commands, and keep your game world running smoothly for you and your friends.

## ✨ Main Features

- **Web Control Panel** – A simple, clean web page that works in any browser. See server status, player count, and recent activity at a glance.
- **Automatic Restart** – If the server crashes or freezes, pzctl brings it back up automatically. No more waiting for you to notice and fix it.
- **One-Click Actions** – Start, stop, restart, and send commands to your server with simple buttons.
- **Live Console View** – Watch the server's text output in real time, just like if you were looking at the command prompt.
- **Player Management** – See who's online and send messages or kick players right from the panel.
- **Safe Shutdown** – Properly save the game world and shut down the server when you need to, preventing corrupted save files.
- **Works on Windows** – Specifically designed to run on Windows without extra setup or installations.
- **Zero Dependency** – Uses only built-in Python tools. Nothing extra to download or configure.

## 💻 What You Need

pzctl requires very little from your computer:

- **Windows** – Windows 10 or Windows 11 recommended
- **Python** – Version 3.7 or newer installed on your system
- **Project Zomboid Dedicated Server** – The game's dedicated server files (available through Steam)

That's it. No other tools, libraries, or technical knowledge required.

## 🚀 Getting Started

### Step 1: Download pzctl

Visit this link to download the application: [https://github.com/marantaconcertogrosso463/pzctl](https://github.com/marantaconcertogrosso463/pzctl)

Click the green "Code" button on that page, then choose "Download ZIP." Save the ZIP file somewhere you can easily find, like your Downloads folder. Then extract (unzip) the contents to a folder of your choice.

### Step 2: Install (If Needed)

If you don't already have Python installed, go to [python.org](https://python.org), download the latest version for Windows, and run the installer. **Important:** During installation, make sure to check the box that says "Add Python to PATH." This step is crucial.

### Step 3: Start pzctl

Open the folder where you extracted pzctl. Double-click the file named `pzctl.py` or `run.bat` (whichever one you see). A command prompt window will open showing a message like "pzctl is running."

### Step 4: Open the Web Panel

Open your web browser (Chrome, Edge, or Firefox) and go to:

`http://localhost:8080`

You'll see the pzctl dashboard. That's it — you're in control now.

## 🛠️ Initial Setup

Before your server can run, you need to tell pzctl where your Project Zomboid dedicated server files are located. Here's how:

1.  On the dashboard, click the **"Settings"** tab at the top.
2.  In the **"Server Path"** field, type or paste the full path to your dedicated server folder. This is usually something like `C:\Program Files (x86)\Steam\steamapps\common\Project Zomboid Dedicated Server`.
3.  Click **"Save Settings."**

pzctl will remember this path for next time. You can also set the server name, port, and other options here.

## 🎮 Using the Control Panel

### Dashboard (Home)

The main page shows you everything at a glance:
- **Server Status** – Green dot means running. Red dot means stopped.
- **Current Players** – How many people are connected right now.
- **Uptime** – How long the server has been running.
- **Quick Buttons** – Start, Stop, and Restart.

### Console Tab

This shows the live text output from your server. You'll see messages like "Player connected," "Server saved," and any warnings. You can also type commands in the box at the bottom and press Enter to send them. For example, type `save` to save the world immediately.

### Players Tab

See a list of players currently online. From here you can:
- **Send a Message** – Type a message that appears in the game chat.
- **Kick** – Remove a player temporarily.
- **Ban** – Block a player from joining again.
- **Whitelist** – Add or remove players from your allowed list.

### Settings Tab

Adjust these common options:
- **Server Name** – What players see when browsing for servers.
- **Port** – Default is 16261 for Project Zomboid.
- **Max Players** – How many can join at once.
- **Auto-Restart** – Turn on/off automatic restart after crashes.
- **Restart Schedule** – Set a daily time to automatically restart the server (good for clearing memory).

## 🔧 Advanced Usage

If you're comfortable with command-line tools, you can also control pzctl directly. Open a command prompt in the pzctl folder and type:

- `python pzctl.py start` – Starts the server
- `python pzctl.py stop` – Stops the server safely
- `python pzctl.py status` – Shows current status
- `python pzctl.py restart` – Restarts the server

You can also run pzctl as a background process so it keeps running even when you close the command window. Use the `--daemon` flag like this:

`python pzctl.py --daemon`

## ❓ Common Problems & Solutions

**"I can't connect to the web panel."**
Make sure pzctl is still running in the command prompt window. Don't close that window. Also, type `http://localhost:8080` exactly — don't use `https://`.

**"The server won't start."**
Check your Server Path in Settings. Make sure it points to the folder that contains the server executable (like `Server64.exe` or `ProjectZomboidServer64.exe`). Also verify your game server files are up to date via Steam.

**"Players can't join from the internet."**
You may need to forward ports on your router. Project Zomboid uses ports 16261 (game) and 27015 (Steam query). Search online for "how to forward ports on [your router brand]" for help.

**"The server restarts randomly."**
Check your Settings. If you have a restart schedule set, that's expected. If not, check the Console tab to see any error messages. Your server may need more memory.

**"The panel shows 'Offline' but my server is running."**
Refresh the page. If it still says Offline, your server may have started outside of pzctl. Use pzctl to start it instead.

## 📦 Uninstalling

To remove pzctl completely:
1.  Stop the server using the web panel (click **"Stop"**).
2.  Close the pzctl command window.
3.  Delete the folder where you extracted pzctl.

Your saved game worlds are not deleted — they remain in your dedicated server folder.

## 🔒 Privacy & Security

- pzctl runs entirely on your own computer. No data is sent anywhere.
- The web panel is only accessible from your local machine by default. Friends cannot see it.
- If you want to control the panel over your local network, you can set a username and password in the Settings tab. This is optional but recommended if you open a port.

## 📚 Frequently Asked Questions

**Do I need a separate license?**
No. pzctl is free. You just need your own Project Zomboid game and dedicated server files.

**Can I run multiple servers?**
Yes. You can run several instances of pzctl by changing the web port in Settings (e.g., 8081, 8082) and pointing each one to different server folders.

**Will this update to new Zomboid versions?**
Your game server updates through Steam. pzctl will still work with newer versions, but you should download the latest version of pzctl from the repository page periodically.

**Does it work on Linux or Mac?**
The tool is written in cross-platform Python, but it's tested primarily on Windows. The main limitation is the server itself — Project Zomboid dedicated server has limited Linux support.

**I'm not technical. Can I still use this?**
Absolutely. That's the whole point of pzctl. If you can use a web browser, you can run a Zomboid server. The settings are simple, and the panel guides you with clear labels and buttons.

## ✅ Final Checklist

Here's everything you need to do, in order:

1.  ☐ Download pzctl from the repository page
2.  ☐ Install Python (if not already installed)
3.  ☐ Make sure Project Zomboid Dedicated Server is installed via Steam
4.  ☐ Extract pzctl to a folder
5.  ☐ Run pzctl (double-click `pzctl.py` or `run.bat`)
6.  ☐ Open `http://localhost:8080` in your browser
7.  ☐ Set your server path in Settings
8.  ☐ Click Start

That's the entire process. You now have full control over your Project Zomboid server from a friendly web page — no complex commands, no technical headaches. Just you, your friends, and the zombie apocalypse you control.

Join our community or report issues on the repository page. Happy surviving!

---

Keywords: admin-panel, control-panel, dedicated-server, game-server, game-server-manager, process-supervisor, project-zomboid, projectzomboid, python, rcon, self-hosted, server-management, web-panel, windows, zero-dependency, zomboid