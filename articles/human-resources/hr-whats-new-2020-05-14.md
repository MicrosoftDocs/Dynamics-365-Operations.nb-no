---
title: Hva er nytt eller endret i Dynamics 365 Human Resources (14. mai 2020)
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Human Resources for 14. mai 2020.
author: Darinkramer
manager: AnnBe
ms.date: 05/14/2020
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
ms.search.validFrom: 2020-05-14
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d68647508c70a20b7ecba3358c7e3ebccd8d71ef
ms.sourcegitcommit: 2bcacef1e010c312f019dbf9740ce87d627848a7
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/20/2020
ms.locfileid: "3712044"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-14-2020"></a>Hva er nytt eller endret i Dynamics 365 Human Resources (14. mai 2020)

Dette emnet beskriver funksjoner som enten er nye eller endret i Dynamics 365 Human Resources. Endringer gjelder for Build-nummeret 8.1.3244. Tallene i parentes i noen overskrifter refererer til støttenumre i Lifecycle Services (LCS).

## <a name="platform-changes"></a>Plattformendringer

Plattformendringer er inkludert i denne ukens frigivelse. Hvis du vil ha mer informasjon, kan du se [Platformoppdateringer for versjon 10.0.10 av Finance and Operations-apper (mai 2020)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-update-34). Denne versjonen inneholder feilrettinger og endringer i lagrede visninger.
 
## <a name="ensure-common-data-service-picklists-are-consistent-with-leave-enums-436343"></a>Sørg for at plukklister i Common Data Service er konsekvente med permisjonsopplistinger (436343)

Plukklister i Common Data Service er konsekvente med permisjonsopplistinger.

## <a name="allow-users-to-configure-leave-request-workflow-based-on-the-request-amount-300044"></a>Tillat brukere å konfigurere en arbeidsflyt for permisjonsforespørsel basert på forespørselsbeløpet (300044)

Brukere kan konfigurere arbeidsflyter for permisjonsforespørsel basert på forespørselsbeløp.
 
## <a name="new-worker-form-exposes-data-through-the-view-menu-when-advanced-security-is-enabled-403185"></a>Nytt arbeiderskjema viser data på Vis-menyen når avansert sikkerhet er aktivert (403185)

Denne versjonen korrigerer hvordan visning av arbeidere på tvers av juridiske enheter fungerer når avansert tilgang er aktivert, og arbeidere i andre firmaer er tilgjengelige.

## <a name="allow-running-leave-accruals-for-a-single-plan-or-a-single-company-318844"></a>Tillat at det kjøres permisjonsavsetninger for én plan eller ett firma (318844)

Med denne endringen kan du kjøre avsetninger for et firma eller en plan.
 
## <a name="show-the-positions-full-time-equivalent-fte-in-the-enrolled-workers-form-414658"></a>Vis stillingens heltidsekvivalent (FTE) i skjemaet Registrerte arbeidere (414658)

FTE-verdien fra stillingen til en arbeider bestemmer en ansatts avsetningssats når FTE-alternativet er aktivert for permisjonstypen. Dette feltet er nå inkludert i skjemaet **Registrerte arbeidere** og dialogboksen **Masseregistrering**.

## <a name="add-leave-balance-expiration-batch-job-431266"></a>Legg til den satsvise jobben for utestående beløp (431266)

En ny satsvis jobb er nå tilgjengelig som kjører daglig. Det reduserer saldoen for gjenværende permisjon når utløpsdatoer blir gjeldende.

## <a name="exporting-personal-contacts-for-an-employee-using-the-worker-personal-contact-person-entity-doesnt-export-personal-contacts-with-the-parent-relationship-type-345893"></a>Eksport av personlige kontaktpersoner for en ansatt ved hjelp av arbeiderens personlige kontaktperson, eksporterer ikke personlige kontakter med den overordnede relasjonstypen (345893)

Dataenheten **Arbeiderens personlige kontaktperson** (**HcmPersonalContactPersonEntity** i DMF og **PersonalContactPerson** i OData) kan ikke eksportere personlige kontakter som har relasjonstypen **Overordnet**. Dette problemet er løst for personlige kontakter som er opprettet etter denne endringen. Eksisterende personlige kontakter av typen **Overordnet** vil bli løst i en senere versjon.

## <a name="reason-codes-display-across-different-scenarios-when-theyre-marked-as-leave-and-absence-and-the-streamlined-employee-form-is-enabled-434163"></a>Årsakskoder vises på tvers av ulike scenarioer når de merkes som permisjon og fravær, og det strømlinjeformede ansattskjemaet er aktivert (434163)

Denne endringen begrenser årsakskodene til bare permisjons- og fraværskoder når du aktiverer strømlinjeformet ansattoppføring.

## <a name="the-preview-feature-assign-a-leave-plan-to-employees-in-the-future-displays-error-433555"></a>Forhåndsvisningsfunksjonen Tilordne en permisjon til ansatte i fremtiden viser feil (433555)

Denne endringen korrigerer en feil når en permisjonsplan har to permisjonstyper tilordnet, og du prøver å tilordne en ansatt.

## <a name="getting-started-banner-appears-for-all-users-441731"></a>Banneret Komme i gang vises for alle brukere (441731)

Med denne endringen er banneret Komme i gang skjult for brukere som ikke er systemadministratorer eller databehandlingsadministratorer. 

## <a name="the-common-data-service-worker-address-entity-works-differently-in-terms-of-date-time-effective-dates-in-human-resources-425071"></a>Enheten Adresse for Common Data Service-arbeider fungerer annerledes når det gjelder datoer som er gyldige i Human Resources (425071)

Denne endringen holder adresseinformasjon justert i bestemte scenarioer, basert på datoene til adressen.

## <a name="unable-to-add-an-attachment-to-an-approved-leave-request-425407"></a>Kan ikke legge til et vedlegg i en godkjent permisjonsforespørsel (425407)

Med denne ukes frigivelse kan du legge til vedlegg i godkjente permisjonsforespørsler uten å endre permisjonsforespørselen.

## <a name="in-preview"></a>I forhåndsvisning

## <a name="leave-suspension"></a>Avbryt permisjon

Du kan avbryte permisjon og fravær i Human Resources for en ansatt. Hvis du avbryter permisjon, stoppes permisjonsavsetningene for utvalgte permisjonstyper. Hvis suspensjonen skjer etter at en avsetning er behandlet, vil avbrudd av permisjon opprette fordelt justering til den ansattes permisjonssaldo. Hvis du vil ha mer informasjon, kan du se [Avbryt permisjon](hr-leave-and-absence-suspend-leave.md).

## <a name="update-user-experience-to-indicate-that-accrual-is-suspended-429550"></a>Oppdater brukeropplevelsen for å angi at avsetning er deaktivert (429550)

Brukeropplevelsen viser nå at avsetningen er utsatt for en plan.

## <a name="suspend-leave-accrual-for-specified-leave-types-272447"></a>Avbryte permisjonsavsetning for angitte permisjonstyper (272447)

I denne versjonen kan HR opprette en regel for å utsette permisjonsavsetninger for ansatte med permisjonsforespørsler som er angitt for fravær som ikke betales. Fravær som ikke betales, kan være en type, men behøver ikke å være det. Du kan stoppe enhver permisjon basert på en annen permisjonstype.

## <a name="dmf-entity-available-for-accrual-suspensions-429549"></a>DMF-enhet tilgjengelig for avsetningssuspensjoner (429549)

En DMF-enhet er nå tilgjengelig for avsetningssuspensjoner.

## <a name="add-reason-code-to-accrual-suspensions-429547"></a>Legg til årsakskode for avsetningsuspensjoner (429547)

Årsakskoder er lagt til i avsetningssuspensjonen.

## <a name="begin-transitioning-from-human-resources-parameters-to-leave-and-absence-parameters"></a>Begynne overgang fra Personale-parametere til permisjons- og fraværsparametere

Denne versjonen begynner med å kombinere Personale-parametere med permisjons- og fraværsparametere.

## <a name="carry-forward-rules"></a>Overføringsregler

Du kan angi en type overføringspermisjon for overføringssaldoer der overføringsjusteringer overføres. Hvis en ansatt for eksempel overfører 10 dager, kan du velge en annen permisjonstype for disse 10 dagene. Hvis du vil ha mer informasjon, kan du se [Konfigurere permisjons- og fraværstyper](hr-leave-and-absence-types.md).

## <a name="see-also"></a>Se også

[Nyheter eller endringer i Human Resources](hr-admin-whats-new.md)</br>
[Oversikt over lanseringsbølge 2 i 2019 for Dynamics 365 Human Resources](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Oppdatere prosess](hr-admin-setup-update-process.md)</br>
[Behandle funksjoner](hr-admin-manage-features.md)