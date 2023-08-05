جلسه چهارم
==========

حلقه ها
-------

**حلقه‌ها یا loops** در زبان برنامه‌نویسی PHP برای تکرار کد و اجرای یک بلاک از دستورات به صورت تکراری استفاده می‌شوند. این ابزار برنامه‌نویسی به شما امکان می‌دهد تا کد‌های تکراری را با حداقل تکرار دستی اجرا کنید، تعدادی از انواع حلقه‌ها در PHP عبارتند از: **for, foreach, while, do while**

**حلقه for:** حلقه for یکی از رایج‌ترین و معمول‌ترین نوع حلقه‌ها در PHP است. این حلقه برای تکرار یک بلاک از دستورات تعداد مشخصی از بارها استفاده می‌شود. ساختار کلی حلقه for به صورت زیر است:

        for ($i = 10;$i <= 10;$i++) {
        // بلاک دستورات که می‌خواهید تکرار شود
        }

        توضیح شروع $i = 10:  این قسمت مشخص می‌کند که حلقه از کجا شروع شود. به طور معمول، یک متغیر کنترلی تعریف می‌شود و مقدار اولیه آن
        تعیین می‌شود.
        توضیح شرط $i <= 10: این قسمت تعیین می‌کند که حلقه تا کجا ادامه یابد. مادامی که شرط برقرار باشد (true)، بلاک دستورات حلقه اجرا
        می‌شود. اگر شرط برقرار نباشد (false)، حلقه پایان می‌یابد.
        توضیح افزایش/کاهش $i++ یا $i--: این قسمت مشخص می‌کند چگونه مقدار متغیر کنترلی در هر دور از حلقه تغییر می‌کند. این مقدار معمولاً
        افزایش یافته یا کاهش می‌یابد تا به شرط خاتمه حلقه برسیم.


مثال:

        for ($i = 1; $i <= 5; $i++){
            echo "شماره: " . $i . PHP\_EOL;
            }
        این کد شماره‌های 1 تا 5 را چاپ می‌کند.


**حلقه while:** حلقه while اجرای بلاک دستورات را تکرار می‌کند تا زمانی که شرط مشخص شده درست باشد. در این نوع حلقه، ابتدا شرط بررسی می‌شود و اگر درست باشد، بلاک دستورات اجرا می‌شود. ساختار حلقه while به این شکل است:

        while ($i <= 5) {
        // بلاک دستورات که می‌خواهید تکرار شود
        }


مثال:

        $i = 1;
        while ($i <= 5) {
        echo "شماره: " . $i . PHP\_EOL;
        $i++;
        }
        این کد همچنان شماره‌های 1 تا 5 را چاپ می‌کند.


**حلقه do-while:** حلقه do-while به همان ترتیبی که حلقه while کار می‌کند، با این تفاوت که ابتدا بلاک دستورات اجرا می‌شود و سپس شرط بررسی می‌شود. بنابراین حداقل یک بار بلاک دستورات اجرا می‌شود حتی اگر شرط اولیه درست نباشد. ساختار حلقه do-while به این شکل است:

        do {
        // بلاک دستورات که می‌خواهید تکرار شود
        } while ($i <= 5);


مثال:

        $i = 1;
        do {
        echo "شماره: " . $i . PHP\_EOL;
        $i++;
        } while ($i <= 5);
        این کد همچنان شماره‌های 1 تا 5 را چاپ می‌کند.


**حلقه foreach:** حلقه foreach یک نوع خاص از حلقه‌ها در PHP است که برای تکرار اعضای یک آرایه یا شیء (object) با استفاده از یک متغیر کنترلی استفاده می‌شود. این نوع حلقه به شما امکان می‌دهد به سادگی از همه عناصر موجود در آرایه یا شیء خود به صورت متوالی بازدید کنید و دستورات مورد نظر خود را اجرا کنید. ساختار کلی حلقه foreach به صورت زیر است:

        foreach ($array\_or\_object as $item) {
        // بلاک دستورات که می‌خواهید برای هر عنصر اجرا شود
        }
        $array\_or\_object: نام آرایه یا شیءی که می‌خواهید از اعضای آن بازدید کنید.
        $item: یک متغیر که در هر مرحله از حلقه، مقدار عنصر فعلی آرایه یا شیء به آن اختصاص می‌یابد.


مثال با آرایه:

        $colors = array("قرمز", "آبی", "سبز", "زرد");
        foreach ($colors as $color) {
        echo $color . PHP\_EOL;
        }
                 این کد همه رنگ‌های موجود در آرایه $colors را چاپ می‌کند.


این‌ها تنها چند نمونه از حلقه‌ها در PHP هستند. همچنین می‌توانید **حلقه‌های تو در تو (nested loops)** نیز بنویسید که یک حلقه دیگر را درون بلاک دستورات یک حلقه دیگر قرار می‌دهد. این قابلیت به شما امکان می‌دهد الگوها و ساختارهای پیچیده‌تری را به صورت تکراری ایجاد کنید.

ترفندهای کار با حلقه
--------------------

در کار با حلقه‌ها در PHP می‌توان خلاقیت به خرج داد. خارج از خلاقیت‌هایی که همیشه در برنامه‌نویسی به کار می‌بریم، دو کلمه کلیدی برای عملیات‌های خاص در حلقه‌ها وجود دارند. **break, continue**

**دستور break:** فرض کنید می‌خواهیم وقتی به عدد 5 رسیدیم، اجرای حلقه به‌طور کامل متوقف شود! یعنی اعداد 5 و 6 و 7 چاپ نشوند. برای این کار از دستور break استفاده می‌کنیم:

        for( $i=1; $i<=7; $i++){
           if( $i==5 ){ break;}
            echo $i . ' ';
        }
        // نتیجه: 1 2 3 4


**دستور continue:** فرض کنید در این حلقه، می‌خواهیم از چاپ عدد 5 جلوگیری کنیم. در حالت قبلی از اجرای حلقه به‌طور کامل جلوگیری شد. اما با اجرای دستور continue فقط اجرای همان دُور از حلقه متوقف شده و به تکرار بعدی منتقل می‌شویم.

        for( $i=1; $i<=7; $i++){
        if( $i==5 ){ continue;}
        echo $i . ' ';
        }
        // Result: 1 2 3 4 6 7