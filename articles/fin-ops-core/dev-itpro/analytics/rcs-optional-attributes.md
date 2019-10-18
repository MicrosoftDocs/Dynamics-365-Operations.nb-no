---
title: Importere filer i XML-format med valgfrie attributter
description: Dette emnet inneholder informasjon om utforming av ER-formater som angir XML-attributter for å analysere innkommende elektroniske dokumenter i XML-format.
author: NickSelin
manager: AnnBe
ms.date: 07/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: eb5d721784f45097ab466f75d43256495aac36ca
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182836"
---
# <a name="import-files-in-xml-format-with-optional-attributes"></a><span data-ttu-id="78cd6-103">Importere filer i XML-format med valgfrie attributter</span><span class="sxs-lookup"><span data-stu-id="78cd6-103">Import files in XML format with optional attributes</span></span>

<span data-ttu-id="78cd6-104">Du kan utforme ER-formater (elektronisk rapportering) for å analysere innkommende elektroniske dokumenter i XML-format.</span><span class="sxs-lookup"><span data-stu-id="78cd6-104">You can design Electronic reporting (ER) formats to parse incoming electronic documents in XML format.</span></span> <span data-ttu-id="78cd6-105">Visse attributter i XML-elementer kan angis som valgfrie i et utformet ER-format.</span><span class="sxs-lookup"><span data-stu-id="78cd6-105">Certain attributes of XML elements can be specified in designed ER format as optional.</span></span> <span data-ttu-id="78cd6-106">Dette gjør at du kan håndtere innkommende filer med og uten slike XML-attributter på riktig måte.</span><span class="sxs-lookup"><span data-stu-id="78cd6-106">It will allow you to handle incoming files with and without such XML attributes properly.</span></span> <span data-ttu-id="78cd6-107">Du kan deretter bruke innholdet fra disse filene til å oppdatere programdata.</span><span class="sxs-lookup"><span data-stu-id="78cd6-107">You can then use the content from these files to update application data.</span></span>

<span data-ttu-id="78cd6-108">Hvis du vil ha mer informasjon om denne funksjonen, fullfører du trinnene i emnet [RCS Importere filer i XML-format med valgfrie attributter](tasks/import-files-xml-format-optional-attributes.md), som er en del av forretningsprosessen 7.5.4.3 Acquire/Develop IT service/solution components (10677).</span><span class="sxs-lookup"><span data-stu-id="78cd6-108">To learn more about this feature, complete the steps in the topic, [RCS Import files in XML format with optional attributes](tasks/import-files-xml-format-optional-attributes.md), which is part of the 7.5.4.3 Acquire/Develop IT service/solution components (10677) business process.</span></span> <span data-ttu-id="78cd6-109">Du kan laste ned denne oppgaveveiledningen og de tilknyttede eksempelfilene fra [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).</span><span class="sxs-lookup"><span data-stu-id="78cd6-109">You can download this task guide and associated sample files from the [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).</span></span>


| <span data-ttu-id="78cd6-110">Innholdsbeskrivelse</span><span class="sxs-lookup"><span data-stu-id="78cd6-110">Content description</span></span>       | <span data-ttu-id="78cd6-111">Fil</span><span class="sxs-lookup"><span data-stu-id="78cd6-111">File</span></span>                                                         |
|---------------------------|--------------------------------------------------------------|
| <span data-ttu-id="78cd6-112">Eksempelfil i XML-format</span><span class="sxs-lookup"><span data-stu-id="78cd6-112">Sample file in XML format</span></span> | <span data-ttu-id="78cd6-113">IncomingDocumentToLearnHowToHandleOptionalAttributes.xml</span><span class="sxs-lookup"><span data-stu-id="78cd6-113">IncomingDocumentToLearnHowToHandleOptionalAttributes.xml</span></span>     |
| <span data-ttu-id="78cd6-114">Oppgaveveiledning</span><span class="sxs-lookup"><span data-stu-id="78cd6-114">Task guide</span></span>                | <span data-ttu-id="78cd6-115">RCS Import files in XML format with optional attributes.axtr</span><span class="sxs-lookup"><span data-stu-id="78cd6-115">RCS Import files in XML format with optional attributes.axtr</span></span> |


<span data-ttu-id="78cd6-116">Fremgangsmåten nedenfor forklarer hvordan en bruker i rollen Systemansvarlig eller Utvikler av elektronisk rapportering kan utforme en ER-formatkonfigurasjon for å importere filer i XML-format som inneholder valgfrie attributter.</span><span class="sxs-lookup"><span data-stu-id="78cd6-116">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can design ER format configuration to import files in XML format containing optional attributes.</span></span> <span data-ttu-id="78cd6-117">For å fullføre disse trinnene må du først fullføre trinnene i fremgangsmåten [Opprette en konfigurasjonsleverandør og merke den som aktiv](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="78cd6-117">To complete these steps, you must first complete the steps in the procedure, [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span> <span data-ttu-id="78cd6-118">Før du begynner, laster du ned filen IncomingDocumentToLearnHowToHandleOptionalAttributes.xml fra Microsoft Download Center (https://go.microsoft.com/fwlink/?linkid=874684 ) og lagrer den lokalt.</span><span class="sxs-lookup"><span data-stu-id="78cd6-118">Before you begin, download and save locally the IncomingDocumentToLearnHowToHandleOptionalAttributes.xml file from Microsoft Download Center (https://go.microsoft.com/fwlink/?linkid=874684 ).</span></span>

1. <span data-ttu-id="78cd6-119">Gå til **Organisasjonsstyring** > **Arbeidsområder** > **Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="78cd6-119">Go to **Organization administration** > **Workspaces** > **Electronic reporting**.</span></span>
2. <span data-ttu-id="78cd6-120">Kontroller at konfigurasjonsleverandøren for eksempelfirmaet Litware, Inc. er tilgjengelig og merket som **Aktiv**.</span><span class="sxs-lookup"><span data-stu-id="78cd6-120">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="78cd6-121">Hvis du ikke ser denne konfigurasjonsleverandøren, må du fullføre trinnene i emnet [Opprette en konfigurasjonsleverandør og merke den som aktiv](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="78cd6-121">If you don’t see this configuration provider, complete the steps in the topic, [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>
3. <span data-ttu-id="78cd6-122">Klikk på **Rapporteringskonfigurasjoner**.</span><span class="sxs-lookup"><span data-stu-id="78cd6-122">Click **Reporting configurations**.</span></span>

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="78cd6-123">Opprett en ny datamodellkonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="78cd6-123">Create a new data model configuration</span></span>
1. <span data-ttu-id="78cd6-124">Klikk på **Opprett konfigurasjon** for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="78cd6-124">Click **Create configuration** to open the drop dialog.</span></span>
2. <span data-ttu-id="78cd6-125">Skriv inn «Modell for å importere XML-fil» i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="78cd6-125">In the **Name** field, type 'Model to import xml file'.</span></span>
3. <span data-ttu-id="78cd6-126">Klikk **Opprett konfigurasjon**.</span><span class="sxs-lookup"><span data-stu-id="78cd6-126">Click **Create configuration**.</span></span>
4. <span data-ttu-id="78cd6-127">Klikk **Utforming**.</span><span class="sxs-lookup"><span data-stu-id="78cd6-127">Click **Designer**.</span></span>
5. <span data-ttu-id="78cd6-128">Klikk på **Ny** for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="78cd6-128">Click **New** to open the drop dialog.</span></span>
6. <span data-ttu-id="78cd6-129">Skriv inn «Rot» i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="78cd6-129">In the **Name** field, type 'Root'.</span></span>
7. <span data-ttu-id="78cd6-130">Klikk **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="78cd6-130">Click **Add**.</span></span>
8. <span data-ttu-id="78cd6-131">Klikk på **Ny** for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="78cd6-131">Click **New** to open the drop dialog.</span></span>
9. <span data-ttu-id="78cd6-132">Skriv inn «Liste» i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="78cd6-132">In the **Name** field, type 'List'.</span></span>
10. <span data-ttu-id="78cd6-133">Velg **Postliste** i **Varetype**-feltet.</span><span class="sxs-lookup"><span data-stu-id="78cd6-133">In the **Item type** field, select **Record list**.</span></span>
11. <span data-ttu-id="78cd6-134">Klikk **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="78cd6-134">Click **Add**.</span></span>
12. <span data-ttu-id="78cd6-135">Klikk på **Ny** for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="78cd6-135">Click **New** to open the drop dialog.</span></span>
13. <span data-ttu-id="78cd6-136">I **Navn**-feltet skriver du inn «Kode».</span><span class="sxs-lookup"><span data-stu-id="78cd6-136">In the **Name** field, type 'Code'.</span></span>
14. <span data-ttu-id="78cd6-137">Velg **Streng** i **Varetype**-feltet.</span><span class="sxs-lookup"><span data-stu-id="78cd6-137">In the **Item type** field, select **String**.</span></span>
15. <span data-ttu-id="78cd6-138">Klikk **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="78cd6-138">Click **Add**.</span></span>
16. <span data-ttu-id="78cd6-139">Klikk **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="78cd6-139">Click **Save**.</span></span>
17. <span data-ttu-id="78cd6-140">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="78cd6-140">Close the page.</span></span>
18. <span data-ttu-id="78cd6-141">Klikk på **Endre status**.</span><span class="sxs-lookup"><span data-stu-id="78cd6-141">Click **Change status**.</span></span>
19. <span data-ttu-id="78cd6-142">Klikk på **Fullført**.</span><span class="sxs-lookup"><span data-stu-id="78cd6-142">Click **Complete**.</span></span>
20. <span data-ttu-id="78cd6-143">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="78cd6-143">Click **OK**.</span></span>

## <a name="create-a-format-for-data-import"></a><span data-ttu-id="78cd6-144">Opprette et format for dataimport</span><span class="sxs-lookup"><span data-stu-id="78cd6-144">Create a format for data import</span></span>
1. <span data-ttu-id="78cd6-145">Klikk på **Opprett konfigurasjon** for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="78cd6-145">Click **Create configuration** to open the drop dialog.</span></span>
2. <span data-ttu-id="78cd6-146">I **Ny**-feltet angir du «Format basert på datamodellen Modell for å importere XML-fil».</span><span class="sxs-lookup"><span data-stu-id="78cd6-146">In the **New** field, enter 'Format based on data model Model to import xml file'.</span></span>
3. <span data-ttu-id="78cd6-147">Skriv inn «Format for å importere XML-fil» i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="78cd6-147">In the **Nam**e field, type 'Format to import xml file'.</span></span> 
4. <span data-ttu-id="78cd6-148">Velg **Ja** i feltet **Støtter dataimport**.</span><span class="sxs-lookup"><span data-stu-id="78cd6-148">Select **Yes** in the **Supports data import** field.</span></span>
5. <span data-ttu-id="78cd6-149">Klikk **Opprett konfigurasjon**.</span><span class="sxs-lookup"><span data-stu-id="78cd6-149">Click **Create configuration**.</span></span>

## <a name="design-a-format-to-parse-incoming-file-in-xml-format"></a><span data-ttu-id="78cd6-150">Utforme et format for å analysere innkommende fil i XML-format</span><span class="sxs-lookup"><span data-stu-id="78cd6-150">Design a format to parse incoming file in xml format</span></span>
1. <span data-ttu-id="78cd6-151">Klikk **Utforming**.</span><span class="sxs-lookup"><span data-stu-id="78cd6-151">Click **Designer**.</span></span>
2. <span data-ttu-id="78cd6-152">Klikk på **Legg til rot** for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="78cd6-152">Click **Add root** to open the drop dialog.</span></span>
3. <span data-ttu-id="78cd6-153">Velg **XML\Element** i treet.</span><span class="sxs-lookup"><span data-stu-id="78cd6-153">In the tree, select **XML\Element**.</span></span>
4. <span data-ttu-id="78cd6-154">Skriv inn «rot» i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="78cd6-154">In the **Name** field, type 'root'.</span></span>
5. <span data-ttu-id="78cd6-155">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="78cd6-155">Click **OK**.</span></span>
6. <span data-ttu-id="78cd6-156">Klikk på **Legg til** for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="78cd6-156">Click **Add** to open the drop dialog.</span></span>
7. <span data-ttu-id="78cd6-157">Velg **XML\Element** i treet.</span><span class="sxs-lookup"><span data-stu-id="78cd6-157">In the tree, select **XML\Element**.</span></span>
8. <span data-ttu-id="78cd6-158">I **Navn**-feltet skriver du inn «dokument».</span><span class="sxs-lookup"><span data-stu-id="78cd6-158">In the **Name** field, type 'document'.</span></span>
9. <span data-ttu-id="78cd6-159">Velg **Én mange** i feltet **Multiplisitet**.</span><span class="sxs-lookup"><span data-stu-id="78cd6-159">In the **Multiplicity** field, select **One many**.</span></span>
10. <span data-ttu-id="78cd6-160">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="78cd6-160">Click **OK**.</span></span>
11. <span data-ttu-id="78cd6-161">Velg **rot\dokument** i treet.</span><span class="sxs-lookup"><span data-stu-id="78cd6-161">In the tree, select **root\document**.</span></span>
12. <span data-ttu-id="78cd6-162">Klikk på **Legg til** for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="78cd6-162">Click **Add** to open the drop dialog.</span></span>
13. <span data-ttu-id="78cd6-163">Velg **XML\Attributt** i treet.</span><span class="sxs-lookup"><span data-stu-id="78cd6-163">In the tree, select **XML\Attribute**.</span></span>
14. <span data-ttu-id="78cd6-164">I **Navn**-feltet skriver du inn «id».</span><span class="sxs-lookup"><span data-stu-id="78cd6-164">In the **Name** field, type 'id'.</span></span>
15. <span data-ttu-id="78cd6-165">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="78cd6-165">Click **OK**.</span></span>
16. <span data-ttu-id="78cd6-166">Klikk **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="78cd6-166">Click **Save**.</span></span>

## <a name="design-a-format-mapping-to-save-parsed-information-to-data-model"></a><span data-ttu-id="78cd6-167">Utforme en formattilordning for å lagre analysert informasjon i datamodell</span><span class="sxs-lookup"><span data-stu-id="78cd6-167">Design a format mapping to save parsed information to data model</span></span>
1.  <span data-ttu-id="78cd6-168">Klikk på **Tilordne format til modell**.</span><span class="sxs-lookup"><span data-stu-id="78cd6-168">Click **Map format to model**.</span></span>
2.  <span data-ttu-id="78cd6-169">Klikk på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="78cd6-169">Click **New**.</span></span>
3.  <span data-ttu-id="78cd6-170">Angi eller velg en verdi i feltet **Definisjon**.</span><span class="sxs-lookup"><span data-stu-id="78cd6-170">In the **Definition** field, enter or select a value.</span></span>
4.  <span data-ttu-id="78cd6-171">I **Navn**-feltet skriver du inn «Tilordning».</span><span class="sxs-lookup"><span data-stu-id="78cd6-171">In the **Name** field, type 'Mapping'.</span></span>
5.  <span data-ttu-id="78cd6-172">Klikk **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="78cd6-172">Click **Save**.</span></span>
6.  <span data-ttu-id="78cd6-173">Klikk **Utforming**.</span><span class="sxs-lookup"><span data-stu-id="78cd6-173">Click **Designer**.</span></span>
7.  <span data-ttu-id="78cd6-174">Utvid **format** i treet.</span><span class="sxs-lookup"><span data-stu-id="78cd6-174">In the tree, expand **format**.</span></span>
8.  <span data-ttu-id="78cd6-175">I treet utvider du **format\rot: XML-element(rot)**.</span><span class="sxs-lookup"><span data-stu-id="78cd6-175">In the tree, expand **format\root: XML Element(root)**.</span></span>
9.  <span data-ttu-id="78cd6-176">I treet velger du \**format\root: XML-element(rot)\dokument: XML-element 1..*</span><span class="sxs-lookup"><span data-stu-id="78cd6-176">In the tree, select \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="78cd6-177">(dokument)\*\*.</span><span class="sxs-lookup"><span data-stu-id="78cd6-177">(document)\*\*.</span></span>
10. <span data-ttu-id="78cd6-178">Klikk på **Bind**.</span><span class="sxs-lookup"><span data-stu-id="78cd6-178">Click **Bind**.</span></span>
11. <span data-ttu-id="78cd6-179">I treet utvider du \**format\rot: XML-element(rot)\dokument: XML-element 1..*</span><span class="sxs-lookup"><span data-stu-id="78cd6-179">In the tree, expand \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="78cd6-180">(dokument)\*\*.</span><span class="sxs-lookup"><span data-stu-id="78cd6-180">(document)\*\*.</span></span>
12. <span data-ttu-id="78cd6-181">I treet velger du \**format\root: XML-element(rot)\dokument: XML-element 1..*</span><span class="sxs-lookup"><span data-stu-id="78cd6-181">In the tree, select \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="78cd6-182">(dokument)\id\*\*.</span><span class="sxs-lookup"><span data-stu-id="78cd6-182">(document)\id\*\*.</span></span>
13. <span data-ttu-id="78cd6-183">I treet utvider du **Liste = format.rot.dokument**.</span><span class="sxs-lookup"><span data-stu-id="78cd6-183">In the tree, expand **List = format.root.document**.</span></span>
14. <span data-ttu-id="78cd6-184">I treet velger du **Liste = format.rot.dokument\Kode**.</span><span class="sxs-lookup"><span data-stu-id="78cd6-184">In the tree, select **List = format.root.document\Code**.</span></span>
15. <span data-ttu-id="78cd6-185">Klikk på **Bind**.</span><span class="sxs-lookup"><span data-stu-id="78cd6-185">Click **Bind**.</span></span>
16. <span data-ttu-id="78cd6-186">Klikk **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="78cd6-186">Click **Save**.</span></span>
17. <span data-ttu-id="78cd6-187">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="78cd6-187">Close the page.</span></span>

## <a name="run-format-mapping"></a><span data-ttu-id="78cd6-188">Kjøre formattilordning</span><span class="sxs-lookup"><span data-stu-id="78cd6-188">Run format mapping</span></span>
1. <span data-ttu-id="78cd6-189">Klikk på **Kjør**.</span><span class="sxs-lookup"><span data-stu-id="78cd6-189">Click **Run**.</span></span>
2. <span data-ttu-id="78cd6-190">Klikk på **Bla gjennom**, og velg filen **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span><span class="sxs-lookup"><span data-stu-id="78cd6-190">Click **Browse** and select the file, **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span></span>
3. <span data-ttu-id="78cd6-191">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="78cd6-191">Click **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="78cd6-192">Den valgte filen er ikke importert, siden formatutformingen forutsetter at et «id»-attributt finnes for «dokument»-elementet, men den importerte filen inneholder ikke noe slikt attributt.</span><span class="sxs-lookup"><span data-stu-id="78cd6-192">The selected file has not been imported as the format design assumes the existence of ‘id’ attribute for the ‘document’ element, but the imported file contains no such attribute.</span></span>

## <a name="modify-format-structure-to-handle-xml-attribute-as-optional"></a><span data-ttu-id="78cd6-193">Endre formatstrukturen for å håndtere XML-attributter som valgfrie</span><span class="sxs-lookup"><span data-stu-id="78cd6-193">Modify format structure to handle xml attribute as optional</span></span>
1. <span data-ttu-id="78cd6-194">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="78cd6-194">Close the page.</span></span>
2. <span data-ttu-id="78cd6-195">Utvid **rot\dokument** i treet.</span><span class="sxs-lookup"><span data-stu-id="78cd6-195">In the tree, expand **root\document**.</span></span>
3. <span data-ttu-id="78cd6-196">Velg **rot\dokument\id** i treet.</span><span class="sxs-lookup"><span data-stu-id="78cd6-196">In the tree, select **root\document\id**.</span></span>
4. <span data-ttu-id="78cd6-197">Velg **Ja** i feltet **Tom streng for manglende attributt**.</span><span class="sxs-lookup"><span data-stu-id="78cd6-197">In the **Empty string for missing attribute** field, select **Yes**.</span></span>
5. <span data-ttu-id="78cd6-198">Klikk **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="78cd6-198">Click **Save**.</span></span>

## <a name="run-format-mapping-to-test-changes"></a><span data-ttu-id="78cd6-199">Kjøre formattilordning for å teste endringer</span><span class="sxs-lookup"><span data-stu-id="78cd6-199">Run format mapping to test changes</span></span>
1. <span data-ttu-id="78cd6-200">Klikk på **Tilordne format til modell**.</span><span class="sxs-lookup"><span data-stu-id="78cd6-200">Click **Map format to model**.</span></span>
2. <span data-ttu-id="78cd6-201">Klikk på **Kjør**.</span><span class="sxs-lookup"><span data-stu-id="78cd6-201">Click **Run**.</span></span>
3. <span data-ttu-id="78cd6-202">Klikk på **Bla gjennom**, og velg filen **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span><span class="sxs-lookup"><span data-stu-id="78cd6-202">Click **Browse** and select the file, **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span></span>
4. <span data-ttu-id="78cd6-203">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="78cd6-203">Click **OK**.</span></span>
5. <span data-ttu-id="78cd6-204">Se gjennom den genererte filen.</span><span class="sxs-lookup"><span data-stu-id="78cd6-204">Review the generated file.</span></span> <span data-ttu-id="78cd6-205">Vær oppmerksom på at samme fil har blitt importert, siden formatutformingen nå regner «id»-attributtet for «dokument»-elementet for å være valgfritt.</span><span class="sxs-lookup"><span data-stu-id="78cd6-205">Note that same file has been imported as the format design now consider the ‘id’ attribute for the ‘document’ element as optional.</span></span>
