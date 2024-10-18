<!DOCTYPE html>
<html lang="fa">
<head>
    <meta charset="UTF-8">
    <title>لیست دامنه‌ها</title>
</head>
<body>
    <h2>لیست دامنه‌ها</h2>
    <p>برای کپی کردن هر دامنه، بر روی دکمه کپی کلیک کنید.</p>
    <div>
        <input type="text" value="dmgmbkd.ir" id="domain1">
        <button onclick="copyToClipboard('domain1')">کپی</button>
    </div>
    <div>
        <input type="text" value="mvkbjb.com" id="domain2">
        <button onclick="copyToClipboard('domain2')">کپی</button>
    </div>
    <div>
        <input type="text" value="mdmkvkd.net" id="domain3">
        <button onclick="copyToClipboard('domain3')">کپی</button>
    </div>
    <script>
    function copyToClipboard(elementId) {
        var copyText = document.getElementById(elementId);
        copyText.select();
        document.execCommand("copy");
    }
    </script>
</body>
</html>
