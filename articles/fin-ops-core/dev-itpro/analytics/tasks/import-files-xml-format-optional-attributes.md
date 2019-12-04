---
title: (RCS) Importere filer i XML-format med valgfrie attributter
description: Dette emnet inneholder informasjon om hvordan en bruker kan utforme ER-formatkonfigurasjon for å importere filer i XML-format som inneholder valgfrie attributter.
author: NickSelin
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-07-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f34302a32b2e06f281dc93d6df160b88ffac7123
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/06/2019
ms.locfileid: "2769791"
---
# <a name="rcs-import-files-in-xml-format-with-optional-attributes"></a><span data-ttu-id="6f527-103">(RCS) Importere filer i XML-format med valgfrie attributter</span><span class="sxs-lookup"><span data-stu-id="6f527-103">(RCS) Import files in XML format with optional attributes</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6f527-104">Fremgangsmåten nedenfor forklarer hvordan en bruker i rollen Systemansvarlig eller Utvikler av elektronisk rapportering kan utforme en ER-formatkonfigurasjon for å importere filer i XML-format som inneholder valgfrie attributter.</span><span class="sxs-lookup"><span data-stu-id="6f527-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can design ER format configuration to import files in XML format containing optional attributes.</span></span> <span data-ttu-id="6f527-105">For å fullføre disse trinnene må du først fullføre trinnene i fremgangsmåten "Opprette en konfigurasjonsleverandør og merke den som aktiv".</span><span class="sxs-lookup"><span data-stu-id="6f527-105">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span> <span data-ttu-id="6f527-106">Før du begynner, laster du ned filen IncomingDocumentToLearnHowToHandleOptionalAttributes.xml fra [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684) og lagrer den lokalt.</span><span class="sxs-lookup"><span data-stu-id="6f527-106">Before you begin, download and save locally the IncomingDocumentToLearnHowToHandleOptionalAttributes.xml file from [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).</span></span>

1.  <span data-ttu-id="6f527-107">Gå til **Alle arbeidsområder** > **Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="6f527-107">Go to **All workspaces** > **Electronic reporting**.</span></span>
2.  <span data-ttu-id="6f527-108">Kontroller at konfigurasjonsleverandøren for eksempelfirmaet Litware, Inc. er tilgjengelig og merket som **Aktiv**.</span><span class="sxs-lookup"><span data-stu-id="6f527-108">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="6f527-109">Hvis du ikke ser denne konfigurasjonsleverandøren, må du fullføre trinnene i prosedyren [Opprette konfigurasjonsleverandører og merke dem som aktive](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="6f527-109">If you don’t see this configuration provider, complete the steps in the procedure [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span>
3.  <span data-ttu-id="6f527-110">Klikk på **Rapporteringskonfigurasjoner**.</span><span class="sxs-lookup"><span data-stu-id="6f527-110">Click **Reporting configurations**.</span></span>

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="6f527-111">Opprett en ny datamodellkonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="6f527-111">Create a new data model configuration</span></span>
1.  <span data-ttu-id="6f527-112">Klikk på **Opprett konfigurasjon** for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="6f527-112">Click **Create configuration** to open the drop dialog.</span></span>
2.  <span data-ttu-id="6f527-113">Skriv inn «Modell for å importere XML-fil» i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="6f527-113">In the **Name** field, type 'Model to import xml file'.</span></span>
3.  <span data-ttu-id="6f527-114">Klikk **Opprett konfigurasjon**.</span><span class="sxs-lookup"><span data-stu-id="6f527-114">Click **Create configuration**.</span></span>
4.  <span data-ttu-id="6f527-115">Klikk **Utforming**.</span><span class="sxs-lookup"><span data-stu-id="6f527-115">Click **Designer**.</span></span>
5.  <span data-ttu-id="6f527-116">Klikk på **Ny** for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="6f527-116">Click **New** to open the drop dialog.</span></span>
6.  <span data-ttu-id="6f527-117">Skriv inn «Rot» i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="6f527-117">In the **Name** field, type 'Root'.</span></span>
7.  <span data-ttu-id="6f527-118">Klikk **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="6f527-118">Click **Add**.</span></span>
8.  <span data-ttu-id="6f527-119">Klikk på **Ny** for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="6f527-119">Click **New** to open the drop dialog.</span></span>
9.  <span data-ttu-id="6f527-120">Skriv inn «Liste» i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="6f527-120">In the **Name** field, type 'List'.</span></span>
10. <span data-ttu-id="6f527-121">Velg **Postliste** i **Varetype**-feltet.</span><span class="sxs-lookup"><span data-stu-id="6f527-121">In the **Item type** field, select **Record list**.</span></span>
11. <span data-ttu-id="6f527-122">Klikk **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="6f527-122">Click **Add**.</span></span>
12. <span data-ttu-id="6f527-123">Klikk på **Ny** for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="6f527-123">Click **New** to open the drop dialog.</span></span>
13. <span data-ttu-id="6f527-124">I **Navn**-feltet skriver du inn «Kode».</span><span class="sxs-lookup"><span data-stu-id="6f527-124">In the **Name** field, type 'Code'.</span></span>
14. <span data-ttu-id="6f527-125">Velg **Streng** i **Varetype**-feltet.</span><span class="sxs-lookup"><span data-stu-id="6f527-125">In the **Item type** field, select **String**.</span></span>
15. <span data-ttu-id="6f527-126">Klikk **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="6f527-126">Click **Add**.</span></span>
16. <span data-ttu-id="6f527-127">Klikk **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="6f527-127">Click **Save**.</span></span>
17. <span data-ttu-id="6f527-128">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="6f527-128">Close the page.</span></span>
18. <span data-ttu-id="6f527-129">Klikk på **Endre status**.</span><span class="sxs-lookup"><span data-stu-id="6f527-129">Click **Change status**.</span></span>
19. <span data-ttu-id="6f527-130">Klikk på **Fullført**.</span><span class="sxs-lookup"><span data-stu-id="6f527-130">Click **Complete**.</span></span>
20. <span data-ttu-id="6f527-131">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="6f527-131">Click **OK**.</span></span>

## <a name="create-a-format-for-data-import"></a><span data-ttu-id="6f527-132">Opprette et format for dataimport</span><span class="sxs-lookup"><span data-stu-id="6f527-132">Create a format for data import</span></span>
1.  <span data-ttu-id="6f527-133">Klikk på **Opprett konfigurasjon** for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="6f527-133">Click **Create configuration** to open the drop dialog.</span></span>
2.  <span data-ttu-id="6f527-134">I **Ny**-feltet angir du «Format basert på datamodellen Modell for å importere XML-fil».</span><span class="sxs-lookup"><span data-stu-id="6f527-134">In the **New** field, enter 'Format based on data model Model to import xml file'.</span></span>
3.  <span data-ttu-id="6f527-135">Skriv inn «Format for å importere XML-fil» i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="6f527-135">In the **Name** field, type 'Format to import xml file'.</span></span>
4.  <span data-ttu-id="6f527-136">Velg **Ja** i feltet **Støtter dataimport**.</span><span class="sxs-lookup"><span data-stu-id="6f527-136">Select **Yes** in the **Supports data import** field.</span></span>
5.  <span data-ttu-id="6f527-137">Klikk **Opprett konfigurasjon**.</span><span class="sxs-lookup"><span data-stu-id="6f527-137">Click **Create configuration**.</span></span>

## <a name="design-a-format-to-parse-incoming-file-in-xml-format"></a><span data-ttu-id="6f527-138">Utforme et format for å analysere innkommende fil i XML-format</span><span class="sxs-lookup"><span data-stu-id="6f527-138">Design a format to parse incoming file in xml format</span></span>
1.  <span data-ttu-id="6f527-139">Klikk **Utforming**.</span><span class="sxs-lookup"><span data-stu-id="6f527-139">Click **Designer**.</span></span>
2.  <span data-ttu-id="6f527-140">Klikk på **Legg til rot** for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="6f527-140">Click **Add root** to open the drop dialog.</span></span>
3.  <span data-ttu-id="6f527-141">Velg **XML\Element** i treet.</span><span class="sxs-lookup"><span data-stu-id="6f527-141">In the tree, select **XML\Element**.</span></span>
4.  <span data-ttu-id="6f527-142">Skriv inn «rot» i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="6f527-142">In the **Name** field, type 'root'.</span></span>
5.  <span data-ttu-id="6f527-143">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="6f527-143">Click **OK**.</span></span>
6.  <span data-ttu-id="6f527-144">Klikk på **Legg til** for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="6f527-144">Click **Add** to open the drop dialog.</span></span>
7.  <span data-ttu-id="6f527-145">Velg **XML\Element** i treet.</span><span class="sxs-lookup"><span data-stu-id="6f527-145">In the tree, select **XML\Element**.</span></span>
8.  <span data-ttu-id="6f527-146">I **Navn**-feltet skriver du inn «dokument».</span><span class="sxs-lookup"><span data-stu-id="6f527-146">In the **Name** field, type 'document'.</span></span>
9.  <span data-ttu-id="6f527-147">Velg **Én mange** i feltet **Multiplisitet**.</span><span class="sxs-lookup"><span data-stu-id="6f527-147">In the **Multiplicity** field, select **One many**.</span></span>
10. <span data-ttu-id="6f527-148">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="6f527-148">Click **OK**.</span></span>
11. <span data-ttu-id="6f527-149">Velg **rot\dokument** i treet.</span><span class="sxs-lookup"><span data-stu-id="6f527-149">In the tree, select **root\document**.</span></span>
12. <span data-ttu-id="6f527-150">Klikk på **Legg til** for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="6f527-150">Click **Add** to open the drop dialog.</span></span>
13. <span data-ttu-id="6f527-151">Velg **XML\Attributt** i treet.</span><span class="sxs-lookup"><span data-stu-id="6f527-151">In the tree, select **XML\Attribute**.</span></span>
14. <span data-ttu-id="6f527-152">I **Navn**-feltet skriver du inn «ID».</span><span class="sxs-lookup"><span data-stu-id="6f527-152">In the **Name** field, type 'ID'.</span></span>
15. <span data-ttu-id="6f527-153">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="6f527-153">Click **OK**.</span></span>
16. <span data-ttu-id="6f527-154">Klikk **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="6f527-154">Click **Save**.</span></span>

## <a name="design-a-format-mapping-to-save-parsed-information-to-data-model"></a><span data-ttu-id="6f527-155">Utforme en formattilordning for å lagre analysert informasjon i datamodell</span><span class="sxs-lookup"><span data-stu-id="6f527-155">Design a format mapping to save parsed information to data model</span></span>
1. <span data-ttu-id="6f527-156">Klikk på **Tilordne format til modell**.</span><span class="sxs-lookup"><span data-stu-id="6f527-156">Click **Map format to model**.</span></span>
2. <span data-ttu-id="6f527-157">Klikk på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="6f527-157">Click **New**.</span></span>
3. <span data-ttu-id="6f527-158">Angi eller velg en verdi i feltet **Definisjon**.</span><span class="sxs-lookup"><span data-stu-id="6f527-158">In the **Definition** field, enter or select a value.</span></span>
4. <span data-ttu-id="6f527-159">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="6f527-159">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="6f527-160">I **Navn**-feltet skriver du inn «Tilordning».</span><span class="sxs-lookup"><span data-stu-id="6f527-160">In the **Name** field, type 'Mapping'.</span></span>
6. <span data-ttu-id="6f527-161">Klikk **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="6f527-161">Click **Save**.</span></span>
7. <span data-ttu-id="6f527-162">Klikk **Utforming**.</span><span class="sxs-lookup"><span data-stu-id="6f527-162">Click **Designer**.</span></span>
8. <span data-ttu-id="6f527-163">Utvid **format** i treet.</span><span class="sxs-lookup"><span data-stu-id="6f527-163">In the tree, expand **format**.</span></span>
9. <span data-ttu-id="6f527-164">I treet utvider du **format\rot: XML-element(rot)**.</span><span class="sxs-lookup"><span data-stu-id="6f527-164">In the tree, expand **format\root: XML Element(root)**.</span></span>
10. <span data-ttu-id="6f527-165">I treet velger du \**format\root: XML-element(rot)\dokument: XML-element 1..*</span><span class="sxs-lookup"><span data-stu-id="6f527-165">In the tree, select \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="6f527-166">(dokument)\*\*.</span><span class="sxs-lookup"><span data-stu-id="6f527-166">(document)\*\*.</span></span>
11. <span data-ttu-id="6f527-167">Klikk på **Bind**.</span><span class="sxs-lookup"><span data-stu-id="6f527-167">Click **Bind**.</span></span>
12. <span data-ttu-id="6f527-168">I treet utvider du \**format\rot: XML-element(rot)\dokument: XML-element 1..*</span><span class="sxs-lookup"><span data-stu-id="6f527-168">In the tree, expand \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="6f527-169">(dokument)\*\*.</span><span class="sxs-lookup"><span data-stu-id="6f527-169">(document)\*\*.</span></span>
13. <span data-ttu-id="6f527-170">I treet velger du \**format\root: XML-element(rot)\dokument: XML-element 1..*</span><span class="sxs-lookup"><span data-stu-id="6f527-170">In the tree, select \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="6f527-171">(dokument)\id\*\*.</span><span class="sxs-lookup"><span data-stu-id="6f527-171">(document)\id\*\*.</span></span>
14. <span data-ttu-id="6f527-172">I treet utvider du **Liste = format.rot.dokument**.</span><span class="sxs-lookup"><span data-stu-id="6f527-172">In the tree, expand **List = format.root.document**.</span></span>
15. <span data-ttu-id="6f527-173">I treet velger du **Liste = format.rot.dokument\Kode**.</span><span class="sxs-lookup"><span data-stu-id="6f527-173">In the tree, select **List = format.root.document\Code**.</span></span>
16. <span data-ttu-id="6f527-174">Klikk på **Bind**.</span><span class="sxs-lookup"><span data-stu-id="6f527-174">Click **Bind**.</span></span>
17. <span data-ttu-id="6f527-175">Klikk **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="6f527-175">Click **Save**.</span></span>
18. <span data-ttu-id="6f527-176">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="6f527-176">Close the page.</span></span>
 
## <a name="run-format-mapping"></a><span data-ttu-id="6f527-177">Kjøre formattilordning</span><span class="sxs-lookup"><span data-stu-id="6f527-177">Run format mapping</span></span>
1. <span data-ttu-id="6f527-178">Klikk på **Kjør**.</span><span class="sxs-lookup"><span data-stu-id="6f527-178">Click **Run**.</span></span>
2. <span data-ttu-id="6f527-179">Klikk på **Bla gjennom**, og velg **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span><span class="sxs-lookup"><span data-stu-id="6f527-179">Click **Browse** and select **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span></span>
3. <span data-ttu-id="6f527-180">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="6f527-180">Click **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="6f527-181">Den valgte filen er ikke importert, siden formatutformingen forutsetter at et «id»-attributt finnes for «dokument»-elementet, men den importerte filen inneholder ikke noe slikt attributt.</span><span class="sxs-lookup"><span data-stu-id="6f527-181">The selected file has not been imported as the format design assumes the existence of ‘id’ attribute for the ‘document’ element, but the imported file contains no such attribute.</span></span>

## <a name="modify-format-structure-to-handle-xml-attribute-as-optional"></a><span data-ttu-id="6f527-182">Endre formatstrukturen for å håndtere XML-attributter som valgfrie</span><span class="sxs-lookup"><span data-stu-id="6f527-182">Modify format structure to handle xml attribute as optional</span></span>
1. <span data-ttu-id="6f527-183">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="6f527-183">Close the page.</span></span>
2. <span data-ttu-id="6f527-184">Utvid **rot\dokument** i treet.</span><span class="sxs-lookup"><span data-stu-id="6f527-184">In the tree, expand **root\document**.</span></span>
3. <span data-ttu-id="6f527-185">Velg **rot\dokument\id** i treet.</span><span class="sxs-lookup"><span data-stu-id="6f527-185">In the tree, select **root\document\id**.</span></span>
4. <span data-ttu-id="6f527-186">Velg **Ja** i feltet **Tom streng for manglende attributt**.</span><span class="sxs-lookup"><span data-stu-id="6f527-186">Select **Yes** in the **Empty string for missing attribute** field.</span></span>
5. <span data-ttu-id="6f527-187">Klikk **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="6f527-187">Click **Save**.</span></span>
 
## <a name="run-format-mapping-to-test-changes"></a><span data-ttu-id="6f527-188">Kjøre formattilordning for å teste endringer</span><span class="sxs-lookup"><span data-stu-id="6f527-188">Run format mapping to test changes</span></span>
1. <span data-ttu-id="6f527-189">Klikk på **Tilordne format til modell**.</span><span class="sxs-lookup"><span data-stu-id="6f527-189">Click **Map format to model**.</span></span>
2. <span data-ttu-id="6f527-190">Klikk på **Kjør**.</span><span class="sxs-lookup"><span data-stu-id="6f527-190">Click **Run**.</span></span>
3. <span data-ttu-id="6f527-191">Klikk på **Bla gjennom**, og velg filen **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span><span class="sxs-lookup"><span data-stu-id="6f527-191">Click **Browse** and select the **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml** file.</span></span>
4. <span data-ttu-id="6f527-192">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="6f527-192">Click **OK**.</span></span>
5. <span data-ttu-id="6f527-193">Se gjennom den genererte filen.</span><span class="sxs-lookup"><span data-stu-id="6f527-193">Review the generated file.</span></span> 

> [!NOTE]
> <span data-ttu-id="6f527-194">Den samme filen har blitt importert siden formatutformingen nå regner «id»-attributtet for «dokument»-elementet for å være valgfritt.</span><span class="sxs-lookup"><span data-stu-id="6f527-194">The same file has been imported as the format design now consider the ‘id’ attribute for the ‘document’ element as optional.</span></span>
