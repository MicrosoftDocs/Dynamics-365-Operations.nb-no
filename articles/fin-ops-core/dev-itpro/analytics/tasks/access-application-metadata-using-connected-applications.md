---
title: Få tilgang til programmetadata ved hjelp av tilkoblede programmer
description: Trinnene i dette emnet forklarer hvordan en bruker av Regulatory Configuration Service kan utforme en ny modelltilordning for elektronisk rapportering ved å bruke metadata.
author: NickSelin
ms.date: 06/29/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0b113f0db1d44dc5fbda30e10d62ff939550f299
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748699"
---
# <a name="access-application-metadata-by-using-connected-applications"></a><span data-ttu-id="ca54e-103">Få tilgang til programmetadata ved hjelp av tilkoblede programmer</span><span class="sxs-lookup"><span data-stu-id="ca54e-103">Access application metadata by using connected applications</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ca54e-104">De følgende trinnene forklarer hvordan en RCS-bruker (Regulatory Configuration Service) i rollen Systemansvarlig eller Utvikler av elektronisk rapportering kan utforme en ny modelltilordning for elektronisk rapportering (ER) ved å bruke metadata i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ca54e-104">The following steps explain how a Regulatory configuration service (RCS) user in the System Administrator or Electronic Reporting Developer role can design a new Electronic reporting (ER) model mapping by using metadata in Finance and Operations.</span></span> <span data-ttu-id="ca54e-105">Du får tilgang til programmetadata på nettet ved å bruke det RCS-tilkoblede programmet.</span><span class="sxs-lookup"><span data-stu-id="ca54e-105">Application metadata will be accessed online by using the RCS connected application.</span></span> <span data-ttu-id="ca54e-106">Et ER-modelltilordningseksempel blir konfigurert for å gi tilgang til utenrikshandelstransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="ca54e-106">Sample ER model mapping will be configured to access foreign trade transactions.</span></span> <span data-ttu-id="ca54e-107">For å fullføre disse trinnene må du først fullføre trinnene i RCS i emnet [Opprette konfigurasjonsleverandører og merke dem som aktive](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="ca54e-107">To complete these steps, in RCS you must first complete the steps in the topic, [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> <span data-ttu-id="ca54e-108">Hvis du ikke har fullført trinnene i emnet [Få tilgang til programmetadata ved hjelp av ER-konfigurasjon](access-application-metadata-er-configuration.md), går du til [siden med eksempler på elektronisk rapportering](https://go.microsoft.com/fwlink/?linkid=862266) for å laste ned og lagre følgende ER-konfigurasjoner: Foreign trade metadata.xml, Foreign trade model.xml, Foreign trade mapping.xml og deretter fullføre trinnene i fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="ca54e-108">If you have not completed the steps in the topic, [Access application metadata by using ER configuration](access-application-metadata-er-configuration.md), go to the [Electronic reporting examples page](https://go.microsoft.com/fwlink/?linkid=862266) to download and save the following ER configurations: Foreign trade metadata.xml; Foreign trade model.xml; Foreign trade mapping.xml, and then complete the steps in the procedure.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="ca54e-109">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="ca54e-109">Prerequisites</span></span>
1. <span data-ttu-id="ca54e-110">Gå til **Alle arbeidsområder** > **Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="ca54e-110">Go to **All workspaces** > **Electronic reporting**.</span></span> 
2. <span data-ttu-id="ca54e-111">Kontroller at konfigurasjonsleverandøren for eksempelfirmaet Litware, Inc. er tilgjengelig og merket som **Aktiv**.</span><span class="sxs-lookup"><span data-stu-id="ca54e-111">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="ca54e-112">Hvis du ikke ser denne konfigurasjonsleverandøren, må du fullføre trinnene i prosedyren [Opprette konfigurasjonsleverandører og merke dem som aktive](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="ca54e-112">If you don't see this configuration provider, complete the steps in the procedure [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> 

## <a name="get-required-er-configurations"></a><span data-ttu-id="ca54e-113">Hente nødvendige ER-konfigurasjoner</span><span class="sxs-lookup"><span data-stu-id="ca54e-113">Get required ER configurations</span></span>
1. <span data-ttu-id="ca54e-114">Klikk på **Rapporteringskonfigurasjoner**.</span><span class="sxs-lookup"><span data-stu-id="ca54e-114">Click **Reporting configurations**.</span></span> 
2. <span data-ttu-id="ca54e-115">Hvis du allerede har fullført trinnene i prosedyren [Få tilgang til programmetadata ved hjelp av en ER-konfigurasjon](access-application-metadata-er-configuration.md), har du allerede alle nødvendige ER-konfigurasjoner (konfigurasjoner for metadata, modell og tilordning for utenrikshandel) i gjeldende RCS-forekomst.</span><span class="sxs-lookup"><span data-stu-id="ca54e-115">If you already completed the steps in the [Access application metadata by using ER configuration](access-application-metadata-er-configuration.md) procedure, you already have all necessary ER configurations (foreign trade metadata, model and mapping configurations) in the current RCS instance.</span></span> <span data-ttu-id="ca54e-116">Du kan hoppe over alle gjenstående trinn i denne underoppgaven.</span><span class="sxs-lookup"><span data-stu-id="ca54e-116">You can skip all the remaining steps of this sub-task.</span></span> 
3. <span data-ttu-id="ca54e-117">Klikk på **Veksle**.</span><span class="sxs-lookup"><span data-stu-id="ca54e-117">Click **Exchange**.</span></span> 
4. <span data-ttu-id="ca54e-118">Klikk på **Last fra XML-fil**.</span><span class="sxs-lookup"><span data-stu-id="ca54e-118">Click **Load from XML file**.</span></span> 
5. <span data-ttu-id="ca54e-119">Klikk på **Bla gjennom**, og velg filen **Foreign trade metadata.xml**.</span><span class="sxs-lookup"><span data-stu-id="ca54e-119">Click **Browse** and select the **Foreign trade metadata.xml** file.</span></span> 
6. <span data-ttu-id="ca54e-120">Klikk på **OK**.</span><span class="sxs-lookup"><span data-stu-id="ca54e-120">Click **OK**.</span></span> 
7. <span data-ttu-id="ca54e-121">Klikk på **Veksle**.</span><span class="sxs-lookup"><span data-stu-id="ca54e-121">Click **Exchange**.</span></span> 
8. <span data-ttu-id="ca54e-122">Klikk på **Last fra XML-fil**.</span><span class="sxs-lookup"><span data-stu-id="ca54e-122">Click **Load from XML file**.</span></span> 
9. <span data-ttu-id="ca54e-123">Klikk på **Bla gjennom**, og velg filen **Foreign trade model.xml**.</span><span class="sxs-lookup"><span data-stu-id="ca54e-123">Click **Browse** and select the **Foreign trade model.xml** file.</span></span> 
10. <span data-ttu-id="ca54e-124">Klikk på **OK**.</span><span class="sxs-lookup"><span data-stu-id="ca54e-124">Click **OK**.</span></span> 
11. <span data-ttu-id="ca54e-125">Klikk på **Veksle**.</span><span class="sxs-lookup"><span data-stu-id="ca54e-125">Click **Exchange**.</span></span> 
12. <span data-ttu-id="ca54e-126">Klikk på **Last fra XML-fil**.</span><span class="sxs-lookup"><span data-stu-id="ca54e-126">Click **Load from XML file**.</span></span> 
13. <span data-ttu-id="ca54e-127">Klikk på **Bla gjennom**, og velg filen **Foreign trade mapping.xml**.</span><span class="sxs-lookup"><span data-stu-id="ca54e-127">Click **Browse** and select the **Foreign trade mapping.xml** file.</span></span> 
14. <span data-ttu-id="ca54e-128">Klikk på **OK**.</span><span class="sxs-lookup"><span data-stu-id="ca54e-128">Click **OK**.</span></span> 

## <a name="register-a-connected-application"></a><span data-ttu-id="ca54e-129">Registrere et tilkoblet program</span><span class="sxs-lookup"><span data-stu-id="ca54e-129">Register a connected application</span></span>
1. <span data-ttu-id="ca54e-130">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="ca54e-130">Close the page.</span></span> 
2. <span data-ttu-id="ca54e-131">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="ca54e-131">Close the page.</span></span> 
3. <span data-ttu-id="ca54e-132">Gå til **Alle arbeidsområder** > **Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="ca54e-132">Go to **All workspaces** > **Electronic reporting**.</span></span> 
4. <span data-ttu-id="ca54e-133">Klikk på **Tilkoblede programmer**.</span><span class="sxs-lookup"><span data-stu-id="ca54e-133">Click **Connected applications**.</span></span> 
5. <span data-ttu-id="ca54e-134">Kontroller at det konfigurerte programmet er basert på Azure, og at det er tilgjengelig for gjeldende RCS-bruker.</span><span class="sxs-lookup"><span data-stu-id="ca54e-134">Make sure that the configured application is Azure based and accessible for the current RCS user.</span></span> <span data-ttu-id="ca54e-135">Det kreves også at den gjeldende RCS-brukeren har tilgang til det valgte programmet og er registrert som en bruker av dette programmet, i en rolle som gir vedkommende tilgangsrettigheter til programmets metadata.</span><span class="sxs-lookup"><span data-stu-id="ca54e-135">It is also required that the current RCS user has access to the selected application and has been registered as a user of this application playing a role giving them privileges to access application's metadata.</span></span> 
6. <span data-ttu-id="ca54e-136">Klikk på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="ca54e-136">Click **New**.</span></span> 
7. <span data-ttu-id="ca54e-137">Skriv inn «MyConnectedApp» i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="ca54e-137">In the **Name** field, type 'MyConnectedApp'.</span></span> 
8. <span data-ttu-id="ca54e-138">I **Program**-feltet skriver du inn «https://mycompany.operations.dynamics.com».</span><span class="sxs-lookup"><span data-stu-id="ca54e-138">In the **Application** field, type 'https:// mycompany.operations.dynamics.com'.</span></span> 
9. <span data-ttu-id="ca54e-139">I **Leietaker**-feltet skriver du inn «mycompany.onmicrosoft.com».</span><span class="sxs-lookup"><span data-stu-id="ca54e-139">In the **Tenant** field, type 'mycompany.onmicrosoft.com'.</span></span> 
10. <span data-ttu-id="ca54e-140">Klikk på **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="ca54e-140">Click **Save**.</span></span> 
11. <span data-ttu-id="ca54e-141">Når du kontrollerer tilkoblingen til det konfigurerte programmet, klikker du på koblingen **Klikk her for å koble til det valgte eksterne programmet** på siden **Koble til eksternt program**.</span><span class="sxs-lookup"><span data-stu-id="ca54e-141">When you check connection to configured application, on the **Connect to remote application** page click **Click here to connect to selected remote application** link.</span></span> 
12. <span data-ttu-id="ca54e-142">Klikk på **Kontroller tilkobling**.</span><span class="sxs-lookup"><span data-stu-id="ca54e-142">Click **Check connection**.</span></span> 
13. <span data-ttu-id="ca54e-143">Klikk på **Lukk**.</span><span class="sxs-lookup"><span data-stu-id="ca54e-143">Click **Close**.</span></span> 
14. <span data-ttu-id="ca54e-144">Etter at valideringen av tilkoblingen har lykkes, oppdateres versjons- og leietakerdetaljene for det konfigurerte programmet i gjeldende rutenett.</span><span class="sxs-lookup"><span data-stu-id="ca54e-144">When the connection validation succeeded, version and tenant details will be updated for the configured application in the current grid.</span></span> 

## <a name="review-existing-model-mapping-configuration"></a><span data-ttu-id="ca54e-145">Se gjennom eksisterende modelltilordningskonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="ca54e-145">Review existing model mapping configuration</span></span>
1. <span data-ttu-id="ca54e-146">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="ca54e-146">Close the page.</span></span> 
2. <span data-ttu-id="ca54e-147">Klikk på **Rapporteringskonfigurasjoner**.</span><span class="sxs-lookup"><span data-stu-id="ca54e-147">Click **Reporting configurations**.</span></span> 
3. <span data-ttu-id="ca54e-148">Utvid **Utenrikshandelsmodell** i treet.</span><span class="sxs-lookup"><span data-stu-id="ca54e-148">In the tree, expand **Foreign trade model**.</span></span> 
4. <span data-ttu-id="ca54e-149">Velg **Utenrikshandelsmodell\Utenrikshandelstilordning** i treet.</span><span class="sxs-lookup"><span data-stu-id="ca54e-149">In the tree, select **Foreign trade model\Foreign trade mapping**.</span></span> 
5. <span data-ttu-id="ca54e-150">Utvid delen **Forutsetninger**.</span><span class="sxs-lookup"><span data-stu-id="ca54e-150">Expand the **Prerequisites** section.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="ca54e-151">Denne tilordningen henviser til metadatakonfigurasjonen for øyeblikket.</span><span class="sxs-lookup"><span data-stu-id="ca54e-151">Currently, this mapping refers to the metadata configuration.</span></span> <span data-ttu-id="ca54e-152">Programmetadata fra denne konfigurasjonen tilbys mens denne modelltilordningen utformes.</span><span class="sxs-lookup"><span data-stu-id="ca54e-152">Application metadata from this configuration will be offered while this model mapping will be designed.</span></span> 

6. <span data-ttu-id="ca54e-153">Klikk på **Utforming**.</span><span class="sxs-lookup"><span data-stu-id="ca54e-153">Click **Designer**.</span></span> 
7. <span data-ttu-id="ca54e-154">Klikk på **Utforming**.</span><span class="sxs-lookup"><span data-stu-id="ca54e-154">Click **Designer**.</span></span> 
8. <span data-ttu-id="ca54e-155">I treet velger du **Dynamics 365 for Operations\Tabellposter**.</span><span class="sxs-lookup"><span data-stu-id="ca54e-155">In the tree, select **Dynamics 365 for Operations\Table records**.</span></span> 
9. <span data-ttu-id="ca54e-156">Klikk på **Legg til rot**.</span><span class="sxs-lookup"><span data-stu-id="ca54e-156">Click **Add root**.</span></span> 
10. <span data-ttu-id="ca54e-157">Angi eller velg en verdi i **Tabell**-feltet.</span><span class="sxs-lookup"><span data-stu-id="ca54e-157">In the **Table** field, enter or select a value.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="ca54e-158">Denne tilordningen henviser til metadatakonfigurasjonen for øyeblikket.</span><span class="sxs-lookup"><span data-stu-id="ca54e-158">Currently, this mapping refers to the metadata configuration.</span></span> <span data-ttu-id="ca54e-159">Programmetadata fra denne konfigurasjonen tilbys mens denne modelltilordningen utformes.</span><span class="sxs-lookup"><span data-stu-id="ca54e-159">Application metadata from this configuration will be offered while this model mapping will be designed.</span></span> 

11. <span data-ttu-id="ca54e-160">Klikk på **Avbryt**.</span><span class="sxs-lookup"><span data-stu-id="ca54e-160">Click **Cancel**.</span></span> 
12. <span data-ttu-id="ca54e-161">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="ca54e-161">Close the page.</span></span> 
13. <span data-ttu-id="ca54e-162">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="ca54e-162">Close the page.</span></span> 

## <a name="assign-connected-application-to-model-mapping"></a><span data-ttu-id="ca54e-163">Tilordne tilkoblet program til modelltilordning</span><span class="sxs-lookup"><span data-stu-id="ca54e-163">Assign connected application to model mapping</span></span> 
1. <span data-ttu-id="ca54e-164">Klikk på **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="ca54e-164">Click **Edit**.</span></span> 
2. <span data-ttu-id="ca54e-165">Velg programmet **MyConnectedApp**.</span><span class="sxs-lookup"><span data-stu-id="ca54e-165">Select **MyConnectedApp** application.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="ca54e-166">Denne tilordningen henviser for øyeblikket til metadataene i det valgte tilkoblede programmet.</span><span class="sxs-lookup"><span data-stu-id="ca54e-166">Currently, this mapping refers to the metadata of the selected connected application.</span></span> <span data-ttu-id="ca54e-167">Når den samme tilordningen henviser til metadatakonfigurasjonen og det tilkoblede programmet samtidig, brukes metadata for det tilkoblede programmet.</span><span class="sxs-lookup"><span data-stu-id="ca54e-167">When the same mapping refers to metadata configuration and connected application at the same time, metadata of the connected application will be used.</span></span> 

3. <span data-ttu-id="ca54e-168">Klikk på **Utforming**.</span><span class="sxs-lookup"><span data-stu-id="ca54e-168">Click **Designer**.</span></span> 
4. <span data-ttu-id="ca54e-169">Klikk på **Utforming**.</span><span class="sxs-lookup"><span data-stu-id="ca54e-169">Click **Designer**.</span></span> 
5. <span data-ttu-id="ca54e-170">I treet velger du **Dynamics 365 for Operations\Tabellposter**.</span><span class="sxs-lookup"><span data-stu-id="ca54e-170">In the tree, select **Dynamics 365 for Operations\Table records**.</span></span> 
6. <span data-ttu-id="ca54e-171">Klikk på **Legg til rot**.</span><span class="sxs-lookup"><span data-stu-id="ca54e-171">Click **Add root**.</span></span> 
7. <span data-ttu-id="ca54e-172">Angi eller velg en verdi i **Tabell**-feltet.</span><span class="sxs-lookup"><span data-stu-id="ca54e-172">In the **Table** field, enter or select a value.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="ca54e-173">Nå ble flere enn to programtabeller tilbudt siden denne tilordningen bruker alle metadataene i det tilkoblede programmet som er tilordnet for den.</span><span class="sxs-lookup"><span data-stu-id="ca54e-173">More than two application tables were offered now as this mapping uses all the metadata of the connected application that has been assigned for it.</span></span> 

8. <span data-ttu-id="ca54e-174">Klikk på **Avbryt**.</span><span class="sxs-lookup"><span data-stu-id="ca54e-174">Click **Cancel**.</span></span> 
9. <span data-ttu-id="ca54e-175">Klikk på **Valider**.</span><span class="sxs-lookup"><span data-stu-id="ca54e-175">Click **Validate**.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="ca54e-176">Vi har bundet elementer i datamodellen til elementer i datakildene som er beskrevet, ved å bruke detaljer i metadata for det tilkoblede programmet som er tilordnet for denne tilordningen.</span><span class="sxs-lookup"><span data-stu-id="ca54e-176">We successfully bound elements of data model with items of data sources that are described by using details of metadata of the connected application that has been assigned for this mapping.</span></span> 

10. <span data-ttu-id="ca54e-177">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="ca54e-177">Close the page.</span></span> 
11. <span data-ttu-id="ca54e-178">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="ca54e-178">Close the page.</span></span> 

<span data-ttu-id="ca54e-179">Når du må evaluere denne modelltilordningen ved å bruke metadata for en annen versjon av programmet, registrerer du et nytt tilkoblet program, tilordner det til denne modelltilordningen og validerer det mot de nye metadataene.</span><span class="sxs-lookup"><span data-stu-id="ca54e-179">When you need to evaluate this model mapping by using metadata of a different version application, register another connected application, assign it to this model mapping and validate it against new metadata.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]