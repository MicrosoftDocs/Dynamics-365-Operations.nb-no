---
title: Ordresperrer
description: "Dette emnet beskriver sperringer på ordrer ved hjelp av Detaljhandel og handel i Dynamics AX."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 79132
ms.assetid: 7c00dc35-73e5-400a-8587-22f37ddfc0e0
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 1cb18e3275b8dcdf0a61531ee056995f6e8fbc8d
ms.lasthandoff: 03/31/2017


---

# <a name="order-holds"></a>Ordresperrer

Dette emnet beskriver sperringer på ordrer ved hjelp av Detaljhandel og handel i Dynamics AX.

En ordre kan sperres av ulike årsaker. Du kan for eksempel sette en ordre på vent til kundens adresse eller betalingsmetode kan bekreftes, eller til en leder kan gå gjennom kundens kredittgrense. I løpet av salgsprosessen hender det at salgsordrer må settes på vent. En salgsordre kan for eksempel settes på vent på grunn av problemer med en kundebetaling, mistanke om svindel, eller for å vente på gjennomgang ved en leder. Når en salgsordre settes på vent, tilordnes en ordresperrekode til salgsordren for å angi årsaken til sperringen. Salgsordre hold koder er konfigurert på **salg og markedsføring**&gt;**Setup**&gt;**ordrer**&gt;**ordren inneholder koder**. En salgsordre kan sperres manuelt på tidspunktet for oppretting eller senere. I tillegg kan kan en ordre sperres automatisk, basert på regler for svindel. Når en ordre er på vent, må du kanskje oppdatere den med mer informasjon. Det kan også hende at du vil sjekke ut den salgsordren når du fortsetter å arbeide med den. Du kan sjekke ut en ordre, sjekke den inn igjen, og med overstyre utsjekkingen av en annen bruker ved å bruke rekkefølgen hold arbeidsbenk (**Retail og commerce**&gt;**kunder**&gt;**bestille sperringer**). Når en ordre er klar til å fullføres, må du fjerne sperringen før du kan fullføre ordreprosessen.


