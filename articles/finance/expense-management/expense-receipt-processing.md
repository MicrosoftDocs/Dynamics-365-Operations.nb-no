---
title: Behandling av utgiftskvitteringer
description: Dette emnet inneholder informasjon om OCR-behandling (optisk tegngjenkjenning) for kvitteringer. Denne funksjonen er utformet for å forbedre brukeropplevelsen når utgiftsrapporter opprettes i Microsoft Dynamics 365 Finance.
author: stsporen
manager: AnnBe
ms.date: 11/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: stsporen
ms.search.validFrom: 2019-11-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 49cdfeac8cda9f1ddd3aca61f902f00f30f3485b
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/21/2020
ms.locfileid: "3154046"
---
# <a name="expense-receipt-processing"></a><span data-ttu-id="01890-104">Behandling av utgiftsmottak</span><span class="sxs-lookup"><span data-stu-id="01890-104">Expense receipt processing</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]


<span data-ttu-id="01890-105">Utgiftsoppføring er forbedret gjennom innføringen av OCR-behandling (optisk tegngjenkjenning) for kvitteringer.</span><span class="sxs-lookup"><span data-stu-id="01890-105">Expense entry has been enhanced through the introduction of optical character recognition (OCR) processing for receipts.</span></span> <span data-ttu-id="01890-106">Denne funksjonen er utformet for å forbedre brukeropplevelsen når utgiftsrapporter opprettes.</span><span class="sxs-lookup"><span data-stu-id="01890-106">This feature is designed to improve the user experience when expense reports are created.</span></span>

## <a name="key-features"></a><span data-ttu-id="01890-107">Hovedfunksjoner</span><span class="sxs-lookup"><span data-stu-id="01890-107">Key features</span></span>

- <span data-ttu-id="01890-108">Forhandlerens navn, dato og totalt beløp trekkes fra kvitteringer.</span><span class="sxs-lookup"><span data-stu-id="01890-108">The merchant name, date, and total amount are extracted from receipts.</span></span>
- <span data-ttu-id="01890-109">Funksjonen prøver å matche ikke-tilknyttede kvitteringer med ikke-tilknyttede utgiftstransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="01890-109">The feature tries to match unattached receipts to unattached expense transactions.</span></span>
- <span data-ttu-id="01890-110">Brukere kan opprette manuelt angitte utgiftstransaksjoner fra kvitteringer.</span><span class="sxs-lookup"><span data-stu-id="01890-110">Users can create manually entered expense transactions from receipts.</span></span>

## <a name="usage-examples"></a><span data-ttu-id="01890-111">Eksempler på bruk</span><span class="sxs-lookup"><span data-stu-id="01890-111">Usage examples</span></span>

- <span data-ttu-id="01890-112">**Legg automatisk til kvitteringer som inkluderer kredittkorttransaksjoner, når en utgiftsrapport opprettes.**</span><span class="sxs-lookup"><span data-stu-id="01890-112">**Automatically attach receipts that include credit card transactions when an expense report is created.**</span></span>

    1. <span data-ttu-id="01890-113">Åpne **Utgiftsadministrering**-arbeidsområdet.</span><span class="sxs-lookup"><span data-stu-id="01890-113">Open the **Expense management** workspace.</span></span>
    2. <span data-ttu-id="01890-114">I **Kvitteringer**-fanen verifiserer du at det ikke finnes tilknyttede kvitteringer.</span><span class="sxs-lookup"><span data-stu-id="01890-114">On the **Receipts** tab, verify that unattached receipts exist.</span></span> <span data-ttu-id="01890-115">Du kan også laste opp kvitteringer i **Kvitteringer**-fanen.</span><span class="sxs-lookup"><span data-stu-id="01890-115">You can also upload receipts on the **Receipts** tab.</span></span>
    3. <span data-ttu-id="01890-116">I **Utgifter**-fanen verifiserer du at det ikke finnes tilknyttede utgifter.</span><span class="sxs-lookup"><span data-stu-id="01890-116">On the **Expenses** tab, verify that unattached expenses exist.</span></span> <span data-ttu-id="01890-117">Vanligvis importerer utgiftsadministratoren disse utgiftene fra kredittkortleverandøren.</span><span class="sxs-lookup"><span data-stu-id="01890-117">Typically, the expense administrator imports these expenses from the credit card provider.</span></span>
    4. <span data-ttu-id="01890-118">Velg **Ny utgiftsrapport**.</span><span class="sxs-lookup"><span data-stu-id="01890-118">Select **New expense report**.</span></span> <span data-ttu-id="01890-119">Vær oppmerksom på at du kan inkludere utgifter og kvitteringer, nå også, når du oppretter en utgiftsrapport.</span><span class="sxs-lookup"><span data-stu-id="01890-119">Notice that you can include expenses, and receipts, now as well, when you create an expense report.</span></span> <span data-ttu-id="01890-120">Hvis du legger til både utgifter og kvitteringer, utløses automatisk matching av kvitteringene med utgiftene.</span><span class="sxs-lookup"><span data-stu-id="01890-120">If you add both expenses and receipts, automatic matching of the receipts against the expenses is triggered.</span></span>

- <span data-ttu-id="01890-121">**Opprett en utgift, eller match en utgift fra en kvittering.**</span><span class="sxs-lookup"><span data-stu-id="01890-121">**Create an expense, or match an expense from a receipt.**</span></span>

    1. <span data-ttu-id="01890-122">På en utgiftsrapport går du til **Kvitteringer**-fane og legger ved en kvittering ved å velge **Legg til kvitteringer**.</span><span class="sxs-lookup"><span data-stu-id="01890-122">On an expense report, on the **Receipts** tab, attach a receipt by selecting **Add receipts**.</span></span>
    2. <span data-ttu-id="01890-123">Under det opplastede bildet av kvitteringen, legger du merke til alternativene **Opprett** og **Match**.</span><span class="sxs-lookup"><span data-stu-id="01890-123">Under the uploaded image of the receipt, notice the **Create** and **Match** options.</span></span>

        - <span data-ttu-id="01890-124">Velg **Opprett** hvis du vil opprette en manuelt angitt utgiftstransaksjon, og fyll ut verdiene som hentes fra kvitteringen.</span><span class="sxs-lookup"><span data-stu-id="01890-124">Select **Create** to create a manually entered expense transaction and fill in the values that are extracted from the receipt.</span></span>
        - <span data-ttu-id="01890-125">Hvis du velger **Match**, prøver systemet å matche en eksisterende utgift med kvitteringen.</span><span class="sxs-lookup"><span data-stu-id="01890-125">If you select **Match**, the system tries to match an existing expense to the receipt.</span></span>

## <a name="installation"></a><span data-ttu-id="01890-126">Installasjon</span><span class="sxs-lookup"><span data-stu-id="01890-126">Installation</span></span>

<span data-ttu-id="01890-127">Denne funksjonen fungerer i kombinasjon med **Utgiftsrapporter avbildet på nytt**-funksjonen for å forenkle utgiftsopplevelsen.</span><span class="sxs-lookup"><span data-stu-id="01890-127">This feature works in combination with the **Expense reports re-imagined** feature to help simplify the expense experience.</span></span>

<span data-ttu-id="01890-128">For å kunne bruke disse avanserte utgiftsfunksjonene må du installere Expense Management Service-tillegget for Microsoft Dynamics 365 Finance, og aktivere funksjonene i forekomsten.</span><span class="sxs-lookup"><span data-stu-id="01890-128">To use these advanced expense capabilities, install the Expense Management Service add-in for Microsoft Dynamics 365 Finance, and turn on the features in your instance.</span></span> <span data-ttu-id="01890-129">Du kan få tilgang til tillegget fra prosjektet i Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="01890-129">You can access the add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="01890-130">Logg på LCS, og åpne ønsket miljø.</span><span class="sxs-lookup"><span data-stu-id="01890-130">Sign in to LCS, and open the desired environment.</span></span>
2. <span data-ttu-id="01890-131">Gå til **Detaljerte opplysninger**.</span><span class="sxs-lookup"><span data-stu-id="01890-131">Go to **Full details**.</span></span>
3. <span data-ttu-id="01890-132">Velg **Vedlikehold**, eller rull ned til hurtigfanen **Miljøtillegg**.</span><span class="sxs-lookup"><span data-stu-id="01890-132">Select **Maintain**, or scroll down to the **Environment add-ins** FastTab.</span></span>
4. <span data-ttu-id="01890-133">Velg **Installer et nytt tillegg**.</span><span class="sxs-lookup"><span data-stu-id="01890-133">Select **Install a new add-in**.</span></span>
5. <span data-ttu-id="01890-134">Velg **Utgiftsadministreringstjeneste**.</span><span class="sxs-lookup"><span data-stu-id="01890-134">Select **Expense Management Service**.</span></span>
6. <span data-ttu-id="01890-135">Følg installasjonsveiledningen, og godta vilkårene.</span><span class="sxs-lookup"><span data-stu-id="01890-135">Follow the installation guide, and agree to the terms and conditions.</span></span>
7. <span data-ttu-id="01890-136">Velg **Installer**.</span><span class="sxs-lookup"><span data-stu-id="01890-136">Select **Install**.</span></span>

<span data-ttu-id="01890-137">I **Funksjonsadministrering**-arbeidsområde aktiverer du følgende funksjoner:</span><span class="sxs-lookup"><span data-stu-id="01890-137">In the **Feature management** workspace, turn on the following features:</span></span>

- <span data-ttu-id="01890-138">Ny utforming av utgiftsrapporter</span><span class="sxs-lookup"><span data-stu-id="01890-138">Expense reports re-imagined</span></span>
- <span data-ttu-id="01890-139">Samsvar og opprett utgift automatisk fra mottak</span><span class="sxs-lookup"><span data-stu-id="01890-139">Auto-match and create expense from receipt</span></span>

<span data-ttu-id="01890-140">Når du aktiverer disse funksjonene, finner følgende handlinger sted:</span><span class="sxs-lookup"><span data-stu-id="01890-140">When you turn on these features the following actions occur:</span></span>

- <span data-ttu-id="01890-141">Det eksisterende **Utgiftsadministrering**-arbeidsområdet erstattes med det nye arbeidsområdet.</span><span class="sxs-lookup"><span data-stu-id="01890-141">The existing **Expense management** workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="01890-142">Det legges til et nytt menyelement for synlighet av reiseregningsfelt.</span><span class="sxs-lookup"><span data-stu-id="01890-142">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="01890-143">Du kan fremdeles åpne forrige **Utgiftsrapporter**-side ved å gå til **Utgiftsadministrering > Mine utgifter > Utgiftsrapporter**.</span><span class="sxs-lookup"><span data-stu-id="01890-143">You can still open the former **Expense reports** page by going to **Expense management > My expenses > Expense reports**.</span></span>
- <span data-ttu-id="01890-144">Arbeidsflyter og alle godkjenninger fører deg fortsatt til den eksisterende reiseregningssiden.</span><span class="sxs-lookup"><span data-stu-id="01890-144">Workflows and any approvals still take you to the existing expense reports page.</span></span>
- <span data-ttu-id="01890-145">Kvitteringer behandles gjennom Microsoft Azure Cognitive Services, og metadata pakkes ut og legges til.</span><span class="sxs-lookup"><span data-stu-id="01890-145">Receipts will be processed through Microsoft Azure Cognitive Services, and metadata will be extracted and added.</span></span>
- <span data-ttu-id="01890-146">Det legges til et alternativ der du kan opprette en utgiftsrapport som inneholder matchede ikke-tilknyttede kvitteringer.</span><span class="sxs-lookup"><span data-stu-id="01890-146">An option is added that lets you create an expense report that includes matched unattached receipts.</span></span>
- <span data-ttu-id="01890-147">Et alternativ som legges til i utgiftsrapporter, lar deg opprette en utgiftslinje fra en kvittering, eller forsøke å matche en eksisterende kvittering med en eksisterende utgiftslinje.</span><span class="sxs-lookup"><span data-stu-id="01890-147">An option that is added to expense reports lets you create an expense line from a receipt, or attempts to match an existing receipt to an existing expense line.</span></span>

<span data-ttu-id="01890-148">Hvis du vil ha mer informasjon om funksjonen for gjentatt avbildning av utgiftsrapporter, kan du se [Gjentatt avbildning av utgiftsrapporter](ExpenseWorkspaceNew.md).</span><span class="sxs-lookup"><span data-stu-id="01890-148">For more information about the Expense reports re-imagined feature, see [Expense reports reimagined](ExpenseWorkspaceNew.md).</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="01890-149">Vanlige spørsmål</span><span class="sxs-lookup"><span data-stu-id="01890-149">Frequently asked questions</span></span>

<span data-ttu-id="01890-150">**Bruker Microsoft dataene mine til sine modeller?**</span><span class="sxs-lookup"><span data-stu-id="01890-150">**Does Microsoft use my data for its models?**</span></span>

<span data-ttu-id="01890-151">Nei, Microsoft har bygget en generell maskinlæringsmodell for tjenesten for kvitteringsbehandling.</span><span class="sxs-lookup"><span data-stu-id="01890-151">No, Microsoft has built a general machine learning model for its receipt processing service.</span></span> <span data-ttu-id="01890-152">Denne modellen er ikke basert på kvitteringene som du laster opp.</span><span class="sxs-lookup"><span data-stu-id="01890-152">This model isn't based on the receipts that you upload.</span></span>

<span data-ttu-id="01890-153">**Hvor er denne funksjonen tilgjengelig, og hvor behandles den?**</span><span class="sxs-lookup"><span data-stu-id="01890-153">**Where is this feature available and processed?**</span></span>

<span data-ttu-id="01890-154">For øyeblikket støttes USA.</span><span class="sxs-lookup"><span data-stu-id="01890-154">Currently, the United States is supported.</span></span>

<span data-ttu-id="01890-155">**Hvor ender kvitteringen mine opp?**</span><span class="sxs-lookup"><span data-stu-id="01890-155">**Where do my receipts go?**</span></span>

<span data-ttu-id="01890-156">Finans kontakter Cognitive Services for å trekke ut feltdataene.</span><span class="sxs-lookup"><span data-stu-id="01890-156">Finance will contact Cognitive Services to extract the field data.</span></span> <span data-ttu-id="01890-157">Cognitive Services beholder en kopi av kvitteringen i opptil 24 timer, mens behandling utføres.</span><span class="sxs-lookup"><span data-stu-id="01890-157">Cognitive Services will retain a copy of your receipt for up to 24 hours while processing occurs.</span></span> <span data-ttu-id="01890-158">Når behandlingen er fullført, fjerner Cognitive Services kvitteringen.</span><span class="sxs-lookup"><span data-stu-id="01890-158">After processing is completed, Cognitive Services will remove the receipt.</span></span> <span data-ttu-id="01890-159">Kvitteringer lagres fremdeles i Finans.</span><span class="sxs-lookup"><span data-stu-id="01890-159">Receipts are still stored in Finance.</span></span>

<span data-ttu-id="01890-160">Hvis du vil ha mer informasjon, kan du se [Aktivere kvitteringsforståelse med den nye funksjonaliteten til skjemagjenkjenner](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span><span class="sxs-lookup"><span data-stu-id="01890-160">For more information, see [Enable receipt understanding with Form Recognizer's new capability](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span></span>
