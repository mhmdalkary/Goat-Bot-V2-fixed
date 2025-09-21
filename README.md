# ELIEBOT - Bot Chat Messenger

![شعار ELIEBOT](https://i.ibb.co/PZxFWbhY/image.jpg)

<p align="center">
	<a href="https://nodejs.org/dist/v16.20.0">
		<img src="https://img.shields.io/badge/Nodejs%20Support-16.x-brightgreen.svg?style=flat-square" alt="Nodejs Support v16.x">
	</a>
	<img alt="size" src="https://img.shields.io/github/repo-size/ntkhang03/Goat-Bot-V2.svg?style=flat-square&label=size">
	<img alt="code-version" src="https://img.shields.io/badge/dynamic/json?color=brightgreen&label=code%20version&prefix=v&query=%24.version&url=https://github.com/ntkhang03/Goat-Bot-V2/raw/main/package.json&style=flat-square">
	<img alt="license" src="https://img.shields.io/badge/license-MIT-green?style=flat-square&color=brightgreen">
</p>

---

## 📝 ملاحظة
هذا بوت محادثة يستخدم حساب شخصي مع Facebook API غير رسمي، وقد يؤدي استخدامه إلى حظر الحساب بسبب الرسائل المزعجة أو أسباب أخرى.  
يوصى باستخدام حساب تجريبي يمكن التخلص منه في أي وقت.  
**ELIEBOT** غير مسؤول عن أي مشاكل قد تنتج عن استخدام البوت.

---

## 🚧 المتطلبات
- Node.js 16.x  
- معرفة بالبرمجة، Javascript، Node.js  
- معرفة بـ Facebook API غير الرسمي  

---

## 📝 الدروس التعليمية
- للهواتف المحمولة: [YouTube Tutorial](https://www.youtube.com/watch?v=grVeZ76HlgA)  
- للـ VPS أو Windows: [YouTube Tutorial](https://www.youtube.com/watch?v=uCbSYNQNEwY)  

---

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

---

## 🛠️ كيفية إنشاء أوامر جديدة
- انظر مجلد `commands` و `events` للحصول على أمثلة  
- في VSCode يمكن استخدام Snippets: `GoatBotCommandCreate` أو `GoatBotEventCreate` (اضغط tab للانتقال للعنصر التالي)  
- الملفات التي تنتهي بـ `.eg.js` لن تُحمّل، غيّر الامتداد إلى `.js` لتفعيلها

---

## 💭 الدعم
للمساعدة التقنية، انضم لمجموعات الدعم التالية:  
- [Discord](https://discord.com/invite/DbyGwmkpVY) (موصى به)  
- [Facebook Group](https://www.facebook.com/groups/goatbot)  
- [Messenger Chat](https://m.me/j/Abbq0B-nmkGJUl2C)  

> يرجى عدم إرسال رسائل خاصة للمطور، استخدم مجموعات الدعم للرد على الأسئلة  

---

## 📚 اللغات المدعومة
- en: English  
- vi: Vietnamese  

يمكن تغيير اللغة في ملف `config.json` أو في المجلد `languages/`، `languages/cmds/`، و `languages/events/`

---

## ✨ حقوق الملكية
- المشروع الأصلي: NTKhang (Goat Bot)  
- النسخة المعدلة: **ELIEBOT** بواسطة **الفريدو**  
- شكر خاص لـ Allou Mohamed لتعديلات المصدر المفتوح
