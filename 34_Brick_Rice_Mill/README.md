# ZI Mill — Brick Field & Rice Mill

Developed by **Zahirul Islam (Rasel)** · https://iamzahirul.com

ইটভাটা অথবা রাইস মিল/চাতালের জন্য (শুরুতে ড্যাশবোর্ডে ব্যবসা বাছুন, পরে সেটিংসেও বদলানো যায়): কাঁচামাল ক্রয় (মাটি, কয়লা / ধান), উৎপাদন ও হার (ভাটা পোড়ানো রাউন্ডে ১ নম্বর/২ নম্বর/পিকেট/আধলা, অথবা ধান থেকে চাল/খুদ/কুঁড়া/তুষ), পাথাইল ও শ্রমিকের মজুরি (হাজার প্রতি বা দিন), পণ্যের স্টক, চালানসহ বিক্রি, ক্রেতার বাকি, সাপ্লায়ার ও সর্দারের দেনা, খরচ আর লাভ।

- **Online demo:** https://zi-mill-demo.vercel.app → নাম দিন → "স্যাম্পল ডেটা দেখুন" (ইটভাটার মৌসুম; নতুন করে শুরু করে ড্যাশবোর্ডে "রাইস মিল / চাতাল" বাছলে রাইস মিলের স্যাম্পল দেখা যায়).
- **Bangla tutorial video:** `video/ZI-Brick-Rice-Mill-Tutorial-Bangla.mp4`.
- **Android APK:** `apk/`. **Laptop:** demo link → Chrome/Edge "Install". **Web build:** `web/`.

## Features
- **Two modes:** brick field or rice mill, picked on the dashboard before the first entry; standard items come ready for each (add the other mode's items any time).
- **Items & stock:** raw material, half-made (raw bricks), products; units — pcs, thousand, kg, maund, ton, bag, cft, truck; stock = opening + bought + made − used − sold; stock value; stock list print.
- **Production:** what went in and what came out, with yield % (e.g. 72% first class bricks, 64% rice from paddy).
- **Labour:** sardar groups or own workers; work (molding, kiln loading / unloading, firing, chatal, drying, bagging); quantity × rate (per thousand, per day); paid now; raw bricks made go into stock; wage sheet print.
- **Sales & challan:** several products, rate, transport, discount, vehicle; paid now — the rest on the customer; challan / invoice print (A5) with signatures.
- **Purchases & expenses:** raw material with carrying, supplier dues; lease, electricity, diesel, salary, fees, workers' food…
- **Parties & dues:** customers (they owe), suppliers and sardars (we owe), ledger, statement, money in / out.
- **Reports:** month-by-month profit (cash basis), product sales, production yield, labour by sardar, dues. Print / CSV.
- Bangla/English, dark mode, PIN lock, backup, offline; optional cloud sync (Supabase).
