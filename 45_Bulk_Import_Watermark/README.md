# ZI Product Studio — Bulk Product Import & Photo Watermark (#45)

Developed by **Zahirul Islam (Rasel)** · https://iamzahirul.com

রিসেলার, ড্রপশিপার ও অনলাইন দোকানের জন্য: সাপ্লায়ারের এক্সেল / CSV শিট থেকে একসাথে সব পণ্য, নিজের লাভ যোগ করে দাম, ছবি থেকে সাপ্লায়ারের নাম কেটে নিজের লোগো ও ফোন নম্বর, আর WooCommerce / ফেসবুক-ইনস্টাগ্রাম শপ ক্যাটালগ / Shopify-র জন্য তৈরি ফাইল।

- **Online demo:** https://zi-catalog-demo.vercel.app → দোকানের নাম দিন → "স্যাম্পল ডেটা দেখুন".
- **Bangla tutorial video:** `video/ZI-Product-Studio-Tutorial-Bangla.mp4`
- **Android APK:** `apk/` · **Laptop:** demo link → Chrome/Edge "Install app" · **Web build:** `web/`
- Source: `C:\ZI\apps\catalog` (copy in `_source/zi-software`).

## Features
- **Import:** .xlsx (reads Excel directly — Bangla, dates, several sheets), .csv / .tsv, or cells pasted from Excel / Google Sheets. Columns matched automatically (Name / পণ্যের নাম, Code / কোড, Price / দাম / MRP, Wholesale / কেনা দাম, Stock / পরিমাণ, Colour, Size, Photo link…), changeable before import. Live preview.
- **Price rule:** selling price from MRP or buying price + profit % + fixed amount, rounded to 10 / 50 / ending in 9. Money like "৳ 1,250/-" or "১২৫০ টাকা" is understood.
- **Same SKU again → update** price & stock instead of a duplicate (or skip). Missing codes get P-1001… Import history per supplier file.
- **Products:** search, category & photo filters, edit form, duplicate, **bulk change** (category, supplier, status, re-price, clear offer, delete) on the products shown, **printable price list with photos**.
- **Photos:** stored on the device; add per product, **match hundreds of photos by file name = SKU** (SW-T800.jpg, SW-T800-2.jpg), download photos from links in the sheet (when the supplier site allows).
- **Photo watermark & resize (batch):** sizes Square 1080 (FB/Instagram), Square 800 (website), Portrait 1080×1350, Story, Wide 1200×628, original, custom; fit whole photo (plain or blurred background) or fill; **crop edges** to remove the supplier's name; **logo** (9 positions, size, opacity); **text line** (shop name · phone · page, colour, dark band); **faint repeated name** against copying; brightness / contrast / colour; JPG / WebP / PNG + quality; file names by SKU / original / prefix; saved presets. Output: one ZIP.
- **Export:** WooCommerce product CSV, **Facebook / Instagram Shop catalog feed**, Shopify CSV, plain Excel sheet — photo links built from your website folder + SKU; step-by-step upload instructions in the app; photos ZIP named to match.
- Bangla / English, offline (installable PWA + APK), backup / restore, optional cloud sync of the product list (photos stay on the device), PIN lock, credit.

## Tested
`tsc` clean, all 283 texts in both languages, Excel reader tested with Bangla headers, dates, rich text, blank rows; all four CSV formats and the photo ZIP generated from the sample data; every page fits a 375 px phone; demo works offline.
