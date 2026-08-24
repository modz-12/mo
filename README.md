# Anime Mods v30

نسخة Single-File فعلية: كل واجهة الموقع وCSS وJavaScript وFirebase داخل `index.html`.

## Firebase
- Authentication: Email/Password + Google.
- Firestore: المستخدمون، المنشورات، التعليقات، الإشعارات، الأنمي، المانجا، النوادي، البلاغات، التقييمات، الرسائل.
- لا تستخدم Firebase Storage.
- الصور والفيديوهات والفصول تعتمد على روابط خارجية مباشرة.

## أهم المجموعات
users, posts, comments, notifications, animes, mangas, clubs, reports, calendar, badges, follows, ratings, messages

## التشغيل
1. أنشئ Firestore Database.
2. فعّل Email/Password وGoogle من Authentication.
3. اجعل البريد `modz57713@gmail.com` حساب المشرف/المالك.
4. انشر قواعد `firestore.rules`.
5. ارفع `index.html` و`firebase.json` إلى Firebase Hosting.

## النشر
firebase deploy --only firestore:rules
firebase deploy --only hosting

ملاحظة: قواعد Firestore تمنع عمليات إدارة الأنمي والمانجا إلا للمشرف. لا توجد بيانات تجريبية مضمّنة؛ يتم إنشاء المحتوى من لوحة الإدارة أو من المستخدمين الحقيقيين.
