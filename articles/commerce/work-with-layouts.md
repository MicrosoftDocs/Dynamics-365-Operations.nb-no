---
title: Arbeide med forhåndsinnstilte oppsett
description: Dette emnet beskriver hvordan du arbeider med forhåndsinnstilte oppsett i Microsoft Dynamics 365 Commerce.
author: phinneyridge
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: ce54be1032777ffcaac474773cdeeef3b9028110
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5793927"
---
# <a name="work-with-preset-layouts"></a><span data-ttu-id="24a19-103">Arbeide med forhåndsinnstilte oppsett</span><span class="sxs-lookup"><span data-stu-id="24a19-103">Work with preset layouts</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="24a19-104">Dette emnet beskriver hvordan du arbeider med forhåndsinnstilte oppsett i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="24a19-104">This topic describes how to work with preset layouts in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="24a19-105">Før du fullfører prosedyrene i dette emnet, må du lese [Forhåndsinnstilte og egendefinerte oppsett](templates-layouts-overview.md#preset-and-custom-layouts).</span><span class="sxs-lookup"><span data-stu-id="24a19-105">Before you complete the procedures in this topic, be sure to read [Preset and custom layouts](templates-layouts-overview.md#preset-and-custom-layouts).</span></span> <span data-ttu-id="24a19-106">Du finner en generell oversikt i [Oversikt over maler og oppsett](templates-layouts-overview.md).</span><span class="sxs-lookup"><span data-stu-id="24a19-106">For a general overview, see [Templates and layouts overview](templates-layouts-overview.md).</span></span>

## <a name="create-a-new-preset-layout"></a><span data-ttu-id="24a19-107">Opprette et nytt forhåndsinnstilt oppsett</span><span class="sxs-lookup"><span data-stu-id="24a19-107">Create a new preset layout</span></span>

<span data-ttu-id="24a19-108">Det finnes to metoder for å opprette en forhåndsinnstilt oppsett.</span><span class="sxs-lookup"><span data-stu-id="24a19-108">There are two methods for creating a preset layout.</span></span> <span data-ttu-id="24a19-109">Du kan lagre et eksisterende egendefinert oppsett som et nytt forhåndsinnstilt oppsett, eller du kan opprette et forhåndsdefinert oppsett fra grunnen av.</span><span class="sxs-lookup"><span data-stu-id="24a19-109">You can save an existing custom layout as a new preset layout, or you can create a preset layout from scratch.</span></span>

### <a name="create-a-preset-layout-from-an-existing-custom-layout"></a><span data-ttu-id="24a19-110">Opprette et forhåndsinnstilt oppsett fra et eksisterende egendefinert oppsett</span><span class="sxs-lookup"><span data-stu-id="24a19-110">Create a preset layout from an existing custom layout</span></span>

<span data-ttu-id="24a19-111">Følg disse trinnene for å opprette et forhåndsinnstilt oppsett fra et eksisterende egendefinert oppsett.</span><span class="sxs-lookup"><span data-stu-id="24a19-111">To create a preset layout from an existing custom layout, follow these steps.</span></span>

1. <span data-ttu-id="24a19-112">Åpne en eksisterende side som ikke bruker et forhåndsinnstilt oppsett, og som har en modulstruktur som du vil bruke på nytt for andre sider på området.</span><span class="sxs-lookup"><span data-stu-id="24a19-112">Open an existing page that doesn't currently use a preset layout, and that has a module structure that you want to reuse for other pages on your site.</span></span>
1. <span data-ttu-id="24a19-113">Velg **Rediger** for å sjekke ut siden.</span><span class="sxs-lookup"><span data-stu-id="24a19-113">Select **Edit** to check out the page.</span></span>
1. <span data-ttu-id="24a19-114">Velg **Lagre som nytt oppsett**.</span><span class="sxs-lookup"><span data-stu-id="24a19-114">Select **Save as new layout**.</span></span> <span data-ttu-id="24a19-115">Dialogboksen **Lagre som nytt oppsett** vises.</span><span class="sxs-lookup"><span data-stu-id="24a19-115">The **Save as new layout** dialog box appears.</span></span>
1. <span data-ttu-id="24a19-116">Angi et navn og en beskrivelse for det forhåndsinnstilte oppsettet.</span><span class="sxs-lookup"><span data-stu-id="24a19-116">Enter a name and description for your preset layout.</span></span> <span data-ttu-id="24a19-117">Verdiene du angir, vises for andre forfattere når de oppretter nye sider fra oppsettet eller bytter til dem.</span><span class="sxs-lookup"><span data-stu-id="24a19-117">The values that you enter will be shown to other authors when they create new pages from your layout or switch to it.</span></span> <span data-ttu-id="24a19-118">Derfor må du angi verdier som kan være nyttige for sideforfattere.</span><span class="sxs-lookup"><span data-stu-id="24a19-118">Therefore, enter values that will be useful to page authors.</span></span>
1. <span data-ttu-id="24a19-119">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="24a19-119">Select **OK**.</span></span>

<span data-ttu-id="24a19-120">Det forhåndsinnstilte oppsettet vil nå være tilgjengelig når du oppretter nye sider eller velger et annet oppsett for en side i samme malhierarki.</span><span class="sxs-lookup"><span data-stu-id="24a19-120">The preset layout will now be available when you create new pages or select a different layout for a page in the same template hierarchy.</span></span>

> [!TIP]
> <span data-ttu-id="24a19-121">Hvis du raskt vil se om en bestemt side er bundet til et forhåndsinnstilt oppsett, velger du siden i sidelistevisningen og undersøker metadataene for oppsett i egenskapsruten til høyre.</span><span class="sxs-lookup"><span data-stu-id="24a19-121">To quickly see whether a specific page is currently bound to a preset layout, select the page in the pages list view, and inspect the layout metadata in the property pane on the right.</span></span>

### <a name="create-a-new-preset-layout"></a><span data-ttu-id="24a19-122">Opprette et nytt forhåndsinnstilt oppsett</span><span class="sxs-lookup"><span data-stu-id="24a19-122">Create a new preset layout</span></span>

<span data-ttu-id="24a19-123">Følg disse trinnene for å opprette et forhåndsinnstilt oppsett fra bunnen av.</span><span class="sxs-lookup"><span data-stu-id="24a19-123">To create a preset layout from scratch, follow these steps.</span></span>

1. <span data-ttu-id="24a19-124">Velg **Oppsett** i navigasjonsruten til venstre.</span><span class="sxs-lookup"><span data-stu-id="24a19-124">In the navigation pane on the left, select **Layouts**.</span></span>
1. <span data-ttu-id="24a19-125">Velg **Nytt oppsett**.</span><span class="sxs-lookup"><span data-stu-id="24a19-125">Select **New Layout**.</span></span> <span data-ttu-id="24a19-126">Dialogboksen **Nytt oppsett** vises.</span><span class="sxs-lookup"><span data-stu-id="24a19-126">The **New layout** dialog box appears.</span></span>
1. <span data-ttu-id="24a19-127">Velg malen som skal brukes for det forhåndsinnstilte oppsettet.</span><span class="sxs-lookup"><span data-stu-id="24a19-127">Select the template to use for your preset layout.</span></span>
1. <span data-ttu-id="24a19-128">Angi et navn og en beskrivelse for det forhåndsinnstilte oppsettet.</span><span class="sxs-lookup"><span data-stu-id="24a19-128">Enter a name and description for your preset layout.</span></span> <span data-ttu-id="24a19-129">Verdiene du angir, vises for andre forfattere når de oppretter nye sider fra oppsettet eller bytter til dem.</span><span class="sxs-lookup"><span data-stu-id="24a19-129">The values that you enter will be shown to other authors when they create new pages from your layout or switch to it.</span></span> <span data-ttu-id="24a19-130">Derfor må du angi verdier som kan være nyttige for sideforfattere.</span><span class="sxs-lookup"><span data-stu-id="24a19-130">Therefore, enter values that will be useful to page authors.</span></span>
1. <span data-ttu-id="24a19-131">Velg **OK** for å opprette det nye forhåndsinnstilte oppsettet, og åpne redigeringsprogrammet for oppsett.</span><span class="sxs-lookup"><span data-stu-id="24a19-131">Select **OK** to create the new preset layout and open the layout editor.</span></span>
1. <span data-ttu-id="24a19-132">I oppsettredigering legger du til og konfigurerer moduler ved å bruke disposisjonstreet til venstre og egenskapsruten til høyre.</span><span class="sxs-lookup"><span data-stu-id="24a19-132">In the layout editor, add and configure modules by using the outline tree on the left and the property pane on the right.</span></span> <span data-ttu-id="24a19-133">(Prosessen ligner på prosessen for å legge til og konfigurere moduler for en mal i malredigeringsprogrammet.) Ordningen av moduler og eventuelle låste standardinnstillinger blir sentralisert modulkonfigurasjon for alle sider som bruker dette forhåndsinnstilte oppsettet.</span><span class="sxs-lookup"><span data-stu-id="24a19-133">(The process resembles the process for adding and configuring modules for a template in the template editor.) The arrangement of modules and any locked default settings become the centralized module configuration for any pages that use this preset layout.</span></span>

## <a name="modify-a-preset-layout"></a><span data-ttu-id="24a19-134">Endre et forhåndsinnstilt oppsett</span><span class="sxs-lookup"><span data-stu-id="24a19-134">Modify a preset layout</span></span>

<span data-ttu-id="24a19-135">Følg disse trinnene for å endre et forhåndsinnstilt oppsett.</span><span class="sxs-lookup"><span data-stu-id="24a19-135">To modify a preset layout, follow these steps.</span></span>

1. <span data-ttu-id="24a19-136">Velg **Oppsett** i navigasjonsruten til venstre.</span><span class="sxs-lookup"><span data-stu-id="24a19-136">In the navigation pane on the left, select **Layouts**.</span></span>
1. <span data-ttu-id="24a19-137">Velg modulen du vil endre, i disposisjonstreet til venstre i oppsettredigering.</span><span class="sxs-lookup"><span data-stu-id="24a19-137">In the layout editor, in the outline tree on the left, select the module to modify.</span></span> <span data-ttu-id="24a19-138">Følg deretter et av disse trinnene:</span><span class="sxs-lookup"><span data-stu-id="24a19-138">Then follow any of these steps:</span></span>

    - <span data-ttu-id="24a19-139">Hvis du vil flytte en modul opp eller ned i det overordnede elementet, velger du ellipseknappen (**...**) for modulen, og deretter velger du **Flytt opp** eller **Flytt ned**.</span><span class="sxs-lookup"><span data-stu-id="24a19-139">To move a module up or down inside its parent, select the ellipsis button (**...**) for the module, and then select **Move up** or **Move down**.</span></span>
    - <span data-ttu-id="24a19-140">Hvis du vil endre standardinnstillingene for en modul, kan du bruke egenskapsruten til å angi standardverdier og eventuelt låse dem for alle nedstrømssider.</span><span class="sxs-lookup"><span data-stu-id="24a19-140">To change a module's default settings, use the property pane to enter default values and optionally lock them for all downstream pages.</span></span>
    - <span data-ttu-id="24a19-141">Hvis du vil legge til nye moduler eller fragmenter i containermoduler, velger du ellipseknappen og deretter **Legg til modul** eller **Legg til fragment**.</span><span class="sxs-lookup"><span data-stu-id="24a19-141">To add new modules or fragments to container modules, select the ellipsis button, and then select **Add module** or **Add fragment**.</span></span>
    - <span data-ttu-id="24a19-142">Hvis du vil fjerne en modul fra oppsettet, velger du ellipseknappen og deretter **Slett**.</span><span class="sxs-lookup"><span data-stu-id="24a19-142">To remove a module from the layout, select the ellipsis button, and then select **Delete**.</span></span>

## <a name="change-a-preset-layout-theme"></a><span data-ttu-id="24a19-143">Endre et forhåndsinnstilt oppsettema</span><span class="sxs-lookup"><span data-stu-id="24a19-143">Change a preset layout theme</span></span>

<span data-ttu-id="24a19-144">En vanlig praksis er å angi et standardtema for alle sider som bruker et forhåndsinnstilt oppsett.</span><span class="sxs-lookup"><span data-stu-id="24a19-144">A typical practice is to set a default theme for all pages that use a preset layout.</span></span>

<span data-ttu-id="24a19-145">Hvis du vil angi eller endre temaet for alle underordnede sider som bruker det forhåndsinnstilte oppsettet, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="24a19-145">To set or change the theme for all child pages that use your preset layout, follow these steps.</span></span>

1. <span data-ttu-id="24a19-146">Velg sidecontainermodulen i disposisjonstreet til venstre i oppsettredigering.</span><span class="sxs-lookup"><span data-stu-id="24a19-146">In the layout editor, in the outline tree on the left, select the page container module.</span></span> <span data-ttu-id="24a19-147">(Denne modulen er vanligvis den andre noden og kalles **Standardside**.)</span><span class="sxs-lookup"><span data-stu-id="24a19-147">(Typically, this module is the second node and is named **Default page**.)</span></span>
1. <span data-ttu-id="24a19-148">I egenskapsruten til høyre velger du et tema i feltet **Tema**.</span><span class="sxs-lookup"><span data-stu-id="24a19-148">In the property pane on the right, in the **Theme** field, select a theme.</span></span>

## <a name="save-check-in-preview-and-publish-a-preset-layout"></a><span data-ttu-id="24a19-149">Lagre, sjekke inn, forhåndsvise og publisere et forhåndsinnstilt oppsett</span><span class="sxs-lookup"><span data-stu-id="24a19-149">Save, check in, preview, and publish a preset layout</span></span>

<span data-ttu-id="24a19-150">Hvis du vil lagre og sjekke inn det forhåndsinnstilte oppsettet, følger du disse trinnene:</span><span class="sxs-lookup"><span data-stu-id="24a19-150">To save and check in your preset layout, follow these steps.</span></span>

1. <span data-ttu-id="24a19-151">Velg **Lagre** øverst i oppsettredigeringsprogrammet.</span><span class="sxs-lookup"><span data-stu-id="24a19-151">Select **Save** at the top of the layout editor.</span></span> <span data-ttu-id="24a19-152">Lagrede endringer påvirker ikke nedstrømssider før de er sjekket inn.</span><span class="sxs-lookup"><span data-stu-id="24a19-152">Saved changes don't affect downstream pages until they are checked in.</span></span>
1. <span data-ttu-id="24a19-153">Velg **Fullfør redigering**.</span><span class="sxs-lookup"><span data-stu-id="24a19-153">Select **Finish editing**.</span></span> <span data-ttu-id="24a19-154">Dine endringer er nå synlige for nedstrøms arbeidsflyter.</span><span class="sxs-lookup"><span data-stu-id="24a19-154">Your changes are now discoverable for downstream workflows.</span></span>

<span data-ttu-id="24a19-155">Hvis du vil forhåndsvise endringene, kan du enten åpne en eksisterende side som bruker det forhåndsinnstilte oppsettet, eller opprette en ny side fra oppsettet.</span><span class="sxs-lookup"><span data-stu-id="24a19-155">To preview your changes, either open an existing page that uses the preset layout or create a new page from the layout.</span></span>

<span data-ttu-id="24a19-156">Når du har forhåndsvist endringene i det forhåndsinnstilte oppsettet, følger du en av disse fremgangsmåtene for å publisere oppsettet på ditt aktive område:</span><span class="sxs-lookup"><span data-stu-id="24a19-156">After you've previewed the changes to your preset layout, follow one of these steps to publish the layout to your live site:</span></span>

* <span data-ttu-id="24a19-157">Gå til **Oppsett**, velg oppsettet, og velg deretter **Publiser**.</span><span class="sxs-lookup"><span data-stu-id="24a19-157">Go to **Layouts**, select the layout, and then select **Publish**.</span></span>
* <span data-ttu-id="24a19-158">Velg oppsettnavnet for å åpne redigeringsprogrammet for oppsett, og velg deretter **Publiser**.</span><span class="sxs-lookup"><span data-stu-id="24a19-158">Select the layout name to open the layout editor, and then select **Publish**.</span></span>
* <span data-ttu-id="24a19-159">Publiser en side som refererer til det upubliserte oppsettet.</span><span class="sxs-lookup"><span data-stu-id="24a19-159">Publish a page that references the unpublished layout.</span></span> <span data-ttu-id="24a19-160">Oppsettet vil automatisk bli publisert.</span><span class="sxs-lookup"><span data-stu-id="24a19-160">The layout will automatically be published.</span></span>

> [!WARNING]
> <span data-ttu-id="24a19-161">Du kan referere til forhåndsinnstilte oppsett på flere sider.</span><span class="sxs-lookup"><span data-stu-id="24a19-161">Preset layouts can be referenced by multiple pages.</span></span> <span data-ttu-id="24a19-162">Når du publiserer et forhåndsinnstilt oppsett, må du være oppmerksom på at du kan påvirke oppsettet på flere sider.</span><span class="sxs-lookup"><span data-stu-id="24a19-162">When you publish a preset layout, be aware that you might affect the layout of multiple pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="24a19-163">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="24a19-163">Additional resources</span></span>

[<span data-ttu-id="24a19-164">Oversikt over maler og oppsett</span><span class="sxs-lookup"><span data-stu-id="24a19-164">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="24a19-165">Arbeide med maler</span><span class="sxs-lookup"><span data-stu-id="24a19-165">Work with templates</span></span>](work-with-templates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
