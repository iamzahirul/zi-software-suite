# ZI Order Manager — F-commerce Orders, Courier & COD

Developed by **Zahirul Islam (Rasel)** · https://iamzahirul.com

ফেসবুক / হোয়াটসঅ্যাপ পেজের বিক্রেতাদের জন্য: অর্ডার, কুরিয়ার বুকিং, শিপিং লেবেল, COD হিসাব, রিটার্ন ও আসল লাভ — এক জায়গায়।

- **Online demo:** https://zi-orders-demo.vercel.app → ব্যবসার নাম দিন → "স্যাম্পল ডেটা দেখুন".
- **Bangla tutorial video (~3.5 min):** `video/ZI-Orders-Tutorial-Bangla.mp4` — show this to clients.
- **Android APK:** `apk/` folder. **Laptop:** demo link → Chrome/Edge "Install". **Web build:** `web/`.

## Features
- **Fast order entry:** paste the customer's Messenger/WhatsApp message → name, phone (Bangla digits too) and address fill in. Products from stock or a custom item, discount, inside/outside Dhaka delivery charge, advance (bKash/Nagad), COD worked out.
- **Fake-order check:** on typing a phone number it shows that customer's past orders: delivered vs returned/refused; risky customers are flagged (limit set in Settings).
- **Order pipeline:** New → Confirmed → Packed → With courier → Delivered / Partly delivered / Returned / Cancelled, with full history. Status tabs with counts, search, **bulk actions** (confirm, packed, shipped, print labels).
- **Courier:** Steadfast — book orders and update delivery status straight from the app with the seller's own API key. Pathao, RedX, Paperfly and others — a **bulk-upload CSV**, then the tracking code is entered.
- **Shipping labels** (4 per A4, barcode, big COD box) and invoices (A4 / 80mm).
- **Courier & COD page:** how much each courier owes (COD − charge), COD on the way, record a courier payment (all unsettled orders get marked), return rate per courier.
- **Customers:** order history by phone number, repeat buyers, risky list, WhatsApp button (confirmation and shipped messages ready-made).
- Products & stock (sold quantity subtracted automatically), expenses incl. **Facebook ad cost per order**.
- Reports: profit & loss (after courier and returns), daily, by source, by courier, by product, by district, return reasons. Print / CSV.
- Bangla/English, dark mode, PIN lock, backup, offline; optional cloud sync (Supabase) for more than one device.

## Steadfast setup (optional, per client)
Steadfast merchant panel → API → copy API key and Secret key → app Settings → "Steadfast courier API". The keys stay on that device. Steadfast booking has not been tried with a live merchant account yet; test it with the client's first order.

## Changelog

### v1.0.1 — 28 Oct 2026
- Orders can no longer be saved with a negative or zero quantity, a negative price, a discount bigger than the subtotal, or an advance bigger than the total (before, a wrong quantity could show negative sales and fake profit).
- Delivery charge now picks "inside Dhaka" correctly when the district is written in Bangla (ঢাকা); all 64 districts in English and Bangla in the district list; pasting a message finds the district too.
- Pasting a one-line message ("Name 017… address") now separates name and address; Bangla digits in the address are kept as typed.
- Warning when the phone number already has an order in progress (stops duplicate orders); stock warning when ordering more than in stock.
- Order date can be changed (for entering yesterday's orders).
- "Undo status" button for an order marked delivered / returned / cancelled by mistake.
- Own-delivery orders no longer appear as money the courier owes you.
- A customer who cancelled before the parcel was sent is no longer counted as "refused" in the fake-order check.
- Profit of a returned order now counts the advance the customer paid; delivered sales of partly-delivered orders use the money actually received.
- Ad cost per order works after switching language.
- Order history times showed the previous day for actions after midnight — fixed.
- Searching orders and customers with Bangla digits (০১৭…) works.
- Carrybee and eCourier added to the courier list.
- Phone screen: order list shows status and COD without sideways scrolling.
- Address on labels/invoices no longer repeats the district.
