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
Het logo en de favicon worden automatisch mee geladen.om het logo en de
favicon automatisch te gebruiken:

Wil je toch een aparte favicon of logo gebruiken, dan kan je die
rechtstreeks configureren:

```yaml
website:
  favicon: "_extensions/onroerenderfgoed/onroerend-erfgoed/favicon.ico"
```

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

## Hergebruik

Het gebruik van de huisstijl, het logo en de fonts zijn enkel toegelaten
in het kader van projecten van Onroerend Erfgoed. Deze elementen zijn expliciet
uitgesloten van de licentievoorwaarden onder de EUPL-1.2.
