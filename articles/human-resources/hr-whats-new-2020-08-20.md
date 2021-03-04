---
title: Hva er nytt eller endret i Dynamics 365 Human Resources (20. august 2020)
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Human Resources for 20. august 2020.
author: Darinkramer
manager: AnnBe
ms.date: 8/20/2020
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
ms.author: dkrame
ms.search.validFrom: 2020-08-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 46dadb8834195c5dd06cd1c56d79324def7d9f2d
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/17/2020
ms.locfileid: "4527487"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-august-20-2020"></a>Hva er nytt eller endret i Dynamics 365 Human Resources (20. august 2020)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dette emnet beskriver funksjoner som enten er nye eller endret i Dynamics 365 Human Resources. Endringer gjelder for Build-nummeret 8.1.3478. Tallene i parentes i noen overskrifter refererer til støttenumre i Lifecycle Services (LCS).

## <a name="show-upcoming-and-pending-leave-of-absence-information-to-cards-in-people-workspace"></a>Vise informasjon om kommende og ventende permisjon i Personer-arbeidsområdet

Alternativene for ventende og kommende permisjonsforespørsler er nå tilgjengelig på permisjons- og fraværskortene i **Personer**-arbeidsområdet.

## <a name="private-field-isnt-yes-by-default-for-employee-role-in-employee-self-service-477106"></a>Privat-feltet er ikke Ja som standard for Ansatt-rolle i Ansattselvbetjening (477106)

Feltet **Privat** går nå som standard til **Ja** når ansatte legger inn nye adresseposter via **Personlig informasjon**-siden i Ansattselvbetjening. 

## <a name="candidates-to-hire-fasttab-in-personnel-management-shows-an-incorrect-count-of-candidates-470110"></a>Kandidater til hurtigfanen for ansettelse i Personaladministrasjon viser feil antall kandidater (470110)

Siden **Personaladministrasjon** viser nå antall kandidater som skal ansettes, på riktig måte. 

## <a name="cant-enter-sickness-for-terminated-employee-when-accrual-is-set-to-zero-446195"></a>Kan ikke angi sykdom for fratrådt ansatt når avsetning er satt til null (446195)

Permisjonstransaksjoner er nå tillatt for fratrådte ansatte i fremtiden, og avsetningen er satt til null. Permisjonstransaksjoner kan angis inntil avslutningsdatoen for den ansatte. 

## <a name="adding-custom-fields-to-the-new-worker-form-disables-the-fields-in-the-action-pane-for-manage-leave-473314"></a>Når du legger til egendefinerte felt i det nye skjemaet Arbeider, deaktiveres feltene i handlingsruten for Administrer permisjon (473314)

Alternativer for handlingsrute i skjemaet **Arbeider** i **Administrer permisjon** vil ikke lenger deaktiveres hvis egendefinerte felt er lagt til i skjemaet **Arbeider**.

## <a name="making-the-leave-comment-field-mandatory-allows-a-leave-request-to-be-submitted-when-no-comment-is-entered-473543"></a>Hvis du gjør permisjonskommentarfeltet obligatorisk, er det mulig å sende en permisjonsforespørsel hvis det ikke er angitt en merknad (473543)

Merknadsfelt kan nå være obligatoriske, og permisjonsforespørsler tar høyde for denne innstillingen. Obligatoriske felt er en evalueringsfunksjonalitet.

### <a name="dmf-entity-available-for-accrual-suspensions"></a>DMF-enhet tilgjengelig for avsetningssuspensjoner

En DMF-enhet er nå tilgjengelig for avsetningssuspensjoner.

## <a name="in-preview"></a>I forhåndsvisning

### <a name="mandatory-fields"></a>Obligatorisk felt

Du kan gjøre felt obligatoriske ved hjelp av tilpasningsfunksjonene i Human Resources. Denne funksjonen krever **Lagrede visninger**. Hvis du vil ha mer informasjon om lagrede visninger, kan du se:

- [Lagrede visninger – generell tilgjengelighet](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/finance-operations/finance-operations-crossapp-capabilities/saved-views--general-availability) i Dynamics 365-planen for lanseringsbølge 2 i 2020
- [Bygge skjemaer som benytter lagrede visninger fullt ut](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/user-interface/understanding-saved-views)

### <a name="human-resources-application-in-teams"></a>Human Resources-søknad i Teams

Ansatte kan se og be om fravær fra jobb i Microsoft Teams. De kan kommunisere med en robot for å opprette permisjonsforespørsler. Hvis du vil ha mer informasjon, kan du se:

- [Ansattopplevelsen fro permisjon og fravær i Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) i Dynamics 365-planen for lanseringsbølge 1 i 2020
- [Human Resources-app i Teams](https://go.microsoft.com/fwlink/?linkid=2127841)

## <a name="coming-soon"></a>Kommer snart

### <a name="human-resources-app-in-teams-preview-features"></a>Human Resources-app i Teams-evalueringsfunksjoner
 
-  **Varslinger**: Innsendere og godkjennere av fritidsforespørsler vil bli varslet i Human Resources-appen i Teams. Godkjennere vil kunne godkjenne eller avslå forespørsler om fritid, og innsendere vil bli varslet hvis forespørselen blir godkjent eller nektet.
 
- **Fritidskalender for leder**: Ledere kan se godkjent og ventende fritid for direkte underordnede i en kalendervisning. Denne visningen gir en enkel forståelse av når teammedlemmene er borte fra arbeid.

### <a name="checklist-entities-included-in-common-data-service"></a>Sjekklisteenheter inkludert i Common Data Service

Sjekklisteenheter for pålasting, avlasting, overføringer og forretningsprosesser vil snart være tilgjengelige i Common Data Service.

## <a name="known-issues"></a>Kjente problemer

Arbeidsområdet **Funksjonsbehandling** viser kanskje funksjoner som er deaktivert som evalueringsfunksjonalitet, når de er generelt tilgjengelige. Nedenfor finner du en liste over generelt tilgjengelige funksjoner som viser feil status. 

- Fordelsbehandling
- Saksbehandling
- Databaselogging (revisjon)
- Permisjonsavsetning for ett firma eller én plan
- Avsetningssuspensjon for permisjon og fravær
- Årsakskode og kommentar for saldojustering
- Kjøp og selg permisjon
- Kalender for permisjon og fravær
- Overføringsregler for permisjon
- Overvåking av permisjonsavsetning
- Sletting av permisjonsavsetning
- Avrunding av permisjonsavsetning
- Konfigurer flere permisjonstyper på én permisjonsplan
- Forbedringer for Oppdater fridager
- Bruk den ansattes FTE for avsetninger
- Visning av kompensasjon på tvers av firmaer
- Skrive ut prestasjonsvurderinger
- Helligdagskorrigeringer for permisjonsavsetning

### <a name="benefit-plan-employee-entity"></a>Fordelsplan for ansatt-enheten 

Vi har nylig oppdaget to problemer i forbindelse med **BenefitsPlanEmployee**-enheten. Ved import av arbeiderregistreringer angis **Dekningskode** og **Kode for plantype** feil. Dette problemet fører til at ansattes fordelsplaner vises feil i skjemaet **Fordelsplaner for arbeider** og i skjemaet **Åpen registrering** i Ansattselvbetjening. Dette problemet kan også påvirke den ansattes evne til å velge planer i Ansattselvbetjening. Det finnes for øyeblikket ingen måte å unngå dette på. Vi behandler dette som en høyt prioritert reparasjon, og vil rulle ut reparasjonen i vår neste utgivelse.

## <a name="see-also"></a>Se også

[Nyheter eller endringer i Human Resources](hr-admin-whats-new.md)</br>
[Oversikt over lanseringsbølge 2 i 2019 for Dynamics 365 Human Resources](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Oppdatere prosess](hr-admin-setup-update-process.md)</br>
[Behandle funksjoner](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]