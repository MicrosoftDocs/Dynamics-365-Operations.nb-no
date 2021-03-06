---
title: Lagerbrikkeopptelling
description: Dette emnet inneholder informasjon om brikkeopptelling, som du bruker til å sammenligne det faktiske innholdet i et lager med lagerbeholdningen.
author: MarkusFogelberg
ms.date: 06/10/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventJournalCount, InventJournalCountTag
audience: Application User
ms.reviewer: kamaybac
ms.custom: 11594
ms.assetid: 03772d0e-5c37-454c-ab85-82bc8b60a76d
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1df4a97dee3dc24856a1b40f3dc8dd095338b614
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5825969"
---
# <a name="inventory-tag-counting"></a>Lagerbrikkeopptelling

[!include [banner](../includes/banner.md)]

Dette emnet inneholder informasjon om brikkeopptelling, som du bruker til å sammenligne det faktiske innholdet i et lager med lagerbeholdningen.

Ved å lage linjer på **Brikkeopptelling**-siden plasserer du et brikkenummer på hver lagervare, for eksempel et tall fra 1 til 500. Når du teller, angir du varenummeret og antallet på en tilsvarende brikke. Denne brikken kan deretter brukes som grunnlag for inndata i brikkeopptellingsjournalen. Når du har postert brikkeopptellingsjournalen, opprettes en ny opptellingsjournal på **Opptelling**-siden. Den nye journalen er basert på brikkeopptellingsjournallinjene du opprettet. Hvis du teller varer ved hjelp av brikker etter en bestemt lagerdimensjon, velger du dimensjonen på **Visningsdimensjoner**-siden som vises når du oppretter brikkeopptellingsjournalen. Hvis du for eksempel vil telle varer på et bestemt lager, merker du av for **Lager**. Hvis glidebryteren **Lås varer under opptelling** på siden **Parametere for beholdnings- og lagerstyring** er valgt, kan ikke varer oppdateres fysisk under tellingen. Varer i brikkeopptellingsjournaler er imidlertid ikke låst under telling. Lagertransaksjoner opprettes ikke før brikkeopptellingslinjene er postert og overført til en opptellingsjournal. Hvis brikker er angitt i tilfeldig rekkefølge og du vil vite hvilke brikker som mangler, klikker du kolonnehodet **Brikke** for å sortere linjene etter brikke.

## <a name="additional-resources"></a>Tilleggsressurser

[Syklustelling](../warehousing/cycle-counting.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]