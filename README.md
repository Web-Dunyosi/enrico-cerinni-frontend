# 👔 Enrico Cerini — Kiyim Do'koni Boshqaruvi Tizimi

[![React](https://img.shields.io/badge/React-18.2-blue?logo=react&style=for-the-badge)](https://react.dev/)
[![Vite](https://img.shields.io/badge/Vite-5.2-purple?logo=vite&style=for-the-badge)](https://vitejs.dev/)
[![TailwindCSS](https://img.shields.io/badge/Tailwind_CSS-3.4-38B2AC?logo=tailwind-css&style=for-the-badge)](https://tailwindcss.com/)
[![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](LICENSE)

**Enrico Cerrini** — bu kiyim-kechak do'konlari uchun mo'ljallangan, savdo, ombor, mijozlar va moliya boshqaruvini to'liq avtomatlashtiruvchi zamonaviy va tezkor **ERP & POS (Point of Sale)** tizimining frontend qismidir.

Ushbu loyiha **React 18**, **Vite** va **Tailwind CSS** texnologiyalari asosida yig'ilgan bo'lib, foydalanuvchiga qulay, chiroyli va yuqori darajada interaktiv interfeysni taqdim etadi.

---

## ✨ Tizimning Asosiy Imkoniyatlari (Modullar)

Tizim kiyim do'konining kundalik ish faoliyatini boshqarish uchun zarur bo'lgan barcha modullarni o'z ichiga oladi:

| Modul | Vazifasi va Imkoniyatlari |
| :--- | :--- |
| **📊 Dashboard (Boshqaruv Paneli)** | Do'konning umumiy holati, kunlik/oylik savdo hajmi, foyda va xarajatlar tahlili hamda grafiklar (Recharts yordamida). |
| **🛒 POS / Checkout (Savdo Terminali)** | Mijozlarga tezkor sotuvlarni amalga oshirish, chegirmalar qo'llash, to'lov usulini tanlash (naqd, karta, nasiya) va chek chop etish. |
| **📦 Inventory (Omborxona boshqaruvi)** | Mahsulotlar katalogi, qoldiq hisobi, yangi tovarlarni qabul qilish va ularning atributlari (o'lcham, rang, brend, fasl) bo'yicha filterlash. |
| **👥 Clients (Mijozlar bazasi / CRM)** | Mijozlar ro'yxati, ularning sotib olish tarixi, sodiqlik darajasi (loyalty) va shaxsiy ma'lumotlarini boshqarish. |
| **💸 Debts (Nasiya va Qarzlar)** | Nasiyaga olingan tovarlar hisobi, qarzdorlar ro'yxati, qarz to'lash muddati va to'langan qismlarni nazorat qilish. |
| **💰 Finance (Kassa & Xarajatlar)** | Do'konning barcha daromad va xarajatlari, kassa holati va operatsiyalar tarixini kuzatish. |
| **📈 Reports (Batafsil Hisobotlar)** | Savdo hisobotlari, ommabop mahsulotlar reytingi va biznes rentabelligi bo'yicha tahliliy ma'lumotlar. |
| **📣 Marketing (Aksiyalar)** | Aksiyalar, chegirmali kodlar (promokodlar) va reklama kampaniyalarini boshqarish. |
| **⚙️ Settings (Tizim Sozlamalari)** | Tizim parametrlari hamda mahsulotlar uchun ranglar, o'lchamlar, fasllar va brendlar katalogini sozlash. |

---

## 🛠️ Texnologik Stack (Frontend)

Loyiha eng zamonaviy va barqaror kutubxonalar yordamida qurilgan:

- **Karkas:** React (v18.2) + Vite (v5.2) — tezkor yig'ish va HMR (Hot Module Replacement) uchun.
- **Dizayn va Stil:** Tailwind CSS (v3.4) + Autoprefixer & PostCSS — moslashuvchan (responsive) va zamonaviy UI.
- **Yo'naltirish (Routing):** React Router DOM (v6.22) — sahifalararo silliq o'tishlar uchun.
- **So'rovlar (API Client):** Axios (v1.6) — backend bilan xavfsiz va tezkor ma'lumot almashinuvi uchun.
- **Forma Boshqaruvi:** React Hook Form (v7.50) — formalarni validatsiya qilish va boshqarish.
- **Vizualizatsiya (Grafiklar):** Recharts (v2.12) — biznes tahlillarini chiroyli grafiklar shaklida ko'rsatish.
- **Ikonkalar:** Lucide React (v0.344) — minimalistik va chiroyli piktogrammalar.
- **Bildirishnomalar:** React Hot Toast (v2.4) — foydalanuvchiga jarayonlar haqida interaktiv xabarlar ko'rsatish.

---

## 📂 Loyiha Strukturasi

Loyiha papkalari strukturasi quyidagicha tashkil etilgan:

```text
enrico-cerrini-frontend/
├── public/                 # Statik resurslar (rasmlar, ikonka va b.)
├── src/
│   ├── api/                # Backend API so'rovlari va sozlamalari
│   ├── components/         # Qayta ishlatiladigan UI komponentlar
│   │   ├── checkout/       # POS checkout qismiga oid komponentlar
│   │   ├── dashboard/      # Dashboardga oid vizualizatsiyalar
│   │   ├── debts/          # Qarzlar modulining komponentlari
│   │   ├── layout/         # Sahifa maketlari (Header, Sidebar, Footer)
│   │   ├── ui/             # Umumiy UI elementlar (Button, Input, Modal, Badge)
│   │   └── ...             # Rang, O'lcham, Brend va boshqa modal komponentlar
│   ├── contexts/           # Global holat (State) boshqaruvi (Auth, AppContext)
│   ├── hooks/              # Custom React hooklar
│   ├── pages/              # Asosiy sahifalar (Dashboard, Inventory, Checkout, va h.k.)
│   ├── styles/             # Global stillar
│   ├── utils/              # Yordamchi funksiyalar (sana formatlash, valyuta va b.)
│   ├── App.jsx             # Ilovaning asosiy kirish komponenti va routerlar
│   ├── main.jsx            # Ilovani DOMga render qiluvchi fayl
│   └── index.css           # Tailwind va global stillar fayli
├── Dockerfile              # Docker orqali build qilish sozlamalari
├── docker-compose.prod.yml # Production uchun to'liq infra-sozlamalar
├── nginx.conf              # Nginx teskari proksi va havfsizlik sozlamalari
├── vite.config.js          # Vite konfiguratsiya fayli
└── package.json            # Loyiha sozlamalari va paketlari
```

---

## 🚀 Loyihani Ishga Tushirish

### 1. Oldindan talab qilinadigan danturlar:
- [Node.js](https://nodejs.org/en) (v18 yoki undan yuqori)
- npm yoki yarn paket menejeri

### 2. Loyihani yuklab olish va paketlarni o'rnatish:
```bash
# Loyihani yuklab oling (agar klon qilinmagan bo'lsa)
git clone <loyiha-repositoriyasi-linki>
cd enrico-cerrini-frontend

# Kutubxonalarni o'rnating
npm install
```

### 3. Konfiguratsiya (.env sozlamalari):
Loyiha ildiz papkasida `.env` faylini yarating (yoki `env.example` dan nusxa oling) va quyidagi o'zgaruvchilarni kiriting:
```env
# Backend API manzili
VITE_API_URL=http://localhost:8000

# Ilova nomi
VITE_APP_NAME="Enrico Cerrini"
```

### 4. Dasturni ishga tushirish:
```bash
# Local muhitda ishga tushirish (Development)
npm run dev

# Production uchun build olish
npm run build

# Olingan buildni tekshirib ko'rish (Preview)
npm run start
```

---

## 🐳 Docker Orqali Ishga Tushirish (Production)

Loyiha production muhitida ishlashga tayyor holda Docker konfiguratsiyalariga ega. Docker Compose backend, postgres va nginx proksini birgalikda ishga tushiradi.

### Loyihani build qilish va ishga tushirish:
```bash
# Docker konteynerlarini orqada fon rejimida yoqish
docker-compose -f docker-compose.prod.yml up --build -d
```

### Nginx va Tarmoq Sozlamalari (`nginx.conf`):
Tizimda xavfsizlik va tezlikni ta'minlash uchun Nginx konfiguratsiyasi mavjud:
- **Teskari Proksi (Reverse Proxy):** So'rovlar `/` orqali frontendga, `/api/` orqali backendga yo'naltiriladi.
- **Xavfsizlik Sarlavhalari (Security Headers):** Clickjacking va XSS xujumlaridan himoya qilish uchun maxsus sarlavhalar sozlangan.
- **Gzip Siqish (Compression):** Statik fayllar (JS, CSS) hajmini kamaytirib, yuklanish tezligini oshiradi.
- **Tezlikni Cheklash (Rate Limiting):** API bo'limiga daqiqasiga ruxsat berilgan so'rovlar sonini nazorat qiladi (masalan, login uchun qat'iy cheklov).

---

## 🔒 Xavfsizlik bo'yicha tavsiyalar
- Productionda ishga tushirishdan oldin `env.production` faylidagi `POSTGRES_PASSWORD`, `JWT_SECRET` va `JWT_REFRESH_SECRET` qiymatlarini mutlaqo o'zgartiring.
- HTTPS protokolini yoqish uchun SSL sertifikatlarini `./ssl` papkasiga joylashtiring.

---

## 📄 Litsenziya

Ushbu loyiha **MIT** litsenziyasi ostida tarqatiladi. Batafsil ma'lumot uchun `LICENSE` fayliga qarang.
