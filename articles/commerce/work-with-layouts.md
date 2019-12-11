---
title: Arbeide med forhåndsinnstilte oppsett
description: Dette emnet beskriver hvordan du arbeider med forhåndsinnstilte oppsett i Microsoft Dynamics 365 Commerce.
author: phinneyridge
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1f2c0638caa7e4f6f831e592e3f7e3f5ab7d1d81
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697825"
---
# <a name="work-with-preset-layouts"></a><span data-ttu-id="91678-103">Arbeide med forhåndsinnstilte oppsett</span><span class="sxs-lookup"><span data-stu-id="91678-103">Work with preset layouts</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="91678-104">Dette emnet beskriver hvordan du arbeider med forhåndsinnstilte oppsett i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="91678-104">This topic describes how to work with preset layouts in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="91678-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="91678-105">Overview</span></span>

<span data-ttu-id="91678-106">Før du fullfører prosedyrene i dette emnet, må du lese [Forhåndsinnstilte og egendefinerte oppsett](templates-layouts-overview.md#preset-and-custom-layouts).</span><span class="sxs-lookup"><span data-stu-id="91678-106">Before you complete the procedures in this topic, be sure to read [Preset and custom layouts](templates-layouts-overview.md#preset-and-custom-layouts).</span></span> <span data-ttu-id="91678-107">Du finner en generell oversikt i [Oversikt over maler og oppsett](templates-layouts-overview.md).</span><span class="sxs-lookup"><span data-stu-id="91678-107">For a general overview, see [Templates and layouts overview](templates-layouts-overview.md).</span></span>

## <a name="create-a-new-preset-layout"></a><span data-ttu-id="91678-108">Opprette et nytt forhåndsinnstilt oppsett</span><span class="sxs-lookup"><span data-stu-id="91678-108">Create a new preset layout</span></span>

<span data-ttu-id="91678-109">Det finnes to metoder for å opprette en forhåndsinnstilt oppsett.</span><span class="sxs-lookup"><span data-stu-id="91678-109">There are two methods for creating a preset layout.</span></span> <span data-ttu-id="91678-110">Du kan lagre et eksisterende egendefinert oppsett som et nytt forhåndsinnstilt oppsett, eller du kan opprette et forhåndsdefinert oppsett fra grunnen av.</span><span class="sxs-lookup"><span data-stu-id="91678-110">You can save an existing custom layout as a new preset layout, or you can create a preset layout from scratch.</span></span>

### <a name="create-a-preset-layout-from-an-existing-custom-layout"></a><span data-ttu-id="91678-111">Opprette et forhåndsinnstilt oppsett fra et eksisterende egendefinert oppsett</span><span class="sxs-lookup"><span data-stu-id="91678-111">Create a preset layout from an existing custom layout</span></span>

<span data-ttu-id="91678-112">Følg disse trinnene for å opprette et forhåndsinnstilt oppsett fra et eksisterende egendefinert oppsett.</span><span class="sxs-lookup"><span data-stu-id="91678-112">To create a preset layout from an existing custom layout, follow these steps.</span></span>

1. <span data-ttu-id="91678-113">Åpne en eksisterende side som ikke bruker et forhåndsinnstilt oppsett, og som har en modulstruktur som du vil bruke på nytt for andre sider på området.</span><span class="sxs-lookup"><span data-stu-id="91678-113">Open an existing page that doesn't currently use a preset layout, and that has a module structure that you want to reuse for other pages on your site.</span></span>
1. <span data-ttu-id="91678-114">Velg **Sjekk ut**.</span><span class="sxs-lookup"><span data-stu-id="91678-114">Select **Check out**.</span></span>
1. <span data-ttu-id="91678-115">Velg **Lagre som nytt oppsett**.</span><span class="sxs-lookup"><span data-stu-id="91678-115">Select **Save as new layout**.</span></span> <span data-ttu-id="91678-116">Dialogboksen **Lagre som nytt oppsett** vises.</span><span class="sxs-lookup"><span data-stu-id="91678-116">The **Save as new layout** dialog box appears.</span></span>
1. <span data-ttu-id="91678-117">Angi et navn og en beskrivelse for det forhåndsinnstilte oppsettet.</span><span class="sxs-lookup"><span data-stu-id="91678-117">Enter a name and description for your preset layout.</span></span> <span data-ttu-id="91678-118">Verdiene du angir, vises for andre forfattere når de oppretter nye sider fra oppsettet eller bytter til dem.</span><span class="sxs-lookup"><span data-stu-id="91678-118">The values that you enter will be shown to other authors when they create new pages from your layout or switch to it.</span></span> <span data-ttu-id="91678-119">Derfor må du angi verdier som kan være nyttige for sideforfattere.</span><span class="sxs-lookup"><span data-stu-id="91678-119">Therefore, enter values that will be useful to page authors.</span></span>
1. <span data-ttu-id="91678-120">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="91678-120">Select **OK**.</span></span>

<span data-ttu-id="91678-121">Det forhåndsinnstilte oppsettet vil nå være tilgjengelig når du oppretter nye sider eller velger et annet oppsett for en side i samme malhierarki.</span><span class="sxs-lookup"><span data-stu-id="91678-121">The preset layout will now be available when you create new pages or select a different layout for a page in the same template hierarchy.</span></span>

> [!TIP]
> <span data-ttu-id="91678-122">Hvis du raskt vil se om en bestemt side er bundet til et forhåndsinnstilt oppsett, velger du siden i sidelistevisningen og undersøker metadataene for oppsett i egenskapsruten til høyre.</span><span class="sxs-lookup"><span data-stu-id="91678-122">To quickly see whether a specific page is currently bound to a preset layout, select the page in the pages list view, and inspect the layout metadata in the property pane on the right.</span></span>

### <a name="create-a-new-preset-layout"></a><span data-ttu-id="91678-123">Opprette et nytt forhåndsinnstilt oppsett</span><span class="sxs-lookup"><span data-stu-id="91678-123">Create a new preset layout</span></span>

<span data-ttu-id="91678-124">Følg disse trinnene for å opprette et forhåndsinnstilt oppsett fra bunnen av.</span><span class="sxs-lookup"><span data-stu-id="91678-124">To create a preset layout from scratch, follow these steps.</span></span>

1. <span data-ttu-id="91678-125">Velg **Oppsett**i navigasjonsruten til venstre.</span><span class="sxs-lookup"><span data-stu-id="91678-125">In the navigation pane on the left, select **Layouts**.</span></span>
1. <span data-ttu-id="91678-126">Velg **Nytt oppsett**.</span><span class="sxs-lookup"><span data-stu-id="91678-126">Select **New Layout**.</span></span> <span data-ttu-id="91678-127">Dialogboksen **Nytt oppsett** vises.</span><span class="sxs-lookup"><span data-stu-id="91678-127">The **New layout** dialog box appears.</span></span>
1. <span data-ttu-id="91678-128">Velg malen som skal brukes for det forhåndsinnstilte oppsettet.</span><span class="sxs-lookup"><span data-stu-id="91678-128">Select the template to use for your preset layout.</span></span>
1. <span data-ttu-id="91678-129">Angi et navn og en beskrivelse for det forhåndsinnstilte oppsettet.</span><span class="sxs-lookup"><span data-stu-id="91678-129">Enter a name and description for your preset layout.</span></span> <span data-ttu-id="91678-130">Verdiene du angir, vises for andre forfattere når de oppretter nye sider fra oppsettet eller bytter til dem.</span><span class="sxs-lookup"><span data-stu-id="91678-130">The values that you enter will be shown to other authors when they create new pages from your layout or switch to it.</span></span> <span data-ttu-id="91678-131">Derfor må du angi verdier som kan være nyttige for sideforfattere.</span><span class="sxs-lookup"><span data-stu-id="91678-131">Therefore, enter values that will be useful to page authors.</span></span>
1. <span data-ttu-id="91678-132">Velg **OK** for å opprette det nye forhåndsinnstilte oppsettet, og åpne redigeringsprogrammet for oppsett.</span><span class="sxs-lookup"><span data-stu-id="91678-132">Select **OK** to create the new preset layout and open the layout editor.</span></span>
1. <span data-ttu-id="91678-133">I oppsettredigering legger du til og konfigurerer moduler ved å bruke disposisjonstreet til venstre og egenskapsruten til høyre.</span><span class="sxs-lookup"><span data-stu-id="91678-133">In the layout editor, add and configure modules by using the outline tree on the left and the property pane on the right.</span></span> <span data-ttu-id="91678-134">(Prosessen ligner på prosessen for å legge til og konfigurere moduler for en mal i malredigeringsprogrammet.) Ordningen av moduler og eventuelle låste standardinnstillinger blir sentralisert modulkonfigurasjon for alle sider som bruker dette forhåndsinnstilte oppsettet.</span><span class="sxs-lookup"><span data-stu-id="91678-134">(The process resembles the process for adding and configuring modules for a template in the template editor.) The arrangement of modules and any locked default settings become the centralized module configuration for any pages that use this preset layout.</span></span>

## <a name="modify-a-preset-layout"></a><span data-ttu-id="91678-135">Endre et forhåndsinnstilt oppsett</span><span class="sxs-lookup"><span data-stu-id="91678-135">Modify a preset layout</span></span>

<span data-ttu-id="91678-136">Følg disse trinnene for å endre et forhåndsinnstilt oppsett.</span><span class="sxs-lookup"><span data-stu-id="91678-136">To modify a preset layout, follow these steps.</span></span>

1. <span data-ttu-id="91678-137">Velg **Oppsett**i navigasjonsruten til venstre.</span><span class="sxs-lookup"><span data-stu-id="91678-137">In the navigation pane on the left, select **Layouts**.</span></span>
1. <span data-ttu-id="91678-138">Velg modulen du vil endre, i disposisjonstreet til venstre i oppsettredigering.</span><span class="sxs-lookup"><span data-stu-id="91678-138">In the layout editor, in the outline tree on the left, select the module to modify.</span></span> <span data-ttu-id="91678-139">Følg deretter et av disse trinnene:</span><span class="sxs-lookup"><span data-stu-id="91678-139">Then follow any of these steps:</span></span>

    - <span data-ttu-id="91678-140">Hvis du vil flytte en modul opp eller ned i det overordnede elementet, velger du ellipseknappen (**...**) for modulen, og deretter velger du **Flytt opp** eller **Flytt ned**.</span><span class="sxs-lookup"><span data-stu-id="91678-140">To move a module up or down inside its parent, select the ellipsis button (**...**) for the module, and then select **Move up** or **Move down**.</span></span>
    - <span data-ttu-id="91678-141">Hvis du vil endre standardinnstillingene for en modul, kan du bruke egenskapsruten til å angi standardverdier og eventuelt låse dem for alle nedstrømssider.</span><span class="sxs-lookup"><span data-stu-id="91678-141">To change a module's default settings, use the property pane to enter default values and optionally lock them for all downstream pages.</span></span>
    - <span data-ttu-id="91678-142">Hvis du vil legge til nye moduler eller fragmenter i containermoduler, velger du ellipseknappen og deretter **Legg til modul** eller **Legg til fragment**.</span><span class="sxs-lookup"><span data-stu-id="91678-142">To add new modules or fragments to container modules, select the ellipsis button, and then select **Add module** or **Add fragment**.</span></span>
    - <span data-ttu-id="91678-143">Hvis du vil fjerne en modul fra oppsettet, velger du ellipseknappen og deretter **Slett**.</span><span class="sxs-lookup"><span data-stu-id="91678-143">To remove a module from the layout, select the ellipsis button, and then select **Delete**.</span></span>

## <a name="change-a-preset-layout-theme"></a><span data-ttu-id="91678-144">Endre et forhåndsinnstilt oppsettema</span><span class="sxs-lookup"><span data-stu-id="91678-144">Change a preset layout theme</span></span>

<span data-ttu-id="91678-145">En vanlig praksis er å angi et standardtema for alle sider som bruker et forhåndsinnstilt oppsett.</span><span class="sxs-lookup"><span data-stu-id="91678-145">A typical practice is to set a default theme for all pages that use a preset layout.</span></span>

<span data-ttu-id="91678-146">Hvis du vil angi eller endre temaet for alle underordnede sider som bruker det forhåndsinnstilte oppsettet, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="91678-146">To set or change the theme for all child pages that use your preset layout, follow these steps.</span></span>

1. <span data-ttu-id="91678-147">Velg sidecontainermodulen i disposisjonstreet til venstre i oppsettredigering.</span><span class="sxs-lookup"><span data-stu-id="91678-147">In the layout editor, in the outline tree on the left, select the page container module.</span></span> <span data-ttu-id="91678-148">(Denne modulen er vanligvis den andre noden og kalles **Standardside**.)</span><span class="sxs-lookup"><span data-stu-id="91678-148">(Typically, this module is the second node and is named **Default page**.)</span></span>
1. <span data-ttu-id="91678-149">I egenskapsruten til høyre velger du et tema i feltet **Tema**.</span><span class="sxs-lookup"><span data-stu-id="91678-149">In the property pane on the right, in the **Theme** field, select a theme.</span></span>

## <a name="save-check-in-preview-and-publish-a-preset-layout"></a><span data-ttu-id="91678-150">Lagre, sjekke inn, forhåndsvise og publisere et forhåndsinnstilt oppsett</span><span class="sxs-lookup"><span data-stu-id="91678-150">Save, check in, preview, and publish a preset layout</span></span>

<span data-ttu-id="91678-151">Hvis du vil lagre og sjekke inn det forhåndsinnstilte oppsettet, følger du disse trinnene:</span><span class="sxs-lookup"><span data-stu-id="91678-151">To save and check in your preset layout, follow these steps.</span></span>

1. <span data-ttu-id="91678-152">Velg **Lagre** øverst i oppsettredigeringsprogrammet.</span><span class="sxs-lookup"><span data-stu-id="91678-152">Select **Save** at the top of the layout editor.</span></span> <span data-ttu-id="91678-153">Lagrede endringer påvirker ikke nedstrømssider før de er sjekket inn.</span><span class="sxs-lookup"><span data-stu-id="91678-153">Saved changes don't affect downstream pages until they are checked in.</span></span>
1. <span data-ttu-id="91678-154">Velg **Sjekk inn**.</span><span class="sxs-lookup"><span data-stu-id="91678-154">Select **Check In**.</span></span> <span data-ttu-id="91678-155">Dine endringer er nå synlige for nedstrøms arbeidsflyter.</span><span class="sxs-lookup"><span data-stu-id="91678-155">Your changes are now discoverable for downstream workflows.</span></span>

<span data-ttu-id="91678-156">Hvis du vil forhåndsvise endringene, kan du enten åpne en eksisterende side som bruker det forhåndsinnstilte oppsettet, eller opprette en ny side fra oppsettet.</span><span class="sxs-lookup"><span data-stu-id="91678-156">To preview your changes, either open an existing page that uses the preset layout or create a new page from the layout.</span></span>

<span data-ttu-id="91678-157">Når du har forhåndsvist endringene i det forhåndsinnstilte oppsettet, følger du en av disse fremgangsmåtene for å publisere oppsettet på ditt aktive område:</span><span class="sxs-lookup"><span data-stu-id="91678-157">After you've previewed the changes to your preset layout, follow one of these steps to publish the layout to your live site:</span></span>

* <span data-ttu-id="91678-158">Gå til **Oppsett**, velg oppsettet, og velg deretter **Publiser**.</span><span class="sxs-lookup"><span data-stu-id="91678-158">Go to **Layouts**, select the layout, and then select **Publish**.</span></span>
* <span data-ttu-id="91678-159">Velg **Publiser** i redigeringsprogrammet for oppsett.</span><span class="sxs-lookup"><span data-stu-id="91678-159">In the layout editor, select **Publish**.</span></span>
* <span data-ttu-id="91678-160">Publiser en side som refererer til det upubliserte oppsettet.</span><span class="sxs-lookup"><span data-stu-id="91678-160">Publish a page that references the unpublished layout.</span></span> <span data-ttu-id="91678-161">Oppsettet vil automatisk bli publisert.</span><span class="sxs-lookup"><span data-stu-id="91678-161">The layout will automatically be published.</span></span>

> [!WARNING]
> <span data-ttu-id="91678-162">Du kan referere til forhåndsinnstilte oppsett på flere sider.</span><span class="sxs-lookup"><span data-stu-id="91678-162">Preset layouts can be referenced by multiple pages.</span></span> <span data-ttu-id="91678-163">Når du publiserer et forhåndsinnstilt oppsett, må du være oppmerksom på at du kan påvirke oppsettet på flere sider.</span><span class="sxs-lookup"><span data-stu-id="91678-163">When you publish a preset layout, be aware that you might affect the layout of multiple pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="91678-164">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="91678-164">Additional resources</span></span>

[<span data-ttu-id="91678-165">Oversikt over maler og oppsett</span><span class="sxs-lookup"><span data-stu-id="91678-165">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="91678-166">Arbeide med maler</span><span class="sxs-lookup"><span data-stu-id="91678-166">Work with templates</span></span>](work-with-templates.md)
