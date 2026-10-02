# RTFT Team Rewards

Live reward tracker for the Right the First Time team. Hosted on Vercel, data saved in a Google Sheet.

## Files
- `index.html` - the page (this is what Vercel hosts)
- `Code.gs` - Google Sheet backend (paste into Apps Script, NOT part of the website)

## Setup (one time, about 10 minutes)

### 1. Google Sheet backend
1. Go to sheets.new and name the sheet **RTFT Team Rewards**.
2. Extensions > Apps Script. Delete everything, paste all of `Code.gs`, click Save.
3. In the toolbar dropdown pick **setup**, click **Run**, then allow access (Advanced > Go to project > Allow).
4. Deploy > New deployment > gear icon > **Web app**.
   - Execute as: **Me**
   - Who has access: **Anyone**
   - Click Deploy and copy the **Web app URL** (starts with https://script.google.com/macros/s/...).
5. Open `index.html`, find `PASTE_YOUR_WEB_APP_URL_HERE` near the top of the script, and replace it with that URL.

### 2. GitHub
1. github.com > New repository > name it `rtft-rewards` > Create.
2. Click **uploading an existing file**, drag in `index.html` and `README.md` (leave `Code.gs` out), then Commit.

### 3. Vercel
1. vercel.com > Add New > Project > Import the `rtft-rewards` repo.
2. Framework preset: **Other**. Leave everything else default. Click Deploy.
3. Share the `.vercel.app` link with the team.

## Day to day
- Anyone with the link can enter revenue, edit rewards, add ideas, and vote. No logins.
- Every change lands in the Google Sheet. You can also edit numbers straight in the sheet.
- The page refreshes every 20 seconds.
- To change the page later, edit `index.html` on GitHub and Vercel redeploys on its own.
- If you edit `Code.gs`, use Deploy > Manage deployments > Edit > New version so the URL stays the same.
