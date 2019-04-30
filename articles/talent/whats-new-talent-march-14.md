---
title: Hva er nytt eller endret i Dynamics 365 for Talent (14. mars 2019)?
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 for Talent.
author: Darinkramer
manager: AnnBe
ms.date: 03/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-03-14
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 38641d6a84340112ce15335533795ed7faf91123
ms.sourcegitcommit: 0b9d7d4c163992a9949bd8c8fffa18eb4ad9fa64
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/15/2019
ms.locfileid: "845201"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-march-14-2019"></a>Hva er nytt eller endret i Dynamics 365 for Talent (14. mars 2019)?

[!include [banner](includes/banner.md)]

Dette emnet beskriver funksjoner som enten er nye eller endret i Talent.

## <a name="changes-in-attract"></a>Endringer i Attract
Det er mindre feilrettinger inkludert i denne utgivelsen.

## <a name="changes-in-onboarding"></a>Endringer i jobbintroduksjon
Det er mindre feilrettinger inkludert i denne utgivelsen.

## <a name="changes-in-core-hr"></a>Endringer i Core HR
**Build 8.1.2186**

### <a name="performance-management-not-working-in-all-scenarios-when-using-duplicate-security-roles"></a>Ytelsesstyring fungerer ikke i alle scenarioer når det brukes duplikate sikkerhetsroller
Endringer i denne versjonen aktiverer ytelsesstyringsscenarioer ved bruk av standardroller eller dupliserte roller.

### <a name="mass-assign-checklists-to-workers"></a>Massetilordne sjekklister til arbeidere
Med denne endringen kan du nå velge flere ansatte og bulktilordne én eller flere sjekklister til de ansatte. 

### <a name="platform-update-24"></a>Plattform update 24
Hvis du vil ha mer informasjon om Plattformoppdatering 24, kan du se [Hva er nytt eller endret i Finance and Operations Plattformoppdatering 24 (mars 2019)](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-24). Viktige endringer i 24-plattformen omfatter: 

- Varsler er aktivert i Talent.
- Det oppdaterte navigasjonsfeltet er nå justert til Office-toppteksten.

### <a name="office-location-update-switches-the-context-to-the-top-of-the-worker-list"></a>Oppdatering av kontoradresse endrer konteksten til toppen av arbeiderlisten
Med den gjeldende versjonen vil ikke endring av kontoradressen lenger endre konteksten til arbeideren som du viser når du tilordner en kontoradresse.

### <a name="position-assignment-end-date-doesnt-display-correctly-on-worker-hire-and-transfer-actions"></a>Sluttdatoen for stillingstilordningen vises ikke riktig på ansettelses- og overføringshandlinger for arbeider
Sluttdatoer for stillingstilordning vises nå riktig basert på den foretrukne tidssonen for brukeren ved bruk av handlinger.

### <a name="common-data-service-job-entity-doesnt-allow-job-type-and-job-function-fields-to-update"></a>Common Data Service-jobbenheten tillater ikke oppdatering av jobbtype- og jobbfunksjonsfeltene
Common Data Service-enheter synkroniseres nå på riktig måte når de oppdateres ved hjelp av Common Data Service.

## <a name="coming-soon"></a>Kommer snart

###  <a name="advanced-compensation-security-fixed-and-variable"></a>Avansert kompensasjonssikkerhet (fast og variabel)
I mange organisasjoner kan kompensasjons- og fordelsansvarlige bare ha tilgang til bestemte kompensasjonsposter. Disse kan være for ledere eller regionale ansatte. Med denne endringen kan HR administrere og vedlikeholde kompensasjonsplanene for ulike ansattgrupper i organisasjonen. Faste og variable planer kan tilordnes til sikkerhetsroller, som bestemmer tilgangen til planene og ansattdataene som er knyttet til dem, for eksempel lønns- eller bonusposter. Bare rollene der tilgang er gitt, kan behandle kompensasjon for disse ansatte.

###  <a name="email-support-for-alerts"></a>E-poststøtte for varsler
Med Platform update 24 kan brukere opprette varslingsregler som automatisk leverer e-postmeldinger til kontakter når de utløses av en hendelse.

### <a name="duplicate-employee-check-interface-changes"></a>Kontroller av dupliserte ansatte: Endringer i grensesnittet
Med denne endringen oppdages duplikater når du angir navnefelt, og statusen viser hvor mange som ble funnet. Du kan velge den angitte lenken for å åpne en ny side for å vurdere om du vil bruke resultatet som ble funnet. For å unngå å forstyrre dataregistreringen åpnes duplikatskjemaet ikke automatisk.
