---
title: Hva er nytt eller endret i Dynamics 365 Talent (19. november 2019)
description: Denne artikkelen beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 11/19/2019
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
ms.search.validFrom: 2019-11-19
ms.dyn365.ops.version: Talent
ms.openlocfilehash: aa984a01e9da30e6da07516fa2986833366a882b
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/17/2020
ms.locfileid: "4527150"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-november-19-2019"></a>Hva er nytt eller endret i Dynamics 365 Talent (19. november 2019)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Denne artikkelen beskriver funksjoner som enten er nye eller endret i Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Endringer i Attract

Denne versjonen inneholder mindre feilrettinger for Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Endringer i Onboard

Denne versjonen inneholder mindre feilrettinger for Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Endringer i Core HR

Endringer som er beskrevet i denne delen, gjelder build nummer 8.1.2621. Tallene i parentes i noen overskrifter refererer til støttenumre i Microsoft Dynamics Lifecycle Services (LCS).

### <a name="platform-update-31-for-finance-and-operations-apps"></a>Plattform Update 31 for Finance and Operations-apper

Hvis du vil ha mer informasjon, se [Forhåndsversjonsfunksjoner i Platform update 31 for Finance and Operations-apper (januar 2020)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-update-31).

### <a name="feature-management-workspace-383856"></a>Arbeidsområde for funksjonsbehandling (383856)

Arbeidsområdet **Funksjonsbehandling** inneholder en liste over funksjoner som leveres i hver utgivelse. Nye funksjoner er deaktivert som standard. Du kan bruke arbeidsområdet til å aktivere dem og vise dokumentasjonen for dem. Hvis du vil ha mer informasjon om funksjonsbehandling, kan du se [Oversikt over funksjonsbehandling](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).

Alle nye funksjoner blir forhåndsvist i minst 30 dager, og vanligvis 30-60 dager. Større funksjoner er vanligvis tilgjengelig i oktober og april i hvert år etter forhåndsvisningsperioden. Så snart du ser nye funksjoner i arbeidsområdet for **funksjonsbehandling**, kan du aktivere dem. Det kan hende at noen funksjoner er aktivert som standard.
 
Noen ganger vil en integrert funksjon være aktivert som standard og kan ikke deaktiveres (for eksempel arbeidsområdet **Funksjonsbehandling**).
 
Når en funksjon er generelt tilgjengelig, kan den aktiveres eller deaktiveres i produksjonsmiljøer. Arbeidsområdet for **funksjonsbehandling** angir når en forhåndsvisningsfunksjon blir obligatorisk. Denne datoen er vanligvis 1. oktober eller 1. april for å justeres med de halvårlige frigivelsesplanene. De kan ikke deaktivere obligatoriske funksjoner. Før den blir obligatorisk, kan du slå en funksjon på og av i alle miljøer.

### <a name="message-appears-when-canceled-action-exists-for-a-position-382887"></a>Meldingen vises når det finnes en avbrutt handling for en stilling (382887)

Følgende melding vises ikke lenger når du velger en bestemt stilling og en avbrutt handling er alt som er tilgjengelig for stillingen: **En ufullstendig handling pågår for stillingen xxxxxx.**

### <a name="in-learning-analytics-the-course-type-and-status-display-incorrect-data-381151"></a>I læringsanalyse viser kurstypen og statusen feil data (381151)

Denne ukens utgivelser oppdaterte læringsanalyse slik at **kurstype** og **status** vises riktig.

### <a name="personnel-number-should-display-in-the-new-worker-form-banner-383832"></a>Personalnummer skal vises i banneret for Ny arbeider-skjema (383832)

I skjemaet **Ny arbeider** vises **Personalnummer** nå i banneret for hurtigreferanse.

### <a name="position-start-date-determines-the-job-record-to-use-when-retrieving-a-compensation-level-during-hire-350361"></a>Startdato for stilling bestemmer jobbposten som skal brukes ved henting av et kompensasjonsnivå under ansettelsesnivået (350361)

I denne versjonen bestemmer **startdato for kompensasjon** nivået som er tildelt den nye jobben.

### <a name="custom-pick-list-fields-in-the-position-table-arent-synchronized-to-common-data-service-387503"></a>Egendefinerte felt for plukkliste i stillingstabellen synkroniseres ikke med Common Data Service (387503)

I denne versjonen synkroniseres plukklistevarer nå med Common Data Service.

### <a name="worker-address-entity-doesnt-synchronize-with-common-data-service-while-importing-new-data-349673"></a>Arbeideradresseenhet synkroniserer ikke med Common Data Service ved import av nye data (349673)

I denne ukens utgivelse synkroniseres adressedata nå med Common Data Service ved import av nye data.

## <a name="in-preview"></a>I forhåndsvisning

### <a name="print-performance-reviews"></a>Skrive ut prestasjonsvurderinger

Se [Skrive ut prestasjonsvurderinger](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) i Dynamics 365: 2019-frigivelsesbølge 2-planen.
