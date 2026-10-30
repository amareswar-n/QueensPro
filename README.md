# Queens Pro – build an APK using only your phone

This project includes a GitHub Actions cloud build workflow. You do NOT need Android Studio or a computer. GitHub will compile the APK in the cloud.

## One-time setup on your phone

1. Download and extract `QueensProAndroidCloudBuild.zip` using your phone's Files app.
2. In your phone browser, sign in to GitHub (create a free account if needed).
3. Create a new **public** repository named `QueensPro` (public repositories can use GitHub Actions free minutes; check GitHub's current limits).
4. Open the new repository, tap **Add file → Upload files**.
5. In your phone's file picker, select the contents of the extracted `QueensProAndroid` folder, including the hidden `.github` folder and its `workflows/build-apk.yml` file. If your file picker hides dot-folders, enable showing hidden files. Upload and commit to `main`.
6. Open the repository's **Actions** tab. Select **Build Queens Pro APK** and, if needed, tap **Run workflow**.
7. Wait for the green successful run. Open that run and scroll to **Artifacts**.
8. Download `Queens-Pro-APK`, extract the downloaded ZIP, and tap `app-debug.apk` to install.

## App privacy and offline operation

- The Android manifest declares no permissions, including no INTERNET permission.
- The game is bundled in the APK and loads from local assets.
- No network connection is used by the installed game.
- Best scores are stored locally on the phone.

## Notes

- The first cloud build needs internet access on GitHub's build servers; your installed game does not.
- This is a debug APK for personal installation, not a Play Store release.
