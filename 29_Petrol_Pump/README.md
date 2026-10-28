# ZI Petrol Pump — Shift Sales

Developed by **Zahirul Islam (Rasel)** · https://iamzahirul.com

পেট্রোল পাম্প / ফিলিং স্টেশনের জন্য — Sheikh Filling Station-এর সফটওয়্যারের হিসাবের নিয়ম ZI প্ল্যাটফর্মে: নজেলের মিটার রিডিং দিয়ে শিফট ক্লোজিং, ড্রয়ারের টাকা কম/বেশি, ট্যাংকের স্টক, ডিপ, ডিপো থেকে তেল রিসিভ, বাকির কাস্টমার, লুব্রিকেন্ট, খরচ আর লাভ।

- **Online demo:** https://zi-pump-demo.vercel.app → প্রতিষ্ঠানের নাম দিন → "স্যাম্পল ডেটা দেখুন" (১৪ দিনের হিসাব).
- **Bangla tutorial video:** `video/ZI-Petrol-Pump-Tutorial-Bangla.mp4`.
- **Android APK:** `apk/`. **Laptop:** demo link → Chrome/Edge "Install". **Web build:** `web/`.

## Features
- **First run:** Octane, Petrol, Diesel, 3 tanks and 4 nozzles are created — set today's prices, tank stock (dip) and each nozzle's meter.
- **New sale:** tap the fuel, type litres or taka (the other is worked out); cash / bKash-Nagad / card / credit; credit customer (limit warning, vehicle number); lubricants by piece; 80mm / 58mm / A5 receipt.
- **Shift closing:** closing meter and test litres per nozzle → litres not entered as sales are added as one cash sale per fuel; cash expected = cash sales + meter cash + dues collected in cash − expenses from the drawer; count the drawer → short / excess. Shift entries are locked; shift report print with signatures.
- **Stock & tanks:** tank gauges with low-stock warning, fuel receive from the depot (tank room check, paid / unpaid, challan), average buy price, weekly dip correction (gain / loss kept), lubricant stock.
- **Credit customers:** companies, bus owners, contractors — limit, vehicles, opening due, ledger, statement, due list, SMS / WhatsApp reminder.
- **Expenses:** salary, electricity, generator fuel, maintenance, rent… paid from the drawer or bank.
- **Reports:** day by day (litres per fuel), by fuel with profit, payment types, profit (gross − expenses ± dip), shifts with short / excess, dip gain/loss, credit customers. Print / CSV.
- **Price change:** type the new government price once; old sales keep their price.
- Bangla/English, dark mode, PIN lock, backup, offline; optional cloud sync (Supabase) so several counters work together.
