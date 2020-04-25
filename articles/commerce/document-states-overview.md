---
title: Dokumentere statuser og livssyklus
description: Dette emnet dekker de ulike dokumenttilstandene for sideelementer i Microsoft Dynamics 365 Commerce.
author: phinneyridge
manager: annbe
ms.date: 04/13/2020
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
ms.openlocfilehash: 4a00f1c363e5ecb0e3e64637a8f487c48df2df72
ms.sourcegitcommit: ac966ea3a6c557fb5f9634b187b0e788d3e82d4d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/14/2020
ms.locfileid: "3261519"
---
# <a name="document-states-and-lifecycle"></a>Dokumentere statuser og livssyklus


[!include [banner](includes/banner.md)]

Dette emnet dekker de ulike dokumenttilstandene for sideelementer i Microsoft Dynamics 365 Commerce.

## <a name="document-state-descriptions"></a>Beskrivelse av dokumenttilstand

Emnet [Sideelementer](page-elements-overview.md) viser ulike dokumenttyper i innholdsbehandlingssystemet (CMS). Disse dokumenttypene kan ha flere tilstander i redigeringsverktøyet. Dokumentstatusen bidrar til å hindre datakonflikter og bruk av versjonskontroll. De bestemmer hvem som kan endre dokumentene, når dokumentene kan endres, og når endringer kan vises av andre personer.

Følgende tabell viser mulige dokumenttilstander for sideelementer i Commerce.

| Dokumenttilstand      | Handling i områdebygger        | beskrivelse                                                  |
| ------------------- | -------------------------- | ------------------------------------------------------------ |
| Sjekket ut         | Velg **Rediger**.           | Det aktuelle dokumentet er sjekket ut til deg. Mens et dokument er i denne tilstanden, kan det ikke endres av andre godkjente systembrukere, og endringer du utfører i dokumentet, er bare synlige for deg. |
| Lagret               | Velg **Lagre**.           | Endringer som er gjort i et utsjekket dokument, blir lagret i databasen, men dokumentet er ennå ikke sjekket inn eller publisert. De lagrede endringene er ikke synlige for andre godkjente systembrukere før forfatteren velger **Fullfør redigering**. De er ikke synlige for eksterne brukere før elementet er publisert. |
| Forkastet utsjekking | Velg **Forkast redigeringer**.  | Alle endringer i det utsjekkede dokumentet forkastes, og varen tilbakestilles til den siste versjonen som ble sjekket inn. |
| Sjekket inn          | Velg **Fullfør redigering**. | Det redigerte dokumentet sjekkes inn. Alle endringer er synlige for andre godkjente systembrukere, og disse brukerne kan deretter redigere dokumentet. Hver innsjekking oppretter en dokumentversjonsregistrering i elementloggen. |
| Publisert           | Velg **Publiser**.        | Dokumentet publiseres, og endringene sendes ut på det aktive området og blir synlige for eksterne brukere. Varer kan bare publiseres hvis de først har blitt sjekket inn ved å velge **Fullfør redigering**. |

## <a name="additional-resources"></a>Tilleggsressurser

[Måter å legge til innhold på](add-manage-content.md)

[Ordliste for sidemodell](page-elements-overview.md)

[Arbeide med publiseringsgrupper](publish-groups.md)

[Arbeide med moduler](work-with-modules.md)

[Arbeide med fragmenter](work-with-fragments.md)

[Oversikt over maler og oppsett](templates-layouts-overview.md)

[Tilpasse områdenavigering](customize-site-navigation.md)
