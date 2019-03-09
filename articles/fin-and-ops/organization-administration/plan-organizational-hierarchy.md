---
title: Planlegge organisasjonshierarkiet
description: Før du setter opp organisasjoner og organisasjonshierarkier, må du sørge for at du forstår hvordan du best kan modellere virksomheten din.
author: sericks007
manager: AnnBe
ms.date: 08/28/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: OMHierarchyManager, OMLegalEntity, OMOperatingUnit
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 17404
ms.assetid: babde0c6-bb5d-45ae-95ca-2af75a0ea292
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 633d85333a510cec9cee2721e6e2330a47b6c78c
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "331995"
---
# <a name="plan-your-organizational-hierarchy"></a>Planlegge organisasjonshierarkiet

[!include [banner](../includes/banner.md)]

Før du definerer organisasjoner og organisasjonshierarkier i Microsoft Dynamics 365 for Finance and Operations, må du passe på å planlegge hvordan virksomheten skal modelleres. Organisasjonsmodellen har en betydelig innvirkning på implementeringen av Finance and Operations og på forretningsprosesser.

Organisasjonshierarkier representerer relasjonene mellom organisasjonene som utgjør en virksomhet. Derfor er strukturen til firmaet den viktigste vurderingen når du utformer organisasjoner. Vi anbefaler at du definerer organisasjonsstrukturer basert på tilbakemelding fra ledere og overordnede prosjektledere fra funksjonsområder, for eksempel økonomi og regnskap, personale, operasjoner, innkjøp og salg og markedsføring.

Når du planlegger hierarkier, er det også viktig å vurdere relasjonen mellom organisasjonshierarkiet og finansdimensjonene. Du kan definere flere organisasjonshierarkier som representerer ulike visninger av virksomheten. Når du bruker finansdimensjoner, kan du opprette rapporter basert på disse visningene. Arbeid med Microsoft Dynamics 365 for Finance and Operations-partneren for å opprette hierarkier som dekker behovene for både organisatorisk og lovbestemt rapportering.

> [!NOTE]
> Selv om du kan bruke finansdimensjoner til å representere juridiske personer uten å skape juridiske personer i Finance and Operations, er finansdimensjoner ikke utformet for å løse de juridiske enheters operasjonelle behov eller forretningsbehov. Funksjonen internenhetsregnskap i Finance and Operations er utviklet for bare å håndtere regnskapsoppføringene som opprettes av hver transaksjon.

> [!IMPORTANT]
> Du bør ikke bestemme hvordan du skal modellere organisasjoner kun basert på informasjonen i denne artikkelen. Denne dokumentasjonen er en veiledning. Du kan arbeide med Finance and Operations-partneren for å få mer hjelp. Finance and Operations-partneren har fått erfaring i ulike bransjer og på tvers av kundebasen.

## <a name="decide-whether-to-model-internal-organizations-as-legal-entities-or-operating-units"></a>Bestemme om du vil modellere interne organisasjoner som juridiske enheter eller driftsenheter

Du må ha minst én juridisk enhet for å representere firmaet i Finance and Operations. En juridisk enhet kan inngå juridiske kontrakter og er påkrevd for å klargjøre regnskapsoppgjør som rapporterer om prestasjonen.

I Finance and Operations kan juridiske enheter brukes til transaksjonsforretninger eller konsolidering. Dette betyr at en juridisk enhet i Finance and Operations ikke nødvendigvis representerer en virkelig enhet i firmaet. Et firma som deltar i transaksjoner, kan for eksempel eie underordnede juridiske enheter. I dette scenariet kreves det en juridisk enhet for transaksjoner, og det kreves en virtuell juridisk enhet for å konsolidere resultatene og saldoene for de underordnede juridiske enhetene.

Interne organisasjoner i bedriften, for eksempel regionale kontorer, kan representeres som juridiske tilleggsenheter eller driftsenheter for den primære juridiske enheten. En driftsenhet er ikke nødvendig for å være en organisasjon i juridisk forstand. Driftsenheter brukes for å styre økonomiske ressurser og driftsprosesser i virksomheten. Avdelinger og kostsentre er for eksempel driftsenheter.

Noen funksjoner i Finance and Operations fungerer ulikt avhengig av om organisasjonen er en juridisk enhet eller en driftsenhet. Vurder nøye funksjonaliteten beskrevet nedenfor når du bestemmer deg.

### <a name="master-data"></a>Hoveddata

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Hvis organisasjonen er modellert som en juridisk enhet

Noen hoveddata, for eksempel kunder, betalingsbetingelser, skattemyndighetere og områdespesifikk lagerbestilling, må defineres for hver juridiske enhet. Noen hoveddata, for eksempel brukere, produkter og de fleste personaldata, deles av alle juridiske enheter.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Hvis organisasjonen er modellert som en driftsenhet

Hoveddata deles mellom driftsenheter.

### <a name="module-parameters"></a>Modulparametere

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Hvis organisasjonen er modellert som en juridisk enhet

Parametere for moduler, for eksempel kundeparametere, leverandørparametere og kontant- og bankparametere, må angis per juridisk enhet. Siden moduloppsettet for juridiske enheter er separat, kan hvert datterselskap overholde lokale lovpålagte krav og forretningspraksis. En juridisk enhet for profesjonelle tjenester og en juridisk enhet for produksjon kan for eksempel ha forskjellige modulparametere, selv om de rapporterer til det samme overordnede firmaet.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Hvis organisasjonen er modellert som en driftsenhet

Modulparametere deles mellom driftsenheter.

### <a name="data-security"></a>Datasikkerhet

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Hvis organisasjonen er modellert som en juridisk enhet

De fleste dataene sikres automatisk av firma-IDen. En firma-ID er en unik ID for dataene som er tilknyttet en juridisk enhet. Et firma kan bare tilknyttes én juridisk enhet, og en juridisk enhet kan bare tilknyttes ett firma. Brukere har bare tilgang til data for firmaer som de har tilgang til. Du trenger ikke å tilpasse Finance and Operations for å sikre data etter firma-ID.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Hvis organisasjonen er modellert som en driftsenhet

Data kan sikres per driftsenhet ved å opprette tilpassede datasikkerhetspolicyer. Datasikkerhetspolicyer brukes til å begrense tilgangen til data. La oss for eksempel si at en bruker bare kan opprette bestillinger i en bestemt driftsenhet. Du kan opprette datasikkerhetspolicyer slik at brukerne ikke får tilgang til bestillingsdata fra en annen driftsenhet. Antall transaksjoner og sikkerhetspolicyer kan påvirke ytelsen. Ta hensyn til ytelsen når du utformer sikkerhetspolicyer.

### <a name="ledgers"></a>Finanskontoer

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Hvis organisasjonen er modellert som en juridisk enhet

Hver juridiske enhet krever en hovedbok som inneholder en kontoplan, regnskapsvaluta, rapporteringsvaluta og regnskapskalender. En balanse kan bare opprettes for en juridisk enhet. Hovedkontoer, dimensjoner, kontostrukturer, kontoplaner og kontoregler kan brukes av mer enn én juridisk enhet.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Hvis organisasjonen er modellert som en driftsenhet

En driftsenhet kan ikke ha sin egen finansinformasjon. Hvis de interne organisasjonene ikke krever unike kontoer, kan du modellere dem som driftsenheter. Finansiell informasjon blir konfigurert for den overordnede juridiske enheten i hierarkiet. Inntektsregnskap kan opprettes for driftsenheter i en juridisk enhet eller for den overordnede juridiske enheten.

### <a name="fiscal-calendars"></a>Økonomiske kalendere

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Hvis organisasjonen er modellert som en juridisk enhet

Hver juridiske enhet har sin egen regnskapskalender. Hvis de interne organisasjonene bruker ulike regnskapsår og regnskapskalendere, må du modellere organisasjonene som juridiske enheter.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Hvis organisasjonen er modellert som en driftsenhet

Driftsenheter må dele en regnskapskalender. Hvis de interne organisasjonene kan bruke de samme regnskapsårene og regnskapskalenderne, kan du modellere organisasjonene som driftsenheter.

### <a name="consolidation"></a>Konsolidering

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Hvis organisasjonen er modellert som en juridisk enhet

Du må konsolidere de finansielle resultatene for regionale kontorer i et enkelt, konsolidert firma for å klargjøre regnskapsoppgjør.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Hvis organisasjonen er modellert som en driftsenhet

Konsolidering er ikke nødvendig, fordi data allerede deles mellom driftsenheter.

### <a name="centralized-payments"></a>Sentraliserte betalinger

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Hvis organisasjonen er modellert som en juridisk enhet

Sentraliserte betalinger må defineres, slik at fakturaer for alle underordnede juridiske enheter kan betales til eller fra én overordnet juridisk enhet.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Hvis organisasjonen er modellert som en driftsenhet

Sentraliserte betalinger er ikke nødvendige, siden alle fakturaer registreres i én juridisk enhet.

### <a name="intercompany-transactions"></a>Konserninterne transaksjoner

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Hvis organisasjonen er modellert som en juridisk enhet

Konserninterne salgsordrer, bestillinger, betalinger eller mottak kan brukes til hverandre. Du trenger ikke å bruke journalbilag. Du kan vise konserninterne transaksjoner på underfinansnivå (kunder, leverandører). Eksemplene nedenfor viser hvordan konserninterne transaksjoner behandles.

##### <a name="example-1-headquarters-provides-services-to-regional-offices-and-must-charge-the-costs-of-those-services-to-the-regional-offices"></a>Eksempel 1: Hovedkontoret tilbyr tjenester til avdelingskontorer og må belaste kostnadene for disse tjenestene til avdelingskontorene

Hvis du modellerer avdelingskontoret som en juridisk enhet, har du følgende alternativer:

- Hovedkontor oppretter en journaloppføring for å kryssbelaste avdelingskontoret for utgiften. Transaksjonene kan ikke aldersfordeles.
- Hovedkvarteret sender en innkjøpsordre for tjenesten til avdelingskontoret. En salgsordre opprettes automatisk i den juridiske enheten for det regionale kontoret, med konserninterne underordnede finanstransaksjoner.

##### <a name="example-2-headquarters-procures-and-pays-for-service-that-is-delivered-to-a-regional-office"></a>Eksempel 2: Hovedkontoret anskaffer og betaler for tjeneste som leveres til et avdelingskontor

Hvis du modellerer avdelingskontoret som en juridisk enhet, har du følgende alternativer:

- Fakturaen og betalingen følger myndighetskravene til hovedkvarteret. Hovedkontoret kan opprette en journaloppføring for å kryssbelaste avdelingskontoret for utgiften. Transaksjonene kan ikke aldersfordeles.
- Fakturaen og betalingen følger myndighetskravene til hovedkvarteret. Hovedkontoret kan opprette en konsernintern underfinanstransaksjon.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Hvis organisasjonen er modellert som en driftsenhet

Konserninterne transaksjoner mellom driftsenheter støttes bare gjennom journalbilag. En driftsenhet kan ikke sende eller motta en bestilling, salgsordre eller faktura fra en annen driftsenhet i samme juridiske enhet. Du kan ikke vise konserninterne transaksjoner på underfinansnivå (kunder, leverandører). Eksemplene nedenfor viser hvordan konserninterne transaksjoner behandles.

##### <a name="example-1-headquarters-provides-services-to-regional-offices-and-must-charge-the-costs-of-those-services-to-the-regional-offices"></a>Eksempel 1: Hovedkontoret tilbyr tjenester til avdelingskontorer og må belaste kostnadene for disse tjenestene til avdelingskontorene

Hvis du modellerer avdelingskontoret som en driftsenhet, registrerer hovedkontoret en utgiftstransaksjon og koder den til avdelingskontoret.

##### <a name="example-2-headquarters-procures-and-pays-for-service-that-is-delivered-to-a-regional-office"></a>Eksempel 2: Hovedkontoret anskaffer og betaler for tjeneste som leveres til et avdelingskontor

Hvis du modellerer avdelingskontoret som en driftsenhet, følger fakturaen og betalingen hovedkontorets forskriftsmessige krav. Fakturaen kan kodes til avdelingskontoret. Bruk en balanserende finansdimensjon i resultatregnskapet for å rapportere kostnader for avdelingskontoret.

### <a name="local-tax-requirements"></a>Krav for lokal skatt

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Hvis organisasjonen er modellert som en juridisk enhet

En juridisk enhet er underlagt avgiftslovene til skattemyndighetene i landet/området der den juridiske enheten er registrert. En juridisk enhet som er registrert i Danmark, er for eksempel underlagt danske avgiftslover og -bestemmelser. I Finance and Operations kan en juridisk enhet tilhøre bare ett land/område. Landet/området du velger for primæradressen for den juridiske enheten, styrer lands-/områdespesifikke funksjoner som er tilgjengelige for den juridiske enheten. Hvis primæradressen for den juridiske enheten for eksempel er i Danmark, blir funksjoner relatert til danske avgiftslover og -bestemmelser, tilgjengelige. Hvis organisasjonene er i forskjellige land/regioner, og krever forskjellige lokale mva-alternativer, må du derfor definere organisasjonene som separate juridiske enheter.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Hvis organisasjonen er modellert som en driftsenhet

Driftsenheter bruker landkonteksten for den overordnede juridiske enheten. Driftsenheter i den samme juridiske enheten kan ikke ha ulike lands-/områdespesifikke krav. Hvis organisasjonene er i samme land/område og bruker de samme avgiftsalternativene, kan du definere dem som driftsenheter.

### <a name="statutory-reporting-for-a-countryregion"></a>Lovbestemt rapportering for land/område

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Hvis organisasjonen er modellert som en juridisk enhet

For land/områder som støttes av Finance and Operations, kan de fleste lovbestemte rapporter opprettes. Hvis du vil ha informasjon om hvilke rapporter som er tilgjengelige for hvert land/område, kan du se [Microsoft Dynamics-lokaliseringsportalen](https://mbs.microsoft.com/customersource/global/ax/support/support-news/GFMLocalizationPortalMC) for Finance and Operations. (CustomerSource-pålogging kreves.)

> [!NOTE]
> I Finance and Operations gir et posteringslag hovedboka deg mulighet til å justere oppføringer til et morselskap som bruker en annen regnskapsstandard enn datterselskapet. For et firma som bruker generelt godtatt regnskapspraksis i Storbritannia (UK GAAP), kan du for eksempel gjør justeringer i posteringslaget. Disse oppføringene kan konsolideres til et morselskap som bruker generelt godkjente regnskapsprinsipper (kalt GAAP) i USA. Justeringspostene har ingen innvirkning UK GAAP-rapportering.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Hvis organisasjonen er modellert som en driftsenhet

Lovbestemte rapporter må opprettes ved hjelp av et annet program. Du må forsikre deg om at data blir registrert i Finance and Operations for å støtte kravene for hver driftsenheten, der de skiller seg fra kravene til hovedkontoret.

### <a name="currency"></a>Valuta

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Hvis organisasjonen er modellert som en juridisk enhet

Hvis organisasjonene må bruke ulike funksjonelle valutaer, må du modellere organisasjonene som juridiske enheter. Funksjonell valuta defineres per juridiske enhet. Du kan imidlertid angi transaksjoner i flere valutaer.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Hvis organisasjonen er modellert som en driftsenhet

Hvis organisasjonene kan bruke én funksjonell valuta, kan du modellere organisasjonene som driftsenheter. Driftsenheter må dele en funksjonell valuta. Du kan imidlertid angi transaksjoner og opprette rapporter i flere valutaer.

### <a name="year-end-closing"></a>Årsavslutning

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Hvis organisasjonen er modellert som en juridisk enhet

Hvis lover og regnskapspraksis er forskjellige i landene/områdene der organisasjonene dine er, må du kanskje bruke ulike årsavslutningsprosedyrer per organisasjon. Dette betyr at du må utforme organisasjonene som juridiske enheter. Hver juridiske enhet har sine egne prosedyrer ved årets slutt.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Hvis organisasjonen er modellert som en driftsenhet

Hvis lover og regnskapspraksis er de samme i landene/områdene der organisasjonene dine er, kan du bruke ett sett med årsavslutningsprosedyrer. Dette betyr at du kan utforme organisasjonene som driftsenheter. Alle driftsenheter må bruke samme prosedyre for årsavslutning.

### <a name="number-sequences"></a>Nummerserier

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Hvis organisasjonen er modellert som en juridisk enhet

Nummerserier for noen referanser kan konfigureres per juridisk enhet. Noen nummerserier kan deles.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Hvis organisasjonen er modellert som en driftsenhet

Nummerserier for noen referanser kan konfigureres per driftsenhet. Noen nummerserier kan deles.

### <a name="products"></a>Produkter

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Hvis organisasjonen er modellert som en juridisk enhet

Produktdefinisjoner deles, og de må frigis til individuelle juridiske enheter før de kan inkluderes i transaksjoner. Hver juridiske enhet har sitt eget sett med frigitte produkter som kan inkluderes i transaksjonsdokumenter. Hvis de interne organisasjonene må bruke ulike sett med produkter, må du modellere organisasjonene som juridiske enheter.

> [!NOTE]
> Selv om produktdefinisjoner deles, kan du, i hver juridiske enhet der et produkt er frigitt, angi ulike salgs-, innkjøps- og lagringsparametere for varen i hvert lagerområde.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Hvis organisasjonen er modellert som en driftsenhet

Alle driftsenheter deler samme sett med produkter. Hvis de interne organisasjonene kan dele samme sett med produkter, kan du modellere organisasjonene som driftsenheter.

### <a name="inquiry-and-reporting"></a>Forespørsel og rapportering

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Hvis organisasjonen er modellert som en juridisk enhet

Du må manuelt endre firmaer for å angi transaksjoner og utføre forespørsler i flere juridiske enheter. På grunn av datasikkerhetsgrenser kan konsolidert forespørsel og rapportering være ressursintensiv og tidkrevende.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Hvis organisasjonen er modellert som en driftsenhet

Du trenger ikke å endre firmaer for å få tilgang til data fra flere driftsenheter. Konsolidert forespørsel og rapportering og individuell regional forespørsel er enklere og raskere.

## <a name="best-practices-for-modeling-organizations-and-hierarchies"></a>Anbefalte fremgangsmåter for modellering av organisasjoner og hierarkier

Vurder følgende anbefalte fremgangsmåter når du implementerer et organisasjonshierarki:

- Opprett en avdeling for å modellere skjæringspunktet mellom en juridisk enhet og en forretningsenhet. Du kan deretter rulle opp data fra en avdeling for en juridisk enhet for lovbestemt rapportering og fra en avdeling til en forretningsenhet for intern rapportering. Avdelinger kan fungere som fortjenestesentre. Hvis du bruker avdelinger, trenger du ikke å bruke juridiske enheter og forretningsenheter som dimensjoner i kontostrukturen. Du kan bruke bare avdelinger som en dimensjon. Du må imidlertid bruke både kostsentre og avdelinger som dimensjoner i kontostrukturen hvis kostsentre bare brukes som kostnadsakkumulatorer og avdelinger brukes til inntektsføring.
- Utforme flere hierarkier for driftsenheter hvis du har omfattende rapporteringskrav for resultater.
- Ikke modeller flere hierarkier for samme hierarkiformål i én juridisk enhet.
- Ikke opprett et hierarki for hvert formål. Vanligvis kan du bruke ett hierarki til flere formål. Ett hierarki av driftsenheter kan for eksempel tilordnes til alle policy-relaterte formål.
- Opprett balanserte hierarkier. Alle noder som har samme avstand fra rotnoden i et hierarki, defineres som et nivå. Bare én type driftsenhet kan forekomme på hvert nivå i et balansert hierarki, og avstanden fra rotnoden til hvert nivå er ensartet. Hvis det er mellomnivåer mellom en avdeling og en juridisk enhet eller en forretningsenhet, må kanskje plassholderorganisasjoner opprette et balansert hierarki.
- Ikke utform et eget hierarki av driftsenheter hvis strukturen for juridiske enheter også er driftsstrukturen. En blandet hierarki av juridiske enhetenr og driftsenheter kan brukes til begge formål.
- Før du modellerer store omstruktureringsscenarier, bruker du hierarkiets gyldighetsdatoer til å foreta en konsekvensanalyse og en valideringstest.
- Bruk kladdemodus for å endre et hierarki før du publiserer en ny versjon i et produksjonsmiljø.
- Begrense antall personer som har tillatelse til å legge til eller fjern organisasjoner fra et hierarki i et produksjonsmiljø. Et mindre antall reduserer sjansen for at kostbare feil kan oppstå, og at det må gjøres rettelser.
