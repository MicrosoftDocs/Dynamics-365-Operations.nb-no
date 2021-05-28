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
ms.openlocfilehash: 6b643c4fe51ae6ce73b34ab81d4e458dcd5032df
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026782"
---
# <a name="you-cant-remove-the-warehouse-demand-forecast-dimension-from-forecast-lines"></a>Du kan ikke fjerne dimensjonen for lagerbehovsprognose fra prognoselinjer

KB-nummer: 4614408

## <a name="symptoms"></a>Symptomer

Dette problemet oppstår når **Lager**-dimensjonen ikke er tilordnet i kategorien **Prognosedimensjoner** på siden **Parametere for behovsprognose**. Likevel vises **Lager**-kolonnen på **Behovsprognose**-siden (**Hovedplanlegging \> Prognoser \> Manuell prognoseenhet \> Behovsprognoselinjer**).

## <a name="resolution"></a>Oppløsning

Innstillingene i kategorien **Prognosedimensjoner** på siden **Parametere for behovsprognose** påvirker ikke siden **Behovsprognose**. De kontrollerer basislinjeprognosen som genereres og vises i den justerte behovsprognosen. De kontrollerer imidlertid ikke dimensjonene som kreves for den "reelle" behovsprognosen. Ved å autorisere postene som vises på siden **Justert behovsprognose**, kan du konvertere dem til "reelle" prognoseoppføringer for en prognosemodell. Denne modellen kan deretter brukes til hovedplanlegging.

På **Behovsprognose**-siden vises dimensjonene for den "reelle" prognosen som vises på behovsprognoselinjene, en del av lagerdimensjonene. (Denne virkemåten likner på virkemåten for salgsordrelinjer.) Hvis systemopptellingen ikke er definert til å bruke **Lager** som en obligatorisk lagerdimensjon, kan du tilpasse siden for å skjule kolonnen.
