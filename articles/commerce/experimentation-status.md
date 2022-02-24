---
title: Se gjennom statusen for et eksperiment
description: Dette emnet beskriver hvilken status et eksperiment har i livssyklusen for eksperimentering i Dynamics 365 Commerce.
author: sushma-rao
manager: AnnBe
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 5ae29fe5ac49d92c261c59d115664b50e87880a0
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4965122"
---
# <a name="review-the-status-of-an-experiment"></a>Se gjennom statusen for et eksperiment
Det er mange trinn i forbindelse med konfigurering og kjøring av et eksperiment i Dynamics 365 Commerce. Hvis du vil ha informasjon om livssyklusen for eksperimentering, kan du se [Eksperimentering i Dynamics 365 Commerce](experimentation-overview.md).

Hvis du vil vite hvor et eksperimenter er i livssyklusen, velger du **Eksperimenter** i den venstre navisjonsruten i Commerce-områdebygger. En liste over eksperimenter vises med statusen for hvert eksperiment i både Commerce og tredjepartstjenesten som brukes til å gjøre det mulig å opprette eksperimenter, tilordne variasjoner og analysere data.

I kolonnen **Commerce-status** kan du vise verdiene nedenfor. 
- **Utkast** – Eksperimentet er koblet til en side eller et fragment i Commerce og redigeres.
- **Publisert** – Eksperimentvariasjonene er klare for visning på nettstedet. Hvis eksperimentet kjører i tredjepartstjenesten, vil brukere av nettstedet se en variasjon av siden eller fragmentet som er valgt av tredjepartstjenesten.
- **Ikke publisert** – Eksperimentet er ikke lenger tilgjengelig på nettstedet. Brukere av nettstedet ser bare standardversjonen av siden eller fragmentet selv om eksperimentet kjører i tredjepartstjenesten.
- **Fullført** - Eksperimentet er fullført, og en variasjon ble fremmet til å være aktiv for alle brukere av nettstedet.

På samme måte kan følgende verdier vises i kolonnen for **status for tredjepart** for å angi statusen for eksperimentene i tredjepartstjenesten.
- **Utkast** – Eksperimentet er konfigurert i tredjepartstjenesten, men er ikke startet.
- **Kjører** – Eksperimentet er startet i tredjepartstjenesten og samler inn data.
- **Stoppet midlertidig** – Eksperimentet er stoppet midlertidig og samler ikke inn data. Du må fortsette eksperimentet for at det skal fortsette å samle inn data.
- **Arkivert** – Eksperimentet er fullført, og det har blitt katalogisert i tredjepartstjenesten for fremtidig referanse.

Diagrammet nedenfor viser begge settene med statuser og hvordan de er relatert til hverandre.

[ ![Statuser for eksperimentering](./media/experimentation_statuses.svg) ](./media/experimentation_statuses.svg#lightbox)
