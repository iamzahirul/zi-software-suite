# ZI Pharmacy — Medicine Shop Management

Developed by **Zahirul Islam (Rasel)** · https://iamzahirul.com

ওষুধের দোকানের কাউন্টার বিক্রি, ব্যাচ ও মেয়াদ, বাকি, ক্রয় ও রিপোর্ট — মোবাইল ও ল্যাপটপে, ইন্টারনেট ছাড়াও চলে।

- **Online demo (client-ke dekhan):** https://zi-pharmacy-demo.vercel.app — open → pharmacy name din → "স্যাম্পল ডেটা দেখুন" (30 diner bikri, purchase, expiry, baki shoho).
- **Android APK:** `apk/` folder.
- **Laptop:** Chrome/Edge-e demo link → "Install" → desktop app, offline-e cholbe.
- **Web build:** `web/` folder — client-er nijer hosting-e dewar jonno.

## Features
- **Counter:** brand / generic / company / barcode search (keyboard ↑↓ Enter), "sold often" list, out-of-stock hole same-generic onno brand suggest, +1 strip button, Rx warning + doctor name, 0/5/10% discount, round to taka, cash/bKash/Nagad/Rocket/card, change & baki, 80mm/58mm/A4 receipt with drug license.
- **Batch & expiry:** protita purchase line alada batch; bikri sobsomoy age-meyad-sesh batch theke (FEFO); meyadottirno batch kokhono bikri hoy na.
- **Purchase:** supplier invoice — batch, expiry month, qty, bonus (10+1), rate, MRP, bill discount, due. Notun MRP dile medicine-er dam update. Opening stock alada.
- **Expiry page:** expired / 1 / 3 / 6 maser moddhe; supplier-ke ferot (dena theke bad) ba fele dewa (loss hisebe).
- **Medicines:** 39 common BD medicine ek click-e, CSV import (template ache, stock+expiry shoho), rack, reorder level, Rx flag, batch-wise stock, adjustment.
- **Customers & baki:** ledger, collection, baki limit, WhatsApp/SMS reminder; **Suppliers & companies:** due, payment, ledger.
- **Invoices & returns:** reprint, partial return stock-e ferot, cash ba bakite adjust.
- **Reports:** profit (net sales − cost − loss − expense), daily, medicine-wise, company-wise, stock value (cost & MRP), MPO-r jonno company-wise **order list**, due list, expenses, cash flow — print + CSV.
- Bangla/English, dark mode, PIN lock, backup/restore, optional cloud sync (several counters/devices).

## Client setup
1. Settings → pharmacy name, address, drug license, usual discount, receipt paper.
2. Medicines → "৩৯টি সাধারণ ওষুধ যোগ করুন" ba CSV import.
3. Purchase → শুরুর স্টক: shelf-er protita batch expiry shoho.
4. Multi-counter: protita device-e alada Device code; cloud sync chaile client-er Supabase-e `zi_sync.sql` run kore connect.

## Changelog

### v1.0.1 — 28 Oct 2026
- A double click (or Ctrl+Enter + click) on "Save sale" no longer saves the same bill twice with the same invoice number; the same guard on returns and purchases.
- A minus or over-100% discount, or a minus "money received", can no longer change the bill or the baki; the discount box accepts decimals like 2.5%.
- Baki limit is now enforced at the counter: the shop is asked before a sale takes a customer over the limit.
- Receipt: "Previous due" and "Total due" are correct right after a sale; A4 invoice shows the amount in words (Taka / টাকা কথায়); return slip shows the customer.
- Purchases / opening stock: negative rates, bonus or discount are refused; a batch whose expiry month has already passed asks for confirmation.
- A received/paid payment entered by mistake can be deleted from the ledger; a customer or supplier with no transactions can be deleted.
- Phone numbers and barcodes typed in Bangla digits now work (call/SMS links, duplicate check, barcode search).
- Stock report values each batch at its own cost (matches the Medicines page); medicine CSV import no longer adds the same medicine twice; customer opening-due date fixed for early-morning entries.
- বাংলা: ডাবল ক্লিকে একই বিল দুবার সেভ বন্ধ, বাকির সীমা মানা হয়, A4 ইনভয়েসে টাকা কথায়, ভুল আদায় মুছে ফেলা যায়।
