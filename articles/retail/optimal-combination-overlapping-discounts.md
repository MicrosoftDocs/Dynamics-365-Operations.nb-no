---
title: Bestemme den optimale kombinasjonen av overlappende rabatter
description: "Når rabatter overlapper hverandre, må du bestemme kombinasjonen av overlappende rabatter som vil produsere totalen for transaksjonen laveste eller høyeste sluttrabatten. Når rabattbeløpet varierer i henhold til prisen for produkter som er kjøpt, for eksempel som i vanlige «Kjøp 1, får 1 X prosent» (BOGO) retail rabatt, blir denne prosessen et problem for kombinatorisk optimalisering."
author: kfend
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations, Retail
ms.custom: 89643
ms.assetid: 09843c9a-3e19-4e4a-a8ce-80650f2095f9
ms.search.region: global
ms.search.industry: Retail
ms.author: kfend
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: af31f0c4cb5304a213f883e3d076731f7cee468e
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---

# <a name="determine-the-optimal-combination-of-overlapping-discounts"></a>Bestemme den optimale kombinasjonen av overlappende rabatter

[!include[banner](includes/banner.md)]


Når rabatter overlapper hverandre, må du bestemme kombinasjonen av overlappende rabatter som vil produsere totalen for transaksjonen laveste eller høyeste sluttrabatten. Når rabattbeløpet varierer i henhold til prisen for produkter som er kjøpt, for eksempel som i vanlige "Kjøp 1, får 1 X prosent" (BOGO) retail rabatt, denne prosessen blir et problem for optimalisering av combinatorial.

Denne artikkelen gjelder for Microsoft Dynamics AX 2012 R3 med KB 3105973 (utgitt 2. november 2015) eller nyere, og for Microsoft Dynamics 365 for Retail. For å finne hvilken kombinasjonen av overlappende rabatter som skal brukes, i tide, har vi innført en metode for å bruk av overlappende rabatter. Vi kaller denne nye metoden **rangering av marginalverdi**. Rangering av marginalverdi brukes når tiden som er nødvendig for å evaluere de mulige kombinasjonene av overlappende rabatter, overskrider en terskel som kan konfigureres på siden **Detaljhandelsparametere**. Under rangering av marginalverdi beregnes en verdi for hver overlappende rabatt ved hjelp av rabattverdien for delte produkter. Overlappende rabatter brukes deretter fra den høyeste verdien i forhold til laveste relative verdi. Opplysninger om den nye metoden, kan du se delen "Marginalverdi" senere i denne artikkelen. Marginalverdien rangeringen er ikke brukt når rabattbeløp for et produkt ikke er berørt av et annet produkt i transaksjonen. Denne metoden brukes for eksempel ikke til to enkle rabatter, eller en enkel rabatt og et enkelt produkt kvantumsrabatt.

## <a name="discount-examples"></a>Rabatteksempler
Du kan opprette et ubegrenset antall detaljhandelsrabatter på et felles sett med produkter i Dynamics AX. Men fordi det er ingen grense, ytelsesproblemer kan oppstå når du prøver å beregne rabatter som skal brukes på de ulike produktene. Følgende eksempler illustrerer problemet mer detaljert. I eksempel 1 starter vi med to produkter og to overlappende rabatter. Deretter, i eksempel 2, viser vi hvordan problemet utvikler seg som flere produkter blir lagt til.

### <a name="example-1-two-products-and-two-discounts"></a>Eksempel 1: To produkter og to rabatter

I dette eksemplet er to produkter nødvendig for å kvalifisere for hver rabatt og rabattene kan ikke kombineres. Rabatter i dette eksemplet er **Beste pris**-rabatter. Begge produkter som er kvalifisert for begge rabatter. Her er de to rabattene.
![Overlappende rabattkombi 01](./media/overlapping-discount-combo-01.jpg)

For to produkter avhenger den beste av disse to rabattene av prisene på de to produktene. Når prisen på begge produktene er lik eller nesten lik, er rabatt 1 bedre. Når prisen på et produkt er betydelig mindre enn prisen på det andre produktet, er rabatt 2 bedre. Her er den matematiske regelen for evaluering av disse to rabattene mot hverandre: ![Overlappende rabattkombi 02](./media/overlapping-discount-combo-02.jpg)

**Merk:** Når prisen på produkt 1 er identisk med to tredjedeler av prisen på produktet 2, er de to rabattene like. I dette eksemplet varierer effektive rabattprosenten for rabatt 1 fra noen få prosent (når prisene på de to produktene er langt fra hverandre) til maksimalt 25 prosent (når de to produktene har samme pris). Effektiv rabattprosent for rabatt 2 er fast. Den er alltid 20 prosent. Fordi den effektive rabattprosenten for rabatt 1 har et område som kan være mer enn eller mindre enn rabatt 2, avhenger av beste rabatt av prisene på de to produktene som må være rabattert. I dette eksemplet er beregningen fullført raskt, fordi bare to rabatter trer i kraft på bare to produkter. Det er bare to mulige kombinasjoner: en bruk av rabatt 1 eller en bruk av rabatt 2. Det finnes ingen unntak å beregne. Verdien av hver rabatt beregnes ved å bruke begge produktene, og den beste rabatten brukes.

### <a name="example-2-four-products-and-two-discounts"></a>Eksempel 2: Fire produkter og to rabatter

Deretter bruker vi fire produkter og de samme to rabattene. Alle fire produkter som er kvalifisert for begge rabatter. Det er tolv mulige kombinasjoner. I siste to rabattene gjelder transaksjonen i en av tre kombinasjoner: to ganger bruk av rabatt 1, to ganger bruk av rabatt 2 eller én gangs bruk av rabatt 1 og én gangs bruk av rabatt 2. For å illustrere de mulige kombinasjonene, skal vi se på to forskjellige sett med fire produktene som har ulike priser:

-   Alle fire produkter har samme pris, $15,00. I dette tilfellet er den beste rabattkombinasjonen to ganger bruk av rabatt 1. To produkter vil ha full pris, og to vil ha 50 prosent avslag. Det rabatterte totalbeløpet for transaksjonen er $45 (15 + 15 + 7,50 + 7,50), som er $15 (25 prosent) av den urabatterte totalsummen på $60. Rabatt 2 er bare $12 (20 prosent).
-   De to produktene er $20 hver, ett produkt er $15 og ett produkt er $5. I dette tilfellet er den beste kombinasjonen én gangs bruk av rabatt 2 og én gangs bruk av rabatt 1. Tabellene nedenfor illustrerer rabattene.

Hvis du vil lese tabellene, kan du bruke et produkt fra en rad og ett produkt fra en kolonne. For eksempel, i tabellen for rabatt 1 får du når du kombinerer de to $20-produktene $10 avslag. I tabellen for diskonto 2 når du kombinerer produktet for $15 og produktet for $5 får du $4 avslag.
![Overlappende rabattkombi 03](./media/overlapping-discount-combo-03.jpg)

Først finner vi den største rabatten som er tilgjengelig fra hvilke som helst to produkter ved hjelp av en av rabattene. De to tabellene viser rabattbeløpet for alle kombinasjoner av de to produktene. De skyggelagte delene i tabellene representerer enten tilfeller der et produkt er forbundet med seg selv, som vi ikke kan gjøre, eller en omvendt sammenkobling av to produkter som gir det samme rabattbeløpet og kan ignoreres. Ved å se på tabellene kan du se at rabatt 1 for de to varene til $20 er den største rabatten som er tilgjengelig for en av rabattene for alle fire produkter. (Denne rabatten er uthevet i grønt i den første tabellen.) Dermed er det bare $15-produktet og $5-produktet igjen. Ved å se på de to tabellene på nytt kan du se at for disse to produktene gir rabatt 1 en rabatt på $2,50, mens rabatt 2 gir en rabatt på $4. Derfor velger vi rabatt 2. Totalrabatten er $14. Hvis du vil gjøre det enklere å visualisere denne diskusjonen, er her to andre tabeller som viser den effektive rabattprosenten for alle mulige kombinasjoner av to produkter, både for rabatt 1 og rabatt 2. Bare halvparten av listen over kombinasjoner er inkludert, fordi rekkefølge de to produktene legges inn i rabatten, er uten betydning for disse to rabattene. Den høyeste effektive rabatten (25 prosent) er uthevet i grønt, og den laveste effektive rabatten (10 prosent) er uthevet i rødt. 

![Overlappende rabattkombi 04](./media/overlapping-discount-combo-04.jpg)

**Merk:** Når prisene varierer, og to eller flere rabatter konkurrerer, er den eneste måten å garantere de beste kombinasjonene av rabatter å evaluere begge rabatter og sammenligne dem.

## <a name="total-possible-combinations"></a>Totalt antall mulige kombinasjoner
Denne delen fortsetter eksemplet fra den forrige delen. Vi vil legge til flere produkter og en annen rabatt, og se hvor mange kombinasjoner som må beregnes og sammenlignes. Tabellen nedenfor viser hvor mange mulige kombinasjoner av rabatter etter hvert som produktantallet øker. Den tabell viser hva som skjer både når det er to overlappende rabatter, som i forrige eksempel, og tre overlappende rabatter. Antall mulige kombinasjoner av rabatter som må evalueres, overskrider snart det som til og med en rask datamaskin kan beregne og sammenligne raskt nok til å være akseptabel for handelstransaksjoner.

![Overlappende rabattkombi 05](./media/overlapping-discount-combo-05.jpg)

Når enda større antall eller flere overlappende rabatter trer i kraft, blir totalt antall mulige kombinasjoner av rabatter raskt flere millioner, og tiden som er nødvendig for å vurdere og velge den beste mulige kombinasjonen, blir raskt merkbar. Noen optimaliseringer har blitt gjort i detaljprismotoren for å redusere det totale antallet kombinasjoner som må evalueres. Fordi antallet overlappende rabatter og antallene i en transaksjon ikke er begrenset, må imidlertid alltid et stort antall kombinasjoner evalueres når det er snakk om overlappende rabatter. Det er dette problemet som rangeringsmetoden med marginalverdi løser.

## <a name="marginal-value-method"></a>Marginalverdimetode
For å løse problemet med et eksponentielt økende antall kombinasjoner som må evalueres, finnes det en optimalisering som beregner verdien per delte produkt for hver rabatt i settet med produkter som to eller flere rabatter kan brukes på. Vi henviser til denne verdien som **marginalverdien** for rabatten for de delte produktene. Marginalverdien er gjennomsnitt økning per produkt av det totale rabattbeløpet når de delte produktene er inkludert i hver rabatt. Marginalverdien beregnes ved å ta det totale rabattbeløpet (DTotal), trekke fra rabattbeløpet uten delte produkter (DMinus\\ delt), og dele denne differansen med antall delte produkter (ProductsShared). 
![Overlappende rabattkombi 06](./media/overlapping-discount-combo-06.jpg)

Etter marginalverdien av hver rabatt i et delt sett med produkter er beregnet, brukes rabattene på de delte produktene i rekkefølge, utførlig, fra høyeste marginalverdi til laveste marginalverdi. Alle gjenværende rabattmuligheter blir ikke sammenlignet hver gang etter en enkelt forekomst av en rabatt er brukt for denne metoden. I stedet er overlappende rabatter sammenlignet én gang og brukes deretter i rekkefølge. Ingen flere sammenligninger utføres. Du kan konfigurere grenseverdien for å bytte til metoden med marginalverdi i kategorien **Rabatt** på siden **Detaljhandelsparametere**. Akseptabel tid til å beregne den totale rabatten varierer på tvers av bransjer for detaljhandel. Nå er imidlertid denne tiden vanligvis mellom noen titalls millisekunder til ett sekund.




