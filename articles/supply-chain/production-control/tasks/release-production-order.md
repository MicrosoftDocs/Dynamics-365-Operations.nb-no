---
title: Frigi en produksjonsordre
description: "Denne fremgangsmåten viser hvordan du frigir en produksjonsordre."
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
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: dadf0e87eac8522f61bb094c146e37f46a21fc09
ms.openlocfilehash: 6e628d8564c093c5d75fffe268b2107262d508c3
ms.contentlocale: nb-no
ms.lasthandoff: 02/06/2018

---
# <a name="release-a-production-order"></a>Frigi en produksjonsordre

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåten viser hvordan du frigir en produksjonsordre. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten. Dette er den fjerde fremgangsmåten av sju som forklarer livssyklusen for produksjonsordren.

1. Gå til Produksjonskontroll > Produksjonsordrer > Alle produksjonsordrer.
    * Velg en produksjonsordre som har statusen Planlagt, i rutenettet.  
2. Klikk Produksjonsordre i handlingsruten.
3. Klikk Frigi.
    * På denne siden kan du kontrollere frigivelsen av det merkede området for produksjonsordrer. Klikk Velg hvis du vil legge til ordrer.  
    * Frigivelsestrinnet angir når produksjonsordren frigis til produksjon-Shop Floor, slik at Shop Floor-operatørene kan rapportere fremdrift om produksjonsjobbene. Produksjonspapirer som inneholder relevant informasjon om behandling av jobbene, kan utstedes. Lagerarbeidet for plukking av råvarer genereres for varer som er definert for lagerprosessen.  
4. Klikk kategorien Generelt.
    * Velg hvilke produksjonsrapporter som skal skrives ut. Jobbkortrapporten skriver ut en side for hver planlagte jobb, og krever at produksjonsordren planlegges på jobbnivået. Rapporten inneholder informasjon om planlagt start- og sluttidspunkt, antallet som skal produseres, og hvilken ressurs som behandler jobben. Rutejobbrapporten samler inn samme informasjon på samme side, men skriver ikke ut en side for hver jobb. Rutekortrapporten viser bare operasjoner, men ikke jobbene. Denne rapporten krever derfor ikke finplanlegging, men kan brukes når produksjonsordrer er planlagt på operasjonsnivået.  
5. Klikk i boksen Skriv ut rutekort.
6. Klikk OK.
7. Lukk siden.

