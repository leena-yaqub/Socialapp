SocialLearningApp — Quick README

What it is
Social Learning App (Jetpack Compose) — quizzes (timed), task manager, realtime chat, onboarding, Firebase auth + Realtime DB, and AdMob ads.

Quick features

Email/password signup & profile (name, email, avatar) via Firebase Auth + Realtime DB

5-question quizzes with per-question timer and saved quiz history

Tasks: add / edit / delete / filter (All / Pending / Done) — realtime sync per user

Group chat via Firebase Realtime Database

Onboarding (3 screens) with banner + interstitial ads

Navigation using Jetpack Compose Navigation

Quick start (dev)

Clone repo:

git clone <repo-url>
cd SocialLearningApp


Put google-services.json into app/.

Open in Android Studio → Sync Gradle.

Build & run:

Windows PowerShell: .\gradlew clean assembleDebug

macOS/Linux: ./gradlew clean assembleDebug

Firebase setup (short)

Create Firebase project.

Add Android app with matching package name; download google-services.json → place in app/.

Enable Email/Password in Authentication.

Create Realtime Database (dev rules permissive).

(Optional) Enable Storage for avatars.

AdMob setup (short)

Create app & ad units (banner + interstitial) in AdMob.

Put IDs in Constants.kt.

Add Mobile Ads dependency and initialize MobileAds.initialize(context) {}.

Important deps (app/build.gradle)

Compose, Navigation, Lifecycle, Coroutines

Firebase: auth-ktx, database-ktx, storage-ktx (via BOM)

Coil: io.coil-kt:coil-compose

Ads: com.google.android.gms:play-services-ads

(If using Room) androidx.room:room-runtime, room-ktx, kapt room-compiler

Quick troubleshooting

Unresolved reference 'kapt' → add id("kotlin-kapt") to plugins.

Room errors no such column → update @Entity fields to match DAO, bump DB version or uninstall app, or use fallbackToDestructiveMigration() for dev.

Compose missing imports (remember, collectAsState) → import androidx.compose.runtime.*.

Gradle wrapper: use .\gradlew on Windows.

Deliverables

Clean repo, README, working APK (attach in Releases), Firebase + AdMob instructions (this file).
<img width="896" height="1344" alt="image" src="https://github.com/user-attachments/assets/244f59f2-e32b-4a0a-9771-2bfcea1861a2" />
<img width="355" height="513" alt="image" src="https://github.com/user-attachments/assets/6b792957-bb50-4fa6-a6dc-ef86e92f2ba1" />
<img width="362" height="494" alt="image" src="https://github.com/user-attachments/assets/3dc9a428-f358-418b-9efd-12eb4eb0bfe4" />
<img width="364" height="547" alt="image" src="https://github.com/user-attachments/assets/324650fe-9d8f-4a54-b45c-cd6b8e5fdea9" />
![WhatsApp Image 2025-08-30 at 00 51 51_8fb2afb8](https://github.com/user-attachments/assets/d2a5ae5b-b8a9-49c7-a669-11328cbadf65)
<img width="331" height="479" alt="image" src="https://github.com/user-attachments/assets/2cf1d8bc-60cb-4718-a201-0a92863ac4f7" />
<img width="239" height="270" alt="image" src="https://github.com/user-attachments/assets/362d60ee-677f-4a60-8cb2-02113df87882" />
<img width="333" height="490" alt="image" src="https://github.com/user-attachments/assets/47f72e9b-e26d-4748-8fe3-1bcc4f547bd9" />
<img width="677" height="605" alt="image" src="https://github.com/user-attachments/assets/a072ed27-2262-43f3-8e23-769027f8a956" />









