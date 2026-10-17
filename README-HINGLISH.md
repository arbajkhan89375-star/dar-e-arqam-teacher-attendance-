# Dar-e-Arqam Academy — Teacher Attendance Android App

## Is package mein kya hai
- Android Studio project with WebView app shell
- Teacher Attendance portal bundled in app assets
- Teacher sign-up/login, students, attendance, history and owner support chat UI
- GitHub Actions workflow that builds an installable debug APK

## APK banane ka workflow
Is environment mein Android SDK/build tools installed nahi hain, isliye APK ko yahin compile karke verify nahi kar sakte. Build ke liye project ko GitHub repository mein upload/push karna hoga. Uske baad Actions workflow APK artifact banayega:
1. GitHub par new private repository `dar-e-arqam-teacher-attendance` banayein.
2. ZIP ke andar ki files repository ke root par upload karein.
3. Actions tab mein `Build Android APK` workflow run karein.
4. Successful run ke Artifacts section se `Dar-e-Arqam-Teacher-Attendance-APK` download karein.
5. Artifact ZIP extract karke `app-debug.apk` install karein.

## Important
- App ko Supabase project aur internet connection chahiye.
- Supabase database migration pehle apply ki gayi thi; Owner role/account abhi separately configure/test karna hoga.
- Production student records use karne se pehle two-teacher isolation, owner messaging, signup and attendance permissions test karna zaroori hai.
- This is a debug APK build workflow, not a Play Store signed release.
