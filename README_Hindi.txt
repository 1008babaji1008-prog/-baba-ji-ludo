BABA JI LUDO + BABA JI CONTROL — READY PACKAGE

IS PACKAGE MEIN
- index.html: Main Ludo game (Offline + Online)
- control.html: Separate Control Panel (Force 6 + fun effects)
- firebase-config.js: Aapke diye hue Firebase project ka config
- database.rules.json: Firebase Realtime Database Rules
- assets/: Dono app icons aur game sound files
- manifest.webmanifest: Ludo web-app metadata

1) FIREBASE MEIN KYA KARNA HAI
A. Firebase Console kholen aur project babajiludo-52663 select karein.
B. Authentication > Sign-in method > Anonymous ko Enable karke Save karein.
C. Realtime Database > Rules kholen. Is package ki database.rules.json file ka poora content paste karke Publish karein.
D. HTML, APK ya images Firebase Database mein upload NAHI karni hain. Sirf Rules yahan set hoti hain.

SECURITY NOTE: Yeh rules friends-only testing ke liye hain. Anonymous sign-in kar sakne wala koi bhi vyakti PIN jaankar us room ka data badal sakta hai. PIN 2003 ko password na samjhein. Personal, payment ya password wali jankari save na karein.

2) GITHUB PAGES PAR KYA UPLOAD KARNA HAI
ZIP extract karke Baba_Ji_Ludo_Ready_Package folder ke ANDAR ki saari files/folders apne GitHub Pages repository ke root mein upload karein. Folder ko as a nested folder upload na karein.
Upload structure:
  index.html
  control.html
  firebase-config.js
  manifest.webmanifest
  database.rules.json
  assets/ (poora folder)

Aapka configured repository URL:
Main Ludo: https://1008babaji1008-prog.github.io/-baba-ji-ludo/
Control:   https://1008babaji1008-prog.github.io/-baba-ji-ludo/control.html
Dono app same Firebase room path use karte hain: babaJiLudoRooms/<Room PIN>
Default Room PIN: 2003

3) CONTROL PANEL CHALANE KA TAREEQA
1. Sabhi players Ludo app mein Online mode se same Room PIN par join karein.
2. Game start hone ke baad har player Settings kholkar “मैं Fun Mode से सहमत हूँ” dabaye.
3. Control URL kholkar same Room PIN daalein aur Connect Room dabayein.
4. Consent poori hone par player select karein, “अगले पासे में 6 (Force 6)” chun kar effect button dabayein.
5. Force 6 sirf selected player ke agle turn ke dice roll par ek baar lagu hota hai. Yeh phone ko control nahi karta.

4) DO ALAG APK BANANE KE LIYE
APK is ZIP mein included NAHI hain. GitHub Pages deploy hone ke baad MIT App Inventor mein do alag WebViewer projects banayein:
- Ludo APK: WebViewer HomeUrl = upar diya Main Ludo URL; app icon = assets/BabaJi_Ludo_Icon.png
- Control APK: WebViewer HomeUrl = upar diya Control URL; app icon = assets/BabaJi_Control_Icon.png
Internet permission/network access on rakhein. Build se pehle dono URLs browser mein kholkar test karein.

TEST STATUS
Dono HTML ke inline JavaScript syntax aur local file references check kiye gaye hain. ZIP integrity bhi check hui. Is environment se Firebase par live login ya do phones ka network test nahi kiya gaya; GitHub upload aur Firebase Rules publish karne ke baad 2 devices par room join, turns, consent aur Force 6 test karein.
