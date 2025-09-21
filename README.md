# ELIEBOT - Bot Chat Messenger

![شعار ELIEBOT](https://i.ibb.co/PZxFWbhY/image.jpg)

Node.js Support v16.x | نسخة ELIEBOT معدلة من Goat Bot الأصلي | تم التعديل بواسطة الفريدو

<p align="center">
  <a href="https://nodejs.org/dist/v16.20.0">
    <img src="https://img.shields.io/badge/Node.js-16.x-brightgreen?style=for-the-badge" alt="Node.js Support">
  </a>
  <a href="#-ملاحظة"><img src="https://img.shields.io/badge/Note-📝-blue?style=for-the-badge" alt="Note"></a>
  <a href="#-المتطلبات"><img src="https://img.shields.io/badge/Requirement-🚧-orange?style=for-the-badge" alt="Requirement"></a>
  <a href="#-الدروس-التعليمية"><img src="https://img.shields.io/badge/Tutorial-📝-purple?style=for-the-badge" alt="Tutorial"></a>
  <a href="#-كيف-يعمل-البوت"><img src="https://img.shields.io/badge/HowItWorks-💡-green?style=for-the-badge" alt="How it works"></a>
  <a href="#️-كيفية-إنشاء-أوامر-جديدة"><img src="https://img.shields.io/badge/Commands-🛠️-blueviolet?style=for-the-badge" alt="Commands"></a>
  <a href="#-الدعم"><img src="https://img.shields.io/badge/Support-💭-yellow?style=for-the-badge" alt="Support"></a>
  <a href="#-اللغات-المدعومة"><img src="https://img.shields.io/badge/Languages-📚-lightgrey?style=for-the-badge" alt="Languages"></a>
  <a href="#-حقوق-الملكية"><img src="https://img.shields.io/badge/Copyright-✨-red?style=for-the-badge" alt="Copyright"></a>
</p>

---

<div style="background: linear-gradient(90deg, #fbc2eb 0%, #a6c1ee 100%); padding: 10px; border-radius: 8px;">
## 📝 ملاحظة
هذا بوت محادثة يستخدم حساب شخصي مع Facebook API غير رسمي، وقد يؤدي استخدامه إلى حظر الحساب بسبب الرسائل المزعجة أو أسباب أخرى.  
يوصى باستخدام حساب تجريبي يمكن التخلص منه في أي وقت.  
**ELIEBOT** غير مسؤول عن أي مشاكل قد تنتج عن استخدام البوت.
</div>

---

<div style="background: linear-gradient(90deg, #f7971e 0%, #ffd200 100%); padding: 10px; border-radius: 8px;">
## 🚧 المتطلبات
- Node.js 16.x  
- معرفة بالبرمجة، Javascript، Node.js  
- معرفة بـ Facebook API غير الرسمي
</div>

---

<div style="background: linear-gradient(90deg, #6a11cb 0%, #2575fc 100%); padding: 10px; border-radius: 8px;">
## 📝 الدروس التعليمية
- للهواتف المحمولة: [YouTube Tutorial](https://www.youtube.com/watch?v=grVeZ76HlgA)  
- للـ VPS أو Windows: [YouTube Tutorial](https://www.youtube.com/watch?v=uCbSYNQNEwY)  
</div>

---

<div style="background: linear-gradient(90deg, #11998e 0%, #38ef7d 100%); padding: 10px; border-radius: 8px;">
## 💡 كيف يعمل البوت؟
- يستخدم البوت Facebook API غير الرسمي لإرسال واستقبال الرسائل  
- عند حدوث حدث جديد (رسالة، رد فعل، انضمام مستخدم، مغادرة مستخدم...) يقوم البوت بإرسال الحدث للـ handlerEvents  

### handlerEvents الرئيسية:
- **onStart**: يتحقق من الأوامر، صلاحيات المستخدم، وحظر الحساب قبل تنفيذ الأمر  
- **onChat**: ينفذ عند إرسال المستخدم رسالة ويتحقق من صلاحياته قبل تنفيذ الأمر  
- **onFirstChat**: ينفذ عند أول رسالة من المستخدم منذ تشغيل البوت  
- **onReaction**: ينفذ عند تفاعل المستخدم مع رسالة محددة  
- **onReply**: ينفذ عند رد المستخدم على رسالة محددة  
- **onEvent**: ينفذ عند حدوث أحداث مثل انضمام/مغادرة مستخدم أو تغيير صلاحيات المشرف
</div>

---

<div style="background: linear-gradient(90deg, #ff416c 0%, #ff4b2b 100%); padding: 10px; border-radius: 8px;">
## 🛠️ كيفية إنشاء أوامر جديدة
- انظر مجلد `commands` و `events` للحصول على أمثلة  
- في VSCode يمكن استخدام Snippets: `GoatBotCommandCreate` أو `GoatBotEventCreate` (اضغط tab للانتقال للعنصر التالي)  
- الملفات التي تنتهي بـ `.eg.js` لن تُحمّل، غيّر الامتداد إلى `.js` لتفعيلها
</div>

---

<div style="background: linear-gradient(90deg, #feda75 0%, #fa7e1e 100%); padding: 10px; border-radius: 8px;">
## 💭 الدعم
- [Discord](https://discord.com/invite/DbyGwmkpVY) (موصى به)  
- [Facebook Group](https://www.facebook.com/groups/goatbot)  
- [Messenger Chat](https://m.me/j/Abbq0B-nmkGJUl2C)  

> يرجى عدم إرسال رسائل خاصة للمطور، استخدم مجموعات الدعم للرد على الأسئلة
</div>

---

<div style="background: linear-gradient(90deg, #bdc3c7 0%, #2c3e50 100%); padding: 10px; border-radius: 8px;">
## 📚 اللغات المدعومة
- en: English  
- vi: Vietnamese  

يمكن تغيير اللغة في ملف `config.json` أو في المجلد `languages/`، `languages/cmds/`، و `languages/events/`
</div>

---

<div style="background: linear-gradient(90deg, #ff512f 0%, #dd2476 100%); padding: 10px; border-radius: 8px;">
## ✨ حقوق الملكية
- المشروع الأصلي: NTKhang (Goat Bot)  
- النسخة المعدلة: **ELIEBOT** بواسطة **الفريدو**  
- شكر خاص لـ Allou Mohamed لتعديلات المصدر المفتوح
</div>
