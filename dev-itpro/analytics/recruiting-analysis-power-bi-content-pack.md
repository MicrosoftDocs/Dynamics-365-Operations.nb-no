---
title: "Rekruttering strømmen BI-innhold"
description: "Dette emnet beskriver Dynamics-365 for operasjoner - Rekruttering strømmen BI-innhold. Det forklarer hvordan du kan få tilgang til rapporter som er inkludert i innhold pack, og gir informasjon om en datamodell og enheter som ble brukt til å lage innhold pack."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations
ms.custom: 263934
ms.assetid: 38e6827b-0819-473c-bc47-821a1ec482b8
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: d307733193b388149f83dd420cc7003edcf7749a
ms.lasthandoff: 03/31/2017


---

# <a name="recruiting-power-bi-content"></a>Rekruttering strømmen BI-innhold

Dette emnet beskriver Dynamics-365 for operasjoner - Rekruttering strømmen BI-innhold. Det forklarer hvordan du kan få tilgang til rapporter som er inkludert i innhold pack, og gir informasjon om en datamodell og enheter som ble brukt til å lage innhold pack.

<a name="accessing-the-content-pack"></a>Tilgang til innhold pack
--------------------------

Du kan finne innhold pack for Rekruttering i delte aktiva biblioteket i Microsoft Dynamics Lifecycle tjenester (LCS). Hvis du vil ha mer informasjon om hvordan du laster ned innhold pack og koble den til din Microsoft Dynamics-365 for operasjoner data, se [strømmen BI-innhold i LCS fra Microsoft og partnere på](power-bi-content-microsoft-partners.md).

## <a name="reports-that-are-included-in-the-content-pack"></a>Rapporter som er inkludert i innhold pack
Når du har koblet innhold pack til din Dynamics 365 for operasjoner data, vise rapportene organisasjonens data. Hvis du aldri har brukt Microsoft Power BI før, kan du lære mer om det på den [veiledende læring side for strøm BI](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). Rapporter som er inkludert i innhold pack har både diagrammer og tabeller som inneholder tilleggsinformasjon. Tabellen nedenfor beskriver rapportene.

| Rapporter                       | Innhold                                                                                               |
|------------------------------|--------------------------------------------------------------------------------------------------------|
| Søkeren analyse           | Søkere med jobben, søker kilder, søkere etter lokasjon og totalt antall søkere           |
| Søkerstatus             | Søkere av typen og statusen og Søkerstatus                                                    |
| Søkeren demografi       | Søkere av alder og kjønn og søkere ved utdanningsnivå og status                             |
| Rekruttering analyse          | NET ansettelse forholdet, gjennomsnittlig antall dager for å ansette, prosent av dårlig ansettelser og Rekruttering kostnader                    |
| Rekrutteringsprosjekter analyse av prosjektet | Flere rekrutteringsprosjekter, åpninger av rekrutteringsprosjektet og søkere etter rekrutteringsprosjekt |

Du kan filtrere diagrammer og fliser på disse rapportene og feste diagrammer og fliser på instrumentbordet. Hvis du vil ha mer informasjon om hvordan du filter og PIN-koden i strømmen BI, se [opprette og konfigurere en instrumentbord](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Forstå datamodellen og enheter
Dynamics 365 for operasjoner data brukes til å fylle ut rapporter i Rekruttering innhold pack. Tabellen nedenfor viser enhetene som innhold pack er basert på.

| Enhet                          | Innhold                                                         | Relasjoner med andre enheter                                                                                                                                                                                                                 |
|---------------------------------|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Rekruttering\_søkeren           | Søkere, ansatt søkere, forholdet mellom netto ansettelse og kostnader          | Rekruttering\_ApplicantName Rekruttering\_Company Rekruttering\_CalendarOffset Recuriting\_dato Rekruttering\_GeographicLocation Rekruttering\_demografi Rekruttering\_jobben Rekruttering\_Media Rekruttering\_RecruitmentProject                                |
| Rekruttering\_ApplicantName       | Søkeren fornavn, Etternavn og fullt navn                   | Rekruttering\_søker Rekruttering\_EmployedApplicant Rekruttering\_TerminatedApplicant                                                                                                                                                               |
| Rekruttering\_CalendarOffset      | Kalenderen forskyvninger stykke rapporter                                | Rekruttering\_søker Rekruttering\_EmployedApplicant Rekruttering\_TerminatedApplicant                                                                                                                                                               |
| Rekruttering\_firma             | Selskaper til å filtrere rapporter med                                   | Rekruttering\_søker Rekruttering\_EmployedApplicant Rekruttering\_TerminatedApplicant                                                                                                                                                               |
| Rekruttering\_dato                | Dager, uker, måneder og år                                   | Rekruttering\_søker Rekruttering\_EmployedApplicant Rekruttering\_TerminatedApplicant                                                                                                                                                               |
| Rekruttering\_demografi        | Fødselsdato, kjønn, etnisk opprinnelse og ekteskapelig status         | Rekruttering\_søker Rekruttering\_EmployedApplicant Rekruttering\_TerminatedApplicant                                                                                                                                                               |
| Rekruttering\_EmployedApplicant   | Søkeren, ytelse, startdato og Søkertype           | Rekruttering\_Company Rekruttering\_CalendarOffset Rekruttering\_dato Rekruttering\_GeographicLocation Rekruttering\_ApplicantName Rekruttering\_ansettelse-Rekruttering\_ytelse Rekruttering\_jobben Rekruttering\_Media Rekruttering\_RecruitmentProject          |
| Rekruttering\_ansettelse          | Startdato, sluttdato og dato for overgang                        | Rekruttering\_søker Rekruttering\_EmployedApplicant Rekruttering\_TerminatedApplicant                                                                                                                                                               |
| Rekruttering\_GeographicLocation  | By, fylke, postnummer-koden og delstat / region                 | Rekruttering\_søker Rekruttering\_EmployedApplicant Rekruttering\_TerminatedApplicant                                                                                                                                                               |
| Rekruttering\_jobb                 | Funksjons-, type- og tittel                                        | Rekruttering\_søker Rekruttering\_EmployedApplicant Rekruttering\_TerminatedApplicant                                                                                                                                                               |
| Rekruttering\_Media               | Kilden for søkere                                             | Rekruttering\_søker Rekruttering\_EmployedApplicant Rekruttering\_TerminatedApplicant                                                                                                                                                               |
| Rekruttering\_ytelse         | Vurdering, beskrivelse og vurderingsmodellen                            | Rekruttering\_søker Rekruttering\_EmployedApplicant Rekruttering\_TerminatedApplicant                                                                                                                                                               |
| Rekruttering\_RecruitmentProject  | Prosjektbeskrivelse, prosjektstatus og åpninger                | Rekruttering\_søker Rekruttering\_EmployedApplicant Rekruttering\_TerminatedApplicant                                                                                                                                                               |
| Rekruttering\_TerminatedApplicant | Avsluttet søkere, årsak, ytelse og Sluttet dato | Rekruttering\_Company Rekruttering\_CalendarOffset Rekruttering\_dato Rekruttering\_GeographicLocation Rekruttering\_ytelse Rekruttering\_demografi Rekruttering\_ansettelse-Rekruttering\_Media Rekruttering\_RecruitmentProject Rekruttering\_ApplicantName |

Disse enhetene ble brukt til å opprette beregnede mål. Disse beregnet mål brukes deretter til å beregne viktige ytelsesindikatorer (KPIer) og rapporter som brukes i content pack. Hvis du vil ta med flere beregninger i rapporter og instrumentbord, kan du laste ned og endre filen Recruiting.pbix fra LCS. Denne filen er standard datamodellen som ble brukt til å opprette innhold pack. Når du har gjort endringene, kan du opprette en organisatorisk innholdspakken og instrumentbord som inneholder informasjon som du har lagt til.

## <a name="additional-resources"></a>Tilleggsressurser
Her er noen nyttige koblinger som er knyttet til enheter og oppretting av Power BI-innhold:

-   [Dataenheter](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)
-   [Opprette innholdspakker for organisasjonen](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Datamodellering med Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Legge til Power BI-fliser i arbeidsområder](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/06/pinning-power-bi-reports-to-dynamics-ax-client/)



