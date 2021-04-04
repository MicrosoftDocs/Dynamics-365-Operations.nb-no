---
title: (RCS) Importere filer i XML-format med valgfrie attributter
description: Dette emnet inneholder informasjon om hvordan en bruker kan utforme ER-formatkonfigurasjon for å importere filer i XML-format som inneholder valgfrie attributter.
author: NickSelin
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-07-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ef090270b2e521b870697bb238b50ea92d4f6958
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565692"
---
# <a name="rcs-import-files-in-xml-format-with-optional-attributes"></a><span data-ttu-id="b31c2-103">(RCS) Importere filer i XML-format med valgfrie attributter</span><span class="sxs-lookup"><span data-stu-id="b31c2-103">(RCS) Import files in XML format with optional attributes</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b31c2-104">Fremgangsmåten nedenfor forklarer hvordan en bruker i rollen Systemansvarlig eller Utvikler av elektronisk rapportering kan utforme en ER-formatkonfigurasjon for å importere filer i XML-format som inneholder valgfrie attributter.</span><span class="sxs-lookup"><span data-stu-id="b31c2-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can design ER format configuration to import files in XML format containing optional attributes.</span></span> <span data-ttu-id="b31c2-105">For å fullføre disse trinnene må du først fullføre trinnene i fremgangsmåten "Opprette en konfigurasjonsleverandør og merke den som aktiv".</span><span class="sxs-lookup"><span data-stu-id="b31c2-105">To complete these steps, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span> <span data-ttu-id="b31c2-106">Før du begynner, laster du ned filen IncomingDocumentToLearnHowToHandleOptionalAttributes.xml fra [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684) og lagrer den lokalt.</span><span class="sxs-lookup"><span data-stu-id="b31c2-106">Before you begin, download and save locally the IncomingDocumentToLearnHowToHandleOptionalAttributes.xml file from [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).</span></span>

1.    <span data-ttu-id="b31c2-107">Gå til **Alle arbeidsområder** > **Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="b31c2-107">Go to **All workspaces** > **Electronic reporting**.</span></span>
2.    <span data-ttu-id="b31c2-108">Kontroller at konfigurasjonsleverandøren for eksempelfirmaet Litware, Inc. er tilgjengelig og merket som **Aktiv**.</span><span class="sxs-lookup"><span data-stu-id="b31c2-108">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="b31c2-109">Hvis du ikke ser denne konfigurasjonsleverandøren, må du fullføre trinnene i prosedyren [Opprette konfigurasjonsleverandører og merke dem som aktive](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="b31c2-109">If you don't see this configuration provider, complete the steps in the procedure [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span>
3.    <span data-ttu-id="b31c2-110">Klikk på **Rapporteringskonfigurasjoner**.</span><span class="sxs-lookup"><span data-stu-id="b31c2-110">Click **Reporting configurations**.</span></span>

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="b31c2-111">Opprett en ny datamodellkonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="b31c2-111">Create a new data model configuration</span></span>
1.    <span data-ttu-id="b31c2-112">Klikk på **Opprett konfigurasjon** for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="b31c2-112">Click **Create configuration** to open the drop dialog.</span></span>
2.    <span data-ttu-id="b31c2-113">Skriv inn «Modell for å importere XML-fil» i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="b31c2-113">In the **Name** field, type 'Model to import xml file'.</span></span>
3.    <span data-ttu-id="b31c2-114">Klikk **Opprett konfigurasjon**.</span><span class="sxs-lookup"><span data-stu-id="b31c2-114">Click **Create configuration**.</span></span>
4.    <span data-ttu-id="b31c2-115">Klikk **Utforming**.</span><span class="sxs-lookup"><span data-stu-id="b31c2-115">Click **Designer**.</span></span>
5.    <span data-ttu-id="b31c2-116">Klikk på **Ny** for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="b31c2-116">Click **New** to open the drop dialog.</span></span>
6.    <span data-ttu-id="b31c2-117">Skriv inn «Rot» i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="b31c2-117">In the **Name** field, type 'Root'.</span></span>
7.    <span data-ttu-id="b31c2-118">Klikk **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="b31c2-118">Click **Add**.</span></span>
8.    <span data-ttu-id="b31c2-119">Klikk på **Ny** for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="b31c2-119">Click **New** to open the drop dialog.</span></span>
9.    <span data-ttu-id="b31c2-120">Skriv inn «Liste» i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="b31c2-120">In the **Name** field, type 'List'.</span></span>
10.    <span data-ttu-id="b31c2-121">Velg **Postliste** i **Varetype**-feltet.</span><span class="sxs-lookup"><span data-stu-id="b31c2-121">In the **Item type** field, select **Record list**.</span></span>
11.    <span data-ttu-id="b31c2-122">Klikk **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="b31c2-122">Click **Add**.</span></span>
12.    <span data-ttu-id="b31c2-123">Klikk på **Ny** for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="b31c2-123">Click **New** to open the drop dialog.</span></span>
13.    <span data-ttu-id="b31c2-124">I **Navn**-feltet skriver du inn «Kode».</span><span class="sxs-lookup"><span data-stu-id="b31c2-124">In the **Name** field, type 'Code'.</span></span>
14.    <span data-ttu-id="b31c2-125">Velg **Streng** i **Varetype**-feltet.</span><span class="sxs-lookup"><span data-stu-id="b31c2-125">In the **Item type** field, select **String**.</span></span>
15.    <span data-ttu-id="b31c2-126">Klikk **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="b31c2-126">Click **Add**.</span></span>
16.    <span data-ttu-id="b31c2-127">Klikk **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="b31c2-127">Click **Save**.</span></span>
17.    <span data-ttu-id="b31c2-128">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="b31c2-128">Close the page.</span></span>
18.    <span data-ttu-id="b31c2-129">Klikk på **Endre status**.</span><span class="sxs-lookup"><span data-stu-id="b31c2-129">Click **Change status**.</span></span>
19.    <span data-ttu-id="b31c2-130">Klikk på **Fullført**.</span><span class="sxs-lookup"><span data-stu-id="b31c2-130">Click **Complete**.</span></span>
20.    <span data-ttu-id="b31c2-131">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="b31c2-131">Click **OK**.</span></span>

## <a name="create-a-format-for-data-import"></a><span data-ttu-id="b31c2-132">Opprette et format for dataimport</span><span class="sxs-lookup"><span data-stu-id="b31c2-132">Create a format for data import</span></span>
1.    <span data-ttu-id="b31c2-133">Klikk på **Opprett konfigurasjon** for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="b31c2-133">Click **Create configuration** to open the drop dialog.</span></span>
2.    <span data-ttu-id="b31c2-134">I **Ny**-feltet angir du «Format basert på datamodellen Modell for å importere XML-fil».</span><span class="sxs-lookup"><span data-stu-id="b31c2-134">In the **New** field, enter 'Format based on data model Model to import xml file'.</span></span>
3.    <span data-ttu-id="b31c2-135">Skriv inn «Format for å importere XML-fil» i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="b31c2-135">In the **Name** field, type 'Format to import xml file'.</span></span>
4.    <span data-ttu-id="b31c2-136">Velg **Ja** i feltet **Støtter dataimport**.</span><span class="sxs-lookup"><span data-stu-id="b31c2-136">Select **Yes** in the **Supports data import** field.</span></span>
5.    <span data-ttu-id="b31c2-137">Klikk **Opprett konfigurasjon**.</span><span class="sxs-lookup"><span data-stu-id="b31c2-137">Click **Create configuration**.</span></span>

## <a name="design-a-format-to-parse-incoming-file-in-xml-format"></a><span data-ttu-id="b31c2-138">Utforme et format for å analysere innkommende fil i XML-format</span><span class="sxs-lookup"><span data-stu-id="b31c2-138">Design a format to parse incoming file in xml format</span></span>
1.    <span data-ttu-id="b31c2-139">Klikk **Utforming**.</span><span class="sxs-lookup"><span data-stu-id="b31c2-139">Click **Designer**.</span></span>
2.    <span data-ttu-id="b31c2-140">Klikk på **Legg til rot** for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="b31c2-140">Click **Add root** to open the drop dialog.</span></span>
3.    <span data-ttu-id="b31c2-141">Velg **XML\Element** i treet.</span><span class="sxs-lookup"><span data-stu-id="b31c2-141">In the tree, select **XML\Element**.</span></span>
4.    <span data-ttu-id="b31c2-142">Skriv inn «rot» i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="b31c2-142">In the **Name** field, type 'root'.</span></span>
5.    <span data-ttu-id="b31c2-143">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="b31c2-143">Click **OK**.</span></span>
6.    <span data-ttu-id="b31c2-144">Klikk på **Legg til** for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="b31c2-144">Click **Add** to open the drop dialog.</span></span>
7.    <span data-ttu-id="b31c2-145">Velg **XML\Element** i treet.</span><span class="sxs-lookup"><span data-stu-id="b31c2-145">In the tree, select **XML\Element**.</span></span>
8.    <span data-ttu-id="b31c2-146">I **Navn**-feltet skriver du inn «dokument».</span><span class="sxs-lookup"><span data-stu-id="b31c2-146">In the **Name** field, type 'document'.</span></span>
9.    <span data-ttu-id="b31c2-147">Velg **Én mange** i feltet **Multiplisitet**.</span><span class="sxs-lookup"><span data-stu-id="b31c2-147">In the **Multiplicity** field, select **One many**.</span></span>
10.    <span data-ttu-id="b31c2-148">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="b31c2-148">Click **OK**.</span></span>
11.    <span data-ttu-id="b31c2-149">Velg **rot\dokument** i treet.</span><span class="sxs-lookup"><span data-stu-id="b31c2-149">In the tree, select **root\document**.</span></span>
12.    <span data-ttu-id="b31c2-150">Klikk på **Legg til** for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="b31c2-150">Click **Add** to open the drop dialog.</span></span>
13.    <span data-ttu-id="b31c2-151">Velg **XML\Attributt** i treet.</span><span class="sxs-lookup"><span data-stu-id="b31c2-151">In the tree, select **XML\Attribute**.</span></span>
14.    <span data-ttu-id="b31c2-152">I **Navn**-feltet skriver du inn «ID».</span><span class="sxs-lookup"><span data-stu-id="b31c2-152">In the **Name** field, type 'ID'.</span></span>
15.    <span data-ttu-id="b31c2-153">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="b31c2-153">Click **OK**.</span></span>
16.    <span data-ttu-id="b31c2-154">Klikk **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="b31c2-154">Click **Save**.</span></span>

## <a name="design-a-format-mapping-to-save-parsed-information-to-data-model"></a><span data-ttu-id="b31c2-155">Utforme en formattilordning for å lagre analysert informasjon i datamodell</span><span class="sxs-lookup"><span data-stu-id="b31c2-155">Design a format mapping to save parsed information to data model</span></span>
1. <span data-ttu-id="b31c2-156">Klikk på **Tilordne format til modell**.</span><span class="sxs-lookup"><span data-stu-id="b31c2-156">Click **Map format to model**.</span></span>
2. <span data-ttu-id="b31c2-157">Klikk på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="b31c2-157">Click **New**.</span></span>
3. <span data-ttu-id="b31c2-158">Angi eller velg en verdi i feltet **Definisjon**.</span><span class="sxs-lookup"><span data-stu-id="b31c2-158">In the **Definition** field, enter or select a value.</span></span>
4. <span data-ttu-id="b31c2-159">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="b31c2-159">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="b31c2-160">I **Navn**-feltet skriver du inn «Tilordning».</span><span class="sxs-lookup"><span data-stu-id="b31c2-160">In the **Name** field, type 'Mapping'.</span></span>
6. <span data-ttu-id="b31c2-161">Klikk **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="b31c2-161">Click **Save**.</span></span>
7. <span data-ttu-id="b31c2-162">Klikk **Utforming**.</span><span class="sxs-lookup"><span data-stu-id="b31c2-162">Click **Designer**.</span></span>
8. <span data-ttu-id="b31c2-163">Utvid **format** i treet.</span><span class="sxs-lookup"><span data-stu-id="b31c2-163">In the tree, expand **format**.</span></span>
9. <span data-ttu-id="b31c2-164">I treet utvider du **format\rot: XML-element(rot)**.</span><span class="sxs-lookup"><span data-stu-id="b31c2-164">In the tree, expand **format\root: XML Element(root)**.</span></span>
10.    <span data-ttu-id="b31c2-165">I treet velger du \**format\root: XML-element(rot)\dokument: XML-element 1..*</span><span class="sxs-lookup"><span data-stu-id="b31c2-165">In the tree, select \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="b31c2-166">(dokument)\*\*.</span><span class="sxs-lookup"><span data-stu-id="b31c2-166">(document)\*\*.</span></span>
11.    <span data-ttu-id="b31c2-167">Klikk på **Bind**.</span><span class="sxs-lookup"><span data-stu-id="b31c2-167">Click **Bind**.</span></span>
12.    <span data-ttu-id="b31c2-168">I treet utvider du \**format\rot: XML-element(rot)\dokument: XML-element 1..*</span><span class="sxs-lookup"><span data-stu-id="b31c2-168">In the tree, expand \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="b31c2-169">(dokument)\*\*.</span><span class="sxs-lookup"><span data-stu-id="b31c2-169">(document)\*\*.</span></span>
13.    <span data-ttu-id="b31c2-170">I treet velger du \**format\root: XML-element(rot)\dokument: XML-element 1..*</span><span class="sxs-lookup"><span data-stu-id="b31c2-170">In the tree, select \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="b31c2-171">(dokument)\id\*\*.</span><span class="sxs-lookup"><span data-stu-id="b31c2-171">(document)\id\*\*.</span></span>
14.    <span data-ttu-id="b31c2-172">I treet utvider du **Liste = format.rot.dokument**.</span><span class="sxs-lookup"><span data-stu-id="b31c2-172">In the tree, expand **List = format.root.document**.</span></span>
15.    <span data-ttu-id="b31c2-173">I treet velger du **Liste = format.rot.dokument\Kode**.</span><span class="sxs-lookup"><span data-stu-id="b31c2-173">In the tree, select **List = format.root.document\Code**.</span></span>
16.    <span data-ttu-id="b31c2-174">Klikk på **Bind**.</span><span class="sxs-lookup"><span data-stu-id="b31c2-174">Click **Bind**.</span></span>
17.    <span data-ttu-id="b31c2-175">Klikk **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="b31c2-175">Click **Save**.</span></span>
18.    <span data-ttu-id="b31c2-176">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="b31c2-176">Close the page.</span></span>
 
## <a name="run-format-mapping"></a><span data-ttu-id="b31c2-177">Kjøre formattilordning</span><span class="sxs-lookup"><span data-stu-id="b31c2-177">Run format mapping</span></span>
1. <span data-ttu-id="b31c2-178">Klikk på **Kjør**.</span><span class="sxs-lookup"><span data-stu-id="b31c2-178">Click **Run**.</span></span>
2. <span data-ttu-id="b31c2-179">Klikk på **Bla gjennom**, og velg **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span><span class="sxs-lookup"><span data-stu-id="b31c2-179">Click **Browse** and select **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span></span>
3. <span data-ttu-id="b31c2-180">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="b31c2-180">Click **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="b31c2-181">Den valgte filen er ikke importert, siden formatutformingen forutsetter at et «id»-attributt finnes for «dokument»-elementet, men den importerte filen inneholder ikke noe slikt attributt.</span><span class="sxs-lookup"><span data-stu-id="b31c2-181">The selected file has not been imported as the format design assumes the existence of 'id' attribute for the 'document' element, but the imported file contains no such attribute.</span></span>

## <a name="modify-format-structure-to-handle-xml-attribute-as-optional"></a><span data-ttu-id="b31c2-182">Endre formatstrukturen for å håndtere XML-attributter som valgfrie</span><span class="sxs-lookup"><span data-stu-id="b31c2-182">Modify format structure to handle xml attribute as optional</span></span>
1. <span data-ttu-id="b31c2-183">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="b31c2-183">Close the page.</span></span>
2. <span data-ttu-id="b31c2-184">Utvid **rot\dokument** i treet.</span><span class="sxs-lookup"><span data-stu-id="b31c2-184">In the tree, expand **root\document**.</span></span>
3. <span data-ttu-id="b31c2-185">Velg **rot\dokument\id** i treet.</span><span class="sxs-lookup"><span data-stu-id="b31c2-185">In the tree, select **root\document\id**.</span></span>
4. <span data-ttu-id="b31c2-186">Velg **Ja** i feltet **Tom streng for manglende attributt**.</span><span class="sxs-lookup"><span data-stu-id="b31c2-186">Select **Yes** in the **Empty string for missing attribute** field.</span></span>
5. <span data-ttu-id="b31c2-187">Klikk **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="b31c2-187">Click **Save**.</span></span>
 
## <a name="run-format-mapping-to-test-changes"></a><span data-ttu-id="b31c2-188">Kjøre formattilordning for å teste endringer</span><span class="sxs-lookup"><span data-stu-id="b31c2-188">Run format mapping to test changes</span></span>
1. <span data-ttu-id="b31c2-189">Klikk på **Tilordne format til modell**.</span><span class="sxs-lookup"><span data-stu-id="b31c2-189">Click **Map format to model**.</span></span>
2. <span data-ttu-id="b31c2-190">Klikk på **Kjør**.</span><span class="sxs-lookup"><span data-stu-id="b31c2-190">Click **Run**.</span></span>
3. <span data-ttu-id="b31c2-191">Klikk på **Bla gjennom**, og velg filen **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span><span class="sxs-lookup"><span data-stu-id="b31c2-191">Click **Browse** and select the **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml** file.</span></span>
4. <span data-ttu-id="b31c2-192">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="b31c2-192">Click **OK**.</span></span>
5. <span data-ttu-id="b31c2-193">Se gjennom den genererte filen.</span><span class="sxs-lookup"><span data-stu-id="b31c2-193">Review the generated file.</span></span> 

> [!NOTE]
> <span data-ttu-id="b31c2-194">Den samme filen har blitt importert siden formatutformingen nå regner «id»-attributtet for «dokument»-elementet for å være valgfritt.</span><span class="sxs-lookup"><span data-stu-id="b31c2-194">The same file has been imported as the format design now consider the 'id' attribute for the 'document' element as optional.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]