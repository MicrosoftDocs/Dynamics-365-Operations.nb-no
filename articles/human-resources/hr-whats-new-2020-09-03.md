---
title: Hva er nytt eller endret i Dynamics 365 Human Resources (03. september 2020)
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Human Resources for 3. september 2020.
author: andreabichsel
ms.date: 09/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-09-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 10978d8843e7bce2800d62b63e58152569be9631
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/13/2021
ms.locfileid: "5891775"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-september-3-2020"></a>Hva er nytt eller endret i Dynamics 365 Human Resources (3. september 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dette emnet beskriver funksjoner som enten er nye eller endret i Dynamics 365 Human Resources. Endringer gjelder for Build-nummeret 8.1.3504. Tallene i parentes i noen overskrifter refererer til støttenumre i Lifecycle Services (LCS).

Hvis du vil ha mer informasjon om kommende funksjoner i Human Resources, kan du se [Oversikt over lanseringsbølge 2 i 2019 for Dynamics 365 Human Resources](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/). Hvis du vil ha mer informasjon om oppdateringsprosessen for Human Resources, kan du se [Oppdatere prosess](hr-admin-setup-update-process.md).

## <a name="in-this-release"></a>I denne versjonen

### <a name="new-default-financial-dimensions-grid-and-dialog-pattern-throughout-human-resources-469495"></a>Nytt standard rutenett for finansdimensjoner og dialogmønster i hele Human Resources (469495)

Det nye mønsteret for finansdimensjoner er nå tilgjengelig i følgende områder:

- Stillingshandlinger (Skjema: **HcmPositionActionDetail**)
- Inntektskoder for lønn (Skjema: **PayrollEarningCode**)

### <a name="entries-dont-appear-in-company-leave-calendar-if-leave-and-absence-calendar-enhancements-arent-enabled-484406"></a>Oppføringer vises ikke i firmaets permisjonskalender hvis forbedringer i permisjons- og fraværskalenderen ikke er aktivert (484406)

Denne versjonen retter opp et problem der permisjonsoppføringer ikke vises i firmaets permisjonskalender. Dette problemet oppstår bare når alternativet **Forbedringer til permisjons- og fraværskalender** ikke er aktivert i Funksjonsbehandling.

### <a name="benefitplanemployeeentity-issue-467597"></a>BenefitPlanEmployeeEntity-problem (467597)

Denne versjonen retter opp et problem med enheten **BenefitsPlanEmployee**. Ved import av arbeiderregistreringer angis **Dekningskode** og **Kode for plantype** er nå riktig angitt. Dette problemet førte til at ansattes fordelsplaner ble vist feil i skjemaene **Fordelsplaner for arbeider** og **Åpen registrering** i Ansattselvbetjening.

### <a name="electronic-file-1094-c-output-missing-letter-in-xml-435190"></a>Elektronisk filutskrift av 1094-C mangler bokstav i XML (435190)

Denne endringen retter opp et problem der utdatafilen 1094-C mangler et nødvendig tegn under sending til IRS.

### <a name="employee-variable-compensation-table-mapped-to-fixed-compensation-form-476117"></a>Variabel kompensasjonstabell for ansatt tilordnet til skjema for fast kompensasjon (476117)

Denne endringen justerer de faste kompensasjonsfeltene med skjemaet for fast kompensasjon. Feltene for variabel kompensasjon er nå bare tilgjengelige med skjemaet for variabel kompensasjon.

### <a name="leave-requests-allowed-before-enrollment-if-that-leave-type-has-a-negative-minimum-balance-469917"></a>Permisjonsforespørsler tillatt før registrering hvis permisjonstypen har en negativ minimumssaldo (469917)

Denne endringen hindrer at du angir permisjonsforespørsler før de registreres i planen, selv om registreringen har en negativ minimumssaldo. Du kan bare angi eller sende forespørsler når planen er aktiv.

### <a name="document-templates-dont-download-457279"></a>Dokumentmaler blir ikke lastet ned (457279)

Med denne endringen kan du nå laste ned alle dokumentmaler. 

### <a name="data-displays-as-column-headers-instead-of-rows-for-the-pay-rate-field-in-the-compensation-plan-report-476077"></a>Data vises som kolonneoverskrifter i stedet for rader for feltet Lønnssats i kompensasjonsplanrapporten (476077)

Analyserapporten viser nå den riktige informasjonen for **Lønnssats**.

## <a name="in-preview"></a>I forhåndsvisning

### <a name="human-resources-application-in-teams"></a>Human Resources-søknad i Teams

Ansatte kan se og be om fravær fra jobb i Microsoft Teams. De kan kommunisere med en robot for å opprette permisjonsforespørsler. Hvis du vil ha mer informasjon, kan du se:

- [Ansattopplevelsen fro permisjon og fravær i Microsoft Teams](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) i Dynamics 365-planen for lanseringsbølge 1 i 2020
- [Human Resources-app i Teams](./hr-admin-teams-leave-app.md) i Human Resources-dokumentasjon

### <a name="human-resources-app-in-teams-preview-features"></a>Human Resources-app i Teams-evalueringsfunksjoner
 
-  **Varslinger**: Innsendere og godkjennere av fritidsforespørsler vil bli varslet i Human Resources-appen i Teams. Godkjennere vil kunne godkjenne eller avslå forespørsler om fritid. Innsendere vil bli varslet hvis forespørselen ble godkjent eller avvist. Hvis du vil ha mer informasjon, kan du se:
   - [Ansattopplevelsen fro permisjon og fravær i Microsoft Teams](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) i Dynamics 365-planen for lanseringsbølge 2 i 2020
   - [Aktivere varslinger for Human Resources-appen i Teams](./hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) i Human Resources-dokumentasjon
   - [Aktivere eller deaktivere Teams-varslinger for enkeltstående brukere](./hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users) i Human Resources-dokumentasjonen
   - [Teams-varslinger](./hr-teams-leave-app.md#respond-to-teams-notifications) i Human Resources-dokumentasjonen
   - [Vise permisjonskalenderen for Teams](./hr-teams-leave-app.md#view-your-teams-leave-calendar) i Human Resources-dokumentasjonen
 
- **Fritidskalender for leder**: Ledere kan se godkjent og ventende fritid for direkte underordnede i en kalendervisning. Denne visningen gir en enkel forståelse av når teammedlemmene er borte fra arbeid. Hvis du vil ha mer informasjon, kan du se:
   - [Ansattopplevelsen fro permisjon og fravær i Microsoft Teams](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) i Dynamics 365-planen for lanseringsbølge 2 i 2020
   - [Vise permisjonskalenderen for Teams](./hr-teams-leave-app.md#view-your-teams-leave-calendar) i Human Resources-dokumentasjonen

### <a name="configuration-option-to-position-work-items-assigned-to-me-list-477004"></a>Konfigurasjonsalternativ for å plassere listen Arbeidselementer som er tilordnet til meg (477004)

Et nytt alternativ er nå tilgjengelig for å plassere listen **Arbeidselementer som er tilordnet til meg** i høyre kolonne på instrumentbordet. Med denne endringen vises alle arbeidselementer og gjøremålslister i samme område. Aktiver denne funksjonaliteten ved å aktivere **Forhåndsvisning – forbedringer av arbeidsflytsopplevelse** i Funksjonsbehandling. Hvis du vil ha mer informasjon om å aktivere forhåndsversjonsfunksjoner, kan du se [Behandle funksjoner](hr-admin-manage-features.md).

Denne funksjonen fremmer også arbeidsflytalternativene som vises i personalhandlingsskjemaene. Arbeidsflytalternativer vises også over hurtigkategorien for handlingen for rask tilgang. Hvis du vil ha mer informasjon, kan du se: 

- [Forbedringer i arbeidsflyten for organisasjons- og personalstyring](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) i Dynamics 365 2020-frigivelsesbølge 2-planen

![Arbeidselementer som er tilordnet til meg](./media/hr-workflow-work-items-assigned-to-me.png)

![Hurtigtilgang til arbeidsflytelementer](./media/hr-workflow-quick-access.png)

## <a name="coming-soon"></a>Kommer snart

### <a name="checklist-entities-included-in-dataverse"></a>Sjekklisteenheter inkludert i Dataverse

Sjekklisteenheter for pålasting, avlasting, overføringer og forretningsprosesser vil snart være tilgjengelige i Dataverse.

### <a name="benefits-management-reason-codes"></a>Årsakskoder for fordelsstyring

Årsakskoder for fordelsstyring kombineres snart med eksisterende årsakskoder i Human Resources. Hvis du har opprettet årsakskoder i fordelsstyringen som er over 15 tegn, må du endre navnet på årsakskoden i skjemaet **Årsakskoder** for Fordelsbehandling slik at det består av 15 tegn eller mindre. Når du har oppdatert navnet, vises årsakskoden under det eksisterende årsakskodeskjemaet i Personaladministrasjon. Denne endringen vil være tilgjengelig i fremtiden, og vil ikke påvirke eksisterende funksjoner.

## <a name="see-also"></a>Se også

[Nyheter eller endringer i Human Resources](hr-admin-whats-new.md)</br>
[Oversikt over lanseringsbølge 2 i 2019 for Dynamics 365 Human Resources](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Oppdatere prosess](hr-admin-setup-update-process.md)</br>
[Behandle funksjoner](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
