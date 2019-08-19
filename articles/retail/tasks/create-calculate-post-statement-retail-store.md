---
title: Opprette, beregne og postere utdrag for en detaljhandel
description: Dette emnet beskriver de manuelle trinnene for å opprette, beregne og postere et utdrag for en butikk.
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailStatementTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 693d1821779d5f7af95b900daa3bb7a2c38a6354
ms.sourcegitcommit: cb63259ad8fa5649ff12bc4a7f195bd1e40bd968
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/16/2019
ms.locfileid: "1755529"
---
# <a name="create-calculate-and-post-statements-for-a-retail-store"></a><span data-ttu-id="578c2-103">Opprette, beregne og postere utdrag for en detaljhandel</span><span class="sxs-lookup"><span data-stu-id="578c2-103">Create, calculate, and post statements for a retail store</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="578c2-104">Dette emnet beskriver de manuelle trinnene for å opprette, beregne og postere et utdrag for en butikk.</span><span class="sxs-lookup"><span data-stu-id="578c2-104">This topic describes the manual steps for creating, calculating, and posting a statement for a store.</span></span> <span data-ttu-id="578c2-105">Det finnes også satsvise jobber som kan konfigureres for de samme oppgavene.</span><span class="sxs-lookup"><span data-stu-id="578c2-105">There are also batch jobs that can be configured for the same tasks.</span></span> <span data-ttu-id="578c2-106">Du finner fremgangsmåten for å konfigurere og kjøre de satsvise jobbene i andre emner.</span><span class="sxs-lookup"><span data-stu-id="578c2-106">The steps for configuring and running the batch jobs can be found in other topics.</span></span> <span data-ttu-id="578c2-107">Hvis du vil fullføre denne prosedyren, må du ha transaksjoner som ble fullført i POS, og deretter overført til Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="578c2-107">To complete this procedure, you must have transactions that were completed in POS and then pulled into Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="578c2-108">Denne registreringen bruker firmaet USRT i demonstrasjonsdataene.</span><span class="sxs-lookup"><span data-stu-id="578c2-108">This recording uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="578c2-109">Velg **Finans for detaljhandelsbutikk** fra hjemmesiden.</span><span class="sxs-lookup"><span data-stu-id="578c2-109">Select **Retail store financials** from the home page.</span></span>
2. <span data-ttu-id="578c2-110">Velg **Nytt utdrag**.</span><span class="sxs-lookup"><span data-stu-id="578c2-110">Select **New statement**.</span></span>
3. <span data-ttu-id="578c2-111">I **Butikknummer**-feltet velger du et alternativ fra rullegardinlisten.</span><span class="sxs-lookup"><span data-stu-id="578c2-111">In the **Store number** field, select a option from the drop-down.</span></span>
4. <span data-ttu-id="578c2-112">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="578c2-112">Select **OK**.</span></span>
5. <span data-ttu-id="578c2-113">**Oppsett**-gruppen inneholder innstillingene som styrer hvilke transaksjoner som inkluderes i utdraget, og hvordan de grupperes i utdragslinjene.</span><span class="sxs-lookup"><span data-stu-id="578c2-113">The **Setup** group has the settings that control what transactions are included in the statement and how they are grouped into statement lines.</span></span> <span data-ttu-id="578c2-114">Du kan åpne **Oppsett**-gruppen og endre disse innstillingene, eller du kan bruke standardinnstillingene.</span><span class="sxs-lookup"><span data-stu-id="578c2-114">You can open the **Setup** group and change these settings, or you can use the defaults.</span></span>  
    - <span data-ttu-id="578c2-115">Feltet **Utdragsmetode** angir hvordan utdragslinjene skal grupperes.</span><span class="sxs-lookup"><span data-stu-id="578c2-115">The **Statement method** field defines how the statement lines will be grouped.</span></span>  
    - <span data-ttu-id="578c2-116">Velg et stabsmedlem eller en kasse i feltet **Stab/kasse** hvis du vil beregne et utdrag bare for bestemte stabsmedlemmer eller kasser.</span><span class="sxs-lookup"><span data-stu-id="578c2-116">Select a staff member or a register in the **staff/register** field if you want to calculate a statement only for the specific staff member or register.</span></span>  
6. <span data-ttu-id="578c2-117">Velg et alternativ i **Avslutningsmetode**-feltet.</span><span class="sxs-lookup"><span data-stu-id="578c2-117">In the **Closing method** field, select an option.</span></span>
7. <span data-ttu-id="578c2-118">Velg **Beregn utdrag** fra handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="578c2-118">Select **Calculate statement** from the Action Pane.</span></span>
8. <span data-ttu-id="578c2-119">Velg **Ja**.</span><span class="sxs-lookup"><span data-stu-id="578c2-119">Select **Yes**.</span></span>
    - <span data-ttu-id="578c2-120">Når du har beregnet utdraget, skal det være opprettet linjer med totalbeløp for hver betalingsmåte og utdragsmetode som ble brukt.</span><span class="sxs-lookup"><span data-stu-id="578c2-120">After calculating the statement, there should be lines created with total amounts for each payment method and statement method that was used.</span></span>  
    - <span data-ttu-id="578c2-121">Angi et opptelt beløp i hver linje hvis den må angis eller oppdateres.</span><span class="sxs-lookup"><span data-stu-id="578c2-121">Enter a counted amount in each line if it needs to be entered or updated.</span></span> <span data-ttu-id="578c2-122">Telt opp-feltet fylles ut med beløp fra kasseoppgjør i POS.</span><span class="sxs-lookup"><span data-stu-id="578c2-122">The counted field is populated with amounts from tender declarations done in POS.</span></span>  
9. <span data-ttu-id="578c2-123">Velg **Poster utdrag** fra handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="578c2-123">Select **Post statement** from the Action Pane.</span></span>
10. <span data-ttu-id="578c2-124">Velg **Lukk**.</span><span class="sxs-lookup"><span data-stu-id="578c2-124">Select **Close**.</span></span>
11. <span data-ttu-id="578c2-125">Lukk ruten.</span><span class="sxs-lookup"><span data-stu-id="578c2-125">Close the pane.</span></span>
12. <span data-ttu-id="578c2-126">Velg **Finans for detaljhandelsbutikk** på hjemmesiden.</span><span class="sxs-lookup"><span data-stu-id="578c2-126">At the home page, select **Retail store financials**.</span></span>
13. <span data-ttu-id="578c2-127">Velg kategorien **Posterte utdrag**.</span><span class="sxs-lookup"><span data-stu-id="578c2-127">Select the **Posted statements** tab.</span></span>

