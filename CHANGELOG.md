# v1.1.0

 - Registreer Flanders Art Sans rechtstreeks in `_brand.yml`
 - theme.scss bevat geen hardgecodeerde kleuren meer. Kleuren komen uit `_brand.yml` is de
   - Quarto-specifieke variabelen ($toc-color, $navbar-bg,
     $callout-color-note, ...) worden defaults.bootstrap.defaults aan
     de paletkleuren gekoppeld
   - gebruik scss:rules sectie gebruikt $brand-* Sass variabelen
 - Bootstrap utility-kleuren "blue" en "purple" volgen merkkleuren
 - Sectienummers (.header-section-number) zelfde kleur als de heading

# v1.0.0

 - first release, cleanup metadata

# v.0.3.2

 - fix extension.yml

# v.0.3.0

 - Verwijder stadaard extra witruimte voor de globale header
 - Voeg extra formaat toe `html+header`, dat wel witruimte voorziet
   voor de Vlaamse globale header 

# v.0.2.0

 - autoload brand

# v0.1.0

New features

 - theming extensie for Flanders Heritage
 - format onroerend-erfgoed-theme
 - branding: kleuren, logo, fonts en favicon
