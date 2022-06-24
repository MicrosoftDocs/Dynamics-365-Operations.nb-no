---
title: Se gjennom statusen for et eksperiment
description: Denne artikkelen beskriver hvilken status et eksperiment har i livssyklusen for eksperimentering i Dynamics 365 Commerce.
author: sushma-rao
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 818435a7c901d2a6b876b9c9db27faffc8b322fc
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8877255"
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

[ ![Statuser for eksperimentering.](./media/experimentation_statuses.svg) ](./media/experimentation_statuses.svg#lightbox)


[!INCLUDE[footer-include](../includes/footer-banner.md)]