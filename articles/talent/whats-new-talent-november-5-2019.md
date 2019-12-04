---
title: Hva er nytt eller endret i Dynamics 365 Talent (5. november 2019)
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 11/05/2019
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
ms.search.validFrom: 2019-11-05
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e6a81209c3c4a95ee51668533d40d4aecc1d58b9
ms.sourcegitcommit: a46fb06138f7f82e973dca3157d30f9b21d3a70b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/08/2019
ms.locfileid: "2778388"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-november-5-2019"></a>Hva er nytt eller endret i Dynamics 365 Talent (5. november 2019)

[!include [banner](includes/banner.md)]

Dette emnet beskriver funksjoner som enten er nye eller endret i Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Endringer i Attract

Denne versjonen inneholder mindre feilrettinger for Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Endringer i Onboard

Denne versjonen inneholder mindre feilrettinger for Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Endringer i Core HR

Endringer som er beskrevet i denne delen, gjelder build nummer 8.1.2598. Tallene i parentes i noen overskrifter refererer til støttenumre i Microsoft Dynamics Lifecycle Services (LCS).

### <a name="copy-a-core-hr-instance"></a>Kopiere en Core HR-forekomst

I denne ukes versjonen kan du bruke Microsoft Dynamics Lifecycle Services (LCS) til å kopiere en Microsoft Dynamics 365 Talent: Core HR-database til et sandkassemiljø. Hvis du har et annet sandkassemiljø, kan du også kopiere databasen fra dette miljøet til et målrettet sandkassemiljø. Hvis du vil ha mer informasjon,  kan du se:

- [Mer omfattende miljøbehandling](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/broader-environment-management) i Dynamics 365: 2019-frigivelsesbølge 2-planen

- [Kopiere en Core HR-forekomst](hr-copy-instance.md) i Talent-dokumentasjon

### <a name="common-data-service-integration-batch-jobs-arent-created-when-common-data-service-integration-is-enabled-388030"></a>Common Data Service-partijobber for integrasjon blir ikke opprettet når Common Data Service-integrering er aktivert (388030)

Denne endringen vil opprette satsvise jobber for Common Data Service-integrering når den aktiveres.

### <a name="the-hcmpersonimageentity-doesnt-resize-the-person-image-when-uploaded-369469"></a>HcmPersonImageEntity endrer ikke størrelse på personbildet når det lastes opp (369469)

Frigivelsen denne uken endrer hvordan bildestørrelser endres for bedre ytelse når de importeres ved hjelp av databehandling.

### <a name="a-positions-available-for-assignment-date-can-be-earlier-than-the-activation-date-340103"></a>En stilling som er tilgjengelig for tilordningsdatoen, kan være tidligere enn aktiveringsdatoen (340103)

Med denne endringen vil det vises en advarsel hvis du velger en **Tilgjengelig for tilordningsdato** som er tidligere enn stillingens **aktiveringsdato**.

### <a name="cant-create-a-compensation-change-request-in-employee-self-service-for-step-based-plans-376872"></a>Kan ikke opprette en kompensasjonsendringsforespørsel i ansattselvbetjening for trinnbaserte planer (376872)

Denne versjonen retter opp et problem når det bes om kompensasjonsendringer via ansattselvbetjening for trinnbaserte planer. 

### <a name="reason-code-doesnt-sync-to-common-data-service-if-the-description-is-longer-than-30-characters-core-hr-allows-60-352682"></a>Årsakskode synkroniseres ikke til Common Data Service hvis beskrivelsen er lengre enn 30 tegn, Core HR tillater 60 (352682)

Med denne endringen blir årsakskoder med flere enn 30 tegn oppdatert i Common Data Service. Endringer som gjøres Common Data Service, vil også gjenspeiles i Talent.

### <a name="address-integration-from-talent-to-finance-and-operations-351961"></a>Adresseintegrering fra Talent til Finance and Operations (351961)

Denne versjonen løser et problem der adresser som oppdateres i Talent, ikke ble oppdatert i Finance and Operations. Endringer i adresseblokker blir nå oppdatert.

## <a name="coming-soon"></a>Kommer snart

### <a name="print-performance-reviews"></a>Skrive ut prestasjonsvurderinger

Se [Skrive ut prestasjonsvurderinger](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) i Dynamics 365: 2019-frigivelsesbølge 2-planen.

### <a name="feature-management-workspace"></a>Arbeidsområde for funksjonsbehandling

Funksjoner legges til og oppdateres i hver versjon. Funksjonsbehandling-opplevelsen gir et arbeidsområde der du kan vise en liste over funksjoner som er levert i hver versjon. Nye funksjoner er deaktivert som standard. Du kan bruke arbeidsområdet til å aktivere dem og vise dokumentasjonen for dem.

Hvis du vil ha mer informasjon om endringene som kommer med funksjonsbehandling, kan du se [Oversikt over funksjonsbehandling](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).
