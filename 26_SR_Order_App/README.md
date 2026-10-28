# ZI SR Order — Distributor Sales (SR / DSR)

Developed by **Zahirul Islam (Rasel)** · https://iamzahirul.com

ডিস্ট্রিবিউটর হাউস ও কোম্পানির জন্য: এসআর রুটে গিয়ে দোকান থেকে অর্ডার নেয় (কার্টন + পিস, স্কিমের ফ্রি পিস নিজে থেকে), ডিএসআর লোড শিট নিয়ে মাল পৌঁছে আদায় করে, দিনের শেষে ডিএসআর হিসাব, দোকানভিত্তিক বাকি ও খতিয়ান, এসআর-এর মাসিক টার্গেট, স্ট্রাইক রেট ও কমিশন, গুদামের স্টক।

- **Online demo:** https://zi-sr-demo.vercel.app → প্রতিষ্ঠানের নাম দিন → "স্যাম্পল ডেটা দেখুন".
- **Bangla tutorial video:** `video/ZI-SR-Order-Tutorial-Bangla.mp4` — show this to clients.
- **Android APK:** `apk/` folder (for SR / DSR phones). **Laptop:** demo link → Chrome/Edge "Install". **Web build:** `web/`.

## Features
- **Take order (SR, phone-first):** pick SR → today's route comes by weekday (e.g. Sat·Mon·Wed). Every shop on the route shows ✓ ordered / ✗ no order (with reason: has stock, closed, no money, due high…) / not visited, and its due. Order in cartons + pieces, scheme free goods (12 + 1) worked out, stock shown, credit-limit warning, discount, note. Save or save & print memo.
- **Delivery (DSR):** all memos waiting for delivery by route / SR; **van load sheet** (product-wise cartons + pieces + free, with each shop's old due and a "collected" column); print all memos; deliver with less quantity if the shop returns some on the spot; cash / bKash collected; "deliver all as ordered".
- **DSR settlement:** delivered value, collected on memos, old dues collected, market returns, cash to deposit, new due created — printable with signatures.
- **Outlets (retailers):** code, owner, route, type, credit limit, opening due; ledger (memo / collection / return), statement (A4), due list by route, SMS / WhatsApp due reminders, days since last payment.
- **Products & stock:** trade price, carton price, MRP, buy price, pack size, scheme; stock = opening + received from company (DO / challan) − delivered + good returns; booked vs available; stock value; price list print.
- **Team & routes:** SR / DSR, monthly target, achievement %, strike rate (ordered ÷ visited shops), commission %; routes with visit days and SR.
- **Collections & market returns:** on-memo and old-due collections by method; returns as good (back to stock) or damaged / expired.
- **Reports:** day by day, SR performance, product sales, route sales, due aging (0–15 / 16–30 / 31–60 / 60+ days), memo-wise gross profit. Print / CSV.
- Memo on A5, A4 or 80mm thermal. Bangla/English, dark mode, PIN lock, backup, works offline; optional cloud sync (Supabase) so every SR's phone sends orders to the office computer.

## Note
GPS check-in of SR visits and a company-side (primary sales) portal can be added on request.
