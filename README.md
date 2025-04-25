# WebShaolin
## Struktura
- css Cascading Style Sheet
- js: Java Script 
- assets/images: Obrazky
- components: js kod
- data: data pro eshop'

## ✅ **ToDo List**

### 📁 **1. Úprava struktury složek**
- [ ] Přesunout všechny CSS soubory do složky `/css`
- [ ] Přesunout všechny obrázky do složky `/assets/images`
- [ ] Přesunout JavaScript soubory do `/js`
- [ ] Vytvořit složku `/components` pro komponenty jako hlavička a patička
- [ ] Vytvořit složku `/data` a umístit tam `produkty.json` se seznamem produktů

---

### 🧹 **2. Refaktoring ukol.html**
- [ ] Přejmenovat `ukol.html` na `index.html`
- [ ] Vytvořit tři nové HTML stránky:
  - [ ] `produkty.html` – přehled produktů
  - [ ] `obcanstvi.html` – stránka o projektu (případně přejmenovat na něco výstižnějšího)
  - [ ] `kontakt.html` – kontaktní formulář / informace

---

### 🧩 **3. Web Components**
- [ ] Vytvořit soubor `/components/my-header.js` a definovat vlastní `<my-header>` element
- [ ] Vytvořit soubor `/components/my-footer.js` pro `<my-footer>`
- [ ] Vytvořit `/components/my-cart.js` pro jednoduché zobrazení počtu položek v košíku

---

### 🛒 **4. Košík (JavaScript + LocalStorage)**
- [ ] Na stránce `produkty.html` přidat tlačítka „Přidat do košíku“
- [ ] Při kliknutí uložit produkt do `localStorage`
- [ ] Na stránce `kosik.html` zobrazit seznam přidaných produktů z `localStorage`
- [ ] Přidat funkci „Odstranit z košíku“ a „Vyčistit košík“
- [ ] Možnost zobrazit počet položek v `<my-cart>` nebo v hlavičce

---

### 🎨 **5. Styling**
- [ ] Vytvořit a upravit `/css/style.css` pro globální styly
- [ ] Zajistit, že všechny HTML soubory správně načítají CSS přes relativní cesty

---

### 🌐 **6. GitHub Pages**
- [ ] Vytvořit GitHub repozitář a pushnout projekt
- [ ] Aktivovat GitHub Pages (branch: `main`, složka `/`)
- [ ] Otestovat, že web běží z veřejné URL

---

### 📜 **7. Budoucí pravidla a konvence (legend)**
- [ ] Dodržovat `lowercase-kebab-case` pro názvy souborů a složek
- [ ] Vyhýbat se diakritice, mezerám a velkým písmenům ve jménech
- [ ] Vše strukturovat **modulárně** – komponenty, styly, data zvlášť
- [ ] Používat **relativní cesty** ke všem souborům

---

## future coding legend
Modularita – Každá věc má svoje místo.
- CSS má svou složku, JavaScript taky.
- Komponenty (např. hlavička nebo patička) patří zvlášť – ať v tom není guláš.
  
Relativní cesty – „Kámo, ať to funguje všude!“
Chceš, aby ti odkazy na obrázky, styly nebo skripty fungovaly doma, na GitHubu i ve škole? Používej relativní cesty:
- Nepiš žádný H:\Python\logo.png, to fakt ne.
   
Názvy složek souvisle a malými písmeny – „lowercase-kebab-case 4ever“ 
Nepoužívej mezeru, nepiš s velkými písmeny, a žádný Componenty nebo MyHeader, vyhoď diakritiku!.
Drž se stylu:
```
my-header.js
product-list.js
footer.html
```
## Použij GitHub Pages!
GitHub Pages je služba, která ti zdarma umožní nasadit (publikovat) eShop z GitHub repozitáře na internet.

- EShop projekt uz máš
- Nahraješ ho na GitHub, uz je taky hotové
- GitHub Pages ti ho udělá živý web s vlastní URL
A nepotřebuješ žádný server, žádný hosting, žádný backend.

## Hints
- Jak  predavat a uchovavat data pomoci Java Scriptu? Pouzij LocalStorage
    https://html.spec.whatwg.org/multipage/#toc-webstorage 

```
// Uložit data
localStorage.setItem("jmeno", "Filip");

// Načíst data
let jmeno = localStorage.getItem("jmeno");  // "Filip"

// Smazat položku
localStorage.removeItem("jmeno");

// Vyčistit celé localStorage
localStorage.clear();
```


- Web Components - Můžeš vytvořit vlastní HTML tagy jako <my-header> a naplnit je pomocí JavaScriptu.

```
class MyHeader extends HTMLElement {
  connectedCallback() {
    this.innerHTML = `
      <header>
        <h1>Můj E-Shop</h1>
        <nav>
          <a href="index.html">Domů</a>
          <a href="produkty.html">Produkty</a>
          <a href="kosik.html">Košík</a>
        </nav>
      </header>
    `;
  }
}

customElements.define('my-header', MyHeader);
```

- struktura webu
```
/WebShaolin/
│
├── index.html                # Domácí stránka (misto Ukol.htm)
├── produkty.html             # Stránka s výběrem produktů
├── kosik.html                # Stránka s košíkem
│
├── /assets/                 # Statické soubory (obrázky, fonty, atd.)
│   ├── /images/             # Obrázky, loga
│
├── /components/             # Web Components (hlavička, patička, atd.)
│   ├── my-header.js
│   ├── my-footer.js
│   └── my-cart.js           # (např. zobrazení počtu položek)
│
├── /css/                    # Stylování webu 
│   └── style.css
│
├── /js/                     # Obecné skripty
│   └── main.js              # Např. zpracování košíku, navigace
│
└── /data/                   # JSON s produkty pro Web 
    └── produkty.json

```













---


