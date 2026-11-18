# Generational Ads: website en Google

Alles wat je nodig hebt om generationalads.nl live te zetten en goed vindbaar te maken in Google.

## Wat er in deze map zit

| Bestand | Waarvoor |
|---|---|
| `index.html` | De hele website |
| `assets/` | Screenshots, korte loops en ontwerpen die de site laat zien |
| `favicon.svg`, `apple-touch-icon.png` | Het icoontje in het browsertabblad en op een telefoon |
| `og-image.jpg` | De afbeelding die verschijnt als iemand je link deelt via WhatsApp, LinkedIn of Facebook |
| `robots.txt` | Vertelt Google dat de hele site gelezen mag worden |
| `sitemap.xml` | Vertelt Google welke pagina's er zijn |

Laat alle bestanden en de map `assets` naast elkaar in dezelfde map staan.

## Wat er al voor Google in de site zit

- Een titel en omschrijving voor de zoekresultaten
- Een vast adres (`https://generationalads.nl/`), zodat Google geen dubbele versies ziet
- Bedrijfsgegevens in een vorm die Google begrijpt: naam, Assen, diensten en dat je door heel Nederland werkt
- Een deelafbeelding met je logo
- Beschrijvende teksten bij alle afbeeldingen
- Eén hoofdkop en een duidelijke opbouw van de koppen

## 1. Live zetten op Vercel

1. Log in op vercel.com en maak een nieuw project aan.
2. Sleep deze hele map erin. Een build-instelling is niet nodig, het is gewone HTML.
3. Ga in het project naar **Settings > Domains** en voeg `generationalads.nl` en `www.generationalads.nl` toe.
4. Vercel laat zien welke DNS-records je bij je domeinregistrar moet invullen. Neem ze precies over.
5. Laat `www` doorverwijzen naar `generationalads.nl`, zodat er maar één adres is.
6. Wacht tot Vercel bij beide domeinen een groen vinkje laat zien. Dat kan een paar minuten tot een paar uur duren.

## 2. Contactformulier koppelen

Het formulier verstuurt pas berichten als het aan een inbox gekoppeld is.

1. Ga naar web3forms.com en vul het e-mailadres in waar aanvragen binnen moeten komen.
2. Je krijgt een access key per mail.
3. Zoek in `index.html` naar `key:''` en zet de key tussen de aanhalingstekens, bijvoorbeeld `key:'abc123'`.
4. Upload de site opnieuw en stuur jezelf een testbericht.

## 3. Google Search Console

Hiermee meld je de site aan bij Google en zie je waarop mensen je vinden.

1. Ga naar search.google.com/search-console en log in met je Google-account.
2. Kies **Property toevoegen > Domein** en vul `generationalads.nl` in.
3. Google geeft je een TXT-record. Zet dat bij je domeinregistrar in de DNS en klik op **Verifiëren**.
4. Ga naar **Sitemaps**, vul `sitemap.xml` in en klik op **Indienen**.
5. Ga naar **URL-inspectie**, plak `https://generationalads.nl/` en klik op **Indexering aanvragen**.

Na een paar dagen tot een week staat de site in Google. In Search Console zie je daarna op welke zoekwoorden je gevonden wordt.

## 4. Google Bedrijfsprofiel

Dit is het blok met je bedrijf rechts in Google en in Google Maps. Voor lokale klanten is dit vaak belangrijker dan de website zelf.

1. Ga naar business.google.com en maak een profiel aan voor Generational Ads.
2. Kies als hoofdcategorie **Webdesigner**. Voeg eventueel **Marketingbureau** en **Grafisch ontwerper** toe.
3. Kies dat je klanten op locatie bedient. Dan hoeft je huisadres niet zichtbaar te zijn.
4. Vul als website `https://generationalads.nl/` in.
5. Voeg je logo, een paar screenshots van websites en je diensten toe.
6. Vraag je klanten om een review. Reviews tellen zwaar mee voor je plek in Google.

## 5. Controleren

- **search.google.com/test/rich-results**: plak je adres en check of Google de bedrijfsgegevens leest.
- **pagespeed.web.dev**: check of de site snel genoeg laadt, vooral op mobiel.
- Stuur je link naar jezelf in WhatsApp en kijk of het logo verschijnt.

## Als je later iets aanpast

- Pas je de tekst flink aan, zet dan in `sitemap.xml` bij `lastmod` de datum van vandaag.
- De omschrijving voor Google staat bovenaan `index.html` bij `meta name="description"`. Houd die onder de 155 tekens.
- Na grote wijzigingen kun je in Search Console opnieuw **Indexering aanvragen**.
