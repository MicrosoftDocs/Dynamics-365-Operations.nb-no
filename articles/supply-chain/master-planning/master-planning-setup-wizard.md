---
title: Veiviser for oppsett for hovedplanlegging (inneholder video)
description: Dette emnet beskriver hvordan du kjører installasjonsveiviseren for hovedplanlegging for å definere hovedplanlegging.
author: ChristianRytt
ms.date: 10/21/2019
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
ms.openlocfilehash: 453184a3fed567b3a09e5e45e7f904bcf855dd6d
ms.sourcegitcommit: ef0dd4245fc499907ffe00e2a32f59a6cd96e45d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/18/2021
ms.locfileid: "7937639"
---
# <a name="master-planning-setup-wizard"></a>Veiviser for oppsett for hovedplanlegging

[!include [banner](../includes/banner.md)]

Dette emnet inneholder en veiledning for **Veiviser for oppsett for hovedplanlegging**. Den forklarer hvordan parameterforslag beregnes, og inneholder også eksempler som viser hvordan ulike selskaper konfigurerer hovedplanlegging, basert på virksomhetens behov.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3YnSB]

Videoen [Veiviser for oppsett for hovedplanlegging Dynamics 365 Supply Chain Management](https://youtu.be/c-e6n-8rZb4) (vises over) er inkludert i [Finance and Operations-spillelisten](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) som er tilgjengelig på YouTube.


## <a name="specific-requirements-of-your-company"></a>Spesifikke krav for firmaet

Den første siden i veiviseren spør om de spesifikke kravene i firmaet. Svarene på disse spørsmålene trenger ikke å være nøyaktige, men du bør kunne gi en grov tilnærming til antall varer og planlagte bestillinger som det vil være for den juridiske enheten. Svarene dine brukes til å konfigurere parametere som gjelder for den juridiske enheten, ikke bare til den overordnede planen du har valgt. Delene nedenfor beskriver parameterne som beregnes, og formlene som brukes.

### <a name="number-of-threads"></a>Antall tråder

- **Hvis du produserer noen av varene:** Antall tråder = antall planlagte ordrer ÷ 1 000
- **Hvis du ikke produserer noen av varene:** Antall tråder = antall varer ÷ 1 000

Hvis antall tråder som er beregnet overskrider 75 prosent av det tilgjengelige antallet tråder, er det avkortet til 75 prosent av antall tråder som er tilgjengelig for hver kunde. (Antall tilgjengelige tråder vil bli fastsatt for hver kunde.)

For mer informasjon, se [Antall tråder](/dynamics365/unified-operations/supply-chain/master-planning/master-planning-performance#number-of-threads).

### <a name="bundle-size"></a>Buntstørrelse

Buntstørrelsen vil bli satt til **1**. Denne verdien er ofte den beste verdien, fordi den bidrar til å forbedre ytelsen til hovedplanlegging.

Hvis du vil ha mer informasjon, kan du se [Antall oppgaver i oppgavebunt for hjelper](/dynamics365/unified-operations/supply-chain/master-planning/master-planning-performance#number-of-tasks-in-helper-task-bundle).

### <a name="firming-bundle-size"></a>Størrelse på autoriseringsbunt

- **Hvis du produserer noen av varene:** Størrelsen på autoriseringsbunten vil bli satt til den største av disse to verdiene: **10** og buntberegningen.
- **Hvis du ikke produserer noen av varene:** Størrelsen på autoriseringsbunten vil bli satt til den største av disse to verdiene: **50** og buntberegningen.

Buntberegning = (antall planlagte bestillinger × (autorisasjonshorisont ÷ dekningshorisont) ÷ antall tråder) ÷ 10

### <a name="cache-size"></a>Hurtigbufferstørrelse

Bufferstørrelsen vil bli satt til **Maksimum**. Denne verdien er ofte den beste verdien, fordi den bidrar til å forbedre ytelsen til hovedplanlegging.

Hvis du vil ha mer informasjon, kan du se [Tildele tid til jobber i en jobbunt](/dynamics365/unified-operations/supply-chain/production-control/allocate-time-jobs-job-bundle).

### <a name="manufacturing-setup"></a>Produksjonsoppsett

Hvis du produserer varer, vises en **Produksjonsoppsett**-side senere i veiviseren.

## <a name="scope-of-the-current-plan"></a>Omfang for aktuell plan

På siden **Omfang for aktuell plan** i veiviseren svarer du på spørsmål som er knyttet til hvor langt i fremtiden ulike krav vil bli vurdert og beregnet i hovedplanlegging. Hvert spørsmål spør om du vil bruke en funksjon og hvordan du vil konfigurere den.

Funksjonen for prognoseplan i veiviseren spør for eksempel om du vil bruke en proprognoseplan i hovedplanleggingen, slik at planlagte bestillinger vil bli foreslått for å oppfylle det forventede behovet.

Følgende alternativer er tilgjengelige:

- **Nei** – hovedplanlegging foreslår ikke planlagte bestillinger for å oppfylle en prognose. I fanen **Horisonter** på siden **Hovedplaner** (**Hovedplanlegging \> Oppsett \> Planer \> Hovedplaner**) setter veiviseren alternativet **Prognoseplan (horisont)** til **Ja** og antall dager til **0** (null). Dette oppsettet vil overstyre tidshorisonten som er angitt i dekningsgruppen. Fordi antall dager er satt til **0** (null), vil ikke funksjonen bli brukt.
- **Ja, som definert i denne hovedplanen** – et felt blir tilgjengelig, der du kan angi antall dager hovedplanleggingen skal foreslå planlagte bestillinger for å oppfylle prognosebehovet. Veiviaseren setter alternativet **Prognoseplan (horisont)** til **Ja** og antall dager til det antallet som er angitt i feltet **Prognoseplan** i fanen **Horisonter** på **Hovedplaner**-siden. Dette oppsettet vil overstyre verdiene som er angitt i dekningsgruppene.
- **Ja, som definert i dekningen** – veiviseren vil sette alternativet **Prognoseplan (horisont)** til **Nei**. Tidshorisontene som er angitt i dekningsgruppen, vil bli brukt til å angi hvor lenge du vil planlegge for prognosen.

De gjenstående spørsmålene på denne siden og svarene følger etter samme skjema:

- **Nei** – alternativet **Prognoseplan (horisont)** vil bli satt til **Ja**, og antall dager blir satt til **0** (null).
- **Ja, som definert i denne hovedplanen** – alternativet **Prognoseplan (horisont)** settes til **Ja**. Antallet dager du angir, vil bli brukt, og vil overstyre verdiene som er angitt i dekningsgruppene.
- **Ja, som definert i dekningsgruppen** – alternativet **Prognoseplan (horisont)** settes til **Nei**.

Hvis du vil ha mer informasjon, se [Finplanlegging](/dynamics365/unified-operations/supply-chain/production-control/job-scheduling).

## <a name="scheduling-options"></a>Planleggingsalternativer

Siden **Planleggingsalternativer** vises bare hvis du svarte **Ja** på spørsmålet om du produserer noen av de planlagte varene, på den første siden i veiviseren.

Svaret på det første spørsmålet på denne siden (om du må planlegge operasjoner delt inn i enkeltjobber) bestemmer planleggingsmetoden i fanen **Generelt** på **Hovedplaner**-siden.

- **Ja** – jobbplanlegging vil bli brukt.
- **Nei** – grovplanlegging vil bli brukt.

Hvis du vil ha mer informasjon, kan du se [Grovplanlegging](/dynamics365/unified-operations/supply-chain/production-control/operations-scheduling) og [Finplanlegging](/dynamics365/unified-operations/supply-chain/production-control/job-scheduling).

## <a name="updates-of-demand-and-supply"></a>Oppdatering av behov og forsyning

Spørsmålene på siden **Oppdatering av behov og forsyning** er knyttet til autorisasjon, handlingsmeldinger og forsinkelser.

Oppsettet av hovedplanleggingen blir oppdatert basert på svarene, i henhold til det samme skjemaet som er beskrevet i den forrige delen:

- **Nei** – alternativet **Horisont** på **Hovedplaner**-siden vil bli satt til **Ja**, og antall dager blir satt til **0** (null).
- **Ja, som definert i denne hovedplanen** – alternativet **Horisont** settes til **Ja**. Antallet dager du angir, vil bli brukt, og vil overstyre verdiene som er angitt i dekningsgruppene.
- **Ja, som definert i dekningsgruppen** – alternativet **Horisont** settes til **Nei**.

Når det gjelder beregnede forsinkelser, vil svarene på spørsmålene i vei viseren oppdatere de tilsvarende parameterne i fanen **Beregnede forsinkelser** på siden **Hovedplaner**.

## <a name="summary-of-your-changes"></a>Oversikt over endringene

Den siste siden i veiviseren viser endringene som anbefales på grunnlag av dine svar. Den viser både verdien i oppsettet (**Gjeldende oppsett**) og verdien som veiviseren anbefaler (**Ny konfigurasjon**).

Du kan også endre parameterne i den nye konfigurasjonen. Parameterne er delt inn i parametere som gjelder for den juridiske enheten og parametere som bare gjelder hovedplanen du har valgt. Hvis du vil vise alle oppsettparameterne som kan endres ved hjelp av veiviseren, velger du **Vis alle parametere** nederst på siden. Du kan deretter endre parameterne.

Til slutt brukes den nye konfigurasjonen når du velger **Fullfør**. Hvis du velger **Avbryt**, brukes ingen av endringene.

## <a name="examples"></a>Eksempler

Denne delen beskriver oppsettet av to oppdiktede firmaer for å vise hvordan oppsettet kan endres i henhold til behovene for hver enkelt virksomhet.

### <a name="example-1-contoso-manufacturer"></a>Eksempel 1: Contoso Manufacturer

Contoso Manufacturer er et produksjonsfirma som produserer høyttalere. Den kjøper de ulike råvarene og-komponentene som brukes for de endelige høyttalerne fra ulike leverandører. Her er noen av egenskapene til forsyningen og produksjonen av den:

- De endelige varene som firmaet produserer, har en stykklistestruktur.
- Alle endelige varer og komponenter planlegges ved hjelp av hovedplanlegging. Manuell planlegging er ikke utført.
- En operasjonsrute er definert for produksjonen av hver endelige vare.
- Produksjonsanlegget produserer de endelige varene. Den har et definert antall mølle- og boremaskiner som brukes til å behandle komponentene. De forskjellige komponentene må behandles av disse maskinene.
- Det finnes mange leverandører. Den gjennomsnittlige leveringstiden for varer er én uke. En gruppe varer fra samme leverandør får en leveringstid på sju uker.

I veiviseren angis følgende verdier for Contoso Manufacturer:

- **Dekning:**

    - **Spørsmål:** "Vil du angi antall dager i planleggingshorisonten?"
    - **Svar:** "Ja, slik det er definert i dekningsgruppene."

    Fordi leveringstiden for varer er svært forskjellige, trenger Contoso ikke å planlegge alle varene for den samme perioden i fremtiden. Dekningsgrupper for varene opprettes. Varer som har en lignende leveringstid, er tilordnet til samme deknings gruppe. Planleggingshorisonten for hver dekningsgruppe (det vil si dekningshorisonten) er ca. leveringstiden pluss en margin på én uke. Hovedplanlegging sørger deretter for at varene planlegges på forhånd, basert på leveringstiden.

    Det blir derfor opprettet to dekningsgrupper for dette eksemplet. Én dekningsgruppe vil ha en dekningshorisont på to uker, og den andre vil ha en dekningshorisont på åtte uker.

    Hvis **Ja, som definert i denne hovedplanen** er valgt som svar, må antall dager som angis, overskride den lengste leveringstiden for alle varene. Fordi mange varer ikke må planlegges så langt på forhånd, vil mange planlagte bestillinger beregnes, men aldri brukes. Kjøretiden for hovedplanleggingen kommer derfor til å økes.

- **Planlegging:**

    - **Spørsmål:** "Må du planlegge operasjoner delt inn i enkeltjobber?"
    - **Svar:** "Ja."

    Contoso Manufacturing må planlegge de enkelte jobbene som vil bli utført på gulvet. Derfor vil det bruke finplanlegging.

- **Kapasitet:**

    - **Spørsmål:** "Ønsker du å planlegge ved å bruke kapasiteten til ressursene?"
    - **Svar:** "Ja, som definert i denne hovedplanen." **10 dager** angis.

    Antallet mølle- og boremaskiner er begrenset. Produksjonsplanlegging må ta denne begrensningen i betraktning, og ordne jobbene i tid i henhold til kapasiteten i ressursene. Med andre ord planlegges jobbene som skal planlegges på nytt, basert på begrensningene til ressursene. Planlegging vil bruke leveringstiden i tillegg til perioden som er definert. (Planlagte produksjonsordrer kan overlappe hverandre.) Fordi produksjonsleveringstiden for varene er sju dager, vurderes kapasiteten til ressursene for hovedplanleggingen i løpet av 10 dager.

- **Sekvensering:**

    - **Spørsmål:** "Ønsker du å sekvensiere planlagte bestillinger ved hjelp av produktets sekvensverdier?"
    - **Svar:** "Ja, slik det er definert i dekningsgruppene."

    En rute er definert for produksjonen av hver endelige vare. Derfor vil hovedplanleggingen planlegge ordrer i tid i henhold til de definerte rutene.

- **Nedbryting:**

    - **Spørsmål:** "Ønsker du å planlegge bestillinger for alle varene i en stykkliste (planlegge for de overordnede og alle de underordnede varene)?"
    - **Svar:** "Ja, slik det er definert i dekningsgruppene."

    Alle varene som brukes for produksjonen, må være planlagt. Fordi varene har svært forskjellige leveringstider, vil hovedplanlegging ha bedre ytelse ved bruk av dekningsgruppene. På nytt kan en margin på én uke angis, og nedbryting kan utføres samtidig som dekningen.

### <a name="example-2-contoso-retailer"></a>Eksempel 2: Contoso Retailer

Contoso Retailer er et distribusjonsfirma i motebransjen. Den bruker hovedplanlegging til å beregne når bestillinger skal plasseres, basert på prognoser for salg. Her er noen av egenskapene:

- Contoso Retailer bruker en behovsprognose til å forutsi salg. Bestillinger vil bli planlagt i henhold til prognosen.
- Butikker bruker rekvisisjoner for etterfylling.
- Leveringstiden fra hovedlageret til hver butikk er omtrent to uker for alle varer.

I veiviseren angis følgende verdier for Contoso Retailer:

- **Behovsprognose:**

    - **Spørsmål:** "Ønsker du å bruke en prognoseplan i hovedplanlegging slik at planlagte bestillinger blir foreslått for å oppfylle det forventede behovet?"
    - **Svar:** "Ja, som definert i denne hovedplanen."

    Contoso har inkludert en behovsprognose for å forutsi salget. Hovedplanlegging må derfor anbefale planlagte bestillinger for å fullføre prognosen.

- **Autorisasjon:**

    - **Spørsmål:** "Ønsker du at hovedplanlegging automatisk skal autorisere planlagte bestillinger til ordredokumenter, for eksempel produksjonsordrer eller bestillinger?"
    - **Svar:** "Ja, som definert i denne hovedplanen." **1 dag** angis.

    Fordi Contoso Retailer vil opprette bestillinger direkte fra de planlagte bestillingene, er det nyttig hvis de planlagte bestillingene automatisk blir autorisert. Fordi selskapet kjører hovedplanlegging hver dag, vil en oppstrammende horisont på én dag automatisk autorisere alle ordrene som kreves for neste dag.

- **Godkjente rekvisisjoner:**

    - **Spørsmål:** "Ønsker du å ta med etterspørsel fra godkjente rekvisisjoner til å etterfylle detaljhandelbutikker?"
    - **Svar:** "Ja, som definert i denne hovedplanen." **1 dag** angis.

    Contoso bruker de godkjente rekvisisjonene fra sine butikker til å opprette bestillingsforslag for å etterfylle disse butikkene. Fordi hovedplanlegging kjøres hver dag, blir rekvisisjonen fra den siste dagen inkludert i planleggingen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]