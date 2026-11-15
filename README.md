# Even Keel

A small daily journal that runs in your phone's browser. Each day you rate four things from 1 to 4 and tick two more:

- **Diet**: how clean you ate
- **Sleep**: how rested you were
- **Fatigue**: how much malaise you felt
- **Mood**: self-esteem and general mood
- **Exercise**: none, home workout, cardio, or both
- **Piano**: practised or not

You can also list what you ate. Each entry is sent to Google's Gemini, which estimates its nutrients, and the day's totals are shown against your daily goals, along with the potassium to sodium ratio (target 2.5 : 1).

The Patterns tab shows streaks, the last four weeks at a glance, and which of your numbers tend to move together.

## Files

| File | What it is |
|---|---|
| `index.html` | The whole app: markup, styles and script in one file |
| `manifest.webmanifest` | Name, colours and icons used when the app is added to a phone's home screen |
| `icon-192.png`, `icon-512.png` | The home-screen icon |
| `README.md` | This page |

There is nothing to install or build.

## Put it online with GitHub Pages

1. Create a new **public** repository on GitHub.
2. Open **Add file → Upload files**, drag in every file from this folder, and commit.
3. Open **Settings → Pages**. Under **Build and deployment**, set **Source** to **Deploy from a branch**, pick the `main` branch and the `/ (root)` folder, and save.
4. After a minute or so the page is live at `https://<your-username>.github.io/<repository-name>/`.

## Use it on your phone

1. Open the address above in Chrome on Android.
2. Open Chrome's menu and choose **Add to Home screen**.
3. In the app, open the **Gemini** section at the bottom of the food log and paste an API key. Create one at <https://aistudio.google.com/apikey>.

The model name next to the key can be changed if Google retires the default one.

## Where your data lives

- Your journal is stored only in the browser you use, on that device. Nothing is sent to GitHub.
- The Gemini API key is stored in the same browser and is sent only to Google.
- What you type into the food log is sent to Google for analysis.
- The data is tied to the page's address. If you move the app to a different address, use **Download backup** and **Restore from backup** on the Patterns tab to carry it over.
- Clearing Chrome's site data erases the journal, so download a backup now and then. Backups never contain the API key.

## Daily goals

Each nutrient has a standard daily goal taken from the FDA Daily Values. Open **Daily goals** in the food log to set your own for any of them. Carbs, fat, saturated fat and added sugar follow your calorie goal unless you set them yourself.

Nutrient amounts are AI estimates from your description, not lab values.
