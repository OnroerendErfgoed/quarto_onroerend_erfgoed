# Quarto theme voor Onroerend Erfgoed

Een Quarto extensie met de huistijl van het agentschap Onroerend Erfgoed.

De extensie biedt een custom html format aan en bevat:

- Vlaamse huisstijl voor websites
- Flanders Art Sans Font
- logo

## Installatie

Om de extensie te installeren in een quarto project, kan je
het onderstaande commando uitvoeren.

```bash
quarto add onroerenderfgoed/quarto_onroerend_erfgoed
```

## Gebruik

Voeg de extensie toe in de YAML header van een document:

```yaml
---
title: "Mijn document"
format: onroerend-erfgoed-html
---
```

Voeg de extensie toe in de `_quarto.yml` van je Quarto project.

 `_quarto.yml`:

```yaml
project:
  type: website
  
format: onroerend-erfgoed-html
```

Het format is een extensie van het html format. Opties voor het
html formaat zijn dus ook geldig voor het
onroerend_erfgoed-html formaat (toc, code-fold, navbar, ...):

```yaml
format:
  onroerend-erfgoed-html:
    toc: true
```

## Logo en favicon

De extensie bevat een `_brand.yml` dat het logo als standaard instelt.
Voeg onderstaande regel toe aan de `_quarto.yml` om het logo en de
favicon automatisch te gebruiken:

```yaml
brand: "_extensions/onroerenderfgoed/onroerend-erfgoed/_brand.yml"
```

Quarto gebruikt dan `logo.svg` standaard als favicon en in de navbar,
zonder verdere configuratie.

Wil je toch een aparte favicon of logo gebruiken, dan kan je die
rechtstreeks configureren:

```yaml
website:
  favicon: "_extensions/onroerenderfgoed/onroerend-erfgoed/favicon.ico"
```

De favicon uit de brand is een svg. Voor maximale compatibiliteit met
oudere browsers kan je de meegeleverde `favicon.ico` gebruiken zoals
hierboven.

## Structuur van de extensie

```
_extensions/onroerenderfgoed/onroerend-erfgoed/
├── _extension.yml   # metadata voor het onroerend-erfgoed-html formaat
├── _brand.yml       # standaard logo (favicon en navbar)
├── theme.scss       # bootstrap variable overrides en custom CSS regels
├── fonts.css        # @font-face Flanders Art Sans
├── logo.svg         # Onroerend Erfgoed logo
├── favicon.ico      # Onroerend Erfgoed favicon
└── fonts/           # Flanders Art Sans Regular (woff, ttf, eot, svg)
```
