---
title: Recruiting-innhold for Power BI
description: "Dette emnet beskriver Dynamics 365 for Operations - Recruiting-innhold for Power BI. Det forklarer også hvordan du får tilgang til rapportene som er inkludert i innholdspakken, og inneholder informasjon om datamodellen og enhetene som brukes til å bygge innholdspakken."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations
ms.custom: 263934
ms.assetid: 38e6827b-0819-473c-bc47-821a1ec482b8
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 4b12a2c8983cf7bef770417f76df324293f06fb2
ms.contentlocale: nb-no
ms.lasthandoff: 05/25/2017


---

# <a name="recruiting-power-bi-content"></a>Recruiting-innhold for Power BI

[!include[banner](../includes/banner.md)]


Dette emnet beskriver Dynamics 365 for Operations - Recruiting-innhold for Power BI. Det forklarer også hvordan du får tilgang til rapportene som er inkludert i innholdspakken, og inneholder informasjon om datamodellen og enhetene som brukes til å bygge innholdspakken.

<a name="accessing-the-content-pack"></a>Tilgang til innholdspakken
--------------------------

Du kan finne Recruiting-innholdspakken i det delte aktivabiblioteket i Microsoft Dynamics Lifecycle Services (LCS). Hvis du vil ha mer informasjon om hvordan du laster ned innholdspakken og kobler den til Microsoft Dynamics 365 for Operations-data, kan du se [Power BI-innhold i LCS fra Microsoft og partnere](power-bi-content-microsoft-partners.md).

## <a name="reports-that-are-included-in-the-content-pack"></a>Rapporter som er inkludert i innholdspakken
Når du har knyttet innholdspakken til Dynamics 365 for Operations-dataene dine, viser rapportene organisasjonens data. Hvis du aldri har brukt Microsoft Power BI før, kan du finne ut mer på siden [Guided Learning for Power BI](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). Rapporter som er inkludert i innholdspakken, har både diagrammer og tabeller som inneholder tilleggsinformasjon. Tabellen nedenfor beskriver rapportene.

| Rapporter                       | Innhold                                                                                               |
|------------------------------|--------------------------------------------------------------------------------------------------------|
| Søkeranalyse           | Søkere etter jobb, søkerkilder og sted og totalt antall søkere           |
| Søkerstatus             | Søkere etter type, status og søkerstatus                                                    |
| Søkerdemografi       | Søkere etter alder, kjønn, utdanningsnivå og status                             |
| Rekrutteringsanalyse          | Netto ansettelsesforhold, gjennomsnittlig antall dager for å ansette, prosent av dårlige ansettelser og rekrutteringskostnader                    |
| Analyse for rekrutteringsprosjekt | Antall rekrutteringsprosjekter, stillinger etter rekrutteringsprosjekt og søkere etter rekrutteringsprosjekt |

Du kan filtrere diagrammer og fliser for disse rapportene, og festes dem på instrumentbordet. Hvis du vil ha mer informasjon om hvordan du filtrerer og fester i Power BI, kan du se [Opprette og konfigurere et instrumentbord](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Forstå datamodellen og enheter
Dynamics 365 for Operations-data brukes til å fylle ut rapporter i Rekruttering-innholdspakken. Tabellen nedenfor viser enhetene som innholdspakken er basert på.

| Enhet                          | Innhold                                                         | Relasjoner med andre enheter                                                                                                                                                                                                                 |
|---------------------------------|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Rekruttering\_Søker           | Søkere, ansatte søkere, netto ansettelsesforhold og kostnader          | Recruiting\_ApplicantName Recruiting\_Company Recruiting\_CalendarOffset Recuriting\_Date Recruiting\_GeographicLocation Recruiting\_Demographics Recruiting\_Job Recruiting\_Media Recruiting\_RecruitmentProject                                |
| Recruiting\_ApplicantName       | Søkerens fornavn, etternavn og fulle navn                   | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_CalendarOffset      | Kalenderforskyvninger for å dele opp rapporter                                | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_Company             | Selskaper til å filtrere rapporter etter                                   | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_Date                | Dager, uker, måneder og år.                                   | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_Demographics        | Fødselsdato, kjønn, etnisk opprinnelse og ekteskapelig status         | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_EmployedApplicant   | Søkeren, ytelse, startdato og søkertype           | Recruiting\_Company Recruiting\_CalendarOffset Recruiting\_Date Recruiting\_GeographicLocation Recruiting\_ApplicantName Recruiting\_Employment Recruiting\_Performance Recruiting\_Job Recruiting\_Media Recruiting\_RecruitmentProject          |
| Recruiting\_Employment          | Startdato, sluttdato og overgangsdato                        | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_GeographicLocation  | By, fylke, postnummer og delstat eller område                 | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_Job                 | Funksjon, type og tittel                                        | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_Media               | Søkerkilde                                             | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_Performance         | Vurdering, beskrivelse og vurderingsmodell                            | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_RecruitmentProject  | Prosjektbeskrivelse, prosjektstatus og stillinger                | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_TerminatedApplicant | Avsluttede søkere, årsak, ytelse og avslutningsdato | Recruiting\_Company Recruiting\_CalendarOffset Recruiting\_Date Recruiting\_GeographicLocation Recruiting\_Performance Recruiting\_Demographics Recruiting\_Employment Recruiting\_Media Recruiting\_RecruitmentProject Recruiting\_ApplicantName |

Disse enhetene ble brukt til å opprette beregnede mål. Disse beregnede målene brukes deretter til å beregne nøkkelytelsesindikatorene (KPI-ene) og rapportene som brukes i innholdspakken. Hvis du vil ta med flere beregninger i rapportene og instrumentbordet, kan du laste ned og endre filen Recruiting.pbix fra LCS. Denne filen er standarddatamodellen som ble brukt til å opprette innholdspakken. Når du har gjort endringene, kan du opprette en innholdspakke og et instrumentbord for organisasjonen som inneholder informasjonen du har lagt til.

## <a name="additional-resources"></a>Tilleggsressurser
Her er noen nyttige koblinger som er knyttet til enheter og oppretting av Power BI-innhold:

-   [Dataenheter](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)
-   [Opprette innholdspakker for organisasjonen](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Datamodellering med Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Legge til Power BI-fliser i arbeidsområder](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/06/pinning-power-bi-reports-to-dynamics-ax-client/)





