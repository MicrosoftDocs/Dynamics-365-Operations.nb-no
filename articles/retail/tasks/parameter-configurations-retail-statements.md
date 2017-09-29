--- 
title: " Parameterkonfigurasjoner for detaljhandelsutdrag"
description: "Denne prosedyren beskriver konfigurasjoner for detaljhandelsparametere som påvirker hvordan detaljhandelsutdrag opprettes og posteres."
author: josaw1
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 731a3ec06efa103ba663df83240c77dfe78bb7cd
ms.contentlocale: nb-no
ms.lasthandoff: 08/29/2017

---
# <a name="parameter-configurations-for-retail-statements"></a><span data-ttu-id="ea5f0-103"> Parameterkonfigurasjoner for detaljhandelsutdrag</span><span class="sxs-lookup"><span data-stu-id="ea5f0-103">Parameter configurations for Retail statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="ea5f0-104">Denne prosedyren beskriver konfigurasjoner for detaljhandelsparametere som påvirker hvordan detaljhandelsutdrag opprettes og posteres.</span><span class="sxs-lookup"><span data-stu-id="ea5f0-104">This procedure demonstrates configurations for Retail parameters that affect how Retail statements get created and posted.</span></span> <span data-ttu-id="ea5f0-105">Denne prosedyren bruker demonstrasjonsfirmaet USRT.</span><span class="sxs-lookup"><span data-stu-id="ea5f0-105">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="ea5f0-106">Gå til Detaljhandel og handel > Hovedkvarteroppsett > Parametere > Detaljhandelsparametere.</span><span class="sxs-lookup"><span data-stu-id="ea5f0-106">Go to Retail and commerce > Headquarters setup  > Parameters > Retail parameters.</span></span>
2. <span data-ttu-id="ea5f0-107">Klikk kategorien Postering.</span><span class="sxs-lookup"><span data-stu-id="ea5f0-107">Click the Posting tab.</span></span>
    * <span data-ttu-id="ea5f0-108">Velg Ja hvis du vil postere de tidsbestemte rabattbeløpene spesielt.</span><span class="sxs-lookup"><span data-stu-id="ea5f0-108">Select "Yes" if you want to post the periodic discount amounts specifically.</span></span>  
    * <span data-ttu-id="ea5f0-109">Velg Standard for å bruke standardkontoer, eller velg Tidsbestemt hvis du vil definere hvilken konto som skal brukes for hver tidsbestemt rabatt.</span><span class="sxs-lookup"><span data-stu-id="ea5f0-109">Select "Standard" to use default accounts, or select "Periodic" if you want to define which account to use for each periodic discount.</span></span>  
    * <span data-ttu-id="ea5f0-110">Velg Sammendrag hvis lagerlinjer skal aggregeres når det er mulig.</span><span class="sxs-lookup"><span data-stu-id="ea5f0-110">Select "Summary" if inventory lines should get aggregated whenever possible.</span></span>  
    * <span data-ttu-id="ea5f0-111">Velg Ja hvis fakturaer og betalinger skal utlignes automatisk som en del av utdragsposteringsprosessen.</span><span class="sxs-lookup"><span data-stu-id="ea5f0-111">Select "Yes" if Invoices and Payments should get automatically settled as part of the Statement posting process.</span></span>  
    * <span data-ttu-id="ea5f0-112">Velg Ja hvis transaksjoner for safedeponering skal aggregeres.</span><span class="sxs-lookup"><span data-stu-id="ea5f0-112">Select "Yes" if Safe drop transactions should get aggregated.</span></span>  
    * <span data-ttu-id="ea5f0-113">Velg Ja hvis transaksjoner for bankdeponering skal aggregeres.</span><span class="sxs-lookup"><span data-stu-id="ea5f0-113">Select "Yes" if Bank drop transactions should get aggregated.</span></span>  
    * <span data-ttu-id="ea5f0-114">Velg Ja hvis du vil aktivere aggregering for utdragspostering.</span><span class="sxs-lookup"><span data-stu-id="ea5f0-114">Select "Yes" to turn aggregation on for Statement posting.</span></span>  
    * <span data-ttu-id="ea5f0-115">Velg Ja for å opprette og behandle order parallelt når utdrag posteres.</span><span class="sxs-lookup"><span data-stu-id="ea5f0-115">Select "Yes" to create and process orders in parallel when statements are posted.</span></span>  
    * <span data-ttu-id="ea5f0-116">Angi maksimalt antall order som skal behandles i hver satsvis jobboppgave.</span><span class="sxs-lookup"><span data-stu-id="ea5f0-116">Enter the maximum orders to be processed in each batch job task.</span></span>  
3. <span data-ttu-id="ea5f0-117">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="ea5f0-117">Click Save.</span></span>


