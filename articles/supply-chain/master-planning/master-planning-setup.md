---
title: Definer hovedplaner
description: Denne artikkelen beskriver diverse viktige strategier og parametere som brukes til å definere hovedplaner.
author: t-benebo
ms.date: 07/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2019-05-31
ms.dyn365.ops.version: AX 10.0.0
ms.openlocfilehash: 150e02916e056946016155d1b4969e99fbd47af5
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740664"
---
# <a name="set-up-master-plans"></a>Definer hovedplaner

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver diverse viktige strategier og parametere som brukes til å definere hovedplanlegging. Det omfatter en oversikt over plantypene som brukes i hovedplanlegging, og forklarer hvilken planstrategi du bør bruke, avhengig av forretningsbehovene dine. Det beskriver også de viktigste parameterne som påvirker planen, og forklarer hvordan disse parameterne påvirker de planlagte ordrene som foreslås.

## <a name="types-of-master-plans"></a>Typer hovedplaner

Hovedplanlegging har to typer planer: statisk og dynamisk. Hver type er utformet for en egen bruk. For å oppnå best mulig ytelse anbefaler vi at du bruker planen som passer for scenariet ditt.

### <a name="static-plan"></a>Statisk plan

Den statiske planen forblir uendret, uavhengig av endringer i forsyning og behov, til neste gang hovedplanleggingen kjøres.

Den statiske planen brukes til å godkjenne og autorisere ordrene som foreslås. Det er en driftsplan som ulike firmaansatte (for eksempel innkjøpere eller produksjonsplanleggere) kan basere beslutningene sine på og bruke til å utføre de daglige oppgavene og aktivitetene.

Den statiske planen støtter også ny generering. En helt ny optimalisert plan beregnes hver gang hovedplanlegging kjøres, og eksisterende ordrer som ikke er godkjent, slettes.

### <a name="dynamic-plan"></a>Dynamisk plan

Den dynamiske planen starter vanligvis som en kopi av den statiske planen, men kan oppdateres hver gang hoveddataene endres. Hvis dataene for eksempel endres, opprettes en ny salgsordre.

Den dynamiske planen brukes til adhocplanlegging. Den gjør at firmaet kan overvåke det endrede ordrenettverket og varetilgjengeligheten uten å forstyrre den statiske planen som andre personer bruker i arbeidsprosessene. Den brukes spesielt i sammenheng med leveringskapasitet (CTP). Den dynamiske planen er standardplanen når nettobehov åpnes fra ordresider (for eksempel sider i salgsordrer, bestillinger eller produksjonsordrer).

Den dynamiske planen bruker nettoendring. Den er derfor med på å garantere en raskere kjøretid.

## <a name="strategies-for-using-master-plans"></a>Strategier for bruk av hovedplaner

Du kan bruke én eller to planer i hovedplanlegging. Strategien du bruker, avhenger av forretningsbehovene dine.

### <a name="one-plan-strategy"></a>Enplansstrategi

Når det gjelder enplansstrategien, bruker du samme hovedplan for den statiske og dynamiske planen. Denne strategien brukes i produser-for-lager-scenarier, der du vanligvis ikke må simulere en plan som oppfyller en ordre.

Enplansstrategien brukes vanligvis i detaljhandels- og distribusjonsindustrier, eller der salgsleveringsdatoer bekreftes basert på serviceavtaler (SLA-er) eller leveringstider. Leveringsdatokontroll kan brukes uten CTP for planen.

Hvis du må foreta en simulering, kan planen kjøres på nytt for varene som krever simuleringen. De planlagte ordrene som ordresimuleringer produserer, blir vanligvis autorisert.

### <a name="two-plan-strategy"></a>Toplansstrategi

Når det gjelder toplansstrategien, bruker du en statisk plan og en annen dynamisk plan. Toplansstrategien brukes vanligvis i konfigurer-etter-ordre- og produksjon-etter-ordre-scenarier, der du må foreta salgsordresimuleringer og beregne nøyaktige leveringsdatoer for salgsordrer, med beregningene ikke kan påvirke daglige operasjoner. Disse simuleringene foretas alltid i den dynamiske planen. Toplansstrategien er for eksempel nyttig i bilindustrien og OEM-bransjer (opprinnelig utstyrsfabrikant).

Leveringsdatokontroll av CTP-typen kan brukes for toplansstrategien. Når CTP brukes, starter den kjøringen automatisk i den dynamiske planen.

### <a name="setting-up-the-plans"></a>Definere planene

Du kan opprette planer på **Hovedplaner**-siden (**Hovedplanlegging \> Oppsett \> Planer \> Hovedplaner**).

Du kan angi hvilke planer som skal brukes for den statiske og dynamiske planen, ved å fylle ut feltene **Gjeldende statisk hovedplan** og **Gjeldende dynamisk hovedplan** på siden **Hovedplanleggingsparametere** (**Hovedplanlegging \> Oppsett \> Hovedplanleggingsparametere**). Hvis du vil bruke enplansstrategien, velger du samme plan i feltene **Gjeldende statisk hovedplan** og **Gjeldende dynamisk hovedplan**.

## <a name="types-of-planning-methods"></a>Typer planleggingsmetoder

Du kan bruke tre beregningsmetoder til å kjøre hovedplanlegging: ny generering og nettoendring. Hver metode fører til en egen plan når den kjøres.

Du angir planleggingsmetoden i dialogboksen **Hovedplanleggingskjøring**. Du kan åpne denne dialogboksen ved å gå til **Hovedplanlegging \> Hovedplanlegging \> Kjør \> Hovedplanlegging** eller velge **Kjør** i arbeidsområdet **Hovedplanlegging**.

### <a name="regeneration"></a>Ny generering

Planleggingsmetoden for ny generering sletter eksisterende planlagte ordrer med mindre de er autorisert. Den genererer nye planlagte ordrer basert på alle behovene. Ny generering er den eneste planleggingsmetoden som er tilgjengelig for statiske planer.

- Endringer i forsyning blir vurdert. Disse endringene omfatter endringer i prognosen.
- Denne metoden tar hensyn til dekningskoden **Periode**.
- Denne metoden støtter produkterstatningsfunksjonaliteten (PI).

### <a name="net-change"></a>Netto endring

Planleggingsmetoden for nettoendring genererer planlagte ordrer for å dekke behovet som er opprettet eller endret siden forrige kjøring av hovedplanlegging. Endringer i forsyning blir ikke vurdert når denne metoden kjøres. Systemet tar ikke hensyn til nye forsyninger, og planlagte ordrer som ble opprettet tidligere, slettes ikke selv om de ikke lenger er nødvendige. Planleggingsmetoden for nettoendring kjører raskere enn metoden for ny generering. Den er bare tilgjengelig for dynamiske planer.

- Handlingsdatoer og terminer oppdateres for alle behov.
- Denne metoden tar ikke hensyn til dekningskoden **Periode**.
- Denne metoden oppfyller ikke prognosen, selv om den er valgt i planen.
- Denne metoden støtter ikke produkterstatningsfunksjonaliteten (PI).

### <a name="net-change-minimized"></a>Netto endring minimert

Planleggingsmetoden for netto endring minimert genererer planlagte ordrer for bare å dekke behovet som er opprettet eller endret siden forrige kjøring av hovedplanlegging. I motsetning til metoden for nettoendring oppdateres handlingsdatoer og fremtidige datoer for denne metoden bare for nye eller endrede behov. Denne planleggingsmetoden er bare tilgjengelig for dynamiske planer.

## <a name="types-of-scheduling-methods"></a>Typer planleggingsmetoder

I hurtigfanen **Generelt** på **Hovedplaner**-siden (**Hovedplanlegging \> Oppsett \> Planer \> Hovedplaner**) må du for hver plan velge planleggingsmetoden som skal brukes for produksjonsordrer. Du kan planlegge produksjonen på operasjonsnivået og jobbnivået.

### <a name="operations-scheduling"></a>Grovplanlegging

Du kan bruke grovplanlegging for å få et generelt estimat over produksjonsprosessen over tid. Grovplanlegging deler ikke operasjonene for produksjonsruten inn i jobber. Hvis du vil ha mer informasjon om grovplanlegging, kan du se [Grovplanlegging](/dynamics365/unified-operations/supply-chain/production-control/operations-scheduling).

### <a name="job-scheduling"></a>Finplanlegging

Finplanlegging er en mer detaljert planleggingsmetode der hver operasjon deles inn i individuelle oppgaver eller jobber. Finplanlegging omfatter informasjon om kapasitet. Den brukes vanligvis til å planlegge enkeltjobber på shop floor i en umiddelbar eller kortsiktig tidsramme. Hvis du vil ha mer informasjon om finplanlegging, kan du se [Finplanlegging](/dynamics365/unified-operations/supply-chain/production-control/job-scheduling).

## <a name="time-fences-in-days"></a>Horisonter i dager

For hver plan kan du velge hvor langt inn i fremtiden de ulike behovene og andre hensyn må beregnes ved hjelp av hovedplanlegging. Perioden kalles en *horisont*. For å få best mulig ytelse i hovedplanlegging anbefaler vi at du justerer de ulike horisontene slik at de dekker forretningsbehovene dine. Du kan finne horisontene for hver plan i hurtigfanen **Horisonter i dager** på **Hovedplaner**-siden (**Hovedplanlegging \> Oppsett \> Planer \> Hovedplaner**).

> [!NOTE]
> Horisontene angir hvor langt inn i fremtiden de ulike behovene og andre hensyn beregnes ved hjelp av hovedplanlegging. Horisontene som er valgt på denne siden, overstyrer horisontene som er definert i dekningsgruppen. Dette betyr at å angi ja for et horisontalternativ og definere dagene, overstyrer horisonten som er definert i dekningsgruppen. Når du angir Nei, blir horisonten definert i dekningsgruppen. Hvis du ikke ønsker eller ikke trenger å bruke et alternativ (du vil for eksempel ikke bruke handlingsmeldinger), angir du **Ja** og setter deretter horisonten til **0** (null) dager.

### <a name="coverage"></a>Dekning

Dekningshorisonten representerer planleggingsperioden, eller hvor langt frem i tid behovet skal tas med. Den angir med andre ord planleggingshorisonten.

Når du setter alternativet **Dekning** til **Ja**, kan du overstyre dekningshorisonten som defineres for varen under hovedplanlegging. I dette tilfellet angir du hvor mange dager hovedplanleggingsberegningen skal dekke behov. Dekningshorisonten beregnes fremover fra og med gjeldende dato. Krav som oppstår før gjeldende dato, blir alltid behandlet.

> [!NOTE]
> For å få best mulig ytelse i hovedplanlegging anbefaler vi at du justerer dekningshorisonten etter planleggingshorisonten.

### <a name="freeze"></a>Låsing

Låsningshorisont representerer perioden der eksisterende planlagte ordrer ikke endres når en ny hovedplan kjøres. De planlagte ordrene er låst, og det blir ikke foreslått noen nye planlagte ordrer.

Når du setter alternativet **Lås** til **Ja**, kan du overstyre låsningshorisonten som defineres for varen under hovedplanlegging. I dette tilfellet angir du antall dager planleggingsaktiviteten skal låses. Husk at ingen nye planlagte ordrer genereres i denne perioden, og eksisterende planlagte ordrer kan ikke endres.

### <a name="firming"></a>Autorisasjon

Autorisasjonshorisonten angir horisonten der planlagte ordrer automatisk konverteres til produksjonsordrer og bestillinger. Denne prosessen kalles også *automatisk autorisasjon av planlagte ordrer*.

Når du setter alternativet **Autorisasjon** til **Ja**, kan du overstyre autorisasjonshorisonten som defineres for varen under hovedplanlegging. I dette tilfellet angir du antall dager bestillingsforslag og planlagte produksjonsordrer skal autoriseres automatisk. Autorisasjonshorisonten beregnes fremover fra og med hovedplanleggingsdatoen. Automatisk autorisasjon av et bestillingsforslag kan bare skje hvis varen er knyttet til en leverandør.

### <a name="forecast-plan"></a>Prognoseplan

Prognoseplanhorisonten angir hvor langt inn i fremtiden hovedplanleggingen oppretter planlagte ordrer for varer som har prognoseberegnet behov.

Når du setter alternativet **Prognoseplan** til **Ja**, kan du overstyre prognoseplanhorisonten som defineres for varen under hovedplanlegging. I dette tilfellet angir du antall dager som salgsprognosen fra prognoseplanen skal inkluderes i hovedplanlegging.

### <a name="capacity"></a>Kapasitet

Kapasitetshorisonten angir hvor langt inn i fremtiden systemet vurderer maksimumskapasiteten til ressursene når ordrer planlegges. Planen planlegger med andre ord produksjonsordrene ved å bruke produksjonsruten for varene, og den vurderer produksjonsrutens ressurser og maksimumskapasiteten til hver ressurs.

Når du setter alternativet **Kapasitet** til **Ja**, kan du overstyre kapasitetshorisonten som defineres for varen under hovedplanlegging. I dette tilfellet angir du antall dager som kapasitet skal planlegges for planlagte produksjonsordrer. Hovedplanlegging bruker varens aktive produksjonsrute og planlegger bakover fra og med behovsdatoen. Hvis behovsdatoen for en planlagt produksjonsordre er utenfor kapasitetshorisonten, bestemmes leveringstiden på grunnlag av varens leveringstid. Kapasitetshorisonten beregnes fremover fra og med gjeldende dato.

### <a name="action-message"></a>Handlingsmelding

Handlingsmeldinger foreslår endringer som kan gjøres i den eksisterende forsyningsordren for å optimalisere forsyningsplanen. De kan for eksempel anbefale at du fremskynder eller utsetter ordrer, eller at du øker eller reduserer ordreantallet.

Når du setter alternativet **Handlingsmelding** til **Ja**, kan du overstyre handlingsmeldingshorisonten som defineres for varen under hovedplanlegging. I dette tilfellet angir du antall dager som hovedplanleggingen skal generere handlingsmeldinger for krav. Handlingsmeldingshorisonten beregnes fremover fra og med gjeldende dato.

Hvis du vil ha mer informasjon om handlingsmeldinger, kan du se [Handlingsmeldinger](/dynamics365/unified-operations/supply-chain/master-planning/action-messages).

> [!NOTE]
> Beregningen av handlingsmeldinger forårsaker en lengre kjøretid for hovedplanlegging. Hvis handlingsmeldinger ikke analyseres og brukes regelmessig (daglig, ukentlig og så videre), bør du vurdere å deaktivere beregningen under hovedplanleggingskjøringen. Hvis du vil deaktivere beregningen, kan du sette **Handlingsmelding**-horisonten til **0** (null) på **Hovedplaner**-siden for hovedplanen du kjører. Kontroller også at innstillingen **Handlingsmelding** er deaktivert for alle dekningsgruppene.

### <a name="calculated-delays"></a>Beregnede forsinkelser

Du kan angi hvor langt inn i fremtiden mulige forsinkelser i planlagte ordrer skal registreres og rapporteres. På denne måten kan du planlegge mulige (forsinkede) leveringsdatoer.

Hvis en planlagt ordre ikke kan fullføres på den forespurte datoen, planlegges den for den tidligste fullføringsdatoen for en transaksjon, basert på leveringstider og tilgjengelighet av materiale og kapasitet.

### <a name="approved-requisitions-time-fence"></a>Horisont for godkjente rekvisisjoner

Du kan definere hovedplanlegging for å opprette planlagte ordrer for rekvisisjonsbehov. Sett alternativet **Inkluder rekvisisjoner** til **Ja** i hurtigfanen **Generelt** på **Hovedplaner**-siden. Når formålet med en godkjent rekvisisjon er etterfylling, oppretter hovedplanleggingen deretter en tilsvarende planlagt ordre automatisk for å oppfylle den. Etterfyllingsmetoden fastsettes av forsyningspolicyene som er definert for varene i organisasjonen. Når etterfyllingsrekvisisjon er opprettet og godkjent, trengs det ingen flere brukerhandlinger.

Hvis du setter alternativet **Godkjente rekvisisjoner - horisont** til **Ja** i hurtigfanen **Horisonter i dager**, kan du overstyre horisonten for godkjente rekvisisjoner som defineres for varen under hovedplanlegging. I dette tilfellet angir du antall dager i fortiden som behov fra godkjente rekvisisjoner som har etterfyllingsformålet, skal tas med i hovedplanlegging. Du kan for eksempel angi at bare ikke-oppfylt, forfalt behov fra godkjente rekvisisjoner som ble opprettet de siste 10 dagene, skal tas med i betraktningen og planlegges.

### <a name="sequencing"></a>Sekvensering

Sekvensering gjør at planlagte ordrer kan ordnes basert på sekvenseringsattributter som er knyttet til det ferdige produktet. Den brukes ofte til å klargjøre produksjonsordrer for emballering. Den kan for eksempel brukes til å pakke bokser i en bestemt rekkefølge basert på farge og størrelse.

Hvis du setter alternativet **Sekvensering** til **Ja**, kan du angi hvor langt inn i fremtiden operasjonene eller jobbene skal sekvenseres. Husk at jo lenger horisonten er, desto lengre tid tar det for hovedplanlegging å kjøre.

### <a name="calculated-delays"></a>Beregnede forsinkelser

Forsinkelsesalternativer er med på å garantere at ordrene har mulige planlagte datoer. Følgende alternativer er tilgjengelige i hurtigfanen **Beregnede forsinkelser** på **Hovedplaner**-siden:

- **Kontroller at de planlagte ordrene ikke opprettes før kjøringsdatoen for hovedplanlegging** – Sett dette alternativet til **Ja** for bidra til å garantere at ordrer ikke kan planlegges for datoer i fortiden.
- **Legg til den beregnede forsinkelsen i behovsdatoen** (under **Bestillingsforslag**) – Sett dette alternativet til **Ja** for å legge til den beregnede forsinkelsen i behovene.
- **Legg til den beregnede forsinkelsen i behovsdatoen** (under **Planlagte produksjonsordrer**) – Sett dette alternativet til **Ja** for å legge til den beregnede forsinkelsen i behovene.
- **Legg til den beregnede forsinkelsen i behovsdatoen** (under **Overføringsforslag**) – Sett dette alternativet til **Ja** for å legge til den beregnede forsinkelsen i behovene.
- **Legg til den beregnede forsinkelsen i behovsdatoen** (under **Planlagt Kanban**) – Sett dette alternativet til **Ja** for å legge til den beregnede forsinkelsen i behovene.

Når du setter alternativene **Legg til den beregnede forsinkelsen i behovsdatoen** til **Ja** for å legge til forsinkelsene i behovene, vurderer systemet kapasiteten til ressursene og oppretter mulige planlagte ordrer. Ny beregning av datoene for planlagt ordre øker kjøretiden for hovedplanlegging. Hvis du ikke trenger å bruke forsinkelsene, angir du derfor **Nei** for alternativene.

## <a name="positive-and-negative-days"></a>Positive og negative dager

Positive og negative dager påvirker hvordan hovedplanlegging foreslår planlagte ordrer og handlinger. Positive og negative dager angis på varedekningsgruppen for varen. Du kan definere de ulike dekningsgruppene og sette parameterne for dem på **Dekningsgrupper**-siden (**Hovedplanlegging \> Oppsett \> Dekning \> Dekningsgrupper**).

### <a name="positive-days"></a>Positive dager

Positive dager angir hvor langt inn i fremtiden hovedplanleggingen vurderer gjeldende beholdning eller mottak for å oppfylle et fremtidig behov. Hvis de positive dagene for eksempel settes til **100**, kan gjeldende beholdning brukes til å oppfylle behovet de neste 100 dagene. Hvis en ordre er 150 dager fra gjeldende dato, oppretter hovedplanleggingen en planlagt ordre for å oppfylle dette behovet, selv om lagerbeholdningen for varen kan oppfylle ordren. Når det gjelder varer som flyttes raskt og har kort leveringstid, vil du kanskje ikke bruke lagerbeholdningen for en ordre som er aktuell langt inn i fremtiden. I dette tilfellet forsvinner den gjeldende lagerbeholdningen raskt, og flere ordrer kan bli opprettet i fremtiden for å oppfylle et fremtidig behov i tide, som er mulig på grunn av den korte leveringstiden for varen.

De positive dagene påvirker også handlingsmeldingene. Systemet kan for eksempel anbefale at du øker et bestillingsforslag, slik at det omfatter et behov som er innenfor antall positive dager i fremtiden. Hvis de positive dagene settes til **100**, og hvis det er behov for en vare om 30 dager fra gjeldende dato, oppretter systemet en planlagt ordre for å oppfylle dette behovet. Hvis det er behov for den samme varen om 90 dager fra gjeldende dato, anbefaler systemet at du øker antallet for ordren om 30 dager fra den gjeldende datoen, slik at ordren også dekker behovet om 90 dager. Hvis det imidlertid er behov for varen om 150 dager fra gjeldende dato, anbefaler ikke systemet at du øker antallet i ordren som allerede var planlagt. Det blir i stedet opprettet en ny planlagt ordre.

Som regel settes positive dager til et tall som er mellom den lengste leveringstiden for varene og dekningshorisonten. Det anbefales at du tilordner varer som fremskaffes eller produseres jevnlig, til en dekningsgruppe der de positive dagene er lik varens leveringstid.

### <a name="negative-days"></a>Negative dager

Negative dager angir hvor sent varemottak tillates. De representerer hvor mange dager du er villig til å vente før du bestiller ny etterfylling, når du har en negativ beholdning eller ikke har en tilstrekkelig beholdning. Negative dager besvarer følgende spørsmål: Skal vi opprette en ny bestilling for varen, eller skal vi bruke et eksisterende innkjøp, selv om vi vet at varen kommer til å bli forsinket?

La oss si at du har en salgsordre for en vare om 15 dager fra gjeldende dato. Du har også en bestilling for den samme varen. Denne bestillingen kommer til å bli mottatt om 20 dager fra den gjeldende datoen. Vil du at systemet skal opprette en bestilling for denne salgsordren, eller vil du bruke den eksisterende ordren selv om du ikke kan oppfylle salgsordren i tide? Hvis de negative dagene er satt til mindre enn **5** for å angi at varen kan bli maksimalt fem dager forsinket, oppretter systemet et nytt bestillingsforslag for å oppfylle salgsordren. Hvis de negative dagene er satt til mer enn **5**, bruker systemet den eksisterende ordren for varen.

De negative dagene påvirker også ytelsen til hovedplanleggingen. Hvis de negative dagene settes til et høyt tall, genereres det mange handlingsmeldinger.

Det anbefales at du setter negative dager til et tall som er mindre enn leveringstiden for varen.

### <a name="dynamic-negative-days"></a>Dynamiske negative dager

Dynamiske negative dager tar hensyn til varens leveringstid og de negative dagene du har angitt. Systemet oppretter et nytt bestillingsforslag basert på horisonten for negative dager som beregnes ved hjelp av følgende formel:

Leveringstid + Negative dager + Gjeldende dato - Behovsdato

Systemet bruker bare de planlagte forsyningsordrene som er innenfor denne horisonten, og det oppretter en ny planlagt ordre utenfor den. Fordelen med dynamiske negative dager er at de tar med den individuelle produktleveringstiden, for å bruke eksisterende ordrer på nytt og unngå å opprette nye planlagte ordrer som ender opp med en senere dag på grunn av forsinkelser forårsaket av leveringstiden. 

Hvis du vil ha mer informasjon, kan du se [Negative dager og dynamiske negative dager](/dynamics365/unified-operations/supply-chain/master-planning/more-about-dynamic-negative-days).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]