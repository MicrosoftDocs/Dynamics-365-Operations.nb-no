---
title: Hva er nytt eller endret i Dynamics 365 Talent (23. oktober 2019)
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 10/23/2019
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
ms.search.validFrom: 2019-10-23
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 94243f83121a1306d8f9ae9be23d24e5c9b63a2d
ms.sourcegitcommit: 07e109dec176a93eff0df8a37ba5d875f212e9f1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/25/2019
ms.locfileid: "2662671"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-october-23-2019"></a>Hva er nytt eller endret i Dynamics 365 Talent (23. oktober 2019)

[!include [banner](includes/banner.md)]

Dette emnet beskriver funksjoner som enten er nye eller endret i Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Endringer i Attract
Denne versjonen inneholder mindre feilrettinger for Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Endringer i Onboard
Denne versjonen inneholder mindre feilrettinger for Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Endringer i Core HR

Endringer som er beskrevet i denne delen, gjelder build nummer 8.1.2569. Tallene i parentes i noen overskrifter refererer til støttenumre i Microsoft Dynamics Lifecycle Services (LCS).

### <a name="platform-update-30-for-finance-and-operations-apps"></a>Platform update 30 for Finance and Operations-apper

Hvis du vil ha mer informasjon, se [Hva er nytt eller endret i Platform Update 30 for Finance and Operations-apper (november 2019)](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/fin-ops/get-started/whats-new-platform-update-30).

### <a name="remove-benefits-open-enrollment-preview-feature"></a>Fjerne åpen registrering for fordeler fra offentlig forhåndsvisning

I forbindelse med vår kunngjøring i blogginnlegget Strategiske investeringene i Core HR gir til store driftsfordeler fjerner Microsoft funksjonen for åpen registrering av fordeler fra den offentlige forhåndsvisningen 18. oktober 2019. I stedet vil ny funksjonalitet bli utgitt i fremtiden. Produksjonsbruk av funksjonen for åpen registrering av fordeler som for øyeblikket er i den offentlige forhåndsvisningen, støttes ikke.

### <a name="error-while-selecting-the-countryregion-on-the-worker-form-a-second-time-350294"></a>Feil når land/område i arbeiderskjemaet velges én gang til (350294)

Ved hjelp av denne ukens frigivelsen er problemet rettet opp når du velger et land/område i **Arbeider**-skjemaet.

### <a name="financial-dimension-values-default-to-the-combination-display-field-when-do-not-allow-manual-entry-is-set-to-true-340097"></a>Finansdimensjonsverdier går som standard til kombinasjonsvisningsfeltet når Ikke tillat manuell registrering er angitt til sann (340097)

Med denne endringen vil systemet angi riktig standard dimensjonsverdi i **Kombinasjonsvisning**-feltet når du definerer finansdimensjoner og bruker alternativet for å ikke tillate manuell registrering.

### <a name="new-relationship-types-should-be-added-to-relationship-lookup-in-the-personal-contacts-form-347691"></a>Nye relasjonstyper skal legges til i relasjonsoppslag i skjemaet for personlige kontakter (347691)

Denne utgivelsen inneholder nye funksjoner for å legge til nye relasjonstyper i tabellen **Relasjonstyper** og gjenspeiler disse endringene i relasjonsoppslaget for personlige kontakter.

### <a name="additional-list-values-in-custom-fields-arent-reflected-in-common-data-service-379599"></a>Flere listeverdier i egendefinerte felt gjenspeiles ikke i Common Data Service (379599)

Med denne ukens utgivelse, der en ny listeverdi legges til i et eksisterende egendefinert felt som allerede er synkronisert med Common Data Service, vil de nye plukklisteverdiene nå vises etter at du har brukt endringer i enheten.

### <a name="on-the-terms-of-employment-page-all-employees-terms-of-employment-appear-after-selecting-open-in-excel-348073"></a>På siden Ansettelsesbetingelser vises alle ansattes ansettelsesbetingelser etter at Åpne i Excel er valgt (348073)

Med denne versjonen vil bare de valgte ansattes ansettelsesbetingelser åpnes i Excel. All selskapssikkerhet blir også respektert.

### <a name="the-association-between-the-work-calendar-holiday-entity-and-the-work-calendar-entity-is-missing-in-common-data-service---324178"></a>Tilknytningen mellom ferieenheten for arbeidskalenderen og enheten for arbeidskalenderen mangler i Common Data Service – (324178)

Denne relasjonen er lagt til i utgivelsen. Denne endringen vil gjøre det mulig å vise arbeidsdager for en ansatt i PowerApps. 

### <a name="error-when-using-employee-self-service-workflows-with-configurable-hierarchies-370132"></a>Feil ved bruk av arbeidsflyter for ansattselvbetjening med konfigurerbare hierarkier (370132)

I denne versjonen er bedre meldingsfunksjonalitet tilgjengelig for hvordan du konfigurerer arbeidsflyter ved hjelp av konfigurerbare hierarkier. 

### <a name="system-allows-creation-of-new-positions-where-the-available-for-assignment-date-is-earlier-than-the-activation-date-340103"></a>System tillater oppretting av nye stillinger der Tilgjengelig for tilordning-datoen er tidligere enn aktiveringsdatoen (340103)

Denne endringen vil vise en advarsel når **Tilgjengelig for tilordning**-datoen er før stillingens **Aktivering**-dato.

## <a name="coming-soon"></a>Kommer snart

### <a name="print-performance-reviews"></a>Skrive ut prestasjonsvurderinger

Se [Skrive ut prestasjonsvurderinger](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) i Dynamics 365: 2019-frigivelsesbølge 2-planen.

### <a name="feature-management-workspace"></a>Arbeidsområde for funksjonsbehandling

Funksjoner legges til og oppdateres i hver versjon. Funksjonsbehandling-opplevelsen gir et arbeidsområde der du kan vise en liste over funksjoner som er levert i hver versjon. Nye funksjoner er deaktivert som standard. Du kan bruke arbeidsområdet til å aktivere dem og vise dokumentasjonen for dem.

Hvis du vil ha mer informasjon om endringene som kommer med funksjonsbehandling, kan du se [Oversikt over funksjonsbehandling](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).
