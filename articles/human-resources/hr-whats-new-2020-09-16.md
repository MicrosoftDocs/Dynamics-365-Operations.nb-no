---
title: Hva er nytt eller endret i Dynamics 365 Human Resources (16. september 2020)
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Human Resources for 16. september 2020.
author: jcart1106
manager: tfehr
ms.date: 09/16/2020
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
ms.author: jcart
ms.search.validFrom: 2020-09-16
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 74a87ddb4ed14042dd4e716ad64bc844a800a0a0
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/03/2021
ms.locfileid: "5113765"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-september-16-2020"></a>Hva er nytt eller endret i Dynamics 365 Human Resources (16. september 2020)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dette emnet beskriver funksjoner som enten er nye eller endret i Dynamics 365 Human Resources. Endringer gjelder for Build-nummeret 8.1.3557. Tallene i parentes ved siden av noen funksjoner refererer til støttenumre i Lifecycle Services (LCS).

## <a name="included-in-this-release"></a>Inkludert i denne versjonen

-  [Lagrede visninger – generell tilgjengelighet](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/finance-operations/finance-operations-crossapp-capabilities/saved-views--general-availability)<br>- Hvis du vil ha mer informasjon se [Lagrede visninger](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/saved-views). 

- Skjemaet **Stillingshandlinger** har et oppdatert dimensjonsrutenett og en ny dialog (469495).

- Hvis du setter **Begrens tilgang til arbeiderinformasjon** til Ja i **Avansert tilgang** i **Delte parametere for personaladministrasjon**, viser fordelsskjemaer nå bare de riktige arbeiderne (393384).

- Nye alternativer for kalendergenerering i **WorkCalendar**-enheten (477055):<br>- Standard sluttidspunkt<br>-    Standard starttidspunkt<br>-  Er fredag arbeidsdag<br>-  Er mandag arbeidsdag<br>-  Er lørdag arbeidsdag<br>- Er søndag arbeidsdag<br>- Er torsdag arbeidsdag<br>- Er tirsdag arbeidsdag<br>- Er onsdag arbeidsdag<br>- ID for helligdag i arbeidskalender

- Enheten **LeaveBankTransactionV1** inneholder nå årsakskoden (477823).

- Du kan nå lagre oppgaveopptak (492923).

- Data er nå publisert fra **HCMWorkerContactEntity** (427620).

- Hurtigfanen **Kompensasjon** vises nå for arbeidertypen oppdragstakeren i skjemaet **Arbeiderhandlinger** (482494).

- Feltene **Nivå** og **Plan** er nå obligatoriske hvis du angir **Fast kompensasjon**. En feilmelding vises hvis du lar disse feltene stå tomme (482497).

- Feltet **Plantype** i **Fordeler** er nå en rullegardinliste (488768).

- Systemadministratorer mottar nå et varsel hvis et egendefinert felt slettes fra Human Resources (481408).

- Under avslutningsprosessen for den ansatte fungerer Human Resources som forventet og endrer ikke det valgte firmaet etter å ha blitt låst (479877). 

- Ledere kan ikke lenger legge til en tallkolonne via egen tilpasning (485317).

- Ledere kan ikke lenger fjerne dataområdefilteret fra ID-numre som utløper (485321).

- Når feltet **Rapporterer til** er tomt, vises stillingsdetaljene fremdeles ved peking over plasseringen (433328).

- Ansatte kan nå vise fordelsplaninformasjon i Ansattselvbetjening (481676).

- Ansatte kan nå se alle registrerte kurs (429048).

- Nå kan du begrense visningsalternativene for siden **Profesjonelle sertifikater**. Du kan begrense visningsalternativene til den gjeldende juridiske enheten, etter arbeiderstatus og etter arbeidertype (451501). 


## <a name="in-preview"></a>I forhåndsvisning

### <a name="human-resources-app-in-teams"></a>Human Resources-app i Teams

Ansatte kan se og be om fravær fra jobb i Microsoft Teams. De kan kommunisere med en robot for å opprette permisjonsforespørsler. Hvis du vil ha mer informasjon, kan du se:

- [Ansattopplevelsen fro permisjon og fravær i Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) i Dynamics 365-planen for lanseringsbølge 1 i 2020
- [Human Resources-app i Teams](https://go.microsoft.com/fwlink/?linkid=2127841) i Human Resources-dokumentasjon

### <a name="human-resources-app-in-teams-preview-features"></a>Human Resources-app i Teams-evalueringsfunksjoner
 
-  **Varslinger**: Innsendere og godkjennere av fritidsforespørsler vil bli varslet i Human Resources-appen i Teams. Godkjennere kan godkjenne eller avslå forespørsler om fritid. Innsendere vil bli varslet hvis forespørselen ble godkjent eller avvist. Hvis du vil ha mer informasjon, kan du se:
   - [Ansattopplevelsen fro permisjon og fravær i Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) i Dynamics 365-planen for lanseringsbølge 2 i 2020
   - [Aktivere varslinger for Human Resources-appen i Teams](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-teams-leave-app#enable-notifications-for-the-human-resources-app-in-teams) i Human Resources-dokumentasjon
   - [Aktivere eller deaktivere Teams-varslinger for enkeltstående brukere](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-teams-leave-app#turn-teams-notifications-on-or-off-for-individual-users) i Human Resources-dokumentasjonen
   - [Teams-varslinger](https://docs.microsoft.com/dynamics365/human-resources/hr-teams-leave-app#teams-notifications) i Human Resources-dokumentasjonen
   - [Vise permisjonskalenderen for Teams](https://docs.microsoft.com/dynamics365/human-resources/hr-teams-leave-app#view-your-teams-leave-calendar) i Human Resources-dokumentasjonen
 
- **Fritidskalender for leder**: Ledere kan se godkjent og ventende fritid for direkte underordnede i en kalendervisning. Denne visningen gir en enkel forståelse av når teammedlemmene er borte fra arbeid. Hvis du vil ha mer informasjon, kan du se:
   - [Ansattopplevelsen fro permisjon og fravær i Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) i Dynamics 365-planen for lanseringsbølge 2 i 2020
   - [Vise permisjonskalenderen for Teams](https://docs.microsoft.com/dynamics365/human-resources/hr-teams-leave-app#view-your-teams-leave-calendar) i Human Resources-dokumentasjonen

### <a name="configuration-option-to-position-work-items-assigned-to-me-list-477004"></a>Konfigurasjonsalternativ for å plassere listen Arbeidselementer som er tilordnet til meg (477004)

Et nytt alternativ er nå tilgjengelig for å plassere listen **Arbeidselementer som er tilordnet til meg** i høyre kolonne på instrumentbordet. Med denne endringen vises alle arbeidselementer og gjøremålslister i samme område. Aktiver denne funksjonaliteten ved å aktivere **Forhåndsvisning – forbedringer av arbeidsflytsopplevelse** i Funksjonsbehandling. Hvis du vil ha mer informasjon om å aktivere forhåndsversjonsfunksjoner, kan du se [Behandle funksjoner](hr-admin-manage-features.md).

Denne funksjonen fremmer også arbeidsflytalternativene som vises i personalhandlingsskjemaene. Arbeidsflytalternativer vises også over hurtigkategorien for handlingen for rask tilgang. Hvis du vil ha mer informasjon, kan du se: 

- [Forbedringer i arbeidsflyten for organisasjons- og personalstyring](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) i Dynamics 365 2020-frigivelsesbølge 2-planen

![Arbeidselementer som er tilordnet til meg](./media/hr-workflow-work-items-assigned-to-me.png)

![Hurtigtilgang til arbeidsflytelementer](./media/hr-workflow-quick-access.png)

### <a name="leave-and-absence-calendar"></a>Kalender for permisjon og fravær

Denne versjonen inneholder flere kalenderalternativer for permisjons- og fraværskalendere. Hvis du vil ha mer informasjon, kan du se [Vise team- og firmakalendere](https://docs.microsoft.com/dynamics365/human-resources/hr-employee-self-service-calendar).

## <a name="coming-soon"></a>Kommer snart

### <a name="checklist-entities-included-in-dataverse"></a>Sjekklisteenheter inkludert i Dataverse

Sjekklisteenheter for pålasting, avlasting, overføringer og forretningsprosesser vil snart være tilgjengelige i Dataverse.

### <a name="benefits-management-reason-codes"></a>Årsakskoder for fordelsstyring

Årsakskoder for fordelsstyring kombineres snart med eksisterende årsakskoder i Human Resources. Hvis du har opprettet årsakskoder i fordelsstyringen som er over 15 tegn, må du endre navnet på årsakskoden i skjemaet **Årsakskoder** for Fordelsbehandling slik at det består av 15 tegn eller mindre. Når du har oppdatert navnet, vises årsakskoden under det eksisterende årsakskodeskjemaet i Personaladministrasjon. Denne endringen vil være tilgjengelig i fremtiden, og vil ikke påvirke eksisterende funksjonalitet.

## <a name="see-also"></a>Se også

[Nyheter eller endringer i Human Resources](hr-admin-whats-new.md)</br>
[Oversikt over lanseringsbølge 2 i 2019 for Dynamics 365 Human Resources](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Oppdatere prosess](hr-admin-setup-update-process.md)</br>
[Behandle funksjoner](hr-admin-manage-features.md)
