---
title: Handelsrabattbehandling
description: Dette emnet beskriver handelsrabattbehandling for Microsoft Dynamics 365 for Finance and Operations.
author: t-benebo
manager: AnnBe
ms.date: 08/17/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: t-benebo
ms.search.validFrom: 2018-01-31
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 550815c5c3fc9a24ec8b67f2a340e0553eef072d
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843343"
---
# <a name="trade-allowance-management"></a>Handelsrabattbehandling

[!include [banner](../includes/banner.md)]

Handelsrabattbehandling hjelper firmaer med å administrere salgstilbudsprogrammer som støtter retail "betal for ytelse" monetære belønninger for kunder som oppnår volum- og atferdsmål. Funksjonene er utformet for firmaer som fokuserer på omfattende kampanje-til-fortjeneste-prosesser, fra kampanjefondbudsjettering og tildelingen, til fradrag Kontraktoppsett, krav for oppretting og behandling, til betalingsbehandling til analyse av kampanjeeffektiviteten.


Denne artikkelen gir en omfattende oversikt over funksjonen godtgjørelse for behandling av handel og vil gjør deg kjent med de vanlige oppgaver som er involvert i behandling av et program for salgstilbud. Flere typer brukere som har drift og beslutningen om å gjøre ansvarsområder forventes å bruke denne funksjonaliteten til å oppnå sine respektive målene:

- Tildeling av detaljert midler til de valgte kontoene, og definere forretningsavtaler for rabatten for kampanjer, basert på stykklisten tilbake og engangs engangsbeløp betalinger (for en avtalt service)
- Kjører forhandlet kampanjen kontraktene via pågående mva og generering av faktura-back krav
- Beregning, godkjenning, og behandler genererte krav, eller sende dem til kunder som fradrag for utligning av leverandørbetaling
- Avstemme kundens korttidsbetaling med trekk som er forfalt
- Spore bruken av kampanjefond og evaluere programmets lønnsomhet og effektiviteten

## <a name="audience-and-purpose"></a>Målgruppe og formål

Informasjonen i dette dokumentet er ment for forretningsmessige beslutningstakere i bedriftsselskaper, i stillinger som innkjøpssjef, finansdirektør og regnskapsfører, som har følgende ansvar:

- Budsjetter og tildeling av midler på høyt nivå
- Planlegging og analysering av tilbud
- Administrasjon av ansatte som behandler faktura bakover krav, kjører betalinger basert på merchandizing hendelser, og utligner korttidsbetalinger og -fradrag

Folk i disse rollene ser etter måter å oppnå disse målene på:

- Bedre utnyttelse av markedsføringstilbudsmidler.
- Fleksibelt imøtekomme ulike typer kampanjeprogrammer og rabatter.
- Reduser administrasjonsbelastningen og feilene som er knyttet til overvåking av kampanjeresultater og behandlingskrav.
- Forbedre kontantstrømsprognosene ved å tilføre fremtidig gjeld.
- Ha et kvantifisert grunnlag for løpende og fremtidige forhandlinger med kunder om kampanjer.

## <a name="promotional-fund-and-trade-allowance-agreement"></a>Kampanjemidler og handelsrabattavtale

En handelsrabattavtale er et belønningsprogram der betal for ytelse monetære belønninger tilbys til kunder som oppnår spesifikke mål for volum og/eller atferd. Kampanjemidler er budsjetterte utgifter. På den måten kan tilbudskampanjene registreres.

### <a name="promotional-fund"></a>Kampanjefinansiering

Midler som er tildelt til handelsrabattavtaler, registreres på **Midler**-siden. Du åpner **Midler**-siden ved å velge **Salg og markedsføring** \> **Handelsrabatter** \> **Midler** \> **Midler**.

![Midler-siden](./media/trade-allowance-management-funds-page.png "Midler-siden")

På **Midler**-siden kan du vise detaljene for kampanjemidler.

Hurtigkategorien **Generelt** viser perioden som midlene er gyldig for, og det budsjetterte beløp. For at midlene skal tildeles til kampanjeavtalen må **Status**-feltet må ha verdien **Godkjent**.

Hurtigfanen **Kunder** viser kundehierarkiet. For å velge kundene som midlene er målrettet mot, drar du dem slik at de under **Finansieringskunder**. Denne hurtigfanen viser også hvordan totalbeløpet for midlene distribueres.

Hurtigfanen **Varer** viser varene som er inkludert i kampanjen.

### <a name="trade-allowance-agreement"></a>Handelsrabattavtale

Når middeldefinisjonen er på plass, er neste trinn i planleggingen av kampanjen å registrere kampanjekontrakter (som kalles handelsrabattavtaler), tildele midler og definere ytelsesmål for hver merchandizing-hendelse.

Handelsrabattavtaler registreres på siden **Handelsrabattavtaler**. Åpne siden **Handelsrabattavtaler** ved å velge **Salg og markedsføring** \> **Handelsrabatter** \> **Handelsrabattavtaler**.

![Siden Handelsrabattavtaler](./media/trade-allowance-management-agreements-page.png "Siden Handelsrabattavtaler")

#### <a name="header"></a>Hode

Velg **Hode** for å bytte til hodvisning.

På hurtigfanen **Generelt** definerer feltene **Ordre til** og **Ordre fra** perioden når avtalen er gyldig. Godkjenningsstatusen **Godkjent intern** for avtalen angir at avtalen er ennå ikke gyldig, og kan ikke brukes under behandling av salgsordren.

**Analyse**-delen av hurtigfanen **Generelt** inneholder viktige felt som definerer antallene og kostnadene som er brukt for kampanjenevalueringen:

- Feltet **Basisenheter** angir hvor mange varer som må selges til de valgte kundene før kampanjen trer i kraft.
- Verdien **Beregnet forsendelsesantall** beregnes på grunnlag av verdien **Økningsprosent**, som er en planlagt måløkning for denne kampanjen.
- Feltet **Kostnad for handelsrabatt** beregnes basert på antall ulike hendelser i handelsrabattavtalen.

På hurtigfanen **Kunder**, i listen til venstre, kan du velge og vise kundegruppene som er definert som forhåndsdefinerte hierarkier. Du kan deretter velge hele hierarkiet eller bestemte kontoer som mål for rabattavtalen.

På hurtigfanen **Varer**, per hurtigkategorien **Varer** på **Midler**-siden blir varer lagt til i avtalen for å tilknytte salgene med rabatten som er avtalt.

På hurtigfanen **Midler** kan du se kampanjemidlene som er knyttet til denne kontrakten. Du kan også vise kontraktens hendelsen kostnadsavregning. En hendelse kostnadsfordeling på 100 prosent betyr at denne kampanjen skal finansieres utelukkende fra én fond. En kampanjeavtale kan også bruke av flere midler, og kan bruke lik eller differensiert fordeling.

#### <a name="lines"></a>Linjer

Velg **Linjer** å bytte til linjevisning.

Kategorien **Varehandelshendelser** viser hvilke typer hendelser som er dekket av en avtale. Det finnes tre typer: tilbakebetaling, engangsbeløp og fakturafradrag.

Når du velger varehandelshendelsen og deretter velger **Beløp**-kategorien, blir detaljer for hendelsen funnet.

![Linjer i handelsrabattavtale](./media/trade-allowance-management-agreements-lines.png "Linjer i handelsrabattavtale")

I delen **Handelsrabattlinjer** angir du antalls- eller mengdeområdene som kunden må oppnå, for definisjoner for å få belønninger.

Når det gjelder en varehandelshendelse av typen **tilbakebetaling**, definerer den øvre delen av **Beløp**-kategorien reglene som brukes for tilbakebetalingen. Reglene kan for eksempel angi følgende betingelser for kravet om tilbakebetaling:

- Det er basert på opprettelsesdatoen for salgsordren (verdien for **Beregningsdatotype** er **Opprettet**).
- Det beregnes basert på salgsordrelinjens beløp før rabatter, ikke nettobeløpet, inkludert rabatter (**Tatt fra**-verdien er **Brutto**).
- Det er basert på antall solgte produkter, ikke beløpet (verdien **Linjeskifttype for rabatt** er **Antall**).
- Det beregnes per periode av en måned (verdien **Summer salg etter** er **Måned**). 
- Det utlignes som et fradrag, ikke ved hjelp av en A/P (verdien for **Betalingstype** er **Kundefradrag**).

Når det gjelder en varehandelshendelse av typen **engangsbeløp**, viser kategorien **Beløp** antallet som skal betales til kunden i form av et fradrag når kunden oppnår spesifikke ytelse. Godkjenningsstatusen **Åpen** angir at engangsbeløpet ennå ikke er betalt.

Hvis du vil bruke avtalen på salgsordrer som oppfyller betingelsene for avtalen, må statusen for den avtalen være **Bekreftet**. 

## <a name="perform-sales-under-the-planned-merchandising-event-and-generate-bill-back-claims"></a>Gjennomføre salg under den planlagte varehandelshendelsen og generere tilbakebetalingskrav

Når du oppretter en salgsordre med linjene som oppfyller kravene til avtalen, kan du vise relatert informasjon på siden **Salgsordre** ved å velge **salgsordrelinje** \> **Vis** \> **Prisdetaljer**.

På siden **Prisdetaljer** i **Rabatter**-hurtigkategorien, ser selgeren en tilbakebetaling fra gyldig godtgjørelse forretningsavtalen (rabattens program-ID vises) og det totale beløpet som er brukt på linjen. Beløpet vises også i feltet **Rabattbeløp** i delen **Marginestimat** for siden **Prisinformasjon**.

Når salgsfakturaen er postert, blir det generert et tilsvarende tilbakebetalingskrav for hver fakturalinje.

> [!NOTE]
> For å åpne siden **Prisdetaljer**, på siden **Kundeparametere** i **Priser**-kategorien velger du **Aktiver Prisdetaljer**-merket. I

## <a name="process-claims-and-pass-them-as-deductions-to-ar"></a>Behandle krav og sende dem som fradrag til kunder

De neste trinnene i prosessen for håndtering av tilbakebetalinger er å gjennomgå, beregne og godkjenne krav og deretter konvertere dem til fradrag.

Den tilbake arbeidsbenk faktura er der eieren av kampanjen avtalen med jevne mellomrom ser gjennom, og behandler krav som genereres. Det er også der kunder administratoren konverterer godkjente krav til fradrag eller regelmessige betalinger, avhengig av betalingsmåten for kravet.

På siden **Arbeidsområde for tilbakebetaling** kan du gå gjennom kravlinjene. Hvis det er krav med statusen **Skal omberegnes**, må de beregnes på nytt for en akkumulert effekt.

### <a name="recalculate-claims"></a>Omberegne krav

Hvis du vil omberegne krav, i handlingsruten, velger du **Summer**. Deretter, i dialogboksen **Slå sammen rabatter**, velger du kunden.

Som et resultat av omberegningen genereres nye krav knyttet til antallene som justerer opprinnelige krav til kvalifiserte beløp per enhet. En justering krav genereres for hver unike kombinasjon av en kunde, en vare, en valuta, en enhet, lagerdimensjoner, finansdimensjoner, og en mva-gruppe. Disse justering krav som har samme referansen til ordren og fakturahodet salgsnummeret som krav som som justeres (det vil si krav som opprinnelig ble opprettet fra salgsdokumentet). I motsetning til de opprinnelige kravet har ikke kravet justering verdier i feltene som beskriver den opprinnelige salgsordrelinjens beløp og antall.

Når omberegningen er fullført, endres statusen for krav til **beregnet**. Hvis du vil godkjenne krav, i handlingsruten, velger du **Godkjenn**.

### <a name="process-claims-and-pass-them-to-ar"></a>Behandle krav og sende dem til kunder

Kravene er nå klar for behandling av kunder. Hvis du vil behandle, i handlingsruten, velger du **Prosess**. 

Statusen er endret ved behandling av krav til **merket**, og angir at en journalpostering (journalen som er postert, er rabatten avsetning journalen, som er angitt i parameterne kunder) har forårsaket oppstår følgende hendelser: 

- Krav er overført til midlertidige kundesaldoen som fradrag.
- Kontoen avsetning rabatten er kreditert for å representere fremtidige ansvaret for kunden.
- Utgiftskontoen rabatten har blitt debitert for å gjenkjenne kostnaden som er påløpt i forbindelse med salg.

For å fullføre prosessen, må den kunder clerk nå håndtere fradrag av belastning ved å overføre dem til på saldoen for kunder som kreditnota (gjeld). 

Å starte oppgaven, i handlingsruten for **Kunde**-siden, velger du **Samle** \> **Utlign transaksjoner**. På siden **Utlign transaksjoner** velger du **Funksjoner** \> **Program for tilbakebetaling**. Denne rabattsiden viser alle tilbakebetalingskrav som tidligere er behandlet.

Hvis du vil opprette en kreditnota, velger du **Merk**-merket for alle linjer, og velg deretter **Funksjoner** \> **Opprett kreditnota**.

En journal posteres ved oppretting av kreditnotaen. (Journalen som er postert, er AR-forbruksjournal, som er angitt i Kunder-parametere.) I så fall er den reelle gjelden (kreditten) flyttet til kundesaldoen. Økonomisk betyr dette at det oppstår følgende hendelser:

- Kundens kundekonto er kreditert.
- Rabattavsetningskontoen er debitert.

Til å godkjenne en varehandelshendelse av typen **engangsbeløp** velger du hendelsen på siden **Handelsrabattavtaler** og deretter, i kategorien **Beløp**, velg **Godkjenn**.

## <a name="settle-the-deduction-that-is-due-and-the-customer-short-pay-by-using-the-deduction-workbench"></a>Utligne fradrag som forfaller og kunden kort betaling ved hjelp av fradrag arbeidsbenk

De forventer seg faktura tilbake velge ofte kunder kort-lønn valgte fakturaene. Hvis du vil unngå problemer med betalingen avstemming senere registrerer clerk i Kunder disse kort betaler som fradrag når han eller hun registrerer de faktiske kundebetalingene. Deretter i arbeidsbenk fradrag, kan disse Kundefradrag lett utlignes mot krav beløpene som forfaller i firmaet.

Hvis du vil registrere en kundes korttidsbetaling i betalingsjournalen, velger du **Kunder** \> **Betalinger** \> **Betalingsjournal** og oppretter en ny betalingsjournal. I handlingsruten, velg deretter **Fradrag**. På siden **Fradrag** kan du opprette og spore beløpet som var betalt for lite.

Innkrevingsleder er nå ansvarlig for utligning av den åpne kreditnotatransaksjonen og korttidstransaksjonen mot hverandre i fradragsarbeidsområdet.

Hvis du vil behandle fradrag, velger du **Salg og markedsføring** \> **Handelsrabatter** \> **Fradrag** \> **Fradragsarbeidsområde**. Den øvre delen av siden inneholder linjer som representerer de korte betaler fra kunden. Den nedre delen av siden viser de åpne kredittransaksjonene for kunder. 

Hvis du vil utligne mot den åpne transaksjonen fradrag, Merk fradrag linjen, og deretter merker du linjen i kategorien åpne transaksjoner. Klikk Vedlikehold > Samsvar i handlingsruten.

Statusen for de opprinnelige kravene er nå satt til **Fullført**.

## <a name="analyze-the-effectiveness-of-the-promotion-and-fund-consumption"></a>Analysere effektiviteten for kampanjen og bruken av midlene

Hvis du vil ha en oversikt over viktig statistikk for programmets og fond bruk, du kan bruke flere rapporter og analytiske visninger som er tilgjengelige i behandling av handel rabatten.

På siden **Handelsrabattaktivitet** viser kategorien **Oversikt** primære detaljer for handelsrabattavtalen. De andre kategoriene viser flere opplysninger om de tilknyttede dokumentene, betalinger og andre hendelser som er knyttet til programmet.

Den **Sammendrag**-kategorien viser det totale antallet varer som er solgt under kampanjen, salgsbeløpet som er fakturert, og stykklisten tilbake og samlet summer som er betalt.

Kategorien **Kreditter for tilbakebetaling** inneholder detaljer om individuelle faktura tilbake som er kreditert til kunden.

Hvis du vil ha en mer analytisk oversikt over de ulike ytelsesmål for kampanjen, kan du bruke analysevisningen. For å gå til analysevisningen, klikk **Salg og markedsføring** \> **Handelsrabatter** \> **Handelsrabattavtaler**. Klikk **Analyse** i handlingsruten.  

Hvis du vil ha en mer analytisk oversikt over de ulike ytelsesmål for kampanjen, kan du bruke analysevisningen. For å gå til analysevisningen, klikk **Salg og markedsføring** \> **Handelsrabatter** \> **Handelsrabattavtaler**. Klikk **Analyse** i handlingsruten. 

