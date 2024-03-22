ولاً، تقوم بالاتي بالترتيب الصحيح:

- المتطلبات:
  - 1 كيكا (1GB) رام
  - 2 كيكا (2GB) تخزين
  - حمل Termux
  - عارض RVNC
  - اتصال بالإنترنت

ثانياً، الأوامر:

1. تحديث الحزم:
  
```shell
   pkg update
   pkg install openssl-tool
```
2. تثبيت حزمة wget:
  
```shell
   pkg install wget
```
3. تثبيت حزمة كالي لينكس:
  
```shell
wget -O install-nethunter-termux https://offs.ec/2MceZWr
```
بعدها 
```shell
chmod +x install-nethunter-termux
```
بعدها 
shell
```shell
./install-nethunter-termux

```
4. اختيار نوع والأداء

NetHunter ARM64 (full): إصدار كامل يتضمن العديد من الأدوات والميزات. يناسب الأشخاص الذين يحتاجون إلى مجموعة كاملة من الأدوات والخيارات.

NetHunter ARM64 (minimal): إصدار أقل حجماً يحتوي على عدد مخفض من الأدوات. يمكن أن يكون هذا الخيار مناسبًا لأولئك الذين يرغبون في توفير مساحة التخزين أو يفضلون الحصول على تثبيت أقل.

NetHunter ARM64 (nano): إصدار صغير جداً يحتوي على عدد قليل جداً من الأدوات. يناسب الأشخاص الذين يحتاجون إلى تثبيت سريع وبسيط ولا يهمهم الحصول على العديد من الأدوات.قم بتحديد النسخة التي

اختر 1 او 2 او 3 حسب اختيارك تنتضر التحميل قد يستغرق وقت طويل

اذا ضهر خيارات ربما 4 او 5 مرات اختر حرف Y 

وأنتضر التحميل
 ملاحضه: وزنه 1كيكابيت مضغوط ويتم فك ضغطه بشكل تلقائي ويكون النهائي 8 كيكابات تقريبا 

بعدها تنتضر قليلان ليفك الضغط ويحمل ال rootfs

5. يقول لك هل تريد حذف الملف اكتب N
سوف تضهر لك كلمت KILI بخط اخضر كبير هذا يعني انه اشتغل الان اصبح لديك نضام كالي لينكس مبسط بواجهة ترمنال وكل الاوامر سوف تتنفذ في كالي لينكس ارسل مثلا


```shell
uname```

الا ارسل هذه لكي يعمل كل شيء في نضام كالي

```shell
nethunter```

يضهر لك انك في نضام كالي


6. الان اذا اردت ان تضهر واجه رسوميه بدل اوامر حمل
RVNC

بعدها اذهب ل termux

ونفذ هذه الاوامر بالترتيب

```shell
nethunter kex &
```
وأفتح التطبيق 
واضغط ال (+) الموجود اسفل الشاشه بعدها يضهر لك مربعين الاول تكتب به 
```curl
localhost:5901
```
الثاني  تكتب به اي شيء مثلا
```text
my Test Net hunter```


تضغط Create 
بعدها connect
بعدها يوجهك لشاشه شبه حمراء تضغط Ok الفوق الشاشه


لحل مشكلة
```shell
[Process completed (signal 9) - press Enter]```

ببساطه حمل اولا 
```shell
apt install android-tools```

بعدها تضغط y
بعدها
```shell
adb```

بعدها اذهب للاعدادات> خيارات المطورين>

 تصحيح اخطاء. usp  (فعلها) 

تصحيح الاخطاء لاسلكيا شغلها وانسخ ip الخاص بك
مثل 192.168.0.104:49285 الخ..  انسخه فقط 


بعدها 
```shell
adb pair Yor_Ip```

بعدها يطلب منك رقم تأخذه من كلمة الاتصال عن طريق رمز (الاقتران بواسطة رمز الاقتران) 

تكتب الرمز 
وبعدها اضغط ok او اتصال لكي يتصل 

وبعدها تنفذ هذه الاوامر تنسخها كلها دفعه واحده وتنفذها

```shell
adb shell "/system/bin/dumpsys activity settings | grep max_phantom_processes"

adb shell "/system/bin/dumpsys activity processes -a"

adb shell "/system/bin/device_config set_sync_disabled_for_tests persistent"

adb shell "/system/bin/device_config put activity_manager max_phantom_processes 2147483647"

adb shell settings put global settings_enable_monitor_phantom_procs false```


بعدها افتح الترمنال واكتب
```shell
nh```

وبعدها
```shell
nethunter kex```


بعدين روح للبرنامج وشغله ومبروك عليك الواحه الرسموميه وتضغيل التطبيق 🥱🖤

by: @x10xxx
ch: @l4vl4
