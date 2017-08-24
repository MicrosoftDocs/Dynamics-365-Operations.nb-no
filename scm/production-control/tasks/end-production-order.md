--- 
title: Avslutte en produksjonsordre
description: "Denne fremgangsmåten viser hvordan du avslutter en produksjonsordre."
author: johanhoffmann
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: a22db527d9ab80da9e3592eeef30b4675a3c39c8
ms.contentlocale: nb-no
ms.lasthandoff: 07/27/2017

---
# <a name="end-a-production-order"></a>Avslutte en produksjonsordre

[!include[task guide banner](../../includes/task-guide-banner.md)]

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


