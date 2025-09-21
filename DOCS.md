# ELIEBOT (نسخة معدلة من Goat Bot)

![شعار ELIEBOT](https://i.ibb.co/Mkpv700s/image.jpg)

هذا المشروع عبارة عن نسخة معدلة من **Goat Bot** الأصلي، تم تطويرها من قبل **الفريدو** باسم **ELIEBOT**  
تم تحسين الوظائف وإضافة مرونة أكبر لإدارة أوامر البوت والمحادثات على فيسبوك.

---

## 🛠️ الوظائف المدمجة
- Translate: ترجمة النصوص  
- convertTime: تحويل الوقت بين الصيغ  
- تمكين/تعطيل `process.stderr.clearLine`  
- getExtFromMimeType: استخراج امتداد الملف من نوع MIME  
- getTime: الحصول على الوقت الحالي  
- jsonStringifyColor: عرض JSON بالألوان  
- randomString/Number: توليد سلسلة أو رقم عشوائي  
- findUid Facebook: البحث عن معرف المستخدم في فيسبوك  
- getStreamsFromAttachment: الحصول على تدفقات المرفقات  
- getStreamFromURL: الحصول على تدفق من رابط  
- Google Drive: رفع، حذف، الحصول على الملفات، إلخ…  
- والمزيد… انظر `utils.js` لمزيد من التفاصيل  

---

## 🧠 التحضير قبل الاستخدام
1. تثبيت **Node.js 16.x**  
2. محرر نصوص أو IDE (VSCode، Sublime Text، Atom، Notepad++، …)  
3. معرفة بـ Javascript: المتغيرات، الدوال، الحلقات، المصفوفات، الكائنات، Promise، async/await  
4. معرفة بـ Node.js: require، module.exports  
5. معرفة بـ Facebook Chat API غير الرسمي: api.sendMessage، api.changeNickname …  

---

## ⚠️ قواعد مهمة
- أي محتوى 18+، فحش، إباحية، خيانة، سياسة، إلخ، ممنوع في **ELIEBOT**  
- تعديل الكود أو إضافة أوامر تخالف هذه القواعد يؤدي إلى حظر دائم  
- احرص على مراجعة كل سطر قبل إضافة أو تعديل أي أمر  

---

## 💾 قاعدة البيانات
- الأنواع المتاحة: JSON، SQLite، MongoDB (تحدد في `config.json`)  
- الاستخدام الأساسي: إدارة المستخدمين (Users) والمحادثات (Threads)  

---

## 🚀 كيفية التشغيل
1. انسخ المشروع على جهازك  
2. تأكد من تثبيت الاعتماديات عبر:
   ```bash
   npm install
