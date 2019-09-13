---
title: Oversikt over arbeidsnedbrytningsstruktur
description: En arbeidsnedbrytningsstruktur (WBS) er en beskrivelse av arbeidet som skal utføres for et prosjekt. Det er et hierarki av oppgaver som representerer prosjektteamets forståelse av arbeidssammensetningen og av størrelsen, kostnaden og varigheten til hver komponent eller oppgave.
author: KimANelson
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjWorkBreakdownStructure
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 23861
ms.assetid: 241a0464-0056-4a69-b468-0afbe2d5f3ae
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 78509898d0c2279750df3860a670d3d7a6badfc0
ms.sourcegitcommit: e286572ce94a9442a5b3076c3ff5b429be0ed512
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/06/2019
ms.locfileid: "1865586"
---
# <a name="work-breakdown-structures-overview"></a>Oversikt over arbeidsnedbrytningsstruktur

[!include [banner](../includes/banner.md)]

En arbeidsnedbrytningsstruktur (WBS) er en beskrivelse av arbeidet som skal utføres for et prosjekt. Det er et hierarki av oppgaver som representerer prosjektteamets forståelse av arbeidssammensetningen og av størrelsen, kostnaden og varigheten til hver komponent eller oppgave. En arbeidsnedbrytningsstruktur har tre viktige formål:

-   Beskrive oppdelingen eller sammensetningen av arbeid i oppgaver
-   Planlegge prosjektarbeidet
-   Beregne kostnaden for hver oppgave

Detaljnivået i en arbeidsnedbrytningsstruktur avhenger av nøyaktighetsnivået som kreves i estimater, og sporingsnivået som er nødvendig mot disse estimatene. Prosjekter som har svært lite slingringsmonn i tidsplan eller kostnader, krever vanligvis en mer detaljert arbeidsnedbrytningsstruktur og krever også grundig sporing av arbeidsfremdriften og kostnadene mot arbeidsnedbrytningsstrukturen. Denne typen prosjekt er vanlig innenfor konstruksjon og ingeniørarbeid. 

Prosjekter i bransjer som media og reklame, programvare og IT-infrastruktur er derimot ofte unike, og produktiviteten står i forhold til erfaringen og kompetansen til personen som utfører oppgaven. Disse bransjene bruker derfor en arbeidsnedbrytningsstruktur til å få et anslag av størrelsen på prosjektet, ikke til å spore fremdriften til prosjektet i detalj. 

Å utvikle en arbeidsnedbrytningsstruktur er en intensiv prosess som vanligvis gjøres over en lang periode og krever samarbeid og informasjon fra en rekke ulike personer. Dette emnet beskriver hvordan du kan bruke forbedringer av arbeidsnedbrytningsstruktur i Microsoft Dynamics 365 for Finance and Operations til å oppfylle behovene for estimater og sporing.

## <a name="prerequisites-for-creating-a-wbs"></a>Forutsetninger for å opprette en arbeidsnedbrytningsstruktur
For å kunne opprette en arbeidsnedbrytningsstruktur må du kunne lage en arbeidsplan og beregne arbeidskostnadene.

### <a name="prerequisites-for-creating-a-work-schedule"></a>Forutsetninger for å lage en arbeidsplan

Fullfør følgende konfigurasjon for å bruke alle planleggingsmulighetene i funksjonene for arbeidsnedbrytningsstruktur:

1.  Definer en standardkalender og en prosjektkalender:
    1.  Klikk **Prosjektstyring og regnskap** &gt; **Oppsett** &gt; **Parametere for prosjektstyring og regnskap** &gt; **Planlegging**. Angi en standardkalender i feltet **Standard arbeidskalender**. Dette blir standard arbeidskalender for nye prosjekter som opprettes.
    2.  Du kan endre standardkalenderen for et bestemt prosjekt. Klikk prosjektets detaljside, og oppdater deretter **Planleggingskalender**-feltet i hurtigfanen **Prosjektteam og planlegging** ved å velge en annen kalender.

2.  Definer standard arbeidsdager og arbeidstimer. Kalenderen du angir som arbeidskalenderen for prosjektet, vil bli brukt i arbeidsnedbrytningsstrukturen til å fastsette følgende informasjon:

-   Virkedager og fridager
-   Antall arbeidstimer per dag

Du definerer virkedagene og arbeidstimene for en kalender eller oppretter en ny kalender ved å klikke på **Organisasjonsstyring** &gt; **Felles** &gt; **Kalendere**.

### <a name="prerequisites-for-estimating-the-cost-of-work"></a>Forutsetninger for beregning av arbeidskostnadene

Hvis du vil bruke hele funksjonaliteten for kostnadsberegning i arbeidsnedbrytningsstrukturen, må du definere kost- og salgsprisene for arbeidere, arbeidskategorier, utgifter og gebyrer samt varer.

-   Du definerer kost- og salgsprisen for arbeid, utgiftene og gebyrkategorier ved å klikke på **Prosjektstyring og regnskap** &gt; **Oppsett** &gt; **Priser**.
-   Du definerer kost- og salgsprisen for varer ved å bruke **Forretningsavtaler**-siden for hver vare på listesiden **Frigitte produkter** i Behandling av produktinformasjon.

## <a name="creating-a-wbs"></a>Opprette en arbeidsnedbrytningsstruktur
Opprettelse av en arbeidsnedbrytningsstruktur omfatter tre aktiviteter:

1.  **Arbeidsnedbryting** – Opprett en oppdeling av arbeid i håndterbare deler eller oppgaver.
2.  **Arbeidsplan** – Beregn tiden det tar å fullføre en oppgave, angi avhengighetsforhold mellom oppgaver, og velg start- og sluttdatoer for oppgaver.
3.  **Kostnadsestimat** – Estimer kostnader for hver oppgave.

Delene nedenfor beskriver hvordan funksjonene for arbeidsnedbrytningsstruktur kan hjelpe deg med hver av disse aktivitetene.

### <a name="work-decomposition"></a>Arbeidsnedbryting

Å opprette en nedbryting eller oppdeling av arbeid er vanligvis det første trinnet i fremgangsmåten for å opprette en arbeidsnedbrytningsstruktur. Funksjonen for arbeidsnedbrytningsstruktur støtter følgende grunnleggende begreper for arbeidsnedbryting eller -oppdeling. 

**Prosjektrotoppgave** Prosjektrotoppgaven er sammendragsoppgaven på øverste nivå for et prosjekt. Alle andre prosjektoppgaver opprettes under den. Prosjektnavnet brukes alltid som navnet på rotoppgaven. Innsatsen, datoene og varigheten til rotnoden oppsummerer verdiene for oppgavene under rotoppgaven. Du kan ikke endre egenskapene for rotnoden eller slette den.

**Sammendrags- eller containeroppgaver** En sammendragsoppgave er en oppgave som har deloppgaver under seg. En sammendragsoppgave har ikke selv noen arbeidsinnsats eller kostnad. Arbeidsinnsatsen og kostnaden til en sammendragsoppgave er i stedet summen av arbeidsinnsatsen og kostnadene til deloppgavene. Den tidligste startdatoen for deloppgavene brukes som startdato for sammendragsoppgaven, og den seneste sluttdatoen for deloppgavene brukes som sluttdatoen. Du kan endre navnet på en sammendragsoppgave, men du kan ikke endre planleggingsegenskapene for innsats, datoer og varighet. Hvis du sletter en sammendragsoppgave, sletter du også alle deloppgavene for den. 

**Bladnodeoppgaver** En bladnodeoppgave representerer den mest kornete arbeidspakken på prosjektet. En bladnode har en estimert innsats, et planlagt antall ressurser, en planlagt start- og sluttdato og varighet. 

Du kan fullføre følgende hierarkioperasjoner for å aktivere opprettelsen av et arbeidshierarki eller en arbeidsoppdeling for et prosjekt. 

**Ny oppgave** Enhver ny oppgave du oppretter, legges automatisk til under rotnoden, og et WBS-nummer tilordnes automatisk til oppgaven. WBS-nummeret representerer oppgavens nivå i hierarkiet. Når det gjelder oppgavene på det første nivået under prosjektrotoppgaven, brukes nummereringen 1, 2, 3 og så videre. Når det gjelder oppgaver under det første nivået, brukes nummereringen 1.1, 1.2, 1.3 og så videre. For hvert nivå som legges til under et tidligere nivå, blir en ny serie med punktnumre lagt til. 

Du kan foreløpig ikke tilpasse WBS-nummereringen. 

**Rykk inn oppgave** Når du rykker inn en oppgave, blir den en underordnet for oppgaven som kommer før den. WBS-nummeret på den nye underordnede oppgaven beregnes automatisk på nytt basert på WBS-nummeret til den overordnede. Den overordnede oppgaven er nå en sammendrags- eller containeroppgave og blir derfor en opprulling av deloppgavene. 

> [!NOTE] 
> Når du rykker inn oppgaver under en oppgave som var en bladnode før innrykksoperasjonen, mister den nyopprettede sammendragsoppgaven datoene, innsatsen og antallet ressurser som tilhører den. Den bruker nå et sammendrag av verdiene for de nye deloppgavene. 

**Rykk ut oppgave** Når du rykker ut en oppgave, er den ikke lenger en deloppgave for den overordnede. WBS-nummeret for denne oppgaven beregnes automatisk på nytt for å gjenspeile oppgavens nye nivå i hierarkiet. Innsats, kostnader og datoer for oppgavens tidligere overordnede oppgave beregnes på nytt for å utelate denne oppgaven. 

**Flytt opp og Flytt ned** Når du klikker **Flytt opp** og **Flytt ned**, endrer du posisjonen til en oppgave i hierarkiet til dens overordnede. Posisjonen til en oppgave påvirker ikke oppgavens innsats, kostnader, datoer eller varighet. WBS-nummeret for oppgaven beregnes imidlertid automatisk på nytt for å gjenspeile oppgavens nye posisjon.

### <a name="schedule-estimation"></a>Tidsplanestimering

Tidsplanestimering er vanligvis det andre trinnet i opprettelsen av en arbeidsnedbrytningsstruktur. Den anbefalte fremgangsmåten er å fullføre tidsplanestimering etter at du opprettet oppgavene. Siden **Arbeidsnedbrytningsstruktur** i Finance and Operations har to deler. Den øvre ruten er ment for tidsplanestimering, og den nedre ruten inneholder fanen **Estimerte kostnader og omsetning** som du kan bruke til kostnadsestimering. 
**Oppgaveavhengigheter** I en arbeidsnedbrytningsstruktur kan du opprette en forgjengerrelasjon mellom oppgaver. Når du tilordner forgjengeroppgaver til en oppgave, kan denne oppgaven bare starte etter at alle forgjengeroppgavene er fullført. Den planlagte startdatoen for oppgaven settes automatisk til den siste datoen for alle forgjengerne. 

**Oppgaveplanlegging i Microsoft Dynamics 365 for Finance and Operations** Følgende faktorer fastsetter planleggingen av bladnodeoppgaver:

-   Forgjengere
-   Innsats
-   Antallet ressurser
-   Start- og sluttdatoer

Startdatoen for en bladnodeoppgave som ikke har forgjengere settes automatisk til planleggingsstartdatoen for prosjektet. Varigheten til en bladnodeoppgave beregnes alltid som antall virkedager mellom start-og sluttdato. 

*<strong><em>Planleggingsregler</em></strong>* Når automatisk planlegging er aktivert, gjelder følgende regler for oppgaveplanlegging for bladnodeoppgaver:

-   Start- og sluttdatoene for en oppgave må være virkedager, i henhold til prosjektets planleggingskalender.
-   Startdatoen for en oppgave som har forgjengere, settes automatisk til den seneste sluttdatoen for forgjengerne.
-   Innsatsen for en oppgave beregnes automatisk slik:

Antall personer × varighet x antall timer for en standard arbeidsdag i prosjektkalenderen. 

I noen tilfeller kan det hende at du vil avvike fra disse reglene. Du kan deaktivere automatisk planlegging for å unngå at Finance and Operations automatisk angir eller retter egenskaper for bladnodeoppgaver. Når du registrerer informasjon for en oppgave som forårsaker et brudd på en hvilken som helst planleggingsregel, vises et ikon for planleggingsfeil for oppgaven. Hvis du ikke vil at planleggingsfeil vises, klikker du **Planleggingsfeil vises** for å deaktivere funksjonen. 

> [!NOTE] 
> Verdiene for en sammendrags- eller containeroppgave blir fortsatt beregnet som summen av verdiene til deloppgavene, uavhengig av om automatisk planlegging er aktivert eller deaktivert. 

**Rette planleggingsfeil** Når automatisk planlegging er aktivert, oppstår det sannsynligvis ikke planleggingsfeil. Hvis du imidlertid deaktiverer automatisk planlegging og deretter aktiverer den på nytt senere, vises kanskje ikonet for planleggingsfeil i arbeidsnedbrytningsstrukturen. 

**Rette planleggingsfeil etter oppgave** Når du dobbeltklikker ikonet for planleggingsfeil for en bestemt oppgave, vises en dialogboks der alle planleggingsfeilene for denne oppgaven vises. Du kan bestemme hvilke planleggingsfeil du vil rette for oppgaven. 

**Rette alle planleggingsfeil** Hvis du vil bruke Finance and Operations til å rette alle planleggingsfeil i arbeidsnedbrytningsstrukturen, klikker du **Reparer alle planleggingsavvik**. 

> [!NOTE] 
> Denne funksjonen kan føre til betydelige endringer i arbeidsnedbrytningsstrukturen. Feil rettes opp i følgende rekkefølge:

1.  Den estimerte innsatsen for alle oppgaver endres slik at den er lik kapasiteten som er definert i prosjektkalenderen.
2.  Startdatoen for hver oppgave endres slik at oppgaven starter etter at alle forgjengeroppgavene er fullført.
3.  Startdatoen for hver oppgave endres for å fjerne mellomrom i startdatoene for forgjengeroppgavene.

### <a name="cost-estimation"></a>Kostnadsanslag

Som nevnt tidligere i dette dokumentet kan du angi kostnadsestimeringen for hver bladnodeoppgave ved hjelp av den **Estimerte kostnader og omsetning** i den nedre ruten på siden **Arbeidsnedbrytningsstruktur**. 

> [!NOTE] 
> Du kan ikke endre kostnadsestimeringen for en sammendrags- eller containeroppgave. Kostnadsestimeringen for et sammendragsoppgave er lik summen av kostnadsestimeringen bladnodeoppgavene for den. Estimert total kostnad for hver oppgave beregnes som summen av de estimerte kostbeløpene for følgende transaksjonstyper:

-   Arbeid
-   Vare eller materiale
-   Utgifter

Transaksjonstypen **Gebyr** brukes til å estimere gebyrbasert omsetning. Denne transaksjonstypen har ingen kostnadskomponent, og derfor tas det ikke hensyn til den når kostnader estimeres. 

Transaksjonstypen **A konto** brukes til å registrere den avtalte salgsverdien i et prosjekt av typen fast verdi. Denne transaksjonstypen tas heller ikke hensyn til når kostnader estimeres. 

Når du beregner kostnader for arbeid, materiale og utgifter for hver oppgave, må du tilordne en prosjektkategori til estimert kost. 

**Beregning av arbeidskostnader** For hver bladnodeoppgave tilordner du en arbeidsinnsats i timer og en standardkategori. Når du definerer en tidsplan for en oppgave, blir derfor arbeidskostnadsestimatet automatisk lagt til i standardkategorien for arbeid. Dette kostnadsestimatet vises i fanen **Estimerte kostnader og omsetning** i rutenettet **Linjedetaljer** for denne oppgaven. Hvis du trenger flere arbeidskostnadsestimater, kan du legge dem til på denne kategorien. Hvis du øker eller reduserer timene på lønnskostnaden, beregnes tidsplanen for oppgaven automatisk. 

**Beregne utgifter og materialkostnader** Du kan også bruke fanen **Estimerte kostnader og omsetning** til å beregne utgifter og materialkostnader for en oppgave, hvis du trenger estimater. 

Kost- og salgsprisen for hvert arbeids- eller utgiftsestimat er basert på definisjonen som brukes for hver kategori i prissettingstabellene i **Prosjektstyring og regnskap** &gt; **Oppsett** &gt; **Prissetting**. Når det gjelder varer, blir kost- og salgspris som standard lagt til fra vare- eller forretningsavtalene på listesiden **Frigitte produkter** i Behandling av produktinformasjon.

## <a name="tracking-progress-on-the-wbs"></a>Spore fremdrift i arbeidsnedbrytningsstrukturen
Enkelte bransjer sporer fremdriften til et prosjekt mot en arbeidsnedbrytningsstruktur på et svært detaljert nivå, mens andre sporer fremdriften på et høyere nivå i arbeidsnedbrytningsstrukturen. Denne delen beskriver hvordan du kan bruke WBS-sporing for prosjektkravene. 

Finance and Operations har tre visninger for arbeidsnedbrytningsstrukturen for et prosjekt: planleggingsvisning, visning av innsatssporing og visning av kostnadssporing.

### <a name="planning-view"></a>Planleggingsvisning

Planleggingsvisningen viser det planlagte estimatet eller basisestimatet for tidsplanen og kostinformasjonen. Selv om det ikke finnes noen funksjoner for å spore versjonen og basisen for en arbeidsnedbrytningsstruktur for prosjekt, er verdiene i denne visningen ment å representere basisversjonen. Delene Tidsplanestimering og Kostnadsestimat i dette emnet beskriver denne visningen og hvordan den brukes til å opprette en arbeidsnedbrytningsstruktur.

### <a name="effort-tracking-view"></a>Visning av innsatssporing

Visningen av innsatssporing viser sporing av fremdriften for oppgaver i arbeidsnedbrytningsstrukturen. Den sammenligner de akkumulerte faktiske innsatstimene for en oppgave med de planlagte innsatstimene. Følgende formler gir verdiene i visningen av innsatssporing:

-   Fremdriftsprosent = faktisk innsats hittil ÷ planlagt innsats for oppgaven
-   Gjenstående innsats (også kalt ETC \[Estimate-to-complete\]) = planlagt innsats – faktisk innsats hittil
-   EAC (Estimate at Complete) = gjenstående innsats + faktisk innsats hittil
-   Prosjektert innsatsavvik = planlagt innsats – EAC

Visningen av innsatssporing viser en prosjektering av innsatsavviket for oppgaven basert på om EAC er større eller mindre enn planlagt innsats:

-   Hvis EAC er større enn planlagt innsats, prosjekteres oppgaven å ta lengre tid enn opprinnelig planlagt og er etter tidsplanen.
-   Hvis EAC er mindre enn planlagt innsats, prosjekteres oppgaven å ta mindre tid enn opprinnelig planlagt og er foran tidsplanen.

**Prosjektlederens nye prosjektering av innsats** Av og til må prosjektlederen eller en annen person som sporer fremdriften for et prosjekt, revidere de opprinnelige estimatene for en oppgave. Oppgaven kan gå raskere eller tregere enn forventet av ulike årsaker. Omfanget kan for eksempel ha blitt redusert, eller arbeidere har mindre erfaring enn opprinnelig planlagt. Prosjekteringer er en prosjektleders oppfatning av estimater basert på den gjeldende statusen til et prosjekt. Du bør vanligvis ikke endre basistallene, fordi en prosjektbasis representerer mye publisert dokument for prosjektets tidsplan og kostnadsestimat som alle interessenter på prosjektet har avtalt. 

Prosjektledere kan endre innsatsen på oppgaver på to måter:

-   Endre den gjenstående innsatsen som er automatisk satt til å oppdatere den faktiske gjenstående innsatsen på oppgaven.
-   Endre fremdriftsprosenten som er automatisk satt til å oppdatere den faktiske fremdriften i oppgaven.

Begge disse metodene fører til en omberegning av oppgavens ETC, EAC og fremdriftsprosent samt det prosjekterte innsatsavviket i oppgaven. EAC, ETC og fremdriftsprosenten i sammendragsoppgaver beregnes også på nytt, og det prosjekterte innsatsavviket oppdateres. 

**Endret innsats i sammendragsoppgaver** Du kan endre innsatsen i sammendrags- eller containeroppgaver. Uansett om du endrer disse verdiene ved hjelp av den gjenstående innsatsen eller fremdriftsprosenten i sammendragsoppgaven, skjer beregningene automatisk i følgende rekkefølge:

1.  EAC, ETC og fremdriftsprosenten i oppgaven blir beregnet.
2.  Nytt EAC distribueres til de underordnede oppgavene i samme proporsjon som det opprinnelige EAC-beløpet.
3.  Nytt EAC i hver bladnodeoppgave beregnes.
4.  Den gjenstående innsatsen og fremdriftsprosenten beregnes på nytt for alle berørte underordnede oppgaver basert på den nye EAC-verdien. Innsatsavviket for oppgavene beregnes også på nytt.
5.  EAC for sammendragsoppgavene beregnes også på nytt fra bladnodene.

Klikk **Utvid til nivå** i visningen av innsatssporing for å angi hvilket nivå du vil spore og vedlikeholde arbeidsnedbrytningsstrukturen på. Arbeidsnedbrytningsstrukturen utvides automatisk til dette nivået i visningen av innsatssporing hver gang du åpner den.

### <a name="cost-tracking-view"></a>Visning av kostnadssporing

Visningen av kostnadssporing viser sporingen av kostnadsforbruk for en oppgave. I denne visningen blir de faktiske kostnadene som er brukt på en oppgave hittil, sammenlignet med de planlagte kostnadene for oppgaven. Følgende formler gir verdiene i visningen av kostnadssporing:

-   Prosent av brukt kostnad = faktisk kostnad hittil ÷ planlagt kostnad for oppgaven
-   CTC (Cost to complete) = planlagt kostnad – faktisk kostnad hittil
-   EAC (Estimate at complete) = CTC + faktisk kostnad hittil
-   Prosjektert kostnadsavvik = planlagt kostnad – EAC

Visningen av kostnadssporing viser en prosjektering av kostnadsavvik for oppgaven basert på om EAC er større eller mindre enn planlagt kostnad:

-   Hvis EAC er større enn planlagt kostnad, prosjekteres oppgaven å bruke mer penger enn opprinnelig planlagt og er over budsjettet.
-   Hvis EAC er mindre enn planlagt kostnad, prosjekteres oppgaven å bruke mindre penger enn opprinnelig planlagt og er under budsjettet.

**Prosjektlederens nye prosjektering av kostnader** Prosjektledere må bruke CTC til å revidere det opprinnelige kostnadsestimatet i en oppgave. Prosjektlederen kan endre CTC-verdien til kostnaden som er nødvendig for å fullføre oppgaven. Hvis du endrer CTC-verdien, beregnes oppgavens CTC, EAC og prosent av brukt kostnad samt det prosjekterte kostnadsavviket på nytt. EAC, ETC og prosenten av brukt kostnad i sammendragsoppgavene beregnes også på nytt, og det prosjekterte kostnadsavviket oppdateres. 

> [!NOTE] 
> Når du endrer innsats for en WBS-oppgave i visningen av innsatssporing, beregnes oppgavens CTC, EAC, prosent av brukt kostnad og prosjektert kostnadsavvik på nytt i visningen av kostnadssporing. Kostnadsendringer påvirker imidlertid ikke verdiene i visningen av innsatssporing, fordi kostnaden etter transaksjonstype (arbeid, materiale eller utgift) eller prosjektkategori ikke endres. 

**Prosjekteringsendring for kostnader i sammendragsoppgaver** Du kan du endre kostnadene i sammendragsoppgaver, og beregningene skjer automatisk i følgende rekkefølge:

1.  EAC, CTC og prosent av brukt kostnad i oppgaven beregnes på nytt.
2.  Nytt EAC distribueres til de underordnede oppgavene i samme proporsjon som opprinnelig EAC i oppgavene.
3.  Nytt EAC beregnes for hver oppgave.
4.  CTS og prosenten av brukt kostnad beregnes på nytt for de berørte underordnede oppgavene basert på EAC-verdien. Kostnadsavviket for oppgavene beregnes også på nytt.
5.  EAC for alle sammendragsoppgavene beregnes basert på denne endringen.

Klikk **Utvid til nivå** i visningen av kostnadssporing for å angi hvilket nivå du vil spore og vedlikeholde arbeidsnedbrytningsstrukturen på. Arbeidsnedbrytningsstrukturen utvides til dette nivået i visningen av kostnadssporing hver gang du åpner den.

### <a name="earned-value-management"></a>Administrasjon av opptjent verdi

Du kan bruke metoden for opptjent verdi til å spore fremdriften til et prosjekt. Du kan vise mål for opptjent verdi i rollesenteret for prosjektlederen. Diagramkomponenten for opptjent verdi viser de tidsinndelte verdiene for planlagte verdi og faktiske kostnader. Opptjent verdi per gjeldende dato vises som et punkt. Tidsinndelte data for opptjent verdi er foreløpig ikke tilgjengelige. 

Tidsfasen i diagrammet for opptjent verdi vises etter uke eller måned. Denne delen beskriver de tre pilarene i metoden for opptjent verdi: planlagt verdi, opptjent verdi og faktiske kostnader. 

**Planlagt verdi** Teorien bak metoden for opptjent verdi angir at grafen for den planlagte verdien representerer hvor raskt prosjektets team planla å opptjene verdi i prosjektet. 

Finance and Operations bruker opptjeningsregelen 0:100 når det tegner inn planlagt verdi. Under denne regelen posteres verdien for oppgaven i oppgaven per sluttdatoen. Ingen verdi posteres før oppgaven er 100 prosent fullført. 

I Prosjektstyring og regnskap angir du sluttdatoen for bladnoder og de planlagte kostnadene for den. Når grafen for planlagt verdi vises etter uke, summeres planlagt verdi etter uke for alle bladnodeoppgaver i løpet av prosjektet. 

**Opptjent verdi** Teorien bak metoden for opptjent verdi angir at grafen for den opptjente verdien representerer hvor raskt prosjektets team faktisk opptjener verdi i prosjektet. 

Finance and Operations bruker opptjeningsregelen 0:100 når det tegner inn opptjent verdi. Under denne regelen posteres verdien for oppgaven i oppgaven per sluttdatoen. Ingen verdi posteres før oppgaven er 100 prosent fullført. 

Når opptjent verdi beregnes, tas det hensyn til fremdriftsprosenten for hver oppgave. Under opptjeningsregelen 0:100 er det bare oppgaver som fullføres i en gitt periode, som vurderes for beregningen av opptjent verdi ved slutten av denne perioden. Opptjent verdi på prosjektet beregnes for alle oppgaver som er fullført når grafen lages. 

> [!NOTE] 
> Foreløpig har ikke systemet for WBS-sporing datastrukturer for lagring av historisk fremdriftsprosent for hver oppgave. Opptjent verdi kan derfor bare rapporteres når kuben behandles. Behandle kuben regelmessig for å oppdatere dataene for opptjent verdi som vises i rollesenteret. 

**Faktiske kostnader** Teorien bak metoden for opptjent verdi angir at grafen for den faktiske kostnaden representerer hvor raskt penger brukes på prosjektet. 

Transaksjoner som posteres til et prosjekt, brukes til å tegne linjen for faktiske kostnader. Kostnadene summeres etter dato. Disse dataene brukes deretter til å tegne de faktiske kostnadene etter uke eller måned i diagrammet for opptjent verdi.

### <a name="how-to-use-the-concepts-of-planned-value-earned-value-and-actual-cost"></a>Bruke begrepene om planlagt verdi, opptjent verdi og faktiske kostnader

**Tidsplanavvik** Under planleggingen oppretter du en prognose for arbeid på en tidslinje. Planlagt verdi er derfor hvor raskt prosjektplanleggere trodde at arbeid kom til å bli fullført på prosjektet. Etter at et prosjekt har kommet i gang, fullføres arbeid, og prosjektet tjener verdi. Når du sammenligner planlagt verdi med opptjent verdi, kan du vise hvordan arbeidsfremdriften er på et prosjekt. Resultatet av denne sammenligningen kalles tidsplanavvik. 

Hvis den planlagte verdien for en periode er større enn den opptjente verdien, er mengden arbeid som er utført på et prosjekt, mindre enn det som var planlagt. Derfor ligger prosjektet etter tidsplanen. Siden planlagt verdi og opptjent verdi uttrykkes monetært, får også forsinkelse på prosjektet en monetær verdi. 

Hvis den planlagte verdien for en periode er mindre enn den opptjente verdien, er mengden arbeid som er utført på et prosjekt, mer enn det som var planlagt. Derfor ligger prosjektet foran tidsplanen. Denne foranliggende tiden får også en monetær verdi.

**Kostnadsavvik** Siden opptjent verdi bruker kostprisen som multiplikatoren, angir opptjent verdi kostnaden for arbeidet som gjøres på et prosjekt. Etter hvert som et prosjekt går fremover, gir transaksjonsloggen en oversikt over penger som faktisk er brukt på dette prosjektet. Når du sammenligner opptjent verdi med faktiske kostnader, kan du vise hvor mye penger som brukes i forhold til verdien som opptjenes. Resultatet av denne sammenligningen kalles kostnadsavvik. 

Hvis den faktiske kostnaden som brukes for en periode, er større enn den opptjente verdien, ble mer penger brukt enn opptjent. Derfor er prosjektet over budsjettet. 

Hvis den faktiske kostnaden som brukes for en periode, er mindre enn den opptjente verdien, ble mer penger opptjent enn brukt. Derfor er prosjektet under budsjettet.

## <a name="wbs-templates"></a>WBS-maler
Du kan bruke funksjonen for WBS-maler til å opprette standardmaler for prosjekter. Hvis prosjektene som firmaet ditt tilbyr, omfatter mye arbeid som kan gjentas, bør du vurdere å opprette en WBS-mal. 

Du kan opprette en WBS-mal fra arbeidsnedbrytningsstrukturen i et eksisterende prosjekt, slik at kunnskapen og de anbefalte fremgangsmåtene du ervervet under planleggingen av dette prosjektet, kan brukes på nytt på lignende prosjekter i fremtiden. Enkelte ganger er det imidlertid kanskje ikke aktuelt å lagre hele arbeidsnedbrytningsstrukturen som en mal. Derfor kan du også opprette maler fra deler av arbeidsnedbrytningsstrukturen for et prosjekt.

### <a name="saving-a-projects-wbs-as-a-template"></a>Lagre et prosjekts arbeidsnedbrytningsstruktur som en mal

Når du oppretter en mal, kan du importere den til arbeidsnedbrytningsstrukturen for et nytt prosjekt under rotnoden eller under en hvilken som helst oppgave i arbeidsnedbrytningsstrukturen for prosjektet.

### <a name="importing-a-wbs-template-into-a-projects-wbs"></a>Importere en WBS-mal til arbeidsnedbrytningsstrukturen for et prosjekt

Når du importerer oppgaver, er oppgavene i malen organisert basert på startdatoen for oppgaven de importeres under. Under importen brukes forgjengerrelasjoner i maloppgavene til å beregne startdatoene for de importerte oppgavene. Målprosjektets standard arbeidskalender brukes til å beregne sluttdatoene for de importerte oppgavene, slik at virkedager og standard arbeidstimer som er definert i det gjeldende prosjektets arbeidskalender, beholdes. 

Kostnadsbeløp og salgspriser på estimatlinjene brukes for å garantere at priser som gjelder spesifikt for prosjektet eller prosjektkontrakten, har gyldige datoer.

### <a name="differences-between-a-projects-wbs-and-a-wbs-template"></a>Forskjellen på arbeidsnedbrytningsstrukturen for et prosjekt og en WBS-mal

-   Oppgavene i WBS-maler har ikke startdatoer og sluttdatoer.

Arbeidsdagene og fridagene angis ikke for WBS-maler.

-   WBS-maler bruker alltid planleggingskalenderen som er definert som standardkalenderen for alle prosjekter.

Standard planleggingskalender brukes bare til å finne ut hvor mange timer det er i en standard virkedag.

-   Forgjengerrelasjoner kopieres ikke til en WBS-mal.

Siden WBS-maler ikke har datoer, kreves ikke stardatologikken som er basert på en forgjengers sluttdato.

-   En estimatlinje for arbeidskostnad opprettes automatisk når en oppgave opprettes i en WBS-mal. Salgsprisen og kostbeløpet kopieres fra den valgte arbeideren.

Utgift og varekost kan opprettes manuelt, på samme måte som i en arbeidsnedbrytningsstruktur for et prosjekt.

-   Planleggingsfeil vises når det er avvik fra følgende formel:

Arbeid = antall ressurser × varighet x antall timer for en standard arbeidsdag 

Du kan rette opp alle planleggingsfeil samtidig ved å klikke **Rett opp alle feil i tidsplan**. 

Du kan også rette planleggingsfeil individuelt ved å klikke advarselsikonet for hver oppgave.



