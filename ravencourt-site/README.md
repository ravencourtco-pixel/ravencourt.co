# Ravencourt.co — Website

Готова, статична веб-страница за Ravencourt.co (websites, branding, social media & advertising studio).

## Содржина на проектот

- `index.html` — целата страница (nav, hero, услуги, ценовник, контакт)
- `assets/favicon.svg` — favicon (RC monogram)
- `robots.txt`, `sitemap.xml` — за SEO/пребарувачи
- `CNAME` — го содржи `ravencourt.co`, потребен за GitHub Pages да го препознае custom доменот

## Како да се објави (GitHub Pages)

1. Ги качуваш сите фајлови и папки во root-от на овој repo (задржи ја истата структура на папки).
2. **Settings → Pages** → Source: `Deploy from a branch` → Branch: `main`, папка `/ (root)` → Save.
3. Полето "Custom domain" под Pages ќе го препознае `ravencourt.co` од CNAME фајлот автоматски — само провери дека стои таму, ако не, внеси го рачно.
4. Во GoDaddy DNS за `ravencourt.co` додади:
   - 4× A record за `@`: `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - 1× CNAME record: `www` → `ravencourtco-pixel.github.io`

Промените обично важат за неколку минути до 24 часа.

## Responsive

Страницата е тестирана и работи без хоризонтален scroll на:

| Уред | Ширина |
|---|---|
| iPhone SE | 375px |
| iPhone 14 / 15 | 390px |
| Android (Pixel) | 412px |
| Tablet / iPad | 768px |
| Laptop | 1280px |
| Desktop / 4K | 1920px+ |

- Под 820px nav-от станува hamburger мени
- Под 900px картичките со цени одат една под друга
- Типографијата е флуидна (`clamp()`), се скалира со ширината на екранот
- Поддршка за iOS safe-area (notch), touch targets ≥44px, `prefers-reduced-motion`

## Уредување содржина

Целата содржина (текст, цени, линкови) е директно во `index.html` — отвори го во било кој текст едитор и пребарај го текстот што сакаш да го смениш. Боите и растојанијата се CSS променливи на врвот од `<style>` блокот.
