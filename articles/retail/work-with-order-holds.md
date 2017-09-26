---
title: Ordresperrer
description: "Dette emnet beskriver sperringer på ordrer ved hjelp av Dynamics 365 for Retail."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 79132
ms.assetid: 7c00dc35-73e5-400a-8587-22f37ddfc0e0
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 59b51840c05fe649cf322bfa64737a321728a5aa
ms.openlocfilehash: c0c0e9a0f863eb33d544f63e40e0531cdaaf6426
ms.contentlocale: nb-no
ms.lasthandoff: 06/20/2017

---

# <a name="order-holds"></a>Ordresperrer

[!include[banner](includes/banner.md)]


Dette emnet beskriver sperringer på ordrer ved hjelp av Dynamics 365 for Retail.

En ordre kan sperres av ulike årsaker. Du kan for eksempel sette en ordre på vent til kundens adresse eller betalingsmetode kan bekreftes, eller til en leder kan gå gjennom kundens kredittgrense. I løpet av salgsprosessen hender det at salgsordrer må settes på vent. En salgsordre kan for eksempel settes på vent på grunn av problemer med en kundebetaling, mistanke om svindel, eller for å vente på gjennomgang ved en leder. Når en salgsordre settes på vent, tilordnes en ordresperrekode til salgsordren for å angi årsaken til sperringen. Sperrekoder for salgsordre konfigureres på **Salg og markedsføring** &gt; **Oppsett** &gt; **Salgsordrer** &gt; **Koder for ordresperringer**. En salgsordre kan sperres manuelt på tidspunktet for oppretting eller senere. I tillegg kan kan en ordre sperres automatisk, basert på regler for svindel. Når en ordre er på vent, må du kanskje oppdatere den med mer informasjon. Det kan også hende at du vil sjekke ut den salgsordren når du fortsetter å arbeide med den. Du kan sjekke ut en salgsordre, sjekke den inn igjen, og også overstyre utsjekkingen av en annen bruker ved å bruke arbeidsområde for ordresperre (**Detaljhandel** &gt; **Kunder** &gt; **Ordresperrer**). Når en ordre er klar til å fullføres, må du fjerne sperringen før du kan fullføre ordreprosessen.




