---
title: Få tilgang til programmetadata ved hjelp av ER-konfigurasjon
description: Trinnene i dette emnet forklarer hvordan en RCS-bruker (Regulatory Configuration Service) kan utforme en ny modelltilordning for elektronisk rapportering (ER) ved å bruke metadata i Finance and Operations.
author: NickSelin
manager: AnnBe
ms.date: 06/28/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fa8e9ac4940bbc1252819ebcc3de2e21c9e0933f
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682171"
---
# <a name="access-application-metadata-by-using-er-configuration"></a><span data-ttu-id="a96e4-103">Få tilgang til programmetadata ved hjelp av ER-konfigurasjon</span><span class="sxs-lookup"><span data-stu-id="a96e4-103">Access application metadata by using ER configuration</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a96e4-104">De følgende trinnene forklarer hvordan en RCS-bruker (Regulatory Configuration Service) i rollen Systemansvarlig eller Utvikler av elektronisk rapportering kan utforme en ny modelltilordning for elektronisk rapportering (ER) ved å bruke programmetadataene.</span><span class="sxs-lookup"><span data-stu-id="a96e4-104">The following steps explain how a Regulatory configuration service (RCS) user in the System Administrator or Electronic Reporting Developer role can design a new Electronic reporting (ER) model mapping by using the application metadata.</span></span> <span data-ttu-id="a96e4-105">Du får tilgang til programmetadata ved å bruke en ER-metadatakonfigurasjon som inneholder et eksempelsett med metadata som gir tilgang til utenrikshandelstransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="a96e4-105">Application metadata will be accessed by using an ER metadata configuration that contains a sample set of metadata to access foreign trade transactions.</span></span> <span data-ttu-id="a96e4-106">For å fullføre disse trinnene må du først fullføre trinnene i emnet [Opprette konfigurasjonsleverandører og merke dem som aktive](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="a96e4-106">To complete these steps, in RCS you must first complete the steps in the topic, [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md) procedure.</span></span> <span data-ttu-id="a96e4-107">Deretter fullfører du trinnene i emnet [Klargjøre programmetadataene som skal brukes i RCS](prepare-application-metadata-rcs.md).</span><span class="sxs-lookup"><span data-stu-id="a96e4-107">Then complete the steps in the topic, [Prepare application metadata to be used in RCS](prepare-application-metadata-rcs.md).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="a96e4-108">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="a96e4-108">Prerequisites</span></span>
1. <span data-ttu-id="a96e4-109">Gå til **Alle arbeidsområder** > **Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="a96e4-109">Go to **All workspaces** > **Electronic reporting**.</span></span> 
2. <span data-ttu-id="a96e4-110">Kontroller at konfigurasjonsleverandøren for eksempelfirmaet Litware, Inc. er tilgjengelig og merket som **Aktiv**.</span><span class="sxs-lookup"><span data-stu-id="a96e4-110">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="a96e4-111">Hvis du ikke ser denne konfigurasjonsleverandøren, må du fullføre trinnene i prosedyren [Opprette konfigurasjonsleverandører og merke dem som aktive](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="a96e4-111">If you don't see this configuration provider, complete the steps in the procedure [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> 

## <a name="import-metadata-configuration"></a><span data-ttu-id="a96e4-112">Importere metadatakonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="a96e4-112">Import metadata configuration</span></span> 
1. <span data-ttu-id="a96e4-113">Klikk på **Metadatakonfigurasjoner**.</span><span class="sxs-lookup"><span data-stu-id="a96e4-113">Click **Metadata configurations**.</span></span> 
2. <span data-ttu-id="a96e4-114">Importer ER-metadatakonfigurasjonen som inneholder metadata, som er konfigurert slik at elektroniske dokumenter genereres for utenrikshandel.</span><span class="sxs-lookup"><span data-stu-id="a96e4-114">Import the ER metadata configuration that contains metadata that has been configured to generate electronic documents for foreign trade business.</span></span> <span data-ttu-id="a96e4-115">Denne ER-metadatakonfigurasjonen har blitt eksportert som en XML-fil mens trinnene i prosedyren [Klargjøre programmetadataene som skal brukes i RCS](prepare-application-metadata-rcs.md) har blitt fullført.</span><span class="sxs-lookup"><span data-stu-id="a96e4-115">This ER metadata configuration has been exported as XML file while the steps in the [Prepare application metadata to be used in RCS](prepare-application-metadata-rcs.md) procedure have been completed.</span></span> 
3. <span data-ttu-id="a96e4-116">Klikk på **Veksle**.</span><span class="sxs-lookup"><span data-stu-id="a96e4-116">Click **Exchange**.</span></span> 
4. <span data-ttu-id="a96e4-117">Klikk på **Last fra XML-fil**.</span><span class="sxs-lookup"><span data-stu-id="a96e4-117">Click **Load from XML file**.</span></span> 
5. <span data-ttu-id="a96e4-118">Klikk på **Bla gjennom**, og velg filen Foreign trade metadata.xml.</span><span class="sxs-lookup"><span data-stu-id="a96e4-118">Click **Browse** and select the 'Foreign trade metadata.xml' file.</span></span> 
6. <span data-ttu-id="a96e4-119">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="a96e4-119">Click **OK**.</span></span> 
7. <span data-ttu-id="a96e4-120">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="a96e4-120">Close the page.</span></span> 

## <a name="create-data-model-configuration"></a><span data-ttu-id="a96e4-121">Opprette en datamodellkonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="a96e4-121">Create data model configuration</span></span>
1. <span data-ttu-id="a96e4-122">Klikk på **Rapporteringskonfigurasjoner**.</span><span class="sxs-lookup"><span data-stu-id="a96e4-122">Click **Reporting configurations**.</span></span> 
2. <span data-ttu-id="a96e4-123">Klikk på **Opprett konfigurasjon** for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="a96e4-123">Click **Create configuration** to open the drop dialog.</span></span> 
3. <span data-ttu-id="a96e4-124">I **Navn**-feltet skriver du inn «Utenrikshandelsmodell».</span><span class="sxs-lookup"><span data-stu-id="a96e4-124">In the **Name** field, type 'Foreign trade model'.</span></span> 
4. <span data-ttu-id="a96e4-125">Klikk **Opprett konfigurasjon**.</span><span class="sxs-lookup"><span data-stu-id="a96e4-125">Click **Create configuration**.</span></span> 
5. <span data-ttu-id="a96e4-126">Klikk **Utforming**.</span><span class="sxs-lookup"><span data-stu-id="a96e4-126">Click **Designer**.</span></span> 
6. <span data-ttu-id="a96e4-127">Klikk på **Ny** for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="a96e4-127">Click **New** to open the drop dialog.</span></span> 
7. <span data-ttu-id="a96e4-128">Skriv inn «Rot» i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="a96e4-128">In the **Name** field, type 'Root'.</span></span> 
8. <span data-ttu-id="a96e4-129">Klikk **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="a96e4-129">Click **Add**.</span></span> 
9. <span data-ttu-id="a96e4-130">Klikk på **Ny** for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="a96e4-130">Click **New** to open the drop dialog.</span></span> 
10.    <span data-ttu-id="a96e4-131">Skriv inn «Transaksjon» i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="a96e4-131">In the **Name** field, type 'Transaction'.</span></span> 
11.    <span data-ttu-id="a96e4-132">Velg **Postliste** i **Varetype**-feltet.</span><span class="sxs-lookup"><span data-stu-id="a96e4-132">In the **Item type** field, select **Record list**.</span></span> 
12.    <span data-ttu-id="a96e4-133">Klikk **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="a96e4-133">Click **Add**.</span></span> 
13.    <span data-ttu-id="a96e4-134">Klikk på **Ny** for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="a96e4-134">Click **New** to open the drop dialog.</span></span> 
14.    <span data-ttu-id="a96e4-135">I **Navn**-feltet skriver du inn «Artikkelkode».</span><span class="sxs-lookup"><span data-stu-id="a96e4-135">In the **Name** field, type 'Commodity code'.</span></span> 
15.    <span data-ttu-id="a96e4-136">Velg **Streng** i **Varetype**-feltet.</span><span class="sxs-lookup"><span data-stu-id="a96e4-136">In the **Item type** field, select **String**.</span></span> 
16.    <span data-ttu-id="a96e4-137">Klikk **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="a96e4-137">Click **Add**.</span></span> 
17.    <span data-ttu-id="a96e4-138">Klikk på **Ny** for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="a96e4-138">Click **New** to open the drop dialog.</span></span> 
18.    <span data-ttu-id="a96e4-139">Skriv inn «Fakturert beløp» i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="a96e4-139">In the **Name** field, type 'Invoiced amount'.</span></span> 
19.    <span data-ttu-id="a96e4-140">Velg **Faktisk** i **Varetype**-feltet.</span><span class="sxs-lookup"><span data-stu-id="a96e4-140">In the **Item type** field, select **Real**.</span></span> 
20.    <span data-ttu-id="a96e4-141">Klikk **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="a96e4-141">Click **Add**.</span></span> 
21.    <span data-ttu-id="a96e4-142">Klikk på **Ny** for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="a96e4-142">Click **New** to open the drop dialog.</span></span> 
22.    <span data-ttu-id="a96e4-143">Skriv inn «Dato» i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="a96e4-143">In the **Name** field, type 'Date'.</span></span> 
23.    <span data-ttu-id="a96e4-144">Velg **Dato** i **Varetype**-feltet.</span><span class="sxs-lookup"><span data-stu-id="a96e4-144">In the **Item type** field, select **Date**.</span></span> 
24.    <span data-ttu-id="a96e4-145">Klikk **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="a96e4-145">Click **Add**.</span></span> 
25.    <span data-ttu-id="a96e4-146">Klikk på **Rotreferanse**.</span><span class="sxs-lookup"><span data-stu-id="a96e4-146">Click **Root reference**.</span></span> 
26.    <span data-ttu-id="a96e4-147">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="a96e4-147">Click **OK**.</span></span> 
27.    <span data-ttu-id="a96e4-148">Klikk **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="a96e4-148">Click **Save**.</span></span> 
28.    <span data-ttu-id="a96e4-149">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="a96e4-149">Close the page.</span></span> 
29.    <span data-ttu-id="a96e4-150">Klikk på **Endre status**.</span><span class="sxs-lookup"><span data-stu-id="a96e4-150">Click **Change status**.</span></span> 
30.    <span data-ttu-id="a96e4-151">Klikk på **Fullført**.</span><span class="sxs-lookup"><span data-stu-id="a96e4-151">Click **Complete**.</span></span> 
31.    <span data-ttu-id="a96e4-152">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="a96e4-152">Click **OK**.</span></span> 

## <a name="create-model-mapping-configuration"></a><span data-ttu-id="a96e4-153">Opprette en modelltilordningskonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="a96e4-153">Create model mapping configuration</span></span> 
1. <span data-ttu-id="a96e4-154">Klikk på **Opprett konfigurasjon** for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="a96e4-154">Click **Create configuration** to open the drop dialog.</span></span> 
2. <span data-ttu-id="a96e4-155">I **Ny**-feltet angir du «Modelltilordning basert på datamodellen Utenrikshandelsmodell».</span><span class="sxs-lookup"><span data-stu-id="a96e4-155">In the **New** field, enter 'Model Mapping based on data model Foreign trade model'.</span></span> 
3. <span data-ttu-id="a96e4-156">I **Navn**-feltet skriver du inn «Utenrikshandelstilordning».</span><span class="sxs-lookup"><span data-stu-id="a96e4-156">In the **Name** field, type 'Foreign trade mapping'.</span></span> 
4. <span data-ttu-id="a96e4-157">Klikk **Opprett konfigurasjon**.</span><span class="sxs-lookup"><span data-stu-id="a96e4-157">Click **Create configuration**.</span></span> 
5. <span data-ttu-id="a96e4-158">Utvid delen **Forutsetninger**.</span><span class="sxs-lookup"><span data-stu-id="a96e4-158">Expand the **Prerequisites** section.</span></span> 
6. <span data-ttu-id="a96e4-159">Klikk **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="a96e4-159">Click **Edit**.</span></span> 
7. <span data-ttu-id="a96e4-160">Klikk på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="a96e4-160">Click **New**.</span></span> 
8. <span data-ttu-id="a96e4-161">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="a96e4-161">In the list, mark the selected row.</span></span> 
9. <span data-ttu-id="a96e4-162">Velg **Konfigurasjon** i feltet **Nødvendig komponenttype**.</span><span class="sxs-lookup"><span data-stu-id="a96e4-162">In the **Prerequisite component type** field, select **Configuration**.</span></span> 
10.    <span data-ttu-id="a96e4-163">Velg konfigurasjonen **Metadata for utenrikshandel**.</span><span class="sxs-lookup"><span data-stu-id="a96e4-163">Select **Foreign trade metadata** configuration.</span></span> 
11.    <span data-ttu-id="a96e4-164">Klikk **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="a96e4-164">Click **Save**.</span></span> 
12.    <span data-ttu-id="a96e4-165">Vi har lagt til referansen i versjon 1 av konfigurasjonen Metadata for utenrikshandel.</span><span class="sxs-lookup"><span data-stu-id="a96e4-165">We added the reference to the version 1 of the 'Foreign trade metadata' configuration.</span></span> <span data-ttu-id="a96e4-166">Programmetadata fra denne konfigurasjonen tilbys mens denne modelltilordningen utformes.</span><span class="sxs-lookup"><span data-stu-id="a96e4-166">Application metadata from this configuration will be offered while this model mapping will be designed.</span></span> 
13.    <span data-ttu-id="a96e4-167">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="a96e4-167">Close the page.</span></span> 
14.    <span data-ttu-id="a96e4-168">Klikk **Utforming**.</span><span class="sxs-lookup"><span data-stu-id="a96e4-168">Click **Designer**.</span></span> 
15.    <span data-ttu-id="a96e4-169">Klikk **Utforming**.</span><span class="sxs-lookup"><span data-stu-id="a96e4-169">Click **Designer**.</span></span> 
16.    <span data-ttu-id="a96e4-170">I treet velger du **Dynamics 365 for Operations\Tabellposter**.</span><span class="sxs-lookup"><span data-stu-id="a96e4-170">In the tree, select **Dynamics 365 for Operations\Table records**.</span></span> 
17.    <span data-ttu-id="a96e4-171">Klikk på **Legg til rot**.</span><span class="sxs-lookup"><span data-stu-id="a96e4-171">Click **Add root**.</span></span> 
18.    <span data-ttu-id="a96e4-172">I **Navn**-feltet skriver du inn «Intrastat».</span><span class="sxs-lookup"><span data-stu-id="a96e4-172">In the **Name** field, type 'Intrastat'.</span></span> 
19.    <span data-ttu-id="a96e4-173">Velg **Intrastat**-tabellposter.</span><span class="sxs-lookup"><span data-stu-id="a96e4-173">Select **Intrastat** table records.</span></span> 
20.    <span data-ttu-id="a96e4-174">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="a96e4-174">Click **OK**.</span></span> 

> [!NOTE]
> <span data-ttu-id="a96e4-175">Bare to tabeller ble tilbudt siden bare to tabeller ble lagt til i settet med metadata som brukes for øyeblikket.</span><span class="sxs-lookup"><span data-stu-id="a96e4-175">The only 2 tables were offered as the only 2 tables were added into the set of metadata which is currently in use.</span></span> 

21.    <span data-ttu-id="a96e4-176">Klikk på **Bind**.</span><span class="sxs-lookup"><span data-stu-id="a96e4-176">Click **Bind**.</span></span> 
22.    <span data-ttu-id="a96e4-177">Utvid **Intrastat** i treet.</span><span class="sxs-lookup"><span data-stu-id="a96e4-177">In the tree, expand **Intrastat**.</span></span> 
23.    <span data-ttu-id="a96e4-178">Velg **Intrastat\AmountMST** i treet.</span><span class="sxs-lookup"><span data-stu-id="a96e4-178">In the tree, select **Intrastat\AmountMST**.</span></span> 
24.    <span data-ttu-id="a96e4-179">Utvid **Transaksjon = Intrastat** i treet.</span><span class="sxs-lookup"><span data-stu-id="a96e4-179">In the tree, expand **Transaction = Intrastat**.</span></span> 
25.    <span data-ttu-id="a96e4-180">Velg **Transaksjon = Intrastat \ Fakturert beløp** i treet.</span><span class="sxs-lookup"><span data-stu-id="a96e4-180">In the tree, select **Transaction = Intrastat\Invoiced amount**.</span></span> 
26.    <span data-ttu-id="a96e4-181">Klikk på **Bind**.</span><span class="sxs-lookup"><span data-stu-id="a96e4-181">Click **Bind**.</span></span> 
27.    <span data-ttu-id="a96e4-182">Velg **Intrastat\TransDate** i treet.</span><span class="sxs-lookup"><span data-stu-id="a96e4-182">In the tree, select **Intrastat\TransDate**.</span></span> 
28.    <span data-ttu-id="a96e4-183">Velg **Transaksjon = Intrastat\Dato** i treet.</span><span class="sxs-lookup"><span data-stu-id="a96e4-183">In the tree, select **Transaction = Intrastat\Date**.</span></span> 
29.    <span data-ttu-id="a96e4-184">Klikk på **Bind**.</span><span class="sxs-lookup"><span data-stu-id="a96e4-184">Click **Bind**.</span></span> 
30.    <span data-ttu-id="a96e4-185">Utvid **Intrastat\>Relasjoner** i treet.</span><span class="sxs-lookup"><span data-stu-id="a96e4-185">In the tree, expand **Intrastat\>Relations**.</span></span> 
31.    <span data-ttu-id="a96e4-186">Utvid **Intrastat\>Relasjoner\IntrastatCommodity** i treet.</span><span class="sxs-lookup"><span data-stu-id="a96e4-186">In the tree, expand **Intrastat\>Relations\IntrastatCommodity**.</span></span> 
32.    <span data-ttu-id="a96e4-187">Velg **Intrastat\>Relasjoner\IntrastatCommodity\Kode** i treet.</span><span class="sxs-lookup"><span data-stu-id="a96e4-187">In the tree, select **Intrastat\>Relations\IntrastatCommodity\Code**.</span></span> 
33.    <span data-ttu-id="a96e4-188">Velg **Transaksjon = Intrastat\Artikkelkode** i treet.</span><span class="sxs-lookup"><span data-stu-id="a96e4-188">In the tree, select **Transaction = Intrastat\Commodity code**.</span></span> 
34.    <span data-ttu-id="a96e4-189">Klikk på **Bind**.</span><span class="sxs-lookup"><span data-stu-id="a96e4-189">Click **Bind**.</span></span> 
35.    <span data-ttu-id="a96e4-190">Klikk på **Valider**.</span><span class="sxs-lookup"><span data-stu-id="a96e4-190">Click **Validate**.</span></span> 

> [!NOTE]
> <span data-ttu-id="a96e4-191">Vi har bundet elementer i datamodellen til elementer i datakildene som er beskrevet, ved å bruke detaljer i programmetadataene fra ER-metadatakonfigurasjonen det henvises til.</span><span class="sxs-lookup"><span data-stu-id="a96e4-191">We have successfully bound elements of data model with items of data sources that are described by using details of application metadata from the referred ER metadata configuration.</span></span> 
36.    <span data-ttu-id="a96e4-192">Klikk **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="a96e4-192">Click **Save**.</span></span> 
37.    <span data-ttu-id="a96e4-193">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="a96e4-193">Close the page.</span></span> 
38.    <span data-ttu-id="a96e4-194">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="a96e4-194">Close the page.</span></span> 
39.    <span data-ttu-id="a96e4-195">Når det er nødvendig, kan du utvide det eksisterende settet med metadata og deretter eksportere den nye, fullførte versjonen av ER-metadatakonfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="a96e4-195">When needed, you can extend the existing set of metadata and then export the new completed version of ER metadata configuration.</span></span> <span data-ttu-id="a96e4-196">Du kan deretter importere den til RCS og oppdatere forutsetningene for den konfigurerte modelltilordningskonfigurasjon som refererer til en ny versjon av importert metadatakonfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="a96e4-196">You can then import it to RCS, and update the prerequisites of the configured model mapping configuration referring to a new version of imported metadata configuration.</span></span> 

> [!NOTE]
> <span data-ttu-id="a96e4-197">Denne måten å hente informasjon om programmetadata på er den eneste tilgjengelige for lokalt distribuerte programmer (når lokale forretningsdata (LBD) eller en lokal distribusjonsmodell brukes).</span><span class="sxs-lookup"><span data-stu-id="a96e4-197">This way of getting information about application metadata is the only one available for locally deployed applications (when local business data (LBD), or on-premises, deployment model is used).</span></span>
        
