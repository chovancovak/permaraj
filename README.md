# Perma ráj

Osobní web Karolíny a Kamila o životě na Sedlčansku, permakulturní zahradě, pomalejším tempu, vztahu k místu a budování sousedské komunity.

Tento soubor slouží především jako **paměť projektu pro další práci s ChatGPT/Codexem**. Zachycuje smysl webu, jeho současnou strukturu, vizuální jazyk i technické zvyklosti. Před dalšími úpravami webu je dobré nejprve projít tento README a potom konkrétní soubory, kterých se změna týká.

## Smysl webu

Perma ráj není prezentovaný jako hotový permakulturní projekt ani jako dokonalý návod. Je to živé místo a průběžný záznam toho, jak jedna rodina hledá vlastní způsob života blíž zemi, lidem a svému skutečnému tempu.

Hlavní sdělení webu:

- **Budujeme. Pomalu. S vědomím souvislostí.**
- Perma ráj je místo pro pěstování jídla i sounáležitosti.
- Permakultura zde není pouze zahradnická metoda, ale způsob uvažování, pozorování a hledání vlastních řešení.
- Odpovědí na klimatické a společenské výzvy není jen sledování špatných zpráv, ale konkrétní tvorba v místě, kde žijeme.
- Důležitou součástí projektu jsou hranice, odpočinek, vědomé zpomalení a přijetí toho, že „už všechno máme“.
- Web přirozeně propojuje Perma ráj s projektem [Síla ne](https://silane.cz), nemá se však proměnit v jeho reklamní stránku.

## Lidé a příběh

Na webu vystupují:

- **Karolína**
- její muž **Kamil**
- jejich děti, o nichž web mluví pouze obecně a s respektem k jejich soukromí

Rodina žila v Praze. V roce 2018 našla zahradu na Sedlčansku a postupně zde vytvořila svůj domov a Perma ráj. Dům i zahradu budovali do velké míry vlastníma rukama, nohama a hlavou.

Tón vyprávění je osobní, pravdivý a klidný. Texty nemají vytvářet dojem, že máme hotový recept pro ostatní. Vhodnější je sdílet zkušenosti, otázky, pokusy, chyby a to, co se postupně učíme.

## Obsahové pilíře

### Tady a teď

Úvodní stránka představuje současný Perma ráj, životní postoj rodiny a základní rozcestník webu.

Její hlavní části jsou:

1. hero s fotografií zamlženého jezírka,
2. úvodní příběh rodiny,
3. „Cesta k naději“,
4. „Permakultura srdcem“,
5. „Žitá Síla ne“,
6. rozcestník mezi inspirací v Perma ráji a podporou v Síle ne,
7. manifest „Už všechno máme“.

### Permakultura

Samostatná stránka věnovaná pojetí permakultury v Perma ráji. Její vzhled obsluhuje zejména `_permakultura.scss`.

### Zápisky

Blogová část webu. Zápisky zachycují vývoj pozemku, plánování, stavbu, spirálu, letní kuchyni, vodu v krajině i každodenní zkušenosti.

Aktuálně jsou ve složce `zapisky/` například:

- `001_vyber_pozemku.html`
- `002_planovani.html`
- `003_kadibudka.html`
- `004_spirala.html`
- `006_o-letni-kuchyni.html`
- `007_voda_v_perma_raji_I.html`
- `008_voda_v_perma_raji_II.html`
- `009_voda_v_permaraji_III.html`

Číslování má historickou mezeru; není nutné je zpětně přečíslovávat.

Pro jednotlivý článek slouží layout `_includes/layouts/sablona-article.njk`.

## Obsahový a jazykový styl

Při psaní nových textů zachovat:

- češtinu a přirozený osobní hlas,
- kratší, srozumitelné věty,
- klidný rytmus a dostatek prostoru,
- konkrétní obrazy ze zahrady a každodenního života,
- otevřenost vůči nedokonalosti a procesu,
- propojení osobní zkušenosti se širšími souvislostmi,
- naději založenou na činnosti, vztazích a místě, ne na líbivých heslech.

Vyhýbat se:

- příliš marketingovému nebo sebeoslavnému tónu,
- představě Perma ráje jako hotového „showroomu“,
- moralizování a univerzálním návodům,
- tlaku na výkon, produktivitu a neustálý růst,
- romantizování venkovského života bez přiznání práce, limitů a chyb.

## Technologie

Web je statický a používá:

- **Eleventy (11ty)**,
- **Nunjucks** pro layouty a partialy,
- **SCSS/Sass** pro styly,
- čisté HTML stránky a články,
- Google Fonts.

Konfigurace Eleventy je v `.eleventy.js`. Závislosti a dostupné příkazy je vždy potřeba ověřit v `package.json`; README záměrně nevymýšlí názvy npm skriptů, které zatím nebyly doloženy.

## Struktura projektu

```text
permaraj_web/
├── _includes/
│   ├── layouts/
│   │   ├── base.njk
│   │   └── sablona-article.njk
│   └── partials/
│       ├── footer.njk
│       ├── head.njk
│       └── header.njk
├── _site/                    # vygenerovaný web; neupravovat ručně
├── .vscode/
│   └── settings.json
├── css/                      # zkompilované CSS
├── img/
│   ├── zapisky/
│   ├── 20260314_174551.jpg
│   ├── favicon-32.png
│   ├── favicon-512.png
│   ├── hero_fog.jpg
│   ├── Kamil_Kaja_v_jezeru.jpg
│   └── klid.JPG
├── node_modules/             # instalované závislosti; necommitovat
├── scss/
│   ├── _article.scss
│   ├── _base.scss
│   ├── _footer.scss
│   ├── _header.scss
│   ├── _homepage.scss
│   ├── _permakultura.scss
│   ├── _posts.scss
│   ├── _variables.scss
│   ├── _zapisky.scss
│   └── style.scss
├── zapisky/
│   └── jednotlivé články
├── .eleventy.js
├── .gitignore
├── index.html
├── kadibudka.jpg
├── package-lock.json
├── package.json
├── permakultura.html
└── zapisky.html
```

Skutečný stav složek má vždy přednost před tímto orientačním stromem. Při větší změně struktury je potřeba strom aktualizovat.

## Layouty a partialy

### `base.njk`

Základní obal stránek. Skládá stránku z hlavičky, hlavního obsahu a patičky a vkládá obsah konkrétní stránky přes Nunjucks.

### `sablona-article.njk`

Šablona detailu zápisku. Pracuje s metadaty článku, například:

- `title`
- `datum`
- `perex`
- `tags`
- `picture`
- `picture_title`

Při úpravě šablony zkontrolovat alespoň jeden starší i jeden novější zápisek, protože historické články nemusejí mít vyplněna všechna metadata.

### `head.njk`

Obsahuje:

- dynamický `<title>`,
- meta description,
- Open Graph metadata,
- Twitter Card metadata,
- canonical URL,
- favicon,
- načtení výsledného CSS,
- načtení písem Libre Baskerville a Source Sans 3.

Aktuální výchozí texty:

- description: „Budujeme. Pomalu. S vědomím souvislostí. Permakulturní zahrada a život v tichu Sedlčanska.“
- OG description: „Budujeme. Pomalu. S vědomím souvislostí. Místo pro pěstování jídla i sounáležitosti.“
- výchozí OG obrázek: `/img/zapisky/026/sedici_panacek.png`

Canonical i Open Graph URL používají doménu `https://permaraj.cz`.

### `header.njk`

Aktuální hlavní navigace:

- Tady a teď → `/`
- Permakultura → `/permakultura`
- Zápisky → `/zapisky`

Aktivní stav je nyní v ukázce přidán napevno pomocí `nav__link--active` u úvodní stránky. Pokud se bude navigace rozvíjet, je vhodné aktivní položku odvozovat z `page.url`.

## Vizuální směr

Design propojuje zemitost Perma ráje s typografickým mostem k projektu Síla ne. Má působit klidně, přirozeně, měkce a současně čistě. Důležitý je dostatek prázdného prostoru.

### Typografie

```scss
$font-primary: "Libre Baskerville", serif;
$font-secondary: "Source Sans 3", sans-serif;
```

- **Libre Baskerville**: nadpisy, citace, výrazné nebo intimnější texty.
- **Source Sans 3**: běžný text, navigace a praktické informace.

### Barevná paleta

```scss
$color-perma-green:     #556B2F; // tmavší olivová
$color-perma-moss:      #849060; // mechová zelená
$color-perma-earth:     #7A6247; // hnědá pro text a klidné prvky
$color-perma-clay:      #B85C38; // cihlový akcent a odkazy
$color-perma-bg:        #F4EFE6; // teplý krémový podklad
$color-white:           #FFFFFF; // čisté plochy a boxy
$color-willow-yellow:   #E0E5A1; // jemná žlutá z vrbových kočiček
$color-border-soft:     #D9CDBE; // jemné linky a rámečky
```

Použití barev:

- krémová tvoří hlavní pozadí,
- hnědá je základní barva textu,
- mechová a olivová propojují web se zahradou,
- cihlová slouží jako střídmý akcent,
- žlutá je drobná přírodní „jiskra“, ne dominantní plocha,
- bílá vytváří klidné oddělené bloky.

### Stíny a zaoblení

```scss
$shadow-soft: 0 12px 30px rgba(0, 0, 0, 0.05);

$radius-sm: 0.375rem;
$radius-md: 0.75rem;
$radius-lg: 1.25rem;
```

Stíny mají být velmi jemné. Zaoblení používáme tam, kde podporuje organický dojem, ne automaticky na každém prvku.

## Responzivita a rozměry

```scss
$tablet: 768px;
$pc: 1250px;

$pad-mobile: 20px;
$pad-tablet: 80px;
$pad-pc: 180px;
```

Sdílené mixiny:

```scss
@mixin section-spacing {
  padding: 4rem $pad-mobile;

  @media (min-width: $tablet) {
    padding: 6rem $pad-tablet;
  }

  @media (min-width: $pc) {
    padding: 8rem $pad-pc;
  }
}

@mixin container-limit {
  max-width: 1400px;
  margin-left: auto;
  margin-right: auto;
}
```

Při tvorbě nové sekce nejprve zvážit použití těchto mixinů. Pro dlouhé texty je vhodné vnitřní kontejner dále zúžit přibližně na 650–900 px.

## Pojmenování CSS tříd

Projekt používá převážně BEM styl:

```text
.blok
.blok__prvek
.blok--varianta
.blok__prvek--varianta
```

Příklady:

- `.hero-home__title`
- `.intro__text--lead`
- `.pathway-card--highlight`
- `.section-hero__subtitle`

Při doplňování stylů zachovat toto pojmenování a styly konkrétní stránky ukládat do příslušného SCSS partialu. `style.scss` má sloužit jako vstupní soubor, který ostatní partialy skládá.

## Opakovaně použitelné prvky

### Univerzální hero podstránek

Pro podstránky slouží `.section-hero` s prvky:

- `.section-hero__container`
- `.section-hero__title`
- `.section-hero__subtitle`
- volitelně `.blog-intro-bio`

### Hero úvodní stránky

`.hero-home` používá celoplošnou fotografii s jemným přechodem do krémového pozadí. Hlavní motiv je zamlžené jezírko (`/img/hero_fog.jpg`). Výška je nyní `80vh`.

### Úvodní obsah

Blok `.intro` obsahuje běžné textové sekce, dvousloupcový grid s fotografií, popisek fotografie a citaci.

### Rozcestníkové karty

`.pathways` a `.pathway-card` tvoří dvě karty:

- Inspirace (Perma ráj)
- Podpora (Síla ne)

### Manifest

`.manifest` je klidná bílá sekce s titulkem „Už všechno máme“, textem a fotografií `/img/klid.JPG`.

## Obrázky a přístupnost

- Obrázky ukládat do `img/`; fotografie k jednotlivým zápiskům ideálně do `img/zapisky/`.
- Používat smysluplný `alt`, který stručně popisuje obsah nebo funkci obrázku.
- U čistě dekorativních obrázků lze použít prázdný `alt=""`.
- Pohlídat velikost souborů, aby fotografie zbytečně nezpomalovaly web.
- Neměnit svévolně velikost písmen v existujících názvech souborů; server může rozlišovat `JPG` a `jpg`.
- Při přidání důležité fotografie zvážit moderní formát a responzivní varianty, ale zachovat jednoduchost projektu.

## SEO a sdílení

Každá stránka by měla mít alespoň:

```yaml
---
layout: layouts/base.njk
title: Název stránky
---
```

Při práci na SEO ověřit:

- unikátní a výstižný titulek,
- popis odpovídající konkrétní stránce nebo článku,
- správnou canonical URL,
- `og:url` konkrétní stránky, ne pouze domovské stránky,
- relevantní obrázek pro sdílení,
- správný výsledný HTML výstup v `_site/`.

Do budoucna je vhodné umožnit stránkám a článkům přepisovat výchozí `description` a sdílecí obrázek přes front matter.

## Postup při úpravách

1. Přečíst tento README.
2. Prohlédnout konkrétní HTML/Nunjucks soubor a odpovídající SCSS partial.
3. Před úpravou zjistit, zda stejnou komponentu nepoužívají i jiné stránky.
4. Upravit zdrojové soubory, ne obsah `_site/` ani ručně generované CSS, pokud kompilaci zajišťuje projekt.
5. Spustit příslušný npm příkaz podle `package.json`.
6. Zkontrolovat výsledek na mobilní i široké obrazovce.
7. Ověřit navigaci, odkazy, obrázky, overflow a čitelnost textu.
8. Pokud se mění struktura, designové tokeny nebo hlavní sdělení, aktualizovat tento README.

## Co nyní zkontrolovat nebo opravit

Tyto body byly zachyceny při prvním seznámení s projektem. Před opravou je vhodné otevřít skutečné soubory a potvrdit, že stále platí.

- V ukázce `_variables.scss` je `$color-white` definována dvakrát.
- V ukázce `head.njk` jsou dvakrát vloženy `style.css`, `preconnect` odkazy i Google Fonts.
- V `.hero-home__title` je `size: 4.5rem`; správná CSS vlastnost je `font-size`.
- `.intro__container` je ve SCSS připravený, ale v zaslaném HTML úvodní stránky se nepoužívá. Proto se nemusí uplatnit zamýšlená maximální šířka 900 px.
- Aktivní položka navigace je zřejmě napevno na „Tady a teď“; na podstránkách může být označena nesprávně.
- `og:url` v ukázce míří vždy na domovskou stránku. Pro správné sdílení podstránek by měl vycházet z `page.url`.
- Výchozí OG obrázek `/img/zapisky/026/sedici_panacek.png` nebyl vidět v zaslaném výřezu struktury; ověřit, že v projektu skutečně existuje.
- V `index.html` zkontrolovat vnoření a uzavření sekcí `.pathways` a `.manifest`. Manifest je nyní podle zaslaného kódu vložen uvnitř `.pathways`, což může být záměr, ale pravděpodobně není.

## Důležitá zásada pro další spolupráci

Při zadání nové práce nehádat obsah souborů pouze podle tohoto README. README poskytuje kontext, ale před změnou je vždy potřeba pracovat s aktuálním kódem. Pokud Karolína pošle jen konkrétní výřez, navrhovaná úprava má respektovat i možnost, že zbytek projektu obsahuje další návaznosti.

Pokud se bude měnit něco podstatného, je užitečné na konci práce stručně doplnit:

- co se změnilo,
- které soubory se změnily,
- jak byla změna ověřena,
- zda přibylo něco, co má být zachyceno i zde.

---

Poslední aktualizace README: **24. srpna 2026**
