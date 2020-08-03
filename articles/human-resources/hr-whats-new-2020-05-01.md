---
title: Hva er nytt eller endret i Dynamics 365 Human Resources (1. mai 2020)
description: Denne artikkelen beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Human Resources.
author: Darinkramer
manager: AnnBe
ms.date: 05/01/2020
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
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e4da626ce3412fba6f90dd7f953c1cbc79ab60c3
ms.sourcegitcommit: bd9ff0d28718d535356ffbe1cffaaf60310dd430
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/13/2020
ms.locfileid: "3555129"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-1-2020"></a>Hva er nytt eller endret i Dynamics 365 Human Resources (1. mai 2020)

Denne artikkelen beskriver funksjoner som enten er nye eller endret i Dynamics 365 Human Resources. Endringer gjelder for Build-nummeret 8.1.3196. Tallene i parentes i noen overskrifter refererer til støttenumre i LCS.

## <a name="new-performance-management-entities-available-in-data-management-framework-dmf"></a>Nye ytelsesstyringsenheter er tilgjengelige i Data Management Framework (DMF)

Følgende enheter er nå tilgjengelige. Hvis du ikke ser disse enhetene oppført i enhetslisten, bruker du alternativet **Oppdater enheter** i **Rammeverkparametere > Enhetsinnstillinger > Oppdater enhetsliste**.

- **Diskusjonskompetanse**
- **Diskusjonsmål**
- **Diskusjonsmål**
- **Diskusjonsemne**
- **Ytelsesjournal**
- **Mål**
- **Mål**

I tillegg ble **totalt resultat** og **gjennomsnittsresultat** lagt til i **Diskusjon**-enheten.

## <a name="increase-length-of-leave-request-comments-275641"></a>Øke lengden på permisjonsforespørselskommentarer (275641)

Kommentarer om permisjonsforespørsler tillater nå mer enn 100 tegn.

## <a name="final-comments-on-reviews-dont-appear-when-the-manager-or-employee-is-signed-into-a-different-company-431688"></a>Endelige kommentarer om gjennomganger vises ikke når lederen eller den ansatte blir logget på et annet firma (431688)

Alle kommentarer vises nå ved visning av gjennomganger.

## <a name="user-defined-links-arent-supported-on-new-worker-form-390374"></a>Brukerdefinerte koblinger støttes ikke for skjema for ny arbeider (390374)

Brukerdefinerte koblinger er nå aktivert i det strømlinjeformede **Arbeider**-skjemaet.

## <a name="hcmratinglevelentity-causes-odata-api-crash-439476"></a>HcmRatingLevelEntity forårsaker OData-API-krasj (439476)

Denne endringen korrigerer API-krasjet. Det dupliserte navnet forårsaket denne feilen.

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

## <a name="known-issues"></a>Kjente problemer

## <a name="sharepoint-preview-doesnt-work-in-some-environments"></a>SharePoint-forhåndsvisning fungerer ikke i enkelte miljøer

Hvis dokumentforhåndsvisning for dokumenter lagret i SharePoint, ikke fungerer, kan du prøve følgende:

1. Kontroller at brukerkontoen for administratorer har en e-post tilknyttet brukeroppføringen. Du kan vise denne informasjonen på **Bruker**-siden. Hvis e-post ikke er konfigurert, må du legge til e-postmeldingen og leverandøren med Excel-tillegget OData. Som standard finnes ikke e-postadressen i Excel-utformingen. Du må redigere Excel-utformingen, legge til alle felt, bruke og oppdatere. Når du har fullført disse trinnene, kan du oppdatere administratorkontoen.

2. Når administratorkontoen har en tilknyttet e-postkonto, logger du på Human Resources med administratorlegitimasjon.

3. Få tilgang til et vedlegg i SharePoint for å starte forhåndsvisning av dokument.

4. Logg på med en annen brukerkonto som har tilgang til vedlegg, og bekreft at forhåndsvisningen fungerer som forventet.

## <a name="see-also"></a>Se også

[Nyheter eller endringer i Human Resources](hr-admin-whats-new.md)</br>
[Oversikt over lanseringsbølge 2 i 2019 for Dynamics 365 Human Resources](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Oppdatere prosess](hr-admin-setup-update-process.md)</br>
[Behandle funksjoner](hr-admin-manage-features.md)