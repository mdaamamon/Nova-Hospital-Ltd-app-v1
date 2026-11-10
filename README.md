# Nova Hospital Ltd – Android App (APK)

এই অ্যাপ ফোনে ইন্সটল করে এক ট্যাপে খুললেই https://novahospitalbd.blogspot.com/ খুলবে।
ওয়েবসাইটে যা বদলাবেন, অ্যাপেও তা-ই দেখাবে (অ্যাপ নতুন করে বানাতে হবে না)।
কল (tel:), ফেসবুক, হোয়াটসঅ্যাপ, ম্যাপ ও অন্য সব লিংক ফোনের নিজস্ব অ্যাপে খোলে।
উপর থেকে নিচে টেনে রিফ্রেশ করা যায়। অ্যাপের নাম: Nova Hospital Ltd

## APK বানানোর ধাপ (সব কাজ GitHub নিজেই করবে)

1. https://github.com এ লগইন করুন → **New repository** → নাম দিন (যেমন `nova-hospital-app`) → **Create repository**।
2. জিপ ফাইলটি কম্পিউটারে Extract করুন। **আপনার লোগো ছবিটি `logo.png` নামে** (ঠিক এই নামে) Extract করা ফোল্ডারের ভেতরে `app` ফোল্ডারের পাশে রাখুন।
3. GitHub রিপোজিটরিতে **uploading an existing file** চাপুন → Extract করা ফোল্ডারের ভেতরের **সব ফাইল ও ফোল্ডার** (`.github`, `app`, `scripts`, `logo.png` সহ) টেনে এনে ছাড়ুন → নিচে **Commit changes**।
   - `.github` ফোল্ডার আপলোড না হলে: **Add file → Create new file** → নামের ঘরে লিখুন `.github/workflows/build-apk.yml` → ফাইলের লেখা কপি-পেস্ট করে Commit করুন।
4. উপরের **Actions** ট্যাব খুলুন। "Build Nova Hospital APK" চলবে (৩–৬ মিনিট)। সবুজ ✔ হলে শেষ।
5. রিপোজিটরির ডান পাশে **Releases** → সর্বশেষটি খুলুন → **NovaHospitalLtd.apk** ডাউনলোড করুন।
   (Releases না পেলে: Actions → সর্বশেষ রান → নিচে **Artifacts** থেকে `NovaHospitalLtd-apk` নামান, Unzip করলে APK পাবেন।)
6. APK ফোনে পাঠিয়ে ইন্সটল করুন। প্রথমবার "Unknown sources / অজানা উৎস থেকে ইন্সটল" অনুমতি দিতে হতে পারে।

## পরে কিছু বদলাতে চাইলে
- **আইকনে লোগো আরও বড়/ছোট:** `scripts/make_icons.sh` ফাইলে `ICON_SCALE` (ডিফল্ট 66) বাড়ান বা কমান।
- **লোগো বদলাতে:** নতুন `logo.png` আপলোড করুন (পুরনোটি Replace হবে) → আবার নিজে থেকেই APK বানাবে।
- **ফেল (লাল ✘) হলে:** Actions-এ ওই রানটি খুলে লাল অংশের লেখা কপি করে আমাকে পাঠান।
- অ্যাপ Android 7.0 বা তার উপরের ফোনে চলবে।
