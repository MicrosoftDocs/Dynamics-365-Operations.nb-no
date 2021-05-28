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
# <a name="you-cant-remove-the-warehouse-demand-forecast-dimension-from-forecast-lines"></a><span data-ttu-id="a7625-103">Du kan ikke fjerne dimensjonen for lagerbehovsprognose fra prognoselinjer</span><span class="sxs-lookup"><span data-stu-id="a7625-103">You can't remove the Warehouse demand forecast dimension from forecast lines</span></span>

<span data-ttu-id="a7625-104">KB-nummer: 4614408</span><span class="sxs-lookup"><span data-stu-id="a7625-104">KB number: 4614408</span></span>

## <a name="symptoms"></a><span data-ttu-id="a7625-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="a7625-105">Symptoms</span></span>

<span data-ttu-id="a7625-106">Dette problemet oppstår når **Lager**-dimensjonen ikke er tilordnet i kategorien **Prognosedimensjoner** på siden **Parametere for behovsprognose**.</span><span class="sxs-lookup"><span data-stu-id="a7625-106">This issue occurs when the **Warehouse** dimension isn't assigned on the **Forecast dimensions** tab of the **Demand forecasting parameter** page.</span></span> <span data-ttu-id="a7625-107">Likevel vises **Lager**-kolonnen på **Behovsprognose**-siden (**Hovedplanlegging \> Prognoser \> Manuell prognoseenhet \> Behovsprognoselinjer**).</span><span class="sxs-lookup"><span data-stu-id="a7625-107">Nevertheless, the **Warehouse** column is shown on the **Demand forecast** page (**Master planning \> Forecasting \> Manual forecast entity \> Demand forecast lines**).</span></span>

## <a name="resolution"></a><span data-ttu-id="a7625-108">Oppløsning</span><span class="sxs-lookup"><span data-stu-id="a7625-108">Resolution</span></span>

<span data-ttu-id="a7625-109">Innstillingene i kategorien **Prognosedimensjoner** på siden **Parametere for behovsprognose** påvirker ikke siden **Behovsprognose**.</span><span class="sxs-lookup"><span data-stu-id="a7625-109">The settings on the **Forecast dimensions** tab of the **Demand forecasting parameter** page don't affect the **Demand forecast** page.</span></span> <span data-ttu-id="a7625-110">De kontrollerer basislinjeprognosen som genereres og vises i den justerte behovsprognosen.</span><span class="sxs-lookup"><span data-stu-id="a7625-110">They control the baseline forecast that is generated and shown in the adjusted demand forecast.</span></span> <span data-ttu-id="a7625-111">De kontrollerer imidlertid ikke dimensjonene som kreves for den "reelle" behovsprognosen.</span><span class="sxs-lookup"><span data-stu-id="a7625-111">However, they don't control the dimensions that are required for the "real" demand forecast.</span></span> <span data-ttu-id="a7625-112">Ved å autorisere postene som vises på siden **Justert behovsprognose**, kan du konvertere dem til "reelle" prognoseoppføringer for en prognosemodell.</span><span class="sxs-lookup"><span data-stu-id="a7625-112">By authorizing the records that are shown on the **Adjusted demand forecast** page, you can convert them to "real" forecast entries for a forecast model.</span></span> <span data-ttu-id="a7625-113">Denne modellen kan deretter brukes til hovedplanlegging.</span><span class="sxs-lookup"><span data-stu-id="a7625-113">That model can then be used for master planning.</span></span>

<span data-ttu-id="a7625-114">På **Behovsprognose**-siden vises dimensjonene for den "reelle" prognosen som vises på behovsprognoselinjene, en del av lagerdimensjonene.</span><span class="sxs-lookup"><span data-stu-id="a7625-114">On the **Demand forecast** page, the dimensions for the "real" forecast that are shown on the demand forecast lines are part of the inventory dimensions.</span></span> <span data-ttu-id="a7625-115">(Denne virkemåten likner på virkemåten for salgsordrelinjer.) Hvis systemopptellingen ikke er definert til å bruke **Lager** som en obligatorisk lagerdimensjon, kan du tilpasse siden for å skjule kolonnen.</span><span class="sxs-lookup"><span data-stu-id="a7625-115">(This behavior resembles the behavior for sales order lines.) If your system isn't set up to use **Warehouse** as a mandatory inventory dimension, you can customize the page to hide the column.</span></span>
