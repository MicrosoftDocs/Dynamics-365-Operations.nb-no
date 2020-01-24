---
title: Unngå avkorting av tekst på stillingshierarki og eksport til Visio
description: Dette emnet forklarer hvordan du løser et problem der navn på personer og stillinger avkortes når kunder viser stillingshierarkiet i Microsoft Dynamics 365 Talent. Avkorting av teksten kan gjøre det vanskelig å ta et skjermbilde eller skrive ut hierarkiet.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 22e8570ccb53e8a7be2c57d3f14fe8034bdb699b
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/06/2019
ms.locfileid: "2898902"
---
# <a name="avoid-text-truncation-on-the-position-hierarchy-and-export-to-visio"></a><span data-ttu-id="5eb46-104">Unngå avkorting av tekst på stillingshierarki og eksport til Visio</span><span class="sxs-lookup"><span data-stu-id="5eb46-104">Avoid text truncation on the position hierarchy and export to Visio</span></span>

<span data-ttu-id="5eb46-105">**Avgang**</span><span class="sxs-lookup"><span data-stu-id="5eb46-105">**Issue**</span></span>

<span data-ttu-id="5eb46-106">Når en kunder viser stillingshierarkiet i Microsoft Dynamics 365 Talent, avkortes navnene på personer og stillinger.</span><span class="sxs-lookup"><span data-stu-id="5eb46-106">When a customer views the position hierarchy in Microsoft Dynamics 365 Talent, the names of individuals and positions are truncated.</span></span> <span data-ttu-id="5eb46-107">Derfor kan det være vanskelig å ta et skjermbilde eller skrive ut og distribuere hierarkiet.</span><span class="sxs-lookup"><span data-stu-id="5eb46-107">Therefore, it can be difficult to take a screenshot, or to print and distribute the hierarchy.</span></span>

![Stillingshierarki](media/position-h.png)

<span data-ttu-id="5eb46-109">**Årsak**</span><span class="sxs-lookup"><span data-stu-id="5eb46-109">**Cause**</span></span>

<span data-ttu-id="5eb46-110">Denne virkemåten er standard.</span><span class="sxs-lookup"><span data-stu-id="5eb46-110">This behavior is by design.</span></span>

<span data-ttu-id="5eb46-111">**Oppløsning**</span><span class="sxs-lookup"><span data-stu-id="5eb46-111">**Resolution**</span></span>

<span data-ttu-id="5eb46-112">Dessverre kan ikke brukere endre størrelsen på teksten på en enkel måte.</span><span class="sxs-lookup"><span data-stu-id="5eb46-112">Unfortunately, users can't easily change the size of the text.</span></span> <span data-ttu-id="5eb46-113">Du kan imidlertid eksportere stillingshierarkiet fra Talent og deretter importere det til Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="5eb46-113">However, you can export the position hierarchy out of Talent and then import it into Microsoft Visio.</span></span> <span data-ttu-id="5eb46-114">Selv om den følgende artikkelen ble skrevet for Microsoft Dynamics AX 2012, gjelder prosessen også for Talent: [Eksportere et stillingshierarki til Microsoft Visio](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/export-a-position-hierarchy-to-microsoft-visio).</span><span class="sxs-lookup"><span data-stu-id="5eb46-114">Although the following article was written for Microsoft Dynamics AX 2012, the process still applies to Talent: [Export a position hierarchy to Microsoft Visio](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/export-a-position-hierarchy-to-microsoft-visio).</span></span>

<span data-ttu-id="5eb46-115">Følg denne fremgangsmåten for å eksportere til Visio.</span><span class="sxs-lookup"><span data-stu-id="5eb46-115">Follow these steps to export to Visio.</span></span>

1. <span data-ttu-id="5eb46-116">I Talent åpner du **Stillinger**-listesiden.</span><span class="sxs-lookup"><span data-stu-id="5eb46-116">In Talent, open the **Positions** list page.</span></span>

    <span data-ttu-id="5eb46-117">Hvis du vil inkludere mer informasjon i organisasjonsstrukturdiagrammet, legger du til felt i **Stillinger**-listen, slik at de er tilgjengelige når du bruker veiviseren senere i denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="5eb46-117">To include more information in the organization structure diagram, add fields to the **Positions** list, so that they are available when you use the wizard later in this procedure.</span></span>

2. <span data-ttu-id="5eb46-118">I handlingsruten velger du Åpne i **Microsoft Office**-knappen, og deretter, under **Eksporter til Excel**, velger du **Stillinger**.</span><span class="sxs-lookup"><span data-stu-id="5eb46-118">On the Action Pane, select the **Open in Microsoft Office** button, and then, under **Export to Excel**, select **Positions**.</span></span> <span data-ttu-id="5eb46-119">Du kan også trykke på Ctrl+T.</span><span class="sxs-lookup"><span data-stu-id="5eb46-119">Alternatively, press Ctrl+T.</span></span>

    ![Eksportere listesiden Stillinger til Excel](media/org-admin.png)

3. <span data-ttu-id="5eb46-121">Lagre Excel-filen som blir eksportert.</span><span class="sxs-lookup"><span data-stu-id="5eb46-121">Save the Excel file that is exported.</span></span>

    ![Eksportere til Excel-dialogboksen](media/export-excel.png)

4. <span data-ttu-id="5eb46-123">I Visio velger du **Visio - Opprett ny** og deretter **Arbeid**-malkategorien.</span><span class="sxs-lookup"><span data-stu-id="5eb46-123">In Visio, select **Visio - Create New**, and select the **Business** template category.</span></span>

    ![Nytt diagram](media/new.png)

5. <span data-ttu-id="5eb46-125">Velg **Veiviser for organisasjonskart**, og velg deretter **Opprett**.</span><span class="sxs-lookup"><span data-stu-id="5eb46-125">Select **Organization Chart Wizard**, and then select **Create**.</span></span>

    ![Dialogboksen Veiviser for organisasjonskart](media/orgchart-wizard.png)

6. <span data-ttu-id="5eb46-127">Velg **Informasjon som allerede er lagret i en fil eller database**, og velg deretter **Neste**.</span><span class="sxs-lookup"><span data-stu-id="5eb46-127">Select **Information that's already stored in a file or database**, and then select **Next**.</span></span>

    ![Veiviser for organisasjonskart 1](media/orgchart-wizard7.png)

7. <span data-ttu-id="5eb46-129">Velg **En tekst-, Org Plus- (\*.txt) eller Excel-fil**, og velg deretter **Neste**.</span><span class="sxs-lookup"><span data-stu-id="5eb46-129">Choose **A text, Org Plus (\*.txt), or Excel file**, and then select **Next**.</span></span>

    ![Veiviser for organisasjonskart 2](media/orgchart-wizard3.png)

8. <span data-ttu-id="5eb46-131">Bla for å velge den eksporterte Excel-filen som inneholder stillingshierarkiet, og velg deretter **Neste**.</span><span class="sxs-lookup"><span data-stu-id="5eb46-131">Browse to select the exported Excel file that contains the position hierarchy, and then select **Next**.</span></span>

    ![Veiviser for organisasjonskart 3](media/orgchart-wizard2.png)

9. <span data-ttu-id="5eb46-133">Angi **Navn**-feltet til **Stilling**, sett feltet **Rapporter til** til **Rapporterer til stilling**, og velg deretter **Neste**.</span><span class="sxs-lookup"><span data-stu-id="5eb46-133">Set the **Name** field to **Position**, set the **Reports to** field to **Reports to position**, and then select **Next**.</span></span>

    ![Veiviser for organisasjonskart 4](media/orgchart-wizard1.png)

10. <span data-ttu-id="5eb46-135">Velg feltene som skal vises på hver node, og velg deretter **Neste**.</span><span class="sxs-lookup"><span data-stu-id="5eb46-135">Select the fields that should be shown on each node, and then select **Next**.</span></span>

    ![Veiviser for organisasjonskart 5](media/orgchart-wizard5.png)

11. <span data-ttu-id="5eb46-137">Legg til **Stilling**-kolonnen i listen **Figurdatafelt**, og velg deretter **Neste**.</span><span class="sxs-lookup"><span data-stu-id="5eb46-137">Add the **Position** column to the **Shape Data fields** list, and then select **Next**.</span></span>

    ![Veiviser for organisasjonskart 6](media/orgchart-wizard6.png)

12. <span data-ttu-id="5eb46-139">Bilder er ikke tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="5eb46-139">Pictures aren't currently available.</span></span> <span data-ttu-id="5eb46-140">På neste side kan du derfor velge **Neste**.</span><span class="sxs-lookup"><span data-stu-id="5eb46-140">Therefore, on the next page, select **Next**.</span></span>
13. <span data-ttu-id="5eb46-141">Velg **Jeg vil at veiviseren skal dele opp organisasjonskartet over flere sider automatisk**.</span><span class="sxs-lookup"><span data-stu-id="5eb46-141">Select **I want the wizard to automatically break my organization chart across pages**.</span></span>

    ![Veiviser for organisasjonskart 7](media/orgchart-wizard4.png)

14. <span data-ttu-id="5eb46-143">Velg **Fullfør**.</span><span class="sxs-lookup"><span data-stu-id="5eb46-143">Select **Finish**.</span></span>

    <span data-ttu-id="5eb46-144">Hvis det finnes stillinger som ikke er inkludert i strukturen, blir du bedt om å inkludere dem i diagrammet.</span><span class="sxs-lookup"><span data-stu-id="5eb46-144">If there are any positions that aren't in the structure, you're asked to include them in the diagram.</span></span>

<span data-ttu-id="5eb46-145">Diagrammet som genereres i Visio, viser hver leder i et eget regneark.</span><span class="sxs-lookup"><span data-stu-id="5eb46-145">The diagram that is generated in Visio shows each manager on a separate worksheet.</span></span>

<span data-ttu-id="5eb46-146">Basert på feltene som du valgte å ta med i diagrammet, viser hver node riktig informasjon når Visio-filen genereres.</span><span class="sxs-lookup"><span data-stu-id="5eb46-146">Based on the fields that you selected to include in the diagram, each node shows the appropriate information when the Visio file is generated.</span></span>

![Hierarkidiagram](media/hierarchy.png)

<span data-ttu-id="5eb46-148">**Tilleggsalternativ**</span><span class="sxs-lookup"><span data-stu-id="5eb46-148">**Additional option**</span></span>

<span data-ttu-id="5eb46-149">I Talent kan du også bruke arbeidsområdet **Personer** til å vise informasjon relatert til hierarkiet.</span><span class="sxs-lookup"><span data-stu-id="5eb46-149">In Talent, you might also be able to use the **People** workspace to view some hierarchy-related information.</span></span>
