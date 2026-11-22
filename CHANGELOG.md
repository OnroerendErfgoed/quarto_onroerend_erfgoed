# v1.2.0

 - theme.scss bevat geen hardgecodeerde kleuren meer; `_brand.yml` is de
   enige bron van waarheid voor de merkkleuren:
   - semantische kleuren en typografie sturen automatisch de
     Bootstrap-basisvariabelen (bodykleuren, linkkleur, kopkleur, lettertype)
   - Quarto-specifieke variabelen ($toc-color, $navbar-bg,
     $callout-color-note, ...) worden via defaults.bootstrap.defaults aan
     de paletkleuren gekoppeld
   - de scss:rules sectie gebruikt de $brand-* Sass variabelen van
     het palet
 - Bootstrap utility-kleuren "blue" en "purple" volgen nu de merkkleuren
   (voorheen de Bootstrap-standaardwaarden)
 - Sectienummers (.header-section-number) krijgen dezelfde kleur als
   hun kop in plaats van de grijze body-kleur

# v1.1.0

 - Vulp `_brand.yml` aan met de merkkleuren (paars, blauw, grijstinten) en
   semantische roltoewijzingen (primary, foreground, background, ...)
 - Registreer Flanders Art Sans rechtstreeks in `_brand.yml`
   (`typography.fonts` met `source: file`) en verwijder het afzonderlijke
   `fonts.css` met de `@font-face` regels

# v0.1.0

New features

 - theming extensie for Flanders Heritage
 - format onroerend-erfgoed-theme
 - branding: kleuren, logo, fonts en favicon

# v.0.2.0

 - autoload brand

# v.0.3.0

 - Verwijder stadaard extra witruimte voor de globale header
 - Voeg extra formaat toe `html+header`, dat wel witruimte voorziet
   voor de Vlaamse globale header 

# v.0.3.2

 - fix extension.yml
