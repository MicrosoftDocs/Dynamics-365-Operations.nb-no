---
title: Finansrapportering
description: "Dette emnet beskriver hvor du kan få tilgang til økonomisk rapportering i Enterprise-utgaven av Microsoft Dynamics 365 for Finance and Operations og hvordan du bruker de økonomiske rapporteringsfunksjoner. Det inneholder en beskrivelse av de økonomiske standardrapportene som tilbys."
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 10444
ms.assetid: 3eae6dc3-ee06-4b6d-9e7d-1ee2c3b10339
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: fedde78a563939fd7080e748c412c89c71586823
ms.contentlocale: nb-no
ms.lasthandoff: 06/13/2017

---

# <a name="financial-reporting"></a>Finansrapportering

[!include[banner](../includes/banner.md)]


Dette emnet beskriver hvor du kan få tilgang til økonomisk rapportering i Enterprise-utgaven av Microsoft Dynamics 365 for Finance and Operations og hvordan du bruker de økonomiske rapporteringsfunksjoner. Det inneholder en beskrivelse av de økonomiske standardrapportene som tilbys.

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
Finansrapportering gir 22 standard finansrapporter. Alle rapportene bruker standard hovedkontokategorier i Dynamics 365 for Finance and Operations. Du kan bruke disse rapportene som de er eller som et utgangspunkt for ditt finansrapporteringsbehov. I tillegg til de tradisjonelle regnskapsoppgjørene, for eksempel resultatregnskap og balanse, inkluderer disse standardrapportene rapporter som viser de forskjellige typene finansrapporter du kan opprette. Hver rapport i den følgende tabellen kobler til en Office Mix-presentasjon om rapporten.

| Standardrapport                                                                                         | beskrivelse                                                                                                                                                                                                                                                                                                          |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [12 måneder Opprulling Én kolonne Resultatregnskap – Standard](https://mix.office.com/watch/76kc7bm3wnt1) | Vis organisasjonens fortjeneste for de siste 12 månedene i én enkelt kolonne.                                                                                                                                                                                                                                      |
| [12 måneder Trend Resultatregnskap – Standard](https://mix.office.com/watch/12brmfge5p8r)                 | Vis organisasjonens fortjeneste for hver av de 12 siste månedene. Disse 12 månedene kan strekke seg over mer enn ett regnskapsår.                                                                                                                                                                                             |
| [Faktisk kontra Budsjett – Standard](https://mix.office.com/watch/fi439lkwr0no)                                | Vis detaljert saldoinformasjon for alle kontoer for det opprinnelige budsjettet, og sammenlign det reviderte budsjettet med faktiske data som har et avvik.                                                                                                                                                                          |
| [Revisjonsdetaljer – Standard](https://mix.office.com/watch/1i15nzd3nwkyh)                                  | Vis detaljert saldoinformasjon for alle kontoer. Denne rapporten viser debet- og kreditsaldoer i rapporteringsvalutaen og i lokal valuta, sammen med mer transaksjonsinformasjon, som for eksempel bruker-ID-en, brukeren som sist endret dataene, datoen for siste endring og journal-ID-en. |
| [Saldoliste – Standard](https://mix.office.com/watch/1kezwu2a10fq4)                                   | Vis detaljert saldoinformasjon for alle kontoer. Denne rapporten viser åpnings- og lukkingssaldoer og debet- og kreditsaldoer for den aktuelle perioden og året hittil, sammen med mer transaksjonsinformasjon, for eksempel bilaget.                                                                    |
| [Balanse – Standard](https://mix.office.com/watch/zkgq0u7visw9)                                   | Vis organisasjonens finansiell stilling for året.                                                                                                                                                                                                                                                             |
| [Balanse og resultatregnskap side ved side – Standard](https://mix.office.com/watch/zkgq0u7visw9) | Vis finansiell stilling og lønnsomhet i organisasjonen for året side ved side.                                                                                                                                                                                                                              |
| [Kontantstrøm – Standard](https://mix.office.com/watch/jd3go9pz6390)                                       | Få innsikt i kontanter som kommer inn til og går ut av organisasjonen.                                                                                                                                                                                                                                   |
| [Detaljert JE- og TB-gjennomgang – Standard](https://mix.office.com/watch/1sw9fmtwgjb1f)                      | Vis åpningssaldo og aktivitetsinformasjon for alle kontoer.                                                                                                                                                                                                                                                      |
| [Detaljert råbalanse – Standard](https://mix.office.com/watch/1ewwgbpv0iwrl)                         | Vis saldoinformasjon for alle kontoer som har debet- og kreditsaldoer, og nettoen for disse saldoene, sammen med transaksjonsdato, bilag og journalbeskrivelse.                                                                                                                                  |
| [Utgifter Tre år Kvartalsvis Trend – Standard](https://mix.office.com/watch/gwm4zu7tmtj8)             | Få innsikt i utgifter for de siste 12 kvartalene over de siste tre årene.                                                                                                                                                                                                                                   |
| [Gjennomgang av finansoverskrifter for JE og TB – Standard](https://mix.office.com/watch/1sw9fmtwgjb1f)            | Se en oversikt over saldoer og aktivitet for finansoverskriftene aktiva, gjeld, eierens egenkapital, omsetning, utgift, gevinst eller tap.                                                                                                                                                                           |
| [Resultatregnskap – Standard](https://mix.office.com/watch/sbuhgl5hzuhi)                                | Vis organisasjonens lønnsomhet for inneværende periode og hittil i år.                                                                                                                                                                                                                                   |
| [Finanstransaksjonsliste – Standard](https://mix.office.com/watch/19h9v2rmh48vy)                        | Vis detaljert saldoinformasjon for alle kontoer. Denne rapporten viser debet- og kreditsaldoer sammen med mer transaksjonsinformasjon som transaksjonsdato, journalnummer, bilag, posteringstype og sporingsnummer.                                                                            |
| [Forhold – Standard](https://mix.office.com/watch/b08hfc5h92me)                                          | Vis solvens, lønnsomhet og effektivitetsrate for organisasjonen for året.                                                                                                                                                                                                                           |
| [Opprulling 12 måneder Utgifter – Standard](https://mix.office.com/watch/iywod5qmqhz7)                       | Få innsikt i utgifter for hver av de siste 12 månedene. Disse 12 månedene kan strekke seg over mer enn ett regnskapsår.                                                                                                                                                                                                       |
| [Opprulling Kvartalsvis Resultatregnskap – Standard](https://mix.office.com/watch/1k4yl6a6oyxqc)               | Vis organisasjonens lønnsomhet kvartalsvis for det siste året samt hittil i år.                                                                                                                                                                                                                   |
| [Side ved side Balanse – Standard](https://mix.office.com/watch/zkgq0u7visw9)                      | Vis organisasjonens finansiell stilling for året. Denne rapporten viser aktiva, gjeld og egenkapital for aksjeeiere side ved side.                                                                                                                                                                                |
| [Råbalansesammendrag – Standard](https://mix.office.com/watch/1ewwgbpv0iwrl)                          | Vis saldoinformasjon for alle kontoer som har åpnings- og avslutningssaldo og debet- og kreditsaldoer, sammen med deres nettoforskjell.                                                                                                                                                                  |
| [Sammendrag Råbalanse Årlig – Standard](https://mix.office.com/watch/1ewwgbpv0iwrl)           | Vis saldoinformasjon for alle kontoer som har åpnings- og avslutningssaldo og debet- og kreditsaldoer, sammen med deres nettoforskjell for gjeldende og forrige år.                                                                                                                           |
| [Ukentlig Salg og rabatter – Standard](https://mix.office.com/watch/112ng0hy5de0j)                     | Få innsikt i salg og rabatter for hver uke i en måned. Denne rapporten inneholder totalt fire uker.                                                                                                                                                                                                              |
| [Budsjettmidler tilgjengelig - standard](https://mix.office.com/watch/15hcpezcbx7tv)                         | Vis en detaljert sammenligning av revidert budsjett, faktiske utgifter, budsjettreservasjoner og budsjettmidler tilgjengelig for alle kontoer                                                                                                                                                                                  |

## <a name="opening-financial-reports"></a>Åpne finansrapporter
Når du klikker **Finansrapportering**-menyen, vises listen over standard finansrapporter for firmaet. Deretter kan du åpne eller endre en rapport. Velg rapportnavnet for å åpne en av standardrapportene. Første gang en rapport åpnes, genereres den automatisk for forrige måned. Hvis du for eksempel åpner en rapport for første gang i august 2016, genereres rapporten for 31. juli 2016. Når en rapport åpnes, kan du begynne å utforske den ved å gå nedover i bestemte deler av data og endre rapportalternativer.

## <a name="creating-and-modifying-financial-reports"></a>Opprette og endre finansrapporter
Du kan opprette en ny rapport fra listen for finansrapporter eller endre en eksisterende rapport. Hvis du har de nødvendige tillatelsene, kan du opprette en ny finansrapport ved å klikke **Ny** i handlingsruten. Et rapportutforming-program lastes ned til enheten. Du kan deretter opprette den nye rapporten etter at rapportutformingen starter. Når du har lagret den nye rapporten, vises den i finansrapportlisten. Listen viser bare rapporter som er opprettet for firmaet som du bruker i Finance and Operations. Hvis du vil ha mer informasjon om prosessen med å opprette og endre finansrapporter i Finance and Operations, se disse [blogginnleggene](https://blogs.msdn.microsoft.com/dynamics_financial_reporting/tag/learning/) fra bloggen for Dynamics-finansrapportering. **Merk:** Datamaskinen som du laster ned klienten for rapportutforming på, må ha versjon 4.6.2 av Microsoft .NET Framework installert. Denne versjonen av Microsoft .NET Framework kan lastes ned og installeres fra [her](https://www.microsoft.com/en-us/download/details.aspx?id=53345). Hvis du bruker Chrome, må du installere et ClickOnce-tillegg for å kunne laste ned klienten for rapportutforming. Hvis du kjører i inkognitomodus, må du kontrollere at ClickOnce-tillegget er aktivert for inkognitomodus. Du kan også endre en rapport som vises i finansrapportlisten. Når området rundt rapportnavnet er merket, klikker du **Rediger** i handlingsruten. Rapportutformingsprogrammet starter.

<a name="see-also"></a>Se også
--------

[Vis finansrapporter](view-financial-reports.md)

[Blogg for Dynamics-finansrapportering](http://blogs.msdn.com/b/dynamics_financial_reporting/)




