---
title: Hva er nytt eller endret i Dynamics 365 Human Resources (28. mai 2020)
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Human Resources for 28. mai 2020.
author: Darinkramer
manager: AnnBe
ms.date: 05/28/2020
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
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 00a5881ea88749c8553e4c810fb57070f217b01c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4419939"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-28-2020"></a>Hva er nytt eller endret i Dynamics 365 Human Resources (28. mai 2020)

Dette emnet beskriver funksjoner som enten er nye eller endret i Dynamics 365 Human Resources. Endringer gjelder for Build-nummeret 8.1.3287. Tallene i parentes i noen overskrifter refererer til støttenumre i LCS.

## <a name="leaverequest-entity-doesnt-work-when-you-enable-multiple-types-per-leave-plan-447498"></a>LeaveRequest-enheten fungerer ikke når du aktiverer flere typer per permisjonsplan (447498)

Med denne endringen er **LeaveEnrollmentV2Entity** nå tilgjengelig for å rette opp feilen som oppstår når du aktiverer flere permisjonstyper.

## <a name="batch-contention-reduction-feature-preview-446619"></a>Funksjon for reduksjon av partikonflikt (forhåndsversjon) (446619)

Når du aktiverer denne funksjonen, kan du forvente en reduksjon i blokkering av tabeller for partirammeverk mens du velger oppgaver og ferdigstiller jobber.

## <a name="updateconflict-while-saving-worker-prevents-editing-a-record-in-people-427915"></a>UpdateConflict ved lagring av arbeider forhindrer redigering av en post i Personer (427915)

Denne endringen korrigerer en feil når du legger til en ny arbeider, oppdaterer adresseinformasjon og endrer språkpreferansen. I dette unike scenariet ble det vist en feilmelding om at posten ikke kunne oppdateres. 

## <a name="unable-to-add-an-attachment-to-an-approved-leave-request-to-resubmit-425407"></a>Kan ikke legge til et vedlegg i en godkjent permisjonsforespørsel for ny innsending (425407)

Denne endringen tillater nå vedlegg i godkjente permisjonsforespørsler.

## <a name="user-can-enter-compensation-for-an-employee-in-a-different-legal-entity-form-409529"></a>Brukeren kan angi kompensasjon for en ansatt i et annet skjema for juridisk enhet (409529)

Denne endringen deaktiverer kompensasjonsalternativer for å hindre utilsiktet registrering av kompensasjonsposter for feil juridisk enhet.

## <a name="error-when-you-transfer-an-employee-and-the-worker-position-assignment-date-is-before-the-position-duration-429402"></a>Feil når du overfører en ansatt, og tilordningsdatoen for arbeiderstillingen kommer før stillingsvarigheten (429402)

Feilmeldinger ved overføring av en ansatt i dette scenariet har blitt oppdatert for å forbedre beskrivelsen av endringene som kreves for å løse problemet.

## <a name="attachments-capabilities-in-employee-self-service-benefits-enrollment"></a>Vedleggsfunksjoner i registrering av selvbetjente fordeler for ansatte
 
Nå kan du legge til vedlegg under prosessen for fordelsregistrering for hver plan som den ansatte registrerer seg i. Du kan deretter vise vedleggene i **Fordeler registrert av arbeider**-skjemaet.

## <a name="in-preview"></a>I forhåndsvisning

## <a name="human-resources-application-in-teams"></a>Human Resources-søknad i Teams

Ansatte kan se og be om fravær fra jobb i Microsoft Teams. De kan kommunisere med en robot for å opprette permisjonsforespørsler. For mer informasjon, se [Human Resources-app i Teams](https://go.microsoft.com/fwlink/?linkid=2127841). 

## <a name="leave-suspension"></a>Avbryt permisjon

Du kan avbryte permisjon og fravær i Human Resources for en ansatt. Hvis du avbryter permisjon, stoppes permisjonsavsetningene for utvalgte permisjonstyper. Hvis suspensjonen skjer etter at en avsetning er behandlet, vil avbrudd av permisjon opprette fordelt justering til den ansattes permisjonssaldo. Hvis du vil ha mer informasjon, kan du se [Avbryt permisjon](hr-leave-and-absence-suspend-leave.md).

## <a name="update-user-experience-to-indicate-that-accrual-is-suspended-429550"></a>Oppdater brukeropplevelsen for å angi at avsetning er deaktivert (429550)

Brukeropplevelsen viser nå at avsetningen er utsatt for en plan.

## <a name="coming-soon"></a>Kommer snart

## <a name="database-logging-in-preview-in-june"></a>Database-loggføring (forhåndsversjon i juni)

Med funksjonen for databaseloggføring kan du bestemme hvilke tabeller og felt som skal overvåkes. Du kan også fastslå hvilke hendelser som skal utløse endringssporing. Forespørselsfunksjoner er tilgjengelige for å se disse endringene over tid.

## <a name="buy-and-sell-leave-in-preview-june-1"></a>Kjøp og salg av permisjon (forhåndsversjon 1. juni)

Noen organisasjoner tilbyr en fordel som gjør det mulig for ansatte å kjøpe eller selge permisjon. Denne prosessen behandles ofte manuelt. Denne funksjonen gir en mer automatisert måte å administrere policyer og forespørsler for HR-avdelingen på, og den bidrar til å eliminere feil samtidig som du effektiviserer permisjonsstyringsprosessen. Hvis du vil ha mer informasjon, kan du se:

- [Administrere policyer for kjøp og salg av permisjon](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [Kjøp og selg permisjon](hr-employee-self-service-buy-sell-leave.md)

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a>Data Management Framework (DMF)-enheter for Fordelsbehandling
 
Enheter for fordelsstyring frigis. DMF-enheter gjør det mulig å importere og eksportere data slik at du enkelt kan konfigurere fordelsbehandling. En mal for fordelsbehandling vil også være tilgjengelig for å flytte data. Malen eksporterer og importerer data på en sekvensiell måte for å respektere dataavhengigheter.

## <a name="add-reason-code-to-accrual-suspensions-june-1"></a>Legg til årsakskode for avsetningsuspensjoner (1. juni)

Årsakskoder er lagt til i avsetningssuspensjonen.

## <a name="carry-forward-rules-june-1"></a>Overføringsregler (1. juni)

Du kan angi en type overføringspermisjon for overføringssaldoer der overføringsjusteringer overføres. Hvis en ansatt for eksempel overfører 10 dager, kan du velge en annen permisjonstype for disse 10 dagene. Hvis du vil ha mer informasjon, kan du se [Konfigurere permisjons- og fraværstyper](hr-leave-and-absence-types.md).

## <a name="suspend-leave-accrual-for-specified-leave-types-june-1"></a>Avbryte permisjonsavsetning for angitte permisjonstyper (1. juni)

I denne versjonen kan HR opprette en regel for å utsette permisjonsavsetninger for ansatte med permisjonsforespørsler som er angitt for fravær som ikke betales. Fravær som ikke betales, kan være en type, men behøver ikke å være det. Du kan stoppe enhver permisjon basert på en annen permisjonstype.

## <a name="dmf-entity-available-for-accrual-suspensions-june-1"></a>DMF-enhet tilgjengelig for avsetningssuspensjoner (1. juni)

En DMF-enhet er nå tilgjengelig for avsetningssuspensjoner.

## <a name="see-also"></a>Se også

[Nyheter eller endringer i Human Resources](hr-admin-whats-new.md)</br>
[Oversikt over lanseringsbølge 2 i 2019 for Dynamics 365 Human Resources](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Oppdatere prosess](hr-admin-setup-update-process.md)</br>
[Behandle funksjoner](hr-admin-manage-features.md)