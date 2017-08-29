--- 
title: "Opprette en bestilling for en engangsleverandør"
description: "Denne fremgangsmåten viser hvordan du oppretter en bestilling manuelt for en engangsleverandør."
author: FrankDahl
manager: AnnBe
ms.date: 08/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 580dfe3680c36a32a24999bc8c266a38a07177fd
ms.contentlocale: nb-no
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-purchase-order-for-a-one-time-supplier"></a>Opprette en bestilling for en engangsleverandør

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåten viser hvordan du oppretter en bestilling manuelt for en engangsleverandør. Leverandøren opprettes automatisk med bestillingen, i stedet for å opprette leverandørkontoen manuelt. Bestillinger opprettes vanligvis av en innkjøpsagent. Eksemplet som vises i denne veiledningen, kan brukes i demonstrasjonsdatafirmaet USMF. Det er en forutsetning at kontoen for engangsleverandør er definert på siden Leverandørparametere.


## <a name="create-a-purchase-order-for-a-one-time-supplier"></a>Opprette en bestilling for en engangsleverandør
1. Gå til Innkjøp og leverandører > Bestillinger > Alle bestillinger.
2. Klikk Ny.
3. Velg Ja i feltet Engangsleverandør.
    * En leverandørkonto blir automatisk opprettet og tilordnet bestillingen. Leverandørkontoen blir opprettet basert på malen som er angitt i kategorien Generelt på siden Leverandørparametere.  
4. I Navn-feltet skriver du inn et unikt navn for leverandøren.
5. Klikk OK.
    * Bestillingen kan nå fullføres og behandles som hvilken som helst ordre. Det finnes ingen spesielle egenskaper som er relatert til hvordan dette gjøres. Fakturaen registrerer en forfallstransaksjon på leverandørkontoen som ble opprettet med ordren, og deretter behandles betalingen. Når dette er fullført, kan leverandørkontoen slettes. Dette gjøres vanligvis av leverandøravdelingen.  


