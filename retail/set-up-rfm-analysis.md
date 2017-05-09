---
title: Konfigurere RFM-analyse
description: Dette emnet forklarer hvordan du setter opp en recency-, frekvens- og pengeanalyse (RFM) av kundene dine.
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 78943
ms.assetid: 8ff9aac3-5ada-4150-85fd-18901c926d53
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: b95d2c4d7d78e8c5ed8d3a04efdd2f8dfe8393ba
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-rfm-analysis"></a>Konfigurere RFM-analyse

[!include[banner](includes/banner.md)]


Dette emnet forklarer hvordan du setter opp en recency-, frekvens- og pengeanalyse (RFM) av kundene dine.

Recency-, frekvens- og pengeanalyse (RFM) er et markedsføringsverktøy organisasjonen kan bruke til å evaluere dataene som genereres av kundebestillinger. Når du har definert RFM-analyse, tilordnes kunder en beregnet RFM-poengsum når de gjør innkjøp. Poengsummen for tilbudsforespørselen kan være en tresifret vurdering eller et samlet tall, avhengig av hvordan organisasjonen har konfigurert analyse av tilbudsforespørsler. Hvis organisasjonen din bruker en tresifret vurdering for resultatet, er det første sifferet kundens recency rangering (hvor nylig kunden har gjort en bestilling fra organisasjonen). Det andre sifferet er kundens frekvensrangering (hvor ofte kunden kjøper fra organisasjonen). Det tredje sifferet er kundens pengerangering (hvor mye kundene bruker når de foretar kjøp fra organisasjonen). Organisasjonen har for eksempel satt vurderingene på en skala fra 1 til 5, der 5 er den høyeste klassifiseringen. I dette tilfellet forteller en kunde vurdering på 535 deg følgende informasjon om kunden:

-   **Recency-rangering på 5** – Kunden har handlet nylig.
-   **Frekvensrangering på 3** – Kunden kjøper produkter fra organisasjonen med moderat hyppighet.
-   **Pengerangering på 5** – når kundene kjøper noe, bruker de et betydelig pengebeløp.

Hvis organisasjonen bruker en sum av tallene, legges de individuelle rangeringene sammen. For det samme eksemplet har kunden en rangering på 13 (5 + 3 + 5).




