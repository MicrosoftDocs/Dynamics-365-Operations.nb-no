---
title: Hva er nytt eller endret i Dynamics 365 Talent – Core HR (23. januar 2019)
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Talent – Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 01/23/2019
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
ms.search.validFrom: 2019-01-23
ms.dyn365.ops.version: Talent
ms.openlocfilehash: f97462f088fc1a3cb94f2a34204fc09f1cd66fb0
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/06/2019
ms.locfileid: "2899134"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-january-23-2019"></a>Hva er nytt eller endret i Dynamics 365 Talent – Core HR (23. januar 2019)

**Build 8.1.2121**

Dette emnet beskriver funksjoner som enten er nye eller endret i Core HR.

## <a name="changes"></a>Endringer

### <a name="import-of-employee-fixed-compensation-not-working-when-creating-new-fixed-compensation-records"></a>Import av fast kompensasjon for ansatte fungerer ikke ved oppretting av nye poster for fast kompensasjon
En endring er gjort i enheten for fast ansattkompensasjon for å hente kompensasjonsnivået ved import. Før denne versjonen ble det vist en melding som indikerer at nivået er nødvendig.

### <a name="remove-the-minimum-balance-field-from-the-time-off-request-dialog-box"></a>Fjernet feltet for minimumssaldo fra dialogboksen for fraværsforespørsel
Feltet for **Minimumssaldo** er fjernet fra dialogboksen for **fraværsforespørsel**. Denne endringen påvirker alle områder der fravær kan forespørres.

### <a name="data-upgrade-for-compensation-levels-not-updating-in-all-scenarios"></a>Dataoppgradering for kompensasjonsnivåer som ikke oppdateres i alle scenarioer
En endring er gjort for å oppdatere kompensasjonsnivået i planer om fast kompensasjon. Denne endringen vil fylle ut kompensasjonsnivået i faste planer for jobben som er tilordnet den ansatte.

### <a name="payroll-information-in-the-manage-changes-page-is-only-available-when-logged-in-as-system-administrator"></a>Lønnsinformasjon på siden Behandle endringer er bare tilgjengelig når du er logget på som systemansvarlig
Denne endringen gir ansatte med lønnsadministratorrollen tilgang til lønnsinformasjon på siden **Tidslinje for endringer > Administrer endringer** for stillingen.

### <a name="job-fields-default-to-positions"></a>Jobbfelt går som standard til stillinger
Når jobben endres for en stilling, vil jobbfeltene som standard settes til stillingen. En varselsmelding vises og gir et alternativ for å godta standardverdiene eller beholde de eksisterende verdiene for disse feltene.

### <a name="probation-period-and-calendar-are-not-displayed-for-future-hired-employees"></a>Prøveperiode og kalender vises ikke for fremtidige ansatte.
Med denne endringen er det lagt til **Prøveperiode** og **Kalender** på siden **Behandle endringer** for å tillate dataregistrering for fremtidige og tidligere ansatte.

### <a name="platform-update-23-for-finance-and-operations"></a>Platform update 23 for Finance and Operations
Mindre feilrettinger er inkludert som en del av plattformoppdatering 23 for Finance and Operations. Hvis du vil ha mer informasjon, se [Hva er nytt eller endret i Dynamics 365 Finance and Operations plattformoppdatering 23 (januar 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-23). 
