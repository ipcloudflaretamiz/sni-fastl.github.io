You
خوب ب جاوا اسکریپت پرا ننوشتی؟
Copilot
درسته. گیت‌هاب از اجرای جاوااسکریپت در فایل‌های Markdown جلوگیری می‌کنه، ولی اگه فایل HTML به صورت جداگانه قرار بگیره، جاوااسکریپت در اون فایل به درستی کار می‌کنه. کد HTML که شامل جاوااسکریپت برای دکمه‌های کپی هست رو باید مستقیم در یک فایل HTML ذخیره کنی.

کد پایتون برای تولید فایل HTML:

python

Copy
def convert_domains_to_html(domain_string):
    domains = domain_string.split()
    html_template = """
<!DOCTYPE html>
<html lang="fa">
<head>
    <meta charset="UTF-8">
    <title>لیست دامنه‌ها</title>
</head>
<body>
    <h2>لیست دامنه‌ها</h2>
    <p>برای کپی کردن هر دامنه، بر روی دکمه کپی کلیک کنید.</p>
    {}
    <script>
    function copyToClipboard(elementId) {{
      var copyText = document.getElementById(elementId);
      copyText.select();
      document.execCommand("copy");
    }}
    </script>
</body>
</html>
"""
    domain_template = """
<div>
  <input type="text" value="{domain}" id="{id}">
  <button onclick="copyToClipboard('{id}')">کپی</button>
</div>
"""
    domain_html = ""
    for i, domain in enumerate(domains, start=1):
        domain_html += domain_template.format(domain=domain.strip(), id=f"domain{i}")
    
    return html_template.format(domain_html)

# رشته‌ی دامنه‌ها
domain_string = """
dmgmbkd.ir mvkbjb.com mdmkvkd.net
"""

# تبدیل دامنه‌ها به HTML
html_output = convert_domains_to_html(domain_string)

# ذخیره کردن به فایل HTML
with open('output.html', 'w', encoding='utf-8') as f:
    f.write(html_output)

print("HTML file generated successfully!")
فایل output.html رو که تولید شده، آپلود کن به ریپازیتوری گیت‌هاب خودت.

در فایل README.md لینک به فایل HTML رو اضافه کن:

markdown

Copy
[برای مشاهده و کپی دامنه‌ها اینجا کلیک کنید](output.html
