---
title: Dokumentere statuser og livssyklus
description: Dette emnet dekker de ulike dokumenttilstandene for sideelementer i Microsoft Dynamics 365 Commerce.
author: phinneyridge
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e3334e4284df681907d879ca2eab5cd12e764c99
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792829"
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

[Aktivere og bruke deling på tvers av kanal](cross-channel-sharing.md)

[Arbeide med moduler](work-with-modules.md)

[Arbeide med fragmenter](work-with-fragments.md)

[Oversikt over maler og oppsett](templates-layouts-overview.md)

[Tilpasse områdenavigering](customize-site-navigation.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]