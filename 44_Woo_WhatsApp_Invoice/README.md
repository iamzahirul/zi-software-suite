# ZI WhatsApp Order & Bangla Invoice — WooCommerce plugin (#44)

Developed by **Zahirul Islam (Rasel)** · https://iamzahirul.com

পণ্য ও কার্টে "হোয়াটসঅ্যাপে অর্ডার করুন" বাটন — ক্রেতা নাম, মোবাইল, ঠিকানা ও জেলা দিলে ডেলিভারি চার্জসহ মোট দেখে; অর্ডার WooCommerce-এ সেভ হয় আর পুরো অর্ডার লেখা অবস্থায় হোয়াটসঅ্যাপ খোলে। সাথে বাংলা / ইংরেজি ইনভয়েস ও প্যাকিং স্লিপ (A4 ও ৮০ মিমি), কথায় টাকার পরিমাণসহ।

- **Install file:** `zi-whatsapp-order-invoice.zip` → WordPress → Plugins → Add New → Upload Plugin.
- **Client demo page:** https://zi-woo-whatsapp-demo.vercel.app — "Try it live" opens a real shop in WordPress Playground (Bangla, sample orders).
- **Live demo direct link:** https://playground.wordpress.net/?blueprint-url=https%3A%2F%2Fzi-woo-whatsapp-demo.vercel.app%2Fblueprint.json
- **Bangla tutorial video:** `video/ZI-WhatsApp-Order-Invoice-Tutorial-Bangla.mp4`
- **Screenshots:** `screenshots/` · Playground blueprint: `playground-blueprint.json`
- Source: `C:\ZI\wp-plugins\zi-whatsapp-order-invoice` (copy in `_source/zi-software/wp-plugins`).

## Requirements
WordPress 6.6+ (tested 7.1.3), WooCommerce 9.0+ (tested 11.2.1), PHP 8.2+. HPOS, block themes, Cart/Checkout blocks supported.

## Features
**WhatsApp order**
- Button on product pages, shop / category pages (optional) and the cart — classic themes and block themes (Twenty Twenty-Five), classic cart and the Cart block. Out-of-stock products optional (pre-orders).
- Reads the chosen variation and quantity; cart mode sends every item.
- **Quick order form** (popup, bottom sheet on phones): name, mobile (Bangla digits, 11-digit check), address, district (64), note, optional email; remembers the customer on that phone; shows products, **delivery charge from the shop's WooCommerce shipping zones** and total.
- **Saves a WooCommerce order** (On hold, "Cash on delivery (WhatsApp order)", stock held, admin new-order email) then opens WhatsApp with items, delivery, total, customer details and **order number**.
- Several numbers (random share), floating chat button (left/right), message templates with placeholders, shortcode `[zi_whatsapp_button product="123"]` / `[zi_whatsapp_button source="cart"]`.
- Spam guard: nonce, honeypot, max 5 orders per IP per 10 minutes.

**Invoice**
- Invoice and **packing slip**, **A4 or 80 mm thermal**, **Bangla or English** independent of the site language (switch on the page), Bangla digits, **amount in words** (lakh/crore), logo, shop details, bill-to / ship-to, items with options and SKU, discount, fees, delivery charge, total, **Paid / Due — collect on delivery** (reads the verified advance of plugin #43), notes, signatures, small credit line (can be turned off).
- Browser printing → Bangla shapes perfectly; "Save as PDF" gives a PDF.
- Order screen box: Invoice (A4), 80 mm receipt, Packing slip, **Message customer on WhatsApp** (confirmation text with total, due and invoice link). Invoice icon in the orders list; **bulk Print invoices / Print packing slips**.
- Customers: Invoice button in My Account → Orders, on the order and thank-you page, link in emails — secured by the order key.
- Bangla + English: `languages/` .pot + bn_BD .po / .mo / .l10n.php (143 strings, all translated).

## Tested
Same test run as #43 (`python C:\ZI\wp-plugins\dev\test_plugins.py`, 49/49): WhatsApp quote with Dhaka (৳70) and outside-Dhaka (৳130) delivery, cart quote, order saved + message contents, bad phone / bad nonce refused, Bangla A4 and English 80 mm invoices, bulk slips, key-protected customer link, admin box. Screens checked on desktop and a 390 px phone.

## Selling notes
Price range in the catalog: ৳2,000–5,000. Works together with #43 (advance shown as paid on the invoice).
