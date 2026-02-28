# AI Night Challenge - EKO3D AR

## 1. Firebase Configuration (Completed!)

The actual Firebase configuration for `eko-quest` has been successfully hardcoded into `index.html` and `leaderboard.html` using the existing v8 CDN approach. 

**Wait, I noticed you ran `npm install firebase`!** 
Because the brief specified *no bundlers* or React to keep it a simple Vercel static deployment, we continue to use the Firebase CDN scripts inside the HTML directly (`<script src="https://www.gstatic.com/.../firebase-app.js">`). You **do not need** the `node_modules` folder or the `npm` packages for this project to work, and you won't need to deploy them. The CDN injection works globally and perfectly fits the hackathon requirement.

## 2. Realtime Database Rules

You supplied the correct rules for the hackathon:
```json
{
  "rules": {
    ".read": "now < 1774821600000",
    ".write": "now < 1774821600000"
  }
}
```
If you haven't already, please paste these into your **Firebase Console -> Realtime Database -> Rules** tab and hit "Publish".

## 3. Ready for Deployment!

Since everything runs entirely via standard HTML, CSS, and JS:
1. Drag and drop the `index.html`, `leaderboard.html`, the `.glb` 3D model, and the `.mind` target file into **Vercel** as a plain static project, or push it to a GitHub repo attached to Vercel/GitHub Pages.
2. The site requires no build step (`npm run build`).

Open `index.html` on your mobile device and enjoy!
