# ZI Landing Page — Sales Page + Order Form

Developed by **Zahirul Islam (Rasel)** · https://iamzahirul.com

এক বা অল্প কয়েকটি পণ্যের অনলাইন বিক্রেতার জন্য: কয়েক মিনিটে সেলস পেজ (ছবি, অফার দাম, টাইমার, রিভিউ, প্রশ্নোত্তর) আর অর্ডার ফর্ম (ডেলিভারি চার্জসহ মোট), অর্ডার হোয়াটসঅ্যাপে ও গুগল শিটে, আর অ্যাপে সব অর্ডারের তালিকা।

- **Online demo (app):** https://zi-landing-demo.vercel.app → নাম দিন → "স্যাম্পল ডেটা দেখুন".
- **Sample sales page:** https://zi-landing-demo.vercel.app/sample.html — show this to clients.
- **Bangla tutorial video:** `video/ZI-Landing-Page-Tutorial-Bangla.mp4`.
- **Android APK:** `apk/` folder. **Laptop:** demo link → Chrome/Edge "Install". **Web build:** `web/`.

## Features
- **Page editor with live phone preview:** shop and product name, short line, regular / offer price (saving shown), photos (inside the file), YouTube video, selling points, details, options (colour / size), two delivery areas and charges, COD note, WhatsApp / phone / bKash, reviews with stars, FAQ, page colour, Bangla or English, offer countdown timer, "only N left", max quantity, order no prefix, Facebook Pixel (PageView + Purchase).
- **Order form on the page:** name, mobile (Bangla digits accepted, 11-digit check), address, area, option, quantity, note; live total with delivery charge; order number; one-tap "confirm on WhatsApp" with all details; sticky order button.
- **Where orders go:** the customer's WhatsApp message, **Google Sheet** via a 6-line Apps Script webhook (copy-paste steps inside the app), and the app's order list (import from the sheet's published CSV; or type in phone orders). Test orders from the preview land in the list.
- **Publish:** download one HTML file and upload to any hosting (Netlify Drop, Vercel, cPanel, GitHub Pages) or the client's domain.
- **Orders:** new → confirmed → shipped → delivered / returned / cancelled, call / WhatsApp confirmation, A4 invoice with COD amount, CSV export, totals.
- Bangla/English, dark mode, PIN lock, backup, offline; optional cloud sync (Supabase).

## Note
Courier booking (Steadfast / Pathao) is in **#07 F-commerce Order Manager**; orders can be moved there via CSV.

## Changelog

### v1.0.1 — 28 Oct 2026
- Page editor: leaving the editor without pressing Save no longer loses your changes (they are saved automatically); closing the browser tab warns first.
- Warning when a page has neither a WhatsApp number nor a Google Sheet link — such a page shows "order placed" but the order reaches nobody. Downloading it asks first.
- Orders imported from the Google Sheet: the mobile number keeps its leading 0, the order date is the Bangladesh date (orders after midnight showed the previous day), and duplicate rows are skipped. New Sheet script (Copy code) stores the mobile number as text — paste it again in Apps Script when convenient.
- Test orders from the preview get the right date.
- Typed-in orders: quantity must be 1 or more (a minus quantity reduced the totals), mobile number checked and saved in 01XXXXXXXXX form, delivery area chosen as area 1 / area 2 for any page.
- Sales page: the offer timer is separate for each page, order sending to the Google Sheet is more reliable when the customer closes the page quickly, "২৩টি" without a stray space, Facebook Pixel ID cleaned.
- Search with Bangla digits; "৮৫টি অর্ডার" wording.
