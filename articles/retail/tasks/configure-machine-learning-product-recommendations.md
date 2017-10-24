--- 
title: " Konfigurere maskinlæringsbaserte produktanbefalinger"
description: "Denne prosedyren oppdaterer dataene i enhetsbutikken som brukes av maskinlæringssystemet som driver produktanbefalingene, og aktiverer deretter produktanbefalinger på salgsstedsklienter."
author: ashishmsft
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: e32c7cf1283487cb7a52f7d8e261b6b587b76364
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="configure-machine-learning-powered-product-recommendations"></a><span data-ttu-id="e5555-103"> Konfigurere maskinlæringsbaserte produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="e5555-103">Configure machine learning-powered product recommendations</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="e5555-104">Denne prosedyren oppdaterer dataene i enhetsbutikken som brukes av maskinlæringssystemet som driver produktanbefalingene, og aktiverer deretter produktanbefalinger på salgsstedsklienter.</span><span class="sxs-lookup"><span data-stu-id="e5555-104">This procedure refreshes the data in the Entity store that is used by the machine learning system that powers product recommendations, and then enables product recommendations on POS clients.</span></span> <span data-ttu-id="e5555-105">Denne prosedyren bruker firmaet USRT i demonstrasjonsdataene.</span><span class="sxs-lookup"><span data-stu-id="e5555-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="e5555-106">Gå til Systemadministrasjon > Oppsett > Enhetsbutikk.</span><span class="sxs-lookup"><span data-stu-id="e5555-106">Go to System administration > Setup > Entity Store.</span></span>
2. <span data-ttu-id="e5555-107">Finn og velg posten RetailSales i listen.</span><span class="sxs-lookup"><span data-stu-id="e5555-107">In the list, find and select the record 'RetailSales'.</span></span>
3. <span data-ttu-id="e5555-108">Klikk Oppdater.</span><span class="sxs-lookup"><span data-stu-id="e5555-108">Click Refresh.</span></span>
4. <span data-ttu-id="e5555-109">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="e5555-109">Click OK.</span></span>
5. <span data-ttu-id="e5555-110">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="e5555-110">Close the page.</span></span>
6. <span data-ttu-id="e5555-111">Gå til Detaljhandel og handel > Hovedkvarteroppsett > Parametere > Detaljhandelsparametere.</span><span class="sxs-lookup"><span data-stu-id="e5555-111">Go to Retail and commerce > Headquarters setup > Parameters > Retail parameters.</span></span>
7. <span data-ttu-id="e5555-112">Klikk kategorien Maskinlæring.</span><span class="sxs-lookup"><span data-stu-id="e5555-112">Click the Machine learning tab.</span></span>
8. <span data-ttu-id="e5555-113">Velg Ja i feltet Aktiver produktanbefalinger.</span><span class="sxs-lookup"><span data-stu-id="e5555-113">Select 'Yes' in the Enable product recommendations field.</span></span>
    * <span data-ttu-id="e5555-114">Hvis du får meldingen Kan ikke hente anbefalingsmodellene, er det fordi du nylig oppdaterte enhetsbutikken og systemet er kanskje ikke ferdig med å assimilere de nye dataene.</span><span class="sxs-lookup"><span data-stu-id="e5555-114">If you receive the message "The recommendation models couldn't be retrieved", it’s because you refreshed the Entity Store very recently and the system may not have finished assimilating the new data.</span></span> <span data-ttu-id="e5555-115">Vent 2–3 timer, og prøv på nytt.</span><span class="sxs-lookup"><span data-stu-id="e5555-115">Wait 2-3 hours and try again.</span></span>  
9. <span data-ttu-id="e5555-116">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="e5555-116">Click Save.</span></span>
10. <span data-ttu-id="e5555-117">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="e5555-117">Close the page.</span></span>


