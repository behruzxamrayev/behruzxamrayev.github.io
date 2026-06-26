# Mening Blogim

Oddiy va tez personal blog sayt — faqat HTML, CSS va JS bilan.

## Fayl tuzilmasi

```
blog/
├── index.html          ← Bosh sahifa
├── blog.html           ← Barcha maqolalar ro'yxati
├── about.html          ← Men haqimda
├── css/
│   └── style.css       ← Barcha stillar
└── blog/
    ├── birinchi-maqola.html
    ├── ikkinchi-maqola.html
    └── ...             ← Yangi maqolalar shu yerga
```

## GitHub Pages ga joylashtirish (bepul hosting)

### 1-qadam: GitHub repository yaratish

1. [github.com](https://github.com) ga kiring
2. "New repository" tugmasini bosing
3. Repository nomini **`username.github.io`** qiling  
   (username — sizning GitHub username'ingiz)
4. "Public" tanlang
5. "Create repository" bosing

### 2-qadam: Fayllarni yuklash

**Variant A — GitHub sahifasidan:**
1. Repository sahifasida "uploading an existing file" ni bosing
2. Barcha fayllarni sudrab tashlang
3. "Commit changes" bosing

**Variant B — Git bilan (tavsiya etiladi):**
```bash
git init
git add .
git commit -m "Birinchi commit"
git branch -M main
git remote add origin https://github.com/username/username.github.io.git
git push -u origin main
```

### 3-qadam: GitHub Pages yoqish

1. Repository → Settings → Pages
2. Source: "Deploy from a branch"
3. Branch: `main` → `/root`
4. Save

Bir necha daqiqadan so'ng saytingiz **`https://username.github.io`** manzilida tayyor bo'ladi!

---

## Yangi maqola qo'shish

1. `blog/` papkasida yangi `.html` fayl yarating  
   Masalan: `blog/yangi-maqola.html`

2. Mavjud maqola faylidan nusxa oling va matnni o'zgartiring

3. `blog.html` da yangi maqolani ro'yxatga qo'shing:
```html
<li class="post-item">
  <a href="blog/yangi-maqola.html">Yangi maqola sarlavhasi</a>
  <span class="post-date">25 Yanvar</span>
</li>
```

4. `index.html` dagi "So'nggi maqolalar" ga ham qo'shing

---

## O'zingiznikiga moslash

- `index.html` — ismingiz va tavsifni o'zgartiring
- `about.html` — o'zingiz haqingizni yozing
- `css/style.css` da `--accent: #2d5a3d;` rangni istaganingizga o'zgartiring
- `ismingiz.uz` ni o'z domen nomingizga almashtiring

## O'z domeningizni ulash (ixtiyoriy)

Agar `ismingiz.uz` domen xaridsangiz:
1. Repository → Settings → Pages → Custom domain
2. Domeningizni kiriting
3. Domen registratorda DNS sozlamalarida CNAME yozuvini qo'shing:
   `www` → `username.github.io`
