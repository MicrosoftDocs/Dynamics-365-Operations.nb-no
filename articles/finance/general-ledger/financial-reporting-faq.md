---
title: Vanlige spørsmål om finansrapportering
description: Dette emnet viser spørsmål som er knyttet til finansrapportering som andre brukere har hatt.
author: jiwo
ms.date: 01/13/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 023354b0e2973f63411bf81cbeb0344333c49112
ms.sourcegitcommit: d63e7e0593084a61362a6cad3937b1fd956c384f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/21/2021
ms.locfileid: "5923031"
---
# <a name="financial-reporting-faq"></a><span data-ttu-id="56f1e-103">Vanlige spørsmål om finansrapportering</span><span class="sxs-lookup"><span data-stu-id="56f1e-103">Financial reporting FAQ</span></span> 

<span data-ttu-id="56f1e-104">Dette emnet gir svar på vanlige spørsmål om finansrapportering.</span><span class="sxs-lookup"><span data-stu-id="56f1e-104">This topic provides answers to frequently asked questions about financial reporting.</span></span> 

## <a name="how-do-i-restrict-access-to-a-report-using-tree-security"></a><span data-ttu-id="56f1e-105">Hvordan begrenser jeg tilgang til en rapport med tresikkerhet?</span><span class="sxs-lookup"><span data-stu-id="56f1e-105">How do I restrict access to a report using tree security?</span></span>

<span data-ttu-id="56f1e-106">Følgende eksempel viser hvordan du begrenser tilgang til en rapport med tresikkerhet.</span><span class="sxs-lookup"><span data-stu-id="56f1e-106">The following example shows how to restrict access to a report using tree security.</span></span>

<span data-ttu-id="56f1e-107">Demofirmaet USMF har en balanserapport som ikke alle finansrapporteringsbrukere skal ha tilgang til.</span><span class="sxs-lookup"><span data-stu-id="56f1e-107">The USMF demo company has a Balance sheet report that not all Financial reporting users should have access to.</span></span> <span data-ttu-id="56f1e-108">Du kan bruke tresikkerhet til å begrense tilgang til en rapport, slik at bare bestemte brukere får tilgang til rapporten.</span><span class="sxs-lookup"><span data-stu-id="56f1e-108">To restrict access, you can use tree security to restrict access to a single report so that only certain users can access the report.</span></span> <span data-ttu-id="56f1e-109">Følg denne fremgangsmåten for å begrense tilgang:</span><span class="sxs-lookup"><span data-stu-id="56f1e-109">Follow these steps to restrict access:</span></span> 

1. <span data-ttu-id="56f1e-110">Logg på Financial Reporter Report Designer.</span><span class="sxs-lookup"><span data-stu-id="56f1e-110">Sign in to Financial Reporter Report Designer.</span></span>
2. <span data-ttu-id="56f1e-111">Opprett en ny tredefinisjon.</span><span class="sxs-lookup"><span data-stu-id="56f1e-111">Create a new tree definition.</span></span> <span data-ttu-id="56f1e-112">Gå til **Fil > Ny > Tredefinisjon**.</span><span class="sxs-lookup"><span data-stu-id="56f1e-112">Go to **File > New > Tree Definition**.</span></span>
3. <span data-ttu-id="56f1e-113">Dobbeltklikk på linjen **Sammendrag** i kolonnen **Enhetssikkerhet**.</span><span class="sxs-lookup"><span data-stu-id="56f1e-113">Double-click the **Summary** line in the **Unit Security** column.</span></span>
4. <span data-ttu-id="56f1e-114">Velg **Brukere og grupper**.</span><span class="sxs-lookup"><span data-stu-id="56f1e-114">Select **Users and Groups**.</span></span>  
5. <span data-ttu-id="56f1e-115">Velg brukerne eller gruppene som må ha tilgang til denne rapporten.</span><span class="sxs-lookup"><span data-stu-id="56f1e-115">Select the users or groups that need access to this report.</span></span> 
6. <span data-ttu-id="56f1e-116">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="56f1e-116">Select **Save**.</span></span>
7. <span data-ttu-id="56f1e-117">I rapportdefinisjonen legger du til den nye tredefinisjonen.</span><span class="sxs-lookup"><span data-stu-id="56f1e-117">In the report definition, add your new tree definition.</span></span>
8. <span data-ttu-id="56f1e-118">Velg **Innstilling** i tredefinisjonen.</span><span class="sxs-lookup"><span data-stu-id="56f1e-118">In the tree definition, select **Setting**.</span></span> <span data-ttu-id="56f1e-119">Under **Valg av rapporteringsenhet** velger du **Inkluder alle enheter**.</span><span class="sxs-lookup"><span data-stu-id="56f1e-119">Under **Reporting unit selection**, select **Include all units**.</span></span>

## <a name="how-do-i-identify-which-accounts-do-not-match-my-balances"></a><span data-ttu-id="56f1e-120">Hvordan identifiserer jeg hvilke kontoer som ikke samsvarer med saldoene?</span><span class="sxs-lookup"><span data-stu-id="56f1e-120">How do I identify which accounts do not match my balances?</span></span>

<span data-ttu-id="56f1e-121">Hvis du har en rapport som ikke samsvarer saldoene, er det noen trinn du kan gå gjennom for å identifisere hver av kontoene og avvikene.</span><span class="sxs-lookup"><span data-stu-id="56f1e-121">If you have a report that doesn't have matching balances, here are some steps you can take to identify each of the accounts and variances.</span></span> 

<span data-ttu-id="56f1e-122">**Financial Reporter Report Designer**</span><span class="sxs-lookup"><span data-stu-id="56f1e-122">**Financial Reporter Report Designer**</span></span>
1. <span data-ttu-id="56f1e-123">Opprett en ny raddefinisjon i Financial Reporter Report Designer.</span><span class="sxs-lookup"><span data-stu-id="56f1e-123">In Financial Reporter Report Designer, create a new row definition.</span></span> 
2. <span data-ttu-id="56f1e-124">Velg **Rediger > Sett inn rader fra dimensjoner**.</span><span class="sxs-lookup"><span data-stu-id="56f1e-124">Select **Edit > Insert Rows from Dimensions**.</span></span>
3. <span data-ttu-id="56f1e-125">Velg **MainAccount**.</span><span class="sxs-lookup"><span data-stu-id="56f1e-125">Select **MainAccount**.</span></span>  
4. <span data-ttu-id="56f1e-126">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="56f1e-126">Select **OK**.</span></span>
5. <span data-ttu-id="56f1e-127">Lagre raddefinisjonen.</span><span class="sxs-lookup"><span data-stu-id="56f1e-127">Save the row definition.</span></span>
6. <span data-ttu-id="56f1e-128">Opprett en ny kolonnedefinisjon</span><span class="sxs-lookup"><span data-stu-id="56f1e-128">Create a new column definition</span></span>
7. <span data-ttu-id="56f1e-129">Opprett en ny rapportdefinisjon.</span><span class="sxs-lookup"><span data-stu-id="56f1e-129">Create a new report definition.</span></span>
8. <span data-ttu-id="56f1e-130">Velg **Innstillinger** og fjern merket for dette alternativet.</span><span class="sxs-lookup"><span data-stu-id="56f1e-130">Select **Settings** and unmark this option.</span></span>  
9. <span data-ttu-id="56f1e-131">Generer rapporten.</span><span class="sxs-lookup"><span data-stu-id="56f1e-131">Generate the report.</span></span> 
10. <span data-ttu-id="56f1e-132">Eksporter rapporten til Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="56f1e-132">Export the report to Microsoft Excel.</span></span>

<span data-ttu-id="56f1e-133">**Dynamics 365 Finance**</span><span class="sxs-lookup"><span data-stu-id="56f1e-133">**Dynamics 365 Finance**</span></span> 
1. <span data-ttu-id="56f1e-134">I Dynamics 365 Finance går du til **Økonomimodul > Forespørsler og rapporter > Råbalanse**.</span><span class="sxs-lookup"><span data-stu-id="56f1e-134">In Dynamics 365 Finance, go to **General Ledger > Inquiries and Reports > Trial Balance**.</span></span>
2. <span data-ttu-id="56f1e-135">Angi følgende parametere:</span><span class="sxs-lookup"><span data-stu-id="56f1e-135">Set the following parameters:</span></span>
   - <span data-ttu-id="56f1e-136">**Fra-dato** – Angi starten på regnskapsåret.</span><span class="sxs-lookup"><span data-stu-id="56f1e-136">**From Date** - Enter the start of the fiscal year.</span></span>
   - <span data-ttu-id="56f1e-137">**Til-dato** – Angi datoen du genererer rapporten for.</span><span class="sxs-lookup"><span data-stu-id="56f1e-137">**To Date** - Enter the date you are generating the report for.</span></span>
   - <span data-ttu-id="56f1e-138">**Finansdimensjon** – Angi dette feltet til **Hovedkontosett**.</span><span class="sxs-lookup"><span data-stu-id="56f1e-138">**Financial Dimension** - Set this field to **Main Account set**.</span></span>
 3. <span data-ttu-id="56f1e-139">Velg **Beregn**.</span><span class="sxs-lookup"><span data-stu-id="56f1e-139">Select **Calculate**.</span></span>
 4. <span data-ttu-id="56f1e-140">Eksporter rapporten til Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="56f1e-140">Export the report to Microsoft Excel.</span></span>

<span data-ttu-id="56f1e-141">Du skal nå kunne kopiere dataene fra Excel-rapporten i finansrapportering til råbalanserapporten slik at du kan sammenligne **sluttsaldokolonnene**.</span><span class="sxs-lookup"><span data-stu-id="56f1e-141">You should now be able to copy the data from the Financial Reporter Excel report to the Trial Balance report, so you can compare the **Closing Balance** columns.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]