# Perio Supervisor App

The doctor's side of the digital **periodontal case sheet** at the **College of Dentistry, University of Karbala**. Scan a student's case, run the timer, score it, sign it with your own signature, and hand the verified score back to the student. Several doctors can hand over running cases to each other and sync their graded cases. No internet needed after the first load.

> Works together with the **Perio Case Sheet — Student** app.

**Open the app:** [`https://UOK-dentistry-college.github.io/perio-case-sheet-doctor/`](https://UOK-dentistry-college.github.io/perio-case-sheet-doctor/)

---

## Install it on your phone (works offline afterwards)

**iPhone / iPad (Safari only)**
1. Open the link above in **Safari**.
2. Tap **Share** → **Add to Home Screen** → **Add**.
3. Always open the app from the **home-screen icon**.

> **iPhone note:** Safari and the home-screen icon keep their data separately. Install first, **then** enter your cases. Anything entered in a Safari tab will not appear in the installed app.

**Android (Chrome)**
1. Open the link in Chrome.
2. Tap the menu **⋮** → **Install app** (or **Add to Home screen**).
or
**Android (the app)**
1. Go to [`realeses`](https://github.com/UOK-dentistry-college/perio-case-sheet-doctor/releases), and download the lataest APK version.
2. after the download is completed open the APK file and install it.

**Computer (the app)**
1. Go to [`realeses`](https://github.com/UOK-dentistry-college/perio-case-sheet-doctor/releases), and download the lataest EXE version.
2. after the download is completed open the EXE file and install it.
---

## First time: create your account

**Account** tab → **Create account**: enter your name, draw your **signature**, and finish. Your account gets a **Key ID**. Every score you share is **signed** with it, so students and other doctors can verify it came from you. Several doctors can have accounts on one phone; the signed-in doctor is shown at the top.

---

## Grading a case

1. **Cases** tab → **Scan student QR**. The case appears in your list.
2. Tap **Start timer**. Use **Stop / Resume**, or **Stop all timers / Resume all** for every running case at once.
3. Tap **Grade** and enter the scores: case sheet /10, motivation + instruction /10, indices /20, diagnosis /20, evaluation /40, infection control and behavior /5, plus the calculus score. Optionally tick **Apply penalty** (a number of points per minute over the time limit).
4. **Save**, or **Save & share** to show the **score QR** for the student to scan.
5. **Share** shows the score QR again at any time. **Edit score** changes a case **you** graded.

The doctor who grades a case is the one whose signature is on it.

---

## Several doctors working together

### Transfer ongoing cases (if a doctor has to leave)
- **Transfer cases** → select the ongoing cases (or **Select all**) → **Transfer selected**.
- A QR appears. If there are many cases it changes by itself between several QR codes.
- The colleague taps **Receive cases** → **Open camera** and keeps it on your screen until it says it is done. Pasting the code also works.
- **Timers keep counting** (they do not reset), and a case you had stopped stays stopped.
- Transferred cases are **locked** on your phone and delete themselves after **10 minutes**, or delete them manually. **Show QR again** is available until then.
- The student simply goes to the substitute doctor, who grades and signs.
- Both phones need the correct automatic date and time, because timers use the phone clock.

### Sync graded cases (so everyone's totals are right)
- **Sync graded cases** → **Send by QR** (choose date, group, and *only me / all doctors*) or **Send file**.
- The other doctor uses **Receive by QR** (camera stays open while the QR codes change) or **Receive file** (both doctors use the same password for files).
- After receiving, a list shows only the **new cases you did not have**. Tick the ones you want and tap **Add selected**.
- No duplicates. Each case keeps the doctor who graded it. Cases graded by another doctor are **read-only** for you.
- Only **graded** cases sync. Ongoing cases can only be transferred.
- Do it both ways so both doctors end up with everything.

---

## Reports and organizing

- **Grades PDF**: pick a **date** (today by default), a **group**, and which doctors, then **Export PDF** for a neat landscape table to copy grades by hand. Leave **Bundle these cases after export** ticked to save them as a bundle named like *Group F · 24/10/2026*.
- **Bundles** tab: open, rename or delete bundles.
- **Students** tab: every student's cases and scores, and a score report PDF.
- **Backup** tab: **Export backup** and **Restore**. Backups are **encrypted with a password you choose. It cannot be recovered**, so keep it safe.

---

## Privacy and responsibility

- Everything is stored **only on your device**. Nothing is uploaded.
- Cases contain **patient information**. Keep your phone locked and keep backups and PDFs private.
- Clearing browser data or deleting the app **deletes your cases and account**, so back up regularly.
- A training and documentation tool for the college, **not** a certified medical record system.

## For developers

A single static `index.html` with all libraries inlined.

| File | Purpose |
|---|---|
| `index.html` | The whole app |
| `manifest.json` | Install name, icons, colors |
| `sw.js` | Offline cache. Change `VERSION` each time you upload a new `index.html` |
| `icons/` | App icons |

**Host on GitHub Pages:** push the files to the repository root → *Settings → Pages → Deploy from a branch → `main` / `(root)`*. HTTPS is required for the camera and for installing.

## License

MIT License. © 2026 Karrar Abdul Manaf Asker and the College of Dentistry, University of Karbala. See [`LICENSE`](LICENSE).
