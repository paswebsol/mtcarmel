# Mt. Carmel Assembly Attendance Management — GitHub Pages / Installable App

This package is prepared for static hosting on GitHub Pages. It includes the app, PWA install metadata, app icons, and an offline service worker. It can be opened on Android, iPhone/iPad, Windows, macOS, Linux, and Chromebook using a supported browser.

## Publish it on GitHub Pages

1. Sign in to GitHub and create a **new public repository** (for example, `mt-carmel-attendance`).
2. Open the repository and choose **Add file → Upload files**.
3. Extract this ZIP on your computer. Upload the **contents** of the `mt-carmel-attendance-github` folder—not the folder itself. `index.html`, `manifest.webmanifest`, `sw.js`, `.nojekyll`, and the icon files must be at the repository root.
4. Commit the uploaded files to the `main` branch.
5. Open **Settings → Pages**. Under **Build and deployment**, choose **Deploy from a branch**, select branch **main** and folder **/(root)**, then save.
6. Wait for GitHub Pages to finish publishing. The URL will look like `https://YOUR-GITHUB-USERNAME.github.io/REPOSITORY-NAME/`.
7. Open that HTTPS URL on each device and test the app. Use the **INSTALL APP** button when available, or follow the on-screen browser instructions.

## Install on devices

- **Android:** Open the published link in Chrome, then tap **INSTALL APP** or use Chrome's menu → Install app / Add to Home screen.
- **iPhone/iPad:** Open the link in Safari → Share → Add to Home Screen.
- **Windows/macOS/Linux/Chromebook:** Open the link in a current Chrome or Edge browser and use **INSTALL APP**, the install icon in the address bar, or the browser menu → Install.
- Installation requires the published HTTPS site. Opening the raw `index.html` file directly may not enable installation or service-worker offline support.

## Important data note

Attendance information is stored in the browser on the device where it is entered. Publishing the app does **not** automatically synchronize records between devices or users. Use the app's **Full App + Data** transfer/backup tools carefully when moving data. Do not share a backup containing personal information with anyone who should not see it.

## Updating the app

Upload the new app files to the same repository and commit the changes. Refresh the published site while online so the service worker can update. The service worker cache is versioned to help the updated app replace older cached files.

## Files that must stay together at repository root

- `index.html` — application
- `manifest.webmanifest` — install name, display settings, icons
- `sw.js` — offline app-shell caching
- `icon-192.png`, `icon-512.png`, `favicon.png` — app icons
- `.nojekyll` — tells GitHub Pages not to run Jekyll processing
