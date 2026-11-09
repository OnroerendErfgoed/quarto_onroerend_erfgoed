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

### Huisstijl toevoegen aan een projecten

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

### Globale header

Er is een apart formaat (`onroerend-erfgoed-html+header` voor
het geval je ook de Vlaamse header en footer
moet toevoegen. Dit formaat voorziet extra witruimte, zodat je in
je profielen de header en footer kan insluiten.

```yaml
project:
  type: website
format: onroerend-erfgoed-html+header
```

Het includen van de header kan dan in een profiel
per omgeving:

`_quarto_local.yml`

```yaml
format:
  html:
    include-in-header:
      - text: |
         <script src="https://tni.widgets.burgerprofiel.dev-vlaanderen.be/api/v1/node_modules/@govflanders/vl-widget-polyfill/dist/index.js"> </script>
         <script src="https://tni.widgets.burgerprofiel.dev-vlaanderen.be/api/v1/node_modules/@govflanders/vl-widget-client/dist/index.js"> </script>
    include-before-body:
      - text: |
          <div id="global-header"><script src="https://tni.widgets.burgerprofiel.dev-vlaanderen.be/api/v1/widget/{{UUID}}/embed"> </script>
          </div>
    include-after-body:
      - text: |
          <div id="global-footer-vlaanderen"><script src=https://tni.widgets.burgerprofiel.dev-vlaanderen.be/api/v1/widget/{{UUID}}/embed></script></div>

  dashboard:
    include-in-header:
      - text: |
         <script src="https://tni.widgets.burgerprofiel.dev-vlaanderen.be/api/v1/node_modules/@govflanders/vl-widget-polyfill/dist/index.js"> </script>
         <script src="https://tni.widgets.burgerprofiel.dev-vlaanderen.be/api/v1/node_modules/@govflanders/vl-widget-client/dist/index.js"> </script>
    include-before-body:
      - text: |
          <div id="global-header"><script src="https://tni.widgets.burgerprofiel.dev-vlaanderen.be/api/v1/widget/{{UUID}}/embed"> </script>
          </div>
    include-after-body:
      - text: |
          <div id="global-footer-vlaanderen"><script src=https://tni.widgets.burgerprofiel.dev-vlaanderen.be/api/v1/widget/{{UUID}}/embed></script></div>

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
