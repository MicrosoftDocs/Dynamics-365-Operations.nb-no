---
title: " Parameterkonfigurasjoner for detaljhandelsutdrag"
description: Denne prosedyren beskriver konfigurasjoner for detaljhandelsparametere som påvirker hvordan detaljhandelsutdrag opprettes og posteres.
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6dacd2b80ca0d51d81d2bdf5bc2636b47da621ee
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1564299"
---
# <a name="parameter-configurations-for-retail-statements"></a><span data-ttu-id="b3186-103"> Parameterkonfigurasjoner for detaljhandelsutdrag</span><span class="sxs-lookup"><span data-stu-id="b3186-103">Parameter configurations for Retail statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="b3186-104">Denne prosedyren beskriver konfigurasjoner for detaljhandelsparametere som påvirker hvordan detaljhandelsutdrag opprettes og posteres.</span><span class="sxs-lookup"><span data-stu-id="b3186-104">This procedure demonstrates configurations for Retail parameters that affect how Retail statements get created and posted.</span></span> <span data-ttu-id="b3186-105">Denne prosedyren bruker demonstrasjonsfirmaet USRT.</span><span class="sxs-lookup"><span data-stu-id="b3186-105">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="b3186-106">Gå til Detaljhandel og handel > Hovedkvarteroppsett > Parametere > Detaljhandelsparametere.</span><span class="sxs-lookup"><span data-stu-id="b3186-106">Go to Retail and commerce > Headquarters setup  > Parameters > Retail parameters.</span></span>
2. <span data-ttu-id="b3186-107">Klikk kategorien Postering.</span><span class="sxs-lookup"><span data-stu-id="b3186-107">Click the Posting tab.</span></span>
    * <span data-ttu-id="b3186-108">Velg Ja hvis du vil postere de tidsbestemte rabattbeløpene spesielt.</span><span class="sxs-lookup"><span data-stu-id="b3186-108">Select "Yes" if you want to post the periodic discount amounts specifically.</span></span>  
    * <span data-ttu-id="b3186-109">Velg Standard for å bruke standardkontoer, eller velg Tidsbestemt hvis du vil definere hvilken konto som skal brukes for hver tidsbestemt rabatt.</span><span class="sxs-lookup"><span data-stu-id="b3186-109">Select "Standard" to use default accounts, or select "Periodic" if you want to define which account to use for each periodic discount.</span></span>  
    * <span data-ttu-id="b3186-110">Velg Sammendrag hvis lagerlinjer skal aggregeres når det er mulig.</span><span class="sxs-lookup"><span data-stu-id="b3186-110">Select "Summary" if inventory lines should get aggregated whenever possible.</span></span>  
    * <span data-ttu-id="b3186-111">Velg Ja hvis fakturaer og betalinger skal utlignes automatisk som en del av utdragsposteringsprosessen.</span><span class="sxs-lookup"><span data-stu-id="b3186-111">Select "Yes" if Invoices and Payments should get automatically settled as part of the Statement posting process.</span></span>  
    * <span data-ttu-id="b3186-112">Velg Ja hvis transaksjoner for safedeponering skal aggregeres.</span><span class="sxs-lookup"><span data-stu-id="b3186-112">Select "Yes" if Safe drop transactions should get aggregated.</span></span>  
    * <span data-ttu-id="b3186-113">Velg Ja hvis transaksjoner for bankdeponering skal aggregeres.</span><span class="sxs-lookup"><span data-stu-id="b3186-113">Select "Yes" if Bank drop transactions should get aggregated.</span></span>  
    * <span data-ttu-id="b3186-114">Velg Ja hvis du vil aktivere aggregering for utdragspostering.</span><span class="sxs-lookup"><span data-stu-id="b3186-114">Select "Yes" to turn aggregation on for Statement posting.</span></span>  
    * <span data-ttu-id="b3186-115">Velg Ja for å opprette og behandle order parallelt når utdrag posteres.</span><span class="sxs-lookup"><span data-stu-id="b3186-115">Select "Yes" to create and process orders in parallel when statements are posted.</span></span>  
    * <span data-ttu-id="b3186-116">Angi maksimalt antall order som skal behandles i hver satsvis jobboppgave.</span><span class="sxs-lookup"><span data-stu-id="b3186-116">Enter the maximum orders to be processed in each batch job task.</span></span>  
3. <span data-ttu-id="b3186-117">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="b3186-117">Click Save.</span></span>

