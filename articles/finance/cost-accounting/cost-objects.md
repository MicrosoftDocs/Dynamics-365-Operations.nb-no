---
title: Kostnadsobjektdimensjoner
description: Når du analyserer kostnader, kan du bruke kostnadelementdimensjoner til å bestemme hvor kostnader flyter til. Du bruker kostnadsobjektdimensjoner brukes til å bestemme hvor du skal tildele kostnader. Denne artikkelen gir informasjon om kostnadsobjektdimensjoner.
author: AndersGirke
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CAMDimensionMember, CAMCostObject
audience: Application User
ms.reviewer: twheeloc
ms.custom: 223174
ms.assetid: 2a1cdd35-30cb-41e7-9506-67fd04a537c5
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: twheeloc
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 3ee481b9dafe202e0a850a31b6ab036d52a20547
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8874645"
---
# <a name="cost-object-dimensions"></a>Dimensjoner for kostnadsobjekt

[!include [banner](../includes/banner.md)]

Når du analyserer kostnader, kan du bruke kostnadelementdimensjoner til å bestemme hvor kostnader flyter til. Du bruker kostnadsobjektdimensjoner brukes til å bestemme hvor du skal tildele kostnader. Denne artikkelen gir informasjon om kostnadsobjektdimensjoner.

Et kostnadsobjekt kan være en hvilken som helst type objekt du vil beregne, fordele kostnader til eller måle direkte. Vanlige kostnadsobjekter omfatter produkter, prosjekter, ressurser, avdelinger, kostsentre og geografiske områder. Ledelsen bruker kostnadsobjekter til å kvantifisere kostnader og utføre fortjenesteanalyse.

## <a name="cost-object-dimensions-and-cost-object-dimension-members"></a>Kostnadsobjektdimensjoner og medlemmer av kostnadsobjektdimensjon
Kostobjekter kalles også *kostnadsobjektdimensjoner*. Etter at du har bestemt deg for hvilken enhet kostnadsobjektdimensjonen skal referere til, må du angi de individuelle dimensjonsverdiene eller importere dem til kostnadsregnskapet fra andre kildesystemer. Disse individuelle dimensjonsverdiene kalles *medlemmer av kostnadsobjektdimensjon*. Du vil for eksempel bruke finansdimensjonen som heter Kostsenter som kostnadsobjektdimensjon. Hvis du vil se hvordan kostnader flyter for individuelle kostsentre, må du importere medlemmene av kostnadsobjektdimensjonen. I så fall er medlemmene av kostnadsobjektdimensjonen de faktiske kostsentrene, for eksempel salg, produksjon, administrasjon og geografiske steder. Skjermbildet nedenfor viser et eksempel på kostsentre som kostnadsobjektdimensjonen med de faktiske kostsentrene som medlemmene av kostnadsobjektdimensjonen. 

[![Skjermbilde som viser kostsentre som kostnadsobjektdimensjon.](./media/cost-object-dimensions.png)](./media/cost-object-dimensions.png)

## <a name="import-cost-object-dimension-members-through-data-connectors"></a>Importere medlemmer av kostnadsobjektdimensjon gjennom datakoblinger
Hvis du vil gjøre import av medlemmer av kostnadsobjektdimensjon enklere, kan du bruke datakoblinger til å hente verdiene fra enhetene som du vil bruke som kostnadsobjektdimensjoner. Du kan bruke det forhåndsbygde datakoblingene eller egendefinerte koblinger som du bygger.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
