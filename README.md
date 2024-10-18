import tkinter as tk
import pyperclip

def copy_to_clipboard():
    text = text_area.get("1.0", "end-1c")  # گرفتن متن از text area
    pyperclip.copy(text)
    label.config(text="متن به کلیپ‌بورد کپی شد.")

# ایجاد پنجره
window = tk.Tk()
window.title("کپی دامنه‌ها به گیت‌هاب")

# ایجاد یک text area برای وارد کردن دامنه‌ها
text_area = tk.Text(window)
text_area.pack()

# ایجاد دکمه برای کپی کردن
copy_button = tk.Button(window, text="کپی به کلیپ‌بورد", command=copy_to_clipboard)
copy_button.pack()

# ایجاد یک label برای نمایش پیام
label = tk.Label(window)
label.pack()

window.mainloop()
