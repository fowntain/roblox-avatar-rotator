# Roblox Avatar Rotator
A lightweight system tray application that automatically rotates your Roblox avatar between preset outfits, to create the effect that your avatar changes every time you reload.

## Features
* **Stays in the background:** Runs silently in the system tray.
* **Easy use:** You can create outfits in the Roblox avatar creator to cycle through.
* **Custom Intervals:** You can set the rotation speed.
* **Minimal Resources:** Uses less than 40MB of RAM and virtually 0% CPU (could be optimized but I wrote ts in python).
* **Logging:** Built in logging for troubleshooting API requests.

---
## Installation
Choose one of the following methods to install and run the application.

### Executable (Recommended)
1. Go to the <a href="https://github.com/fowntain/roblox-avatar-rotator/releases/latest">**Releases**</a>.
2. Download `RobloxRotator.zip`.
3. Extract the contents to a folder.
4. Run `RobloxRotator.exe`.

> [!NOTE]
> *Since this app isn't digitally signed, Windows Defender or other antivirus software may flag it. You might have to whitelist the application or select "Run Anyway" to proceed. All the code is open-source, so you may look through it or compile it yourself.*


### Build from Source (Advanced)
1. Install [Python](https://www.python.org/downloads/).
2. Clone or download this repository.
3. Open a terminal in the `src` folder.
4. Install the required dependencies:
```bash
pip install -r requirements.txt
```

5. Compile the application:
```bash
pyinstaller --noconsole --onefile --name "RobloxRotator" --hidden-import=winotify --hidden-import=pystray main.pyw
```
6. The executable will be generated in the `dist` folder.


### Run as Python Script (Developer)
1. Install [Python](https://www.python.org/downloads/).
2. Clone or download this repository.
3. Open a terminal in the `src` folder.
4. Install dependencies:
```bash
pip install -r requirements.txt

```
5. Run the script:
```bash
pythonw main.pyw

```



## Configuration

1. **Launch the Application:** A tray icon will appear in your taskbar (system tray).
2. **Open Settings:** Right-click the tray icon and select **Settings**.
3. **Authentication:** Paste your `.ROBLOSECURITY` cookie into the field.
4. **Select Outfits:** Click **Fetch My Outfits**, wait for the list to load, and select the outfits you wish to rotate.
5. **Save:** Click **Save & Close**.
6. **Start:** Right-click the tray icon and select **Start**.

## Security Warning
>[!WARNING]
>This application requires your `.ROBLOSECURITY` cookie to function. This cookie grants full access to your Roblox account.
>* **Never share your cookie** with anyone.
>* This application stores your configuration locally in a `config.json` file on your computer, so do NOT open this file when others can see your screen.
>* The source code is provided in this repository for full transparency. You are encouraged to review `src/main.pyw` to ensure it is safe before use.
