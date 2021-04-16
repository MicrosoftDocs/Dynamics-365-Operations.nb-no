---
title: Klargjøre programspesifikke metadata for RCS og ER
description: Dette emnet forklarer hvordan du klargjør programspesifikke metadata for Regulatory Configuration Service (RCS) og elektronisk rapportering (ER).
author: NickSelin
ms.date: 04/04/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: f0501fd67da0cbc5c10171b55004cb7f4fd4fd16
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5743709"
---
# <a name="prepare-application-specific-metadata-for-rcs-and-er"></a><span data-ttu-id="a3257-103">Klargjøre programspesifikke metadata for RCS og ER</span><span class="sxs-lookup"><span data-stu-id="a3257-103">Prepare application-specific metadata for RCS and ER</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="a3257-104">Dette emnet går gjennom eksempler på følgende oppgaver:</span><span class="sxs-lookup"><span data-stu-id="a3257-104">This topic walks you through examples of the following tasks:</span></span>

- [<span data-ttu-id="a3257-105">Klargjøre programmetadataene som kan brukes i RCS</span><span class="sxs-lookup"><span data-stu-id="a3257-105">Prepare application metadata that can be used in RCS</span></span>](#prepare-application-metadata-that-can-be-used-in-rcs)
- [<span data-ttu-id="a3257-106">Få tilgang til programmetadata ved hjelp av en ER-konfigurasjon</span><span class="sxs-lookup"><span data-stu-id="a3257-106">Access application metadata by using an ER configuration</span></span>](#access-application-metadata-by-using-an-er-configuration)
- [<span data-ttu-id="a3257-107">Få tilgang til programmetadata ved hjelp av tilkoblede programmer</span><span class="sxs-lookup"><span data-stu-id="a3257-107">Access application metadata by using connected applications</span></span>](#access-application-metadata-by-using-connected-applications)

## <a name="prepare-application-metadata-that-can-be-used-in-rcs"></a><span data-ttu-id="a3257-108">Klargjøre programmetadataene som kan brukes i RCS</span><span class="sxs-lookup"><span data-stu-id="a3257-108">Prepare application metadata that can be used in RCS</span></span>

<span data-ttu-id="a3257-109">Fremgangsmåten nedenfor viser hvordan en bruker som har rollen **Systemansvarlig** eller **Utvikler av elektronisk rapportering**, kan lage en ER-konfigurasjon (elektronisk rapportering) som inneholder metadata for programmet , og som brukes til å utforme ER-modelltilordningskonfigurasjoner i Regulatory Configuration Service (RCS).</span><span class="sxs-lookup"><span data-stu-id="a3257-109">The following procedure shows how a user who has the **System Administrator** or **Electronic Reporting Developer** role can create an Electronic reporting (ER) configuration that contains metadata for the application, and that is used to design ER model mapping configurations in Regulatory configuration service (RCS).</span></span> <span data-ttu-id="a3257-110">Eksemplet på ER-modelltilordningskonfigurasjon som lages i dette eksemplet, brukes til å få tilgang til utenrikshandelstransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="a3257-110">The sample ER model mapping configuration that is created in this example will be used to access foreign trade transactions.</span></span>

<span data-ttu-id="a3257-111">I dette eksemplet ønsker du å bruke RCS til å utforme en ER-løsning for programmet som skal brukes til å generere elektroniske dokumenter som inneholder informasjon fra forretningsdomenet for utenrikshandel.</span><span class="sxs-lookup"><span data-stu-id="a3257-111">For this example, you want to use RCS to design an ER solution for the application that will be used to generate electronic documents that contain information from the foreign trade business domain.</span></span> <span data-ttu-id="a3257-112">Hvis du vil angi tilordningen mellom ER-datamodellen og kildene til nødvendige data, må du ha tilgang til programmetadata i RCS.</span><span class="sxs-lookup"><span data-stu-id="a3257-112">To specify the mapping between the ER data model and the sources of required data, you must have access to application metadata in RCS.</span></span> <span data-ttu-id="a3257-113">Du må derfor konfigurere en ny ER-metadatakonfigurasjon som en del av utformingen av ER-løsningen, og som inneholder alle metadataene som kreves for å kunne generere ER-rapporter for det valgte forretningsdomenet.</span><span class="sxs-lookup"><span data-stu-id="a3257-113">Therefore, as part of the process of designing the ER solution, you must configure a new ER metadata configuration that contains all the metadata that is currently required in order to generate ER reports for the selected business domain.</span></span>

> [!NOTE]
> <span data-ttu-id="a3257-114">I dette eksemplet skal du opprette en konfigurasjon for eksempelfirmaet Litware, Inc. Denne fremgangsmåten kan utføres i et hvilket som helst firma.</span><span class="sxs-lookup"><span data-stu-id="a3257-114">In this example, you will create a configuration for the sample company, Litware, Inc. These steps can be performed in any company.</span></span>

1. <span data-ttu-id="a3257-115">Gå til **Organisasjonsstyring \> Arbeidsområder \> Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="a3257-115">Go to **Organization administration \> Workspaces \> Electronic reporting**.</span></span>
2. <span data-ttu-id="a3257-116">Kontroller at konfigurasjonsleverandøren for eksempelfirmaet Litware, Inc. er tilgjengelig og merket som **Aktiv**.</span><span class="sxs-lookup"><span data-stu-id="a3257-116">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="a3257-117">Hvis du ikke ser denne konfigurasjonsleverandøren, fullfører du fremgangsmåten [Opprette konfigurasjonsleverandører og merke dem som aktive](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="a3257-117">If you don't see this configuration provider, complete the [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure.</span></span> 
3. <span data-ttu-id="a3257-118">Velg **Metadatakonfigurasjoner**.</span><span class="sxs-lookup"><span data-stu-id="a3257-118">Select **Metadata configurations**.</span></span>
4. <span data-ttu-id="a3257-119">Velg **Opprett konfigurasjon**.</span><span class="sxs-lookup"><span data-stu-id="a3257-119">Select **Create configuration**.</span></span>
5. <span data-ttu-id="a3257-120">Skriv inn et navn i **Navn**-feltet i rullegardinboksen.</span><span class="sxs-lookup"><span data-stu-id="a3257-120">In the drop-down dialog box, in the **Name** field, enter a name.</span></span> <span data-ttu-id="a3257-121">I dette eksemplet angir du **Metadata for utenrikshandel**.</span><span class="sxs-lookup"><span data-stu-id="a3257-121">For this example, enter **Foreign trade metadata**.</span></span>
6. <span data-ttu-id="a3257-122">Velg **Opprett konfigurasjon**.</span><span class="sxs-lookup"><span data-stu-id="a3257-122">Select **Create configuration**.</span></span>
7. <span data-ttu-id="a3257-123">Velg **Utforming**.</span><span class="sxs-lookup"><span data-stu-id="a3257-123">Select **Designer**.</span></span>
8. <span data-ttu-id="a3257-124">Velg **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="a3257-124">Select **Add**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a3257-125">Du kan velge alle metadata for hele programmet eller for merkede modeller eller moduler.</span><span class="sxs-lookup"><span data-stu-id="a3257-125">You can select all metadata either for the whole application, or for selected models or modules.</span></span> <span data-ttu-id="a3257-126">I begge tilfeller må du være oppmerksom på at følgende metadata blir lagt til automatisk: tabeller med poster, opplistinger og utvidede datatyper (EDT-er).</span><span class="sxs-lookup"><span data-stu-id="a3257-126">In both cases, be aware that the following metadata will be automatically added: tables of records, enumerations, and extended data types (EDTs).</span></span> <span data-ttu-id="a3257-127">Når det kreves flere typer metadata, må de legges til manuelt.</span><span class="sxs-lookup"><span data-stu-id="a3257-127">When additional types of metadata are required, they must be manually added.</span></span>

    <span data-ttu-id="a3257-128">Du må legge til enkelte metadata som er knyttet til utenrikshandelstransaksjoner, og velge metadataelementer manuelt.</span><span class="sxs-lookup"><span data-stu-id="a3257-128">You must add some metadata that is related to foreign trade transactions and manually select metadata items.</span></span>

9. <span data-ttu-id="a3257-129">Velg **Legg til datakilde \> Tabellposter**.</span><span class="sxs-lookup"><span data-stu-id="a3257-129">Select **Add data source \> Table records**.</span></span>
10. <span data-ttu-id="a3257-130">Filtrer etter verdien **Intrastat** i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="a3257-130">Filter on a value of **Intrastat** in the **Name** field.</span></span>
11. <span data-ttu-id="a3257-131">Velg **Intrastat**-tabellposten.</span><span class="sxs-lookup"><span data-stu-id="a3257-131">Select the **Intrastat** table record.</span></span>
12. <span data-ttu-id="a3257-132">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="a3257-132">Select **OK**.</span></span>

    <span data-ttu-id="a3257-133">Du må legge til metadatainformasjon om Intrastat-tabellen med poster.</span><span class="sxs-lookup"><span data-stu-id="a3257-133">You must add metadata information about the Intrastat table of records.</span></span>

13. <span data-ttu-id="a3257-134">Velg **Tabellposter Intrastat \> \>Relasjoner \> IntrastatCommodity (Tabellposter EcoResCategory)** i treet.</span><span class="sxs-lookup"><span data-stu-id="a3257-134">In the tree, select **Table records Intrastat \> \>Relations \> IntrastatCommodity (Table records EcoResCategory)**.</span></span>
14. <span data-ttu-id="a3257-135">Velg **Legg til metadata**.</span><span class="sxs-lookup"><span data-stu-id="a3257-135">Select **Add metadata**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a3257-136">Metadata om nødvendige relasjoner for den valgte tabellen med poster må legges til manuelt.</span><span class="sxs-lookup"><span data-stu-id="a3257-136">Metadata about required relations for the selected table of records must be added manually.</span></span>

15. <span data-ttu-id="a3257-137">Velg **Legg til datakilde**.</span><span class="sxs-lookup"><span data-stu-id="a3257-137">Select **Add data source**.</span></span>
16. <span data-ttu-id="a3257-138">Velg **Opplisting**.</span><span class="sxs-lookup"><span data-stu-id="a3257-138">Select **Enumeration**.</span></span>
17. <span data-ttu-id="a3257-139">Filtrer etter verdien **IntrastatDirection** i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="a3257-139">Filter on a value of **IntrastatDirection** in the **Name** field.</span></span>
18. <span data-ttu-id="a3257-140">Velg opplistingsposten **IntrastatDirection**.</span><span class="sxs-lookup"><span data-stu-id="a3257-140">Select the **IntrastatDirection** enumeration record.</span></span>
19. <span data-ttu-id="a3257-141">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="a3257-141">Select **OK**.</span></span>
20. <span data-ttu-id="a3257-142">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="a3257-142">Select **Save**.</span></span>
21. <span data-ttu-id="a3257-143">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="a3257-143">Close the page.</span></span>
22. <span data-ttu-id="a3257-144">Fullfør kladdeversjonen av metadatakonfigurasjonen:</span><span class="sxs-lookup"><span data-stu-id="a3257-144">Complete the draft version of the metadata configuration:</span></span>

    1. <span data-ttu-id="a3257-145">Velg **Endre status \> Fullført**.</span><span class="sxs-lookup"><span data-stu-id="a3257-145">Select **Change status \> Complete**.</span></span>
    2. <span data-ttu-id="a3257-146">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="a3257-146">Select **OK**.</span></span>
    3. <span data-ttu-id="a3257-147">Velg fullført versjon 1.</span><span class="sxs-lookup"><span data-stu-id="a3257-147">Select the completed version 1.</span></span>

23. <span data-ttu-id="a3257-148">Eksporter den fullførte versjonen av metadatakonfigurasjonen fra programmet som en XML-fil:</span><span class="sxs-lookup"><span data-stu-id="a3257-148">Export the completed version of the metadata configuration from the application as an XML file:</span></span>

    1. <span data-ttu-id="a3257-149">Velg **Veksle \> Eksporter som XML-fil**.</span><span class="sxs-lookup"><span data-stu-id="a3257-149">Select **Exchange \> Export as XML file**.</span></span>
    2. <span data-ttu-id="a3257-150">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="a3257-150">Select **OK**.</span></span>

<span data-ttu-id="a3257-151">ER-metadatakonfigurasjonen du laget, lagres som filen **Foreign trade metadata.xml**.</span><span class="sxs-lookup"><span data-stu-id="a3257-151">The ER metadata configuration that you created is saved as the **Foreign trade metadata.xml** file.</span></span> <span data-ttu-id="a3257-152">Du kan nå importere den til RCS, slik at den kan brukes som kilden til metadata for forretningsdomenet for utenrikshandel.</span><span class="sxs-lookup"><span data-stu-id="a3257-152">You can now import it into RCS, so that it can be used as the source of metadata for the foreign trade business domain.</span></span> <span data-ttu-id="a3257-153">Basert på denne informasjonen kan du angi tilordningen mellom programmetadata og ER-datamodellen.</span><span class="sxs-lookup"><span data-stu-id="a3257-153">Based on this information, you can specify the mapping between application metadata and the ER data model.</span></span>

## <a name="access-application-metadata-by-using-an-er-configuration"></a><span data-ttu-id="a3257-154">Få tilgang til programmetadata ved hjelp av en ER-konfigurasjon</span><span class="sxs-lookup"><span data-stu-id="a3257-154">Access application metadata by using an ER configuration</span></span>

<span data-ttu-id="a3257-155">Fremgangsmåten nedenfor viser hvordan en RCS-bruker som har rollen **Systemansvarlig** eller **Utvikler av elektronisk rapportering**, kan utforme en ny ER-modelltilordning ved hjelp av metadata fra programmet.</span><span class="sxs-lookup"><span data-stu-id="a3257-155">The following procedure shows how an RCS user who has the **System Administrator** or **Electronic Reporting Developer** role can design a new ER model mapping by using metadata from the application.</span></span> <span data-ttu-id="a3257-156">Du får tilgang til programmetadata ved å bruke en ER-metadatakonfigurasjon som inneholder et eksempelsett med metadata som gir tilgang til utenrikshandelstransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="a3257-156">Application metadata will be accessed by using an ER metadata configuration that contains a sample set of metadata to access foreign trade transactions.</span></span>

<span data-ttu-id="a3257-157">Før du kan fullføre denne fremgangsmåten, må du først fullføre følgende fremgangsmåter:</span><span class="sxs-lookup"><span data-stu-id="a3257-157">Before you can complete this procedure, you must first complete the following procedures:</span></span>

- [<span data-ttu-id="a3257-158">Opprette konfigurasjonsleverandører og merke dem som aktive</span><span class="sxs-lookup"><span data-stu-id="a3257-158">Create configuration providers and mark them as active</span></span>](tasks/er-configuration-provider-mark-it-active-2016-11.md)
- [<span data-ttu-id="a3257-159">Klargjøre programmetadataene som kan brukes i RCS</span><span class="sxs-lookup"><span data-stu-id="a3257-159">Prepare application metadata that can be used in RCS</span></span>](#prepare-application-metadata-that-can-be-used-in-rcs)

1. <span data-ttu-id="a3257-160">Gå til **Alle arbeidsområder \> Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="a3257-160">Go to **All workspaces \> Electronic reporting**.</span></span>
2. <span data-ttu-id="a3257-161">Kontroller at konfigurasjonsleverandøren for eksempelfirmaet Litware, Inc. er tilgjengelig og merket som **Aktiv**.</span><span class="sxs-lookup"><span data-stu-id="a3257-161">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="a3257-162">Hvis du ikke ser denne konfigurasjonsleverandøren, fullfører du fremgangsmåten [Opprette konfigurasjonsleverandører og merke dem som aktive](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="a3257-162">If you don't see this configuration provider, complete the [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure.</span></span> 
3. <span data-ttu-id="a3257-163">Importer ER-metadatakonfigurasjonen som inneholder metadata for programmet, og som er konfigurert slik at elektroniske dokumenter genereres for det utenlandske forretningsdomenet.</span><span class="sxs-lookup"><span data-stu-id="a3257-163">Import the ER metadata configuration that contains metadata for the application, and that is configured to generate electronic documents for the foreign trade business domain.</span></span> <span data-ttu-id="a3257-164">Du laget denne ER-metadatakonfigurasjonen og eksporterte den som en XML-fil i fremgangsmåten [Klargjøre programmetadataene som kan brukes i RCS](#prepare-application-metadata-that-can-be-used-in-rcs) tidligere i dette emnet.</span><span class="sxs-lookup"><span data-stu-id="a3257-164">You created this ER metadata configuration and exported it as an XML file in the [Prepare application metadata that can be used in RCS](#prepare-application-metadata-that-can-be-used-in-rcs) procedure earlier in this topic.</span></span>

    1. <span data-ttu-id="a3257-165">Velg **Metadatakonfigurasjoner**.</span><span class="sxs-lookup"><span data-stu-id="a3257-165">Select **Metadata configurations**.</span></span>
    2. <span data-ttu-id="a3257-166">Velg **Veksle**.</span><span class="sxs-lookup"><span data-stu-id="a3257-166">Select **Exchange**.</span></span>
    3. <span data-ttu-id="a3257-167">Velg **Last fra XML-fil**.</span><span class="sxs-lookup"><span data-stu-id="a3257-167">Select **Load from XML file**.</span></span>
    4. <span data-ttu-id="a3257-168">Bla gjennom for å velge filen **Foreign trade metadata.xml**.</span><span class="sxs-lookup"><span data-stu-id="a3257-168">Browse to select the **Foreign trade metadata.xml** file.</span></span>
    5. <span data-ttu-id="a3257-169">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="a3257-169">Select **OK**.</span></span>
    6. <span data-ttu-id="a3257-170">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="a3257-170">Close the page.</span></span>

4. <span data-ttu-id="a3257-171">Opprett en datamodellkonfigurasjon:</span><span class="sxs-lookup"><span data-stu-id="a3257-171">Create a data model configuration:</span></span>

    1. <span data-ttu-id="a3257-172">Velg **Rapporteringskonfigurasjoner**.</span><span class="sxs-lookup"><span data-stu-id="a3257-172">Select **Reporting configurations**.</span></span>
    2. <span data-ttu-id="a3257-173">Velg **Opprett konfigurasjon**.</span><span class="sxs-lookup"><span data-stu-id="a3257-173">Select **Create configuration**.</span></span>
    3. <span data-ttu-id="a3257-174">Skriv inn **Utenrikshandelsmodell** i **Navn**-feltet i rullegardinboksen.</span><span class="sxs-lookup"><span data-stu-id="a3257-174">In the drop-down dialog box, in the **Name** field, enter **Foreign trade model**.</span></span>
    4. <span data-ttu-id="a3257-175">Velg **Opprett konfigurasjon**.</span><span class="sxs-lookup"><span data-stu-id="a3257-175">Select **Create configuration**.</span></span>
    5. <span data-ttu-id="a3257-176">Velg **Utforming**.</span><span class="sxs-lookup"><span data-stu-id="a3257-176">Select **Designer**.</span></span>
    6. <span data-ttu-id="a3257-177">Velg **Ny** for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="a3257-177">Select **New** to open the drop dialog.</span></span>

        1. <span data-ttu-id="a3257-178">Skriv inn **Rot** i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="a3257-178">In the **Name** field, type **Root**.</span></span>
        2. <span data-ttu-id="a3257-179">Velg **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="a3257-179">Select **Add**.</span></span>
    
    7. <span data-ttu-id="a3257-180">Velg **Ny** for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="a3257-180">Select **New** to open the drop dialog.</span></span>

        1. <span data-ttu-id="a3257-181">Skriv inn **Transaksjon** i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="a3257-181">In the **Name** field, type **Transaction**.</span></span>
        2. <span data-ttu-id="a3257-182">Velg **Postliste** i **Varetype**-feltet.</span><span class="sxs-lookup"><span data-stu-id="a3257-182">In the **Item type** field, select **Record list**.</span></span>
        3. <span data-ttu-id="a3257-183">Velg **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="a3257-183">Select **Add**.</span></span>
 
    8. <span data-ttu-id="a3257-184">Velg **Ny** for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="a3257-184">Select **New** to open the drop dialog.</span></span>

        1. <span data-ttu-id="a3257-185">I **Navn**-feltet skriver du inn **Artikkelkode**.</span><span class="sxs-lookup"><span data-stu-id="a3257-185">In the **Name** field, type **Commodity code**.</span></span>
        2. <span data-ttu-id="a3257-186">Velg **Streng** i **Varetype**-feltet.</span><span class="sxs-lookup"><span data-stu-id="a3257-186">In the **Item type** field, select **String**.</span></span>
        3. <span data-ttu-id="a3257-187">Velg **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="a3257-187">Select **Add**.</span></span>

    9. <span data-ttu-id="a3257-188">Velg **Ny** for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="a3257-188">Select **New** to open the drop dialog.</span></span>

        1. <span data-ttu-id="a3257-189">Skriv inn **Fakturert beløp** i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="a3257-189">In the Name field, type **Invoiced amount**.</span></span>
        2. <span data-ttu-id="a3257-190">Velg **Faktisk** i **Varetype**-feltet.</span><span class="sxs-lookup"><span data-stu-id="a3257-190">In the **Item type** field, select **Real**.</span></span>
        3. <span data-ttu-id="a3257-191">Velg **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="a3257-191">Select **Add**.</span></span>

    10. <span data-ttu-id="a3257-192">Velg **Ny** for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="a3257-192">Select **New** to open the drop dialog.</span></span>

        1. <span data-ttu-id="a3257-193">Skriv inn **Dato** i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="a3257-193">In the **Name** field, type **Date**.</span></span>
        2. <span data-ttu-id="a3257-194">Velg **Dato** i **Varetype**-feltet.</span><span class="sxs-lookup"><span data-stu-id="a3257-194">In the **Item type** field, select **Date**.</span></span>
        3. <span data-ttu-id="a3257-195">Velg **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="a3257-195">Select **Add**.</span></span>
 
    11. <span data-ttu-id="a3257-196">Velg **Legg til \> Rotreferanse**.</span><span class="sxs-lookup"><span data-stu-id="a3257-196">Select **Add \> Root reference**.</span></span>
    12. <span data-ttu-id="a3257-197">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="a3257-197">Select **OK**.</span></span>
    13. <span data-ttu-id="a3257-198">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="a3257-198">Select **Save**.</span></span>
    14. <span data-ttu-id="a3257-199">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="a3257-199">Close the page.</span></span>
    15. <span data-ttu-id="a3257-200">Velg **Endre status \> Fullført**.</span><span class="sxs-lookup"><span data-stu-id="a3257-200">Select **Change status \> Complete**.</span></span>
    16. <span data-ttu-id="a3257-201">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="a3257-201">Select **OK**.</span></span>

5. <span data-ttu-id="a3257-202">Opprett en modelltilordningskonfigurasjon:</span><span class="sxs-lookup"><span data-stu-id="a3257-202">Create a model mapping configuration:</span></span>

    1. <span data-ttu-id="a3257-203">Velg **Opprett konfigurasjon**.</span><span class="sxs-lookup"><span data-stu-id="a3257-203">Select **Create configuration**.</span></span>
    2. <span data-ttu-id="a3257-204">I **Ny**-feltet i rullegardinboksen skriver du inn **Modelltilordning basert på datamodellen Utenrikshandelsmodell**.</span><span class="sxs-lookup"><span data-stu-id="a3257-204">In the drop-down dialog box, in the **New** field, enter **Model Mapping based on data model Foreign trade model**.</span></span>
    3. <span data-ttu-id="a3257-205">I **Navn**-feltet angir du **Utenrikshandelstilordning**.</span><span class="sxs-lookup"><span data-stu-id="a3257-205">In the **Name** field, enter **Foreign trade mapping**.</span></span>
    4. <span data-ttu-id="a3257-206">Velg **Opprett konfigurasjon**.</span><span class="sxs-lookup"><span data-stu-id="a3257-206">Select **Create configuration**.</span></span>
    5. <span data-ttu-id="a3257-207">Velg **Rediger** i hurtigfanen **Forutsetninger**.</span><span class="sxs-lookup"><span data-stu-id="a3257-207">On the **Prerequisites** FastTab, select **Edit**.</span></span>
    6. <span data-ttu-id="a3257-208">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="a3257-208">Select **New**.</span></span>
    7. <span data-ttu-id="a3257-209">Velg **Konfigurasjon** i feltet **Nødvendig komponenttype**.</span><span class="sxs-lookup"><span data-stu-id="a3257-209">In the **Prerequisite component type** field, select **Configuration**.</span></span>
    8. <span data-ttu-id="a3257-210">Velg konfigurasjonen **Metadata for utenrikshandel**.</span><span class="sxs-lookup"><span data-stu-id="a3257-210">Select the **Foreign trade metadata** configuration.</span></span>
    9. <span data-ttu-id="a3257-211">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="a3257-211">Select **Save**.</span></span> <span data-ttu-id="a3257-212">Legg merke til at referansen er lagt til i versjon 1 av konfigurasjonen **Metadata for utenrikshandel**.</span><span class="sxs-lookup"><span data-stu-id="a3257-212">Notice that the reference is added to version 1 of the **Foreign trade metadata** configuration.</span></span> <span data-ttu-id="a3257-213">Programmetadata fra denne konfigurasjonen tilbys når modelltilordningen er utformet.</span><span class="sxs-lookup"><span data-stu-id="a3257-213">Application metadata from this configuration will be offered while the model mapping is designed.</span></span>
    10. <span data-ttu-id="a3257-214">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="a3257-214">Close the page.</span></span>
    11. <span data-ttu-id="a3257-215">Velg **Utforming**.</span><span class="sxs-lookup"><span data-stu-id="a3257-215">Select **Designer**.</span></span>
    12. <span data-ttu-id="a3257-216">Velg **Utforming**.</span><span class="sxs-lookup"><span data-stu-id="a3257-216">Select **Designer**.</span></span>
    13. <span data-ttu-id="a3257-217">Velg **Dynamics 365 for Operations \> Tabellposter** i treet.</span><span class="sxs-lookup"><span data-stu-id="a3257-217">In the tree, select **Dynamics 365 for Operations \> Table records**.</span></span>
    14. <span data-ttu-id="a3257-218">Velg **Legg til rot**.</span><span class="sxs-lookup"><span data-stu-id="a3257-218">Select **Add root**.</span></span>
    15. <span data-ttu-id="a3257-219">Angi **Intrastat** i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="a3257-219">In the **Name** field, enter **Intrastat**.</span></span>
    16. <span data-ttu-id="a3257-220">Velg **Intrastat**-tabellposter.</span><span class="sxs-lookup"><span data-stu-id="a3257-220">Select **Intrastat** table records.</span></span>
    17. <span data-ttu-id="a3257-221">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="a3257-221">Select **OK**.</span></span>

        > [!NOTE]
        > <span data-ttu-id="a3257-222">Bare to tabeller tilbys, fordi bare to tabeller ble lagt til i settet med metadata som brukes for øyeblikket.</span><span class="sxs-lookup"><span data-stu-id="a3257-222">Only two tables are offered, because only two tables were added to the set of metadata that is currently used.</span></span>

    18. <span data-ttu-id="a3257-223">Velg **Bind**.</span><span class="sxs-lookup"><span data-stu-id="a3257-223">Select **Bind**.</span></span>
    19. <span data-ttu-id="a3257-224">Velg **Intrastat \> AmountMST** i treet.</span><span class="sxs-lookup"><span data-stu-id="a3257-224">In the tree, select **Intrastat \> AmountMST**.</span></span>
    20. <span data-ttu-id="a3257-225">Velg **Transaksjon = Intrastat \> Fakturert beløp** i treet.</span><span class="sxs-lookup"><span data-stu-id="a3257-225">In the tree, select **Transaction = Intrastat \> Invoiced amount**.</span></span>
    21. <span data-ttu-id="a3257-226">Velg **Bind**.</span><span class="sxs-lookup"><span data-stu-id="a3257-226">Select **Bind**.</span></span>
    22. <span data-ttu-id="a3257-227">Velg **Intrastat \> TransDate** i treet.</span><span class="sxs-lookup"><span data-stu-id="a3257-227">In the tree, select **Intrastat \> TransDate**.</span></span>
    23. <span data-ttu-id="a3257-228">Velg **Transaksjon = Intrastat \> Dato** i treet.</span><span class="sxs-lookup"><span data-stu-id="a3257-228">In the tree, select **Transaction = Intrastat \> Date**.</span></span>
    24. <span data-ttu-id="a3257-229">Velg **Bind**.</span><span class="sxs-lookup"><span data-stu-id="a3257-229">Select **Bind**.</span></span>
    25. <span data-ttu-id="a3257-230">Velg **Intrastat \> \>Relasjoner \> IntrastatCommodity \> Kode** i treet.</span><span class="sxs-lookup"><span data-stu-id="a3257-230">In the tree, select **Intrastat \> \>Relations \> IntrastatCommodity \> Code**.</span></span>
    26. <span data-ttu-id="a3257-231">Velg **Transaksjon = Intrastat \> Artikkelkode** i treet.</span><span class="sxs-lookup"><span data-stu-id="a3257-231">In the tree, select **Transaction = Intrastat \> Commodity code**.</span></span>
    27. <span data-ttu-id="a3257-232">Velg **Bind**.</span><span class="sxs-lookup"><span data-stu-id="a3257-232">Select **Bind**.</span></span>
    28. <span data-ttu-id="a3257-233">Velg **Valider**.</span><span class="sxs-lookup"><span data-stu-id="a3257-233">Select **Validate**.</span></span>

        > [!NOTE]
        > <span data-ttu-id="a3257-234">Etter at valideringen er fullført, har du bundet elementer i datamodellen til elementer i datakildene som er beskrevet, ved å bruke detaljer i programmetadataene fra ER-metadatakonfigurasjonen det henvises til.</span><span class="sxs-lookup"><span data-stu-id="a3257-234">After validation is completed, you've successfully bound elements of the data model to items of the data sources that are described by using details of the application metadata from the referenced ER metadata configuration.</span></span>

    29. <span data-ttu-id="a3257-235">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="a3257-235">Select **Save**.</span></span>

<span data-ttu-id="a3257-236">Du kan utvide det eksisterende settet med metadata i programmet etter behov.</span><span class="sxs-lookup"><span data-stu-id="a3257-236">As you require, you can extend the existing set of metadata in the application.</span></span> <span data-ttu-id="a3257-237">Du kan deretter eksportere den nye, fullførte versjonen av ER-metadatakonfigurasjonen, importere den til RCS og oppdatere forutsetningene for den konfigurerte modelltilordningskonfigurasjon slik at den henviser til en ny versjon av den importerte metadatakonfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="a3257-237">You can then export the new completed version of the ER metadata configuration, import it into RCS, and update the prerequisites of the configured model mapping configuration to refer to a new version of the imported metadata configuration.</span></span>

> [!NOTE]
> <span data-ttu-id="a3257-238">Denne metoden for å hente informasjon om programmetadata er den eneste tilgjengelige metoden for programmer som er distribuert lokalt (det vil si når lokale forretningsdata \[LBD\] eller en lokal distribusjonsmodell brukes til programmet).</span><span class="sxs-lookup"><span data-stu-id="a3257-238">This method for getting information about application metadata is the only available method for applications that are locally deployed (that is, when a local business data \[LBD\], or on-premises, deployment model is used for the application).</span></span>

## <a name="access-application-metadata-by-using-connected-applications"></a><span data-ttu-id="a3257-239">Få tilgang til programmetadata ved hjelp av tilkoblede programmer</span><span class="sxs-lookup"><span data-stu-id="a3257-239">Access application metadata by using connected applications</span></span>

<span data-ttu-id="a3257-240">Fremgangsmåten nedenfor viser hvordan en RCS-bruker som har rollen **Systemansvarlig** eller **Utvikler av elektronisk rapportering**, kan utforme en ny ER-modelltilordning ved hjelp av metadata for programmet.</span><span class="sxs-lookup"><span data-stu-id="a3257-240">The following procedure shows how an RCS user who has the **System Administrator** or **Electronic Reporting Developer** role can design a new ER model mapping by using metadata of the application.</span></span> <span data-ttu-id="a3257-241">Du får tilgang til programmetadata på nettet ved å bruke et RCS-tilkoblet program.</span><span class="sxs-lookup"><span data-stu-id="a3257-241">Application metadata will be accessed online by using RCS connected application.</span></span> <span data-ttu-id="a3257-242">Et ER-modelltilordningseksempel blir konfigurert for å gi tilgang til utenrikshandelstransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="a3257-242">A sample ER model mapping will be configured to access foreign trade transactions.</span></span>

<span data-ttu-id="a3257-243">For å kunne fullføre denne fremgangsmåten må du først fullføre fremgangsmåten [Opprette konfigurasjonsleverandører og merke dem som aktive](tasks/er-configuration-provider-mark-it-active-2016-11.md) i RCS.</span><span class="sxs-lookup"><span data-stu-id="a3257-243">To complete this procedure, you must first complete the [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure in RCS.</span></span> <span data-ttu-id="a3257-244">Hvis du ikke har fullført fremgangsmåten [Få tilgang til programmetadata ved hjelp av en ER-konfigurasjon](#access-application-metadata-by-using-an-er-configuration) tidligere i dette emnet ennå, går du til siden [Oppgaveveiledninger for elektronisk rapportering for Dynamics 365 for Finance and Operations 8.1](https://go.microsoft.com/fwlink/?linkid=2082739) for å laste ned følgende ER-konfigurasjonsfiler på forhånd og lagre dem lokalt: **Foreign trade metadata.xml**, **Foreign trade model.xml** og **Foreign trade mapping.xml**.</span><span class="sxs-lookup"><span data-stu-id="a3257-244">If you haven't yet completed the [Access application metadata by using an ER configuration](#access-application-metadata-by-using-an-er-configuration) procedure earlier in this topic, go to [Electronic Reporting Task Guides for Dynamics 365 for Finance and Operations 8.1](https://go.microsoft.com/fwlink/?linkid=2082739) page to download the following ER configuration files in advance and save them locally: **Foreign trade metadata.xml**, **Foreign trade model.xml**, and **Foreign trade mapping.xml**.</span></span>


### <a name="get-required-er-configurations"></a><span data-ttu-id="a3257-245">Hente nødvendige ER-konfigurasjoner</span><span class="sxs-lookup"><span data-stu-id="a3257-245">Get required ER configurations</span></span>

<span data-ttu-id="a3257-246">Hvis du allerede har fullført fremgangsmåten [Få tilgang til programmetadata ved hjelp av en ER-konfigurasjon](#access-application-metadata-by-using-an-er-configuration) tidligere i dette emnet, har du allerede alle nødvendige ER-konfigurasjoner (konfigurasjonene for metadata, modell og tilordning for utenrikshandel) i gjeldende RCS-forekomst.</span><span class="sxs-lookup"><span data-stu-id="a3257-246">If you've already completed the [Access application metadata by using an ER configuration](#access-application-metadata-by-using-an-er-configuration) procedure earlier in this topic, you already have all the required ER configurations (the foreign trade metadata, model, and mapping configurations) in the current RCS instance.</span></span> <span data-ttu-id="a3257-247">I så fall kan du hoppe over denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="a3257-247">In that case, you can skip this procedure.</span></span>

1. <span data-ttu-id="a3257-248">Gå til **Alle arbeidsområder \> Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="a3257-248">Go to **All workspaces \> Electronic reporting**.</span></span>
2. <span data-ttu-id="a3257-249">Velg **Rapporteringskonfigurasjoner**.</span><span class="sxs-lookup"><span data-stu-id="a3257-249">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="a3257-250">Last inn konfigurasjonsfilene **Foreign trade metadata.xml**, **Foreign trade model.xml** og **Foreign trade mapping.xml**, og gjenta følgende fremgangsmåten for hver av dem:</span><span class="sxs-lookup"><span data-stu-id="a3257-250">Load the **Foreign trade metadata.xml**, **Foreign trade model.xml**, and **Foreign trade mapping.xml** configuration files repeating the following chain of steps for each of them:</span></span>

    1. <span data-ttu-id="a3257-251">Velg **Veksle**.</span><span class="sxs-lookup"><span data-stu-id="a3257-251">Select **Exchange**.</span></span>
    2. <span data-ttu-id="a3257-252">Velg **Last fra XML-fil**.</span><span class="sxs-lookup"><span data-stu-id="a3257-252">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="a3257-253">Velg **Bla gjennom** og velg en fil.</span><span class="sxs-lookup"><span data-stu-id="a3257-253">Select **Browse**, and select a file.</span></span>
    4. <span data-ttu-id="a3257-254">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="a3257-254">Select **OK**.</span></span>

### <a name="register-the-connection-with-the-application"></a><span data-ttu-id="a3257-255">Registrere tilkoblingen til programmet</span><span class="sxs-lookup"><span data-stu-id="a3257-255">Register the connection with the application</span></span>

1. <span data-ttu-id="a3257-256">Gå til **Alle arbeidsområder \> Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="a3257-256">Go to **All workspaces \> Electronic reporting**.</span></span>
2. <span data-ttu-id="a3257-257">Velg **Tilkoblede programmer**.</span><span class="sxs-lookup"><span data-stu-id="a3257-257">Select **Connected applications**.</span></span>
3. <span data-ttu-id="a3257-258">Kontroller at det konfigurerte programmet er basert på Microsoft Azure, og at det er tilgjengelig generelt for RCS-brukere.</span><span class="sxs-lookup"><span data-stu-id="a3257-258">Make sure that the configured application is based on Microsoft Azure, and that it is accessible in general to RCS users.</span></span> <span data-ttu-id="a3257-259">Den gjeldende RCS-brukeren må ha tilgang til det konfigurerte programmet som registreres som en bruker av dette programmet, i en rolle som gir vedkommende tilgangsrettigheter til programmets metadata.</span><span class="sxs-lookup"><span data-stu-id="a3257-259">The current RCS user must have access to the configured application being registered as a user of this application in a role that gives them privileges to access the application's metadata.</span></span>
4. <span data-ttu-id="a3257-260">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="a3257-260">Select **New**.</span></span>
5. <span data-ttu-id="a3257-261">I **Navn**-feltet angir du **MyConnectedApp** som navnet på det tilkoblede programmet.</span><span class="sxs-lookup"><span data-stu-id="a3257-261">In the **Name** field, enter **MyConnectedApp** as the name of the connected application.</span></span>
6. <span data-ttu-id="a3257-262">I **Program**-feltet angir du URL-adressen til programmet.</span><span class="sxs-lookup"><span data-stu-id="a3257-262">In the **Application** field, specify the URL of the application.</span></span>
7. <span data-ttu-id="a3257-263">I **Leietaker**-feltet angir du leverandøren av programmet.</span><span class="sxs-lookup"><span data-stu-id="a3257-263">In the **Tenant** field, specify the provider of the application.</span></span>
8. <span data-ttu-id="a3257-264">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="a3257-264">Select **Save**.</span></span> 
9. <span data-ttu-id="a3257-265">Når du kontrollerer tilkoblingen til det konfigurerte programmet, velger du koblingen **Klikk her for å koble til det valgte eksterne programmet** på siden **Koble til eksternt program**.</span><span class="sxs-lookup"><span data-stu-id="a3257-265">When you check the connection to the configured application, on the **Connect to remote application** page, select the **Select here to connect to selected remote application** link.</span></span> 
10. <span data-ttu-id="a3257-266">Velg **Kontroller tilkobling** for å validere tilgang til det konfigurerte programmet.</span><span class="sxs-lookup"><span data-stu-id="a3257-266">Select **Check connection** to validate access to the configured application.</span></span>
11. <span data-ttu-id="a3257-267">Velg **Lukk**.</span><span class="sxs-lookup"><span data-stu-id="a3257-267">Select **Close**.</span></span>

<span data-ttu-id="a3257-268">Etter at du har fullført denne fremgangsmåten og valideringen av tilkoblingen har lykkes, oppdateres versjons- og leietakerdetaljene for det konfigurerte programmet i gjeldende rutenett.</span><span class="sxs-lookup"><span data-stu-id="a3257-268">After you complete this procedure and validation of the connection succeeds, the version and tenant details for the configured application will be updated in the current grid.</span></span>

### <a name="review-the-existing-model-mapping-configuration"></a><span data-ttu-id="a3257-269">Se gjennom den eksisterende modelltilordningskonfigurasjonen</span><span class="sxs-lookup"><span data-stu-id="a3257-269">Review the existing model mapping configuration</span></span>

1. <span data-ttu-id="a3257-270">Gå til **Alle arbeidsområder \> Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="a3257-270">Go to **All workspaces \> Electronic reporting**.</span></span>
2. <span data-ttu-id="a3257-271">Velg **Rapporteringskonfigurasjoner**.</span><span class="sxs-lookup"><span data-stu-id="a3257-271">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="a3257-272">Velg **Utenrikshandelsmodell \> Utenrikshandelstilordning** i treet.</span><span class="sxs-lookup"><span data-stu-id="a3257-272">In the tree, select **Foreign trade model \> Foreign trade mapping**.</span></span>
4. <span data-ttu-id="a3257-273">Velg hurtigfanen **Forutsetninger**.</span><span class="sxs-lookup"><span data-stu-id="a3257-273">Select the **Prerequisites** FasTab.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a3257-274">Denne tilordningen henviser til metadatakonfigurasjonen for øyeblikket.</span><span class="sxs-lookup"><span data-stu-id="a3257-274">Currently, this mapping refers to the metadata configuration.</span></span> <span data-ttu-id="a3257-275">Programmetadata fra denne konfigurasjonen tilbys når denne modelltilordningen er utformet.</span><span class="sxs-lookup"><span data-stu-id="a3257-275">Application metadata from this configuration will be offered while this model mapping is designed.</span></span>

4. <span data-ttu-id="a3257-276">Velg **Utforming**.</span><span class="sxs-lookup"><span data-stu-id="a3257-276">Select **Designer**.</span></span>
5. <span data-ttu-id="a3257-277">Velg **Utforming**.</span><span class="sxs-lookup"><span data-stu-id="a3257-277">Select **Designer**.</span></span>
6. <span data-ttu-id="a3257-278">Velg **Dynamics 365 for Operations \> Tabellposter** i treet.</span><span class="sxs-lookup"><span data-stu-id="a3257-278">In the tree, select **Dynamics 365 for Operations \> Table records**.</span></span>
7. <span data-ttu-id="a3257-279">Velg **Legg til rot**.</span><span class="sxs-lookup"><span data-stu-id="a3257-279">Select **Add root**.</span></span>
8. <span data-ttu-id="a3257-280">Angi eller velg en verdi i **Tabell**-feltet.</span><span class="sxs-lookup"><span data-stu-id="a3257-280">In the **Table** field, enter or select a value.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a3257-281">Denne tilordningen henviser til metadatakonfigurasjonen for øyeblikket.</span><span class="sxs-lookup"><span data-stu-id="a3257-281">Currently, this mapping refers to the metadata configuration.</span></span> <span data-ttu-id="a3257-282">Programmetadata fra denne konfigurasjonen tilbys når denne modelltilordningen er utformet.</span><span class="sxs-lookup"><span data-stu-id="a3257-282">Application metadata from this configuration will be offered while this model mapping is designed.</span></span>

9. <span data-ttu-id="a3257-283">Velg **Avbryt**.</span><span class="sxs-lookup"><span data-stu-id="a3257-283">Select **Cancel**.</span></span>

### <a name="assign-the-connected-application-to-a-model-mapping"></a><span data-ttu-id="a3257-284">Tilordne det tilkoblede programmet til en modelltilordning</span><span class="sxs-lookup"><span data-stu-id="a3257-284">Assign the connected application to a model mapping</span></span>

1. <span data-ttu-id="a3257-285">Velg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="a3257-285">Select **Edit**.</span></span>
2. <span data-ttu-id="a3257-286">Velg programmet **MyConnectedApp** i feltet **Tilkoblet program**.</span><span class="sxs-lookup"><span data-stu-id="a3257-286">In the **Connected application field**, select the **MyConnectedApp** application.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a3257-287">Denne tilordningen henviser til metadataene i det valgte tilkoblede programmet.</span><span class="sxs-lookup"><span data-stu-id="a3257-287">This mapping refers to the metadata of the selected connected application.</span></span> <span data-ttu-id="a3257-288">Hvis en tilordning henviser til metadatakonfigurasjonen og det tilkoblede programmet samtidig, brukes metadataene for det tilkoblede programmet.</span><span class="sxs-lookup"><span data-stu-id="a3257-288">If a mapping refers to the metadata configuration and the connected application at the same time, the metadata of the connected application will be used.</span></span>

3. <span data-ttu-id="a3257-289">Velg **Utforming**.</span><span class="sxs-lookup"><span data-stu-id="a3257-289">Select **Designer**.</span></span>
4. <span data-ttu-id="a3257-290">Velg **Utforming**.</span><span class="sxs-lookup"><span data-stu-id="a3257-290">Select **Designer**.</span></span>
5. <span data-ttu-id="a3257-291">Velg **Dynamics 365 for Operations \> Tabellposter** i treet.</span><span class="sxs-lookup"><span data-stu-id="a3257-291">In the tree, select **Dynamics 365 for Operations \> Table records**.</span></span>
6. <span data-ttu-id="a3257-292">Velg **Legg til rot**.</span><span class="sxs-lookup"><span data-stu-id="a3257-292">Select **Add root**.</span></span>
7. <span data-ttu-id="a3257-293">Angi eller velg en verdi i **Tabell**-feltet.</span><span class="sxs-lookup"><span data-stu-id="a3257-293">In the **Table** field, enter or select a value.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a3257-294">På dette stadiet er det flere enn to programtabeller som tilbys, fordi denne tilordningen bruker alle metadataene i det tilkoblede programmet som er tilordnet til den.</span><span class="sxs-lookup"><span data-stu-id="a3257-294">At this point, more than two application tables are offered, because this mapping uses all the metadata of the connected application that has been assigned to it.</span></span>

8. <span data-ttu-id="a3257-295">Velg **Avbryt**.</span><span class="sxs-lookup"><span data-stu-id="a3257-295">Select **Cancel**.</span></span>
9. <span data-ttu-id="a3257-296">Velg **Valider**.</span><span class="sxs-lookup"><span data-stu-id="a3257-296">Select **Validate**.</span></span>

<span data-ttu-id="a3257-297">Du har nå bundet elementer i datamodellen til elementer i datakildene som er beskrevet, ved å bruke detaljer i metadataene for det tilkoblede programmet som er tilordnet til denne tilordningen.</span><span class="sxs-lookup"><span data-stu-id="a3257-297">You've now bound elements of the data model to items of the data sources that are described by using details of the metadata of the connected application that has been assigned to this mapping.</span></span>

<span data-ttu-id="a3257-298">Når du må evaluere denne modelltilordningen ved å bruke metadataene for en annen versjon av programmet, registrerer du et nytt tilkoblet program, tilordner det til denne modelltilordningen og validerer det mot de nye metadataene.</span><span class="sxs-lookup"><span data-stu-id="a3257-298">When you must evaluate this model mapping by using the metadata of a different version of the application, register another connected application, assign it to this model mapping, and validate it against the new metadata.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a3257-299">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="a3257-299">Additional resources</span></span>

<span data-ttu-id="a3257-300">Du kan også spille av oppgaveveiledningen **Klargjøre programmetadataene som kan brukes i RCS** i programmet samt oppgaveveiledningene **Få tilgang til programmetadata ved hjelp av en ER-konfigurasjon** og **Få tilgang til programmetadata ved hjelp av tilkoblede programmer** i RCS.</span><span class="sxs-lookup"><span data-stu-id="a3257-300">Alternatively, you can play the **Prepare application metadata that can be used in RCS** task guide in the application as as well as the **Access application metadata by using an ER configuration** and **Access application metadata by using connected applications** task guides in RCS.</span></span> <span data-ttu-id="a3257-301">Disse oppgaveveiledningene kan lastes ned fra siden [Oppgaveveiledninger for elektronisk rapportering for Dynamics 365 for Finance and Operations 8.1](https://go.microsoft.com/fwlink/?linkid=2082739).</span><span class="sxs-lookup"><span data-stu-id="a3257-301">These task guides can be downloaded from the [Electronic Reporting Task Guides for Dynamics 365 for Finance and Operations 8.1](https://go.microsoft.com/fwlink/?linkid=2082739) page.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]