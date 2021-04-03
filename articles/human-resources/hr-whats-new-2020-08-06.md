---
title: Hva er nytt eller endret i Dynamics 365 Human Resources (06. august 2020)
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Human Resources for 6. august 2020.
author: andreabichsel
manager: tfehr
ms.date: 08/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-08-06
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 235af2d4d10687e9d7d7676c29c95428eab99b0a
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/17/2021
ms.locfileid: "5467729"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-august-06-2020"></a>Hva er nytt eller endret i Dynamics 365 Human Resources (06. august 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dette emnet beskriver funksjoner som enten er nye eller endret i Dynamics 365 Human Resources. Endringer gjelder for Build-nummeret 8.1.3444. Tallene i parentes i noen overskrifter refererer til støttenumre i LCS.

## <a name="platform-update-1001236-is-now-available"></a>Platform Update 10.0.12(36) er nå tilgjengelig

Hvis du vil ha mer informasjon, kan du se [Platformoppdateringer for versjon 10.0.12 av Finance and Operations-apper (august 2020)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-update-10-0-12).

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a>Data Management Framework (DMF)-enheter for Fordelsbehandling
 
Enheter for fordelsstyring frigis. DMF-enheter gjør det mulig å importere og eksportere data slik at du enkelt kan konfigurere fordelsbehandling. En mal for fordelsbehandling vil være tilgjengelig for å flytte data. Malen eksporterer og importerer data på en sekvensiell måte for å respektere dataavhengigheter. Hvis du vil ha mer informasjon, kan du se:

- [Støtte for DMF-enheter](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/dmf-entity-support) i Dynamics 365-planen for lanseringsbølge 1 i 2020
- [Oversikt over databehandling](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities-data-packages)


## <a name="claire-creates-a-workflow-for-buying-and-selling-leave-requests-446557"></a>Claire oppretter en arbeidsflyt for innkjøp og salg av permisjonsforespørsler (446557)

Hvis du vil ha mer informasjon, kan du se:

- [Tillate ansatte å kjøpe og selge](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/allow-employees-buy-sell-leave) i Dynamics 365-planen for lanseringsbølge 2 i 2020
- [Administrere policyer for kjøp og salg av permisjon](https://docs.microsoft.com/dynamics365/human-resources/hr-leave-and-absence-manage-buy-and-sell-leave-policies)
- [Kjøp og selg permisjon](https://docs.microsoft.com/dynamics365/human-resources/hr-employee-self-service-buy-sell-leave)


## <a name="worker-postal-addresses-v2-entity-has-access-across-legal-entities-with-restricted-access-459126"></a>Postadresser for arbeidere v2-enheten har tilgang på tvers av juridiske enheter med begrenset tilgang (459126)

Med denne endringen begrenser enheten **Postadresse for arbeider V2** basert på tilgangen for den juridiske enheten som er angitt for brukeren.

## <a name="workflow-email-hyperlink-fails-to-open-relevant-reviews-437398"></a>Hyperkobling i e-post om arbeidsflyt kan ikke åpne relevante gjennomganger (437398)

Når du bruker plassholderen til å åpne en ytelsesgjennomgang i gjennomgangsarbeidsflyten, vil hyperkoblingen som ble generert i e-postmeldingen, nå åpne den valgte posten.

## <a name="new-entities-for-buying-and-selling-leave-473180"></a>Nye enheter for kjøp og salg av permisjon (473180)

Enheter for dataadministrasjonsrammeverket er nå tilgjengelige for kjøp og salg av permisjon. Hvis du vil ha mer informasjon, kan du se [Oversikt over databehandling](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities-data-packages).

## <a name="when-viewing-record-information-and-using-advanced-filters-a-user-could-gain-access-to-other-employees-records-472490"></a>Når du viser postinformasjon og bruker avanserte filtre, kan en bruker få tilgang til andre ansattes poster (472490)

Med denne endringen kan brukere av selvbetjening for ansatte bare få tilgang til sine egne poster. Visning av postinformasjon mens du endrer filtreringsalternativet, viser ikke lenger tilleggsdata.

## <a name="personnel-management-analytics-include-exited-worker-records-382893"></a>Analyse i Personaladministrasjon inkluderer poster for arbeidere som har sluttet (382893)

Med denne versjonen inkluderer analyse i Personaladministrasjon nå bare aktive arbeidere. 
 
## <a name="unable-to-process-a-merit-increase-for-an-employee-473125"></a>Kan ikke behandle en personlig tilleggsøkning for en ansatt (473125)

Denne endringen gjør at du kan angi personlig tilleggsøkning når du endrer gyldighetsdatoen for den nye personlige tilleggsøkningen.

## <a name="review-workflow-can-be-started-more-than-once-467541"></a>Gjennomgangsarbeidsflyt kan startes mer enn én gang (467541)

Med denne endringen kan du bare starte arbeidsflyten for ytelsesgjennomgang én gang. Statusen for prosjektlederen viser ikke lenger alternativet for å starte gjennomgangen.

## <a name="leave-request-work-flow-ends-in-error-when-canceling-an-approved-leave-request-472063"></a>Arbeidsflyten for permisjonsforespørsel avsluttes med en feil under avbrudd av en godkjent permisjonsforespørsel (472063)

Når du avbryter en godkjent permisjonsforespørsel i denne versjonen, vil ikke lenger statusen til forespørselen være godkjent, og arbeidsflyten vil fortsette.

## <a name="system-suggests-exited-workers-when-creating-a-new-review-form-the-template-460624"></a>Systemet foreslår utgåtte arbeidere under oppretting av en ny gjennomgang fra malen (460624)

Med denne endringen er ikke avsluttede arbeidere lenger tilgjengelige når du oppretter nye gjennomganger fra en mal. Du kan ikke opprette gjennomganger for ansatte som er utenfor ansettelsesdatoene.

## <a name="position-hierarchy-circular-reference-detection-415879"></a>Registrering av sirkelreferanse i stillingshierarki (415879)

Med denne endringen er oppdaging av sirkelreferanse i stillingshierarki begrenset til ett enkelt tidspunkt. Du kan kjøre oppdaging av sirkelreferanse for ulike datoer for å kontrollere at rapporteringsstrukturen ikke har noen sirkelreferanser.

## <a name="buy-and-sell-leave"></a>Kjøp og selg permisjon 

Noen organisasjoner tilbyr en fordel som gjør det mulig for ansatte å kjøpe eller selge permisjon. Denne prosessen behandles ofte manuelt. Denne funksjonen automatiserer behandling av policyer og forespørsler for personalavdelingen. Den strømlinjeformer permisjonsstyringsprosessen og bidrar til å eliminere feil. Hvis du vil ha mer informasjon, kan du se:

- [Tillate ansatte å kjøpe og selge](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/allow-employees-buy-sell-leave) i Dynamics 365-planen for lanseringsbølge 2 i 2020
- [Administrere policyer for kjøp og salg av permisjon](https://docs.microsoft.com/dynamics365/human-resources/hr-leave-and-absence-manage-buy-and-sell-leave-policies)
- [Kjøp og selg permisjon](https://docs.microsoft.com/dynamics365/human-resources/hr-employee-self-service-buy-sell-leave)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a>Permisjonsavsetning for ett enkelt firma eller én enkelt plan

Kunder kan behandle avsetninger for ett enkelt firma eller en enkel permisjons- og fraværsplan. Denne muligheten gir klarhet for avsetningsprosessen for kunder med forskjellige policyer for fraværsår eller permisjonsavsetning. Hvis du vil ha mer informasjon, se [Avsett permisjon per firma eller per permisjonsplan](hr-leave-and-absence-accrue.md).

## <a name="add-attachments-to-time-off-requests"></a>Legge til vedlegg i fraværsforespørsler

Muligheten til å legge til vedlegg i godkjente permisjonsforespørsler er viktig i det gjeldende COVID-19-miljøet. Ansatte kan nå legge til disse vedleggene. De har også mer innsikt i hvordan det gjøres oppdateringer for permisjonsforespørsler. Hvis du vil ha mer informasjon, kan du se [Legge til et vedlegg i en eksisterende forespørsel](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).

## <a name="add-reason-code-to-accrual-suspensions"></a>Legge til årsakskode for avsetningsuspensjoner 

Årsakskoder er lagt til i avsetningssuspensjonen.

## <a name="carry-forward-rules"></a>Overføringsregler 

Du kan angi en type overføringspermisjon for overføringssaldoer der overføringsjusteringer overføres. Hvis en ansatt for eksempel overfører 10 dager, kan du velge en annen permisjonstype for disse 10 dagene. Hvis du vil ha mer informasjon, kan du se [Konfigurere permisjons- og fraværstyper](hr-leave-and-absence-types.md).

## <a name="suspend-leave-accrual-for-specified-leave-types"></a>Avbryte permisjonsavsetning for angitte permisjonstyper

Du kan opprette en regel for å utsette permisjonsavsetninger for ansatte med permisjonsforespørsler som er angitt for fravær som ikke betales. Fravær som ikke betales, kan være en type, men behøver ikke å være det. Du kan stoppe enhver permisjon basert på en annen permisjonstype.

## <a name="in-preview"></a>I forhåndsvisning

### <a name="mandatory-fields"></a>Obligatorisk felt

Du kan gjøre felt obligatoriske ved hjelp av tilpasningsfunksjonene i Human Resources. Denne funksjonen krever **Lagrede visninger**. Hvis du vil ha mer informasjon om lagrede visninger, kan du se:

- [Lagrede visninger – generell tilgjengelighet](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/finance-operations/finance-operations-crossapp-capabilities/saved-views--general-availability) i Dynamics 365-planen for lanseringsbølge 2 i 2020
- [Bygge skjemaer som benytter lagrede visninger fullt ut](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/user-interface/understanding-saved-views)

### <a name="human-resources-application-in-teams"></a>Human Resources-søknad i Teams

Ansatte kan se og be om fravær fra jobb i Microsoft Teams. De kan kommunisere med en robot for å opprette permisjonsforespørsler. Hvis du vil ha mer informasjon, kan du se:

- [Ansattopplevelsen fro permisjon og fravær i Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) i Dynamics 365-planen for lanseringsbølge 1 i 2020
- [Human Resources-app i Teams](https://go.microsoft.com/fwlink/?linkid=2127841)

### <a name="dmf-entity-available-for-accrual-suspensions"></a>DMF-enhet tilgjengelig for avsetningssuspensjoner

En DMF-enhet er nå tilgjengelig for avsetningssuspensjoner.

## <a name="coming-soon"></a>Kommer snart

## <a name="checklist-entities-included-in-dataverse"></a>Sjekklisteenheter inkludert i Dataverse

Sjekklisteenheter for pålasting, avlasting, overføringer og forretningsprosesser vil snart være tilgjengelige i Dataverse.

## <a name="known-issues"></a>Kjente problemer

Arbeidsområdet **Funksjonsbehandling** viser kanskje funksjoner som er deaktivert som evalueringsfunksjonalitet, når de er generelt tilgjengelige. Nedenfor finner du en liste over generelt tilgjengelige funksjoner som viser feil status. 

1.  Fordelsbehandling
2.  Saksbehandling
3.  Databaselogging (revisjon)
4.  Permisjonsavsetning for ett firma eller én plan
5.  Avsetningssuspensjon for permisjon og fravær
6.  Årsakskode og kommentar for saldojustering
7.  Kjøp og selg permisjon
8.  Kalender for permisjon og fravær
9.  Overføringsregler for permisjon
10. Overvåking av permisjonsavsetning
11. Sletting av permisjonsavsetning
12. Avrunding av permisjonsavsetning
13. Konfigurer flere permisjonstyper på én permisjonsplan
14. Forbedringer for Oppdater fridager
15. Bruk den ansattes FTE for avsetninger
16. Visning av kompensasjon på tvers av firmaer
17. Skrive ut prestasjonsvurderinger
18. Helligdagskorrigeringer for permisjonsavsetning

## <a name="see-also"></a>Se også

[Nyheter eller endringer i Human Resources](hr-admin-whats-new.md)</br>
[Oversikt over lanseringsbølge 2 i 2019 for Dynamics 365 Human Resources](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Oppdatere prosess](hr-admin-setup-update-process.md)</br>
[Behandle funksjoner](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]