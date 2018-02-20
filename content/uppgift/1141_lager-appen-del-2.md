---
author: efo
category: javascript
revision:
  "2018-01-17": (A, efo) Första utgåvan i samband med kursen webapp v3.
...
Lager appen del 2
==================================
[FIGURE src=image/webapp/pick-list.png?w=c4 class="right"]

I kursmoment 1 skapade vi grunden för vår lager app. Vi ska i detta kursmoment förbättra strukturen på både vår JavaScript kod och CSS kod. Vi ska bygga en plocklista vy där lagerarbetarna får en bra översikt över vart produkterna från en order finns. När varorna är plockade ska status ändras för ordern och lagersaldo ska minskas.



<!--more-->



Förkunskaper {#forkunskaper}
-----------------------
Du har gjort uppgiften [Lager appen del 1](uppgift/lager-appen-del-1). Du har jobbat dig igenom övningarna [Knappar för mobilen](kunskap/knappar-for-mobilen) och [Struktur i JavaScript](kunskap/struktur-i-var-javascript).


Introduktion {#intro}
-----------------------
Börja med att kopiera din lager app från kmom01, om du inte gjorde det i övningen, så har du nått att utgå ifrån.

<strong>OBS! Gör bara detta om du inte gjorde det i övningen.</strong>

```bash
# stå i me-katalogen
cp kmom01/lager1/* kmom02/lager2/
```

Använd lager [API:t](https://lager.dbwebb.se) dokumentationen och speciellt sektionen om order. Här kan du hämta ut ordern och alla orderrader. När du ska uppdatera lagersaldot använder du dig av `PUT` HTTP-metoden för produkterna.



Krav {#krav}
-----------------------
1. Strukturera dina JavaScript filer med webpack, så bara en fil inkluderas i `index.html`.

1. Strukturera din CSS kod, så du har olika moduler för dina komponenter, gärna med hjälp av en CSS preprocessor (less eller sass).

1. Skapa en vy där lagerarbetarna ser alla ordrar redo för att packas. Från order-vyn kan man ta sig till plocklista vyn.

1. Plocklista vyn visar alla varor i en order och vart dessa finns.

1. När varorna är plockade ska det finnas möjlighet att byta status för ordern med en knapp.

1. När status för ordern ändras måste även lagersaldot för de packade varorna minskas.

1. Gör ett medvetet val om du vill använda flat design eller ej.

1. Navigationen ska tydligt visa vilken vy användaren är i.

1. Validera och publicera din kod enligt följande.

```bash
# Ställ dig i kurskatalogen
dbwebb validate lager2
dbwebb publish lager2
```

Rätta eventuella fel som dyker upp och publicera igen. När det ser grönt ut så är du klar.



Extrauppgift {#extra}
-----------------------
* Använd en checkbox för varje produkt, ska bara gå att klicka på knappen om alla checkboxar är iklickade.



Tips från coachen {#tips}
-----------------------

Validera och publicera ofta. Så slipper du en massa validerings- och publiceringsfel i slutet av övningen.

När du gör *publish* så körs även *validate*. Blir det för mycket fel när du kör *publish* så kan det bli enklare att bara göra *validate* till att börja med.

Lycka till och hojta till i forumet om du behöver hjälp!