# ZI Survey Dashboard — KoBo / SurveyCTO → Dashboard

Developed by **Zahirul Islam (Rasel)** · https://iamzahirul.com

এনজিও ও রিসার্চ ফার্মের জন্য: KoBoToolbox, SurveyCTO, ODK বা যেকোনো CSV সার্ভে ডেটা থেকে এক মিনিটে চার্ট, ইন্ডিকেটর, ক্রস-ট্যাব, এনুমারেটর মনিটরিং, ডেটা যাচাই ও প্রিন্টযোগ্য রিপোর্ট। সব হিসাব ব্রাউজারেই — ডেটা বাইরে যায় না, অফলাইনেও চলে।

- **Online demo:** https://zi-survey-demo.vercel.app → নাম দিন → "স্যাম্পল ডেটা দেখুন" (WASH baseline survey, 640 households).
- **Bangla tutorial video:** `video/ZI-Survey-Dashboard-Tutorial-Bangla.mp4` — show this to clients.
- **Android APK:** `apk/` folder. **Laptop:** demo link → Chrome/Edge "Install". **Web build:** `web/`.

## Features
- **Import:** CSV with comma / semicolon / tab (KoBo "XML values and headers", SurveyCTO wide CSV, ODK Central). **KoBo API pull** with server + form UID + API token, one-tap refresh. Several datasets side by side.
- **Column types guessed automatically** (single choice, multiple choice, number, date, GPS, text, system) — rename, change type or hide in "Columns". Date, area, enumerator, ID, start and end columns picked automatically.
- **Auto dashboard:** submissions, per day, average interview length, enumerators, submissions per day chart; a chart for every question — bars with %, multiple-choice option rates, mean / median / min / max / SD with histogram, GPS dot map coloured by area, sample text answers.
- **Indicators:** "% of households where question = answer" cards (e.g. sanitary latrine, soap available).
- **Filters:** date range + area / enumerator / any choice question — everything updates.
- **Cross-tab:** any two questions, counts / row % / column % with heat shading; print / CSV.
- **Data quality & field monitoring:** enumerator productivity (per day, average duration, short interviews), too-short interviews (set the minutes), duplicate IDs, missing answers per question, numeric outliers (3 SD).
- **Records:** filtered raw data, search, CSV export. **Printable report** with a frequency table and bar for every question.
- Bangla/English, dark mode, PIN lock, backup, offline; optional cloud sync (Supabase).

## Note
KoBo API pull needs the client's own API token. If a KoBo server blocks browser requests (CORS), export CSV from KoBo and import it — everything else works the same. Excel (.xlsx) files: save as CSV UTF-8 first (direct XLSX import can be added).

## Changelog

### v1.0.1 — 28 Oct 2026
- Statistics: the median of an even number of answers is now the average of the two middle values (before it took the upper one), and SD is the sample SD (n − 1), the same as SPSS / Excel STDEV — outlier checks use it too.
- KoBo API pull now follows KoBo's page links, so forms with more than one page of submissions come in complete.
- Add indicator: the answer box suggests the answers found in your data, and an answer that no record has is refused ("Yes" also finds "yes").
- Bangla wording: "রেকর্ড", "প্রশ্ন" no longer show as "টি রেকর্ড" on their own; "২টি প্রশ্নে".
- Dataset import date showed the previous day for imports after midnight — fixed.
- "Shorter than (minutes)" box accepts Bangla digits.
