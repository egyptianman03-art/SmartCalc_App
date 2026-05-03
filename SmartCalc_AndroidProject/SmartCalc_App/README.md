# SmartCalc — Ahmed El-aref
## تعليمات بناء APK

### المتطلبات
- Android Studio (أحدث إصدار) — تحميل من: https://developer.android.com/studio
- JDK 11 أو أحدث (بيجي مع Android Studio)

### خطوات البناء

**1. افتح المشروع**
   - شغّل Android Studio
   - اختار: File → Open → اختار فولدر SmartCalc_App

**2. انتظر Gradle يحمّل المكتبات**
   - أول مرة بتاخد 3-5 دقائق

**3. بناء APK للتجربة (Debug)**
   - من القائمة: Build → Build Bundle(s)/APK(s) → Build APK(s)
   - الـ APK هيتحفظ في: app/build/outputs/apk/debug/app-debug.apk

**4. بناء APK للنشر (Release)**
   - Build → Generate Signed Bundle/APK
   - اختار APK
   - اعمل Keystore جديد أو استخدم موجود
   - الـ APK هيتحفظ في: app/build/outputs/apk/release/

### تثبيت APK على الموبايل مباشرة
1. انقل ملف app-debug.apk للموبايل
2. فعّل "تثبيت من مصادر غير معروفة" في الإعدادات
3. افتح الملف وثبّت

### هيكل المشروع
```
SmartCalc_App/
├── app/
│   ├── src/main/
│   │   ├── assets/
│   │   │   └── index.html        ← التطبيق كاملاً
│   │   ├── java/com/ahmedelaref/smartcalc/
│   │   │   └── MainActivity.java ← WebView wrapper
│   │   ├── res/                  ← أيقونات وموارد
│   │   └── AndroidManifest.xml
│   └── build.gradle
├── build.gradle
└── settings.gradle
```
