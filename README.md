# ELIEBOT - Bot Chat Messenger

![شعار ELIEBOT](https://i.ibb.co/PZxFWbhY/image.jpg)

Node.js Support v16.x | نسخة ELIEBOT معدلة من Goat Bot الأصلي | تم التعديل بواسطة الفريدو

---

<p align="center">
  <table>
    <tr>
      <td><a href="#-ملاحظة" style="text-decoration:none"><kbd>📝 Note</kbd></a></td>
      <td><a href="#-المتطلبات" style="text-decoration:none"><kbd>🚧 Requirement</kbd></a></td>
      <td><a href="#-الدروس-التعليمية" style="text-decoration:none"><kbd>📝 Tutorial</kbd></a></td>
      <td><a href="#-كيف-يعمل-البوت" style="text-decoration:none"><kbd>💡 How it works</kbd></a></td>
      <td><a href="#️-كيفية-إنشاء-أوامر-جديدة" style="text-decoration:none"><kbd>🛠️ Commands</kbd></a></td>
      <td><a href="#-الدعم" style="text-decoration:none"><kbd>💭 Support</kbd></a></td>
      <td><a href="#-اللغات-المدعومة" style="text-decoration:none"><kbd>📚 Languages</kbd></a></td>
      <td><a href="#-حقوق-الملكية" style="text-decoration:none"><kbd>✨ Copyright</kbd></a></td>
    </tr>
  </table>
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
