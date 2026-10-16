# بناء تطبيق Blue Mark Sweets لنظام Android

هذا المشروع يغلّف ملفات الموقع الأصلية داخل تطبيق Android باستخدام Capacitor. ملفات الموقع موجودة في `www/`، ولم يُقصد تعديل صفحاتها أو بيانات Firebase.

## إنشاء APK عبر GitHub Actions

1. أنشئ مستودعًا جديدًا في GitHub.
2. ارفع **محتويات هذا المجلد** إلى جذر المستودع (يجب أن يكون `package.json` في الجذر).
3. افتح تبويب **Actions** في المستودع.
4. وافق على تفعيل GitHub Actions إن طُلب منك.
5. شغّل سير العمل **Build Android APK** عبر `Run workflow`، أو ادفع الملفات إلى فرع `main` أو `master`.
6. بعد نجاح العملية، افتح نتيجة التشغيل وانزل إلى **Artifacts**.
7. نزّل `Blue-Mark-Sweets-APK.zip` وفك ضغطه لتحصل على `app-debug.apk`.

## ملاحظات مهمة

- هذا APK تجريبي موقّع بمفتاح debug، مناسب للتثبيت والاختبار. للنشر الرسمي على Google Play، يلزم إعداد توقيع إصدار release بمفتاح خاص.
- التطبيق يحتاج الإنترنت للاتصال بـ Firebase. التخزين المحلي/العمل دون إنترنت يظل محدودًا بما يدعمه كود الموقع وFirestore.
- إذا كان تسجيل الدخول عبر Firebase Authentication مستخدمًا، قد تحتاج إلى إضافة `localhost` إلى Authorized domains في إعدادات Firebase Authentication.
- لم أستطع تشغيل بناء Android فعليًا في هذه البيئة؛ ملف APK نفسه سيُنشأ بعد نجاح GitHub Actions.
