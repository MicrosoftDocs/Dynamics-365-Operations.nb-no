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
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 455dee5a14ca0c44ba823a467baa78352b367ec8
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5221311"
---
# <a name="create-calculate-and-post-statements-for-a-retail-store"></a><span data-ttu-id="0d588-103">Opprette, beregne og postere utdrag for en detaljhandel</span><span class="sxs-lookup"><span data-stu-id="0d588-103">Create, calculate, and post statements for a retail store</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0d588-104">Dette emnet beskriver de manuelle trinnene for å opprette, beregne og postere et utdrag for en butikk.</span><span class="sxs-lookup"><span data-stu-id="0d588-104">This topic describes the manual steps for creating, calculating, and posting a statement for a store.</span></span> <span data-ttu-id="0d588-105">Det finnes også satsvise jobber som kan konfigureres for de samme oppgavene.</span><span class="sxs-lookup"><span data-stu-id="0d588-105">There are also batch jobs that can be configured for the same tasks.</span></span> <span data-ttu-id="0d588-106">Du finner fremgangsmåten for å konfigurere og kjøre de satsvise jobbene i andre emner.</span><span class="sxs-lookup"><span data-stu-id="0d588-106">The steps for configuring and running the batch jobs can be found in other topics.</span></span> <span data-ttu-id="0d588-107">Hvis du vil fullføre denne prosedyren, må du ha transaksjoner som ble fullført i POS, og deretter overført til Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="0d588-107">To complete this procedure, you must have transactions that were completed in POS and then pulled into Dynamics 365 Commerce.</span></span> <span data-ttu-id="0d588-108">Denne registreringen bruker firmaet USRT i demonstrasjonsdataene.</span><span class="sxs-lookup"><span data-stu-id="0d588-108">This recording uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="0d588-109">Velg **Finans for butikk** fra hjemmesiden.</span><span class="sxs-lookup"><span data-stu-id="0d588-109">Select **Store financials** from the home page.</span></span>
2. <span data-ttu-id="0d588-110">Velg **Nytt utdrag**.</span><span class="sxs-lookup"><span data-stu-id="0d588-110">Select **New statement**.</span></span>
3. <span data-ttu-id="0d588-111">I **Butikknummer**-feltet velger du et alternativ fra rullegardinlisten.</span><span class="sxs-lookup"><span data-stu-id="0d588-111">In the **Store number** field, select a option from the drop-down.</span></span>
4. <span data-ttu-id="0d588-112">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="0d588-112">Select **OK**.</span></span>
5. <span data-ttu-id="0d588-113">**Oppsett**-gruppen inneholder innstillingene som styrer hvilke transaksjoner som inkluderes i utdraget, og hvordan de grupperes i utdragslinjene.</span><span class="sxs-lookup"><span data-stu-id="0d588-113">The **Setup** group has the settings that control what transactions are included in the statement and how they are grouped into statement lines.</span></span> <span data-ttu-id="0d588-114">Du kan åpne **Oppsett**-gruppen og endre disse innstillingene, eller du kan bruke standardinnstillingene.</span><span class="sxs-lookup"><span data-stu-id="0d588-114">You can open the **Setup** group and change these settings, or you can use the defaults.</span></span>  
    - <span data-ttu-id="0d588-115">Feltet **Utdragsmetode** angir hvordan utdragslinjene skal grupperes.</span><span class="sxs-lookup"><span data-stu-id="0d588-115">The **Statement method** field defines how the statement lines will be grouped.</span></span>  
    - <span data-ttu-id="0d588-116">Velg et stabsmedlem eller en kasse i feltet **Stab/kasse** hvis du vil beregne et utdrag bare for bestemte stabsmedlemmer eller kasser.</span><span class="sxs-lookup"><span data-stu-id="0d588-116">Select a staff member or a register in the **staff/register** field if you want to calculate a statement only for the specific staff member or register.</span></span>  
6. <span data-ttu-id="0d588-117">Velg et alternativ i **Avslutningsmetode**-feltet.</span><span class="sxs-lookup"><span data-stu-id="0d588-117">In the **Closing method** field, select an option.</span></span>
7. <span data-ttu-id="0d588-118">Velg **Beregn utdrag** fra handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="0d588-118">Select **Calculate statement** from the Action Pane.</span></span>
8. <span data-ttu-id="0d588-119">Velg **Ja**.</span><span class="sxs-lookup"><span data-stu-id="0d588-119">Select **Yes**.</span></span>
    - <span data-ttu-id="0d588-120">Når du har beregnet utdraget, skal det være opprettet linjer med totalbeløp for hver betalingsmåte og utdragsmetode som ble brukt.</span><span class="sxs-lookup"><span data-stu-id="0d588-120">After calculating the statement, there should be lines created with total amounts for each payment method and statement method that was used.</span></span>  
    - <span data-ttu-id="0d588-121">Angi et opptelt beløp i hver linje hvis den må angis eller oppdateres.</span><span class="sxs-lookup"><span data-stu-id="0d588-121">Enter a counted amount in each line if it needs to be entered or updated.</span></span> <span data-ttu-id="0d588-122">Telt opp-feltet fylles ut med beløp fra kasseoppgjør i POS.</span><span class="sxs-lookup"><span data-stu-id="0d588-122">The counted field is populated with amounts from tender declarations done in POS.</span></span>  
9. <span data-ttu-id="0d588-123">Velg **Poster utdrag** fra handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="0d588-123">Select **Post statement** from the Action Pane.</span></span>
10. <span data-ttu-id="0d588-124">Velg **Lukk**.</span><span class="sxs-lookup"><span data-stu-id="0d588-124">Select **Close**.</span></span>
11. <span data-ttu-id="0d588-125">Lukk ruten.</span><span class="sxs-lookup"><span data-stu-id="0d588-125">Close the pane.</span></span>
12. <span data-ttu-id="0d588-126">Velg **Finans for butikk** på hjemmesiden.</span><span class="sxs-lookup"><span data-stu-id="0d588-126">At the home page, select **Store financials**.</span></span>
13. <span data-ttu-id="0d588-127">Velg kategorien **Posterte utdrag**.</span><span class="sxs-lookup"><span data-stu-id="0d588-127">Select the **Posted statements** tab.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]