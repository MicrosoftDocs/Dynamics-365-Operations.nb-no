---
title: Administrere livssyklus til konfigurasjoner for elektronisk rapportering (ER)
description: Dette emnet beskriver hvordan du administrerer livssyklusen til ER-konfigurasjoner (elektronisk rapportering) for Microsoft Dynamics 365 Finance-løsningen.
author: NickSelin
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERMappedFormatDesigner, ERModelMappingDesigner, ERModelMappingTable, ERSolutionImport, ERSolutionTable, ERVendorTable, ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58801
ms.assetid: 35ad19ea-185d-4fce-b9cb-f94584b14f75
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6206b3a1ac298af98e4b69b6800b9a493658c4ea
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/27/2019
ms.locfileid: "2181295"
---
# <a name="manage-the-electronic-reporting-er-configuration-lifecycle"></a><span data-ttu-id="8d59b-103">Administrere livssyklus til konfigurasjoner for elektronisk rapportering (ER)</span><span class="sxs-lookup"><span data-stu-id="8d59b-103">Manage the Electronic reporting (ER) configuration lifecycle</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8d59b-104">Dette emnet beskriver hvordan du administrerer livssyklusen til ER-konfigurasjoner (elektronisk rapportering) for Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="8d59b-104">This topic describes how to manage the lifecycle of Electronic reporting (ER) configurations for Microsoft Dynamics 365 Finance.</span></span>

## <a name="overview"></a><span data-ttu-id="8d59b-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="8d59b-105">Overview</span></span>

<span data-ttu-id="8d59b-106">Elektronisk rapportering (ER) er en motor som støtter lovbestemte obligatoriske og landsspesifikke elektroniske dokumenter.</span><span class="sxs-lookup"><span data-stu-id="8d59b-106">Electronic reporting (ER) is an engine that supports statutory required and country-specific electronic documents.</span></span> <span data-ttu-id="8d59b-107">Vanligvis forutsetter ER en mulighet til å utføre følgende oppgaver for ett enkelt dokument elektronisk.</span><span class="sxs-lookup"><span data-stu-id="8d59b-107">In general, ER assumes an ability to perform the following tasks for a single electronic document.</span></span> <span data-ttu-id="8d59b-108">Hvis du vil ha mer informasjon, se [Oversikt over elektronisk rapportering](general-electronic-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="8d59b-108">For more details, see [Electronic reporting overview](general-electronic-reporting.md).</span></span>

- <span data-ttu-id="8d59b-109">Utforme en mal for et elektronisk dokument:</span><span class="sxs-lookup"><span data-stu-id="8d59b-109">Design a template for an electronic document:</span></span>

    - <span data-ttu-id="8d59b-110">Identifiser de påkrevde datakildene som kan presenteres i dokumentet:</span><span class="sxs-lookup"><span data-stu-id="8d59b-110">Identify the required sources of data that can be presented in the document:</span></span>

        - <span data-ttu-id="8d59b-111">Underliggende data, for eksempel datatabeller, dataenheter og klasser.</span><span class="sxs-lookup"><span data-stu-id="8d59b-111">Underlying data, such as data tables, data entities, and classes.</span></span>
        - <span data-ttu-id="8d59b-112">Prosess-spesifikke egenskaper, for eksempel dato og klokkeslett for kjøring og tidssone.</span><span class="sxs-lookup"><span data-stu-id="8d59b-112">Process-specific properties, such as execution date and time, and time zone.</span></span>
        - <span data-ttu-id="8d59b-113">Inndataparametre for brukere, angitt av sluttbrukeren under kjøring.</span><span class="sxs-lookup"><span data-stu-id="8d59b-113">User input parameters, specified by the end user at run time.</span></span>

    - <span data-ttu-id="8d59b-114">Definer de nødvendige dokumentetelementene og deres topologi for å angi et endelig dokumentformat.</span><span class="sxs-lookup"><span data-stu-id="8d59b-114">Define the required document elements and their topology to specify a final document format.</span></span>
    - <span data-ttu-id="8d59b-115">Konfigurer den ønskede flyten av data fra valgte datakilder til definerte dokumentelementer (via datakildebindinger til dokumentets formatkomponenter) og angi kontrollogikk for prosessen.</span><span class="sxs-lookup"><span data-stu-id="8d59b-115">Configure the desired flow of data from selected data sources to defined document elements (via data source bindings to document format components), and specify process control logic.</span></span>

- <span data-ttu-id="8d59b-116">Gjør en mal tilgjengelig slik at den kan brukes i andre forekomster:</span><span class="sxs-lookup"><span data-stu-id="8d59b-116">Make a template available so that it can be used in other instances:</span></span>

    - <span data-ttu-id="8d59b-117">Endre en dokumentmal som ble opprettet til en ER-konfigurasjon, og eksporter konfigurasjonen fra den gjeldende programforekomsten som en XML-pakke som kan lagres lokalt eller i LCS.</span><span class="sxs-lookup"><span data-stu-id="8d59b-117">Transform a document template that was created into an ER configuration, and export the configuration from the current application instance as an XML package that can be stored either locally or in LCS.</span></span>
    - <span data-ttu-id="8d59b-118">Gjør om en ER-konfigurasjon til en dokumentmal for program.</span><span class="sxs-lookup"><span data-stu-id="8d59b-118">Transform an ER configuration into an application document template.</span></span>
    - <span data-ttu-id="8d59b-119">Importer en XML-pakke som er lagret lokalt eller i LCS, i den gjeldende forekomsten.</span><span class="sxs-lookup"><span data-stu-id="8d59b-119">Import an XML package that is stored either locally or in LCS into the current instance.</span></span>

- <span data-ttu-id="8d59b-120">Tilpass malen for et elektronisk dokument:</span><span class="sxs-lookup"><span data-stu-id="8d59b-120">Customize the template of an electronic document:</span></span>

    - <span data-ttu-id="8d59b-121">Inkluder en mal fra LCS i den gjeldende forekomsten som en ER-konfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="8d59b-121">Bring a template from LCS into the current instance as an ER configuration.</span></span>
    - <span data-ttu-id="8d59b-122">Utform en tilpasset versjon av ER-konfigurasjonen og behold en referanse til den grunnleggende versjonen.</span><span class="sxs-lookup"><span data-stu-id="8d59b-122">Design a custom version of an ER configuration, and keep a reference to the base version.</span></span>

- <span data-ttu-id="8d59b-123">Integrer en mal med en bestemt forretningsprosess, slik at den er tilgjengelig i programmet:</span><span class="sxs-lookup"><span data-stu-id="8d59b-123">Integrate a template with a particular business process, so that it's available in the application:</span></span>

    - <span data-ttu-id="8d59b-124">Konfigurer innstillinger slik at programmet starter å bruke en ER-konfigurasjon, ved å referere til denne konfigurasjonen i en parameter som er relatert til prosessen.</span><span class="sxs-lookup"><span data-stu-id="8d59b-124">Configure settings so that the application starts to use an ER configuration, by referring to that configuration in a process-related parameter.</span></span> <span data-ttu-id="8d59b-125">For eksempel, se ER-konfigurasjonen i en bestemt leverandørbetalingsmetode for å generere en melding om elektronisk betaling for behandling av fakturaer.</span><span class="sxs-lookup"><span data-stu-id="8d59b-125">For example, refer to the ER configuration in a specific Accounts payable payment method to generate an electronic payment message for processing invoices.</span></span>

- <span data-ttu-id="8d59b-126">Bruk en mal i en bestemt forretningsprosess:</span><span class="sxs-lookup"><span data-stu-id="8d59b-126">Use a template in a specific business process:</span></span>

    - <span data-ttu-id="8d59b-127">Kjør en ER-konfigurasjon i en spesifikk forretningsprosess.</span><span class="sxs-lookup"><span data-stu-id="8d59b-127">Run an ER configuration in a specific business process.</span></span> <span data-ttu-id="8d59b-128">For eksempel for å generere en melding om elektronisk betaling for behandling av fakturaer når en betaløingsmetode som refererer til ER-konfigurasjonen, er valgt.</span><span class="sxs-lookup"><span data-stu-id="8d59b-128">For example, to generate an electronic payment message for processing invoices when a payment method that references the ER configuration is selected.</span></span>

## <a name="concepts"></a><span data-ttu-id="8d59b-129">Begreper</span><span class="sxs-lookup"><span data-stu-id="8d59b-129">Concepts</span></span>
<span data-ttu-id="8d59b-130">Følgende roller og dedikerte aktiviteter er knyttet til livssyklusen for ER-konfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="8d59b-130">The following roles and related activities are associated with the ER configuration lifecycle.</span></span>

| <span data-ttu-id="8d59b-131">Rolle</span><span class="sxs-lookup"><span data-stu-id="8d59b-131">Role</span></span>                                       | <span data-ttu-id="8d59b-132">Aktiviteter</span><span class="sxs-lookup"><span data-stu-id="8d59b-132">Activities</span></span>                                                      | <span data-ttu-id="8d59b-133">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="8d59b-133">Description</span></span> |
|--------------------------------------------|-----------------------------------------------------------------|-------------|
| <span data-ttu-id="8d59b-134">Funksjonell konsulent for elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="8d59b-134">Electronic reporting functional consultant</span></span> | <span data-ttu-id="8d59b-135">Opprett og administrer ER-komponenter (modeller og formater).</span><span class="sxs-lookup"><span data-stu-id="8d59b-135">Create and manage ER components (models and formats).</span></span>           | <span data-ttu-id="8d59b-136">En forretningsperson som utformer ER-domenespesifikke datamodeller, utformer de nødvendige malene for elektroniske dokumenter, og binder dem i henhold til dette.</span><span class="sxs-lookup"><span data-stu-id="8d59b-136">A business person who designs ER domain–specific data models, designs the required templates for electronic documents, and binds them accordingly.</span></span> |
| <span data-ttu-id="8d59b-137">Utvikler av elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="8d59b-137">Electronic reporting developer</span></span>             | <span data-ttu-id="8d59b-138">Opprett og behandle datatilordninger for modellen.</span><span class="sxs-lookup"><span data-stu-id="8d59b-138">Create and manage data model mappings.</span></span>                          | <span data-ttu-id="8d59b-139">En spesialist som velger de nødvendige Finance-datakildene og binder dem til ER-domenespesifikke datamodeller.</span><span class="sxs-lookup"><span data-stu-id="8d59b-139">A specialist who selects the required Finance data sources and binds them to ER domain–specific data models.</span></span> |
| <span data-ttu-id="8d59b-140">Regnskapsansvarlig</span><span class="sxs-lookup"><span data-stu-id="8d59b-140">Accounting supervisor</span></span>                      | <span data-ttu-id="8d59b-141">Konfigurer prosessrelaterte innstillinger som refererer til ER-artefakter.</span><span class="sxs-lookup"><span data-stu-id="8d59b-141">Configure process-related settings that reference ER artifacts.</span></span> | <span data-ttu-id="8d59b-142">For eksempel en **Regnskapsansvarlig**-rolle som tillater at innstillingene for en ER-konfigurasjon kan brukes i en bestemt leverandørbetalingsmåte for å generere en melding om elektronisk betaling for behandling av fakturaer.</span><span class="sxs-lookup"><span data-stu-id="8d59b-142">For example, an **Accounting supervisor** role that allows the settings of an ER configuration to be used in a particular Accounts payable payment method to generate an electronic payment message for processing invoices.</span></span> |
| <span data-ttu-id="8d59b-143">Leverandørbetalingsassistent</span><span class="sxs-lookup"><span data-stu-id="8d59b-143">Accounts payable payments clerk</span></span>            | <span data-ttu-id="8d59b-144">Bruk ER-artefakter i en bestemt forretningsprosess.</span><span class="sxs-lookup"><span data-stu-id="8d59b-144">Use ER artifacts in a specific business process.</span></span>                | <span data-ttu-id="8d59b-145">For eksempel en **Leverandørbetalingsassistent**-rolle som tillater at meldinger om elektronisk betaling kan genereres for behandling av fakturaer, basert på ER-formatet som er konfigurert for en bestemt betalingsmåte.</span><span class="sxs-lookup"><span data-stu-id="8d59b-145">For example, an **Accounts payable payments clerk** role that allows electronic payment messages to be generated for processing invoices, based on the ER format that is configured for a specific payment method.</span></span> |

## <a name="er-configuration-development-lifecycle"></a><span data-ttu-id="8d59b-146">Utviklinglivssyklus for ER-konfigurasjon</span><span class="sxs-lookup"><span data-stu-id="8d59b-146">ER configuration development lifecycle</span></span>
<span data-ttu-id="8d59b-147">Av følgende ER-relaterte årsaker anbefaler vi at du utformer ER-konfigurasjoner i utviklingsmiljøet, som en separat forekomst av Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="8d59b-147">For the following ER-related reasons, we recommend that you design ER configurations in the development environment, as a separate instance of Finance and Operations:</span></span>

- <span data-ttu-id="8d59b-148">Brukere som har en av rollene **Utvikler av elektronisk rapportering** eller **Funksjonell konsulent for elektronisk rapportering**, kan redigere konfigurasjoner og kjøre dem for testformål.</span><span class="sxs-lookup"><span data-stu-id="8d59b-148">Users in either the **Electronic reporting developer** role or the **Electronic reporting functional consultant** role can edit configurations and run them for testing purposes.</span></span> <span data-ttu-id="8d59b-149">Dette scenariet kan føre til kall av metoder for klasser og tabeller som kan være farlige for forretningsdata og ytelse for forekomsten.</span><span class="sxs-lookup"><span data-stu-id="8d59b-149">This scenario can cause calls of methods of classes and tables that might harm business data and the performance of the instance.</span></span>
- <span data-ttu-id="8d59b-150">Kall av metoder for klasser og tabeller som ER-datakilder for ER-konfigurasjoner er ikke begrenset av startpunkter og logget firmainnhold.</span><span class="sxs-lookup"><span data-stu-id="8d59b-150">Calls of methods of classes and tables as ER data sources of ER configurations aren't restricted by entry points and logged company content.</span></span> <span data-ttu-id="8d59b-151">Brukere som har rollene **Utvikler av elektronisk rapportering** eller **Funksjonell konsulent for elektronisk rapportering** kan få tilgang til forretningssensitive data.</span><span class="sxs-lookup"><span data-stu-id="8d59b-151">Therefore, users in either the **Electronic reporting developer** role or the **Electronic reporting functional consultant** role can access business-sensitive data.</span></span>

<span data-ttu-id="8d59b-152">ER-konfigurasjoner som er utformet i utviklingsmiljøet, kan lastes opp til testmiljøet for konfigurasjonsevalueringen (riktig prosessintegrering, riktige resultater, ytelse) og kvalitetssikring (riktige tilgangsrettigheter drevet av rolle, arbeidsdeling osv.).</span><span class="sxs-lookup"><span data-stu-id="8d59b-152">ER configurations that are designed in the development environment can be uploaded to the test environment for the configuration evaluation (proper process integration, correctness of results, and performance) and quality assurance, such as correctness of role-driven access rights and segregation of duties.</span></span> <span data-ttu-id="8d59b-153">Funksjoner som gjør at utveksling av ER-konfigurasjoner kan brukes til dette formålet.</span><span class="sxs-lookup"><span data-stu-id="8d59b-153">The features that enable ER configuration interchange can be used for this purpose.</span></span> <span data-ttu-id="8d59b-154">Til slutt kan kontrollerte ER-konfigurasjoner lastes opp til LCS, der de kan deles med abonnenter eller til produksjonsmiljøet for intern bruk, som vist i illustrasjonen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="8d59b-154">Finally, proven ER configurations can be uploaded either to LCS, where they can be shared with service subscribers, or to the production environment for internal use, such as shown in the following illustration.</span></span>

![Livssyklus for ER-konfigurasjon](./media/ger-configuration-lifecycle.png)

## <a name="additional-resources"></a><span data-ttu-id="8d59b-156">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="8d59b-156">Additional resources</span></span>

[<span data-ttu-id="8d59b-157">Oversikt over elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="8d59b-157">Electronic reporting overview</span></span>](general-electronic-reporting.md)
