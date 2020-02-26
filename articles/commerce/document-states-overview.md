---
title: Dokumentere statuser og livssyklus
description: Dette emnet dekker de ulike dokumenttilstandene for sideelementer i Microsoft Dynamics 365 Commerce.
author: phinneyridge
manager: annbe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: b4f1c462f734b2d58843308f0f877fe18a4d9af7
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002987"
---
# <a name="document-states-and-lifecycle"></a>Dokumentere statuser og livssyklus


[!include [banner](includes/banner.md)]

Dette emnet dekker de ulike dokumenttilstandene for sideelementer i Microsoft Dynamics 365 Commerce.

## <a name="document-state-descriptions"></a>Beskrivelse av dokumenttilstand

Emnet [Sideelementer](page-elements-overview.md) viser ulike dokumenttyper i innholdsbehandlingssystemet (CMS). Disse dokumenttypene kan ha flere tilstander i redigeringsverktøyet. Dokumentstatusen bidrar til å hindre datakonflikter og bruk av versjonskontroll. De bestemmer hvem som kan endre dokumentene, når dokumentene kan endres, og når endringer kan vises av andre personer.

Følgende tabell viser mulige dokumenttilstander for sideelementer i Commerce.

| Dokumenttilstand | Beskrivelse |
|---|---|
| Sjekket ut | Når en CMS-vare er sjekket ut til deg, kan den ikke redigeres av andre godkjente systembrukere. Endringer du utfører i elementet, er bare synlige for deg. |
| Sjekket inn | Når en CMS-vare sjekkes inn, er alle endringer synlige for andre godkjente systembrukere, og disse brukerne kan deretter sjekke ut elementet og redigere det. Hver innsjekking oppretter en dokumentversjonsregistrering i elementloggen. |
| Publisert | Når en CMS-vare publiseres, skyves den til det aktive området ditt og blir synlig på Internett for ikke-godkjente eksterne brukere. Elementer kan bare publiseres hvis de er sjekket inn. |
| Lagret | Endringer som er gjort i en utsjekket CMS-vare, kan lagres i CMS før varen sjekkes inn eller publiseres. Disse lagrede endringene er ikke synlige for andre godkjente systembrukere før varen sjekkes inn. De er ikke synlige for eksterne brukere før elementet er publisert. |
| Forkastet utsjekking | Når en utsjekket CMS-vare forkastes, slettes alle lagrede endringer, og varen tilbakestilles til den versjonen som sist ble sjekket inn. |

## <a name="additional-resources"></a>Tilleggsressurser

[Måter å legge til innhold på](add-manage-content.md)

[Ordliste for sidemodell](page-elements-overview.md)

[Arbeide med publiseringsgrupper](publish-groups.md)

[Arbeide med moduler](work-with-modules.md)

[Arbeide med fragmenter](work-with-fragments.md)

[Oversikt over maler og oppsett](templates-layouts-overview.md)

[Tilpasse områdenavigering](customize-site-navigation.md)
