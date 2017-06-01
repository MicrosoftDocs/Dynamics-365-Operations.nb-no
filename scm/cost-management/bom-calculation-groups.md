---
title: Beregningsgrupper for stykkliste
description: "Denne artikkelen inneholder informasjon om beregningsgrupper for stykklister og hvordan du definerer dem. Hvis du vil kjøre en stykklisteberegning, må du definere beregningsgrupper og tilordne dem til individuelle elementer, eller angi en standard beregningsgruppe. Beregningsinnstillingene fra beregningsgruppen brukes deretter som standardverdier på siden Stykklisteberegning på tidspunktet for stykklisteberegning."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMCalcGroup, BOMCalcTable, BOMCalcTrans, InventItemPrice
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 94063
ms.assetid: 63e1b7dc-c2c5-41b0-81ed-e3e02d1b39e0
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 3372c22d6ed90e7669f1335fdd3366b8e167ad27
ms.contentlocale: nb-no
ms.lasthandoff: 05/25/2017


---

# <a name="bom-calculations-groups"></a>Beregningsgrupper for stykkliste

[!include[banner](../includes/banner.md)]


Denne artikkelen inneholder informasjon om beregningsgrupper for stykklister og hvordan du definerer dem. Hvis du vil kjøre en stykklisteberegning, må du definere beregningsgrupper og tilordne dem til individuelle elementer, eller angi en standard beregningsgruppe. Beregningsinnstillingene fra beregningsgruppen brukes deretter som standardverdier på siden Stykklisteberegning på tidspunktet for stykklisteberegning. 

En standard beregningsgruppe kreves på siden **Parametere for beholdnings- og lagerstyring**, eller en produktspesifikk beregningsgruppe kreves på siden **Detaljer om frigitt produkt**. Systemet søker først etter beregningsgruppeoppsettet på siden **Detaljer om frigitt produkt**. Hvis det ikke finnes en beregningsgruppe der, søker det på siden **Parametere for beholdnings- og lagerstyring**. Hvis systemet ikke finner en beregningsgruppe, mottar brukeren en feilmelding under beregningen. En beregningsgruppe inneholder policyer for kostprismodellen salgsprismodellen og sjekkliste for advarsler. Beregningsinnstillingene fra beregningsgruppen brukes som standardverdier på siden **Stykklisteberegning** på tidspunktet for stykklisteberegning.

## <a name="purposes-of-bom-calculation-groups"></a>Formålet med stykklisteberegningsgrupper
Du kan tilordne en stykklisteberegningsgruppe til varer av flere grunner:

-   Ved å angi feltet **Kostprismodell**, man du angi kilden til en innkjøpt komponents kostbidragsdata under beregning av den planlagte kostnaden til en produsert vare. Noen produsenter beregner planlagte kostnader ved å bruke forretningsavtaler om innkjøpspris for innkjøpte komponenter eller annet som grunnlag, for eksempel innkjøpsprisposter i en kostnadsversjon.
-   Ved å angi feltet **Salgsprismodell**, kan du angi hvordan varens data brukes til å beregne en foreslått salgspris. Du kan angi varesalgsprisen eller kostgruppen. Noen produsenter ønsker å beregne en foreslått salgspris for produserte varer. Den beregnede salgsprisen kan gjenspeile en rullende pris-metode som er basert på komponentens salgsprispost. Den beregnede salgsprisen kan også gjenspeile en kostnader pluss påslag-tilnærming som baseres på komponentens kostnad og fortjenesteprosenten, som er knyttet til varens kostnadsgruppe.
-   Ved å bruke feltet **Stopp nedbryting**., kan du angi at en produsert vare skal behandles som en innkjøpt vare til opprullet kost-formål under stykklisteberegning. En vanlig situasjon der dette kan være aktuelt, er hvis en vare som vanligvis kjøpes, noen ganger produseres, eller hvis en vare som vanligvis produseres, kjøpes inn i stedet. Varen utpekes først som en produsert vare for å definere stykkliste- og ruteinformasjon, og for å støtte produksjonsordrer for varen. Flagget **Stopp nedbryting** hindre imidlertid at kostnadsberegninger bruker varens stykkliste og rute. I stedet bruker stykklisteberegningen varens angitte kostnader.

## <a name="calculation-groups"></a>Beregningsgrupper
Du definerer beregningsgrupper under **Oppsett for policyer for forhåndsbestemte kostnader** i Kostnadsstyring. Beregningsgrupper som er tilordnet til varer, lar deg angi hvordan kostnader eller salgspris for komponenter, som beskrevet av beregningsgruppen, er kilde for beregningen. På siden **Beregningsgrupper** kan du definere en kostprismodell, en alternativ kostprismodell, en salgsprismodell og advarsler.

### <a name="cost-price-model"></a>Kostprismodell

Det finnes fire alternativer for feltet **Kostprismodell**:

-   **Varekostpris** – Kostprisen fra tabellen **Frigitt produkt** brukes, eller kombinasjonen av varedimensjoner brukes som kostprisen.
-   **Kjøpspris på vare** – Innkjøpspris fra feltet **Kostpris** i kategorien **Kjøpe** på siden **Liste over frigitte produkter**, brukes.
-   **Forretningsavtaler** – Du kan konfigurere forretningsavtaler for bestemte kombinasjoner av varer og leverandører, eller for bestemte områder. Deretter, når du velger alternativet **Forretningsavtaler** her, brukes forretningsavtalen som du opprettet for kjøpsprisen, sammen med varen og området.
-   **Lagerpris** – Gjeldende lagerverdi for varen brukes til å beregne enhetskosten i stykklisteberegningen. En enhetskostpris beregnes bare hvis det posterte antallet og det fysiske antallet er større enn 0 (null).

### <a name="alternative-cost-price"></a>Alternativ kostpris

Feltet **Alternativ kostpris** har de samme alternativene som feltet **Kostprismodell**. Dette feltet brukes imidlertid bare når en pris ikke finnes i den primære kostprismodellen.

### <a name="sales-price-model"></a>Salgsprismodell

Det er to alternativer for beregning av feltet **Salgspriser**:

-   **Kostgruppe** – Når dette alternativet er valgt, beregnes salgsprisen basert på kostpris og fortjenesteinnstillingsprosent fra kostgruppen.
-   **Salgspris på vare** – Når dette alternativet er valgt, brukes salgsprisen i hurtigfanen **Selg** fra tabellen Frigitt produkt.

### <a name="stop-explosion"></a>Stopp nedbryting

Alternativet **Stopp nedbryting** brukes til å angi når en produsert vare skal behandles som en innkjøpsvare. Vanligvis må du la alternativet **Stopp nedbryting** være umerket. Ved å merke av for dette alternativet, angir du at en produsert vare skal behandles som en innkjøpskomponent i stedet for en produsert komponent for stykklisteberegning. Varens kostnader kan fremdeles beregnes med stykklisteberegninger, avhengig av området. Nedbrytingen av planlagte bestillinger og produksjonsordrer stoppes i stykklisten der komponentene er tilknyttet beregningsgruppen der det er merket av for **Stopp nedbryting**. Grovplanlegging genererer de planlagte ordrene på selve stykklisten, ikke på de underliggende varene som utgjør stykklisten. I utgangspunktet, hvis du merker av for dette alternativet, angir du at en kostnad ikke legges til i stykklisteberegningen for varer som har denne beregningsgruppen.

### <a name="warnings"></a>Advarsler

I hurtigfanen **Advarsler** kan du velge alternativer for alle advarsler som brukere skal motta når de utfører stykklisteberegninger. Hvis du velger for eksempel merker av for **Ingen stykkliste**, mottar brukeren en advarsel hvis det ikke finnes noen aktiv stykklisteversjon for én av komponentene eller den overordnede varen som stykklisteberegningen kjøres for. Hvis du merker av for **Ingen rute**, mottar brukeren en advarsel hvis det ikke blir funnet en aktiv ruteversjon. Hvis du vil bruke ressurser på rutene og operasjonene, kan du angi at systemet skal kontrollere om disse ressursene finnes. Deretter, hvis en ressurs ikke finnes på hver linje i den aktive ruten, mottar brukeren en advarsel. Du kan også verifisere og kontrollere forbruk. Forbruket er antallet i en bestemt rute. Vanligvis representerer dette tiden som kreves for å utføre en bestemt operasjon i produksjonsprosessen. Du kan kontrollere om en vare ikke har kostpris. Hvis det ikke er noen aktive kostpris for en vare, blir ingen kost lagt til i stykklisteberegningen. Du kan også kontrollere og bekrefte alderen til kostprisen. Angi for eksempel **60** for å angi at enhetskostprisen må evalueres på nytt etter 60 dager. Hvis denne grensen nås, genererer systemet en advarsel. En kostpris ble for eksempel angitt for en vare i januar i år. Hvis det er nå august, som er mer enn 60 dager etter at kostprisen ble angitt, mottar brukeren en advarsel når stykklisteberegningen kjøres. Du kan angi i prosent i feltet **Minste dekningsgrad**. Denne verdien angir punktet da minste dekningsgrad ikke oppfylles. Hvis dekningsgraden for en bestemt komponent ikke oppfylles, mottar brukeren en advarsel. Dette feltet bidrar derfor til å garantere at du ikke undervurderer kostnadene og ekstra indirekte kostnader som kan være nødvendige for varene.
Standard oppsett i Parametere for beholdnings- og lagerstyring
--------------------------------------------------------------

Siden det kreves beregningsgrupper for å kjøre beregninger, må du definere en standard beregningsgruppe i Parametere for beholdnings- og lagerstyring. Dette oppsettet lar firmaer ha en standard kostgruppe og fortjenesteinnstilling for alle varer. Deretter, hvis en bestemt vare har spesielle beregningskrav, kan brukeren tilordne en annen beregningsgruppe til varen. Vanligvis kan du definere beregningsgrupper på komponentvarene for stykklisten i stedet for stykklistevarer. Når advarsler vises, brukes imidlertid beregningsgrupper. En beregningsgruppe som er tilordnet til varer, overstyrer standardverdien som er definert i parametere for lagerstyring. Du kan definere standardparameteren ved å gå til **Kostnadsstyring** &gt; **Oppsett for regnskapspolicyer for beholdning** &gt; **Parametere** &gt; **Lagerregnskap** &gt; **Beregningsgruppe**. Ved å definere en standard konfigurasjonsgruppe, kan du også konfigurere advarselsbetingelsene som vises for brukere under stykklisteberegningen hvis de valgte komponentene kan føre til beregningsfeil.
Vise advarsler på siden Fullført
------------------------------------------

En stykklisteberegning genererer advarsler. Du kan vise advarslene om en valgt vare. Opprett for eksempel en ny salgsordre for vare D0001 i Salg og markedsføring. Deretter går du til salgsordrelinjen på **Oppdater linje**-menyen, og klikker **Beregn basert på stykkliste/formel** for å vise beregningsdetaljene og advarslene. Du kan også vise resultatene for stykklisteberegning på siden **Fullført**. For advarselsmeldinger gjelder bare to av advarselsbetingelsene for produserte varer, mens fire advarselsbetingelser gjelder alle varer:
-   Identifiser når en produsert var ikke har noen aktiv stykkliste.
-   Identifiser når en produsert vare ikke har noen aktiv rute.
-   Identifiser med varen på en stykklistelinje har antallet 0 (null).
-   Identifiser når varen på en stykklistelinje har kostnaden 0 (null), eller når den ikke har noen kostnadspost.
-   Identifiser når en vare på en stykklistelinje har en utdatert kostnad. Advarselen viser til en sammenligning av beregningsdatoen og antallet dager som er angitt for største tillatte alder for kostnad.
-   Identifiser når en vare på en stykklistelinje har en fortjeneste i prosent som er mindre enn den du ønsker.

Du kan definere flere stykklisteberegningsgrupper, avhengig av dine behov for variasjoner i advarsler. Én stykklisteberegningsgruppe som for eksempel har advarselsbetingelser for en aktiv stykkliste, et komponentantall som er 0 (null) og komponentkostnad som er 0 (null), kan være nok. Når du starter en stykklisteberegning, kan du overstyre advarselsbetingelsene som er tilordnet stykklisteberegningsgruppen. Du kan også legge til eller fjerne advarselsbetingelser. Hvis gjeldende situasjon for eksempel ikke omfatter rutedata, kan du fjerne den gjeldende advarselsbetingelsen for en aktiv rute. **Obs!** Timeregistrering inkluderer en **Beregningsgrupper**-side, men siden har ingen relasjon til stykklisteberegningsgrupper. I Timeregistrering kan arbeidere tilordnes til beregningsgrupper som gjenspeiler grupperingen av arbeidere som er tilknyttet samme arbeidsleder eller overordnet. Beregning av arbeiderregistreringer kan gjøres automatisk eller manuelt av en arbeidsleder eller overordnet.




