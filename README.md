# 🎬 Reel Text Generator

<div dir="rtl">

## العربية

<p align="center">
  <img src="https://img.shields.io/badge/HTML-5-E34F26?style=flat-square&logo=html5&logoColor=white"/>
  <img src="https://img.shields.io/badge/CSS-3-1572B6?style=flat-square&logo=css3&logoColor=white"/>
  <img src="https://img.shields.io/badge/JavaScript-Vanilla-F7DF1E?style=flat-square&logo=javascript&logoColor=black"/>
  <img src="https://img.shields.io/badge/Export-Auto%20MP4%20%7C%20WebM-red?style=flat-square"/>
  <img src="https://img.shields.io/badge/Browser%20Support-Chrome%20%7C%20Edge%20%7C%20Firefox-blue?style=flat-square"/>
</p>

<p align="center">
  مولّد نصوص سينمائي يعمل بالكامل داخل المتصفح ويختار تلقائيًا أفضل صيغة تصدير مدعومة حسب المتصفح.
</p>

---

## ✨ المميزات

- 🎥 **اختيار تلقائي للتصدير** — يصدّر **MP4** عندما يكون مدعومًا، ويتحوّل إلى **WebM** في المتصفحات التي لا تدعم التصدير المباشر إلى MP4.
- 🌐 **ثنائي اللغة** — دعم كامل للعربية والإنجليزية مع دعم RTL والتشكيل.
- 🌙 **الوضع الداكن / الفاتح**.
- ⚙️ **قابل للتخصيص بالكامل** — حجم النص، السرعة، عدد الأسطر، التوهج، الاتجاه، والمدة.
- ⚡ **أداء سلس** — المعاينة والتسجيل من نفس مسار الرسم.
- 📐 **مقاس 9:16** — بدقة 1080 × 1920 مناسب للريلز والتيك توك.
- 💾 **ملف HTML واحد** — سهل التعديل والتشغيل والاستضافة.

---

## 🦊 دعم Firefox

يعمل المشروع على **Firefox** بشكل طبيعي، لكن التصدير في النسخة الحالية يكون **WebM** بدل **MP4** المباشر.

- **Chrome / Edge**: تصدير MP4 مباشر عندما يكون مدعومًا.
- **Firefox**: تصدير WebM بشكل ثابت وموثوق.
- **باقي المتصفحات الحديثة**: يتم اختيار أفضل صيغة مدعومة تلقائيًا.

> باختصار: الأداة تعمل على Firefox أيضًا، لكن قد تكون الصيغة النهائية WebM بدل MP4.

---

## 🚀 التجربة المباشرة

👉 **[جرّب الأداة هنا](https://hossam-majrashi.github.io/reel-text-generator/)**

---

## 📸 المعاينة

| الوضع الداكن | الوضع الفاتح |
|-------------|-------------|
| ![dark](https://placehold.co/400x220/0a0a0a/ffffff?text=Dark+Mode) | ![light](https://placehold.co/400x220/f4f4f4/111111?text=Light+Mode) |

---

## 🎬 سلوك التصدير

| المتصفح | نتيجة التصدير | ملاحظات |
|--------|---------------|---------|
| **Chrome / Edge** | **MP4** عند الدعم، وإلا fallback | أفضل تجربة لتصدير MP4 المباشر |
| **Firefox** | **WebM** | تسجيل وتنزيل موثوق |
| **المتصفحات الحديثة الأخرى** | أفضل صيغة مدعومة تلقائيًا | حسب دعم MediaRecorder والترميز |

> التطبيق يفحص دعم المتصفح ويستخدم أفضل صيغة متاحة تلقائيًا.

---

## 🛠️ الاستخدام

**الخيار 1 — مباشر**
```text
حمّل index.html ← افتحه في المتصفح ← ولّد ← سجّل ← نزّل
```

**الخيار 2 — GitHub Pages**
```text
اعمل Fork للمستودع ← Settings ← Pages ← Deploy from main branch
```

**الخيار 3 — خادم محلي**
```bash
# Python
python -m http.server 8080

# Node
npx serve .
```

---

## ⚙️ أدوات التحكم

| الأداة | الوصف |
|-------|-------|
| **Text** | النص الذي يتحرك داخل الفيديو |
| **Text Size** | حجم الخط الأساسي |
| **Speed** | سرعة الحركة |
| **Lines** | عدد الأسطر |
| **Glow** | شدة التوهج |
| **Direction** | اتجاه الحركة |
| **Duration** | مدة التسجيل |
| **Format** | اختيار أفضل سلوك تصدير مدعوم حسب المتصفح |

---

## 🏗️ ملاحظات تقنية

### مسار الرسم
```text
إعدادات النص
     │
     ▼
OffscreenCanvas (1080×1920)
     │
     ▼
Preview Canvas (270×480)
     │
     ▼
مسار التسجيل داخل المتصفح
```

### منطق التصدير
```text
إذا كان MP4 المباشر مدعومًا
     └─ Export MP4

إذا لم يكن MP4 المباشر مدعومًا
     └─ Export WebM
```

### استراتيجية التوافق
- **لا يتم فرض MP4 على كل المتصفحات**.
- **يتم الحفاظ على تنزيل موثوق** خصوصًا في Firefox.
- **الواجهة توضّح السلوك الحقيقي** للمستخدم.

</div>

---

## English

<p align="center">
  <img src="https://img.shields.io/badge/HTML-5-E34F26?style=flat-square&logo=html5&logoColor=white"/>
  <img src="https://img.shields.io/badge/CSS-3-1572B6?style=flat-square&logo=css3&logoColor=white"/>
  <img src="https://img.shields.io/badge/JavaScript-Vanilla-F7DF1E?style=flat-square&logo=javascript&logoColor=black"/>
  <img src="https://img.shields.io/badge/Export-Auto%20MP4%20%7C%20WebM-red?style=flat-square"/>
  <img src="https://img.shields.io/badge/Browser%20Support-Chrome%20%7C%20Edge%20%7C%20Firefox-blue?style=flat-square"/>
</p>

<p align="center">
  A cinematic text animation generator that runs entirely in the browser and automatically uses the best export format supported by your browser.
</p>

---

## ✨ Features

- 🎥 **Automatic export selection** — exports **MP4** where supported and falls back to **WebM** on browsers that do not support direct MP4 export.
- 🌐 **Bilingual** — full Arabic (RTL) + English support, Arabic diacritics supported.
- 🌙 **Dark / Light** theme toggle.
- ⚙️ **Fully customizable** — text size, speed, line count, glow, scroll direction, and duration.
- ⚡ **Optimised render flow** — preview and recording use the same animation pipeline.
- 📐 **9:16 canvas** — 1080 × 1920, ideal for Instagram / TikTok Reels.
- 💾 **Single HTML file** — easy to edit, host, and run locally.

---

## 🦊 Firefox Support

Firefox works correctly in this project, but in the current safe implementation it exports **WebM** instead of direct **MP4**.

- **Chrome / Edge**: direct MP4 export when supported.
- **Firefox**: reliable WebM export.
- **Other modern browsers**: the app automatically chooses the best supported recording format.

> In short: the tool works in Firefox too, but the final file may be WebM instead of MP4.

---

## 🚀 Live Demo

👉 **[Try it here](https://hossam-majrashi.github.io/reel-text-generator/)**

---

## 📸 Preview

| Dark Mode | Light Mode |
|-----------|------------|
| ![dark](https://placehold.co/400x220/0a0a0a/ffffff?text=Dark+Mode) | ![light](https://placehold.co/400x220/f4f4f4/111111?text=Light+Mode) |

---

## 🎬 Export Behavior

| Browser | Export Result | Notes |
|--------|---------------|-------|
| **Chrome / Edge** | **MP4** when supported, otherwise fallback | Best experience for direct MP4 export |
| **Firefox** | **WebM** | Reliable recording and download |
| **Other modern browsers** | Best supported format automatically | Depends on MediaRecorder and codec support |

> The app detects browser support and uses the best available format automatically.

---

## 🛠️ Usage

**Option 1 — Direct**
```text
Download index.html → open it in your browser → generate → record → download
```

**Option 2 — GitHub Pages**
```text
Fork this repo → Settings → Pages → Deploy from main branch
```

**Option 3 — Local server**
```bash
# Python
python -m http.server 8080

# Node
npx serve .
```

---

## ⚙️ Controls

| Control | Description |
|---------|-------------|
| **Text** | The text that scrolls across the reel |
| **Text Size** | Base font size |
| **Speed** | Scroll speed |
| **Lines** | Number of text rows |
| **Glow** | Glow intensity |
| **Direction** | Scroll direction |
| **Duration** | Recording length |
| **Format** | Uses the best supported export behavior for the current browser |

---

## 🏗️ Technical Notes

### Render Pipeline
```text
Text settings
     │
     ▼
OffscreenCanvas (1080×1920)
     │
     ▼
Preview Canvas (270×480)
     │
     ▼
Browser recording pipeline
```

### Export Logic
```text
If direct MP4 is supported
     └─ Export MP4

If direct MP4 is not supported
     └─ Export WebM
```

### Compatibility Strategy
- **Do not force MP4 on every browser**.
- **Keep downloading reliable**, especially in Firefox.
- **Keep the UI honest** about actual export behavior.

---

## 📁 Structure

```text
reel-text-generator/
├── index.html
└── README.md
```

---

## 📄 License

MIT © [Hossam Hassan Majrashi](https://github.com/hossam-majrashi)

---

<p align="center">Built with ❤️ using vanilla HTML · CSS · JavaScript</p>
