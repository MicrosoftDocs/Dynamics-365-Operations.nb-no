---
title: Finansdimensjoner
description: Dette emnet beskriver de ulike typene finansdimensjoner og hvordan de er definert.
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ems.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DimensionDetails, DimensionValueDetails, SysTranslationDetail
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 25871
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 3950dc3fcd1e293802c88bf2616a27e139b48399
ms.contentlocale: nb-no
ms.lasthandoff: 08/29/2017

---

# <a name="financial-dimensions"></a><span data-ttu-id="f5af8-103">Finansdimensjoner</span><span class="sxs-lookup"><span data-stu-id="f5af8-103">Financial dimensions</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="f5af8-104">Dette emnet forklarer de ulike typene finansdimensjoner og hvordan de er definert.</span><span class="sxs-lookup"><span data-stu-id="f5af8-104">This topic explains the various types of financial dimensions and how they are set up.</span></span>

<span data-ttu-id="f5af8-105">Bruk **Finansdimensjoner**-siden til å opprette finansdimensjoner som du kan bruke som kontosegmenter for kontoplaner.</span><span class="sxs-lookup"><span data-stu-id="f5af8-105">Use the **Financial dimensions** page to create financial dimensions that you can use as account segments for charts of accounts.</span></span> <span data-ttu-id="f5af8-106">Det finnes to typer finansdimensjoner: egendefinerte dimensjoner og enhetsstøttede dimensjoner.</span><span class="sxs-lookup"><span data-stu-id="f5af8-106">There are two types of financial dimensions: custom dimensions and entity-backed dimensions.</span></span> <span data-ttu-id="f5af8-107">Egendefinerte dimensjoner deles på tvers av juridiske enheter, og verdiene angis og vedlikeholdes av brukerne.</span><span class="sxs-lookup"><span data-stu-id="f5af8-107">Custom dimensions are shared across legal entities, and the values are entered and maintained by users.</span></span> <span data-ttu-id="f5af8-108">For enhetsstøttede dimensjoner er verdiene definert andre steder i systemet, for eksempel som kunde- eller butikkenheter.</span><span class="sxs-lookup"><span data-stu-id="f5af8-108">For entity-backed dimensions, the values are defined somewhere else in the system, such as Customers or Stores entities.</span></span> <span data-ttu-id="f5af8-109">Noen enhetsstøttede dimensjoner deles på tvers av juridiske enheter, mens andre enhetsstøttede dimensjoner er firmaspesifikke.</span><span class="sxs-lookup"><span data-stu-id="f5af8-109">Some entity-backed dimensions are shared across legal entities, whereas other entity-backed dimensions are company-specific.</span></span> 

<span data-ttu-id="f5af8-110">Når du har opprettet finansdimensjonene, bruker du **Finansdimensjonsverdier**-siden til å tilordne flere egenskaper til hver finansdimensjon.</span><span class="sxs-lookup"><span data-stu-id="f5af8-110">After you've created the financial dimensions, use the **Financial dimension values** page to assign additional properties to each financial dimension.</span></span> 

<span data-ttu-id="f5af8-111">Du kan bruke finansdimensjoner til å representere juridiske enheter.</span><span class="sxs-lookup"><span data-stu-id="f5af8-111">You can use financial dimensions to represent legal entities.</span></span> <span data-ttu-id="f5af8-112">Du trenger ikke å opprette de juridiske enhetene i Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span><span class="sxs-lookup"><span data-stu-id="f5af8-112">You don't have to create the legal entities in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span></span> <span data-ttu-id="f5af8-113">Finansdimensjoner er imidlertid ikke utviklet for å håndtere drifts- eller forretningbehovene til juridiske enheter.</span><span class="sxs-lookup"><span data-stu-id="f5af8-113">However, financial dimensions aren’t designed to address the operational or business requirements of legal entities.</span></span> <span data-ttu-id="f5af8-114">Funksjonen internenhetsregnskap i Finance and Operations er utviklet for bare å håndtere regnskapsoppføringene som opprettes av hver transaksjon.</span><span class="sxs-lookup"><span data-stu-id="f5af8-114">The interunit accounting functionality in Finance and Operations is designed to address only the accounting entries that are created by each transaction.</span></span> 

<span data-ttu-id="f5af8-115">Før du setter opp finansdimensjoner som juridiske enheter, vurderer du forretningsprosessene i følgende områder for å se hvorvidt dette oppsettet fungerer for din organisasjon:</span><span class="sxs-lookup"><span data-stu-id="f5af8-115">Before you set up financial dimensions as legal entities, evaluate your business processes in the following areas to determine whether this setup will work for your organization:</span></span>

- <span data-ttu-id="f5af8-116">Lager</span><span class="sxs-lookup"><span data-stu-id="f5af8-116">Inventory</span></span>
- <span data-ttu-id="f5af8-117">Kjøp og salg mellom finansdimensjoner og juridiske enheter</span><span class="sxs-lookup"><span data-stu-id="f5af8-117">Sales and purchases between financial dimensions and legal entities</span></span>
- <span data-ttu-id="f5af8-118">Mva-beregning og rapportering</span><span class="sxs-lookup"><span data-stu-id="f5af8-118">Sales tax calculation and reporting</span></span>
- <span data-ttu-id="f5af8-119">Driftsrapportering</span><span class="sxs-lookup"><span data-stu-id="f5af8-119">Operational reporting</span></span>

<span data-ttu-id="f5af8-120">Her er noen av begrensningene:</span><span class="sxs-lookup"><span data-stu-id="f5af8-120">Here are some of the limitations:</span></span>

- <span data-ttu-id="f5af8-121">Du kan bare bruke mva-funksjonaliteten med juridiske enheter, ikke med finansdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="f5af8-121">You can use sales tax functionality only with legal entities, not with financial dimensions.</span></span>
- <span data-ttu-id="f5af8-122">Noen av rapportene inneholder ikke finansdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="f5af8-122">Some reports don't include financial dimensions.</span></span> <span data-ttu-id="f5af8-123">Derfor kan det hende du må endre rapportene for å rapportere etter finansdimensjon.</span><span class="sxs-lookup"><span data-stu-id="f5af8-123">Therefore, to report by financial dimension, you might have to modify the reports.</span></span>

## <a name="custom-dimensions"></a><span data-ttu-id="f5af8-124">Egendefinerte dimensjoner</span><span class="sxs-lookup"><span data-stu-id="f5af8-124">Custom dimensions</span></span>

<span data-ttu-id="f5af8-125">For å opprette en brukerdefinert finansdimensjon velger du **Egendefinerte dimensjoner** i feltet **&lt;Bruk verdier fra&gt;**.</span><span class="sxs-lookup"><span data-stu-id="f5af8-125">To create a user-defined financial dimension, in the **Use values from** field, select **&lt; Custom dimension &gt;**.</span></span> <span data-ttu-id="f5af8-126">Du kan også angi en kontomaske for å begrense mengden og typen informasjon som du kan angi for dimensjonsverdier.</span><span class="sxs-lookup"><span data-stu-id="f5af8-126">You can also specify an account mask to limit the amount and type of information that you can enter for dimension values.</span></span> <span data-ttu-id="f5af8-127">Du kan angi tegn som forblir de samme for hver dimensjonsverdi, for eksempel bokstaver eller en bindestrek (-).</span><span class="sxs-lookup"><span data-stu-id="f5af8-127">You can enter characters that remain the same for each dimension value, such as letters or a hyphen (-).</span></span> <span data-ttu-id="f5af8-128">Du kan også angi nummertegn (\#) og og-tegn (&) om plassholdere for bokstaver og tall som vil endres hver gang en dimensjonsverdi opprettes.</span><span class="sxs-lookup"><span data-stu-id="f5af8-128">You can also enter number signs (\#) and ampersands (&) as placeholders for letters and numbers that will change every time that a dimension value is created.</span></span> <span data-ttu-id="f5af8-129">Bruk et nummertegn (\#) som plassholder for et tall og et og-tegn (&) som plassholder for en bokstav.</span><span class="sxs-lookup"><span data-stu-id="f5af8-129">Use a number sign (\#) as a placeholder for a number and an ampersand (&) as a placeholder for a letter.</span></span> <span data-ttu-id="f5af8-130">Feltet for formatmasken er bare tilgjengelig når du velger **&lt;Egendefinert dimensjon&gt;** i feltet **Bruk verdier fra**.</span><span class="sxs-lookup"><span data-stu-id="f5af8-130">The field for the format mask is available only when you select **&lt; Custom dimension &gt;** in the **Use values from** field.</span></span>

<span data-ttu-id="f5af8-131">**Eksempel**</span><span class="sxs-lookup"><span data-stu-id="f5af8-131">**Example**</span></span>

<span data-ttu-id="f5af8-132">Hvis du vil begrense dimensjonsverdien til bokstavene «CC» og tre tall, kan du angi **CC-\#\#\#** som formatmaske.</span><span class="sxs-lookup"><span data-stu-id="f5af8-132">To limit the dimension value to the letters "CC" and three numbers, enter **CC-\#\#\#** as the format mask.</span></span>

## <a name="entity-backed-dimensions"></a><span data-ttu-id="f5af8-133">Enhetsstøttede dimensjoner</span><span class="sxs-lookup"><span data-stu-id="f5af8-133">Entity-backed dimensions</span></span>

<span data-ttu-id="f5af8-134">Hvis du vil opprette en enhetsstøttet finansdimensjon, velger du en systemdefinert enhet som basis for finansdimensjonen, i feltet **Bruk verdier fra**.</span><span class="sxs-lookup"><span data-stu-id="f5af8-134">To create an entity-backed financial dimension, in the **Use values from** field, select a system-defined entity to base the financial dimension on.</span></span> <span data-ttu-id="f5af8-135">Finansdimensjonsverdier opprettes deretter fra den enheten.</span><span class="sxs-lookup"><span data-stu-id="f5af8-135">Financial dimension values are then created from that entity.</span></span> <span data-ttu-id="f5af8-136">Hvis du for eksempel vil opprette dimensjonsverdier for prosjekter, velger du **Prosjekter**.</span><span class="sxs-lookup"><span data-stu-id="f5af8-136">For example, to create dimension values for projects, select **Projects**.</span></span> <span data-ttu-id="f5af8-137">En dimensjonsverdi opprettes deretter for hvert prosjektnavn.</span><span class="sxs-lookup"><span data-stu-id="f5af8-137">A dimension value is then created for each project name.</span></span> <span data-ttu-id="f5af8-138">Siden **Finansdimensjonsverdier** viser verdiene for enheten.</span><span class="sxs-lookup"><span data-stu-id="f5af8-138">The **Financial dimension values** page shows the values for the entity.</span></span> <span data-ttu-id="f5af8-139">Hvis disse verdiene er firmaspesifikke, viser siden også firmaet.</span><span class="sxs-lookup"><span data-stu-id="f5af8-139">If those values are company-specific, the page also shows the company.</span></span>

## <a name="activating-dimensions"></a><span data-ttu-id="f5af8-140">Aktivering av dimensjoner</span><span class="sxs-lookup"><span data-stu-id="f5af8-140">Activating dimensions</span></span>

<span data-ttu-id="f5af8-141">Når du aktiverer en finansdimensjon, oppdateres tabellen slik at den inkluderer navnet på finansdimensjonen.</span><span class="sxs-lookup"><span data-stu-id="f5af8-141">When you activate a financial dimension, the table is updated so that it includes the name of the financial dimension.</span></span> <span data-ttu-id="f5af8-142">Slettede dimensjoner fjernes.</span><span class="sxs-lookup"><span data-stu-id="f5af8-142">Deleted dimensions are removed.</span></span> <span data-ttu-id="f5af8-143">Du kan angi dimensjonsverdier før du aktiverer en finansdimensjon.</span><span class="sxs-lookup"><span data-stu-id="f5af8-143">You can enter dimension values before you activate a financial dimension.</span></span> <span data-ttu-id="f5af8-144">En finansdimensjon ikke imidlertid ikke brukes hvor som helst før den er aktivert.</span><span class="sxs-lookup"><span data-stu-id="f5af8-144">However, a financial dimension can't be consumed anywhere until it's activated.</span></span> <span data-ttu-id="f5af8-145">Du kan for eksempel ikke legge til en finansdimensjon i en kontostruktur før finansdimensjonen er aktivert.</span><span class="sxs-lookup"><span data-stu-id="f5af8-145">For example, you can't add a financial dimension to an account structure until the financial dimension has been activated.</span></span> <span data-ttu-id="f5af8-146">Når du klikker **Aktiver**, oppdateres alle dimensjoner, og viser statusendringer.</span><span class="sxs-lookup"><span data-stu-id="f5af8-146">When you click **Activate**, all dimensions are updated and show status changes.</span></span> 

## <a name="translations"></a><span data-ttu-id="f5af8-147">Oversettelser</span><span class="sxs-lookup"><span data-stu-id="f5af8-147">Translations</span></span>

<span data-ttu-id="f5af8-148">På siden  **Tekstoversettelse** kan du skrive inn tekst for den valgte finansdimensjonen i forskjellige språk.</span><span class="sxs-lookup"><span data-stu-id="f5af8-148">On the **Text translation** page, you can enter text for the selected financial dimension in various languages.</span></span> <span data-ttu-id="f5af8-149">På siden  **Tekstoversettelse** kan du skrive inn tekst for hovedkontoen i forskjellige språk.</span><span class="sxs-lookup"><span data-stu-id="f5af8-149">On the **Main account translation** page, you can enter text for the main account in various languages.</span></span> 

## <a name="legal-entity-overrides"></a><span data-ttu-id="f5af8-150">Overstyringer for juridisk enhet</span><span class="sxs-lookup"><span data-stu-id="f5af8-150">Legal entity overrides</span></span>

<span data-ttu-id="f5af8-151">Alle dimensjonene er ikke gyldig for alle juridiske enheter.</span><span class="sxs-lookup"><span data-stu-id="f5af8-151">Not all dimensions are valid for all legal entities.</span></span> <span data-ttu-id="f5af8-152">Dessuten kan noen dimensjoner bare være relevante i en bestemt periode.</span><span class="sxs-lookup"><span data-stu-id="f5af8-152">Additionally, some dimensions might be relevant only for a specific period.</span></span> <span data-ttu-id="f5af8-153">I disse tilfellene kan du bruke delen **Overstyringer for juridisk enhet** til å angi firmaene dimensjonen skal suspenderes for, eieren, og tidsperioden dimensjonen er aktiv.</span><span class="sxs-lookup"><span data-stu-id="f5af8-153">In these cases, you can use the **Legal entity overrides** section to specify the companies that the dimension should be suspended for, the owner, and the period when the dimension is active.</span></span>

## <a name="deleting-financial-dimensions"></a><span data-ttu-id="f5af8-154">Slette finansdimensjoner</span><span class="sxs-lookup"><span data-stu-id="f5af8-154">Deleting financial dimensions</span></span>

<span data-ttu-id="f5af8-155">For å opprettholde referanseintegriteten for dataene, kan finansdimensjoner sjelden slettes.</span><span class="sxs-lookup"><span data-stu-id="f5af8-155">To help maintain referential integrity of the data, financial dimensions can rarely be deleted.</span></span> <span data-ttu-id="f5af8-156">Hvis du prøver å slette en finansdimensjon, evalueres følgende kriterier:</span><span class="sxs-lookup"><span data-stu-id="f5af8-156">If you try to delete a financial dimension, the following criteria are evaluated:</span></span>

- <span data-ttu-id="f5af8-157">Er finansdimensjonen brukt på posterte eller uposterte transaksjoner, eller en type dimensjonsverdikombinasjon?</span><span class="sxs-lookup"><span data-stu-id="f5af8-157">Has the financial dimension been used on any posted or unposted transactions, or any type of dimension value combination?</span></span>
- <span data-ttu-id="f5af8-158">Er finansdimensjonen brukt i en aktiv kontostruktur, avansert regelstruktur eller i et finansdimensjonssett?</span><span class="sxs-lookup"><span data-stu-id="f5af8-158">Is the financial dimension used in any active account structure, advanced rule structure, or financial dimension set?</span></span>
- <span data-ttu-id="f5af8-159">Er finansdimensjonen en del et standardformat for finansdimensjonsintegrasjon?</span><span class="sxs-lookup"><span data-stu-id="f5af8-159">Is the financial dimension part of a default financial dimension integration format?</span></span>
- <span data-ttu-id="f5af8-160">Er finansdimensjonen er satt opp som standarddimensjon?</span><span class="sxs-lookup"><span data-stu-id="f5af8-160">Has the financial dimension been set up as a default dimension?</span></span>

<span data-ttu-id="f5af8-161">Hvis ett av vilkårene er oppfylt, kan du ikke slette finansdimensjonen.</span><span class="sxs-lookup"><span data-stu-id="f5af8-161">If any of the criteria are met, you can't delete the financial dimension.</span></span>


<span data-ttu-id="f5af8-162">Hvis du vil ha mer informasjon, se følgende emner:</span><span class="sxs-lookup"><span data-stu-id="f5af8-162">For more information, see the following topics:</span></span>
- [<span data-ttu-id="f5af8-163">Definere finansdimensjoner</span><span class="sxs-lookup"><span data-stu-id="f5af8-163">Define financial dimensions</span></span>](tasks/define-financial-dimensions.md)
- [<span data-ttu-id="f5af8-164">Vedlikeholde standardmaler for finansdimensjon</span><span class="sxs-lookup"><span data-stu-id="f5af8-164">Maintain financial dimension default templates</span></span>](tasks/maintain-financial-dimension-default-templates.md)

