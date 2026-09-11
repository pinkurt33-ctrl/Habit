# Habit Focus

2 ghante ke liye YouTube, Chrome, MX Player, Playstore aur Google app ko
block karne wala Android app. Phone calls aur messages hamesha allow rehte
hain.

## Kaise build karein (Android Studio)

1. Android Studio kholo → **Open** → is `HabitFocus` folder ko select karo.
2. Gradle sync hone do (pehli baar 2-5 min lag sakte hain, internet chahiye).
3. Phone ko USB se connect karo (Developer Options → USB Debugging on karo),
   ya ek emulator use karo.
4. Upar **Run ▶** button dabao. App phone par install ho jayega.

## App use karne ka tareeka

1. App kholo, jo apps block karni hain unko check rehne do (sab pre-checked
   hain).
2. **"1. Accessibility permission on karo"** dabao → Settings khulegi →
   **Habit Focus** dhoondo → on karo. Ye zaroori hai, isi se app ko pata
   chalta hai ki tum kaunsa app khol rahe ho.
3. Wapas app mein aao, **"2. Start Focus (2 ghante)"** dabao.
4. Ab agle 2 ghante tak jaise hi tum YouTube/Chrome/MX Player/Playstore/
   Google kholne ki koshish karoge, turant Home bhej diya jayega aur ek
   "lock" screen dikhegi. Phone call aur messages normal chalte rahenge.
5. Timer khatam hote hi sab kuch apne aap wapas khul jayega. Beech mein
   band karna ho to app mein "Focus band karo" dabao (khud discipline pe
   depend karta hai — is app mein jaan-bujhkar koi extra lock nahi lagaya
   gaya, taaki tum ise khud edit kar sako).

## Duration ya blocked apps badalna ho

- Duration: `MainActivity.kt` mein `twoHoursMillis` line dhoondo.
- Apps: `FocusPrefs.kt` mein `AVAILABLE_APPS` map mein naya package name
  add/remove karo (package name Play Store URL se mil jata hai, e.g.
  `id=com.google.android.youtube`).

## Zaroori note

- Ye app sirf tumhare apne phone par, tumhari apni marzi se chalta hai.
- Accessibility permission ek powerful permission hai — isse sirf apna
  banaya hua trusted app hi use karo.
- Play Store par publish karne ke liye Google ki Accessibility API policy
  padhni padegi (wo self-control/parental-control apps allow karta hai,
  lekin review sakht hota hai).
