---
title: " Definere fordelspoeng"
description: Denne prosedyren hjelper med å definere fordelspoeng.
author: scott-tucker
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailLoyaltyRewardPoints
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9557b25af0fba6429d34564e1a3e158b6258698a
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023536"
---
# <a name="define-loyalty-reward-points"></a><span data-ttu-id="2b9ed-103"> Definere fordelspoeng</span><span class="sxs-lookup"><span data-stu-id="2b9ed-103">Define loyalty reward points</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="2b9ed-104">Denne prosedyren hjelper med å definere fordelspoeng.</span><span class="sxs-lookup"><span data-stu-id="2b9ed-104">This procedure walks through defining loyalty reward points.</span></span> <span data-ttu-id="2b9ed-105">Du må definere fordelspoeng før du oppretter et fordelsprogram.</span><span class="sxs-lookup"><span data-stu-id="2b9ed-105">You should set up loyalty reward points before you set up a loyalty program.</span></span> <span data-ttu-id="2b9ed-106">Denne prosedyren bruker demonstrasjonsdatafirmaet USRT.</span><span class="sxs-lookup"><span data-stu-id="2b9ed-106">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="2b9ed-107">Gå til Detaljhandel og handel > Kunder > Fordel > Fordelspoeng.</span><span class="sxs-lookup"><span data-stu-id="2b9ed-107">Go to Retail and Commerce > Customers > Loyalty > Loyalty reward points.</span></span>
2. <span data-ttu-id="2b9ed-108">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="2b9ed-108">Click New.</span></span>
3. <span data-ttu-id="2b9ed-109">Skriv inn en verdi i feltet ID for fordelspoeng.</span><span class="sxs-lookup"><span data-stu-id="2b9ed-109">In the Reward point ID field, type a value.</span></span>
4. <span data-ttu-id="2b9ed-110">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="2b9ed-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="2b9ed-111">Velg et alternativ i feltet Type fordelspoeng.</span><span class="sxs-lookup"><span data-stu-id="2b9ed-111">In the Reward point type field, select an option.</span></span>
    * <span data-ttu-id="2b9ed-112">Velg Antall hvis du vil at fordelspoengene skal avrundes til nærmeste heltall.</span><span class="sxs-lookup"><span data-stu-id="2b9ed-112">Select Quantity if you want the reward points to be rounded to the nearest integer.</span></span> <span data-ttu-id="2b9ed-113">Velg Beløp hvis du vil at fordelspoengene skal avrundes i henhold til valutaavrundingsregler.</span><span class="sxs-lookup"><span data-stu-id="2b9ed-113">Select Amount if you want the reward points to be rounded according to currency rounding rules.</span></span> <span data-ttu-id="2b9ed-114">Hvis du velger Antall, hopper du over neste trinn i prosedyren.</span><span class="sxs-lookup"><span data-stu-id="2b9ed-114">If you select Quantity, skip the next step of this procedure..</span></span>  
6. <span data-ttu-id="2b9ed-115">Skriv inn en verdi i Valuta-feltet.</span><span class="sxs-lookup"><span data-stu-id="2b9ed-115">In the Currency field, type a value.</span></span>
    * <span data-ttu-id="2b9ed-116">Alle utstedte poeng vil ha den valgte valutaen for fordelspoeng av typen Beløp.</span><span class="sxs-lookup"><span data-stu-id="2b9ed-116">For Amount type reward points, all points issued will have the selected currency.</span></span> <span data-ttu-id="2b9ed-117">Dette feltet gjelder ikke for fordelspoeng av typen Antall. Hopp over dette trinnet.</span><span class="sxs-lookup"><span data-stu-id="2b9ed-117">For Quantity type reward points, this field doesn't apply—skip this step.</span></span>  
7. <span data-ttu-id="2b9ed-118">Merk av eller fjern merket for Kan løses inn.</span><span class="sxs-lookup"><span data-stu-id="2b9ed-118">Check or uncheck the Redeemable checkbox.</span></span>
8. <span data-ttu-id="2b9ed-119">Angi et tall i Innløsningsrangering-feltet.</span><span class="sxs-lookup"><span data-stu-id="2b9ed-119">In the Redeem ranking field, enter a number.</span></span>
    * <span data-ttu-id="2b9ed-120">Innløsningsrangering brukes når to eller flere innløsbare fordelspoeng kan brukes til å betale for produkter.</span><span class="sxs-lookup"><span data-stu-id="2b9ed-120">Redeem ranking is used when two or more redeemable reward points can be used to pay for products.</span></span> <span data-ttu-id="2b9ed-121">Hvis de to fordelspoengene har samme innløsningsrangering, må det som må senke antall poeng brukes.</span><span class="sxs-lookup"><span data-stu-id="2b9ed-121">If the two reward points have the same redeem ranking, then the one that needs to lower number of points will be used.</span></span>  
9. <span data-ttu-id="2b9ed-122">Du må angi en verdi i feltet Verdi for utløpstid.</span><span class="sxs-lookup"><span data-stu-id="2b9ed-122">In the Expiration time value field, enter a number.</span></span>
    * <span data-ttu-id="2b9ed-123">Fordelspoengene utløper angitt antall dager, måneder eller år etter at poengene ble utstedt.</span><span class="sxs-lookup"><span data-stu-id="2b9ed-123">The reward points will expire the specified number of days, months, or years after when the points are issued.</span></span> <span data-ttu-id="2b9ed-124">Verdien 0 betyr at fordelspoengene aldri utløper.</span><span class="sxs-lookup"><span data-stu-id="2b9ed-124">A value of ‘0’ means the loyalty reward points will never expire.</span></span>  
10. <span data-ttu-id="2b9ed-125">Velg et alternativ i feltet Enhet for utløpstid.</span><span class="sxs-lookup"><span data-stu-id="2b9ed-125">In the Expiration time unit field, select an option.</span></span>
11. <span data-ttu-id="2b9ed-126">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="2b9ed-126">Click Save.</span></span>
