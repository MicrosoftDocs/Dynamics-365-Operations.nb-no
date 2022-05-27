---
title: Hva er nytt eller endret i Dynamics 365 Human Resources (23. juli 2020)
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Human Resources for 23. juli 2020.
author: andreabichsel
ms.date: 07/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-07-23
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: baf92234bc63449435324cc2d199a0529e53857a
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/04/2022
ms.locfileid: "8692037"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-july-23-2020"></a>Hva er nytt eller endret i Dynamics 365 Human Resources (23. juli 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Dette emnet beskriver funksjoner som enten er nye eller endret i Dynamics 365 Human Resources. Endringer gjelder for Build-nummeret 8.1.3416. Tallene i parentes i noen overskrifter refererer til støttenumre i LCS.

## <a name="deleting-financial-dimensions-on-a-position-doesnt-work-as-expected-445476"></a>Sletting av finansdimensjoner for en stilling fungerer ikke som forventet (445476)

Hvis du fjerner dimensjoner fra en stilling, fjernes de samme posisjonene nå fra Dataverse.

## <a name="positions-not-in-hierarchy-show-inactive-positions-397257"></a>Stillinger som ikke er i hierarkiet, viser inaktive stillinger (397257)

Stillinger som er inaktive (har en utløpt varighet), vises ikke lenger i stillingshierarkiet som **Stillinger som ikke er i hierarkiet**. 

## <a name="validation-occurring-between-leaveenrollmententity-and-hcmworkerentity-on-data-management-framework-dmf-import-causes-slow-data-loads-442324"></a>Validering som skjer mellom LeaveEnrollmentEntity og HcmWorkerEntity ved DMF-import (Data Management Framework), fører til langsom datalasting (442324)

Endringer i denne versjonen øker ytelsen til **LeaveEnrollmentEntity**.

## <a name="unable-to-personalize-in-organization-administration-447490"></a>Kan ikke tilpasse i organisasjonsadministrasjon (447490)

Med denne endringen kan du nå tilpasse koblingene under **Organisasjonsadministrasjon**.

## <a name="in-preview"></a>I forhåndsvisning

## <a name="mandatory-fields"></a>Obligatorisk felt 

Du kan nå endre feltene ved hjelp av tilpasningsfunksjonene i Human Resources. Denne funksjonen krever **Lagrede visninger**.

## <a name="human-resources-application-in-teams"></a>Human Resources-søknad i Teams

Ansatte kan se og be om fravær fra jobb i Microsoft Teams. De kan kommunisere med en robot for å opprette permisjonsforespørsler. For mer informasjon, se [Human Resources-app i Teams](./hr-admin-teams-leave-app.md). 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a>Data Management Framework (DMF)-enheter for Fordelsbehandling
 
Enheter for fordelsstyring frigis. DMF-enheter gjør det mulig å importere og eksportere data slik at du enkelt kan konfigurere fordelsbehandling. En mal for fordelsbehandling vil være tilgjengelig for å flytte data. Malen eksporterer og importerer data på en sekvensiell måte for å respektere dataavhengigheter.

## <a name="buy-and-sell-leave"></a>Kjøp og selg permisjon 

Noen organisasjoner tilbyr en fordel som gjør det mulig for ansatte å kjøpe eller selge permisjon. Denne prosessen behandles ofte manuelt. Denne funksjonen automatiserer behandling av policyer og forespørsler for personalavdelingen. Den strømlinjeformer permisjonsstyringsprosessen og bidrar til å eliminere feil. Hvis du vil ha mer informasjon, kan du se:

- [Administrere policyer for kjøp og salg av permisjon](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [Kjøp og selg permisjon](hr-employee-self-service-buy-sell-leave.md)

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

## <a name="dmf-entity-available-for-accrual-suspensions"></a>DMF-enhet tilgjengelig for avsetningssuspensjoner 

En DMF-enhet er nå tilgjengelig for avsetningssuspensjoner.

## <a name="coming-soon"></a>Kommer snart

## <a name="checklist-entities-included-in-dataverse"></a>Sjekklisteenheter inkludert i Dataverse

Sjekklisteenheter for pålasting, avlasting, overføringer og forretningsprosesser vil snart være tilgjengelige i Dataverse.

## <a name="platform-changes"></a>Plattformendringer

Platform update 10.0.12 (36)

## <a name="see-also"></a>Se også

[Nyheter eller endringer i Human Resources](hr-admin-whats-new.md)</br>
[Oversikt over lanseringsbølge 2 i 2019 for Dynamics 365 Human Resources](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Oppdatere prosess](hr-admin-setup-update-process.md)</br>
[Behandle funksjoner](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]