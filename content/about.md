---
Title: About
Description: Info about the page
icon: fas fa-info-circle
---

# Om webbplatsen

På webbplatsen används flera tekniker.

PHP änvänds som grundläggande programmeringsspråk.


## Composer
Genom Composer, som är ett pakethanteringssystem för PHP används följande paket:
* Pico CMS används som CMS-ramverk
* Twig är ett templatemallsystem som används av Pico för att göra sidmallar
* Cimage används för att skala bilder

## NPM
NPM används för att ladda ner ytterligare paket. NPM är ett pakethanteringssystem för node/JS.

Paket som används är:
* stylelint för att kontrollera koden
* normalize.css för att "återställa" CSS-koden och göra den likadan som utgångspunkt för samtliga olika webbläsare
* SASS används för hantering av CSS

## CSS
CSS används genom SASS för design/style och närliggande funktioner.

## SASS
SASS är en förkompilator för CSS-kod

Sidan använder bl.a. följande SASS-tekniker:
* import (testade även med use, men när fontawsome var inblandat blev det rörigt, så jag gick tillbaka till import)
* jag har delat upp filerna i några funktionella grupper, utöver de som var beskrivna i uppgiftstexten
* mixin och include
* variabler (som primärt sparas i variables.scss)
* nästlade nivåer (där jag dock backade från ytterligare nivåer när lintern klagade)

# Övrigt
Fontawsome används för ikonerna, förutom bok-ikonen som är en unicode-icon.

Google Fonts används för fonterna, Nunito Sans resp PT Serif

# Allmänt om stilen
Jag försökte få till en tilltalande stil som fungerar både på datorer och mobiler. Jag la brytpunkten mellan desktop och mobil på samma bredd för både visad meny vs hamburgermeny och för när fontstorleken skalas ner.
