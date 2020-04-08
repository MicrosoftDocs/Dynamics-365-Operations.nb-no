---
title: " Behandle justeringer av fordelspoeng"
description: Denne prosedyren beskriver hvordan du slår opp fordelskortinformasjon og justerer fordelspoeng.
author: scott-tucker
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailLoyaltyCards, RetailLoyaltyCardRewardPointTrans, RetailLoyaltyCardRewardPointAdjustment, RetailAffiliationLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bdbd9fa60fe4d000359e4695a9fb034fae3ca1b0
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140739"
---
# <a name="process-loyalty-reward-point-adjustments"></a><span data-ttu-id="7e714-103"> Behandle justeringer av fordelspoeng</span><span class="sxs-lookup"><span data-stu-id="7e714-103">Process loyalty reward point adjustments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7e714-104">Denne prosedyren beskriver hvordan du slår opp fordelskortinformasjon og justerer fordelspoeng.</span><span class="sxs-lookup"><span data-stu-id="7e714-104">This procedure demonstrates how to look up loyalty card information and adjust loyalty reward points.</span></span> <span data-ttu-id="7e714-105">Demonstrasjonsdatafirmaet USRT brukes til å opprette denne oppgaven.</span><span class="sxs-lookup"><span data-stu-id="7e714-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="7e714-106">Denne oppgaven er ment for rollen som driftsleder for handel eller kundeserviceleder.</span><span class="sxs-lookup"><span data-stu-id="7e714-106">This task is intended for the Commerce operations manager role or a Customer service manager role.</span></span>

1. <span data-ttu-id="7e714-107">Gå til Fordelskort.</span><span class="sxs-lookup"><span data-stu-id="7e714-107">Go to Loyalty cards.</span></span>
2. <span data-ttu-id="7e714-108">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="7e714-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="7e714-109">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="7e714-109">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="7e714-110">Klikk Korttransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="7e714-110">Click Card transactions.</span></span>
    * <span data-ttu-id="7e714-111">Du kan vise alle fordelstransaksjoner for det valgte fordelskortet på denne siden.</span><span class="sxs-lookup"><span data-stu-id="7e714-111">On this page you can view all loyalty transactions for the selected loyalty card.</span></span>  
5. <span data-ttu-id="7e714-112">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="7e714-112">Close the page.</span></span>
6. <span data-ttu-id="7e714-113">Klikk Kortjusteringer.</span><span class="sxs-lookup"><span data-stu-id="7e714-113">Click Card adjustments.</span></span>
7. <span data-ttu-id="7e714-114">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="7e714-114">Click New.</span></span>
8. <span data-ttu-id="7e714-115">Angi eller velg en verdi i Fordelspoeng-feltet.</span><span class="sxs-lookup"><span data-stu-id="7e714-115">In the Reward point field, enter or select a value.</span></span>
9. <span data-ttu-id="7e714-116">Angi et tall i Beløp eller antall-feltet.</span><span class="sxs-lookup"><span data-stu-id="7e714-116">In the Amount or quantity field, enter a number.</span></span>
    * <span data-ttu-id="7e714-117">Du kan legge til eller fjerne poeng fra fordelskortet med positive eller negative beløp.</span><span class="sxs-lookup"><span data-stu-id="7e714-117">You can add or remove points from the loyalty card by using positive or negative amounts.</span></span>  
10. <span data-ttu-id="7e714-118">Angi eller velg en verdi i Fordelsprogram-feltet.</span><span class="sxs-lookup"><span data-stu-id="7e714-118">In the Loyalty program field, enter or select a value.</span></span>
11. <span data-ttu-id="7e714-119">Skriv inn en verdi i feltet Kommentar.</span><span class="sxs-lookup"><span data-stu-id="7e714-119">In the Comment field, type a value.</span></span>
12. <span data-ttu-id="7e714-120">Klikk Poster justering.</span><span class="sxs-lookup"><span data-stu-id="7e714-120">Click Post adjustment.</span></span>
13. <span data-ttu-id="7e714-121">Klikk Ja.</span><span class="sxs-lookup"><span data-stu-id="7e714-121">Click Yes.</span></span>
14. <span data-ttu-id="7e714-122">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="7e714-122">Close the page.</span></span>
    * <span data-ttu-id="7e714-123">Vanligvis vil du nå oppdatere siden for å se resultatet av justeringen av fordelspoengene i kategorien Fordelspoengsammendrag. Men hvis du kjører dette som en oppgaveveiledning, skal du ikke oppdatere nå. Hvis du gjør det, stopper oppgaveveiledningen.</span><span class="sxs-lookup"><span data-stu-id="7e714-123">Normally at this point you'd refresh the page to see the result of the reward points adjustment in the Reward point summary tab. But if you are running this as a task guide, don't refresh now because if you do, the task guide will stop.</span></span>  
15. <span data-ttu-id="7e714-124">Klikk Korttransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="7e714-124">Click Card transactions.</span></span>
16. <span data-ttu-id="7e714-125">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="7e714-125">Close the page.</span></span>

