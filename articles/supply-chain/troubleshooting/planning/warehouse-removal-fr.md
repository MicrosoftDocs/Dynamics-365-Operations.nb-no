---
title: Du kan ikke fjerne dimensjonen for lagerbehovsprognose fra prognoselinjer
description: Du kan ikke fjerne dimensjonen for lagerbehovsprognose fra prognoselinjer.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ForecastSales
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 96af593d2e8a738258fe614f0f252620cb48c5f19eeb4425c9659ee6f9cd8c0c
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6741219"
---
# <a name="you-cant-remove-the-warehouse-demand-forecast-dimension-from-forecast-lines"></a>Du kan ikke fjerne dimensjonen for lagerbehovsprognose fra prognoselinjer

KB-nummer: 4614408

## <a name="symptoms"></a>Symptomer

Dette problemet oppstår når **Lager**-dimensjonen ikke er tilordnet i kategorien **Prognosedimensjoner** på siden **Parametere for behovsprognose**. Likevel vises **Lager**-kolonnen på **Behovsprognose**-siden (**Hovedplanlegging \> Prognoser \> Manuell prognoseenhet \> Behovsprognoselinjer**).

## <a name="resolution"></a>Oppløsning

Innstillingene i kategorien **Prognosedimensjoner** på siden **Parametere for behovsprognose** påvirker ikke siden **Behovsprognose**. De kontrollerer basislinjeprognosen som genereres og vises i den justerte behovsprognosen. De kontrollerer imidlertid ikke dimensjonene som kreves for den "reelle" behovsprognosen. Ved å autorisere postene som vises på siden **Justert behovsprognose**, kan du konvertere dem til "reelle" prognoseoppføringer for en prognosemodell. Denne modellen kan deretter brukes til hovedplanlegging.

På **Behovsprognose**-siden vises dimensjonene for den "reelle" prognosen som vises på behovsprognoselinjene, en del av lagerdimensjonene. (Denne virkemåten likner på virkemåten for salgsordrelinjer.) Hvis systemopptellingen ikke er definert til å bruke **Lager** som en obligatorisk lagerdimensjon, kan du tilpasse siden for å skjule kolonnen.
