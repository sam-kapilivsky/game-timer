# Game Timer: put it on your phone with GitHub Pages

A tap-to-reset countdown timer for card games. These files make it an installable web app (a PWA) that works offline once it has loaded one time.

## What is in this folder

| File | What it does |
|---|---|
| `index.html` | The timer itself |
| `manifest.webmanifest` | Tells the phone the app's name, icon and full-screen mode |
| `sw.js` | Saves the files on the phone so it works with no signal |
| `icons/` | The app icons |

`index.html` must sit at the top level of your GitHub repository, not inside a subfolder.

## Part 1: Publish it with GitHub Pages (free)

1. Create a free account at github.com if you do not have one.
2. Click **+** (top right) > **New repository**.
   - Name it something simple, like `game-timer`.
   - Set it to **Public**. (Free GitHub Pages hosting works with public repositories. Pages for private repositories is limited to paid plans, so check GitHub's current rules if you want private.)
   - Tick **Add a README file**, then **Create repository**.
3. In the new repository click **Add file** > **Upload files**.
4. Unzip this folder on your computer first. Drag in **the contents**: `index.html`, `manifest.webmanifest`, `sw.js` and the `icons` folder. Do not drag in the zip file or a parent folder. (If your browser will not take the `icons` folder, upload the four PNG files in a second step and type `icons/` before each file name, or use GitHub Desktop.)
5. Scroll down and click **Commit changes**.
6. Go to **Settings** > **Pages** (left sidebar).
7. Under **Build and deployment**, set **Source** to **Deploy from a branch**. Set **Branch** to `main` and the folder to `/ (root)`. Click **Save**.
8. Wait one to two minutes, then reload that Settings > Pages screen. It will show your address:

   `https://YOUR-USERNAME.github.io/game-timer/`

   Open it on your phone to check that it loads.

## Part 2: Install it on your phone

**iPhone or iPad:** open the address in **Safari** (not Chrome). Tap the **Share** button, then **Add to Home Screen**, then **Add**. It opens full screen with no browser bar.

**Android:** open the address in **Chrome**. Tap the **menu (three dots)** and choose **Install app** (or **Add to Home screen**).

Open it once while you have a connection. After that it works offline.

## Part 3: Set up the phone for game night

- **Screen stays on.** The app asks the phone to keep the screen on while it is open. If your phone still sleeps, set Auto-Lock to **Never** (iPhone: Settings > Display & Brightness) or turn on **Stay awake** while charging (Android developer options).
- **Sound.** On iPhone, the ring/silent switch may mute the buzzer and ticks. Check it before the game and turn the volume up.
- **No stray touches.** On iPhone, turn on **Guided Access** (Settings > Accessibility). Triple-click the side button to start it, which stops swipes from leaving the app.
- **Charging.** Plug the phone in for the game, then unplug it afterwards. Leaving an old phone on a charger at 100% for months can swell the battery.

## How the timer works

- Tap the red center button to start. Tap it again to reset and restart.
- Hold the center button for one second to stop and go back to ready.
- Press and hold the gear (top left) for one second to set the time.
- The button fades from green to red as time runs out. The ticking in the last 10 seconds and the buzz at zero need the sound on.

## Updating the app later

1. Change the files on GitHub (open a file, click the pencil, edit, commit; or upload the new version over the old one).
2. **Also open `sw.js` and change `game-timer-v1` to `game-timer-v2`** (then v3 and so on). If you skip this step, phones keep showing the old saved version.
3. On the phone, open the app twice (the first open fetches the update, the second shows it). If it still looks old, remove the app from the home screen and install it again.

## Troubleshooting

| Problem | Fix |
|---|---|
| Page shows 404 | `index.html` is not at the top level of the repository, or Pages is not switched on yet. Wait a couple of minutes and recheck Settings > Pages. |
| No "Install" option on Android | Use Chrome, make sure the address starts with `https://`, and load the page once fully. |
| The icon is missing on the home screen | Upload the `icons` folder again and check that the file names match. |
| The app opens in a browser, not full screen | On iPhone, use Safari for Add to Home Screen. Remove the old shortcut and add it again. |
| No sound | iPhone silent switch, or volume down. Tap the button once first, since phones block sound until you touch the screen. |
