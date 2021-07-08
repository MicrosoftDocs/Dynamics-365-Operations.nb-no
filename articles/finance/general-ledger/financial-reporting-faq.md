---
title: Vanlige spørsmål om finansrapportering
description: Dette emnet gir svar på vanlige spørsmål om finansrapportering.
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
ms.openlocfilehash: e1b67f86446403933005008a9a1e2cc6739dc516
ms.sourcegitcommit: ecabf43282a3e55f1db40341aa3f3c7950b9e94c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/16/2021
ms.locfileid: "6266639"
---
# <a name="financial-reporting-faq"></a><span data-ttu-id="159d1-103">Vanlige spørsmål om finansrapportering</span><span class="sxs-lookup"><span data-stu-id="159d1-103">Financial reporting FAQ</span></span>

<span data-ttu-id="159d1-104">Dette emnet gir svar på vanlige spørsmål om finansrapportering.</span><span class="sxs-lookup"><span data-stu-id="159d1-104">This topic provides answers to frequently asked questions about Financial reporting.</span></span>

## <a name="how-do-i-restrict-access-to-a-report-by-using-tree-security"></a><span data-ttu-id="159d1-105">Hvordan begrenser jeg tilgang til en rapport med tresikkerhet?</span><span class="sxs-lookup"><span data-stu-id="159d1-105">How do I restrict access to a report by using tree security?</span></span>

<span data-ttu-id="159d1-106">Følgende eksempel viser hvordan du begrenser tilgang til en rapport med tresikkerhet.</span><span class="sxs-lookup"><span data-stu-id="159d1-106">The following example shows how to restrict access to a report by using tree security.</span></span>

<span data-ttu-id="159d1-107">Demofirmaet USMF har en **balanserapport** som ikke alle finansrapporteringsbrukere skal ha tilgang til.</span><span class="sxs-lookup"><span data-stu-id="159d1-107">The USMF demo company has a **Balance sheet** report that not all Financial reporting users should have access to.</span></span> <span data-ttu-id="159d1-108">Du kan bruke tresikkerhet til å begrense tilgang til en rapport, slik at bare bestemte brukere får tilgang til den.</span><span class="sxs-lookup"><span data-stu-id="159d1-108">You can use tree security to restrict access to a single report so that only specific users can access it.</span></span>

1. <span data-ttu-id="159d1-109">Logg på Financial Reporter Report Designer.</span><span class="sxs-lookup"><span data-stu-id="159d1-109">Sign in to Financial Reporter Report Designer.</span></span>
2. <span data-ttu-id="159d1-110">Velg **Fil \> Ny \> Tredefinisjon** til å opprette en ny tredefinisjon.</span><span class="sxs-lookup"><span data-stu-id="159d1-110">Select **File \> New \> Tree Definition** to create a new tree definition.</span></span>
3. <span data-ttu-id="159d1-111">Dobbelttrykk (eller dobbeltklikk) på linjen **Sammendrag** i kolonnen **Enhetssikkerhet**.</span><span class="sxs-lookup"><span data-stu-id="159d1-111">Double-tap (or double-click) the **Summary** line in the **Unit Security** column.</span></span>
4. <span data-ttu-id="159d1-112">Velg **Brukere og grupper**.</span><span class="sxs-lookup"><span data-stu-id="159d1-112">Select **Users and Groups**.</span></span>
5. <span data-ttu-id="159d1-113">Velg brukerne eller gruppene som må ha tilgang til rapporten.</span><span class="sxs-lookup"><span data-stu-id="159d1-113">Select the users or groups that require access to the report.</span></span>
6. <span data-ttu-id="159d1-114">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="159d1-114">Select **Save**.</span></span>
7. <span data-ttu-id="159d1-115">I rapportdefinisjonen legger du til den nye tredefinisjonen.</span><span class="sxs-lookup"><span data-stu-id="159d1-115">In the report definition, add your new tree definition.</span></span>
8. <span data-ttu-id="159d1-116">Velg **Innstilling** i tredefinisjonen.</span><span class="sxs-lookup"><span data-stu-id="159d1-116">In the tree definition, select **Setting**.</span></span> <span data-ttu-id="159d1-117">Under **Valg av rapporteringsenhet** velger du **Inkluder alle enheter**.</span><span class="sxs-lookup"><span data-stu-id="159d1-117">Then, under **Reporting unit selection**, select **Include all units**.</span></span>

## <a name="how-do-i-identify-which-accounts-dont-match-my-balances"></a><span data-ttu-id="159d1-118">Hvordan identifiserer jeg hvilke kontoer som ikke samsvarer med saldoene?</span><span class="sxs-lookup"><span data-stu-id="159d1-118">How do I identify which accounts don't match my balances?</span></span>

<span data-ttu-id="159d1-119">Hvis du har en rapport som ikke samsvarer saldoene, bruker du følgende fremgangsmåter til å identifisere hver konto og hvert avvik.</span><span class="sxs-lookup"><span data-stu-id="159d1-119">If you have a report that doesn't have matching balances, use the following procedures to identify each account and variance.</span></span>

### <a name="in-financial-reporter-report-designer"></a><span data-ttu-id="159d1-120">I Financial Reporter Report Designer</span><span class="sxs-lookup"><span data-stu-id="159d1-120">In Financial Reporter Report Designer</span></span>

1. <span data-ttu-id="159d1-121">Opprett en ny raddefinisjon.</span><span class="sxs-lookup"><span data-stu-id="159d1-121">Create a new row definition.</span></span>
2. <span data-ttu-id="159d1-122">Velg **Rediger \> Sett inn rader fra dimensjoner**.</span><span class="sxs-lookup"><span data-stu-id="159d1-122">Select **Edit \> Insert Rows from Dimensions**.</span></span>
3. <span data-ttu-id="159d1-123">Velg **MainAccount**.</span><span class="sxs-lookup"><span data-stu-id="159d1-123">Select **MainAccount**.</span></span>
4. <span data-ttu-id="159d1-124">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="159d1-124">Select **OK**.</span></span>
5. <span data-ttu-id="159d1-125">Lagre raddefinisjonen.</span><span class="sxs-lookup"><span data-stu-id="159d1-125">Save the row definition.</span></span>
6. <span data-ttu-id="159d1-126">Opprett en ny kolonnedefinisjon.</span><span class="sxs-lookup"><span data-stu-id="159d1-126">Create a new column definition.</span></span>
7. <span data-ttu-id="159d1-127">Opprett en ny rapportdefinisjon.</span><span class="sxs-lookup"><span data-stu-id="159d1-127">Create a new report definition.</span></span>
8. <span data-ttu-id="159d1-128">Velg **Innstillinger** og fjern merket for dette alternativet.</span><span class="sxs-lookup"><span data-stu-id="159d1-128">Select **Settings** and unmark this option.</span></span>
9. <span data-ttu-id="159d1-129">Generer rapporten.</span><span class="sxs-lookup"><span data-stu-id="159d1-129">Generate the report.</span></span> 
10. <span data-ttu-id="159d1-130">Eksporter rapporten til Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="159d1-130">Export the report to Microsoft Excel.</span></span>

### <a name="in-dynamics-365-finance"></a><span data-ttu-id="159d1-131">I Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="159d1-131">In Dynamics 365 Finance</span></span>

1. <span data-ttu-id="159d1-132">Gå til **Økonomimodul \> Forespørsler og rapporter \> Råbalanse**.</span><span class="sxs-lookup"><span data-stu-id="159d1-132">Go to **General ledger \> Inquiries and reports \> Trial balance**.</span></span>
2. <span data-ttu-id="159d1-133">Angi følgende felter:</span><span class="sxs-lookup"><span data-stu-id="159d1-133">Set the following fields:</span></span>

    - <span data-ttu-id="159d1-134">**Fra-dato** – Angi startdatoen på regnskapsåret.</span><span class="sxs-lookup"><span data-stu-id="159d1-134">**From Date** – Enter the start date of the fiscal year.</span></span>
    - <span data-ttu-id="159d1-135">**Til-dato** – Angi datoen du genererer rapporten for.</span><span class="sxs-lookup"><span data-stu-id="159d1-135">**To Date** – Enter the date that you're generating the report for.</span></span>
    - <span data-ttu-id="159d1-136">**Finansdimensjon** – Angi dette feltet til **Hovedkontosett**.</span><span class="sxs-lookup"><span data-stu-id="159d1-136">**Financial Dimension** – Set this field to **Main Account set**.</span></span>

3. <span data-ttu-id="159d1-137">Velg **Beregn**.</span><span class="sxs-lookup"><span data-stu-id="159d1-137">Select **Calculate**.</span></span>
4. <span data-ttu-id="159d1-138">Eksporter rapporten til Excel.</span><span class="sxs-lookup"><span data-stu-id="159d1-138">Export the report to Excel.</span></span>

<span data-ttu-id="159d1-139">Du skal nå kunne kopiere dataene fra Excel-rapporten i Financial Reporter til rapporten **Råbalanse** slik at du kan sammenligne kolonnene **Sluttsaldo**.</span><span class="sxs-lookup"><span data-stu-id="159d1-139">You should now be able to copy the data from the Financial Reporter Excel report to the **Trial Balance** report, so that you can compare the **Closing Balance** columns.</span></span>

## <a name="when-i-design-a-report-in-report-designer-or-when-i-generate-a-financial-report-i-received-the-following-message-the-operation-could-not-be-completed-due-to-a-problem-in-the-data-provider-framework-how-should-i-respond"></a><span data-ttu-id="159d1-140">Når jeg utformer en rapport i Report Designer, eller når jeg genererer en finansrapport, får jeg følgende melding: Operasjonen kan ikke fullføres på grunn av et problem i dataleverandørrammeverket.</span><span class="sxs-lookup"><span data-stu-id="159d1-140">When I design a report in Report Designer, or when I generate a financial report, I received the following message: "The operation could not be completed due to a problem in the data provider framework."</span></span> <span data-ttu-id="159d1-141">Hvordan skal jeg svare?</span><span class="sxs-lookup"><span data-stu-id="159d1-141">How should I respond?</span></span>

<span data-ttu-id="159d1-142">Meldingen indikerer at det oppstod et problem da systemet forsøkte å hente økonomiske metadata fra datatorget mens du brukte finansrapportering.</span><span class="sxs-lookup"><span data-stu-id="159d1-142">The message indicates that an issue occurred when the system tried to retrieve financial metadata from the data mart while you were using Financial reporting.</span></span> <span data-ttu-id="159d1-143">Det finnes to måter å svare på dette problemet på:</span><span class="sxs-lookup"><span data-stu-id="159d1-143">There are two ways to respond to this issue:</span></span>

- <span data-ttu-id="159d1-144">Gå gjennom integreringsstatusen for dataene ved å gå til **Verktøy \> Integreringsstatus** i Report Designer.</span><span class="sxs-lookup"><span data-stu-id="159d1-144">Review the integration status of the data by going to **Tools \> Integration status** in Report Designer.</span></span> <span data-ttu-id="159d1-145">Hvis integreringen ikke er fullført, må du vente til den er fullført.</span><span class="sxs-lookup"><span data-stu-id="159d1-145">If the integration is incomplete, wait for it to be completed.</span></span> <span data-ttu-id="159d1-146">Deretter prøver du det du gjorde da du mottok meldingen.</span><span class="sxs-lookup"><span data-stu-id="159d1-146">Then retry what you were doing when you received the message.</span></span>
- <span data-ttu-id="159d1-147">Kontakt kundestøtte for å identifisere og arbeide deg gjennom problemet.</span><span class="sxs-lookup"><span data-stu-id="159d1-147">Contact Support to identify and work through the issue.</span></span> <span data-ttu-id="159d1-148">Det kan være inkonsekvente data i systemet.</span><span class="sxs-lookup"><span data-stu-id="159d1-148">There might be inconsistent data in the system.</span></span> <span data-ttu-id="159d1-149">Støtteteknikere kan hjelpe deg med å identifisere problemet på serveren og finne bestemte data som kan kreve en oppdatering.</span><span class="sxs-lookup"><span data-stu-id="159d1-149">Support engineers can help you identify that issue on the server and find the specific data that might require an update.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
