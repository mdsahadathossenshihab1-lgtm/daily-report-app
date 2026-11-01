# CallReport Pro — ডেইলি কল রিপোর্ট অ্যাপ

প্রফেশনাল ড্যাশবোর্ডসহ প্রতিদিনের কল রিপোর্ট অ্যাপ। ভিডিও রেফারেন্স ছাড়াই, Shihab-এর নির্দেশে সিম্পল ভার্সনের বদলে নতুন করে প্রফেশনালভাবে বানানো।

## নতুন ওয়ার্কফ্লো (2026-11-01)
- Quick সেভ: কল করার সময় সবকিছু ফিলাপ করতে হবে না — শুধু Agent ID দিন, Invalid নম্বরগুলো পেস্ট করুন (কমা / স্পেস / নতুন লাইন, যেকোনোভাবে, ডুপ্লিকেট অটো বাদ যাবে), Quick বাটনে সেভ করুন। রিপোর্টটি "শুধু Invalid" হিসেবে থাকবে।
- পরে ওই রিপোর্ট Edit করে পুরো ফিলাপ করুন, পুরো সেভে ক্লিক করলেই অটোমেটিক "অ্যাডমিনকে পাঠানোর রিপোর্ট" দেখাবে, বড় কপি বাটনসহ — কপি করে অ্যাডমিনকে পাঠিয়ে দিন।
- ফিল্ড: Date, Time, Agent ID, Total Calls, Connected, Registration, FTD, Invalid Number, Total Amount Recharged, Problems

## ফিচার
- ৩টি ট্যাব: ড্যাশবোর্ড / নতুন রিপোর্ট / সব রিপোর্ট
- ড্যাশবোর্ডে আজকের ও সর্বমোট সামারি, Connected / Registration / FTD রেটের প্রোগ্রেস বার, সাম্প্রতিক রিপোর্ট
- ফিল্ড: Date, Time, Agent ID, Total Calls, Connected, Registration, FTD, Invalid Number (কমা দিয়ে লিস্ট), Total Amount Recharged, Problems
- প্রতিটি রিপোর্টের জন্য দেওয়া ফরম্যাটেই “ফরম্যাট কপি করুন” বাটন
- এডিট / মুছুন, তারিখ ও Agent ID দিয়ে ফিল্টার, CSV ডাউনলোড
- ডেটা ব্রাউজারের localStorage-এ থাকে, কোনো সার্ভার/ডাটাবেস লাগে না
- মোবাইল-ফার্স্ট, PWA manifest সহ — ফোনে Add to Home Screen করা যায়

## চালানো / ডিপ্লয়
শুধু `index.html` খুললেই চলবে। Vercel-এ static সাইট হিসেবে ডিপ্লয় করা যায়, কোনো build step লাগে না।

## Firebase v3 (2026-11-01)
- Project: S A Topup bazar (fir-a-topup-bazar), Realtime Database only, node daily_reports.
- Reports save to Firebase when online, localStorage is offline fallback/cache. Existing users node is NOT touched.
- Note: current Realtime Database rules are open (read/write true) — tighten before production use in a separate step.
