# Katalog programov

Enostranska spletna vitrina za predstavitev programov: slika 16:9 (Imgur) + YouTube video, opis, cena, šifra, kategorije. Admin je zaščiten z GitHub tokenom, podatki se shranjujejo v `data.json` v tem repozitoriju.

## Namestitev (enkrat)

1. Na GitHubu ustvari repozitorij (npr. `programi`) in naloži `index.html` (in ta README).
2. **Settings → Pages → Build and deployment**: Source = *Deploy from a branch*, Branch = `main`, mapa `/ (root)`. Stran bo na `https://UPORABNIK.github.io/programi/`.
3. Ustvari token: **GitHub → Settings → Developer settings → Personal access tokens → Fine-grained tokens → Generate new token**
   - Repository access: *Only select repositories* → samo ta repozitorij
   - Permissions → Repository permissions → **Contents: Read and write**
   - Kopiraj token (`github_pat_…`) in ga shrani na varno mesto.

## Uporaba

- Na strani klikni **Admin** (desno zgoraj), vnesi token (lastnik/repozitorij se izpolnita samodejno na github.io).
- **+ Dodaj program**: naziv, šifra, cena, kategorija, Imgur povezava slike, YouTube povezava, opis.
- **Kategorije** in **Stran** (naslov, podnaslov, kontaktni e-naslov) urejaš prek gumbov v admin vrstici.
- Na koncu klikni **Shrani na GitHub**. Sprememba je na javni strani vidna po približno minuti.

## Opombe

- Slika: uporabi direktno povezavo `https://i.imgur.com/XXXXXXX.jpg` (povezava na stran `imgur.com/XXXXXXX` se pretvori samodejno; albumi `/a/…` ne delujejo).
- Telefon: ko ga zasučeš ležeče, vsaka slika in vsak video zapolni cel zaslon. Dotik slike jo odpre celozaslonsko.
- Token se nikoli ne shrani v repozitorij, ostane samo v tvojem brskalniku (po želji »Zapomni si«).
- Brez `data.json` stran prikaže vzorčni vnos; datoteka nastane ob prvem shranjevanju iz admina.
