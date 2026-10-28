# ZI POS — Billing & Stock

Developed by **Zahirul Islam (Rasel)** · https://iamzahirul.com

দোকানের বিক্রি, স্টক, বাকি, ইনভয়েস — মোবাইল ও ল্যাপটপ দুটোতেই, ইন্টারনেট ছাড়াও চলে।

- **Online demo (client-ke dekhan):** https://zi-pos-demo.vercel.app — open → shop name din → "স্যাম্পল ডেটা দেখুন" chaple full demo data chole ashe.
- **Android APK:** `apk/` folder — phone-e copy kore install korun (Settings → "Install unknown apps" allow).
- **Laptop:** Chrome/Edge-e demo link khulun → address bar-er "Install" icon (ba About page-er "অ্যাপ ইনস্টল করুন") → desktop app hoye jabe, offline-e cholbe.
- **Web build:** `web/` folder — client-er nijer domain/hosting-e upload korar jonno.

## Features
- POS sell screen: product search, USB/Bluetooth barcode scanner, camera scan (Android Chrome), discount (৳/%), VAT, cash/bKash/Nagad/Rocket/card/bank, change & due
- Invoice print: 80mm / 58mm thermal, A4 (logo, barcode, signature), money receipt, return slip
- Products & stock: categories, units, warranty, serial/IMEI, low-stock alert, stock adjustment, stock history, barcode label print (A4 sheet / 38×25mm roll), CSV import/export
- Customers & suppliers: due ledger, receive/pay, statement print, WhatsApp/SMS due reminder
- Purchases (stock in), sales return (cash or adjust due), void invoice, expenses
- Dashboard & reports: today/month sales, profit, cash flow by method, daily sales, product-wise profit, stock value, due list, expenses — print + CSV
- Bangla/English, dark mode, PIN lock, backup/restore file, optional cloud sync (phone + laptop same data via client's Supabase)

## Client setup checklist
1. Settings → business name, phone, address, logo, invoice paper (80mm/A4), invoice footer.
2. Products → Import CSV (template ache) or one by one; "বারকোড বানান" for items without barcode, then print labels.
3. Multi-device: each device-e Settings → Device code alada (A, B, C…). Cloud sync: client-er Supabase project-e `supabase/zi_sync.sql` run → Settings → Cloud sync-e connect.
4. Weekly backup remind kore — Backup page theke file Google Drive-e rakhte bolun.

## Changelog

### v1.0.1 — 28 Oct 2026
- A double click (or F9 + click) on "Complete sale" no longer saves the same bill twice with the same invoice number; the same guard on sales returns and purchases.
- A minus sign typed in discount, VAT or paid no longer raises the bill or the due; negative prices and zero quantities are refused.
- Purchases: quantities and prices with decimals (1.5 kg, ৳12.75) can be typed again; editing an old purchase no longer brings back its old buying price.
- Invoice: shows "Previous due" and "Total due" correctly right after a sale; A4 invoice shows the amount in words (Taka / টাকা কথায়); return slip shows the customer and payment method.
- New: hold a sale and serve the next customer, then resume it (Hold / Held sales on the sell screen).
- New: a received/paid payment entered by mistake can be deleted from the customer/supplier ledger; a customer or supplier with no transactions can be deleted.
- Phone numbers typed in Bangla digits are saved as normal digits (call/SMS/WhatsApp work) and duplicates are caught; barcodes typed in Bangla digits are found.
- Product CSV import: units like "Pcs"/"KG" are recognised and the same item twice in a file is added once. Deleting a product warns if it still has stock.
- Reports: "Invoices" row label fixed in Bangla; sample data now shows a few low-stock items; small text fixes.
- বাংলা: ডাবল ক্লিকে একই বিল দুবার সেভ হওয়া বন্ধ, হোল্ড বিক্রি, A4 ইনভয়েসে টাকা কথায়, ভুল আদায় মুছে ফেলার সুবিধা।
