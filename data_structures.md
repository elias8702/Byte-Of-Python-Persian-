<div dir=rtl>

# ساختار داده‌ها

ساختارهای داده اساسا یک *ساختاری* رو در خود نگه داری می‌کند. که این قابلیت را دارند که *داده‌های* را در خود نگه دارند. به عبارت دیگر ساختار داده برای ذخیره سازی مجموعه‌ی از داده‌های به هم مرتبط استفاده می‌‌شود.

در پایتون چهار نوع داده وجود دارد list ،tuple ،dictionary و  set که هر کدام از این‌ها مورد برسی قرار می‌گیرد و خواهید دید که چگونه با استفاده از این ابزارها زندگی خود را راحت‌تر می‌کنیم. 

## لیست 

لیست چیست؟ ساختار داده‌ای است که مجموعه‌ی از ایتم‌های منظم را در خود نگه داری می‌کند. برای مثال این امکان وجود دارد که *دنباله‌ی* از اقلام را در یک لیست ذخیره کنید.
ساده تر بگم تصور کنید که یک لیست خرید دارید که اقلام ان در خط‌های جداگانه نوشته شده درسته؟، در حالی که در پایتون همین لیست بر روی یک خط با کاما از هم جدا شده است. به همین راحتی!!

این لیست اقلام باید `ab` داخل  '[ ]'square brackets گذاشته شوند تا پایتون بفهمد که شما دارید از 'list' استفاده می‌کنید.
بعد ایجاد یک لیست امکاناتی نظیر جتستجو کردن، پاک کردن، اضافه کردن اقلام برخوردار خواهید بود.

از انجای که این لیست قابلیت اضاف‌کردن، پاک‌کردن دارد، پس می‌توانیم بگوییم که این لیست *(از نوع قابل تغییر)mutable* است. به همین راحتی!

## مقدمه‌ کوچکی درباره‌ی اشیاء و کلاس‌ها

گرچه تا به امروز بحث و گفتگو درباره‌ی اشیا و کلاس‌ها را به تاخیر انداخته‌ایم. ولی برای درک بهتر لیست یک توضیح کوچکی نیاز است. این موضوع را در  [بخش بعدی](./oop.md#oop) دقیق برسی خواهیم کرد.

برای درک بهتر به مثال زیر توجه کنید.

وقتی که یک متغییر را مقداری را به ان اختصاص می‌دهیم `i=5` ، یک *شی* ساخته ایم. متغییر `i` کلاسی است از نوع `int`.
برای درک بهتر  `help(int)` را می‌توانید مطالعه کنید.

کلاس‌ها این امکان را دارند که از *methods* استفاده کنند. برای مثال پایتون *متدی* به نام `append` دارد که می‌تواند یک ایتم به انتهای لیست اضافه کند.
برای مثال:  `mylist.append('ali')`

همانطور که در مثال بالا می‌بینید ایتم ali را به mylist اضافه می‌کند. نکته با استفاده از نقطه امکان دسترسی به متد‌های ان اشیا را داریم.

یک کلاس همچنین می‌تواند *fields* داشته باشد. این متغییرها/نام‌ها را زمانی می‌توانید استفاده کنیدکه شی از ان کلاس داشته باشید. فیلد های هم با نقطه قابل دسترس هستند. برای مثال:`mylist.field`




برای مثال (فایل `ds_using_list.py` را ذخیره کنید)

<div dir=ltr>


<pre><code>{% include "./programs/ds_using_list.py" %}</code></pre>

<div dir=rtl>


خروجی:

<div dir=ltr>

<pre><code>{% include "./programs/ds_using_list.txt" %}</code></pre>

<div dir=rtl>




**چگونه و چطور**

متغییر  `zoo` به یک دسته از ایتم‌ها اشاره دارد. همچنین می‌دانیم که تابع `len` می‌تواند طول یک رشته را به دست بیاورد. پس این متغییر به ما می‌گوید که من یک  [رشته](#sequence) هستم.

حالا قسط داریم تمام حیوانات را به یک **باغ وحش جدید چندتایی** ببریم بخاطر اینکه باغ وحش قدیمی دارد بسته می‌شود.بنابراین `new_zoo` حاوی حیواناتی است که در حال حاضر وجود دارند و حیواناتی که از باغ وحش قدیمی گرفتیم. زیادی خوتون گیج و درگیر نکیند کمی جلو تر موضوع را خواهید فهمید.
 
با استفاده از دوجفت  '[ ]' می‌توانیم موقعیت حیوانات را در لیست مشخص کنیم که کدام حیوان در کجا قرار گرفته است. به این روش  _indexing_  می‌گویند.
برای مثال با استفاده از  `[new_zoo[2` امکان دسترسی به سومین بخش از باغ وحش را داریم.
حال به این دستور نگاه کنید  `[new_zoo[2][2` امکان دسترسی به طبقه سوم باغ وحش بخش سوم را داریم. جالب مگه نه!
به این مفهوم در پایتون  tuple (چندتایی) می‌گویند.



<!-- -->

>**نکته برای برنامه‌نویسان پریل**
>
>

دستور لیست هویت خود را همانند پریل از دست نمی‌دهد. این خاصیت در لیست های تو در تو و چندتای هم به همین صورت است. این‌ها شی‌های هستند که ذخیره در شی‌های دیگر می‌شوند.

## لغت نامه 

یک فرهنگ لغت همانند کتابی است با ادرس‌ها وجزییات تماس با افراد تنها با دانستن نام می‌توانید هر کسی را پیدا کنید. این مفهومی است برای دستور 'Dictionary'.
برای مثال ما *keys* را با  *مقداری* مرتبط می‌کنیم.
این تکته را بخاطر داشته باشید که کلید باید منحصر به فرد باشد. چون ممکن است اطلاعات به درستی تحلیل نشوند، برای مثال اگر نام دوفرد مثل هم باشد. ممکن است به فرد مورد نیازی که خواسته بوده‌اید نرسید.

برای نام کلیدها باید نامی باشد که تغییر نیابد ولی برای مقدار ان اگر تغییر یافت مشکلی ندارد. پس برای کلیدها باید یک شی ساده‌ای را استفاده کینم. پس این نتیجه را می‌گیرم که کلیدی که ساخته‌ایم باید منحصربه‌فرد باشد.

جفت کلیدها و مقادیر ان در Dictionary به صورت زیر نوشته می‌شود.`d = {key1 : value1, key2 : value2 }`. همان طور که می‌بینید جفت کلید با ویلگول از هم دیگر جدا شده اند و در یک کروشه قرار گرفته اند.

به یاد داشته باشید داشتن یک جفت کلید عمل مرتب‌سازی اتفاق نمی‌افتد.
اگر یک فرهنگ مرتب می‌خواهید باید از قابل خودتان ان را مرتب کنید.
لغت‌نامه‌هایی که اینجا از ان استفاده می‌کنید جزء اشیاء کلاس `dict` هستند.


برای مثال (فایل  `ds_using_dict.py` را ذخیره کنید)

<div dir=ltr>


<pre><code class="lang-python">{% include "./programs/ds_using_dict.py" %}</code></pre>
<div dir=rtl>


خروجی:
<div dir=ltr>


<pre><code>{% include "./programs/ds_using_dict.txt" %}</code></pre>

 <div dir=rtl>



**چگونه و چطوری**

با استفاده از روش‌های که قبلا گفتیم یک دایرکتوری به نام  `ab` ایجاد می‌کنیم. با رعایت دستور العمل ساده با مشخص کردن دوجفت کلید با استفاده از ایندکس به جفت کلید ارزش می‌دهیم همانطور که در بحث لیست گفته شد.
حال بااستفاده از دوست قدیمی دستور `del` می‌توانیم  key-value را حذف کنیم. کارمون فقط مشخص کردن دایرکتوری  ،ایندکس است که کلید حذف شود از این بعداش با دستور  `del` است. در این روش نیازی به دانستن مقدار کلید نیست.


در گام بعدی با روش   `items` دسترسی به هر جفت کلید دایرکتوری که خودش اجازه دسترسی  tuples و  ایتم ها می‌دهد را  داشته باشیم. این جفت کلید ها را بازیابی می‌کنیم و به ان متیغیر ها  `نام` و  `ادرسی` می‌دهیم.
با استفاده از حلقه  `for..in` این مقادیر را در  for-block چاپ می‌کنیم.


همچنین با استفاده از ایندکس دوجفت کلید دیگر   را اضافه و ارزشی به ان اختصاص دهیم.مثل  موارد فوق که انجام دادیم. 

با استفاده  از اپراتور `in ' می توانیم  بررسی کنیم  که این جفت کلید-ارزش وجود دارد.


برای لیست روش های کلاس `dict`، به« کمک (dict) »مراجعه کنید.

> ** کلمات کلیدی Arguments and Dictionary **
> اگر از روش کلید واژه در توابع خود استفاده کرده‌اید حواستان باشد که در پارامتر تعریف تابع ارزش جفت کلیدها مشخص شده باشد. وقتی کلید را فراخوانی می‌کنید کلیدی از دایرکتوری هاست.(که در جدول کامپایلر به نام  _symbol table_ شناخته می‌شود.


## رشته‌ها

لیست، tuples همه‌ی این‌ها نمونه‌ای از رشته‌ها هستند. ولی چه چیز انقدر رشته ‌ها را خاص می‌کند؟

ویژگی‌ها اصلی عبارت از اند:  *membership tests*، *indexing operations* که این امکان را می‌دهد بخشی از رشته دسترسی مستقیم داشته باشیم.

سه نوع رشته داریم:lists, tuples ،strings

همچنین عملیات *slicing* یا برش دادن که اجازه می‌دهد به بخشی از رشته درسترسی داشته باشیم.


برای مثال (فایل   `ds_seq.py` را ذخیره کنید)

<div dir=ltr>

<pre><code class="lang-python">{% include "./programs/ds_seq.py" %}</code></pre>
 <div dir=rtl>
 
 خروجی:

<div dir=ltr>


<pre><code>{% include "./programs/ds_seq.txt" %}</code></pre>

 <div dir=rtl>
 
 **چگونه و چطوری**
 
اول از همه دیدیم که چگونه از ایندکس استفاده کنیم که ایتم خاصی را از رشته بازمی‌گرداند. این روش در _عملوند‌ها_ اشاره شده است. هر زمان که یک عدد را در پایتون در داخل ` []` بگذارید همانطور که در بالا نشان داده شده است. پایتون ان ایتم را از داخل رشته استخراج می‌کند. این نکته را در نظر داشته باشید که شمارش پایتون از مقدار صفر شروع می‌شود.
از این رو اگر ایتم اول را می‌خواهیم استخراج کنیم باید `[shoplist [0`  از همچین چیزی استفاده کنیم عدد صفر مقدار اولیه ایتم را بازمی‌گرداند.
حال اگر چهارمین ایتم را استخراج کنیم از چه عددی استفاده می‌کنیم؟


بله درست سه : 



<div dir=ltr>
`shoplist[3]`

<div dir=rtl>


ایندکس که برای استخراج رشته به استفاده می‌اید می‌تواند یک عدد منفی باشد. در این صورت رشته را از انتها می‌خوانیم. بنابراین  `[shoplist[-1`  این دستور مقدار اخرین رشته و   `[shoplist[-2` دومین را از اخر رشته بازمی‌گرداند.

عملیات برش دادن هم در داخل ` []`  انجام می‌شود با این تفاوت که عددی که وارد می‌کنیم را با دونقطه از هم دیگر جدا می‌کنیم. این بسیار شبیه همین رشته‌های ایندکسی که در بالا استفاده کردید هست. نکته اعداد اختیاری هستند ولی دونقطه اختیاری نیستند.

اولین شماره قبل از دونقطه عملوند برش هست که از کجا رشته برش می‌خورد. عدد دوم هم که ایندکس رشته هست. اگر شماره اول مشخص نشده باشد پایتون از اول رشته شروع می‌کند، اگر از رشته دوم خارج شود پایتون از انتهای رشته متوقف می‌شود.

نکته قطعه بازگشتی موقعیت  _starts_ از جای شروع، شروع می‌کند و موقعیت پایان درست قبل از  _end_ پایان می‌یابد یعنی موقعیت شروع. پس موقعیت پایان از رشته خذف می‌شود.

پس  `[shoplist[1:3` این تکیه‌ی از رشته در موقعیت یک ۱ را بازمی‌گرداند، که شامل موقعیت دو هم می‌شود که در موقعیت ۳ متوقف می‌شود پس بنابراین یک  *slice* دو ایتم را باز‌میگرداند. به طور مشابه:  `[:]shoplist` این تمامی رشته‌ها را بازمی‌گرداند.

از این استدلال هم می‌توانید استفاده کنید. _step_  برای قطعه‌ها.(به طور پیش فرض هر گام برابر یک  است)

<div dir=ltr>

```python
>>> shoplist = ['apple', 'mango', 'carrot', 'banana']
>>> shoplist[::1]
['apple', 'mango', 'carrot', 'banana']
>>> shoplist[::2]
['apple', 'carrot']
>>> shoplist[::3]
['apple', 'banana']
>>> shoplist[::-1]
['banana', 'carrot', 'mango', 'apple']
```


<div dir=rtl>

نکته وقتی که گام برابر ۲ است موقعیت صفر، دو 0, 2 بازگردانده می‌شود. وقتی گام ۳ است ایتم صفر، سه 0, 3 بازگردانده می‌شود.


با استفاده از ترکیبات مختلف در پایتون به طور تعاملی تر و سریع تر سعی کنید نتایج را بیابید. چیز بزرگ در مورد رشته‌ها این است که  tuples,  lists and strings  می‌توانید به همان شیوه دسترسی پیدا کنید.
