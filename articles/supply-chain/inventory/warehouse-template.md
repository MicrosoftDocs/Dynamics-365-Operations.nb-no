---
title: Definere et lager ved hjelp av en mal for lagerkonfigurasjon
description: Dette emnet forklarer hvordan du definerer et lager ved hjelp av en mal for lagerkonfigurasjon.
author: perlynne
manager: AnnBe
ms.date: 11/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DataManagementWorkspace, DMFQuickImportExportEnhanced, DMFDefinitionGroupTemplate, DMFEntityTemplateDefinitionLoadDialog
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: AX 7.3
ms.translationtype: HT
ms.sourcegitcommit: 0ca19ab9ed7a52328c5dd5252c418bb9343bdc2b
ms.openlocfilehash: 87ade03ec2ba78c4d7f5832bfa6dc1b7eabd8d94
ms.contentlocale: nb-no
ms.lasthandoff: 12/14/2017

---

# <a name="set-up-a-warehouse-by-using-a-warehouse-configuration-template"></a><span data-ttu-id="845e8-103">Definere et lager ved hjelp av en mal for lagerkonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="845e8-103">Set up a warehouse by using a warehouse configuration template</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="845e8-104">Dette emnet forklarer hvordan du definerer et lager ved hjelp av en mal for lagerkonfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="845e8-104">This topic explains how to set up a warehouse by using a warehouse configuration template.</span></span> <span data-ttu-id="845e8-105">Det finnes flere forhåndsdefinerte konfigurasjonsmaler som du kan bruke.</span><span class="sxs-lookup"><span data-stu-id="845e8-105">There are several predefined configuration templates that you can use.</span></span> <span data-ttu-id="845e8-106">Hvis du vil ha informasjon om hvordan du bruker disse malene, se [Konfigurasjonsdatamaler](../../dev-itpro/data-entities/configuration-data-templates.md).</span><span class="sxs-lookup"><span data-stu-id="845e8-106">For information about how to use these templates, see [Configuration data templates](../../dev-itpro/data-entities/configuration-data-templates.md).</span></span>

## <a name="scenarios-where-configuration-templates-can-be-helpful"></a><span data-ttu-id="845e8-107">Scenarier der konfigurasjonsmaler kan være nyttige</span><span class="sxs-lookup"><span data-stu-id="845e8-107">Scenarios where configuration templates can be helpful</span></span>

<span data-ttu-id="845e8-108">Konfigurasjonsmaler kan være nyttige i mange scenarier.</span><span class="sxs-lookup"><span data-stu-id="845e8-108">Configuration templates can be helpful in many scenarios.</span></span> <span data-ttu-id="845e8-109">Her er noen eksempler:</span><span class="sxs-lookup"><span data-stu-id="845e8-109">Here are some examples:</span></span>

- <span data-ttu-id="845e8-110">Du har fullført og testet et konfigurasjonsoppsett i et testmiljø, og nå vil du kopiere oppsettet til et produksjonsmiljø.</span><span class="sxs-lookup"><span data-stu-id="845e8-110">You've completed and tested a configuration setup in a test environment, and you now want to copy the setup to a production environment.</span></span>
- <span data-ttu-id="845e8-111">Du vil rulle lageroppsettet ut til flere juridiske enheter eller opprette et nytt lager i den samme juridiske enheten.</span><span class="sxs-lookup"><span data-stu-id="845e8-111">You want to roll the warehouse setup out to several legal entities or create a new warehouse in the same legal entity.</span></span>
- <span data-ttu-id="845e8-112">Du vil klargjøre en demonstrasjon av funksjonen for lageret raskt.</span><span class="sxs-lookup"><span data-stu-id="845e8-112">You want to quickly prepare for a demo of the warehouse functionality.</span></span>
- <span data-ttu-id="845e8-113">Du vil at eksisterende elementer og lagre skal bruke funksjonaliteten i Lagerstyring i stedet for funksjonaliteten i Beholdningsstyring.</span><span class="sxs-lookup"><span data-stu-id="845e8-113">You want existing items and warehouses to use the functionality in Warehouse management instead of the functionality in Inventory management.</span></span>

<span data-ttu-id="845e8-114">Dette emnet fokserer på det første av disse scenariene.</span><span class="sxs-lookup"><span data-stu-id="845e8-114">This topic focuses on the first of these scenarios.</span></span> <span data-ttu-id="845e8-115">Det viser hvordan du kan bruke en konfigurasjonsmal til å kopiere et konfigurasjonsoppsett fra et testmiljø til et produksjonsmiljø.</span><span class="sxs-lookup"><span data-stu-id="845e8-115">It shows how you can use a configuration template to copy a configuration setup from a test environment to a production environment.</span></span>

## <a name="copy-a-configuration-setup-from-a-test-environment-to-a-production-environment"></a><span data-ttu-id="845e8-116">Kopiere et konfigurasjonsoppsett fra et testmiljø til et produksjonsmiljø</span><span class="sxs-lookup"><span data-stu-id="845e8-116">Copy a configuration setup from a test environment to a production environment</span></span>

<span data-ttu-id="845e8-117">I dette scenariet finnes konfigurasjonsoppsettet for et lager og enkelte transaksjonsprosesser allerede i et testmiljø.</span><span class="sxs-lookup"><span data-stu-id="845e8-117">For this scenario, the configuration setup for a warehouse and some transaction processes already exist in a test environment.</span></span> <span data-ttu-id="845e8-118">Nå ønsker du å kopiere konfigurasjonsoppsettet for lageret fra testmiljøet til et produksjonsmiljø.</span><span class="sxs-lookup"><span data-stu-id="845e8-118">You now want to copy the configuration setup for the warehouse from the test environment to a production environment.</span></span>

> [!NOTE]
> <span data-ttu-id="845e8-119">Det er viktig at du tar med andre relaterte oppsettdata når du kopierer et konfigurasjonsoppsett.</span><span class="sxs-lookup"><span data-stu-id="845e8-119">It's important that you include other related setup data when you copy a configuration setup.</span></span> <span data-ttu-id="845e8-120">Du kan for eksempel definere produkter ved å kopiere oppsettet fra et testmiljø.</span><span class="sxs-lookup"><span data-stu-id="845e8-120">For example, you want to set up products by copying the setup from a test environment.</span></span> <span data-ttu-id="845e8-121">Du kan imidlertid definere et fast plukksted for et produkt før produktet blir opprettet.</span><span class="sxs-lookup"><span data-stu-id="845e8-121">However, you can't set up a fixed picking location for a product before that product is created.</span></span> <span data-ttu-id="845e8-122">Selv om enkelte konfigurasjonsmaler ikke støtter denne typen avhengighet, finnes det standard datamaler som støtter dette.</span><span class="sxs-lookup"><span data-stu-id="845e8-122">Although individual configuration templates don't support this type of dependency, there are default data templates that support it.</span></span> <span data-ttu-id="845e8-123">Du kan enkelt inkludere disse standard datamalene i en konfigurasjonsprosess.</span><span class="sxs-lookup"><span data-stu-id="845e8-123">You can easily include these default data templates in a configuration process.</span></span>

### <a name="export-a-default-warehouse-template"></a><span data-ttu-id="845e8-124">Eksportere en standardmal for lager</span><span class="sxs-lookup"><span data-stu-id="845e8-124">Export a default warehouse template</span></span> 

1. <span data-ttu-id="845e8-125">Åpne arbeidsområdet **Databehandling**.</span><span class="sxs-lookup"><span data-stu-id="845e8-125">Open the **Data management** workspace.</span></span>

    > [!NOTE]
    > <span data-ttu-id="845e8-126">Hvis du bruker dette arbeidsområdet for første gang, må du laste inn alle dataenhetene før du fortsetter.</span><span class="sxs-lookup"><span data-stu-id="845e8-126">If you're using this workspace for the first time, you must load all the data entities before you continue.</span></span>

2. <span data-ttu-id="845e8-127">Velg flisen **Maler**, og velg deretter **Last standardmaler** for å laste inn standardmalene.</span><span class="sxs-lookup"><span data-stu-id="845e8-127">Select the **Templates** tile, and then select **Load default templates** to load the default templates.</span></span>

    > [!NOTE]
    > <span data-ttu-id="845e8-128">**Last standardmaler** er bare tilgjengelig i **Utvidet**-visningen.</span><span class="sxs-lookup"><span data-stu-id="845e8-128">**Load default templates** is available only in the **Enhanced** view.</span></span> <span data-ttu-id="845e8-129">Velg **Rammeverkparametere**, og deretter i feltet **Vis standarder** velger du **Utvidet visning**.</span><span class="sxs-lookup"><span data-stu-id="845e8-129">Select **Framework parameters**, and then, in the **View defaults** field, select **Enhanced view**.</span></span>

3. <span data-ttu-id="845e8-130">Når standardmalene er lastet inn, kan du endre dem slik at de overholder dine forretningskrav.</span><span class="sxs-lookup"><span data-stu-id="845e8-130">After the default templates are loaded, you can change them so that they meet your business requirements.</span></span>

    > [!NOTE]
    > <span data-ttu-id="845e8-131">Hvis du vil laste inn standardmaler og importere maler, må du ha administratortilgang for systemet.</span><span class="sxs-lookup"><span data-stu-id="845e8-131">To load default templates and import templates, you must have system administrator access.</span></span> <span data-ttu-id="845e8-132">Dette kravet bidrar til å sikre at alle enheter er riktig lastet inn i malen.</span><span class="sxs-lookup"><span data-stu-id="845e8-132">This requirement helps guarantee that all entities are correctly loaded into the template.</span></span>

4. <span data-ttu-id="845e8-133">Kontroller at du er i den juridiske enheten du vil eksportere de bedriftsspesifikke dataene fra.</span><span class="sxs-lookup"><span data-stu-id="845e8-133">Make sure that you're in the legal entity that you want to export the company-specific data from.</span></span>
5. <span data-ttu-id="845e8-134">I arbeidsområdet, velger du **Eksporter**.</span><span class="sxs-lookup"><span data-stu-id="845e8-134">In the workspace, select **Export**.</span></span>
6. <span data-ttu-id="845e8-135">Opprett et nytt eksportprosjekt.</span><span class="sxs-lookup"><span data-stu-id="845e8-135">Create a new export project.</span></span>
7. <span data-ttu-id="845e8-136">Velg **+ Legg til mal**, og finn standardmalen **400 - WMS** for lageret.</span><span class="sxs-lookup"><span data-stu-id="845e8-136">Select **+ Add template**, and find the **400 - WMS** default warehouse template.</span></span> <span data-ttu-id="845e8-137">Denne malen legger til dataenheter for lagerkonfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="845e8-137">This template adds data entities for warehouse configuration.</span></span>

    > [!NOTE]
    > <span data-ttu-id="845e8-138">Hvis dataene som du eksporterer, må filtreres (du ønsker for eksempel å eksportere bare dataene som er knyttet til et bestemt lager), må du evaluere hver dataenhet og legge til filtrering via en spørring.</span><span class="sxs-lookup"><span data-stu-id="845e8-138">If the data that you're exporting must be filtered (for example, you want to export only the data that is related to a specific warehouse), you must evaluate each data entity and add filtering via a query.</span></span> <span data-ttu-id="845e8-139">Du kan også eksportere alle dataene og deretter slette postene som ikke er påkrevd i målfilene.</span><span class="sxs-lookup"><span data-stu-id="845e8-139">Alternatively, you can export all data and then delete the records that aren't required in the destination files.</span></span>

8. <span data-ttu-id="845e8-140">Velg **Eksporter**.</span><span class="sxs-lookup"><span data-stu-id="845e8-140">Select **Export**.</span></span> <span data-ttu-id="845e8-141">Data som er knyttet til alle dataenhetene i prosjektet, eksporteres.</span><span class="sxs-lookup"><span data-stu-id="845e8-141">Data that is related to all the data entities in the project is exported.</span></span>

<span data-ttu-id="845e8-142">Du kan laste ned en zip-fil for datapakken.</span><span class="sxs-lookup"><span data-stu-id="845e8-142">You can download a zip file for the data package.</span></span> <span data-ttu-id="845e8-143">Denne filen inneholder alle dataene i det valgte formatet (for eksempel et Excel-format).</span><span class="sxs-lookup"><span data-stu-id="845e8-143">This file contains all the data in the selected format (for example, Excel format).</span></span> <span data-ttu-id="845e8-144">Som nevnt, må enkelte poster i datapakkefilene kanskje oppdateres før du kan importere dem til produksjonsmiljøet.</span><span class="sxs-lookup"><span data-stu-id="845e8-144">As has been mentioned, some records in the data package files might have to be updated before you can import them into the production environment.</span></span> <span data-ttu-id="845e8-145">Hvis du oppdaterer en post, må du kontrollere at du ikke endrer filnavnet.</span><span class="sxs-lookup"><span data-stu-id="845e8-145">If you update a record, make sure that you don't change the file name.</span></span>

### <a name="import-a-warehouse-configuration-setup"></a><span data-ttu-id="845e8-146">Importere et konfigurasjonsoppsett for lager</span><span class="sxs-lookup"><span data-stu-id="845e8-146">Import a warehouse configuration setup</span></span>

1. <span data-ttu-id="845e8-147">I målmiljøet må du kontrollere at du er i firmaet der du vil importere lagerdataene.</span><span class="sxs-lookup"><span data-stu-id="845e8-147">In the destination environment, make sure that you're in the company that you want to import the warehouse data into.</span></span>

    > [!NOTE]
    > <span data-ttu-id="845e8-148">Før du gjør importen, må du identifisere dataavhengigheter.</span><span class="sxs-lookup"><span data-stu-id="845e8-148">Before you do the import, you should identify any data dependencies.</span></span> <span data-ttu-id="845e8-149">Malen **Lagerstyring** inneholder for eksempel en dataenhet som heter **Disposisjonskoder for lager**.</span><span class="sxs-lookup"><span data-stu-id="845e8-149">For example, the **Warehouse management** template includes a data entity that is named **Warehouse disposition codes**.</span></span> <span data-ttu-id="845e8-150">Denne enheten inneholder data som er knyttet til oppsettsiden **Disposisjonskoder** (**Lagerstyring** > **Oppsett** > **Mobilenhet** > **Disposisjonskoder**).</span><span class="sxs-lookup"><span data-stu-id="845e8-150">This entity contains data that is related to the **Disposition codes** setup page (**Warehouse management** > **Setup** > **Mobile device** > **Disposition codes**).</span></span> <span data-ttu-id="845e8-151">Hvis et eksisterende oppsett allerede håndterer prosessen for salgsordrer, inneholder feltet **Returdisposisjonskode** en verdi for feltet.</span><span class="sxs-lookup"><span data-stu-id="845e8-151">If an existing setup already handles the return process for sales orders, the **Return disposition code** field contains a value.</span></span> <span data-ttu-id="845e8-152">Disposisjonskoden i dette feltet er knyttet til dataenheten **Disposisjonskode**, som er en del av malen **Salg og markedsføring**.</span><span class="sxs-lookup"><span data-stu-id="845e8-152">The disposition code in this field is related to the **Disposition code** data entity, which is part of the **Sales and marketing** template.</span></span> <span data-ttu-id="845e8-153">Hvis dataene fra dataenheten **Disposisjonskode** ikke er importert før dataene fra feltet **Disposisjonskoder for lager**, vil importen mislykkes.</span><span class="sxs-lookup"><span data-stu-id="845e8-153">If the data from the **Disposition code** data entity isn't imported before the data from the **Warehouse disposition codes** field, the import will fail.</span></span>

2. <span data-ttu-id="845e8-154">I arbeidsområdet **Databehandling** velger du **Importer**.</span><span class="sxs-lookup"><span data-stu-id="845e8-154">In the **Data management** workspace, select **Import**.</span></span>
3. <span data-ttu-id="845e8-155">Opprett et nytt importprosjekt.</span><span class="sxs-lookup"><span data-stu-id="845e8-155">Create a new import project.</span></span>
4. <span data-ttu-id="845e8-156">Velg **+ Legg til fil**, og last opp zip-filen for datapakken.</span><span class="sxs-lookup"><span data-stu-id="845e8-156">Select **+ Add file**, and upload the zip file for the data package.</span></span>
5. <span data-ttu-id="845e8-157">Velg **Import**.</span><span class="sxs-lookup"><span data-stu-id="845e8-157">Select **Import**.</span></span> <span data-ttu-id="845e8-158">I **Utvidet**-visningen kan du bruke **Filter**-alternativet for raskt å få oversikt over problemer som kan oppstå under importen.</span><span class="sxs-lookup"><span data-stu-id="845e8-158">In the **Enhanced** view, you can use the **Filter** option to quickly get an overview of issues that might occur during the import.</span></span>

<span data-ttu-id="845e8-159">**Vis utførelseslogg** gir deg detaljert informasjon om hver dataenhet som importeres.</span><span class="sxs-lookup"><span data-stu-id="845e8-159">The **View execution** log provides detailed information about each data entity that is imported.</span></span> <span data-ttu-id="845e8-160">Du kan bruke oppsamling datavisningen for å gå raskt til målet dataene.</span><span class="sxs-lookup"><span data-stu-id="845e8-160">You can use the staging data view to quickly get to the target data.</span></span> <span data-ttu-id="845e8-161">På denne måten kan du se hva de importerte dataene ser slik på de tilknyttede sidene i programmet.</span><span class="sxs-lookup"><span data-stu-id="845e8-161">In this way, you can see what the imported data looks like on the related pages in the application.</span></span> <span data-ttu-id="845e8-162">Når du bruker standard datamalene, fungerer importsekvensen for hver dataenhet på den forhåndsdefinerte måten, for å garantere at alle avhengige data importeres først.</span><span class="sxs-lookup"><span data-stu-id="845e8-162">When you use the default data templates, the import sequence for each data entity works in the predefined manner, to help guarantee that all dependent data is imported first.</span></span> <span data-ttu-id="845e8-163">Hvis egendefinerte enheter inngår i prosjektet, må du kontrollere at den riktige rekkefølgen er definert.</span><span class="sxs-lookup"><span data-stu-id="845e8-163">If custom data entities are part of the project, you must make sure that the correct sequence is defined.</span></span> <span data-ttu-id="845e8-164">Hvis du vil ha mer informasjon, kan du se [Konfigurasjonsdatamaler](../../dev-itpro/data-entities/configuration-data-templates.md).</span><span class="sxs-lookup"><span data-stu-id="845e8-164">For more information, see [Configuration data templates](../../dev-itpro/data-entities/configuration-data-templates.md).</span></span>

## <a name="related-topic"></a><span data-ttu-id="845e8-165">Relaterte emne</span><span class="sxs-lookup"><span data-stu-id="845e8-165">Related topic</span></span>

[<span data-ttu-id="845e8-166">Konfigurasjonsdatamaler</span><span class="sxs-lookup"><span data-stu-id="845e8-166">Configuration data templates</span></span>](../../dev-itpro/data-entities/configuration-data-templates.md)

