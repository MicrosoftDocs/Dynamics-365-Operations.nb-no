---
title: Hva er nytt eller endret i Dynamics 365 Talent (10. desember 2019)
description: Denne artikkelen beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 12/10/2019
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
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 18f86f5d87b780d5d4ffc83330d389077987dda6
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528177"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-december-10-2019"></a>Hva er nytt eller endret i Dynamics 365 Talent (10. desember 2019)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dette emnet beskriver funksjoner som enten er nye eller endret i Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Endringer i Attract

Denne versjonen inneholder mindre feilrettinger for Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Endringer i Onboard

Denne versjonen inneholder mindre feilrettinger for Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Endringer i Core HR

Endringer som er beskrevet i denne delen, gjelder build nummer 8.1.2660. Tallene i parentes i noen overskrifter refererer til støttenumre i Microsoft Dynamics Lifecycle Services (LCS).

### <a name="feature-management-workspace"></a>Arbeidsområde for funksjonsbehandling

Arbeidsområdet **Funksjonsbehandling** inneholder en liste over funksjoner som leveres i hver utgivelse. Nye funksjoner er deaktivert som standard. Du kan bruke arbeidsområdet til å aktivere dem og vise dokumentasjonen for dem. Hvis du vil ha mer informasjon om funksjonsbehandling, kan du se [Oversikt over funksjonsbehandling](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).

Alle nye funksjoner blir forhåndsvist i minst 30 dager, og vanligvis 30-60 dager. Større funksjoner er vanligvis tilgjengelig i oktober og april i hvert år etter forhåndsvisningsperioden. Så snart du ser nye funksjoner i arbeidsområdet for **funksjonsbehandling**, kan du aktivere dem. Det kan hende at noen funksjoner er aktivert som standard.
 
Noen ganger vil en integrert funksjon være aktivert som standard og kan ikke deaktiveres (for eksempel arbeidsområdet **Funksjonsbehandling**).
 
Når en funksjon er generelt tilgjengelig, kan den aktiveres eller deaktiveres i produksjonsmiljøer. Arbeidsområdet for **funksjonsbehandling** angir når en forhåndsvisningsfunksjon blir obligatorisk. Denne datoen er vanligvis 1. oktober eller 1. april for å justeres med de halvårlige frigivelsesplanene. De kan ikke deaktivere obligatoriske funksjoner. Før den blir obligatorisk, kan du slå en funksjon på og av i alle miljøer.

### <a name="streamlined-worker-form-has-moved-to-the-feature-management-workspace-390583"></a>Strømlinjeformet arbeiderskjema er flyttet til arbeidsområdet for funksjonsbehandling (390583)

Med denne endringen kan det strømlinjeformede arbeiderskjemaet nå aktiveres i arbeidsområdet **Funksjonsbehandling**. Denne funksjonen er flyttet fra **Systemparametere**-skjemaet i **Systemadministrasjon**.

### <a name="prevent-hcmworkerpayrollinfo-records-from-being-written-without-a-worker-value-394526"></a>Forhindre at HcmWorkerPayrollInfo-poster skrives uten en arbeiderverdi (394526)

Med denne versjonen opprettes ikke lenger **HcmWorkerPayrollInfo**-poster under uten arbeiderreferanse i dette scenariet. 

### <a name="message-log-associated-to-the-action-isnt-populated-when-the-action-fails-to-complete-374007"></a>Meldingsloggen som er knyttet til handlingen, fylles ikke ut når handlingen mislykkes (374007)

Denne versjonen inkluderer en endring for å fylle ut handlingsmeldingsloggen når en handling mislykkes i enkelte scenarier. 

### <a name="common-data-service-integration-batch-job-creation-388030"></a>Opprettelse av satsvis jobb for Common Data Service-integrering (388030)

Med denne endringen opprettes satsvise jobber for Common Data Service-integrering når tjenesten er aktivert.

### <a name="additional-pick-list-values-to-custom-fields-arent-reflected-in-common-data-service-after-clicking-apply-on-the-custom-fields-form-379599"></a>Flere plukklisteverdier i egendefinerte felt gjenspeiles ikke i Common Data Service når du klikker Bruk på egendefinerte felt-skjemaet (379599)

Med denne endringen blir nye plukklisteverdier som er angitt i Talent, nå synkronisert til Common Data Service når du bruker endringene.

### <a name="update-to-common-data-service-for-then-leave-bank-transaction-entity-turns-into-an-insert-on-talent-side-352938"></a>Oppdatering til enheten for permisjonsbanktransaksjonen for Common Data Service blir til en innsetting på Talent-side (352938)

Denne endringen korrigerer et problem der en oppdatering til en permisjonsbanktransaksjon oppretter en ny post i Talent.

## <a name="in-preview"></a>I forhåndsvisning

Forhåndsvisningsfunksjoner er bare tilgjengelige i **Sandkasse**-miljøer.

### <a name="print-performance-reviews"></a>Skrive ut prestasjonsvurderinger

Se [Skrive ut prestasjonsvurderinger](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) i Dynamics 365: 2019-frigivelsesbølge 2-planen.



[!INCLUDE[footer-include](../includes/footer-banner.md)]