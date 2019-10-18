---
title: Definere leverandørbetalingsbetingelser
description: Dette emnet forklarer hvordan du konfigurerer betalingsbetingelser for leverandørfakturaer.
author: abruer
manager: AnnBe
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PaymTerm, CashDisc
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6432d04aa821e76d67e2c430e514f4b9056d8228
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/27/2019
ms.locfileid: "2179281"
---
# <a name="define-vendor-payment-terms"></a><span data-ttu-id="76a22-103">Definere leverandørbetalingsbetingelser</span><span class="sxs-lookup"><span data-stu-id="76a22-103">Define vendor payment terms</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="76a22-104">Dette emnet forklarer hvordan du konfigurerer betalingsbetingelser for leverandørfakturaer.</span><span class="sxs-lookup"><span data-stu-id="76a22-104">This topic explains how to set up payment terms for vendor invoices.</span></span> <span data-ttu-id="76a22-105">Denne oppgaven bruker demonstrasjonsfirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="76a22-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="76a22-106">Gå til **Navigasjonsrute > Moduler > Leverandører > Betalingsoppsett > Betalingsbetingelser**.</span><span class="sxs-lookup"><span data-stu-id="76a22-106">Go to **Navigation pane > Modules > Accounts payable > Payment setup > Terms of payment**.</span></span>
2. <span data-ttu-id="76a22-107">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="76a22-107">Select **New**.</span></span> <span data-ttu-id="76a22-108">Siden Betalingsbetingelser brukes til å definere hvordan forfallsdatoen beregnes.</span><span class="sxs-lookup"><span data-stu-id="76a22-108">The Terms of payment page is used to define how the due date will be calculated.</span></span> <span data-ttu-id="76a22-109">Den brukes ikke til å definere hvordan kontantrabatten skal beregnes.</span><span class="sxs-lookup"><span data-stu-id="76a22-109">It is not used to define how the cash discount date will be calculated.</span></span>  
3. <span data-ttu-id="76a22-110">Skriv inn en verdi i **Betalingsbetingelser**-feltet.</span><span class="sxs-lookup"><span data-stu-id="76a22-110">In the **Terms of payment** field, type a value.</span></span>
4. <span data-ttu-id="76a22-111">Skriv inn en verdi i **Beskrivelse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="76a22-111">In the **Description field**, type a value.</span></span>
5. <span data-ttu-id="76a22-112">Angi et tall i **Dager**-feltet.</span><span class="sxs-lookup"><span data-stu-id="76a22-112">In the **Days** field, enter a number.</span></span> <span data-ttu-id="76a22-113">Tallet som er angitt her, brukes til å legge til forfallsdatoen, eller til slutten av perioden angitt i betalingsmåten.</span><span class="sxs-lookup"><span data-stu-id="76a22-113">The number entered here will be used to add to the due date, or to the end of the period identified in the Payment method.</span></span> <span data-ttu-id="76a22-114">Hvis du for eksempel velger **Netto**, legges tallet til forfallsdatoen.</span><span class="sxs-lookup"><span data-stu-id="76a22-114">For example, if you select **Net**, the number will be added to the due date.</span></span> <span data-ttu-id="76a22-115">Hvis du velger **Inneværende måned**, legges nummeret til den siste dagen i gjeldende måned for å beregne forfallsdatoen.</span><span class="sxs-lookup"><span data-stu-id="76a22-115">If you select **Current month**, it will add the number to the last day of the current month to calculate the due date.</span></span>  
6. <span data-ttu-id="76a22-116">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="76a22-116">Select **Save**.</span></span>
7. <span data-ttu-id="76a22-117">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="76a22-117">Close the page.</span></span>
8. <span data-ttu-id="76a22-118">Gå til **Leverandører > Betalingsoppsett > Kontantrabatt**.</span><span class="sxs-lookup"><span data-stu-id="76a22-118">Go to **Accounts payable > Payment setup > Cash discounts**.</span></span>
9. <span data-ttu-id="76a22-119">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="76a22-119">Select **New**.</span></span>
10. <span data-ttu-id="76a22-120">Angi en ID i **Kontantrabatt**-feltet.</span><span class="sxs-lookup"><span data-stu-id="76a22-120">In the **Cash discount** field, enter an ID.</span></span>
11. <span data-ttu-id="76a22-121">Skriv inn en verdi i **Beskrivelse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="76a22-121">In the **Description** field, type a value.</span></span>
12. <span data-ttu-id="76a22-122">Hvis leverandøren tilbyr en trinnvis rabatt, velger du neste kontantrabatt etter at den gjeldende er utløpt.</span><span class="sxs-lookup"><span data-stu-id="76a22-122">If the vendor offers a tiered discount, select the next cash discount after the current one is expired.</span></span>
13. <span data-ttu-id="76a22-123">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="76a22-123">Close the page.</span></span>
14. <span data-ttu-id="76a22-124">Angi et tall i **Dager**-feltet.</span><span class="sxs-lookup"><span data-stu-id="76a22-124">In the **Days** field, enter a number.</span></span> <span data-ttu-id="76a22-125">Antallet som er angitt i **Dager**-feltet, brukes til å beregne kontantrabattdatoen, avhengig av hvilket alternativ som er valgt i feltet **Netto/løpende**.</span><span class="sxs-lookup"><span data-stu-id="76a22-125">The quantity entered in the **Days** field will be used to calculate the Cash discount date, based on what option was selected in the **Net/Current** field.</span></span> <span data-ttu-id="76a22-126">Hvis **Netto** er valgt, legges antallet til fakturadatoen for å bestemme kontantrabattdatoen.</span><span class="sxs-lookup"><span data-stu-id="76a22-126">If **Net** was selected, the quantity will be added to the invoice date to determine the cash discount date.</span></span> <span data-ttu-id="76a22-127">Hvis **Gjeldende måned** er valgt, legges antallet til på slutten av gjeldende måned for å bestemme kontantrabattdatoen.</span><span class="sxs-lookup"><span data-stu-id="76a22-127">If **Current month** was selected, the quantity will be added to the end of the currency month to determine the cash discount date.</span></span>  
15. <span data-ttu-id="76a22-128">Angi prosenten av kontantrabatten i **Rabatt**-feltet.</span><span class="sxs-lookup"><span data-stu-id="76a22-128">Enter the percentage of the cash discount in the **Discount** field.</span></span> 
16. <span data-ttu-id="76a22-129">Angi hovedkontoen som kontantrabatten skal bokføres på for kundefakturaer, og angi deretter hovedkontoen som kontantrabatten skal bokføres på for leverandørfakturaer.</span><span class="sxs-lookup"><span data-stu-id="76a22-129">Enter the main account to which the cash discount will be posted for customer invoices, then enter the main account to which the cash discount will be posted for vendor invoices.</span></span> <span data-ttu-id="76a22-130">Hvis **Motkontoer for rabatt** er satt til **Bruk hovedkonto for leverandørrabatt**, brukes hovedkontoen.</span><span class="sxs-lookup"><span data-stu-id="76a22-130">If **Discount offset accounts** is set to **Use main account for vendor discount**, then the Main account will be used.</span></span> <span data-ttu-id="76a22-131">Hvis alternativet er satt til **Kontoer på fakturalinjene**, posteres kontantrabatten til anleggsmiddel/utgiftshovedkontoene på fakturalinjene.</span><span class="sxs-lookup"><span data-stu-id="76a22-131">If the option is set to **Accounts on the invoice lines**, the cash discount will be posted to the asset/expense accounts on the invoice's lines.</span></span>  
17. <span data-ttu-id="76a22-132">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="76a22-132">Select **Save**.</span></span>

