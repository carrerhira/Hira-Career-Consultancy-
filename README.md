# Hira Career Consultancy: Website

Ye ek single-page website hai. Content `index.html` mein hai, design `css/style.css` mein, aur logic `index.html` ke andar ek `<script>` tag mein hai.

## Folder structure

```
hira-website/
├── index.html      ← poori website: content (HTML)
├── css/
│   └── style.css   ← design: colours, layout, mobile view
├── js/
│   └── script.js   ← logic: (logic section) Note: don't change anithing
├── assets/
│   └── logo.png    ← aapka logo (PNG, transparent ho to behtar)
└── README.md       ← ye file
```

## Website kaise chalayein

1. `index.html` par double-click karein, browser mein khul jayegi.
2. Live karne ke liye poora `hira-website` folder Netlify Drop (app.netlify.com/drop) par drag karein.

## Content kahan badlein

Sab kuch `index.html` mein hai. Jagah dhoondhne ke liye `<!-- EDIT: ... -->` comments dekhein.

| Kya badalna hai | Kahan |
|---|---|
| WhatsApp number | `<body data-wa-number="917746027982">` (country code ke saath, bina `+` ke) |
| Page title aur description | `<head>` mein `<title>` aur `<meta name="description">` |
| Logo | `assets/logo.png` mein image rakhein. Naam badalna ho to brand ke `<strong>` aur `<small>` text badlein |
| Top bar text | Top bar ke `<span>` tags |
| Hero headline aur intro | `Hero` section (`<h1>`, `<p class="hero-lead">`) |
| Hero card ke steps | `Hero` ke right side wala `<ul class="steps-list">` |
| Services (4 cards) | `Services` section, har `<article class="card">` |
| How we work (3 steps) | `How we work` section, har `<div class="how-step">` |
| Packages aur prices | `Packages` section, har `<article class="plan">`. `featured` class wala card highlight hota hai |
| FAQ | `FAQ` section, har `<details>` |
| Contact email aur phone | Contact section ka `contact-info` part, aur footer |
| Enquiry form fields | Form ke `<div class="field">` blocks. `data-wa-label` wahi naam hai jo WhatsApp message mein jayega |
| Footer text aur developer credit | Sabse neeche `<footer>` |

### Form field kaise add karein

Ek `<div class="field">` copy karein aur ye attributes set karein:

```html
<div class="field">
  <label for="city">City *</label>
  <input id="city" name="city" type="text" required data-wa-label="City" placeholder="e.g. Pune">
</div>
```

- `id` aur `name` unique hone chahiye.
- `data-wa-label` WhatsApp message mein dikhega.
- `required` lagane par field zaroori ho jati hai.
- Poori width chahiye to `<div class="field full">` use karein.

## WhatsApp form kaise kaam karta hai

1. Client form bharta hai aur **Send company enquiry** dabata hai.
2. Form check hota hai (required fields, email, phone ke 10 digits).
3. Message ready hota hai aur WhatsApp khulta hai, jahan number pehle se set hota hai.
4. Client WhatsApp mein **Send** dabata hai. Message tabhi jaata hai.

**Mobile:** pehle WhatsApp app khulne ki koshish hoti hai. Agar app na mile to 1.5 second baad WhatsApp Web khulta hai. Ye best-effort hai, kyunki kuch browsers mein app khulne ka sahi pata nahi chalta.

**Desktop:** WhatsApp Desktop ya WhatsApp Web new tab mein khulta hai.

## Design badalna

`css/style.css` ke top par `:root` block mein colours hain:

```css
:root {
  --teal: #1F4E47;   /* main green */
  --gold: #D4A24C;   /* accent */
  --rust: #B5502A;   /* buttons */
  --cream: #FAF6F0;  /* background */
  --navy: #0E2A47;   /* top bar aur footer */
  ...
}
```

Mobile size (720px se kam) par WhatsApp button gol aur chhota ho jata hai, aur sirf icon dikhta hai. Ye `@media (max-width: 720px)` block mein hai.

## Pending items (publish se pehle)

- [ ] **WhatsApp number confirm karein.** Deck mein ``  Website par `7746027982` set hai. Sahi 10-digit number `data-wa-number` mein daalein.
- [ ] **Logo add karein:** `assets/logo.png`.
- [ ] **Email confirm karein:** deck mein `Carrerhira@gmail.com` likha hai. Spelling check karein.
- [ ] **Packages aur prices:** final terms confirm karke update karein.
- [ ] **Privacy Policy aur Terms:** footer ke links abhi `#` par hain. Inke alag pages banane honge.
- [ ] **Developer credit:** footer mein Chandan Patel ka naam aur email hai. If you need help plese contect Me On Email.
- [ ] **Mobile test:** Android aur iPhone par form submit karke WhatsApp khulne ka behaviour check karein.

## Ek zaroori note.

