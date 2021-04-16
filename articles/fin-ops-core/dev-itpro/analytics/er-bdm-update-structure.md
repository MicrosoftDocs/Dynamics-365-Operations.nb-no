---
title: Oppdatere strukturen til en forretningsdokumentmal
description: Dette emnet forklarer hvordan du oppdaterer strukturen til en forretningsdokumentmal ved hjelp av funksjonen for administrasjon av forretningsdokument.
author: NickSelin
ms.date: 11/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters, ERBDTemplateEditor
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-12-01
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 203c9f0990051c1618660959dad0e184add68ffa
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750490"
---
# <a name="update-the-structure-of-a-business-document-template"></a><span data-ttu-id="96fee-103">Oppdatere strukturen til en forretningsdokumentmal</span><span class="sxs-lookup"><span data-stu-id="96fee-103">Update the structure of a business document template</span></span> 

[!include[banner](../includes/banner.md)]

<span data-ttu-id="96fee-104">I **Malstruktur**-ruten i malredigeringsprogrammet [Administrasjon av forretningsdokument](er-business-document-management.md) kan du endre en forretningsdokumentmal ved å [legge til nye felter](er-bdm-add-field-to-excel-template.md) i en mal i Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="96fee-104">In the **Template structure** pane of the [Business document management](er-business-document-management.md) template editor, you can modify a business document template by [adding new fields](er-bdm-add-field-to-excel-template.md) to a template in Microsoft Excel.</span></span> <span data-ttu-id="96fee-105">Strukturen til malen oppdateres deretter automatisk i Dynamics 365 Finance, slik at den gjenspeiler endringene du har gjort i **Malstruktur**-ruten.</span><span class="sxs-lookup"><span data-stu-id="96fee-105">The structure of the template is then automatically updated in Dynamics 365 Finance, so that it reflects the changes that you made in the **Template structure** pane.</span></span>

<span data-ttu-id="96fee-106">Du kan også endre en mal ved hjelp av nettbasert funksjonalitet i Office 365.</span><span class="sxs-lookup"><span data-stu-id="96fee-106">You can also modify a template by using Office 365 online functionality.</span></span> <span data-ttu-id="96fee-107">Du kan for eksempel legge til et nytt navngitt element, for eksempel et bilde eller en figur, i det redigerbare regnearket.</span><span class="sxs-lookup"><span data-stu-id="96fee-107">For example, you can add a new named item, such as a picture or shape, to the editable worksheet.</span></span> <span data-ttu-id="96fee-108">I dette tilfellet oppdateres ikke strukturen til malen i Finance automatisk, og elementet du la til, vises ikke i **Malstruktur**-ruten.</span><span class="sxs-lookup"><span data-stu-id="96fee-108">In this case, the structure of the template isn't automatically updated in Finance, and the item that you added doesn't appear in the **Template structure** pane.</span></span> <span data-ttu-id="96fee-109">Oppdatere malstrukturen manuelt i Finance ved å velge **Oppdater struktur** på siden for malredigering.</span><span class="sxs-lookup"><span data-stu-id="96fee-109">Manually update the template structure in Finance by selecting **Update structure** on the template editor page.</span></span>

<span data-ttu-id="96fee-110">Hvis du vil ha mer informasjon om denne funksjonen, kan du fullføre eksemplet nedenfor.</span><span class="sxs-lookup"><span data-stu-id="96fee-110">For more information about this feature, complete the following example.</span></span>

## <a name="example-update-the-structure-of-a-business-document-template"></a><span data-ttu-id="96fee-111">Eksempel: oppdatere strukturen til en forretningsdokumentmal</span><span class="sxs-lookup"><span data-stu-id="96fee-111">Example: Update the structure of a business document template</span></span>

<span data-ttu-id="96fee-112">Dette eksemplet viser hvordan en systemadministrator kan oppdatere strukturen til en forretningsdokumentmal i Finance etter at malen er endret i Office Online.</span><span class="sxs-lookup"><span data-stu-id="96fee-112">This example shows how a system administrator can update the structure of a business document template in Finance after the template is modified in Office Online.</span></span> <span data-ttu-id="96fee-113">Delene nedenfor forklarer hvilke trinn som er involvert.</span><span class="sxs-lookup"><span data-stu-id="96fee-113">The following sections explain the steps that are involved.</span></span>

### <a name="prepare-a-business-document-template-for-editing"></a><span data-ttu-id="96fee-114">Klargjøre en forretningsdokumentmal for redigering</span><span class="sxs-lookup"><span data-stu-id="96fee-114">Prepare a business document template for editing</span></span>

<span data-ttu-id="96fee-115">Fullfør følgende prosedyrer i [Oversikt over administrasjon av forretningsdokument](er-business-document-management.md).</span><span class="sxs-lookup"><span data-stu-id="96fee-115">Complete the following procedures in [Business document management overview](er-business-document-management.md).</span></span>

1. [<span data-ttu-id="96fee-116">Konfigurere ER-parametere</span><span class="sxs-lookup"><span data-stu-id="96fee-116">Configure ER parameters</span></span>](er-business-document-management.md#configure-er-parameters)
2. [<span data-ttu-id="96fee-117">Importere ER-løsninger</span><span class="sxs-lookup"><span data-stu-id="96fee-117">Import ER solutions</span></span>](er-business-document-management.md#import-er-solutions)
3. [<span data-ttu-id="96fee-118">Aktivere administrasjon av forretningsdokument</span><span class="sxs-lookup"><span data-stu-id="96fee-118">Enable Business document management</span></span>](er-business-document-management.md#enable-business-document-management)
4. [<span data-ttu-id="96fee-119">Konfigurere parametere</span><span class="sxs-lookup"><span data-stu-id="96fee-119">Configure parameters</span></span>](er-business-document-management.md#configure-parameters)

### <a name="edit-a-business-document-template"></a><span data-ttu-id="96fee-120">Redigere en forretningsdokumentmal</span><span class="sxs-lookup"><span data-stu-id="96fee-120">Edit a business document template</span></span>

1. <span data-ttu-id="96fee-121">I **Forretningsdokumentadministrering**-arbeidsområdet velger du **Nytt dokument**.</span><span class="sxs-lookup"><span data-stu-id="96fee-121">In the **Business document management** workspace, select **New document**.</span></span>
2. <span data-ttu-id="96fee-122">På siden **Opprett en ny mal** velger du malen **Fritekstfaktura (ER-eksempel) (Excel)**.</span><span class="sxs-lookup"><span data-stu-id="96fee-122">On the **Create a new template** page, select the **Free text invoice (ER sample)(Excel)** template.</span></span>
3. <span data-ttu-id="96fee-123">Velg **Opprett dokument**.</span><span class="sxs-lookup"><span data-stu-id="96fee-123">Select **Create document**.</span></span>
4. <span data-ttu-id="96fee-124">I **Tittel**-feltet skriver du inn **Eksempel på fritekstfaktura for Litware**.</span><span class="sxs-lookup"><span data-stu-id="96fee-124">In the **Title** field, enter **FTI sample Litware**.</span></span>
5. <span data-ttu-id="96fee-125">Velg **OK** for å opprette den nye malen.</span><span class="sxs-lookup"><span data-stu-id="96fee-125">Select **OK** to create the new template.</span></span>

    > [!NOTE]
    > <span data-ttu-id="96fee-126">Hvis du ennå ikke har logget på Office Online, blir du [ledet til påloggingssiden for Office 365](er-business-document-management.md#frequently-asked-questions).</span><span class="sxs-lookup"><span data-stu-id="96fee-126">If you haven't yet signed in to Office Online, you're [directed to the Office 365 sign-in page](er-business-document-management.md#frequently-asked-questions).</span></span> <span data-ttu-id="96fee-127">Du kan gå tilbake til Finance-miljøet ved å velge **Tilbake**-knappen i nettleseren.</span><span class="sxs-lookup"><span data-stu-id="96fee-127">To return to your Finance environment, select the **Back** button in your browser.</span></span>

    <span data-ttu-id="96fee-128">Den nye malen åpnes for redigering i den innebygde kontrollen for Excel Online på siden for malredigering.</span><span class="sxs-lookup"><span data-stu-id="96fee-128">The new template is opened for editing in the Excel Online embedded control on the template editor page.</span></span>

<span data-ttu-id="96fee-129">[![Bruke arbeidsområdet for administrasjon av forretningsdokument til å begynne å redigere en forretningsdokumentmal](./media/er-bdm-update-structure1.gif)](./media/er-bdm-update-structure1.gif)</span><span class="sxs-lookup"><span data-stu-id="96fee-129">[![Using the Business document management workspace to start to edit a business document template](./media/er-bdm-update-structure1.gif)](./media/er-bdm-update-structure1.gif)</span></span>

### <a name="review-the-current-structure-of-the-editable-template"></a><span data-ttu-id="96fee-130">Se gjennom gjeldende struktur for den redigerbare malen</span><span class="sxs-lookup"><span data-stu-id="96fee-130">Review the current structure of the editable template</span></span>

1. <span data-ttu-id="96fee-131">Velg **Støttelinjer** i **Vis**-gruppen i **Visning**-fanen på båndet i Excel Online.</span><span class="sxs-lookup"><span data-stu-id="96fee-131">In Excel Online, on the ribbon, on the **View** tab, in the **Show** group, select **Gridlines**.</span></span>
2. <span data-ttu-id="96fee-132">I den redigerbare malen velger du rektanglet ovenfor maltittelen.</span><span class="sxs-lookup"><span data-stu-id="96fee-132">In the editable template, select the rectangle above the template title.</span></span> <span data-ttu-id="96fee-133">Dette rektanglet er et bilde kalt **rptHeaderCompLogo**.</span><span class="sxs-lookup"><span data-stu-id="96fee-133">This rectangle is a picture that is named **rptHeaderCompLogo**.</span></span>
3. <span data-ttu-id="96fee-134">Hvis **Malstruktur**-ruten er skjult, velger du **Vis struktur**.</span><span class="sxs-lookup"><span data-stu-id="96fee-134">If the **Template structure** pane is hidden, select **Show structure**.</span></span>
4. <span data-ttu-id="96fee-135">Utvid **Rapport \> Faktura \> rptHeader \> rptHeaderPart1** i **Malstruktur**-ruten.</span><span class="sxs-lookup"><span data-stu-id="96fee-135">In the **Template structure** pane, expand **Report \> Invoice \> rptHeader \> rptHeaderPart1**.</span></span>
5. <span data-ttu-id="96fee-136">Legg merke til at elementet **rptHeaderCompLogo** vises som et underordnet element for **Rapport \> Faktura \> rptHeader \> rptHeaderPart1** i malstrukturen i Finance.</span><span class="sxs-lookup"><span data-stu-id="96fee-136">Notice that, in the template structure in Finance, the **rptHeaderCompLogo** item is presented as a child item of **Report \> Invoice \> rptHeader \> rptHeaderPart1**.</span></span>

<span data-ttu-id="96fee-137">[![Bruke arbeidsområdet for administrasjon av forretningsdokument til å se gjennom gjeldende struktur for en redigerbar mal](./media/er-bdm-update-structure2.gif)](./media/er-bdm-update-structure2.gif)</span><span class="sxs-lookup"><span data-stu-id="96fee-137">[![Using the Business document management workspace to review the current structure of an editable template](./media/er-bdm-update-structure2.gif)](./media/er-bdm-update-structure2.gif)</span></span>

### <a name="update-the-structure-of-a-business-document-template-by-deleting-a-picture"></a><span data-ttu-id="96fee-138">Oppdatere strukturen til en forretningsdokumentmal ved å slette et bilde</span><span class="sxs-lookup"><span data-stu-id="96fee-138">Update the structure of a business document template by deleting a picture</span></span>

1. <span data-ttu-id="96fee-139">Velg bildet **rptHeaderCompLogo** i den redigerbare malen i Excel Online.</span><span class="sxs-lookup"><span data-stu-id="96fee-139">In Excel Online, in the editable template, select the **rptHeaderCompLogo** picture.</span></span>
2. <span data-ttu-id="96fee-140">Følg ett av disse trinnene for å slette det valgte bildet fra den redigerbare malen:</span><span class="sxs-lookup"><span data-stu-id="96fee-140">Follow one of these steps to delete the selected picture from the editable template:</span></span>

    - <span data-ttu-id="96fee-141">Trykk på **Delete** på tastaturet.</span><span class="sxs-lookup"><span data-stu-id="96fee-141">Select the **Delete** key on your keyboard.</span></span>
    - <span data-ttu-id="96fee-142">Velg og hold (eller høyreklikk på) bildet, og velg deretter **Klipp ut**.</span><span class="sxs-lookup"><span data-stu-id="96fee-142">Select and hold (or right-click) the picture, and then select **Cut**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="96fee-143">Elementet **rptHeaderCompLogo** er fortsatt i malstrukturen i Finance, selv om bildet ikke lenger er inkludert i Excel-malen.</span><span class="sxs-lookup"><span data-stu-id="96fee-143">The **rptHeaderCompLogo** item is currently still present in the template structure in Finance, even though the picture is no longer included in the Excel template.</span></span>

3. <span data-ttu-id="96fee-144">Velg **Oppdater struktur** for å synkronisere strukturen til den redigerbare malen i Excel og Finance.</span><span class="sxs-lookup"><span data-stu-id="96fee-144">Select **Update structure** to sync the structure of the editable template in Excel and Finance.</span></span>
4. <span data-ttu-id="96fee-145">Utvid **Rapport \> Faktura \> rptHeader \> rptHeaderPart1** i **Malstruktur**-ruten.</span><span class="sxs-lookup"><span data-stu-id="96fee-145">In the **Template structure** pane, expand **Report \> Invoice \> rptHeader \> rptHeaderPart1**.</span></span>
5. <span data-ttu-id="96fee-146">Legg merke til at elementet **rptHeaderCompLogo** ikke lenger er inkludert i malstrukturen i Finance.</span><span class="sxs-lookup"><span data-stu-id="96fee-146">Notice that the **rptHeaderCompLogo** item is no longer included in the template structure in Finance.</span></span>

<span data-ttu-id="96fee-147">[![Bruke arbeidsområdet for administrasjon av forretningsdokument til å slette et bilde fra en forretningsdokumentmal](./media/er-bdm-update-structure3.gif)](./media/er-bdm-update-structure3.gif)</span><span class="sxs-lookup"><span data-stu-id="96fee-147">[![Using the Business document management workspace to delete a picture from a business document template](./media/er-bdm-update-structure3.gif)](./media/er-bdm-update-structure3.gif)</span></span>

### <a name="update-the-structure-of-a-business-document-template-by-adding-a-picture"></a><span data-ttu-id="96fee-148">Oppdatere strukturen til en forretningsdokumentmal ved å legge til et bilde</span><span class="sxs-lookup"><span data-stu-id="96fee-148">Update the structure of a business document template by adding a picture</span></span>

1. <span data-ttu-id="96fee-149">Velg **Bilde** i **Illustrasjoner**-gruppen i **Sett inn**-fanen på båndet i Excel Online.</span><span class="sxs-lookup"><span data-stu-id="96fee-149">In Excel Online, on the ribbon, on the **Insert** tab, in the **Illustrations** group, select **Picture**.</span></span>
2. <span data-ttu-id="96fee-150">Velg **Velg fil**, bla frem til bildet du vil legge til, velg det, og velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="96fee-150">Select **Choose file**, browse to the image that you want to add, select it, and then select **OK**.</span></span>
3. <span data-ttu-id="96fee-151">Velg **Sett inn**.</span><span class="sxs-lookup"><span data-stu-id="96fee-151">Select **Insert**.</span></span>
4. <span data-ttu-id="96fee-152">Flytt det nye bildet til det er på riktig sted.</span><span class="sxs-lookup"><span data-stu-id="96fee-152">Move the new picture until it's in the correct place.</span></span> <span data-ttu-id="96fee-153">Bildet får som standard et navn i Excel.</span><span class="sxs-lookup"><span data-stu-id="96fee-153">By default, Excel names the picture.</span></span> <span data-ttu-id="96fee-154">Bildet kan for eksempel få navnet **Bilde 2**.</span><span class="sxs-lookup"><span data-stu-id="96fee-154">For example, it might name the picture **Picture 2**.</span></span>
5. <span data-ttu-id="96fee-155">Velg **Oppdater struktur** for å synkronisere strukturen til den redigerbare malen i Excel og Finance.</span><span class="sxs-lookup"><span data-stu-id="96fee-155">Select **Update structure** to sync the structure of the editable template in Excel and Finance.</span></span>
6. <span data-ttu-id="96fee-156">Utvid **Rapport \> Faktura \> rptHeader \> rptHeaderPart1** i **Malstruktur**-ruten.</span><span class="sxs-lookup"><span data-stu-id="96fee-156">In the **Template structure** pane, expand **Report \> Invoice \> rptHeader \> rptHeaderPart1**.</span></span>
7. <span data-ttu-id="96fee-157">Legg merke til at det nye bildet nå er inkludert som et element i malstrukturen i Finance.</span><span class="sxs-lookup"><span data-stu-id="96fee-157">Notice that the new picture is now included as an item in the template structure in Finance.</span></span>

<span data-ttu-id="96fee-158">[![Bruke arbeidsområdet for administrasjon av forretningsdokument til å legge til et bilde i en forretningsdokumentmal](./media/er-bdm-update-structure4.gif)](./media/er-bdm-update-structure4.gif)</span><span class="sxs-lookup"><span data-stu-id="96fee-158">[![Using the Business document management workspace to add a picture to a business document template](./media/er-bdm-update-structure4.gif)](./media/er-bdm-update-structure4.gif)</span></span>

## <a name="related-links"></a><span data-ttu-id="96fee-159">Relaterte koblinger</span><span class="sxs-lookup"><span data-stu-id="96fee-159">Related links</span></span>

[<span data-ttu-id="96fee-160">Oversikt over elektronisk rapportering (ER)</span><span class="sxs-lookup"><span data-stu-id="96fee-160">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="96fee-161">Oversikt over administrasjon av forretningsdokument</span><span class="sxs-lookup"><span data-stu-id="96fee-161">Business document management overview</span></span>](er-business-document-management.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]