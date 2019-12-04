---
title: Kostnadsobjektdimensjoner
description: Når du analyserer kostnader, kan du bruke kostnadelementdimensjoner til å bestemme hvor kostnader flyter til. Du bruker kostnadsobjektdimensjoner brukes til å bestemme hvor du skal tildele kostnader. Dette emnet gir informasjon om kostnadsobjektdimensjoner.
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimensionMember
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 223174
ms.assetid: 2a1cdd35-30cb-41e7-9506-67fd04a537c5
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 6c15402993568c53eda8e03351fc2fccbcd82ab8
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770833"
---
# <a name="cost-object-dimensions"></a>Kostnadsobjektdimensjoner

[!include [banner](../includes/banner.md)]

Når du analyserer kostnader, kan du bruke kostnadelementdimensjoner til å bestemme hvor kostnader flyter til. Du bruker kostnadsobjektdimensjoner brukes til å bestemme hvor du skal tildele kostnader. Dette emnet gir informasjon om kostnadsobjektdimensjoner.

Et kostnadsobjekt kan være en hvilken som helst type objekt du vil beregne, fordele kostnader til eller måle direkte. Vanlige kostnadsobjekter omfatter produkter, prosjekter, ressurser, avdelinger, kostsentre og geografiske områder. Ledelsen bruker kostnadsobjekter til å kvantifisere kostnader og utføre fortjenesteanalyse.

## <a name="cost-object-dimensions-and-cost-object-dimension-members"></a>Kostnadsobjektdimensjoner og medlemmer av kostnadsobjektdimensjon
Kostobjekter kalles også *kostnadsobjektdimensjoner*. Etter at du har bestemt deg for hvilken enhet kostnadsobjektdimensjonen skal referere til, må du angi de individuelle dimensjonsverdiene eller importere dem til kostnadsregnskapet fra andre kildesystemer. Disse individuelle dimensjonsverdiene kalles *medlemmer av kostnadsobjektdimensjon*. Du vil for eksempel bruke finansdimensjonen som heter Kostsenter som kostnadsobjektdimensjon. Hvis du vil se hvordan kostnader flyter for individuelle kostsentre, må du importere medlemmene av kostnadsobjektdimensjonen. I så fall er medlemmene av kostnadsobjektdimensjonen de faktiske kostsentrene, for eksempel salg, produksjon, administrasjon og geografiske steder. Skjermbildet nedenfor viser et eksempel på kostsentre som kostnadsobjektdimensjonen med de faktiske kostsentrene som medlemmene av kostnadsobjektdimensjonen. 

[![Skjermbilde som viser kostsentre som kostnadsobjektdimensjon](./media/cost-object-dimensions.png)](./media/cost-object-dimensions.png)

## <a name="import-cost-object-dimension-members-through-data-connectors"></a>Importere medlemmer av kostnadsobjektdimensjon gjennom datakoblinger
Hvis du vil gjøre import av medlemmer av kostnadsobjektdimensjon enklere, kan du bruke datakoblinger til å hente verdiene fra enhetene som du vil bruke som kostnadsobjektdimensjoner. Du kan bruke det forhåndsbygde datakoblingene eller egendefinerte koblinger som du bygger.



