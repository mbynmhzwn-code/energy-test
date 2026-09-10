سامانه جزوه‌ها و منابع — مهندسی انرژی شریف

فایل‌های اضافه‌شده:
- notes.html: صفحه عمومی جزوه‌ها و منابع
- admin.html: پنل ورود و آپلود مدیر
- supabase-config.js: کلیدهای عمومی Supabase (anon فقط)
- schema.sql: ساخت جدول و Policyهای پایه

راه‌اندازی:
1) در Supabase یک پروژه رایگان بساز.
2) Authentication > Users > Add user: یک ایمیل و رمز برای مدیر بساز.
3) Storage > New bucket: نام bucket را notes بگذار و Public را فعال کن.
4) SQL Editor را باز کن و schema.sql را اجرا کن.
5) Settings > API، Project URL و anon public key را در supabase-config.js قرار بده.
6) کل پوشه را روی GitHub Pages آپلود کن.

نکته امنیتی:
- service_role key را هرگز در سایت قرار نده.
- در نسخه پایه، هر حساب authenticated امکان آپلود دارد. اگر فقط یک مدیر می‌خواهی، Policyهای storage و جدول notes را با auth.uid() به شناسه همان کاربر محدود کن.
