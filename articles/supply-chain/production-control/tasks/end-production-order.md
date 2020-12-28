---
title: Avslutte en produksjonsordre
description: Denne fremgangsmåten viser hvordan du avslutter en produksjonsordre.
author: johanhoffmann
manager: tfehr
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fade659c320e0ea1059644324859c9a3cb273c96
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4434107"
---
# <a name="end-a-production-order"></a>Avslutte en produksjonsordre

[!include [banner](../../includes/banner.md)]

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
