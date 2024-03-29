---
title: Lagerlokasjoner
description: Lagerlokasjoner brukes med grunnleggende lageraktiviteter (WMS I) til å angi hvor varene er lagret, og der varer hentes fra i et WMS I-lager.
author: yufeihuang
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WMSLocation, WMSBlockingCause, WHSLocation
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2134
ms.assetid: 69bf6922-4151-447f-b678-4ba95637f54c
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bd5ad086cadd2e49585614e7650bb7e30a4e7328
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8888593"
---
# <a name="inventory-locations"></a>Lagerlokasjoner

[!include [banner](../includes/banner.md)]

Lagerlokasjoner brukes med grunnleggende lageraktiviteter (WMS I) til å angi hvor varene er lagret, og der varer hentes fra i et WMS I-lager.

Denne artikkelen gjelder funksjoner i beholdningstyringsmodulen. Det gjelder ikke for funksjoner i lagerstyringsmodulen.

Termen lokasjon brukes om et sted der varer lagres og hentes fra.

For hver lokasjon kan stedet der varen legges inn, også angis. De er som standard like. Varer legges vanligvis inn og hentes fra den samme siden av en lokasjon, men ikke alltid. Varer som for eksempel er lagret på lagringsreoler legges inn fra én gang, og hentes fra en annen. De viktigste inndataene angis ved et lokasjonsnavn som vanligvis bestemmes av lokasjonens koordinater: lager, gang, reol, hylle og boks.. Dette navnet eller denne IDen kan angis manuelt, eller genereres fra lokasjonskoordinatene, for eksempel 01-02-03-4 for gang 1, reol 2, hylle 3, posisjon 4 på Lagerlokasjoner-siden.
Lokasjonsegenskaper

En lokasjon har følgende kjennetegn:
-   Størrelse (høyde, bredde, dybde og dermed volum)
-   Lager, gang, reol, hylle og boksposisjon
-   Lokasjonstype (bulklokasjon, plukklokasjon, mottakssone, utleveringsport, produksjonsinnleveringssted, inspeksjonslokasjon eller kanban-supermarked)

Du kan bruke kontrolltekst i online-systemer til å kontrollere at operatøren har valgt riktig lokasjon for en bestemt vare. Denne kontrollteksten kan opprettes manuelt eller det brukes som standardtekst.

## <a name="sort-codes"></a>Sorteringskoder
Bruk sorteringskoder for å optimalisere håndteringen av plukklinjer, som beskriver informasjonen som kreves for plukking av varer fra lager, inkludert plukkordren. Sorteringskoder kan angis etter gangen og andre koordinater, eller tilordnes manuelt for lokasjonen.

## <a name="blocked-locations"></a>Blokkerte lokasjoner
Noen ganger vil du kanskje angi at en lokasjon er blokkert for en tidsperiode, for eksempel ved reparasjon. Andre ganger vil du kanskje angi at du vil blokkere bare innleveringen eller utleveringen.

## <a name="tree-structure"></a>Trestruktur

På Lagerlokasjoner-siden kan du vise lageroppsettet i en trestruktur basert på koordinatene for lagerlokasjoner, i et definert visningsformat.

## <a name="maintain-inventory-locations-via-the-warehouse-form"></a>Vedlikeholde lagerlokasjoner via lagerskjemaet

Det er mulig å kopiere lokasjoner fra ett lager til et annet og opprette lokasjoner via en veiviser. Før du kjører veiviseren, må du kontrollere at du har definert navnene på standardlokasjon på Lager-siden.



## <a name="additional-resources"></a>Tilleggsressurser

[Opprette et nytt lageroppsett](tasks/create-new-warehouse-layout.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]