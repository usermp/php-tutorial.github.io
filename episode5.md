
جلسه پنجم
=========

function توابع
--------------

**توابع :** توابع در PHP یکی از اجزای اصلی برنامه نویسی هستند که به شما اجازه می‌دهند کد را تا قطعه‌های کوچکتر تقسیم کرده و از آنها به عنوان بلوک‌های ساخته‌شده و قابل استفاده مجدد در برنامه‌هایتان استفاده کنید. توابع به شما این امکان را می‌دهند که کد خود را به شکل سازمان‌دهی شده‌تر، قابل مدیریت‌تر، و قابلیت استفاده مجدد بالاتری داشته باشید. در ادامه، توضیح کاملی در مورد توابع در PHP ارائه می‌شود.

**تعریف تابع:** شما می‌توانید یک تابع را به کمک کلمه کلیدی **function** در PHP تعریف کنید. معمولاً یک تابع شامل نام تابع، پارامترها (اختیاری) و بلاک کدی است که تابع اجرا می‌کند. مثال:

        function greet($name) {
        echo "سلام، $name!";
        }


**فراخوانی تابع:** بعد از تعریف یک تابع، شما می‌توانید آن را با فراخوانی نام تابع و ارسال مقادیر پارامترها به آن فراخوانی کنید. مثال:

        greet("علی"); // این تابع "سلام، علی!" را چاپ می‌کند


**پارامترها:** توابع می‌توانند پارامترهایی (ورودی‌ها) را بپذیرند. پارامترها درون پرانتز پس از نام تابع تعریف می‌شوند و با کاما از یکدیگر جدا می‌شوند. مقادیری که به عنوان پارامترها فرستاده می‌شوند، در داخل تابع مورد استفاده قرار می‌گیرند. مثال:

        function add($num1, $num2) {
        $result = $num1 + $num2;
        return $result;
        }
        $sum = add(5, 3); // $sum برابر با 8 خواهد بود


**بازگشت مقدار:** توابع می‌توانند مقداری را با استفاده از کلمه کلیدی return به عنوان خروجی برگردانند. این مقدار می‌تواند یک مقدار عددی، متنی، آرایه، یا حتی یک شیء باشد. مثال:

        function multiply($num1, $num2) {
        $result = $num1 \* $num2;
        return $result;
        }

        $product = multiply(4, 7); // $product برابر با 28 خواهد بود


**متغیرهای محلی:** متغیرهایی که در داخل یک تابع تعریف می‌شوند، متغیرهای محلی هستند و تنها در داخل تابع دسترسی دارند. این به شما اجازه می‌دهد تا متغیرهای محلی برای محاسبات مخصوص به تابع استفاده کنید بدون تداخل با متغیرهای خارج از تابع.

**مثال توابع تودرتو:** شما می‌توانید توابع را تودرتو (nested) تعریف کنید، به این معنا که یک تابع دیگر را در داخل یک تابع دیگر فراخوانی کنید. این به شما اجازه می‌دهد که توابع را به شکل سلسله‌مراتبی برای بهبود سازماندهی کدتان استفاده کنید.

        function calculate($a, $b) {
        function add($x, $y) {
        return $x + $y;
        }

        function subtract($x, $y) {
        return $x - $y;
        }

        $sum = add($a, $b);
        $difference = subtract($a, $b);

        return \[$sum, $difference\];
        }

        $result = calculate(10, 5); // $result برابر با آرایه \[15, 5\] خواهد بود


**توضیحات:** توابع می‌توانند توسط توضیحات (داکبلوک) توصیف شوند تا توسعه‌دهندگان دیگر بتوانند بفهمند که چه کاری انجام می‌دهند. توضیحات با استفاده از کلمه کلیدی **/\*\* ... \*/ یا //** در ابتدای تعریف تابع قرار م

        /\*\*
        \* این تابع، دو عدد را جمع می‌کند و نتیجه را برمی‌گرداند.
        \*
        \* @param int $num1 اولین عدد جهت جمع.
        \* @param int $num2 دومین عدد جهت جمع.
        \* @return int جمع دو عدد.
        \*/
        function addNumbers($num1, $num2) {
        // انجام عمل جمع
        $result = $num1 + $num2;

        // بازگرداندن نتیجه
        return $result;
        }


تمرین
-----

**تمرین 1: محاسبه معدل دانشجویی** نوشتن یک تابع به نام calculateAverage که میانگین نمرات دانشجو را محاسبه کرده و آن را برگرداند. تابع باید یک آرایه از نمرات را به عنوان ورودی بپذیرد و میانگین آنها را محاسبه کند.

        function calculateAverage($grades) {
        // محاسبه میانگین نمرات و بازگرداندن آن
        }


**تمرین 2: تبدیل متن به حروف بزرگ** نوشتن یک تابع به نام convertToUppercase که یک رشته را به حروف بزرگ تبدیل کند و نتیجه را برگرداند.

        function convertToUppercase($text) {
        // تبدیل متن به حروف بزرگ و بازگرداندن نتیجه
        }


**تمرین 3: تولید رمز عبور تصادفی** نوشتن یک تابع به نام generateRandomPassword که یک رمز عبور تصادفی با طول مشخص را تولید کند و آن را برگرداند. مثلاً رمز عبور 8 حرفی.

        function generateRandomPassword($length) {
        // تولید رمز عبور تصادفی و بازگرداندن آن
        }


**تمرین 4: تعداد کلمات یک نوشته** نوشتن یک تابع به نام countWords که تعداد کلمات یک نوشته را برا اساس اسپیس شمارش کند

        function countWords($string) {
        // شمارش تعدا کلمات یک رشته
        }


**تمرین 5: محاسبه BMI** نوشتن یک تابع به نام calculateBMI این تابع میزان BMI (شاخص توده بدنی) را بر اساس وزن و قد محاسبه می‌کند.

        function calculateBMI($weightKg, $heightM) {
        // محاسبه BMI
        }


**تمرین 6: بیشترین عدد در یک آرایه** نوشتن یک تابع به نام findMax که بشترین عدد یک آرایه را بازگردانی می کند.

        function calculateBMI($weightKg, $heightM) {
        // بیشترین عدد یک آرایه
        }