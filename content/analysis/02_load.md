---
Title: load
Description: Laddningstid
Template: analys
---

Analys av laddningstider på webbplatser
=======================

Uppgiften går ut på att testa och mäta ett antal webbplatser utifrån hur snabbt de laddas och om de innehåller några saker som kan förbättras med tanke på laddningstid och användbarhet.

Urval
-----------------------

De undersökta webb&shy;platserna är precis som för färgvalet "huvud"-universiteten för de fastlands&shy;nordiska huvud&shy;städerna:
* [Köpenhamns universitet, KU](https://www.ku.dk/)
* [Stockholms universitet, SU](https://www.su.se/)
* [Universitetet i Oslo, UiO](https://www.uio.no/)
* [Helsingfors universitet, HU](https://www.helsinki.fi/sv)

Dessa är stora företrädare för högre utbildning i Norden, och får därmed antas vara ett relevant urval av webbplatser för stora universitet i Nordisk kontext.

Metod
-----------------------

De valda sidorna analyserades med [Google PageSpeed Insights](https://pagespeed.web.dev/) samt med webbläsarens devtools-verktyg, fliken Nätverk.

I Google PageSpeed Insights noterades, uppdelat på mobil och desktop dels prestandavärdet, och dels godkänt eller underkänt för "Core Web Vitals". 

I webbläsaren noterades dels antal objekt som laddades, storleken på dem (MB) samt laddninstioden (sekunder) för tre olika försök och medeltiden för dem beräknades.

Resultat
-----------------------

<div class="kalkyl">
    <iframe src="https://docs.google.com/spreadsheets/d/e/2PACX-1vStoEdWVs30hsePyb23Cv3TelysfyV9F2LxUVboQVr-GoKK13ct9iBUsNCvmhQi2NLxeZD6ixywrEl-/pubhtml?gid=0&amp;single=true&amp;widget=true&amp;headers=false"></iframe>
</div>
*I Google-kolumnerna är det första värdet (siffervärde 0-100) från prestanda-testet, och G/U från [Core Web Vitals](https://web.dev/articles/vitals).*

Analys
-----------------------

Köpenhamns unviersitet har generellt låga tider, om än inte fullt så låga som Oslo. Antal laddade objekt ligger högre än både Oslo och Helsingfors, men betydligt lägre än Stockholm. Alla objekt laddas direkt. De verkar ha arbetat mycket med att få ner laddtiderna, trots en mer traditionell teknik. Bildfiler laddas väldigt snabbt.

Stockholms unversitet laddar både väldigt många objekt och väldigt mycket data. Tiderna är också de sämsta i min tidsstudie, men det kan noteras att de flesta objekt var klara snabbare på forsknings- och nyhetssidan, men det var var några få objekt som verkar ligga på externa webbplatser tog de extra ca 3-4 sekunderna. Utan dessa hade sidorna laddat klart snabbare. Men det finns även annat att arbeta på. T.ex. bildfilerna är både många och tar tid att ladda. Här hade de kunnat optimera mer (på liknande sätt som Köpenhamn). Stockholm borde även arbeta med mobilanpassning, som fick väldigt låga betyg hos Google.

Uppenbart är att Universitetet i Oslo arbetat mycket med att få ner laddningstiderna. De är helt enastående jämfört med de andra. Någon sida har lite sämre värden på mobil, men överlag är det ändå helt utan anmärkning, och sidorna känns jättesnabba. Värt att notera för Universitetet i Oslo är att de sidorna inte laddar allt material från början. När man skrollar ner på sidan hämtas mer material, t.ex. bilderna till nyheter som är längre ner. Detta gör att man kan få fördröjningar *efter* att sidan laddats. Dock verkar de ha tänkt även på detta, och "tilläggsladdningstiderna" är relativt korta, så det upplevs ändå inte som så fördröjande, även om man märker det. De flesta övriga unviversiteten laddade allt (eller i princip allt) material redan från början, vilket då tar lite längre tid (förutom hos KU), men då sker inga fördröjningar senare när man tittar/läser längre ner på sidan.

Helsingfors universitet faller framför allt på First Contentful Paint (FCP)-testet, dvs hur lång tid det tar före något "vettigt" visas överhuvudtaget. I övrigt är de ganska snabba, och bilderna i sig laddas snabbt. Det verkar vara deras JS-skript som ställer till det, så detta borde de se över. Även Helsingfors använder sig delvis av "ladda när man skrollar", men mindre än Oslo. De bilder som laddas i efterhand laddas snabbt (som deras andra bilder).

Min rangordning blir: Oslo (1), Köpenhamn (2), Stockholm (3), Helsingfors (4). De två första är i en klass för sig, men Oslo får vinsten för att deras förfarande känns både mer snabbare och modernt, och för sin lyckade mobilanpassning. Köpenhamn har lyckats väldigt bra med optimering av snabbhet på en mer traditionell sida som laddar allt från början. Både Stockholm och Helsingfors är långsammare och de märks. Helsingfors förlorar pga deras vädligt långa fördröjning före något visas överhuvudtaget.

Mitt eget upplevad gränsvärde går nog vid 4-5 sekunder, före en webbplats upplevs som långsam. Men samtidigt gör sättet som Helsingfors använder att "hålla inne" sidan i nästan den tiden före den släpps som mer frustrerande än Stockholm, även om tiden i sig är kortare för Helsingfors än Stockholm.

Referenser
-----------------------

De analyserade sidorna.
[Google PageSpeed Insights](https://pagespeed.web.dev/)
[Core Web Vitals](https://web.dev/articles/vitals)

Övrigt
-----------------------

Analysen/rapporten skrevs av Karim Andersson (kaae22).