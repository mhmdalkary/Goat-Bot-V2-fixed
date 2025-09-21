# ELIEBOT - Bot Chat Messenger

![شعار ELIEBOT](https://i.ibb.co/PZxFWbhY/image.jpg)

Node.js Support v16.x | نسخة ELIEBOT معدلة من Goat Bot الأصلي | تم التعديل بواسطة الفريدو

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
- شكر خاص لـ Allou Mohamed لتعديلات المصدر المفتوح		```
    - the handler will automatically add method `delete`, if this method is called, it will delete the message from the set.
    - next, it will check `permission` of the user and `execute` if the user has permission and `log` information to the console.

  - `onReply`:
    - the handler will run when the user `replies` to a `message has messageID` is set in `GoatBot.onReply` as follows:
		```javascript
		// example:
		global.GoatBot.onReply.set(msg.messageID, {
			messageID: msg.messageID,
			commandName,
			// ... and more
		});
		```
    - the handler will automatically add method `delete`, if this method is called, it will delete the message from the set.
    - next, it will check `permission` of the user and `execute` if the user has permission and `log` information to the console.  

  - `onEvent`:
    - the handler will run `when the user has a new event` type `event` (new user join, user leave chat box, change admin box,...)
		```javascript
		// example:
		global.GoatBot.onEvent.set(msg.messageID, {
			messageID: msg.messageID,
			commandName,
			// ... and more
		});
		```
		- it will loop through all `onEvent` and get the command determined by the key `commandName` and execute the `onEvent` in that command.
		- if it return a `function` or `async function` then it will call the function and `log` information to the console.

  - `handlerEvent`:
    - the handler will run `when the user has a new event` type `event` (new user join, user leave chat box, change admin box,...)
    - it will get all the eventCommand set in `GoatBot.eventCommands` (scripts placed in the `scripts/events` folder)
    - it will loop through all `eventCommands` and run the `onStart` in that command.
    - if it return a `function` or `async function` then it will call the function and `log` information to the console.


## 🛠️ **How to create new commands**
- See [here](https://github.com/ntkhang03/Goat-Bot-V2/blob/main/DOCS.md)

## 💭 **Support**
If you have major coding issues with this bot, please join and ask for help.
- https://discord.com/invite/DbyGwmkpVY (recommended)
- https://www.facebook.com/groups/goatbot
- https://m.me/j/Abbq0B-nmkGJUl2C
- ~~https://t.me/gatbottt~~ (no longer supported)
- ***Please do not inbox me, I do not respond to private messages, any questions please join the chat group for answers. ThankThanks!***

## 📚 **Support Languages in source code**
- Currently, the bot supports 2 languages:
- [x] `en: English`
- [x] `vi: Vietnamese`

- Change language in `config.json` file
- You can customize the language in the folder `languages/`, `languages/cmds/` and `languages/events/`

## 📸 **Screenshots**
- ### Bot
<details>
	<summary>
 		Rank system
	</summary>

  - Rank card:
  <p><img src="https://i.ibb.co/d0JDJxF/rank.png" width="399px"></p>

  - Rankup notification:
  <p><img src="https://i.ibb.co/WgZzthH/rankup.png" width="399px"></p>

  - Custom rank card:
  <p><img src="https://i.ibb.co/hLTThLW/customrankcard.png" width="399px"></p>
</details>

<details>
	<summary>
 		Weather
	</summary>
	<p><img src="https://i.ibb.co/2FwWVLv/weather.png" width="399px"></p>
</details>

<details>
	<summary>
 		Auto send notification when have user join or leave box chat (you can custom message)
	</summary>
	<p><img src="https://i.ibb.co/Jsb5Jxf/wcgb.png" width="399px"></p>
</details>

## ✨ **Copyright (C)**
- **[NTKhang (NTKhang03)](https://github.com/ntkhang03)**
 ## Thanks for Allou Mohamed For the open source changes.
