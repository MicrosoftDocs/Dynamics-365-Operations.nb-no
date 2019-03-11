---
title: Avslutte en produksjonsordre
description: Denne fremgangsmåten viser hvordan du avslutter en produksjonsordre.
author: johanhoffmann
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8f5cb4afdc0285a6ccf28dbd362df3799c0ecc74
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "357364"
---
# <a name="end-a-production-order"></a>Avslutte en produksjonsordre

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåten viser hvordan du avslutter en produksjonsordre. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten. Dette er den siste fremgangsmåten av sju som forklarer livssyklusen for produksjonsordren.


## <a name="end-a-production-order"></a>Avslutte en produksjonsordre
1. Gå til Produksjonskontroll > Produksjonsordrer > Alle produksjonsordrer.
    * Velg en produksjonsordre med statusen Ferdigmeldt.  
2. Klikk Produksjonsordre i handlingsruten.
3. Klikk Avslutt.
    * På denne siden kan du bekrefte at du vil avslutte produksjonsordren.  
4. Klikk kategorien Generelt.
5. Angi en dato i Dato-feltet.
6. Velg "Tildeling" i feltet Svinnmetode.
    * Når du velger metoden Tildeling, legges kostnadene fra de kasserte materialene til de ferdige varene.  
7. Klikk OK.

## <a name="validate-calculation-results"></a>Validere beregningsresultater
1. Klikk Styr kostnader i handlingsruten.
2. Klikk Vis kostnadssammenligning.
    * Når du har avsluttet produksjonsordren, kan du sammenligne den estimerte kostprisen mot den realiserte kostprisen for å få en oversikt over produksjonsavvikene.  
