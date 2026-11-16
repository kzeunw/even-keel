# Even Keel

A small daily journal that runs in your phone's browser. Each day you rate four things from 1 to 4 and tick two more:

- **Diet**: how clean you ate
- **Sleep**: how rested you were
- **Energy**: from drained (1) to energetic (4)
- **Mood**: self-esteem and general mood
- **Exercise**: home workout, cardio, or both (leave it unselected for none)
- **Piano**: practised or not

You can also list what you ate. Each entry is sent to Google's Gemini, which estimates its nutrients, and the day's totals are shown against your daily goals, along with the potassium to sodium ratio (target 2.5 : 1). Tap any nutrient to see which foods it mainly came from that day. The pencil next to an entry puts its text back in the box so you can rewrite it.

Meals you eat often can be saved in the Settings tab. Each one shows as a button under the food box, and one tap adds it to the day. A saved meal is estimated the first time you add it and is instant after that.

The Patterns tab shows highlights (your logging streak, your best day, and this week's piano and exercise days against your weekly targets), the last two weeks at a glance, the nutrients you are often short on or over, and which of your numbers tend to move together.

A vitamin or mineral is listed as often short when it stays under 75% of its goal on at least half of the days with a full food log. Saturated fat, added sugar and sodium are listed when they go over their limit that often. Days with under half the calorie goal logged are left out.

The nutrient lists and the links between your numbers update once a day, at midnight, from the days before today. Entries you add during the day, including ones added to past days, show up there after the next midnight. The highlights and the two-week grid update straight away.

The best day is the one with the highest score: the average of the four ratings, plus 1 point for piano and 1 point for any exercise, out of 6.

The Settings tab holds the Gemini API key, your saved meals, your weekly targets for exercise and piano days (4 each to start with) and your daily nutrient goals.

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
3. In the app, open the **Settings** tab and paste an API key into the **Gemini** section. Create one at <https://aistudio.google.com/apikey>.

The model name next to the key can be changed if Google retires the default one.

## Where your data lives

- Your journal is stored only in the browser you use, on that device. Nothing is sent to GitHub.
- The Gemini API key is stored in the same browser and is sent only to Google.
- What you type into the food log is sent to Google for analysis.
- The data is tied to the page's address. If you move the app to a different address, use **Download backup** and **Restore from backup** on the Patterns tab to carry it over.
- Clearing Chrome's site data erases the journal, so download a backup now and then. Backups never contain the API key.

## Daily goals

Each nutrient has a standard daily goal taken from the FDA Daily Values. Open **Daily goals** in the Settings tab to set your own for any of them. Carbs, fat, saturated fat and added sugar follow your calorie goal unless you set them yourself.

Nutrient amounts are AI estimates from your description, not lab values.
