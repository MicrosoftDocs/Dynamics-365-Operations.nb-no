---
title: Aktivere manuell publisering av vurderinger og vurderinger av en moderator
description: Dette emnet beskriver hvordan du aktiverer manuell publisering av vurderinger og omtaler av en moderator i Microsoft Dynamics 365 Commerce, og hvordan du publiserer vurderinger og omtaler manuelt.
author: gvrmohanreddy
manager: annbe
ms.date: 09/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-09-03
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 0709173b8c3dfb7018d0bd9a712554112722a1f3
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/04/2022
ms.locfileid: "8693288"
---
# <a name="enable-manual-publishing-of-ratings-and-reviews-by-a-moderator"></a>Aktivere manuell publisering av vurderinger og vurderinger av en moderator

[!include [banner](includes/banner.md)]

Dette emnet beskriver hvordan du aktiverer manuell publisering av vurderinger og omtaler av en moderator i Microsoft Dynamics 365 Commerce, og hvordan du publiserer vurderinger og omtaler manuelt.

Dynamics 365 Commerce sin løsning for vurderinger og omtaler bruker Azure Cognitive Services til å automatisk fjerne upassende ord i gjennomgangstitler og -innhold, og til å publisere vurderinger og omtaler. Derfor er ikke manuell inngripen nødvendig for å gå gjennom og publisere vurderinger og omtaler på e-handelsområdet.

Det kan imidlertid hende at enkelte selskaper foretrekker at selskaper gjennomgår og godkjenner omtaler manuelt før de publiseres. Hvis du vil aktivere manuell publisering av vurderinger og omtaler av en moderator, må du aktivere funksjonen **Krev moderator for vurderinger og omtaler** i Commerce-områdebyggeren.

## <a name="enable-the-require-moderator-for-ratings-and-reviews-feature-in-commerce-site-builder"></a>Aktivere funksjonen Krev moderator for vurderinger og omtaler i Commerce-områdebygger

Følg denne fremgangsmåten for å aktivere funksjonen **Krev moderator for vurderinger og omtaler** i Commerce-områdebygger.

1. Gå til **Hjem \> Omtaler \> Innstillinger**.
1. Sett alternativet **Krev moderator for vurderinger og omtaler** til **På**.

> [!NOTE]
> Ved å aktivere funksjonen **Krev moderator for vurderinger og omtaler** stopper du automatisk publisering av vurderinger og omtaler, slik at manuell publisering nå kreves. Imidlertid vil Azure Cognitive Services fortsette med å fjerne upassende ord i gjennomgangstitler og -innhold.

<!--![Require moderator for ratings and reviews setting in Commerce site builder.](media/Ratings-reviews-settings-human-moderation.png)-->

## <a name="publish-ratings-and-reviews"></a>Publisere vurderinger og omtaler

Når du aktiverer funksjonen **Krev moderator for vurderinger og omtaler** må en moderator manuelt vurdere og publisere vurderinger og omtaler i e-handelsområdet.

Gjør følgende for å gå gjennom og publisere vurderinger og omtaler i Commerce-områdebygger:

1. Gå til **Omtaler \> Sensur**.
1. Hvis **Status**-feltet for en rad er satt til **Upublisert** i rutenettet, er vurderingen og gjennomgangen i denne raden ikke publisert ennå. Hvis du bare vil vise upubliserte vurderinger og omtaler, velger du **Status: Trenger gjennomgang** i statusfilteret over rutenettet.
1. Velg én eller flere vurderinger og omtaler med statusen **Upublisert**, og velg deretter **Publiser** på kommandolinjen. De valgte vurderingene og omtalene legges til i publiseringskøen og vises på e-handelsområdet etter at de er publisert.

> [!NOTE]
> - Når en vurdering og omtale er publisert, endres statusverdien fra **Upublisert** til en nullverdi (tomt felt).
> - Hvis du velger flere vurderinger og omtaler som har forskjellige statuser, og deretter velger **Publiser**, vil vurderinger og omtaler som ikke er publisert ennå, bli publisert. Vurderinger og omtaler som allerede er publisert, vil imidlertid ikke bli publisert på nytt.

Illustrasjonen nedenfor viser et eksempel der tre upubliserte vurderinger og omtaler velges på **Sensur**-siden i Commerce-områdebygger.

![Tre upubliserte vurderinger og omtaler valgt på Sensur-siden i Commerce-områdebygger.](media/Ratings-reviews-publishing-reviews.png)

<!--![Dynamics 365 Commerce - Ratings and Review configuration 2](media/Ratings-reviews-published-reviews.png)-->
<!--![Status filter](media/Ratings-reviews-published-reviews-status-filter.png)-->

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over vurderinger og anmeldelser](ratings-reviews-overview.md)

[Velge å bruke vurderinger og anmeldelser](opt-in-ratings-reviews.md)

[Administrere vurderinger og anmeldelser](manage-reviews.md)

[Konfigurere vurderinger og anmeldelser](configure-ratings-reviews.md)

[Synkronisere produktvurderinger](sync-product-ratings.md)

[Importer og eksporter vurderinger og omtaler](import-export-reviews.md)

[Konfigurer tjeneste-til-tjeneste-godkjenning](service-to-service-auth.md)

[Vanlige spørsmål om rangeringer og anmeldelser](ratings-reviews-faq.md)
