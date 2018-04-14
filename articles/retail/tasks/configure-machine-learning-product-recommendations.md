--- 
title: " Konfigurere maskinlæringsbaserte produktanbefalinger"
description: "Denne prosedyren oppdaterer dataene i enhetsbutikken som brukes av maskinlæringssystemet som driver produktanbefalingene, og aktiverer deretter produktanbefalinger på salgsstedsklienter."
author: ashishmsft
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 854b396a847c0764f1eea2a6fc57c68226800d29
ms.contentlocale: nb-no
ms.lasthandoff: 04/13/2018

---
# <a name="configure-machine-learning-powered-product-recommendations"></a><span data-ttu-id="5a175-103"> Konfigurere maskinlæringsbaserte produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="5a175-103">Configure machine learning-powered product recommendations</span></span>

[!INCLUDE [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="5a175-104">Denne prosedyren oppdaterer dataene i enhetsbutikken som brukes av maskinlæringssystemet som driver produktanbefalingene, og aktiverer deretter produktanbefalinger på salgsstedsklienter.</span><span class="sxs-lookup"><span data-stu-id="5a175-104">This procedure refreshes the data in the Entity store that is used by the machine learning system that powers product recommendations, and then enables product recommendations on POS clients.</span></span> <span data-ttu-id="5a175-105">Denne prosedyren bruker firmaet USRT i demonstrasjonsdataene.</span><span class="sxs-lookup"><span data-stu-id="5a175-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="5a175-106">Gå til Systemadministrasjon > Oppsett > Enhetsbutikk.</span><span class="sxs-lookup"><span data-stu-id="5a175-106">Go to System administration > Setup > Entity Store.</span></span>
2. <span data-ttu-id="5a175-107">Finn og velg posten RetailSales i listen.</span><span class="sxs-lookup"><span data-stu-id="5a175-107">In the list, find and select the record 'RetailSales'.</span></span>
3. <span data-ttu-id="5a175-108">Klikk Oppdater.</span><span class="sxs-lookup"><span data-stu-id="5a175-108">Click Refresh.</span></span>
4. <span data-ttu-id="5a175-109">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="5a175-109">Click OK.</span></span>
5. <span data-ttu-id="5a175-110">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="5a175-110">Close the page.</span></span>
6. <span data-ttu-id="5a175-111">Gå til Detaljhandel og handel > Hovedkvarteroppsett > Parametere > Detaljhandelsparametere.</span><span class="sxs-lookup"><span data-stu-id="5a175-111">Go to Retail and commerce > Headquarters setup > Parameters > Retail parameters.</span></span>
7. <span data-ttu-id="5a175-112">Klikk kategorien Maskinlæring.</span><span class="sxs-lookup"><span data-stu-id="5a175-112">Click the Machine learning tab.</span></span>
8. <span data-ttu-id="5a175-113">Velg Ja i feltet Aktiver produktanbefalinger.</span><span class="sxs-lookup"><span data-stu-id="5a175-113">Select 'Yes' in the Enable product recommendations field.</span></span>
    * <span data-ttu-id="5a175-114">Hvis du får meldingen Kan ikke hente anbefalingsmodellene, er det fordi du nylig oppdaterte enhetsbutikken og systemet er kanskje ikke ferdig med å assimilere de nye dataene.</span><span class="sxs-lookup"><span data-stu-id="5a175-114">If you receive the message "The recommendation models couldn't be retrieved", it’s because you refreshed the Entity Store very recently and the system may not have finished assimilating the new data.</span></span> <span data-ttu-id="5a175-115">Vent 2–3 timer, og prøv på nytt.</span><span class="sxs-lookup"><span data-stu-id="5a175-115">Wait 2-3 hours and try again.</span></span>  
9. <span data-ttu-id="5a175-116">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="5a175-116">Click Save.</span></span>
10. <span data-ttu-id="5a175-117">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="5a175-117">Close the page.</span></span>


