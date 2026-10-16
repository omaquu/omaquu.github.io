# Omaquu — GitHub Landing Page / Portfolio Hub

Tyylikäs, moderni ja kevyt Bento Grid -tyylinen aloitussivu GitHub Pagesille. Sisältää sisäänrakennetun suomi/englanti -kielikytkimen (🇫🇮 FI / 🇬🇧 EN), sulavat animaatiot ja dynaamisen korttivalon ilman raskaita riippuvuuksia.

## 🚀 Mukana olevat linkit & projektit

- **Pääsivusto**: [omaquu.com](https://omaquu.com) — Livestriimit & somelinkit
- **Pelit (Tulossa)**:
  - **Tin & Sand** — Diorama-tyylinen WW2 autobattler -strategiapeli
  - **Mindflower** — Diablo-vaikutteinen steampunk ARPG
- **Sovellukset & Työkalut**:
  - **EQCoach** — [https://omaquu.github.io/EQCoach/](https://omaquu.github.io/EQCoach/) (Interaktiivinen valmennustyökalu)
  - **GamerGamma** — [https://omaquu.github.io/gamergamma/](https://omaquu.github.io/gamergamma/) (Gamma-paneelin oma nettisivu) & [GitHub Repo](https://github.com/omaquu/gamergamma)

---

## 🌐 Kaksikielisyys (FI / EN)

Sivun yläkulmassa on kielivalitsin (🇫🇮 FI / 🇬🇧 EN).
- Vaihto tapahtuu välittömästi ilman sivun uudelleenlatausta.
- Valinta tallentuu selaimen muistiin (`localStorage`).
- Voit lisätä tai muokata käännöksiä suoraan `index.html`-tiedoston `i18nData`-oliosta.

---

## 🛠️ Julkaisu GitHub Pagesiin (2 minuuttia)

### Vaihtoehto 1: Pääsivustoksi osoitteeseen `https://omaquu.github.io/` (Suositus)

1. Luo GitHubissa uusi julkinen repositorio nimellä: **`omaquu.github.io`**
2. Kopioi nämä tiedostot (`index.html`, `style.css`, `README.md`) kyseiseen repoon.
3. Tee commit & push:
   ```bash
   git init
   git add .
   git commit -m "Initial commit for landing page"
   git branch -M main
   git remote add origin https://github.com/omaquu/omaquu.github.io.git
   git push -u origin main
   ```
4. Sivusi on heti julki osoitteessa: **`https://omaquu.github.io`**!

---

### Vaihtoehto 2: Erillinen alasivu (esim. `omaquu.github.io/hub`)

1. Luo repositorio esim. nimellä `hub` tai `landing-page`.
2. Puske tiedostot kyseiseen repoon.
3. Mene repositorion asetuksiin: **Settings** -> **Pages** -> Valitse Source: **Deploy from a branch** (Branch: `main`, Folder: `/ (root)`) -> Paina **Save**.

---

## ➕ Miten lisään uuden projektilaatikon?

Avaa `index.html` ja kopioi `bento-grid` -elementin sisälle uusi kortti:

```html
<!-- Uusi projekti -->
<a href="https://linkki-projektiisi.com" target="_blank" rel="noopener noreferrer" class="bento-card col-6">
  <div class="card-top">
    <div class="card-icon icon-purple">
      <!-- Ikoni (SVG) -->
      <svg fill="none" stroke="currentColor" viewBox="0 0 24 24" stroke-width="2">
        <polygon points="12 2 2 7 12 12 22 7 12 2"></polygon>
      </svg>
    </div>
    <div class="card-arrow">
      <svg fill="none" stroke="currentColor" viewBox="0 0 24 24" stroke-width="2">
        <path d="M7 17L17 7M17 7H7M17 7V17"></path>
      </svg>
    </div>
  </div>

  <h3 class="card-title">Projektin Nimi</h3>
  <p class="card-desc">
    Lyhyt kuvaus siitä, mitä tämä tekee tai mistä on kyse.
  </p>

  <div class="tag-list">
    <span class="tag highlight">Tagi 1</span>
    <span class="tag">Tagi 2</span>
  </div>

  <div class="card-action">
    Avaa projekti &rarr;
  </div>
</a>
```

### Laatikon koot:
- `col-12` = Koko rivin levyinen laatikko (kuten omaquu.com pääkortti)
- `col-6` = Puolen rivin levyinen laatikko (2 vierekkäin tietokoneella, 1 mobiilissa)
- `col-4` = Kolmasosan levyinen laatikko (3 vierekkäin tietokoneella)
