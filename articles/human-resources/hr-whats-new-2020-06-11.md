---
title: Hva er nytt eller endret i Dynamics 365 Human Resources (11. juni 2020)
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Human Resources for 11. juni 2020.
author: andreabichsel
ms.date: 06/16/2020
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
ms.search.validFrom: 2020-06-11
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8265c0b6218f69b95f2729140aa303edeaa31443
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/13/2021
ms.locfileid: "5891943"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-june-11-2020"></a>Hva er nytt eller endret i Dynamics 365 Human Resources (11. juni 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Denne artikkelen beskriver funksjoner som enten er nye eller endret i Dynamics 365 Human Resources. Endringer gjelder for Build-nummeret 8.1.3316. Tallene i parentes i noen overskrifter refererer til støttenumre i LCS.

## <a name="streamlined-employee-form-sometimes-causes-child-form-close-x-buttons-to-stop-working-442369"></a>Strømlinjeformet ansattskjema fører noen ganger til at lukkeknapper for underordnet skjema (X) slutter å fungere (442369)

Når skjemaet **Arbeider** ble aktivert, virker ikke lukkeknappen (**X**) av og til for underordnede skjemaer. Dette problemet var forbigående. Du kan lukke skjemaet etter at du forlater det, og deretter komme tilbake til det. Du kan for eksempel velge et menyelement til venstre og gå tilbake til **Arbeider**-skjemaet og deretter lukke det. Denne ukens versjon retter opp dette problemet. 

## <a name="the-worker-personal-contact-person-entity-doesnt-export-personal-contacts-with-a-parent-relationship-type"></a>Enheten Arbeiderens personlige kontaktperson eksporterer ikke personlige kontakter med en overordnet relasjonstype

Med denne versjonen eksporterer **Arbeiderens personlige kontaktperson** alle relasjonstyper.

## <a name="the-hcmpositionworkerassignmentv2entity-should-be-part-of-the-ceridian-payroll-integration-package-by-default-448506"></a>HcmPositionWorkerAssignmentV2Entity skal være en del av Ceridian-lønnsintegrasjonspakken som standard (448506)

Med denne endringen er **HcmPositionWorkerAssignmentV2Entity** inkludert i Ceridian-lønnsintegrasjonspakken.

## <a name="in-preview"></a>I forhåndsvisning

## <a name="database-logging"></a>Databaselogging

Med funksjonen for databaseloggføring kan du bestemme hvilke tabeller og felt som skal overvåkes. Du kan også fastslå hvilke hendelser som skal utløse endringssporing. Du kan bruke funksjonen for databaselogging for å se endringene over tid. Hvis du vil ha mer informasjon, se [Konfigurere og administrere databaselogging](hr-admin-database-logging.md).

## <a name="human-resources-application-in-teams"></a>Human Resources-søknad i Teams

Ansatte kan se og be om fravær fra jobb i Microsoft Teams. De kan kommunisere med en robot for å opprette permisjonsforespørsler. For mer informasjon, se [Human Resources-app i Teams](./hr-admin-teams-leave-app.md). 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a>Data Management Framework (DMF)-enheter for Fordelsbehandling
 
Enheter for fordelsstyring frigis. DMF-enheter gjør det mulig å importere og eksportere data slik at du enkelt kan konfigurere fordelsbehandling. En mal for fordelsbehandling vil være tilgjengelig for å flytte data. Malen eksporterer og importerer data på en sekvensiell måte for å respektere dataavhengigheter.

## <a name="buy-and-sell-leave"></a>Kjøp og selg permisjon 

Noen organisasjoner tilbyr en fordel som gjør det mulig for ansatte å kjøpe eller selge permisjon. Denne prosessen behandles ofte manuelt. Denne funksjonen automatiserer behandling av policyer og forespørsler for personalavdelingen. Den strømlinjeformer permisjonsstyringsprosessen og bidrar til å eliminere feil. Hvis du vil ha mer informasjon, kan du se:

- [Administrere policyer for kjøp og salg av permisjon](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [Kjøp og selg permisjon](hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a>Permisjonsavsetning for ett enkelt firma eller én enkelt plan

Kunder kan behandle avsetninger for ett enkelt firma eller en enkel permisjons- og fraværsplan. Denne muligheten gir klarhet til avsetningsprosessen for kunder med forskjellige policyer for fraværsår eller permisjonsavsetning. Hvis du vil ha mer informasjon, se [Avsett permisjon per firma eller per permisjonsplan](hr-leave-and-absence-accrue.md).

## <a name="add-attachments-to-time-off-requests"></a>Legge til vedlegg i fraværsforespørsler

Muligheten til å legge til vedlegg i godkjente permisjonsforespørsler er viktig i det gjeldende COVID-19-miljøet. Ansatte kan nå legge til disse vedleggene. De har også mer innsikt i hvordan det gjøres oppdateringer for permisjonsforespørsler. Hvis du vil ha mer informasjon, kan du se [Legge til et vedlegg i en eksisterende forespørsel](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).

## <a name="add-reason-code-to-accrual-suspensions"></a>Legge til årsakskode for avsetningsuspensjoner 

Årsakskoder er lagt til i avsetningssuspensjonen.

## <a name="carry-forward-rules"></a>Overføringsregler 

Du kan angi en type overføringspermisjon for overføringssaldoer der overføringsjusteringer overføres. Hvis en ansatt for eksempel overfører 10 dager, kan du velge en annen permisjonstype for disse 10 dagene. Hvis du vil ha mer informasjon, kan du se [Konfigurere permisjons- og fraværstyper](hr-leave-and-absence-types.md).

## <a name="suspend-leave-accrual-for-specified-leave-types"></a>Avbryte permisjonsavsetning for angitte permisjonstyper

Du kan opprette en regel for å utsette permisjonsavsetninger for ansatte med permisjonsforespørsler som er angitt for fravær som ikke betales. Fravær som ikke betales, kan være en type, men behøver ikke å være det. Du kan stoppe enhver permisjon basert på en annen permisjonstype.

## <a name="dmf-entity-available-for-accrual-suspensions"></a>DMF-enhet tilgjengelig for avsetningssuspensjoner 

En DMF-enhet er nå tilgjengelig for avsetningssuspensjoner.

## <a name="coming-soon"></a>Kommer snart

## <a name="new-platform-capabilities"></a>Nye plattformegenskaper 

Du kan gjøre felt obligatoriske ved hjelp av personalisering. Denne funksjonen vil kreve at du aktiverer **Lagrede visninger**.

## <a name="configure-the-name-of-employee-self-service"></a>Konfigurere navnet på ansattselvbetjening

Et nytt alternativ vil være tilgjengelig i Personale-parametere for å oppdatere navnet på arbeidsområdet Ansattselvbetjening til Selvbetjening. 

## <a name="see-also"></a>Se også

[Nyheter eller endringer i Human Resources](hr-admin-whats-new.md)</br>
[Oversikt over lanseringsbølge 2 i 2019 for Dynamics 365 Human Resources](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Oppdatere prosess](hr-admin-setup-update-process.md)</br>
[Behandle funksjoner](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]