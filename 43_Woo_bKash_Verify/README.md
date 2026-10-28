# ZI bKash & Nagad Payment Verify — WooCommerce plugin (#43)

Developed by **Zahirul Islam (Rasel)** · https://iamzahirul.com

বিকাশ / নগদ / রকেট / উপায়ে ম্যানুয়াল পেমেন্ট: ক্রেতা টাকা পাঠিয়ে নম্বর ও TrxID দেন, দোকানদার এক স্ক্রিন থেকে যাচাই বা বাতিল করেন। একই TrxID দুইবার ব্যবহার করা যায় না; ডেলিভারি চার্জ অগ্রিম নেওয়া যায়।

- **Install file:** `zi-bkash-nagad-verify.zip` → WordPress → Plugins → Add New → Upload Plugin.
- **Client demo page:** https://zi-woo-bkash-demo.vercel.app — "Try it live" opens a real WordPress + WooCommerce shop in the browser (WordPress Playground, Bangla, sample payments waiting).
- **Live demo direct link:** https://playground.wordpress.net/?blueprint-url=https%3A%2F%2Fzi-woo-bkash-demo.vercel.app%2Fblueprint.json
- **Bangla tutorial video:** `video/ZI-bKash-Nagad-Verify-Tutorial-Bangla.mp4`
- **Screenshots:** `screenshots/` · Playground blueprint: `playground-blueprint.json`
- Source: `C:\ZI\wp-plugins\zi-bkash-nagad-verify` (copy in `_source/zi-software/wp-plugins`).

## Requirements
WordPress 6.6+ (tested 7.1.3), WooCommerce 9.0+ (tested 11.2.1), PHP 8.2+ (tested 8.2 and 8.3). HPOS and the block checkout are supported.

## Features
- **4 wallets** as separate checkout options: bKash, Nagad, Rocket, Upay — each with its own number, account type (Personal → Send Money, Agent → Cash Out, Merchant → Payment), QR image, extra instructions, TrxID length check.
- **Checkout box** (block checkout and classic `[woocommerce_checkout]`, also the "pay for order" page): USSD code, number + Copy button, exact amount, steps; sender number (Bangla digits / +880 accepted) and TrxID (auto upper-case).
- **Advance payment:** full total / delivery charge only / fixed amount — the rest is cash on delivery and shown everywhere ("Pay on delivery").
- **MFS charge %** (e.g. 1.85) added as a fee live when the method is chosen.
- **Duplicate-TrxID guard** enforced by a unique database key (even two checkouts at the same second can't reuse a TrxID). Can be turned off.
- **Verify screen** (WooCommerce → bKash/Nagad Verify): counts, Pending / Verified / Rejected tabs, search by TrxID / number / order no, filter by wallet and dates, Verify / Reject (with reason) / Reopen, bulk actions, delete record (frees a TrxID), CSV export (Excel-ready UTF-8), pending count bubble in the menu.
- **Order flow:** paid → On hold (stock held, normal new-order emails with payment details) → Verify → Processing (payment complete + transaction ID; advance orders stay "not fully paid") → or Reject → Failed / Cancelled + **"Payment rejected" email** (editable in WooCommerce → Settings → Emails) with a pay-again link. Every step adds an order note.
- **Order screen box** with all details, Verify / Reject / Reopen and earlier attempts; **TrxID column** and **TrxID search** in the orders list.
- **Customer:** payment status box on the thank-you page, My Account order page and in emails.
- **Bangla + English:** `languages/` has .pot, bn_BD .po / .mo / .l10n.php (149 strings, all translated). Credit on the settings page, gateway pages and plugin header.

## Tested (local WordPress 7.1.3 + WooCommerce 11.2.1 on PHP 8.2, and WordPress Playground PHP 8.3)
`python C:\ZI\wp-plugins\dev\test_plugins.py` — 49 checks for #43 + #44 all pass: block checkout via Store API, charge added/removed when switching wallets, duplicate / short TrxID and bad number refused, Nagad delivery-charge advance, classic checkout, thank-you page, verify / reject / pay again after rejection, order list column and search, CSV export, no PHP notices.

## Selling notes
- Price range in the catalog: ৳3,000–6,000. Setup: enter numbers in WooCommerce → Settings → Payments.
- The demo zip on Vercel has a random file name and is not linked from the page (only the Playground blueprint uses it).
