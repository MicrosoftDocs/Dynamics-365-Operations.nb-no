---
title: Finansrapportering
description: Dette emnet beskriver hvor du kan få tilgang til økonomisk rapportering i Microsoft Dynamics 365 for Finance and Operations og hvordan du bruker de økonomiske rapporteringsfunksjoner. Det inneholder en beskrivelse av de økonomiske standardrapportene som tilbys.
author: aprilolson
manager: AnnBe
ms.date: 09/26/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 10444
ms.assetid: 3eae6dc3-ee06-4b6d-9e7d-1ee2c3b10339
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c6d504a7b0640f45de4aa9f8fb60d2b1d37818bb
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "316976"
---
# <a name="financial-reporting"></a>Finansrapportering

[!include [banner](../includes/banner.md)]

Dette emnet beskriver hvor du kan få tilgang til økonomisk rapportering i Microsoft Dynamics 365 for Finance and Operations og hvordan du bruker de økonomiske rapporteringsfunksjoner. Det inneholder en beskrivelse av de økonomiske standardrapportene som tilbys.

<a name="accessing-financial-reporting"></a>Tilgang til finansrapportering
-----------------------------

Du finner **Finansrapportering**-menyen på følgende steder i Dynamics 365 for Finance and Operations:

-   **Økonomimodul** &gt; **Forespørsler og rapporter**
-   **Budsjettering** &gt; **Forespørsler og rapporter** &gt; **Grunnleggende budsjettering**
-   **Budsjettering** &gt; **Forespørsler og rapporter** &gt; **Budsjettplanlegging**
-   **Budsjettering** &gt; **Forespørsler og rapporter** &gt; **Budsjettkontroll**
-   Konsolideringer

Hvis du vil opprette og generere finansrapporter for en juridisk enhet, må du angi følgende informasjon for den juridiske enheten:

-   Økonomisk kalender
-   Finans
-   Kontoplan
-   Valuta

Funksjonene for økonomisk rapportering er tilgjengelige for brukere som er tilordnet de nødvendige rettighetene og pliktene via sikkerhetsrollene sine. De følgende delene viser disse rettighetene og pliktene sammen med de tilknyttede rollene.

### <a name="duties"></a>Plikter

| Etikett for plikt                            | Beskrivelse                                                             | Navn på applikasjonsobjekttre                         |
|---------------------------------------|-------------------------------------------------------------------------|----------------------------------|
| Vedlikehold finansrapporteringssikkerhet | Vedlikehold finansrapporteringssikkerhet og utfør administrative oppgaver. | FinansrapportersikkerhetVedlikehold |
| Vedlikehold finansrapporter            | Utform og vedlikehold finansrapporter.                                  | FinansrapporterVedlikehold         |
| Generer finansrapporter            | Generer og oppdater finansrapporter.                                 | FinansrapporterGenerer         |
| Gå gjennom finansresultat          | Gå gjennom og analyser finansresultat.                               | FinansrapporterUtførGjennomgang       |

### <a name="privileges"></a>Rettigheter

| Etikett for rettighet                       | Beskrivelse                                                             | Navn på applikasjonsobjekttre                         |
|---------------------------------------|-------------------------------------------------------------------------|----------------------------------|
| Vedlikehold finansrapporteringssikkerhet | Vedlikehold finansrapporteringssikkerhet og utfør administrative oppgaver. | FinansrapportersikkerhetVedlikehold |
| Vedlikehold finansrapporter            | Utform og vedlikehold finansrapporter.                                  | FinansapporterVedlikeholdRapporter  |
| Generer finansrapporter            | Generer og oppdater finansrapporter.                                 | FinansrapporterGenererRapporter  |
| Vis finansrapporter                | Vis finansrapporter.                                                 | FinansrapporterVis             |

### <a name="roles"></a>Roller

| Etikett for rettighet                       | Avgift                                  | Roller                                                                           |
|---------------------------------------|---------------------------------------|---------------------------------------------------------------------------------|
| Vedlikehold finansrapporteringssikkerhet | Vedlikehold finansrapporteringssikkerhet | Sikkerhetsadministrator                                                          |
| Vedlikehold finansrapporter            | Vedlikehold finansrapporter            | Regnskapssjef, Regnskapsansvarlig, Økonomikontrollør, Budsjettbehandler |
| Generer finansrapporter            | Generer finansrapporter            | CEO, CFO, Regnskapsfører                                                            |
| Vis finansrapporter                | Gå gjennom finansresultat          | Ikke tilordnet                                                                   |

Når en bruker er lagt til eller en rolle er endret, skal brukeren kunne få tilgang til økonomisk rapportering på noen få minutter. **Merk:** Sysadmin-rollen er lagt til alle roller i finansrapportering.

## <a name="default-reports"></a>Standardrapporter
Finansrapportering gir 22 standard finansrapporter. Alle rapportene bruker standard hovedkontokategorier i Dynamics 365 for Finance and Operations. Du kan bruke disse rapportene som de er eller som et utgangspunkt for ditt finansrapporteringsbehov. I tillegg til de tradisjonelle regnskapsoppgjørene, for eksempel resultatregnskap og balanse, inkluderer disse standardrapportene rapporter som viser de forskjellige typene finansrapporter du kan opprette. 

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
| Detaljert råbalanse – Standard                         | Vis saldoinformasjon for alle kontoer som har debet- og kreditsaldoer, og nettoen for disse saldoene, sammen med transaksjonsdato, bilag og journalbeskrivelse.                                                                                                                                  |
| Utgifter Tre år Kvartalsvis Trend – Standard             | Få innsikt i utgifter for de siste 12 kvartalene over de siste tre årene.                                                                                                                                                                                                                                   |
| Gjennomgang av finansoverskrifter for JE og TB – Standard            | Se en oversikt over saldoer og aktivitet for finansoverskriftene aktiva, gjeld, eierens egenkapital, omsetning, utgift, gevinst eller tap.                                                                                                                                                                           |
| Resultatregnskap – Standard                                | Vis organisasjonens lønnsomhet for inneværende periode og hittil i år.                                                                                                                                                                                                                                   |
| Finanstransaksjonsliste – Standard                        | Vis detaljert saldoinformasjon for alle kontoer. Denne rapporten viser debet- og kreditsaldoer sammen med mer transaksjonsinformasjon som transaksjonsdato, journalnummer, bilag, posteringstype og sporingsnummer.                                                                            |
| Forhold – Standard                                          | Vis solvens, lønnsomhet og effektivitetsrate for organisasjonen for året.                                                                                                                                                                                                                           |
| Opprulling 12 måneder Utgifter – Standard                       | Få innsikt i utgifter for hver av de siste 12 månedene. Disse 12 månedene kan strekke seg over mer enn ett regnskapsår.                                                                                                                                                                                                       |
| Opprulling Kvartalsvis Resultatregnskap – Standard               | Vis organisasjonens lønnsomhet kvartalsvis for det siste året samt hittil i år.                                                                                                                                                                                                                   |
| Side ved side Balanse – Standard                      | Vis organisasjonens finansiell stilling for året. Denne rapporten viser aktiva, gjeld og egenkapital for aksjeeiere side ved side.                                                                                                                                                                                |
| Råbalansesammendrag – Standard                          | Vis saldoinformasjon for alle kontoer som har åpnings- og avslutningssaldo og debet- og kreditsaldoer, sammen med deres nettoforskjell.                                                                                                                                                                  |
| Sammendrag Råbalanse Årlig – Standard           | Vis saldoinformasjon for alle kontoer som har åpnings- og avslutningssaldo og debet- og kreditsaldoer, sammen med deres nettoforskjell for gjeldende og forrige år.                                                                                                                           |
| Ukentlig Salg og rabatter – Standard                     | Få innsikt i salg og rabatter for hver uke i en måned. Denne rapporten inneholder totalt fire uker.                                                                                                                                                                                                              |
| Budsjettmidler tilgjengelig - standard                         | Vis en detaljert sammenligning av revidert budsjett, faktiske utgifter, budsjettreservasjoner og budsjettmidler tilgjengelig for alle kontoer                                                                                                                                                                                  |

## <a name="opening-financial-reports"></a>Åpne finansrapporter
Når du klikker **Finansrapportering**-menyen, vises listen over standard finansrapporter for firmaet. Deretter kan du åpne eller endre en rapport. Velg rapportnavnet for å åpne en av standardrapportene. Første gang en rapport åpnes, genereres den automatisk for forrige måned. Hvis du for eksempel åpner en rapport for første gang i august 2016, genereres rapporten for 31. juli 2016. Når en rapport åpnes, kan du begynne å utforske den ved å gå nedover i bestemte deler av data og endre rapportalternativer.

## <a name="creating-and-modifying-financial-reports"></a>Opprette og endre finansrapporter
Du kan opprette en ny rapport fra listen for finansrapporter eller endre en eksisterende rapport. Hvis du har de nødvendige tillatelsene, kan du opprette en ny finansrapport ved å klikke **Ny** i handlingsruten. Et rapportutforming-program lastes ned til enheten. Du kan deretter opprette den nye rapporten etter at rapportutformingen starter. Når du har lagret den nye rapporten, vises den i finansrapportlisten. Listen viser bare rapporter som er opprettet for firmaet som du bruker i Finance and Operations. 

> [!NOTE] 
> Datamaskinen som du laster ned klienten for rapportutforming på, må ha versjon 4.6.2 av Microsoft .NET Framework installert. Denne versjonen av Microsoft .NET Framework kan lastes ned og installeres fra [Microsoft Download Center](https://www.microsoft.com/en-us/download/details.aspx?id=53345). Hvis du bruker Chrome, må du installere et ClickOnce-tillegg for å kunne laste ned klienten for rapportutforming. Hvis du kjører i inkognitomodus, må du kontrollere at ClickOnce-tillegget er aktivert for inkognitomodus. Du kan også endre en rapport som vises i finansrapportlisten. Når området rundt rapportnavnet er merket, klikker du **Rediger** i handlingsruten. Rapportutformingsprogrammet starter.

## <a name="additional-resources"></a>Tilleggsressurser
- [Vise finansrapporter](view-financial-reports.md)



