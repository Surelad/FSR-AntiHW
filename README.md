# FSR-AntiHW — Quick Start & Releases 🚀

FSR-AntiHW reads a passage you paste into the popup, looks at a multiple-choice question on the page, asks an AI which answer is best, then highlights & clicks that answer for you. Fast to install, easy to use.

## ⬇️ How to download

A. Download ZIP (easy)

Click Releases ➡️ Source Code zip

Unzip somewhere on your PC.

B. Git clone (for devs)

git clone https://github.com/<Surelad>/fsr-antihw.git
cd fsr-antihw

## 🧩 Load unpacked into Chrome (2 minutes)

Open Chrome and go to chrome://extensions/.

Toggle Developer mode (top-right).

Click Load unpacked.

Select the unzipped fsr-antihw folder (the folder containing manifest.json).

You should now see FSR-AntiHW in your extensions list.

## ⚙️ First use — simple steps

Click the extension icon (top-right) → popup opens.

Paste the passage (text/story) into the textarea.

Click 💾 Save Passage (you’ll see ✅ Passage saved!).

Open the page with the multiple-choice questions.

Click 👁️ Show Answer in the popup → the script runs on the active tab and will highlight & click the AI’s chosen answer.

It will attempt several questions before stopping.

## 🛠 Troubleshooting

Nothing happens? Make sure you saved the passage first.

Not finding answers? Site HTML might be different; the script looks for typical h2 div and <button> elements. Custom sites may need small tweaks.

Debug: Right-click → Inspect → Console and look for [Matcher AI] logs.

⚠️ Cohere API — rate limits & exhausted keys

This release may include a public/embedded key or rely on a shared key. Keys have limited uses.

If the extension suddenly stops working it may be because the embedded Cohere key ran out or got rate-limited.

Where to check for a new working build / key:

r/fucksparx (Reddit)

r/fucksparxreader (Reddit)

Releases on this GitHub repo (check the Releases tab)

If you can’t get it working from a release, search those subreddits for the newest build or instructions.

## 🔒 Privacy & security notes (read this)

Do not paste sensitive info into the passage — the text is sent to the AI service.

The shipped build may use obfuscation to hide keys from casual file viewing — this is not secure. A determined person can extract keys.

Best practice: run your own backend and store the API key in an environment variable (env). Point content.js to your endpoint. This is the only real way to protect your key long-term.

## 🧰 Want privacy or reliability?

Deploy a tiny server (Cloudflare Worker, Vercel, Render) and save COHERE_KEY as an env var.

Change content.js to POST to your server instead of Cohere directly.

This avoids shared key exhaustion and keeps control with you.

## ❤️ Contributing & support

Found a bug or a site the extension doesn’t work on? Open an issue or submit a PR.

For the latest builds or keys: check GitHub Releases, r/fucksparx, or r/fucksparxreader.
Need the latest release or a replacement key? Check the repo Releases page or our Discord.

