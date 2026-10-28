# ZI Token — Token & Queue System

Developed by **Zahirul Islam (Rasel)** · https://iamzahirul.com

ডাক্তারের চেম্বার, ক্লিনিক, ডায়াগনস্টিক সেন্টার, সার্ভিস সেন্টার ও অফিসের জন্য সিরিয়াল সিস্টেম: সার্ভিস অনুযায়ী টোকেন (A-001, B-001…), কাউন্টার থেকে "পরের জনকে ডাকুন", ঘণ্টার শব্দ ও বাংলা ভয়েসে ঘোষণা, ওয়েটিং রুমের টিভিতে বড় করে কে কোন কাউন্টারে, আনুমানিক অপেক্ষার সময়, আর দিনের রিপোর্ট।

- **Online demo:** https://zi-token-demo.vercel.app → প্রতিষ্ঠানের নাম দিন → "স্যাম্পল ক্লিনিক লোড".
- **Bangla tutorial video:** `video/ZI-Token-Tutorial-Bangla.mp4` — show this to clients.
- **Android APK:** `apk/` folder. **Laptop:** demo link → Chrome/Edge "Install". **Web build:** `web/`.

## Features
- **Issue token:** one big button per service; optional name, mobile and priority (elderly / disabled / emergency); shows people ahead and approximate wait; 58 mm token slip (auto-print option for a kiosk).
- **Counter:** each counter / doctor's room calls its own lines — call next, call again, done, did not come, send to another line (doctor → report delivery); waiting list with minutes waited; SMS the next ones.
- **Voice:** ding-dong chime and announcement "টোকেন নম্বর এ ১২, রুম ১০১-এ আসুন" (Bangla voice where the device has one, otherwise English), repeat count.
- **TV display:** full screen for the waiting room — latest call in large letters, now serving at every counter, next tokens per line, clock, scrolling notice. Open it on a second monitor / TV from the same PC: it updates instantly and announces each call. On several devices use cloud sync.
- **Waiting time:** estimated from today's real average service time and the number of open counters.
- **Tokens & reports:** every token with issue time, wait and counter; daily numbers, tokens by hour and by day, average wait, average service time, by service and by counter; CSV.
- Daily numbering resets automatically; Bangla/English, dark mode, PIN lock, backup, offline; optional cloud sync (Supabase) for several devices.
