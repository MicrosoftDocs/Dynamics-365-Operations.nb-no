---
title: BOM-beregninger
description: Beregningene av kostnadsakkumulering og salgspris kalles stykklisteberegninger (BOM), og du innleder dem fra Beregninger-siden. Dette emnet gir informasjon om BOM-beregninger.
author: YuyuScheller
manager: AnnBe
ms.date: 04/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMCalcDialog, BOMCalcTable, CostingVersion, InventItemPrice, SalesQuotationTable, SalesTable, SMAServiceOrderTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 273763
ms.assetid: c6fa3348-eafa-4847-9132-e65c5f55cbf4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.dyn365.ops.intro: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: b1bcf11a8f6fc4921e8659fe1d00c093e3ad5b74
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---

# <a name="bom-calculations"></a>BOM-beregninger

[!include[banner](../includes/banner.md)]


Beregningene av kostnadsakkumulering og salgspris kalles stykklisteberegninger (BOM), og du innleder dem fra Beregninger-siden. Dette emnet gir informasjon om BOM-beregninger.

Beregningene av kostnadsakkumulering og salgspris kalles stykklisteberegninger (BOM), og du innleder dem fra **Beregninger**-siden. Du bruker **Beregninger**-siden til å utføre følgende oppgaver:

-   Beregne kostnaden for en produsert vare, og generere en tilknyttet post for varekost innenfor en kostversjon.
-   Beregne salgsprisen for en produsert vare, og generere en tilknyttet post for varesalgspris innenfor en kostversjon.

Hvordan du bruker **Beregninger**-siden, varierer litt avhengig av hvordan du innleder stykklisteberegningene. Bruken av **Beregninger**-siden er også avhengig av om stykklisteberegningene omfatter en kostversjon for standardkostnader eller planlagte kostnader, og av flere policyer som defineres innenfor kostversjonen som brukes i stykklisteberegningene. **Obs!** Det brukes en variasjon av **Beregninger**- når det gjelder varelinjer for salgsordrer, salgstilbud eller tjenesteordrer. Disse beregningene kalles ordrespesifikke stykklisteberegninger. En ordrespesifikk stykklisteberegning genererer ikke en post for varekost innenfor en etterkalkuleringsversjon. I stedet genererer den en beregningspost som vises på siden **Detaljer for stykklisteberegning**. Beregningsposten inneholder en beregnet kostnad og en beregnet salgspris. **Beregninger**-siden kan åpnes for en enkelt produsert vare eller for en kostnadsversjon:

-   For å beregne kostnader for en enkelt produsert vare starter du stykklisteberegninger fra **Varepris**-siden. **Beregninger**-siden arver varens ID. Etterkalkuleringsversjon, stykklisteversjon, ruteversjon, beregningsantall, beregningsdato og område må angis.
    -   Som standard settes stykklisteversjonen og ruteversjonen til de aktive versjonene for varen, området, datoen og beregningsantallet. Du kan imidlertid overstyre standardverdiene med godkjente versjoner.
    -   Beregningsantallet er som standard satt til varens standard ordreantall. Du kan imidlertid overstyre standardverdien.
    -   Beregningsdato og område kan være obligatoriske i kostversjonen, eller brukerne kan angi egne verdier hvis obligatorisk dato eller område ikke finnes i kostversjonen. En beregningsdato i fremtiden bestemmer hvordan ventende kostnadsposter brukes. Stykklisteberegningene vil bruke en ventende kostnadspost med den nærmeste fra-datoen som ligger på eller før beregningsdatoen.
-   Hvis du vil beregne kostnader for alle produserte varer eller utvalgte varer, eller oppdatere varer avhengig av hvor de brukes, starter du stykklisteberegninger fra siden **Oppsett av etterkalkuleringsversjon** eller siden **Vedlikehold av etterkalkuleringsversjon**. **Beregninger**-siden arver etterkalkuleringsversjonen.
    -   Beregningene forutsetter at den aktive stykklisteversjonen og ruteversjonen brukes for en produsert vare (sammen med tilknyttet område, dato og antall), unntatt hvis en delstykkliste eller en underrute er angitt for den produserte komponenten.
    -   For beregningene antas det at det standard ordreantall brukes for produserte varer. Standard ordreantall danner grunnlaget for beregning av komponentantall, for å fastsette de relevante stykklisteversjonene og ruteversjonene (når du bruker antallsavhengige stykklister og ruter), og for å amortisere konstante kostnader. Denne forutsetningen gjelder imidlertid ikke når en produsert komponent har stykklistelinjetypen **Produksjon** eller **Leverandør**, eller når du bruker en Produksjon etter ordre-nedbrytingsmodus for stykklisteberegningene, fordi antall vil vise til det angitte beregningsantallet.
    -   Beregningsdato og område kan være obligatoriske i kostversjonen, eller brukerne kan angi egne verdier hvis obligatorisk dato eller område ikke finnes i kostversjonen.

Andre variasjoner i stykklisteberegninger gjenspeiler etterkalkuleringstypen og begrensningene i etterkalkuleringsversjonen:

-   Stykklisteberegninger som bruker standardkostnader, må begrenses i samsvar med kostversjonspolicyer, fordi begrensningen sikrer at standard prinsipper for etterkalkulasjon brukes. Standard prinsipper for etterkalkulasjon krever at begrensninger i bruken av standardkostnader for kjøpte varer iverksettes, at nedbrytingsmodus på ett enkelt nivå brukes, og at tillegg inkluderes i enhetskostnader.
-   Stykklisteberegninger som bruker planlagte kostnader, trenger ikke utføres i samsvar med standard prinsipper for etterkalkulasjon. Disse stykklisteberegningene kan bruke forskjellige nedbrytingsmoduser og alternative kilder til kostdata for kjøpte varer, og iverksetting av begrensninger innenfor kostversjonen er valgfri.

### <a name="bom-calculations-that-use-standard-costs"></a>Stykklisteberegninger som bruker standardkostnader

Policyer innenfor kostversjonen (for standardkostnader) kan gjøre iverksetting av fem policyer for stykklisteberegning obligatorisk. Alternativet **Registreringsbegrensning** i kostversjonen gjør én av disse policyene obligatorisk der tillegg må inkluderes i enhetsprisen. Tillegg for kjøpte varer kan angis manuelt, mens tillegg for produserte varer gjenspeiler den beregnede amortiseringen av konstante kostnader. Alternativet **Registreringsbegrensning** i kostversjonen gjør de fire andre policyene for stykklisteberegning obligatoriske:

-   Kilden til kjøpte varers kostbidrag må baseres på standardkostnadene. Det vil si at stykklisteberegninger må bruke poster for varekostnader innenfor den angitte kostversjonen, eller innenfor tilbakefallsversjonen som inneholder standardkostnadene.
-   Nedbrytingsmodusen må være på et enkelt nivå for å sikre nøyaktig og konsistent beregning av standardkostnader.
-   Fortjenesteinnstillingen må være obligatorisk for å oppnå konsistente resultater i beregningen av varens salgspris. Kostversjonen må tillate innhold i salgspriser for å bruke fortjenesteinnstillingen og for å generere varens salgsprisposter.
-   Tilbakefallsprinsippet må være obligatorisk og kan angis til **Ingen**, **Aktiv** (for aktive kostnadsposter) eller **Etterkalkuleringsversjon** (for en angitt kostversjon).

### <a name="bom-calculations-that-use-planned-costs"></a>Stykklisteberegninger som bruker planlagte kostnader

Policyer innenfor kostversjonen (for planlagte kostnader) kan eventuelt gjøre iverksetting av fem policyer for stykklisteberegning obligatorisk. Policyene kan også bare angi standardverdier. Alternativet **Registreringsbegrensning** i kostversjonen avgjør om policyen for stykklisteberegning for tillegg skal være obligatorisk eller fungere som en standardverdi. Inkludering av tillegg i enhetsprisen er valgfri. Alternativet **Registreringsbegrensning** i kostversjonen avgjør om de fire andre policyene for stykklisteberegning skal være obligatoriske eller fungere som standardverdier.

-   Kilden til kostbidragene for en innkjøpt vare kan være varekostnadspostene innen en kostnadsversjon. Kilden kan også defineres av stykklisteberegningsgruppen som er tilordnet til varen. For eksempel kan stykklisteberegningsgruppen definere forretningsavtaler om innkjøpspris som kilden til kostbidragsdata.
-   Nedbrytingsmodusen kan være på et enkelt nivå, på flere nivåer, på produksjon etter ordre eller baseres på stykklistelinjeelement. Nedbrytingsmodusen for stykklistelinjetype repliserer kostnadsberegningslogikken for produksjonsordreestimater.
-   Fortjenesteinnstillingen kan være obligatorisk eller en standardverdi. Kostversjonen må tillate innhold i salgspriser for å bruke fortjenesteinnstillingen og for å generere varens salgsprisposter.
-   Tilbakefallsprinsippet kan være obligatorisk eller en standardverdi. Tilbakefallsprinsippet kan angis til **Ingen**, **Aktiv** (for aktive kostnadsposter) eller **Etterkalkuleringsversjon** (for en angitt kostversjon).

Stykklisteberegninger genererer advarselsmeldinger og andre typer meldinger. Flere policyer for stykklisteberegning fastsetter typene meldinger. Varselsbetingelsene er definert i stykklisteberegningsgruppen som er tilordnet varene. Du kan imidlertid overkjøre disse varselsvilkårene når du starter en stykklisteberegning. Når tilbakefallsprinsippet brukes, er det ofte nyttig å vise tilbakefallsinformasjon som en informasjonsmelding. Når du prøver å oppdatere kostnader for varer med manglende kostnadsposter, er det også nyttig å kunne identifisere varer som ikke ble oppdatert, ved hjelp av informasjonsmeldingen.

## <a name="bom-calculations-that-use-the-fallback-principle"></a>Stykklisteberegninger som bruker tilbakefallprinsippet
Følgende situatjoner illusterer to bruksmåter for tilbakefallsprinsippet:

-   **Fremgangsmåte med to versjoner for oppdatering av standard kostpris** − En etterkalkuleringsversjon kan inneholde trinnvise endringer i standard kostpris, for eksempel uavsluttede kostprisposter som representerer nye varer eller endringer i kostpris. I denne situasjonen kan tilbakefallsprinsippet identifisere bruk av aktive standard kostpriser som inngår i andre etterkalkuleringsversjoner.
-   **Simulering av effekten av kostnader endres ved hjelp av planlagte kostnader** - En etterkalkuleringsversjon for planlagte kostnader kan inneholde trinnvise endringer til simuleringsformål. Denne etterkalkuleringsversjon vil inneholde uavsluttede kostprisposter som representerer de simulerte kostprisendringene for varer, kostnadskategorier og beregningsformler for indirekte kostnader. I denne situasjonen kan tilbakefallsprinsippet identifisere bruk av aktive standard kostpriser som inngår i andre etterkalkuleringsversjoner.

## <a name="bom-calculation-of-a-suggested-sales-price"></a>Stykklisteberegning av en foreslått salgspris
Når du bruker en påslagstilnærming som tar høyde for fastsatt/beregnet fortjeneste, gjenspeiler varens beregnede salgspris settet med fortjenestesettprosenter som er angitt for stykklisteberegningen, og kostnadene som er tilknyttet komponentvarene, rutingsoperasjoner og administrasjonskostnader som kan brukes. Tilnærmingen gjenspeiler fortjenestesettprosenter som er tilordnet kostnadsgruppene, og kostnadsgruppene som er tilordnet varer, kostnadskategorier for rutingsoperasjoner, og de indirekte kostnadsberegningsformlene for administrasjonskostnader. Settene med fortjenestesettprosenter kalles **Standard**, **Fortjeneste 1**, **Fortjeneste 2** og **Fortjeneste 3**. I settet fortjeneste 1 kan for eksempel en fortjenestesettprosent på 50 prosent defineres for en kostgruppe som er tilordnet til innkjøpt materiale, og en fortjenestesettprosent på 80 prosent kan defineres for en kostgruppe som er tilordnet kostnadskategorier for rutingsoperasjoner. Konteksten til stykklisteberegningen bestemmer hvordan resultatene for en beregnet salgspris håndteres:

-   **Stykklisteberegning for en vare og angitt kostnadsversjon** − Stykklisteberegningen genererer en ventende salgsprispost i kostnadsversjonen. Denne salgsprisposten angir startpunktet for visning av beregningsdetaljene (for eksempel på siden **Beregn varekostnad**). Salgsprisposten fungerer først og fremst som referanseinformasjon, og den brukes ikke som grunnlag for en salgspris på salgsordrer.
-   **Ordrespesifikk stykklisteberegning** − Det brukes en variasjon av **Stykklisteberegning**-siden når det gjelder varelinjer for salgsordrer, salgstilbud eller serviceordrer. En ordrespesifikk stykklisteberegning genererer ikke en kostnadspost innen en kostnadsversjon. I stedet genererer den en beregningspost som vises på siden **Resultater for stykklisteberegning**. Denne beregningsposten angir startpunktet for visning av beregningsdetaljene (for eksempel på siden **Beregn varekostnad**). Informasjon om en valgt beregningspost kan overføres til den opprinnelige linjevaren. Den beregnede salgsprisen kan for eksempel overføres til en salgsordrelinjevare.

## <a name="orderspecific-bom-calculations"></a>Ordrespesifikke stykklisteberegninger
En ordrespesifikk stykklisteberegning er en variant av en stykklisteberegning for en produsert vare. Den ordrespesifikke stykklisteberegningen utføres i sammenheng med en salgsordre, et salgstilbud eller en serviceordrelinjevare. En ordrespesifikk stykklisteberegning genererer en beregningspost som vises på siden **Resultater for stykklisteberegning**. Beregningsposten inneholder en beregnet vekt, en beregnet kostnad som bygger på aktive kostnadsposter, og en beregnet salgspris. Beregningsposten som hver ordrespesifikke stykklisteberegning for en vare genererer på siden **Resultater for stykklisteberegning**, identifiseres entydig av et beregningsnummer. Resultatene fra en beregningspost kan eventuelt overføres til det opprinnelige linjeelementet. Det er to forskjeller på en ordrespesifikk stykklisteberegning og en stykklisteberegning for en produsert vare:

-   En ordrespesifikk stykklisteberegning genererer ikke en post for varekost innenfor en etterkalkuleringsversjon. Dette betyr at policyene for stykklisteberegning ikke gjelder når en post for varekost opprettes eller når en kostnadspost overskrives.
-   En ordrespesifikk stykklisteberegning vil alltid bruke de aktive kostnadspostene for komponenter, kostnadskategoriene og beregningsformlene for indirekte kostnader.






