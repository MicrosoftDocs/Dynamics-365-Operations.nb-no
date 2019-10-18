---
title: Klargjøre programmetadataene som skal brukes i RCS
description: Trinnene i dette emnet forklarer hvordan en bruker kan opprette en ny ER-konfigurasjon (elektronisk rapportering) som inneholder programmetadata for utforming av ER-modelltilordningskonfigurasjoner i Regulatory Configuration Service (RCS).
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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e3a33eefca98e14ed0435f8f1a7a9f90a69498ee
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182169"
---
# <a name="prepare-application-metadata-to-be-used-in-rcs"></a><span data-ttu-id="6d9e5-103">Klargjøre programmetadataene som skal brukes i RCS</span><span class="sxs-lookup"><span data-stu-id="6d9e5-103">Prepare application metadata to be used in RCS</span></span>
[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6d9e5-104">Trinnene nedenfor forklarer hvordan en bruker i rollen Systemansvarlig eller Utvikler av elektronisk rapportering kan opprette en ny ER-konfigurasjon (elektronisk rapportering) som inneholder programmetadata for utforming av ER-modelltilordningskonfigurasjoner i Regulatory Configuration Service (RCS).</span><span class="sxs-lookup"><span data-stu-id="6d9e5-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains application metadata for designing ER model mapping configurations in Regulatory configuration service (RCS).</span></span> <span data-ttu-id="6d9e5-105">Denne konfigurasjonen brukes til å utforme et eksempel på ER-modelltilordningskonfigurasjon for å få tilgang til utenrikshandelstransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="6d9e5-105">This configuration will be used for designing a sample ER model mapping configuration to access foreign trade transactions.</span></span> <span data-ttu-id="6d9e5-106">I dette eksemplet skal du opprette en konfigurasjon for eksempelfirmaet Litware, Inc. Denne fremgangsmåten kan utføres i et hvilket som helst firma.</span><span class="sxs-lookup"><span data-stu-id="6d9e5-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in any company.</span></span> <span data-ttu-id="6d9e5-107">For å fullføre disse trinnene må du først fullføre trinnene i emnet [Opprette konfigurasjonsleverandører og merke dem som aktive](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="6d9e5-107">To complete these steps, you must first complete the steps in the topic, [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="6d9e5-108">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="6d9e5-108">Prerequisites</span></span>
1.  <span data-ttu-id="6d9e5-109">Gå til **Organisasjonsstyring** > **Arbeidsområder** > **Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="6d9e5-109">Go to **Organization administration** > **Workspaces** > **Electronic reporting**.</span></span> 
2.  <span data-ttu-id="6d9e5-110">Kontroller at konfigurasjonsleverandøren for eksempelfirmaet Litware, Inc. er tilgjengelig og merket som **Aktiv**.</span><span class="sxs-lookup"><span data-stu-id="6d9e5-110">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="6d9e5-111">Hvis du ikke ser denne konfigurasjonsleverandøren, må du fullføre trinnene i prosedyren [Opprette konfigurasjonsleverandører og merke dem som aktive](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="6d9e5-111">If you don’t see this configuration provider, complete the steps in the procedure [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> 
3.  <span data-ttu-id="6d9e5-112">Klikk på **Metadatakonfigurasjoner**.</span><span class="sxs-lookup"><span data-stu-id="6d9e5-112">Click **Metadata configurations**.</span></span> 
4.  <span data-ttu-id="6d9e5-113">Anta at RCS brukes til å utforme en ER-løsning for et Finance and Operations-program som skal brukes til å generere elektroniske dokumenter som inneholder informasjon fra forretningsdomenet for utenrikshandel.</span><span class="sxs-lookup"><span data-stu-id="6d9e5-113">Assume that RCS will be used to design an ER solution for a Finance and Operation application that will generate electronic documents that contain information from foreign trade business domain.</span></span> <span data-ttu-id="6d9e5-114">Hvis du vil angi tilordningen mellom ER-datamodell og kilder til nødvendige data, må vi ha tilgang til programmetadata for Finance and Operations-programmet i RCS.</span><span class="sxs-lookup"><span data-stu-id="6d9e5-114">To specify the mapping between ER data model and sources of required data, in RCS we need to have access to metadata of the Finance and Operation application.</span></span> <span data-ttu-id="6d9e5-115">Vi konfigurerer derfor en ny ER-metadatakonfigurasjon som en del av utformingen av ER-løsningen, og som inneholder alle metadataene som kreves for å generere ER-rapporter for det valgte forretningsdomenet.</span><span class="sxs-lookup"><span data-stu-id="6d9e5-115">Therefore, as part of designing ER solution we configure a new ER metadata configuration containing all metadata that is currently required for generation ER reports for selected business domain.</span></span> 

## <a name="add-metadata-configuration"></a><span data-ttu-id="6d9e5-116">Legge til metadatakonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="6d9e5-116">Add metadata configuration</span></span> 
1.  <span data-ttu-id="6d9e5-117">Klikk på **Opprett konfigurasjon** for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="6d9e5-117">Click **Create configuration** to open the drop dialog.</span></span> 
2.  <span data-ttu-id="6d9e5-118">I **Navn**-feltet skriver du inn «Metadata for utenrikshandel».</span><span class="sxs-lookup"><span data-stu-id="6d9e5-118">In the **Name** field, type 'Foreign trade metadata'.</span></span> 
3.  <span data-ttu-id="6d9e5-119">Klikk **Opprett konfigurasjon**.</span><span class="sxs-lookup"><span data-stu-id="6d9e5-119">Click **Create configuration**.</span></span> 
4.  <span data-ttu-id="6d9e5-120">Klikk **Utforming**.</span><span class="sxs-lookup"><span data-stu-id="6d9e5-120">Click **Designer**.</span></span> 
5.  <span data-ttu-id="6d9e5-121">Klikk **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="6d9e5-121">Click **Add**.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="6d9e5-122">Du kan velge alle metadataene for hele programmet eller valgte modeller eller moduler.</span><span class="sxs-lookup"><span data-stu-id="6d9e5-122">You can select all metadata for the entire application or selected models or selected modules.</span></span> <span data-ttu-id="6d9e5-123">Vær i dette tilfellet oppmerksom på at følgende metadata blir lagt til automatisk: tabeller med poster, opplistinger og utvidede datatyper.</span><span class="sxs-lookup"><span data-stu-id="6d9e5-123">Be aware that in this case the following metadata will be automatically added: tables of records, enumerations, and extended data types.</span></span> <span data-ttu-id="6d9e5-124">Når det er behov flere typer metadata, må de legges til manuelt.</span><span class="sxs-lookup"><span data-stu-id="6d9e5-124">When additional types of metadata are needed, they must be added manually.</span></span> 
 
<span data-ttu-id="6d9e5-125">Vi har enkelte metadata som er knyttet til utenrikshandelstransaksjoner, ved å velge metadataelementer manuelt.</span><span class="sxs-lookup"><span data-stu-id="6d9e5-125">We have some foreign trade transactions related metadata by selecting metadata items manually.</span></span> 
  
6.  <span data-ttu-id="6d9e5-126">Klikk på **Legg til datakilde**.</span><span class="sxs-lookup"><span data-stu-id="6d9e5-126">Click **Add data source**.</span></span> 
7.  <span data-ttu-id="6d9e5-127">Klikk på **Tabellposter**.</span><span class="sxs-lookup"><span data-stu-id="6d9e5-127">Click **Table records**.</span></span> 
8.  <span data-ttu-id="6d9e5-128">Bruk hurtigfilteret til å filtrere på **Navn**-feltet med verdien «Intrastat».</span><span class="sxs-lookup"><span data-stu-id="6d9e5-128">Use the Quick Filter to filter on the **Name** field with a value of 'Intrastat'.</span></span> 
9.  <span data-ttu-id="6d9e5-129">Velg **Intrastat**-tabellposten.</span><span class="sxs-lookup"><span data-stu-id="6d9e5-129">Select the **Intrastat** table record.</span></span> 
10. <span data-ttu-id="6d9e5-130">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="6d9e5-130">Click **OK**.</span></span>
  
<span data-ttu-id="6d9e5-131">Vi la til metadatainformasjon om Intrastat-tabellen med poster.</span><span class="sxs-lookup"><span data-stu-id="6d9e5-131">We added metadata information about the Intrastat table of records.</span></span> 
  
11. <span data-ttu-id="6d9e5-132">Utvid **Tabellposter Intrastat**\>**Relasjoner** i treet.</span><span class="sxs-lookup"><span data-stu-id="6d9e5-132">In the tree, expand **Table records Intrastat**\>**Relations**.</span></span> 
12. <span data-ttu-id="6d9e5-133">Velg **Tabellposter Intrastat**\>**Relasjoner\IntrastatCommodity (Tabellposter EcoResCategory)** i treet.</span><span class="sxs-lookup"><span data-stu-id="6d9e5-133">In the tree, select **Table records Intrastat**\>**Relations\IntrastatCommodity (Table records EcoResCategory)**.</span></span>   
13. <span data-ttu-id="6d9e5-134">Klikk på **Legg til metadata**.</span><span class="sxs-lookup"><span data-stu-id="6d9e5-134">Click **Add metadata**.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="6d9e5-135">Metadata om nødvendige relasjoner for den valgte tabellen med poster må legges til manuelt.</span><span class="sxs-lookup"><span data-stu-id="6d9e5-135">Metadata about required relations for selected table of records must be added manually.</span></span> 
  
16. <span data-ttu-id="6d9e5-136">Klikk på **Legg til datakilde**.</span><span class="sxs-lookup"><span data-stu-id="6d9e5-136">Click **Add data source**.</span></span> 
17. <span data-ttu-id="6d9e5-137">Klikk på **Opplisting**.</span><span class="sxs-lookup"><span data-stu-id="6d9e5-137">Click **Enumeration**.</span></span> 
18. <span data-ttu-id="6d9e5-138">Bruk hurtigfilteret til å filtrere på **Navn**-feltet med verdien «IntrastatDirection».</span><span class="sxs-lookup"><span data-stu-id="6d9e5-138">Use the Quick Filter to filter on the **Name** field with a value of 'IntrastatDirection'.</span></span> 
19. <span data-ttu-id="6d9e5-139">Velg posten **IntrastatDirection-opplisting**.</span><span class="sxs-lookup"><span data-stu-id="6d9e5-139">Select the **IntrastatDirection enumeration** record.</span></span> 
20. <span data-ttu-id="6d9e5-140">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="6d9e5-140">Click **OK**.</span></span> 
21. <span data-ttu-id="6d9e5-141">Klikk **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="6d9e5-141">Click **Save**.</span></span>  
22. <span data-ttu-id="6d9e5-142">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="6d9e5-142">Close the page.</span></span> 
  
## <a name="complete-the-draft-version-of-metadata-configuration"></a><span data-ttu-id="6d9e5-143">Fullføre kladdeversjonen av metadatakonfigurasjonen</span><span class="sxs-lookup"><span data-stu-id="6d9e5-143">Complete the draft version of metadata configuration</span></span>
1.  <span data-ttu-id="6d9e5-144">Klikk på **Endre status**.</span><span class="sxs-lookup"><span data-stu-id="6d9e5-144">Click **Change status**.</span></span> 
2.  <span data-ttu-id="6d9e5-145">Klikk på **Fullført**.</span><span class="sxs-lookup"><span data-stu-id="6d9e5-145">Click **Complete**.</span></span> 
3.  <span data-ttu-id="6d9e5-146">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="6d9e5-146">Click **OK**.</span></span> 
4.  <span data-ttu-id="6d9e5-147">Velg fullført versjon **1**.</span><span class="sxs-lookup"><span data-stu-id="6d9e5-147">Select the completed version **1**.</span></span> 
  
## <a name="export-the-completed-version-of-metadata-configuration-from-application-as-xml-file"></a><span data-ttu-id="6d9e5-148">Eksportere den fullførte versjonen av metadatakonfigurasjonen fra programmet som en XML-fil</span><span class="sxs-lookup"><span data-stu-id="6d9e5-148">Export the completed version of metadata configuration from application as XML file</span></span>
1.  <span data-ttu-id="6d9e5-149">Klikk på **Veksle**.</span><span class="sxs-lookup"><span data-stu-id="6d9e5-149">Click **Exchange**.</span></span> 
2.  <span data-ttu-id="6d9e5-150">Klikk på **Eksporter som XML-fil**.</span><span class="sxs-lookup"><span data-stu-id="6d9e5-150">Click **Export as XML file**.</span></span> 
3.  <span data-ttu-id="6d9e5-151">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="6d9e5-151">Click **OK**.</span></span> 
    
<span data-ttu-id="6d9e5-152">ER-metadatakonfigurasjonen har blitt lagret som en XML-fil som kan importeres til RCS og brukes som kilden til informasjon om metadata for forretningsdomenet for utenrikshandel.</span><span class="sxs-lookup"><span data-stu-id="6d9e5-152">The created ER metadata configuration has been saved as XML file that can be imported to RCS and used as the source of information about metadata for the foreign trade business domain.</span></span> <span data-ttu-id="6d9e5-153">Basert på denne informasjonen kan vi angi tilordningen mellom programmetadata og ER-datamodellen.</span><span class="sxs-lookup"><span data-stu-id="6d9e5-153">Based on this information, we can specify the mapping between application metadata and ER data model.</span></span>
