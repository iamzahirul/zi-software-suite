# ZI Recruiting Agency — Manpower manager

Developed by **Zahirul Islam (Rasel)** · https://iamzahirul.com

বিদেশে লোক পাঠানো রিক্রুটিং এজেন্সির জন্য: প্রার্থীর পাসপোর্ট থেকে ফ্লাইট পর্যন্ত পুরো ফাইল (মেডিকেল, পুলিশ ক্লিয়ারেন্স, ভিসা, মোফা, ফিঙ্গারপ্রিন্ট, বিএমইটি ট্রেনিং, ম্যানপাওয়ার ক্লিয়ারেন্স, টিকেট), ভিসা/ডিমান্ড লট, এজেন্ট (দালাল) কমিশন, টাকা গ্রহণ ও খরচের হিসাব।

- **Online demo:** https://zi-recruit-demo.vercel.app → এজেন্সির নাম দিন → "স্যাম্পল ডেটা দেখুন".
- **Bangla tutorial video:** `video/ZI-Recruiting-Agency-Tutorial-Bangla.mp4` — show this to clients.
- **Android APK:** `apk/` folder. **Laptop:** demo link → Chrome/Edge "Install". **Web build:** `web/`.

## Features
- **Candidates (প্রার্থী):** registration with photo, passport no / issue / expiry, father, mother, DOB, NID, mobile + guardian mobile, district & address, trade, country, visa lot, agent and commission, package (contract amount). Search by name, passport, mobile, reg. no; filter by stage and country; print the list.
- **File tracker — 10 steps:** passport received → medical (centre, fit / unfit / waiting, validity) → police clearance → visa (no, issue, expiry) → MOFA → fingerprint → BMET training → manpower clearance (smart card) → ticket (airline, PNR, flight date/time) → flown. One tap on a step records its date and the fee paid for it (added to the candidate's costs); undo a step; cancel or reopen a file with refund.
- **Alerts:** passport validity below N months (Settings, default 6), medical expiring within 15 days (validity days in Settings, default 90), visa expiring within 30 days, flights in the next 7 days. One-tap flight SMS / WhatsApp to all flyers.
- **Money:** payments from candidates with money receipt (A4 / 80mm), booking money & instalments, due per candidate, costs per candidate, expected profit per file; payment reminders and status updates by SMS / WhatsApp (no SMS gateway needed — opens the phone's SMS app or WhatsApp).
- **Visas & demands:** each visa lot / demand letter from a sponsor — country, trade, salary, quantity, used / left, cost per visa, selling package, expiry; add candidates straight into a lot; print its candidate list.
- **Agents:** sub-agents (dalal) with usual commission, candidates brought, commission earned / paid / payable, pay agent, agent statement.
- **Accounts:** money in / out for any period, costs by category (medical, visa, MOFA, ticket, BMET, office rent, salary…), received by method.
- **Reports:** flights, stage-wise, country-wise, profit per candidate, candidate dues, agents — print or export CSV (Excel).
- **Print:** candidate file (A4 with photo and step checklist), money receipt, candidate lists, agent statement. RL no on documents.
- Bangla/English, dark mode, PIN lock, backup, offline; optional cloud sync (Supabase) for several office PCs.

## Needs from the client
- Nothing paid is required. For automatic bulk SMS (instead of one-tap SMS/WhatsApp) an SMS gateway account would be needed.
