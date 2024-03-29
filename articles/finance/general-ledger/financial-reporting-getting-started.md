---
title: Oversikt over finansrapportering
description: Denne artikkelen beskriver hvor du kan få tilgang til økonomisk rapportering i Microsoft Dynamics 365 Finance og hvordan du bruker de økonomiske rapporteringsfunksjoner.
author: aprilolson
ms.date: 06/20/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "10444"
- intro-internal
ms.assetid: 3eae6dc3-ee06-4b6d-9e7d-1ee2c3b10339
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9d0c2e821ee504cd62a536674ef91ee89a25c0a9
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/29/2022
ms.locfileid: "9066425"
---
# <a name="get-started-with-financial-reporting"></a>Kom i gang med finansrapportering 

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver hvor du kan få tilgang til Financial Reporting, og hvordan du bruker finansrapporteringsfunksjonene. Det inneholder også en beskrivelse av de økonomiske standardrapportene som tilbys.

## <a name="enable-financial-reporting"></a>Aktiver finansrapportering
For at organisasjonen skal kunne bruke finansrapporteringstjenesten, må en LCS-administrator (Lifecycle Services) aktivere denne tjenesten i LCS-portalen for organisasjonen. Hvis finansrapportering ikke er klargjort for miljøet, kontakter du LCS-administratoren for å aktivere tjenesten. 

## <a name="accessing-financial-reporting"></a>Tilgang til finansrapportering

Du finner **Financial reporting**-menyen på følgende lokasjoner:

- **Økonomimodul** > **Forespørsler og rapporter**
- **Budsjettering** > **Forespørsler og rapporter** > **Grunnleggende budsjettering**
- **Budsjettering** > **Forespørsler og rapporter** > **Budsjettplanlegging**
- **Budsjettering** > **Forespørsler og rapporter** > **Budsjettkontroll**
- Konsolideringer

Hvis du vil opprette og generere finansrapporter for en juridisk enhet, må du angi følgende informasjon for den juridiske enheten:

- Økonomisk kalender
- Ledger
- Kontoplan
- Valuta.
- Postere en transaksjon til minst én konto
- MainAccount er oppført i **Valgt**-kolonnen i siden **Oppsett for Financial Reporting** (**Økonomimodul > Finansoppsett > Oppsett for Financial Reporting**)

## <a name="granting-security-access-to-financial-reporting"></a>Tildele sikkerhetstilgang til Financial Reporting

Funksjonene for økonomisk rapportering er tilgjengelige for brukere som er tilordnet de nødvendige rettighetene og pliktene via sikkerhetsrollene sine. De følgende delene viser disse rettighetene og pliktene sammen med de tilknyttede rollene.

### <a name="duties"></a>Plikter

| Etikett for plikt                            | beskrivelse                                                             | Navn på applikasjonsobjekttre                         |
|---------------------------------------|-------------------------------------------------------------------------|----------------------------------|
| Vedlikehold finansrapporteringssikkerhet | Vedlikehold Financial Reporting-sikkerhet og utfør administrative oppgaver. | FinansrapportersikkerhetVedlikehold |
| Vedlikehold finansrapporter            | Utform og vedlikehold finansrapporter.                                  | FinansrapporterVedlikehold         |
| Generer finansrapporter            | Generer og oppdater finansrapporter.                                 | FinansrapporterGenerer         |
| Gå gjennom finansresultat          | Gå gjennom og analyser finansresultat.                               | FinansrapporterUtførGjennomgang       |

### <a name="privileges"></a>Rettigheter

| Etikett for rettighet                       | beskrivelse                                                             | Navn på applikasjonsobjekttre                         |
|---------------------------------------|-------------------------------------------------------------------------|----------------------------------|
| Vedlikehold finansrapporteringssikkerhet | Vedlikehold Financial Reporting-sikkerhet og utfør administrative oppgaver. | FinansrapportersikkerhetSystemvedlikehold |
| Vedlikehold finansrapporter            | Utform og vedlikehold finansrapporter.                                  | FinansapporterVedlikeholdRapporter  |
| Generer finansrapporter            | Generer og oppdater finansrapporter.                                 | FinansrapporterGenererRapporter  |
| Vis finansrapporter                | Vis finansrapporter.                                                 | FinansrapporterVis             |

### <a name="roles"></a>Roller

| Etikett for rettighet                       | Plikt                                  | Roller                                                                           |
|---------------------------------------|---------------------------------------|---------------------------------------------------------------------------------|
| Vedlikehold finansrapporteringssikkerhet | Vedlikeholde Financial Reporting-sikkerhet | Sikkerhetsadministrator                                                          |
| Vedlikehold finansrapporter            | Vedlikehold finansrapporter            | Regnskapssjef, Regnskapsansvarlig, Økonomikontrollør, Budsjettbehandler |
| Generer finansrapporter            | Generer finansrapporter            | CEO, CFO, Regnskapsfører                                                            |
| Vis finansrapporter                | Gå gjennom finansresultat          | Ikke tilordnet                                                                   |

Når en bruker er lagt til eller en rolle er endret, skal brukeren kunne få tilgang til Financial Reporting på noen få minutter. 

> [!NOTE]
> Sysadmin-rollen er lagt til alle roller i Financal Reporting.

## <a name="report-deletions-and-expirations"></a>Rapportslettinger og -utløp

Brukere som genererer en rapport, kan slette sine egne rapporter. Brukere med plikten **Vedlikehold finansrapporteringssikkerhet**, kan slette andres rapporter. 

I versjon 10.0.8 ble konseptet med utløpsdatoer innført. En ny nødvendig funksjon er aktivert på **Alle**-siden i arbeidsområdet for funksjonsbehandling. Funksjonen **Oppbevaringspolicyer for finansrapport** inneholder følgende endringer:
* Nylig genererte rapporter blir automatisk merket som å ha en utløpsdato på 90 dager fra når de genereres.
* Eventuelle eksisterende rapporter fra før funksjonen ble installert vil bli gitt en 90 dagers utløpsperiode. Datoen kan vises som tom for en kort tidsperiode før Financial Reporting-tjenesten kjører, en rapport genereres, og tjenesten utfører oppdateringen til eksisterende rapporter med en tom utløpsdato. 
* Brukere med **Vedlikehold finansrapporteringssikkerhet**, har tilgang til denne funksjonaliteten. Alle brukere i plikten **Vedlikehold finansrapporter** gitt rettigheten **Vedlikehold utløp for finansrapport** vil også ha muligheten til å endre utløpsperioden. For øyeblikket er det to tilgjengelige bevaringsalternativer: 

    * Utløp av 90 dager.
    * Et alternativ for å angi at rapporten aldri skal utløpe.

Når et utløp, for eksempel 90 dager, er valgt, blir den brukt 90 dager fra i dag. Dette er en annen virke måte enn 90 dager fra den opprinnelige genereringsdatoen som ble angitt da rapporten ble generert. 

Flere alternativer vil bli tatt med i fremtidig funksjonalitet. Utløpet på 90 dager vil være standard, og brukere med riktige tillatelser kan overstyre standardinnstillingene på listesiden **Finansrapporter**.

## <a name="default-reports"></a>Standardrapporter

Finansrapportering gir 22 standard finansrapporter. Alle rapportene bruker standard hovedkontokategorier. Du kan bruke disse rapportene som de er eller som et utgangspunkt for ditt finansrapporteringsbehov. I tillegg til de tradisjonelle regnskapsoppgjørene, for eksempel resultatregnskap og balanse, inkluderer disse standardrapportene rapporter som viser de forskjellige typene finansrapporter du kan opprette. 

<!--Each report in the following table links to an Office Mix presentation about the report.-->

| Standardrapport                                                                                         | Beskrivelse                                                                                                                                                                                                                                                                                                          |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 12 måneder Opprulling Én kolonne Resultatregnskap – Standard | Vis organisasjonens fortjeneste for de siste 12 månedene i én enkelt kolonne.                                                                                                                                                                                                                                      |
| 12 måneder Trend Resultatregnskap – Standard                 | Vis organisasjonens fortjeneste for hver av de 12 siste månedene. Disse 12 månedene kan strekke seg over mer enn ett regnskapsår.                                                                                                                                                                                             |
| Faktisk kontra Budsjett – Standard                                | Vis detaljert saldoinformasjon for alle kontoer for det opprinnelige budsjettet, og sammenlign det reviderte budsjettet med faktiske data som har et avvik.                                                                                                                                                                          |
| Revisjonsdetaljer – Standard                                  | Vis detaljert saldoinformasjon for alle kontoer. Denne rapporten viser debet- og kreditsaldoer i rapporteringsvalutaen og i lokal valuta, sammen med mer transaksjonsinformasjon, som for eksempel bruker-ID-en, brukeren som sist endret dataene, datoen for siste endring og journal-ID-en. |
| Saldoliste – Standard                                   | Vis detaljert saldoinformasjon for alle kontoer. Denne rapporten viser åpnings- og lukkingssaldoer og debet- og kreditsaldoer for den aktuelle perioden og året hittil, sammen med mer transaksjonsinformasjon, for eksempel bilaget.                                                                    |
| Balanse – Standard                                   | Vis organisasjonens finansiell stilling for året.                                                                                                                                                                                                                                                             |
| Balanse og resultatregnskap side ved side – Standard | Vis finansiell stilling og lønnsomhet i organisasjonen for året side ved side.                                                                                                                                                                                                                              |
| Kontantstrøm – Standard                                       | Få innsikt i kontanter som kommer inn til og går ut av organisasjonen.                                                                                                                                                                                                                                   |
| Detaljert JE- og TB-gjennomgang – Standard                      | Vis åpningssaldo og aktivitetsinformasjon for alle kontoer.                                                                                                                                                                                                                                                      |
| [Detaljert råbalanse – Standard](trial-balance-financial-reports.md)| Vis saldoinformasjon for alle kontoer som har debet- og kreditsaldoer, og nettoen for disse saldoene, sammen med transaksjonsdato, bilag og journalbeskrivelse.                                                                                                                                  |
| Utgifter Tre år Kvartalsvis Trend – Standard             | Få innsikt i utgifter for de siste 12 kvartalene over de siste tre årene.                                                                                                                                                                                                                                   |
| Gjennomgang av finansoverskrifter for JE og TB – Standard            | Se en oversikt over saldoer og aktivitet for finansoverskriftene aktiva, gjeld, eierens egenkapital, omsetning, utgift, gevinst eller tap.                                                                                                                                                                           |
| [Resultatregnskap – Standard](income-statement-financial-report.md)| Vis organisasjonens lønnsomhet for inneværende periode og hittil i år.                                                                                                                                                                                                                                   |
| Finanstransaksjonsliste – Standard                        | Vis detaljert saldoinformasjon for alle kontoer. Denne rapporten viser debet- og kreditsaldoer sammen med mer transaksjonsinformasjon som transaksjonsdato, journalnummer, bilag, posteringstype og sporingsnummer.                                                                            |
| Forhold – Standard                                          | Vis solvens, lønnsomhet og effektivitetsrate for organisasjonen for året.                                                                                                                                                                                                                           |
| Opprulling 12 måneder Utgifter – Standard                       | Få innsikt i utgifter for hver av de siste 12 månedene. Disse 12 månedene kan strekke seg over mer enn ett regnskapsår.                                                                                                                                                                                                       |
| Opprulling Kvartalsvis Resultatregnskap – Standard               | Vis organisasjonens lønnsomhet kvartalsvis for det siste året samt hittil i år.                                                                                                                                                                                                                   |
| Side ved side Balanse – Standard                      | Vis organisasjonens finansiell stilling for året. Denne rapporten viser aktiva, gjeld og egenkapital for aksjeeiere side ved side.                                                                                                                                                                                |
| [Råbalansesammendrag – Standard](trial-balance-financial-reports.md)| Vis saldoinformasjon for alle kontoer som har åpnings- og avslutningssaldo og debet- og kreditsaldoer, sammen med deres nettoforskjell.                                                                                                                                                                  |
| [Sammendrag Råbalanse Årlig – Standard](trial-balance-financial-reports.md)| Vis saldoinformasjon for alle kontoer som har åpnings- og avslutningssaldo og debet- og kreditsaldoer, sammen med deres nettoforskjell for gjeldende og forrige år.                                                                                                                           |
| Ukentlig Salg og rabatter – Standard                     | Få innsikt i salg og rabatter for hver uke i en måned. Denne rapporten inneholder totalt fire uker.                                                                                                                                                                                                              |
| Budsjettmidler tilgjengelig - standard                         | Vis en detaljert sammenligning av revidert budsjett, faktiske utgifter, budsjettreservasjoner og budsjettmidler tilgjengelig for alle kontoer                                                                                                                                                                                  |

## <a name="opening-financial-reports"></a>Åpne finansrapporter

Når du velger **Financial Reporting**-menyen, vises listen over standard finansrapporter for firmaet. Deretter kan du åpne eller endre en rapport. Velg rapportnavnet for å åpne en av standardrapportene. Første gang en rapport åpnes, genereres den automatisk for forrige måned. Hvis du for eksempel åpner en rapport for første gang i august 2019, genereres rapporten for 31. juli 2019. Når en rapport åpnes, kan du begynne å utforske den ved å gå nedover i bestemte deler av data og endre rapportalternativer.

## <a name="creating-and-modifying-financial-reports"></a>Opprette og endre finansrapporter

Du kan opprette en ny rapport fra listen for finansrapporter eller endre en eksisterende rapport. Hvis du har de nødvendige tillatelsene, kan du opprette en ny finansrapport ved å velge **Ny** i handlingsruten. Et rapportutforming-program lastes ned til enheten. Du kan deretter opprette den nye rapporten etter at rapportutformingen starter. Når du har lagret den nye rapporten, vises den i finansrapportlisten. Listen viser bare rapporter som er opprettet for firmaet som du bruker i Dynamics 365 Finance. 

## <a name="reporting-tree-definitions"></a>Rapporteringstredefinisjoner

En av komponentene som brukes til å bygge finansrapporter, er en rapporteringstredefinisjon. En rapporteringstredefinisjon bidrar til å definere strukturen og hierarkiet i organisasjonen. Den er en hierarkisk struktur på tvers av dimensjoner som basert på dimensjonsrelasjonene i de økonomiske dataen. Den inneholder informasjon på rapporteringsenhetsnivå og et sammendragsnivå for alle enheter i treet.

Du kan opprette et ubegrenset antall rapporteringstrær for å vise organisasjonens data på forskjellige måter. Hvert rapporteringstre kan inneholde en hvilken som helst kombinasjon av avdelinger og sammendragsenheter, men en rapportdefinisjon kan bare kobles til ett rapporteringstre om gangen. 

## <a name="update-the-financial-reporting-version-through-slipstreaming"></a>Oppdatere Financial Reporting-versjonen ved hjelp av integrering

Økonomi- og driftsapper oppdateres hver måned. Financial Reporting oppdateres ikke nødvendigvis oppdateres på den frekvensen. Kundene har dessuten flere alternativer når de implementerer oppdateringer for økonomi- og driftsapper. Financial Reporting-oppdateringer installeres automatisk. Financial Reporting har en angitt versjon som forbrukes i et kundemiljø når en serviceoppdatering implementeres, når nedetid startes, eller når en kundes miljø er i vedlikeholdsmodus. Denne prosessen kalles *integrering* eller *true-up*, fordi alle kundeimplementeringer settes til samme versjon av Financial Reporting.

Endringer som frigis i hver versjon, finner du under [Hva er nytt eller endret i Dynamics 365 Finance](../../finance/get-started/whats-new-home-page.md). Du finner plattformoppdateringer og reparasjonsfiler under Tilleggsressurser nederst på siden for hver versjon.

Den valgte oppdaterte versjonen er en gjennomgått og validert versjon av Financial Reporting som er klar for produksjon. Den er kompatibel med alle tidligere eller fremtidige versjoner av Dynamics 365 Finance. Financial Reporting kan for eksempel være på det siste 10.0.19-bygget, mens kunden fremdeles er i programversjon 10.0.16.

> [!NOTE]
> Det eneste forholdet der kunder kan flytte til en tidligere versjon (et nedgraderingsscenario) oppstår hvis Microsoft stopper en true-up-utrulling på grunn av et problem. Så snart en reparasjon er tilgjengelig, brukes den automatisk.

Slipprosessen er fullstendig automatisert og krever ingen kundehandling. Tre topologier forbruker integrasjonen, hver på litt ulike måter:

- **Lokal** – Lokale distribusjoner støtter ikke integrasjon og true-up.
- **Infrastruktur som en tjeneste (IaaS)** – Integrasjonslogikken brukes under enhver operasjon som prøver å oppdatere Financial Reporting. Den inneholder binære oppdateringer eller kringkastinger som inneholder binære oppdateringer.
- **Selvbetjening** – Enhver operasjon som krever nedetid for Financial Reporting, bruker integrasjonslogikken:

    - Binære oppdateringer eller kringkastinger som inneholder binære oppdateringer
    - S-oppdatering av eller annen nedetid for infrastruktur
    - AOT-pakkedistribusjoner

## <a name="troubleshooting-issues-opening-report-designer"></a>Feilsøke problemer med å åpne Rapportutforming

Det finnes noen vanlige problemer som kan føre til problemer når du åpner Rapportutforming. Disse problemene og fremgangsmåten for å løse dem er som følger.

Problem 1: Rapportutforming starter ikke når du velger **Ny** eller **Rediger**.

* Under Internet Explorer velger du **Innstillinger**, og deretter velger du **Alternativer for Internett**. Velg kategorien **Sikkerhet**. Velg Klarerte områder, og velg deretter **Områder**. I **Legg til dette nettstedet i sonen** angir du "\*\.dynamics.com" (uten anførselstegn) og velger deretter **Legg til**. 
* Under Internet Explorer velger du **Innstillinger**, og deretter velger du **Alternativer for Internett**. Velg **Sikkerhet**-kategorien. Velg Klarerte områder. I området merket Sikkerhetsnivå for denne sonen endrer du alternativet til **Middels–lavt**.
* Deaktiver popup-blokkering i leseren.
* Arbeidsstasjoner kreves for å installere Microsoft .NET Framework 4.7.2 eller senere. Denne versjonen av Microsoft .NET Framework kan lastes ned og installeres fra [Microsoft Download Center](https://dotnet.microsoft.com/download/dotnet-framework/net472).
* Hvis du bruker Chrome-leseren, må du installere et ClickOnce-tillegg for å kunne laste ned Rapportutforming-klienten. Hvis du kjører Chrome i inkognitomodus, må du kontrollere at ClickOnce-tillegget er aktivert for inkognitomodus. Hvis du vil ha mer informasjon om Chrome ClickOnce-utvidelsen, kan du se [Systemkrav for skydistribusjoner](../../fin-ops-core/fin-ops/get-started/system-requirements.md).
* Hvis du bruker Microsoft Edge med en Chrome-leser, trenger du ikke å installere et ClickOnce-tillegg for Edge Chromium. Du må imidlertid aktivere alternativet ClickOnce for å laste ned rapportformingsklienten. Hvis du kjører i inkognitomodus, må du kontrollere at ClickOnce-tillegget er aktivert for inkognitomodus.

    1. Åpne en ny nettleser i Microsoft Edge.
    2. Angi **edge://flags**, og velg **Enter**.
    3. Søk etter alternativet **ClickOnce kundestøtte**, eller bruk denne direkte koblingen: **edge://flags/#edge-click-once**.
    4. Sett rullegardinmenyen til **Aktivert**.
    5. Velg **Start leseren på nytt**.

Problem 2: Brukeren er ikke tilordnet de nødvendige tillatelsene til å bruke Financial Reporting. 

* Hvis du vil kontrollere om brukeren ikke har tillatelse, velger du **Ja** ved feilen "Kan ikke koble til Financial Reporting-serveren. Velg Ja hvis du vil fortsette og angi en annen serveradresse". Velg deretter **Tilkoblingstest**. Hvis du ikke har tillatelse til det, vil du se en melding om at "Tilkoblingsforsøket mislyktes. Brukeren har ikke nødvendige tillatelser til å koble til serveren. Kontakt systemansvarlig".
* Nødvendige tillatelser er oppført ovenfor i [Tildele sikkerhetstilgang til Financial Reporting](#granting-security-access-to-financial-reporting). Sikkerhet i Financial Reporting er basert på disse rettighetene. Du får ikke tilgang med mindre disse rettighetene (eller en annen sikkerhetsrolle som inneholder disse rettighetene) er tilordnet til deg. 
* Integrasjonsoppgaven **Firmabrukeres leverandør til selskap** (som også er ansvarlig for og kjent som brukerintegrasjon), kjører med et intervall på 5 minutter. Det kan ta opptil 10 minutter før alle endringer i tillatelser trer i kraft i Financial Reporting. 

    Hvis en annen bruker kan åpne Rapportutforming, velger du **Verktøy**, og deretter velger du **Integreringsstatus**. Kontroller at integreringskartet, "Firmabrukeres leverandør til selskap", har blitt kjørt riktig fordi du var tilordnet tillatelse til å bruke Financial Reporting. 

* Det er mulig at en annen feil har forhindret **integrasjon fra Dynamics-bruker til Financial Reporting-bruker** i å fullføres. Det er mulig at en datatorgtilbakestilling er startet og ikke er fullført ennå, eller at det har oppstått en annen systemfeil. Prøv å kjøre prosessen på nytt senere. Hvis problemet vedvarer, kontakter du systemansvarlig.

Problem 3: Du kan fortsette etter påloggingssiden for **ClickOnce Report Designer**, men du kan ikke fullføre påloggingen i Report Designer. 

* Tiden som er angitt på den lokale datamaskinen når du angir påloggingsinformasjonen din, må være innen fem minutter av tiden på Financial Reporting-serveren. Hvis det er en forskjell på mer enn fem minutter, vil ikke systemet tillate pålogging. 
* Hvis tiden på datamaskinen er forskjellig fra tiden på Financial Reporting-server, anbefaler vi at du aktiverer Windows-alternativet for å angi datamaskinens tid automatisk. 

## <a name="troubleshoot-report-designer-issues-with-event-viewer"></a>Feilsøk problemer med Report Designer med Hendelsesliste

Du kan bruke hendelseslisten til å analysere noen av problemene som oppstår ved bruk av Financial Reporting. 

### <a name="what-happens-when-you-have-connections-issues-with-financial-reporting"></a>Hva skjer når du har tilkoblinger problemer med Financial Reporting? 

Her er noen trinn du kan gjøre for å gjøre løsningen med Microsoft kundestøtte mer effektiv og gi deg en raskere løsning. 
 
Trinnene nedenfor går gjennom prosessen med å aktivere Hendelseslistemeldinger for Financial Reporting. Loggene som hendelseslisten genererer, vil hjelpe teknikere med å identifisere kilden til tilkoblingsproblemet raskt. Send kopier av disse loggene sammen med forespørselen når du kontakter kundestøtte.


1. Kopier RegisterETW.zip-filen til klientarbeidsstasjonen (helst skrivebordet), og pakk ut [RegisterETW.zip](https://mbs2.microsoft.com/fileexchange/?fileID=60b1106b-d5f8-4e0f-8041-039102505122).
2. Kontroller at Windows Hendelsesliste er lukket.
3. Åpne en ledetekst for Administrator PowerShell, og gå til katalogen der RegisterETW.ps1 er plassert.
4. Kjør følgende kommando: .\RegisterETW.ps1

    Et vellykket utdata i PowerShell vil bli kontrollert med meldingen, **Competed RegisterETW-skriptet**.

    Åpne Hendelsesliste på nytt, og du vil nå se disse loggene under **Microsoft > Dynamics**:

    * Klient for blandet virkelighet
    * MR-DVT
    * MR-integrasjon
    * MR-logger
    * MR-rapportering
    * MR_SchedulerTasks
    * MR-Sql
    * MR-TraceManager

5. Reproduser problemet i Report Designer.
6. Eksporter MR-Logger-hendelsen ved hjelp av Hendelsesliste.

## <a name="troubleshoot-issues-connecting-to-financial-reporting"></a>Feilsøk problemer som kobles til Financial Reporting

Problem: Du får feilmeldingen Kan ikke koble til Financial Reporting-serveren.

* Avgjør om problemet oppstår i nettlesere Chrome og Edge.
* Hvis problemet bare forekommer i én nettleser, kan det være ClickOnce-problem. 
* Når du får feilmeldingen om tilkobling, velger du **Test** for å teste tilkoblingen for å se hvilken melding som vises. 
* Problemet kan være et resultat av en annen bruker ikke har tilgang til Financial Reporting. Hvis en bruker ikke har tilgang, mottar de en melding som sier at de ikke har tillatelse.
* Hvis problemet oppstår på flere nettlesere, må du kontrollere at tidsklokken på arbeidsstasjonen er satt til Automatisk.
* Samarbeid med en bruker som har sikkerhetsadministratorens rettigheter i Dynamics 365 Finance, og administratorrettigheter til nettverksdomenet, for å logge deg på arbeidsstasjonen for å se om de kan koble seg til. Hvis de kan koble seg til, kan det være knyttet til nettverkstillatelser.
* Deaktiver brannmuren midlertidig på arbeidsstasjonen. Hvis du deretter kan koble til Report Designer, er problemet med brannmuren. Samarbeid med organisasjonens IT-avdeling for å løse problemet.

## <a name="additional-resources"></a>Tilleggsressurser

- [Vis finansrapporter](view-financial-reports.md)
- [Definisjoner av rapporteringstre i finansrapporter](../../fin-ops-core/dev-itpro/analytics/financial-reporting-tree-definitions.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

