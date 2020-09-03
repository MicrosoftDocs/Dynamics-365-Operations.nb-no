---
title: Endre et ER-formatet for å generere et egendefinert elektronisk dokument
description: Dette emnet beskriver hvordan du justerer et Microsoft-levert format for elektronisk rapportering (ER) slik at det genererer et egendefinert elektronisk dokument.
author: NickSelin
manager: AnnBe
ms.date: 06/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERParameters, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, EROperationDesigner, ERVendorTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 67763b29744c4262249ef1ec04e7df490b31fe5b
ms.sourcegitcommit: 1e6a7b50596eaf9d965e0155f3f2c50f7f50747e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/22/2020
ms.locfileid: "3498109"
---
# <a name="adjust-an-er-format-to-generate-a-custom-electronic-document"></a><span data-ttu-id="fe902-103">Endre et ER-formatet for å generere et egendefinert elektronisk dokument</span><span class="sxs-lookup"><span data-stu-id="fe902-103">Adjust an ER format to generate a custom electronic document</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="fe902-104">Fremgangsmåtene i dette emnet forklarer hvordan en bruker i rollen systemansvarlig eller funksjonsrådgiver for elektronisk rapportering kan utføre disse oppgavene:</span><span class="sxs-lookup"><span data-stu-id="fe902-104">The procedures in this topic explain how a user in the System Administrator or Electronic Reporting Functional Consultant role can perform these tasks:</span></span>

- <span data-ttu-id="fe902-105">Konfigurere parametere for [rammeverket for elektronisk rapportering (ER)](general-electronic-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="fe902-105">Configure parameters for the [Electronic reporting (ER) framework](general-electronic-reporting.md).</span></span>
- <span data-ttu-id="fe902-106">Importer ER-konfigurasjoner som leveres av Microsoft, og som brukes til å generere en betalingsfil mens en [leverandørbetaling](../../../finance/cash-bank-management/tasks/vendor-payment-overview.md) blir behandlet.</span><span class="sxs-lookup"><span data-stu-id="fe902-106">Import ER configurations that are provided by Microsoft and used to generate a payment file while a [vendor payment](../../../finance/cash-bank-management/tasks/vendor-payment-overview.md) is being processed.</span></span>
- <span data-ttu-id="fe902-107">Opprett en egendefinert versjon av en standard ER-formatkonfigurasjon som leveres av Microsoft.</span><span class="sxs-lookup"><span data-stu-id="fe902-107">Create a custom version of a standard ER format configuration that is provided by Microsoft.</span></span>
- <span data-ttu-id="fe902-108">Endre den egendefinerte ER-formatkonfigurasjonen slik at den genererer betalingsfiler som oppfyller kravene til en bestemt bank.</span><span class="sxs-lookup"><span data-stu-id="fe902-108">Modify the custom ER format configuration so that it generates payment files that meets the requirements of a specific bank.</span></span>
- <span data-ttu-id="fe902-109">Ta i bruk endringer som er gjort i standard ER-formatkonfigurasjon i den egendefinert ER-formatkonfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="fe902-109">Adopt changes that are made to the standard ER format configuration in the custom ER format configuration.</span></span>

<span data-ttu-id="fe902-110">Alle disse fremgangsmåtene kan utføres i **GBSI**-firmaet.</span><span class="sxs-lookup"><span data-stu-id="fe902-110">All the following procedures can be done in the **GBSI** company.</span></span> <span data-ttu-id="fe902-111">Ingen koding er nødvendig.</span><span class="sxs-lookup"><span data-stu-id="fe902-111">No coding is required.</span></span>

- [<span data-ttu-id="fe902-112">Konfigurere ER-rammeverket</span><span class="sxs-lookup"><span data-stu-id="fe902-112">Configure the ER framework</span></span>](#ConfigureFramework)

    - [<span data-ttu-id="fe902-113">Konfigurere ER-parametere</span><span class="sxs-lookup"><span data-stu-id="fe902-113">Configure ER parameters</span></span>](#ConfigureParameters)
    - [<span data-ttu-id="fe902-114">Aktivere en ER-konfigurasjonsleverandør</span><span class="sxs-lookup"><span data-stu-id="fe902-114">Activate an ER configuration provider</span></span>](#ActivateProvider)

        - [<span data-ttu-id="fe902-115">Se gjennom listen over ER-konfigurasjonsleverandører</span><span class="sxs-lookup"><span data-stu-id="fe902-115">Review the list of ER configuration providers</span></span>](#ReviewProvidersList)
        - [<span data-ttu-id="fe902-116">Legg til en ny ER-konfigurasjonsleverandør</span><span class="sxs-lookup"><span data-stu-id="fe902-116">Add a new ER configuration provider</span></span>](#ActivateProvider)
        - [<span data-ttu-id="fe902-117">Aktivere en ER-konfigurasjonsleverandør</span><span class="sxs-lookup"><span data-stu-id="fe902-117">Activate an ER configuration provider</span></span>](#ActivateAddedProvider)

- [<span data-ttu-id="fe902-118">Importer standard ER-formatkonfigurasjoner</span><span class="sxs-lookup"><span data-stu-id="fe902-118">Import the standard ER format configurations</span></span>](#ImportERSolution1)

    - [<span data-ttu-id="fe902-119">Importer standard ER-konfigurasjoner</span><span class="sxs-lookup"><span data-stu-id="fe902-119">Import the standard ER configurations</span></span>](#ImportERFormat1)
    - [<span data-ttu-id="fe902-120">Se gjennom importerte ER-konfigurasjoner</span><span class="sxs-lookup"><span data-stu-id="fe902-120">Review the imported ER configurations</span></span>](#ReviewImportedERSolution)

- [<span data-ttu-id="fe902-121">Klargjøre en leverandørbetaling for behandling</span><span class="sxs-lookup"><span data-stu-id="fe902-121">Prepare a vendor payment for processing</span></span>](#PrepareVendorPayment)

    - [<span data-ttu-id="fe902-122">Legg til bankinformasjon for en leverandørkonto</span><span class="sxs-lookup"><span data-stu-id="fe902-122">Add bank information for a vendor account</span></span>](#AddBankAccount)
    - [<span data-ttu-id="fe902-123">Angi en leverandørbetaling</span><span class="sxs-lookup"><span data-stu-id="fe902-123">Enter a vendor payment</span></span>](#EnterVendorPayment)

- [<span data-ttu-id="fe902-124">Behandle en leverandørbetaling ved hjelp av standard ER-format</span><span class="sxs-lookup"><span data-stu-id="fe902-124">Process a vendor payment by using the standard ER format</span></span>](#ProcessVendorPayment1)

    - [<span data-ttu-id="fe902-125">Konfigurere den elektroniske betalingsmåten</span><span class="sxs-lookup"><span data-stu-id="fe902-125">Set up the electronic payment method</span></span>](#ConfigureMethodOfPayment1)
    - [<span data-ttu-id="fe902-126">Behandle en leverandørbetaling</span><span class="sxs-lookup"><span data-stu-id="fe902-126">Process a vendor payment</span></span>](#ProcessPayment1)

- [<span data-ttu-id="fe902-127">Tilpasse standard ER-format</span><span class="sxs-lookup"><span data-stu-id="fe902-127">Customize the standard ER format</span></span>](#CustomizeProvidedFormat)

    - [<span data-ttu-id="fe902-128">Opprette et egendefinert format</span><span class="sxs-lookup"><span data-stu-id="fe902-128">Create a custom format</span></span>](#DeriveProvidedFormat)
    - [<span data-ttu-id="fe902-129">Redigere et egendefinert format</span><span class="sxs-lookup"><span data-stu-id="fe902-129">Edit a custom format</span></span>](#ConfigureDerivedFormat)
    - [<span data-ttu-id="fe902-130">Merke et egendefinert format som kjørbart</span><span class="sxs-lookup"><span data-stu-id="fe902-130">Mark a custom format as runnable</span></span>](#MarkFormatRunnable)

- [<span data-ttu-id="fe902-131">Behandle en leverandørbetaling ved hjelp av egendefinert ER-format</span><span class="sxs-lookup"><span data-stu-id="fe902-131">Process a vendor payment by using the custom ER format</span></span>](#ProcessVendorPayment2)

    - [<span data-ttu-id="fe902-132">Konfigurere den elektroniske betalingsmåten</span><span class="sxs-lookup"><span data-stu-id="fe902-132">Set up the electronic payment method</span></span>](#ConfigureMethodOfPayment2)
    - [<span data-ttu-id="fe902-133">Behandle en leverandørbetaling</span><span class="sxs-lookup"><span data-stu-id="fe902-133">Process a vendor payment</span></span>](#ProcessPayment2)

- [<span data-ttu-id="fe902-134">Importer nye versjoner av standard ER-formatkonfigurasjoner</span><span class="sxs-lookup"><span data-stu-id="fe902-134">Import new versions of the standard ER format configurations</span></span>](#ImportERSolution2)

    - [<span data-ttu-id="fe902-135">Importer nye versjoner av standard ER-konfigurasjoner</span><span class="sxs-lookup"><span data-stu-id="fe902-135">Import new versions of the standard ER configurations</span></span>](#ImportERFormat2)
    - [<span data-ttu-id="fe902-136">Se gjennom importerte ER-formatkonfigurasjoner</span><span class="sxs-lookup"><span data-stu-id="fe902-136">Review the imported ER format configurations</span></span>](#ReviewImportedERFormat)

- [<span data-ttu-id="fe902-137">Ta i bruk endringene i den nye versjonen av et importert format i et egendefinert format</span><span class="sxs-lookup"><span data-stu-id="fe902-137">Adopt the changes in the new version of an imported format in a custom format</span></span>](#AdoptNewBaseVersion)

    - [<span data-ttu-id="fe902-138">Fullfør gjeldende utkastversjon av et egendefinert format</span><span class="sxs-lookup"><span data-stu-id="fe902-138">Complete the current draft version of a custom format</span></span>](#CompleteDerivedFormat)
    - [<span data-ttu-id="fe902-139">Rebasere et egendefinert format på nytt til en ny grunnversjon</span><span class="sxs-lookup"><span data-stu-id="fe902-139">Rebase a custom format to a new base version</span></span>](#RebaseDerivedFormat)
    - [<span data-ttu-id="fe902-140">Behandle en leverandørbetaling ved hjelp av et rebasert ER-format</span><span class="sxs-lookup"><span data-stu-id="fe902-140">Process a vendor payment by using a rebased ER format</span></span>](#ProcessPayment3)

- [<span data-ttu-id="fe902-141">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="fe902-141">Additional resources</span></span>](#References)

## <a name="configure-the-er-framework"></a><a id="ConfigureFramework"></a><span data-ttu-id="fe902-142">Konfigurere ER-rammeverket</span><span class="sxs-lookup"><span data-stu-id="fe902-142">Configure the ER framework</span></span>

<span data-ttu-id="fe902-143">Som en bruker i rollen funksjonsrådgiver for elektroniske rapportering, må du konfigurere minimumsparameterne for ER-parametere før du kan begynne å bruke ER-rammeverket til å utforme en egendefinert versjon av et standardformat.</span><span class="sxs-lookup"><span data-stu-id="fe902-143">As a user in the Electronic Reporting Functional Consultant role, you must configure the minimal set of ER parameters before you can start to use the ER framework to design a custom version of a standard ER format.</span></span>

### <a name="configure-er-parameters"></a><a id="ConfigureParameters"></a><span data-ttu-id="fe902-144">Konfigurere ER-parametere</span><span class="sxs-lookup"><span data-stu-id="fe902-144">Configure ER parameters</span></span>

1. <span data-ttu-id="fe902-145">Gå til **Organisasjonsstyring** \> **Arbeidsområder** \> **Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="fe902-145">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="fe902-146">På siden **Lokaliseringskonfigurasjoner**, i delen **Relaterte koblinger**, velger du flisen **Parametere for elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="fe902-146">On the **Localization configurations** page, in the **Related links** section, select **Electronic reporting parameters**.</span></span>
3. <span data-ttu-id="fe902-147">På **Parametere for elektronisk rapportering**-siden, i **Generelt**-fanen angi **Aktiver utformingsmodus** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="fe902-147">On the **Electronic reporting parameters** page, on the **General** tab, set the **Enable design mode** option to **Yes**.</span></span>
4. <span data-ttu-id="fe902-148">Angi følgende parametere i fanen **Vedlegg**:</span><span class="sxs-lookup"><span data-stu-id="fe902-148">On the **Attachments** tab, set the following parameters:</span></span>

    - <span data-ttu-id="fe902-149">I **Konfigurasjoner**-feltet velger du **Fil**-typen for **USMF**-firmaet.</span><span class="sxs-lookup"><span data-stu-id="fe902-149">In the **Configurations** field, select the **File** type for the **USMF** company.</span></span>
    - <span data-ttu-id="fe902-150">I feltene **Jobbarkiv**, **Midlertidig**, **Grunnlinje** og **Annet** velger du **Fil**-typen.</span><span class="sxs-lookup"><span data-stu-id="fe902-150">In the **Job archive**, **Temporary**, **Baseline**, and **Others** fields, select the **File** type.</span></span>

<span data-ttu-id="fe902-151">Hvis du vil ha mer informasjon om ER-parametere, kan du se [Konfigurere ER-rammeverket](electronic-reporting-er-configure-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="fe902-151">For more information about ER parameters, see [Configure the ER framework](electronic-reporting-er-configure-parameters.md).</span></span>

### <a name="activate-an-er-configuration-provider"></a><a id="ActivateProvider"></a><span data-ttu-id="fe902-152">Aktivere en ER-konfigurasjonsleverandør</span><span class="sxs-lookup"><span data-stu-id="fe902-152">Activate an ER configuration provider</span></span>

<span data-ttu-id="fe902-153">Hver ER-konfigurasjon som legges til, er merket som eid av en ER-konfigurasjonsleverandør.</span><span class="sxs-lookup"><span data-stu-id="fe902-153">Every ER configuration that is added is marked as owned by an ER configuration provider.</span></span> <span data-ttu-id="fe902-154">ER-konfigurasjonsleverandøren som aktiveres i **Elektronisk rapportering**-arbeidsområdet, brukes til dette formålet.</span><span class="sxs-lookup"><span data-stu-id="fe902-154">The ER configuration provider that is activated in the **Electronic reporting** workspace is used for this purpose.</span></span> <span data-ttu-id="fe902-155">Derfor må du aktivere en ER-konfigurasjonsleverandør i **Elektronisk rapportering**-arbeidsområdet før du begynner å legge til eller redigere ER-konfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="fe902-155">Therefore, you must activate an ER configuration provider in the **Electronic reporting** workspace before you start to add or edit ER configurations.</span></span>

> [!NOTE]
> <span data-ttu-id="fe902-156">Bare eieren av en ER-konfigurasjon kan redigere den.</span><span class="sxs-lookup"><span data-stu-id="fe902-156">Only the owner of an ER configuration can edit it.</span></span> <span data-ttu-id="fe902-157">Derfor, før en ER-konfigurasjon kan redigeres, må du aktivere en ER-konfigurasjonsleverandør i **Elektronisk rapportering**-arbeidsområdet.</span><span class="sxs-lookup"><span data-stu-id="fe902-157">Therefore, before an ER configuration can be edited, the appropriate ER configuration provider must be activated in the **Electronic reporting** workspace.</span></span>

#### <a name="review-the-list-of-er-configuration-providers"></a><a id="ReviewProvidersList"></a><span data-ttu-id="fe902-158">Se gjennom listen over ER-konfigurasjonsleverandører</span><span class="sxs-lookup"><span data-stu-id="fe902-158">Review the list of ER configuration providers</span></span>

1. <span data-ttu-id="fe902-159">Gå til **Organisasjonsstyring** \> **Arbeidsområder** \> **Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="fe902-159">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="fe902-160">På siden **Lokaliseringskonfigurasjoner**, i delen **Relaterte koblinger**, velger du flisen **Konfigurasjonsleverandører**.</span><span class="sxs-lookup"><span data-stu-id="fe902-160">On the **Localization configurations** page, in the **Related links** section, select **Configuration providers**.</span></span>
3. <span data-ttu-id="fe902-161">På **Konfigurasjonsleverandørtabell**-siden har hver leverandørpost et unikt navn og en unik URL-adresse.</span><span class="sxs-lookup"><span data-stu-id="fe902-161">On the **Configuration provider table** page, each provider record has a unique name and URL.</span></span> <span data-ttu-id="fe902-162">Se gjennom innholdet på denne siden.</span><span class="sxs-lookup"><span data-stu-id="fe902-162">Review the contents of this page.</span></span> <span data-ttu-id="fe902-163">Hvis det allerede finnes en post for **Litware, Inc.** (`https://www.litware.com`), hopper du over den neste fremgangsmåten og [legger til en ny ER-konfigurasjonsleverandør](#ActivateProvider).</span><span class="sxs-lookup"><span data-stu-id="fe902-163">If a record for **Litware, Inc.** (`https://www.litware.com`) already exists, skip the next procedure, [Add a new ER configuration provider](#ActivateProvider).</span></span>

#### <a name="add-a-new-er-configuration-provider"></a><a id="ActivateProvider"></a><span data-ttu-id="fe902-164">Legg til en ny ER-konfigurasjonsleverandør</span><span class="sxs-lookup"><span data-stu-id="fe902-164">Add a new ER configuration provider</span></span>

1. <span data-ttu-id="fe902-165">Gå til **Organisasjonsstyring** \> **Arbeidsområder** \> **Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="fe902-165">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="fe902-166">På siden **Lokaliseringskonfigurasjoner**, i delen **Relaterte koblinger**, velger du flisen **Konfigurasjonsleverandører**.</span><span class="sxs-lookup"><span data-stu-id="fe902-166">On the **Localization configurations** page, in the **Related links** section, select **Configuration providers**.</span></span>
3. <span data-ttu-id="fe902-167">Velg **Ny** på siden **Konfigurasjonsleverandører**.</span><span class="sxs-lookup"><span data-stu-id="fe902-167">On the **Configuration providers** page, select **New**.</span></span>
4. <span data-ttu-id="fe902-168">I **Navn**-feltet angir du **Litware, Inc.**</span><span class="sxs-lookup"><span data-stu-id="fe902-168">In the **Name** field, enter **Litware, Inc.**</span></span>
5. <span data-ttu-id="fe902-169">I **Internett-adresse**-feltet angir du `https://www.litware.com`.</span><span class="sxs-lookup"><span data-stu-id="fe902-169">In the **Internet address** field, enter `https://www.litware.com`.</span></span>
6. <span data-ttu-id="fe902-170">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="fe902-170">Select **Save**.</span></span>

#### <a name="activate-an-er-configuration-provider"></a><a id="ActivateAddedProvider"></a><span data-ttu-id="fe902-171">Aktivere en ER-konfigurasjonsleverandør</span><span class="sxs-lookup"><span data-stu-id="fe902-171">Activate an ER configuration provider</span></span>

1. <span data-ttu-id="fe902-172">Gå til **Organisasjonsstyring** \> **Arbeidsområder** \> **Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="fe902-172">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="fe902-173">På **Lokaliseringskonfigurasjoner**-siden, i **Konfigurasjonsleverandører**-delen, velger du **Litware, Inc.**-flisen og deretter **Angi aktiv**.</span><span class="sxs-lookup"><span data-stu-id="fe902-173">On the **Localization configurations** page, in the **Configuration providers** section, select the **Litware, Inc.** tile, and then select **Set active**.</span></span>

<span data-ttu-id="fe902-174">Hvis du ha mer informasjon om ER-konfigurasjonsleverandører, kan du se [Opprette konfigurasjonsleverandører og merke dem som aktive](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="fe902-174">For more information about ER configuration providers, see [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>

## <a name="import-the-standard-er-format-configurations"></a><a id="ImportERSolution1"></a><span data-ttu-id="fe902-175">Importer standard ER-formatkonfigurasjoner</span><span class="sxs-lookup"><span data-stu-id="fe902-175">Import the standard ER format configurations</span></span>

### <a name="import-the-standard-er-configurations"></a><a id="ImportERFormat1"></a><span data-ttu-id="fe902-176">Importer standard ER-konfigurasjoner</span><span class="sxs-lookup"><span data-stu-id="fe902-176">Import the standard ER configurations</span></span>

<span data-ttu-id="fe902-177">Hvis du vil legge til standard ER-konfigurasjoner i den gjeldende forekomsten av Microsoft Dynamics 365 Finance, må du importere dem fra ER-[repositoriet](general-electronic-reporting.md#Repository) som ble konfigurert for den forekomsten.</span><span class="sxs-lookup"><span data-stu-id="fe902-177">To add the standard ER configurations to your current instance of Microsoft Dynamics 365 Finance, you must import them from the ER [repository](general-electronic-reporting.md#Repository) that was configured for that instance.</span></span>

1. <span data-ttu-id="fe902-178">Gå til **Organisasjonsstyring** \> **Arbeidsområder** \> **Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="fe902-178">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="fe902-179">På **Lokaliseringskonfigurasjoner**-siden, i **Konfigurasjonsleverandører**-delen, velger du **Microsoft**-flisen og deretter **Repositorier** for å vise listen over repositorier for Microsoft-leverandøren.</span><span class="sxs-lookup"><span data-stu-id="fe902-179">On the **Localization configurations** page, in the **Configuration providers** section, select the **Microsoft** tile, and then select **Repositories** to view the list of repositories for the Microsoft provider.</span></span>
3. <span data-ttu-id="fe902-180">På **Konfigurasjonsrepositorier**-siden velger du repositoriet for **Global**-typen, og deretter velger du **Åpne**.</span><span class="sxs-lookup"><span data-stu-id="fe902-180">On the **Configuration repositories** page, select the repository of the **Global** type, and then select **Open**.</span></span> <span data-ttu-id="fe902-181">Hvis du blir spurt om godkjenning for å koble til Regulatory Configuration Service, følger du godkjenningsinstruksjonene.</span><span class="sxs-lookup"><span data-stu-id="fe902-181">If you're prompted for authorization to connect to Regulatory Configuration Service, follow the authorization instructions.</span></span>
4. <span data-ttu-id="fe902-182">På **Konfigurasjonsrepositorier**-siden går du til konfigurasjonstreet i venstre rute og velger **BBS (Storbritannia)**-formatkonfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="fe902-182">On the **Configuration repository** page, in the configuration tree in the left pane, select the **BACS (UK)** format configuration.</span></span>
5. <span data-ttu-id="fe902-183">I **Versjoner**-hurtigkategorien velger du versjon **1.1** for den valgte ER-formatkonfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="fe902-183">On the **Versions** FastTab, select version **1.1** of the selected ER format configuration.</span></span>
6. <span data-ttu-id="fe902-184">Velg **Importer** for å laste ned den valgte versjonen fra det globale repositoriet til den gjeldende forekomsten av Finance.</span><span class="sxs-lookup"><span data-stu-id="fe902-184">Select **Import** to download the selected version from the Global repository to the current Finance instance.</span></span>

![Konfigurasjonsrepositorium-side](./media/er-quick-start2-import-solution1.png)

> [!TIP]
> <span data-ttu-id="fe902-186">Hvis du har problemer med å få tilgang til det [globale repositoriet](er-download-configurations-global-repo.md), kan du [laste ned konfigurasjoner](download-electronic-reporting-configuration-lcs.md) fra Microsoft Dynamics Lifecycle Services (LCS) i stedet.</span><span class="sxs-lookup"><span data-stu-id="fe902-186">If you have trouble accessing the [Global repository](er-download-configurations-global-repo.md), you can [download configurations](download-electronic-reporting-configuration-lcs.md) from Microsoft Dynamics Lifecycle Services (LCS) instead.</span></span>

### <a name="review-the-imported-er-configurations"></a><a id="ReviewImportedERSolution"></a><span data-ttu-id="fe902-187">Se gjennom importerte ER-konfigurasjoner</span><span class="sxs-lookup"><span data-stu-id="fe902-187">Review the imported ER configurations</span></span>

1. <span data-ttu-id="fe902-188">Gå til **Organisasjonsstyring** \> **Arbeidsområder** \> **Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="fe902-188">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="fe902-189">På siden **Lokaliseringskonfigurasjoner**, i delen **Konfigurasjoner**, velger du flisen **Rapporteringskonfigurasjoner**.</span><span class="sxs-lookup"><span data-stu-id="fe902-189">On the **Localization configurations** page, in the **Configurations** section, select the **Reporting configurations** tile.</span></span>
3. <span data-ttu-id="fe902-190">På **Konfigurasjoner**-siden, i konfigurasjonstreet i venstre rute, utvider du **Betalingsmodell**.</span><span class="sxs-lookup"><span data-stu-id="fe902-190">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**.</span></span>
4. <span data-ttu-id="fe902-191">Legg merke til at i tillegg til det valgte ER-formatet for **BBS (Storbritannia)**, ble andre ER-konfigurasjoner importert.</span><span class="sxs-lookup"><span data-stu-id="fe902-191">Notice that, in addition to the selected **BACS (UK)** ER format, other required ER configurations were imported.</span></span> <span data-ttu-id="fe902-192">Kontroller at følgende ER-konfigurasjoner er tilgjengelige i konfigurasjonstreet:</span><span class="sxs-lookup"><span data-stu-id="fe902-192">Make sure that the following ER configurations are available in the configuration tree:</span></span>

    - <span data-ttu-id="fe902-193">**Betalingsmodell** – denne konfigurasjonen inneholder ER-komponenten for [datamodell](general-electronic-reporting.md#data-model-and-model-mapping-components) som representerer datastrukturen til betalingsforretningsdomenet.</span><span class="sxs-lookup"><span data-stu-id="fe902-193">**Payment model** – This configuration contains the [data model](general-electronic-reporting.md#data-model-and-model-mapping-components) ER component that represents the data structure of the payment business domain.</span></span>
    - <span data-ttu-id="fe902-194">**Betalingsmodelltilordning 1611** – denne konfigurasjonen inneholder ER-komponenten for [modelltilordning](general-electronic-reporting.md#data-model-and-model-mapping-components) som beskriver hvordan datamodellen fylles ut med programdata ved kjøring.</span><span class="sxs-lookup"><span data-stu-id="fe902-194">**Payment model mapping 1611** – This configuration contains the [model mapping](general-electronic-reporting.md#data-model-and-model-mapping-components) ER component that describes how the data model is filled in with application data at runtime.</span></span>
    - <span data-ttu-id="fe902-195">**BBS (Storbritannia)** – denne konfigurasjonen inneholder ER-komponenter for [format](general-electronic-reporting.md#FormatComponentOutbound) og formattilordning.</span><span class="sxs-lookup"><span data-stu-id="fe902-195">**BACS (UK)** – This configuration contains the [format](general-electronic-reporting.md#FormatComponentOutbound) and format mapping ER components.</span></span> <span data-ttu-id="fe902-196">Formatkomponenten angir rapportoppsettet.</span><span class="sxs-lookup"><span data-stu-id="fe902-196">The format component specifies the report layout.</span></span> <span data-ttu-id="fe902-197">Formattilordningskomponenten inneholder modelldatakilden og angir hvordan rapportoppsettet fylles ut ved hjelp av denne datakilden under kjøring.</span><span class="sxs-lookup"><span data-stu-id="fe902-197">The format mapping component contains the model data source and specifies how the report layout is filled in by using this data source at runtime.</span></span>

![Siden Konfigurasjoner](./media/er-quick-start2-imported-solution1.png)

## <a name="prepare-a-vendor-payment-for-processing"></a><a id="PrepareVendorPayment"></a><span data-ttu-id="fe902-199">Klargjøre en leverandørbetaling for behandling</span><span class="sxs-lookup"><span data-stu-id="fe902-199">Prepare a vendor payment for processing</span></span>

### <a name="add-bank-information-for-a-vendor-account"></a><a id="AddBankAccount"></a><span data-ttu-id="fe902-200">Legg til bankinformasjon for en leverandørkonto</span><span class="sxs-lookup"><span data-stu-id="fe902-200">Add bank information for a vendor account</span></span>

<span data-ttu-id="fe902-201">Du må legge til bankinformasjon for en leverandørkonto som skal refereres til senere i en registrert betaling.</span><span class="sxs-lookup"><span data-stu-id="fe902-201">You must add bank information for a vendor account that will be referred to later in a registered payment.</span></span>

1. <span data-ttu-id="fe902-202">Gå til **Leverandører** \> **Leverandører** \> **Alle leverandører**.</span><span class="sxs-lookup"><span data-stu-id="fe902-202">Go to **Accounts payable** \> **Vendors** \> **All vendors**.</span></span>
2. <span data-ttu-id="fe902-203">På **Alle leverandører**-siden velger du **GB_SI_000001**-leverandørkontoen og, i handlingsruten, på **Leverandør**-fanen, i **Definer**-gruppen, velger du **Bankkontoer**.</span><span class="sxs-lookup"><span data-stu-id="fe902-203">On the **All vendors** page, select the **GB_SI_000001** vendor account, and then, on the Action Pane, on the **Vendor** tab, in the **Set up** group, select **Bank accounts**.</span></span>
3. <span data-ttu-id="fe902-204">På **Leverandørbankkontoer**-siden velger du **Ny** og angir deretter følgende informasjon:</span><span class="sxs-lookup"><span data-stu-id="fe902-204">On the **Vendor bank accounts** page, select **New**, and then enter the following information:</span></span>

    1. <span data-ttu-id="fe902-205">Angi **GBP OPER** i feltet **Bankkonto**.</span><span class="sxs-lookup"><span data-stu-id="fe902-205">In the **Bank account** field, enter **GBP OPER**.</span></span>
    2. <span data-ttu-id="fe902-206">Velg **BankGBP** i feltet **Bankgrupper**.</span><span class="sxs-lookup"><span data-stu-id="fe902-206">In the **Bank groups** field, select **BankGBP**.</span></span>
    3. <span data-ttu-id="fe902-207">Angi **202015** i feltet **Bankkontonummer**.</span><span class="sxs-lookup"><span data-stu-id="fe902-207">In the **Bank account number** field, enter **202015**.</span></span>
    4. <span data-ttu-id="fe902-208">Angi <a id="DefineSWIFTCode"></a>**CHASDEFXXXX** i **SWIFT**-feltet.</span><span class="sxs-lookup"><span data-stu-id="fe902-208">In the **SWIFT code** field, enter <a id="DefineSWIFTCode"></a>**CHASDEFXXXX**.</span></span>
    5. <span data-ttu-id="fe902-209">Angi **GB33BUKB20201555555555** i feltet **IBAN**.</span><span class="sxs-lookup"><span data-stu-id="fe902-209">In the **IBAN** field, enter **GB33BUKB20201555555555**.</span></span>
    6. <span data-ttu-id="fe902-210">I **Rutingsnummer**-feltet beholder du standardverdien <a id="DefineRoutingNumber"></a>**123456**.</span><span class="sxs-lookup"><span data-stu-id="fe902-210">In the **Routing number** field, keep the default value, <a id="DefineRoutingNumber"></a>**123456**.</span></span>

    ![Leverandørbankkontoer-side](./media/er-quick-start2-bank-account.png)

4. <span data-ttu-id="fe902-212">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="fe902-212">Select **Save**.</span></span>
5. <span data-ttu-id="fe902-213">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="fe902-213">Close the page.</span></span>
6. <span data-ttu-id="fe902-214">På **Alle leverandører**-siden åpner du **GB_SI_000001**-leverandørkontoen.</span><span class="sxs-lookup"><span data-stu-id="fe902-214">On the **All vendors** page, open the **GB_SI_000001** vendor account.</span></span>
7. <span data-ttu-id="fe902-215">På leverandørdetaljersiden velger du **Rediger** for å gjøre siden redigerbar, ved behov.</span><span class="sxs-lookup"><span data-stu-id="fe902-215">On the vendor details page, select **Edit** to make the page editable, if required.</span></span>
8. <span data-ttu-id="fe902-216">På **Betaling**-hurtigfanen velger du **GBP OPER** i **Bankkonto**-feltet.</span><span class="sxs-lookup"><span data-stu-id="fe902-216">On the **Payment** FastTab, in the **Bank account** field, select **GBP OPER**.</span></span>

    ![Leverandørdetaljerside](./media/er-quick-start2-bank-account-reference.png)

9. <span data-ttu-id="fe902-218">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="fe902-218">Select **Save**.</span></span>
10. <span data-ttu-id="fe902-219">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="fe902-219">Close the page.</span></span>

### <a name="enter-a-vendor-payment"></a><a id="EnterVendorPayment"></a><span data-ttu-id="fe902-220">Angi en leverandørbetaling</span><span class="sxs-lookup"><span data-stu-id="fe902-220">Enter a vendor payment</span></span>

<span data-ttu-id="fe902-221">Du må angi en ny leverandørbetaling ved å bruke et [betalingsforslag](https://docs.microsoft.com/dynamics365/finance/accounts-payable/create-vendor-payments-payment-proposal).</span><span class="sxs-lookup"><span data-stu-id="fe902-221">You must enter a new vendor payment by using a [payment proposal](https://docs.microsoft.com/dynamics365/finance/accounts-payable/create-vendor-payments-payment-proposal).</span></span>

1. <span data-ttu-id="fe902-222">Gå til **Leverandører** \> **Betalinger** \> **Leverandørbetalingsjournal**.</span><span class="sxs-lookup"><span data-stu-id="fe902-222">Go to **Accounts payable** \> **Payments** \> **Vendor payment journal**.</span></span>
2. <span data-ttu-id="fe902-223">Velg **Ny** på siden **Leverandørbetalingsjournal**.</span><span class="sxs-lookup"><span data-stu-id="fe902-223">On the **Vendor payment journal** page, select **New**.</span></span>
3. <span data-ttu-id="fe902-224">Velg **VendPay** i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="fe902-224">In the **Name** field, select **VendPay**.</span></span>
4. <span data-ttu-id="fe902-225">Velg **Linjer**.</span><span class="sxs-lookup"><span data-stu-id="fe902-225">Select **Lines**.</span></span>
5. <span data-ttu-id="fe902-226">Velg **Betalingsforslag** \> **Opprett betalingsforslag**.</span><span class="sxs-lookup"><span data-stu-id="fe902-226">Select **Payment proposal** \> **Create payment proposal**.</span></span>
6. <span data-ttu-id="fe902-227">I **Leverandørbetalingsforslag**-dialogboksen konfigurerer du betingelser for å filtrere poster bare for **GB_SI_000001**-leverandørkontoen, og velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="fe902-227">In the **Vendor payment proposal** dialog box, configure conditions to filter for records for the **GB_SI_000001** vendor account only, and then select **OK**.</span></span>
7. <span data-ttu-id="fe902-228">Velg linjen for **00000007_Inv**-fakturaen, og velg deretter **Opprett betaling**.</span><span class="sxs-lookup"><span data-stu-id="fe902-228">Select the line for the **00000007_Inv** invoice, and then select **Create payment**.</span></span>

    ![Dialogboksen Leverandørbetalingsforslag](./media/er-quick-start2-payment-proposal.png)

8. <span data-ttu-id="fe902-230">Kontroller at betalingen som er angitt, er konfigurert til å bruke **elektronisk** som betalingsmåten.</span><span class="sxs-lookup"><span data-stu-id="fe902-230">Verify that the payment that is entered is configured to use the **Electronic** method of payment.</span></span>

    ![Leverandørbetalinger-siden](./media/er-quick-start2-payment-line.png)

## <a name="process-a-vendor-payment-by-using-the-standard-er-format"></a><a id="ProcessVendorPayment1"></a><span data-ttu-id="fe902-232">Behandle en leverandørbetaling ved hjelp av standard ER-format</span><span class="sxs-lookup"><span data-stu-id="fe902-232">Process a vendor payment by using the standard ER format</span></span>

### <a name="set-up-the-electronic-payment-method"></a><a id="ConfigureMethodOfPayment1"></a><span data-ttu-id="fe902-233">Konfigurere den elektroniske betalingsmåten</span><span class="sxs-lookup"><span data-stu-id="fe902-233">Set up the electronic payment method</span></span>

<span data-ttu-id="fe902-234">Du må konfigurere den elektroniske betalingsmåten slik at den bruker den importerte ER-formatkonfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="fe902-234">You must configure the electronic method of payment so that it uses the imported ER format configuration.</span></span>

1. <span data-ttu-id="fe902-235">Gå til **Leverandører** \> **Betalingsoppsett** \> **Betalingsmåter**.</span><span class="sxs-lookup"><span data-stu-id="fe902-235">Go to **Accounts payable** \> **Payment setup** \> **Methods of payment**.</span></span>
2. <span data-ttu-id="fe902-236">På **Betalingsmåter – leverandører**-siden velger du **elektronisk** betalingsmåte i ruten til venstre.</span><span class="sxs-lookup"><span data-stu-id="fe902-236">On the **Methods of payment - vendors** page, select the **Electronic** method of payment in the left pane.</span></span>
3. <span data-ttu-id="fe902-237">Velg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="fe902-237">Select **Edit**.</span></span>
4. <span data-ttu-id="fe902-238">I hurtigfanen **Filformater** setter du alternativet **Generelt elektronisk eksportformat** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="fe902-238">On the **File formats** FastTab, set the **General electronic Export format** option to **Yes**.</span></span>
5. <span data-ttu-id="fe902-239">I feltet **Eksportformatkonfigurasjon** velger du formatkonfigurasjonen **BBS (Storbritannia)**.</span><span class="sxs-lookup"><span data-stu-id="fe902-239">In the **Export format configuration** field, select the **BACS (UK)** format configuration.</span></span>

    ![Siden Betalingsmåter – leverandører](./media/er-quick-start2-method-of-payment1.png)

6. <span data-ttu-id="fe902-241">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="fe902-241">Select **Save**.</span></span>

### <a name="process-a-vendor-payment"></a><a id="ProcessPayment1"></a><span data-ttu-id="fe902-242">Behandle en leverandørbetaling</span><span class="sxs-lookup"><span data-stu-id="fe902-242">Process a vendor payment</span></span>

1. <span data-ttu-id="fe902-243">Gå til **Leverandører** \> **Betalinger** \> **Leverandørbetalingsjournal**.</span><span class="sxs-lookup"><span data-stu-id="fe902-243">Go to **Accounts payable** \> **Payments** \> **Vendor payment journal**.</span></span>
2. <span data-ttu-id="fe902-244">På siden **Leverandørbetalingsjournal** velger du betalingsjournalen du la til tidligere, og deretter velger du **Linjer**.</span><span class="sxs-lookup"><span data-stu-id="fe902-244">On the **Vendor payment journal** page, select the payment journal that you added earlier, and then select **Lines**.</span></span>
3. <span data-ttu-id="fe902-245">På **Leverandørbetalinger**-siden velger du **Generer betalinger**.</span><span class="sxs-lookup"><span data-stu-id="fe902-245">On the **Vendor payments** page, select **Generate payments**.</span></span>
4. <span data-ttu-id="fe902-246">Angi følgende informasjon i dialogboksen **Generer betalinger**:</span><span class="sxs-lookup"><span data-stu-id="fe902-246">In the **Generate payments** dialog box, enter the following information:</span></span>

    - <span data-ttu-id="fe902-247">Velg **Elektronisk** i feltet **Betalingsmåte**.</span><span class="sxs-lookup"><span data-stu-id="fe902-247">In the **Method of payment** field, select **Electronic**.</span></span>
    - <span data-ttu-id="fe902-248">Velg **GBSI OPER** i feltet **Bankkonto**.</span><span class="sxs-lookup"><span data-stu-id="fe902-248">In the **Bank account** field, select **GBSI OPER**.</span></span>

5. <span data-ttu-id="fe902-249">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="fe902-249">Select **OK**.</span></span>
6. <span data-ttu-id="fe902-250">I **Parametere for elektronisk rapport**-dialogboksen setter du **Skriv ut kontrollrapport** til **Ja**, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="fe902-250">In the **Electronic report parameters** dialog box, set the **Print control report** option to **Yes**, and then select **OK**.</span></span>

    ![Dialogsiden Parametere for elektronisk rapport](./media/er-quick-start2-payment-dialog1.png)

    > [!NOTE]
    > <span data-ttu-id="fe902-252">I tillegg til betalingsfilen kan du nå generere kontrollrapporten.</span><span class="sxs-lookup"><span data-stu-id="fe902-252">In addition to the payment file, you can now generate the control report.</span></span>

7. <span data-ttu-id="fe902-253">Last ned zip-filen, og pakk deretter ut følgende filer:</span><span class="sxs-lookup"><span data-stu-id="fe902-253">Download the zip file, and then extract the following files from it:</span></span>

    - <span data-ttu-id="fe902-254">Kontrollrapporten i Excel-format</span><span class="sxs-lookup"><span data-stu-id="fe902-254">The control report in Excel format</span></span>
    - <span data-ttu-id="fe902-255">Betalingsfilen i TXT-format</span><span class="sxs-lookup"><span data-stu-id="fe902-255">The payment file in TXT format</span></span>

        <span data-ttu-id="fe902-256">Legg merke til at i henhold til [strukturen](#PositionRoutingNumber) for angitt ER-format, vil betalingslinjen i den genererte filen starte med rutingsnummeret som ble [definert](#DefineRoutingNumber) for den konfigurerte bankkontoen.</span><span class="sxs-lookup"><span data-stu-id="fe902-256">Notice that, in accordance with the [structure](#PositionRoutingNumber) of the provided ER format, the payment line in the generated file starts with the routing number that was [defined](#DefineRoutingNumber) for the configured bank account.</span></span>

        ![Betalingsfil i TXT-format](./media/er-quick-start2-payment-file1.png)

## <a name="customize-the-standard-er-format"></a><a id="CustomizeProvidedFormat"></a><span data-ttu-id="fe902-258">Tilpasse standard ER-format</span><span class="sxs-lookup"><span data-stu-id="fe902-258">Customize the standard ER format</span></span>

<span data-ttu-id="fe902-259">For eksemplet som vises i denne delen, vil du bruke ER-konfigurasjonene som leveres av Microsoft, til å generere leverandørbetalingsfiler i BBS-format, men du må legge til en tilpasning for å støtte kravene til en bestemt bank.</span><span class="sxs-lookup"><span data-stu-id="fe902-259">For the example that is shown in this section, you want to use the ER configurations that are provided by Microsoft to generate vendor payment files in BACS format, but you must add a customization to support the requirements of a specific bank.</span></span> <span data-ttu-id="fe902-260">Du vil også ha muligheten til å oppgradere det egendefinerte formatet når nye versjoner av ER-konfigurasjoner blir tilgjengelige.</span><span class="sxs-lookup"><span data-stu-id="fe902-260">You also want to be able to upgrade your custom format when new versions of ER configurations become available.</span></span> <span data-ttu-id="fe902-261">Du vil imidlertid ha muligheten til å utføre oppgraderingen til den laveste kostnaden.</span><span class="sxs-lookup"><span data-stu-id="fe902-261">However, you want to be able to do the upgrade at the lowest cost.</span></span>

<span data-ttu-id="fe902-262">I dette tilfellet må du som representanten for Litware, Inc., opprette (avlede) en ny ER-formatkonfigurasjon ved å bruke **BBS (Storbritannia)**-konfigurasjonen fra Microsoft som et grunnlag.</span><span class="sxs-lookup"><span data-stu-id="fe902-262">In this case, as the representative of Litware, Inc., you must create (derive) a new ER format configuration by using the **BACS (UK)** Microsoft-provided configuration as a base.</span></span>

### <a name="create-a-custom-format"></a><a id="DeriveProvidedFormat"></a><span data-ttu-id="fe902-263">Opprette et egendefinert format</span><span class="sxs-lookup"><span data-stu-id="fe902-263">Create a custom format</span></span>

1. <span data-ttu-id="fe902-264">Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Konfigurasjoner**.</span><span class="sxs-lookup"><span data-stu-id="fe902-264">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="fe902-265">På **Konfigurasjoner**-siden, i konfigurasjonstreet i venstre rute, utvider du **Betalingsmodell** og velger **BBS (Storbritannia)**.</span><span class="sxs-lookup"><span data-stu-id="fe902-265">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**, and then select **BACS (UK)**.</span></span> <span data-ttu-id="fe902-266">Litware, Inc. bruker versjon 1.1 av denne ER-formatkonfigurasjonen som grunnlaget for den egendefinerte versjonen.</span><span class="sxs-lookup"><span data-stu-id="fe902-266">Litware, Inc. will use version 1.1 of this ER format configuration as the base for the custom version.</span></span>
3. <span data-ttu-id="fe902-267">Velg **Opprett konfigurasjon** for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="fe902-267">Select **Create configuration** to open the drop-down dialog box.</span></span> <span data-ttu-id="fe902-268">Du kan bruke denne dialogboksen til å opprette en ny konfigurasjon for et egendefinert betalingsformat.</span><span class="sxs-lookup"><span data-stu-id="fe902-268">You can use this dialog box to create a new configuration for a custom payment format.</span></span>
4. <span data-ttu-id="fe902-269">I **Ny**-feltgruppen velger du alternativet **Avled fra navn: BBS (Storbritannia), Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="fe902-269">In the **New** field group, select the **Derive from Name: BACS (UK), Microsoft** option.</span></span>
5. <span data-ttu-id="fe902-270">Angi **BBS (Storbritannia egendefinert)** i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="fe902-270">In the **Name** field, enter **BACS (UK custom)**.</span></span>

    ![Rullegardinlisten Opprett konfigurasjon](./media/er-quick-start2-add-derived-format.png)

6. <span data-ttu-id="fe902-272">Velg **Opprett konfigurasjon**.</span><span class="sxs-lookup"><span data-stu-id="fe902-272">Select **Create configuration**.</span></span>

<span data-ttu-id="fe902-273">Versjon 1.1.1 av ER-formatkonfigurasjonen **BBS (Storbritannia egendefinert)** er opprettet.</span><span class="sxs-lookup"><span data-stu-id="fe902-273">Version 1.1.1 of the **BACS (UK custom)** ER format configuration is created.</span></span> <span data-ttu-id="fe902-274">Denne versjonen har [statusen](general-electronic-reporting.md#component-versioning) **Utkast** og kan redigeres.</span><span class="sxs-lookup"><span data-stu-id="fe902-274">This version has a [status](general-electronic-reporting.md#component-versioning) of **Draft** and can be edited.</span></span> <span data-ttu-id="fe902-275">Det gjeldende innholdet i egendefinert ER-format samsvarer med innholdet i formatet som leveres av Microsoft.</span><span class="sxs-lookup"><span data-stu-id="fe902-275">The current content of your custom ER format matches the content of the format that is provided by Microsoft.</span></span>

![Siden Konfigurasjoner](./media/er-quick-start2-derived-format-configuration1.png)

### <a name="edit-a-custom-format"></a><a id="ConfigureDerivedFormat"></a><span data-ttu-id="fe902-277">Redigere et egendefinert format</span><span class="sxs-lookup"><span data-stu-id="fe902-277">Edit a custom format</span></span>

<span data-ttu-id="fe902-278">Du må konfigurere det egendefinerte formatet slik at det overholder bankspesifikke krav.</span><span class="sxs-lookup"><span data-stu-id="fe902-278">You must configure your custom format so that it meets bank-specific requirements.</span></span> <span data-ttu-id="fe902-279">En bank kan for eksempel kreve at betalingsfiler som genereres, omfatter SWIFT-koden (Society for Worldwide Interbank Financial Telecommunication) til en bank som er tilordnet agentrollen i den behandlede leverandørbetalingen.</span><span class="sxs-lookup"><span data-stu-id="fe902-279">For example, a bank might require that payment files that are generated include the Society for Worldwide Interbank Financial Telecommunication (SWIFT) code of a bank that is assigned the agent role in the processed vendor payment.</span></span> <span data-ttu-id="fe902-280">SWIFT-koder er internasjonale bankkoder som identifiserer bestemte banker over hele verden.</span><span class="sxs-lookup"><span data-stu-id="fe902-280">SWIFT codes are international bank codes that identify specific banks worldwide.</span></span> <span data-ttu-id="fe902-281">De kalles også bank-ID-koder (BIC-er).</span><span class="sxs-lookup"><span data-stu-id="fe902-281">They are also known as Bank Identifier Codes (BICs).</span></span> <span data-ttu-id="fe902-282">SWIFT-koden må ha en lengde på 11 tegn, og den må angis på begynnelsen av hver betalingslinje i en generert betalingsfil.</span><span class="sxs-lookup"><span data-stu-id="fe902-282">The SWIFT code must be 11 characters long, and it must be entered at the beginning of every payment line in a generated payment file.</span></span>

1. <span data-ttu-id="fe902-283">Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Konfigurasjoner**.</span><span class="sxs-lookup"><span data-stu-id="fe902-283">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="fe902-284">På **Konfigurasjoner**-siden, i konfigurasjonstreet i venstre rute, utvider du **Betalingsmodell** og velger **BBS (Storbritannia egendefinert)**.</span><span class="sxs-lookup"><span data-stu-id="fe902-284">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**, and then select **BACS (UK custom)**.</span></span>
3. <span data-ttu-id="fe902-285">I **Versjoner**-hurtigkategorien velger du versjon **1.1.1** for den valgte konfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="fe902-285">On the **Versions** FastTab, select version **1.1.1** of the selected configuration.</span></span>
4. <span data-ttu-id="fe902-286">Velg **Utforming**.</span><span class="sxs-lookup"><span data-stu-id="fe902-286">Select **Designer**.</span></span>
5. <span data-ttu-id="fe902-287">På **Formatutforming**-siden velger du **Vis detaljer** for å vise mer informasjon om formatelementene.</span><span class="sxs-lookup"><span data-stu-id="fe902-287">On the **Format designer** page, select **Show details** to view more information about the format elements.</span></span>
6. <span data-ttu-id="fe902-288">Vis og gå gjennom følgende elementer:</span><span class="sxs-lookup"><span data-stu-id="fe902-288">Expand and review the following elements:</span></span>

    - <span data-ttu-id="fe902-289">**BACSReportsFolder**-elementet for **Mappe**-typen.</span><span class="sxs-lookup"><span data-stu-id="fe902-289">The **BACSReportsFolder** element of the **Folder** type.</span></span> <span data-ttu-id="fe902-290">Dette elementet brukes til å generere utdata i ZIP-format.</span><span class="sxs-lookup"><span data-stu-id="fe902-290">This element is used to generate output in ZIP format.</span></span>
    - <span data-ttu-id="fe902-291">**Fil**-elementet for **Fil**-typen.</span><span class="sxs-lookup"><span data-stu-id="fe902-291">The **file** element of the **File** type.</span></span> <span data-ttu-id="fe902-292">Dette elementet brukes til å generere en betalingsfil i TXT-format.</span><span class="sxs-lookup"><span data-stu-id="fe902-292">This element is used to generate a payment file in TXT format.</span></span>
    - <span data-ttu-id="fe902-293">**Transaksjoner**-elementet for **Sekvens**-typen.</span><span class="sxs-lookup"><span data-stu-id="fe902-293">The **transactions** element of the **Sequence** type.</span></span> <span data-ttu-id="fe902-294">Dette elementet brukes til å generere en enkelt betalingslinje i en betalingsfil.</span><span class="sxs-lookup"><span data-stu-id="fe902-294">This element is used to generate a single payment line in a payment file.</span></span>
    - <span data-ttu-id="fe902-295">**Transaksjon**-elementet for **Sekvens**-typen.</span><span class="sxs-lookup"><span data-stu-id="fe902-295">The **transaction** element of the **Sequence** type.</span></span> <span data-ttu-id="fe902-296">Dette elementet brukes til å generere individuelle felter for en enkelt betalingslinje.</span><span class="sxs-lookup"><span data-stu-id="fe902-296">This element is used to generate individual fields of a single payment line.</span></span>

7. <span data-ttu-id="fe902-297">Velg **transaksjon**-elementet.</span><span class="sxs-lookup"><span data-stu-id="fe902-297">Select the **transaction** element.</span></span>

    ![Transaksjonselement i ER-operasjonsutforming](./media/er-quick-start2-derived-format0.png)

    > [!NOTE]
    > <span data-ttu-id="fe902-299">Den angitte rapporten er konfigurert slik at <a id="PositionRoutingNumber"></a>alle betalingslinjer starter med bankregistreringsnummeret.</span><span class="sxs-lookup"><span data-stu-id="fe902-299">The provided report is configured so that <a id="PositionRoutingNumber"></a>every payment line starts with the bank routing number.</span></span> <span data-ttu-id="fe902-300">**VendBankRouteNum**-formatelementet brukes til dette formålet.</span><span class="sxs-lookup"><span data-stu-id="fe902-300">The **vendBankRouteNum** format element is used for this purpose.</span></span> 

8. <span data-ttu-id="fe902-301">Velg **Legg til**, og velg deretter **Tekst\\streng**-typen for formatelementet du legger til:</span><span class="sxs-lookup"><span data-stu-id="fe902-301">Select **Add**, and then select the **Text\\String** type of the format element that you're adding:</span></span>

    1. <span data-ttu-id="fe902-302">I **Navn**-feltet angir du **vendBankSWIFT**.</span><span class="sxs-lookup"><span data-stu-id="fe902-302">In the **Name** field, enter **vendBankSWIFT**.</span></span>
    2. <span data-ttu-id="fe902-303">Angi **11** i feltet **Minimumslengde**.</span><span class="sxs-lookup"><span data-stu-id="fe902-303">In the **Minimum length** field, enter **11**.</span></span>
    3. <span data-ttu-id="fe902-304">Angi **11** i feltet **Maksimumslengde**.</span><span class="sxs-lookup"><span data-stu-id="fe902-304">In the **Maximum length** field, enter **11**.</span></span>
    4. <span data-ttu-id="fe902-305">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="fe902-305">Select **OK**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="fe902-306">**VendBankSWIFT**-elementet vil bli brukt til å angi SWIFT-koden til en leverandørbank i genererte filer.</span><span class="sxs-lookup"><span data-stu-id="fe902-306">The **vendBankSWIFT** element will be used to enter the SWIFT code of a vendor bank in generated files.</span></span>

9. <span data-ttu-id="fe902-307">Velg **vendBankSWIFT** i formatstrukturtreet.</span><span class="sxs-lookup"><span data-stu-id="fe902-307">In the format structure tree, select **vendBankSWIFT**.</span></span>
10. <span data-ttu-id="fe902-308">Velg **Flytt opp** for å flytte det valgte formatelementet opp ett nivå.</span><span class="sxs-lookup"><span data-stu-id="fe902-308">Select **Move up** to move the selected format element up one level.</span></span> <span data-ttu-id="fe902-309">Gjenta dette trinnet til **vendBankSWIFT**-elementet er det <a id="PositionSWIFTCode"></a>første elementet under det overordnede **transaksjons**elementet.</span><span class="sxs-lookup"><span data-stu-id="fe902-309">Repeat this step until the **vendBankSWIFT** element is the <a id="PositionSWIFTCode"></a>first element under the parent **transaction** element.</span></span>

    ![VendBankSWIFT som det første elementet under transaksjon i ER-operasjonsutforming](./media/er-quick-start2-derived-format1.png)

11. <span data-ttu-id="fe902-311">Mens **vendBankSWIFT** fremdeles er valgt i formatstrukturtreet, velger du **Tilordning**-fanen og utvider datakilden **modell**.</span><span class="sxs-lookup"><span data-stu-id="fe902-311">While the **vendBankSWIFT** is still selected in the format structure tree, select the **Mapping** tab, and then expand the **model** data source.</span></span>
12. <span data-ttu-id="fe902-312">Utvid **model.Payment** \> **model.Payment.CreditorAgent**, og velg **model.Payment.CreditorAgent.BICFI**-datakildefelt.</span><span class="sxs-lookup"><span data-stu-id="fe902-312">Expand **model.Payment** \> **model.Payment.CreditorAgent**, and select the **model.Payment.CreditorAgent.BICFI** data source field.</span></span> <span data-ttu-id="fe902-313">Dette datakildefeltet viser SWIFT-koden til en leverandørbank som er tilordnet agentrollen i den behandlede leverandørbetalingen.</span><span class="sxs-lookup"><span data-stu-id="fe902-313">This data source field exposes the SWIFT code of a vendor bank that is assigned the agent role in the processed vendor payment.</span></span>
13. <span data-ttu-id="fe902-314">Velg **Bind**.</span><span class="sxs-lookup"><span data-stu-id="fe902-314">Select **Bind**.</span></span> <span data-ttu-id="fe902-315">Formatelementet **vendBankSWIFT** er nå bundet med **model.CreditorAgent.BICFI** -datakilden, slik at SWIFT-koder blir angitt i genererte betalingsfiler.</span><span class="sxs-lookup"><span data-stu-id="fe902-315">The **vendBankSWIFT** format element is now bound with the **model.Payment.CreditorAgent.BICFI** data source field, so that SWIFT codes will be entered in generated payment files.</span></span>

    ![vendBankSWIFT-formatelementet som er bundet til model.Payment.CreditorAgent.BICFI-datakildefeltet i ER-operasjonsutforming](./media/er-quick-start2-derived-format2.png)

14. <span data-ttu-id="fe902-317">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="fe902-317">Select **Save**.</span></span>
15. <span data-ttu-id="fe902-318">Lukk utformingssiden.</span><span class="sxs-lookup"><span data-stu-id="fe902-318">Close the designer page.</span></span>

### <a name="mark-a-custom-format-as-runnable"></a><a id="MarkFormatRunnable"></a><span data-ttu-id="fe902-319">Merke et egendefinert format som kjørbart</span><span class="sxs-lookup"><span data-stu-id="fe902-319">Mark a custom format as runnable</span></span>

<span data-ttu-id="fe902-320">Nå som den første versjonen av det egendefinerte formatet er opprettet og har statusen **Utkast**, kan du kjøre det for testformål.</span><span class="sxs-lookup"><span data-stu-id="fe902-320">Now that the first version of your custom format has been created and has a status of **Draft**, you can run it for testing purposes.</span></span> <span data-ttu-id="fe902-321">Når du skal kjøre rapporten, må du behandle en leverandørbetaling ved å bruke betalingsmåten som refererer til det egendefinerte ER-formatet.</span><span class="sxs-lookup"><span data-stu-id="fe902-321">To run the report, you must process a vendor payment by using the payment method that refers to your custom ER format.</span></span> <span data-ttu-id="fe902-322">Som standard [vurderes](general-electronic-reporting.md#component-versioning) bare versjonene som har statusen **Fullført** eller **Delt** når du kaller opp et ER-format fra programmet.</span><span class="sxs-lookup"><span data-stu-id="fe902-322">By default, when you call an ER format from the application, only versions that have a status of **Completed** or **Shared** are [considered](general-electronic-reporting.md#component-versioning).</span></span> <span data-ttu-id="fe902-323">Denne virkemåten hjelper til med å forhindre at ER-formater som har uferdige utforminger, brukes.</span><span class="sxs-lookup"><span data-stu-id="fe902-323">This behavior helps prevent ER formats that have unfinished designs from being used.</span></span> <span data-ttu-id="fe902-324">Testingen kjøres imidlertid ved at du kan tvinge programmet til å bruke versjonen av ER-formatet som har statusen **Utkast**.</span><span class="sxs-lookup"><span data-stu-id="fe902-324">However, for your test runs, you can force the application to use the version of your ER format that has a status of **Draft**.</span></span> <span data-ttu-id="fe902-325">På denne måten kan du justere gjeldende formatversjon hvis det kreves endringer.</span><span class="sxs-lookup"><span data-stu-id="fe902-325">In this way, you can adjust the current format version if any modifications are required.</span></span> <span data-ttu-id="fe902-326">Hvis du vil ha mer informasjon, kan du se [Relevans](electronic-reporting-destinations.md#applicability).</span><span class="sxs-lookup"><span data-stu-id="fe902-326">For more information, see [Applicability](electronic-reporting-destinations.md#applicability).</span></span>

<span data-ttu-id="fe902-327">Hvis du vil bruke utkastversjonen av et ER-format, må du eksplisitt markere ER-formatet.</span><span class="sxs-lookup"><span data-stu-id="fe902-327">To use the draft version of an ER format, you must explicitly mark the ER format.</span></span>

1. <span data-ttu-id="fe902-328">Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Konfigurasjoner**.</span><span class="sxs-lookup"><span data-stu-id="fe902-328">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="fe902-329">På **Konfigurasjoner**-siden, i handlingsruten i kategorien **Konfigurasjoner** i gruppen **Avanserte innstillinger**, velger du **Brukerparametere**.</span><span class="sxs-lookup"><span data-stu-id="fe902-329">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="fe902-330">I dialogboksen **Brukerparametere** setter du **Kjøringsinnstillinger** til **Ja**, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="fe902-330">In the **User parameters** dialog box, set the **Run settings** option to **Yes**, and then select **OK**.</span></span>
4. <span data-ttu-id="fe902-331">Velg **Rediger** for å gjøre gjeldende side redigerbar, hvis nødvendig.</span><span class="sxs-lookup"><span data-stu-id="fe902-331">Select **Edit** to make the current page editable, as required.</span></span>
5. <span data-ttu-id="fe902-332">I konfigurasjonstreet i venstre rute velger du **BBS (Storbritannia)**.</span><span class="sxs-lookup"><span data-stu-id="fe902-332">In the configuration tree in the left pane, select **BACS (UK custom)**.</span></span>
6. <span data-ttu-id="fe902-333">Sett **Kjør utkast**-alternativet til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="fe902-333">Set the **Run Draft** option to **Yes**.</span></span>

    ![Alternativet Kjør utkast på Konfigurasjoner-siden](./media/er-quick-start2-derived-format-configuration2.png)

## <a name="process-a-vendor-payment-by-using-the-custom-er-format"></a><a id="ProcessVendorPayment2"></a><span data-ttu-id="fe902-335">Behandle en leverandørbetaling ved hjelp av egendefinert ER-format</span><span class="sxs-lookup"><span data-stu-id="fe902-335">Process a vendor payment by using the custom ER format</span></span>

### <a name="set-up-the-electronic-payment-method"></a><a id="ConfigureMethodOfPayment2"></a><span data-ttu-id="fe902-336">Konfigurere den elektroniske betalingsmåten</span><span class="sxs-lookup"><span data-stu-id="fe902-336">Set up the electronic payment method</span></span>

<span data-ttu-id="fe902-337">Du må konfigurere den elektroniske betalingsmåten slik at det egendefinerte ER-formatet brukes til å behandle leverandørbetalinger.</span><span class="sxs-lookup"><span data-stu-id="fe902-337">You must configure the electronic method of payment so that your custom ER format is used to process vendor payments.</span></span>

1. <span data-ttu-id="fe902-338">Gå til **Leverandører** \> **Betalingsoppsett** \> **Betalingsmåter**.</span><span class="sxs-lookup"><span data-stu-id="fe902-338">Go to **Accounts payable** \> **Payment setup** \> **Methods of payment**.</span></span>
2. <span data-ttu-id="fe902-339">På **Betalingsmåter – leverandører**-siden velger du **elektronisk** betalingsmåte i ruten til venstre.</span><span class="sxs-lookup"><span data-stu-id="fe902-339">On the **Methods of payment - vendors** page, select the **Electronic** method of payment in the left pane.</span></span>
3. <span data-ttu-id="fe902-340">Velg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="fe902-340">Select **Edit**.</span></span>
4. <span data-ttu-id="fe902-341">I hurtigfanen **Filformat** setter du alternativet **Generelt elektronisk eksportformat** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="fe902-341">On the **File format** FastTab, set the **General electronic export format** option to **Yes**.</span></span>
5. <span data-ttu-id="fe902-342">I feltet **Eksportformatkonfigurasjon** velger du formatkonfigurasjonen **BBS (Storbritannia egendefinert)**.</span><span class="sxs-lookup"><span data-stu-id="fe902-342">In the **Export format configuration** field, select the **BACS (UK custom)** format configuration.</span></span>

    ![Siden Betalingsmåter – leverandører](./media/er-quick-start2-method-of-payment2.png)

6. <span data-ttu-id="fe902-344">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="fe902-344">Select **Save**.</span></span>

### <a name="process-a-vendor-payment"></a><a id="ProcessPayment2"></a><span data-ttu-id="fe902-345">Behandle en leverandørbetaling</span><span class="sxs-lookup"><span data-stu-id="fe902-345">Process a vendor payment</span></span>

1. <span data-ttu-id="fe902-346">Gå til **Leverandører** \> **Betalinger** \> **Leverandørbetalingsjournal**.</span><span class="sxs-lookup"><span data-stu-id="fe902-346">Go to **Accounts payable** \> **Payments** \> **Vendor payment journal**.</span></span>
2. <span data-ttu-id="fe902-347">På siden **Leverandørbetalingsjournal** velger du betalingsjournalen du opprettet tidligere.</span><span class="sxs-lookup"><span data-stu-id="fe902-347">On the **Vendor payment journal** page, select the payment journal that you created earlier.</span></span>
3. <span data-ttu-id="fe902-348">Velg **Linjer**.</span><span class="sxs-lookup"><span data-stu-id="fe902-348">Select **Lines**.</span></span>
4. <span data-ttu-id="fe902-349">På **Leverandørbetalinger**-siden velger du **Betalingsstatus** \> **Ingen** over rutenettet.</span><span class="sxs-lookup"><span data-stu-id="fe902-349">On the **Vendor payments** page, above the grid, select **Payment status** \> **None**.</span></span>
5. <span data-ttu-id="fe902-350">Velg **Generer betaling**.</span><span class="sxs-lookup"><span data-stu-id="fe902-350">Select **Generate payment**.</span></span>
6. <span data-ttu-id="fe902-351">Angi følgende informasjon i dialogboksen **Generer betalinger**:</span><span class="sxs-lookup"><span data-stu-id="fe902-351">In the **Generate payments** dialog box, enter the following information:</span></span>

    - <span data-ttu-id="fe902-352">Velg **Elektronisk** i feltet **Betalingsmåte**.</span><span class="sxs-lookup"><span data-stu-id="fe902-352">In the **Method of payment** field, select **Electronic**.</span></span>
    - <span data-ttu-id="fe902-353">Velg **GBSI OPER** i feltet **Bankkonto**.</span><span class="sxs-lookup"><span data-stu-id="fe902-353">In the **Bank account** field, select **GBSI OPER**.</span></span>

7. <span data-ttu-id="fe902-354">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="fe902-354">Select **OK**.</span></span>
8. <span data-ttu-id="fe902-355">I **Parametere for elektronisk rapport**-dialogboksen setter du **Skriv ut kontrollrapport** til **Ja**, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="fe902-355">In the **Electronic report parameters** dialog box, set the **Print control report** option to **Yes**, and then select **OK**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="fe902-356">I tillegg til betalingsfilen kan du bare generere kontrollrapporten.</span><span class="sxs-lookup"><span data-stu-id="fe902-356">In addition to the payment file, you can generate only the control report.</span></span>

9. <span data-ttu-id="fe902-357">Last ned zip-filen, og pakk deretter ut følgende filer:</span><span class="sxs-lookup"><span data-stu-id="fe902-357">Download the zip file, and then extract the following files from it:</span></span>

    - <span data-ttu-id="fe902-358">Kontrollrapporten i Excel-format</span><span class="sxs-lookup"><span data-stu-id="fe902-358">The control report in Excel format</span></span>
    - <span data-ttu-id="fe902-359">Betalingsfilen i TXT-format</span><span class="sxs-lookup"><span data-stu-id="fe902-359">The payment file in TXT format</span></span>

        <span data-ttu-id="fe902-360">Legg merke til at i henhold til strukturen i egendefinert ER-format, [starter](#PositionSWIFTCode) betalingslinjen i den genererte filen nå med SWIFT-koden som ble [angitt](#DefineSWIFTCode) for bankkontoen til leverandøren som har utført betalingen.</span><span class="sxs-lookup"><span data-stu-id="fe902-360">Notice that, in accordance with the structure of your custom ER format, the payment line in the generated file now [starts](#PositionSWIFTCode) with the SWIFT code that was [entered](#DefineSWIFTCode) for the bank account of the vendor whose payment has been processed.</span></span>

        ![Betalingsfil i TXT-format](./media/er-quick-start2-payment-file2.png)

## <a name="import-new-versions-of-the-standard-er-format-configurations"></a><a id="ImportERSolution2"></a><span data-ttu-id="fe902-362">Importer nye versjoner av standard ER-formatkonfigurasjoner</span><span class="sxs-lookup"><span data-stu-id="fe902-362">Import new versions of the standard ER format configurations</span></span>

<span data-ttu-id="fe902-363">For eksemplet som vises i denne delen, mottar du en melding om Kunnskapsbaseartikkel [KB3763330](https://fix.lcs.dynamics.com/Issue/Details?kb=3182046).</span><span class="sxs-lookup"><span data-stu-id="fe902-363">For the example that is shown in this section, you receive a notification about Knowledge Base article [KB3763330](https://fix.lcs.dynamics.com/Issue/Details?kb=3182046).</span></span> <span data-ttu-id="fe902-364">Dette varselet informerer deg om den nye versjonen av ER-formatet **BBS (Storbritannia)** er publisert av Microsoft.</span><span class="sxs-lookup"><span data-stu-id="fe902-364">This notification informs you about the new version of the **BACS (UK)** ER format that has been published by Microsoft.</span></span> <span data-ttu-id="fe902-365">I tillegg til kontrollrapporten lar denne nye versjonen brukere generere betalingsmeldingsrapporten og deltakernotatrapporten mens en leverandørbetaling blir behandlet.</span><span class="sxs-lookup"><span data-stu-id="fe902-365">In addition to the control report, this new version lets users generate the payment advice report and the attending note report while a vendor payment is being processed.</span></span> <span data-ttu-id="fe902-366">Du vil begynne å bruke denne funksjonaliteten.</span><span class="sxs-lookup"><span data-stu-id="fe902-366">You want to start to use that functionality.</span></span>

### <a name="import-new-versions-of-the-standard-er-configurations"></a><a id="ImportERFormat2"></a><span data-ttu-id="fe902-367">Importer nye versjoner av standard ER-konfigurasjoner</span><span class="sxs-lookup"><span data-stu-id="fe902-367">Import new versions of the standard ER configurations</span></span>

<span data-ttu-id="fe902-368">Hvis du vil legge til nye versjoner av ER-konfigurasjoner i den gjeldende Finance-forekomsten, må du importere dem fra ER-[repositoriet](general-electronic-reporting.md#Repository) som du har konfigurert.</span><span class="sxs-lookup"><span data-stu-id="fe902-368">To add new versions of the ER configurations to the current Finance instance, you must import them from the ER [repository](general-electronic-reporting.md#Repository) that you've configured.</span></span>

1. <span data-ttu-id="fe902-369">Gå til **Organisasjonsstyring** \> **Arbeidsområder** \> **Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="fe902-369">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="fe902-370">På **Lokaliseringskonfigurasjoner**-siden, i **Konfigurasjonsleverandører**-delen, velger du **Microsoft**-flisen og deretter **Repositorier** for å vise listen over repositorier for Microsoft-leverandøren.</span><span class="sxs-lookup"><span data-stu-id="fe902-370">On the **Localization configurations** page, in the **Configuration providers** section, select the **Microsoft** tile, and then select **Repositories** to view the list of repositories for the Microsoft provider.</span></span>
3. <span data-ttu-id="fe902-371">På **Konfigurasjonsrepositorier**-siden velger du repositoriet for **Global**-typen, og deretter velger du **Åpne**.</span><span class="sxs-lookup"><span data-stu-id="fe902-371">On the **Configuration repositories** page, select the repository of the **Global** type, and then select **Open**.</span></span> <span data-ttu-id="fe902-372">Hvis du blir spurt om godkjenning for å koble til Regulatory Configuration Service, følger du godkjenningsinstruksjonene.</span><span class="sxs-lookup"><span data-stu-id="fe902-372">If you're prompted for authorization to connect to Regulatory Configuration Service, follow the authorization instructions.</span></span>
4. <span data-ttu-id="fe902-373">På **Konfigurasjonsrepositorier**-siden går du til konfigurasjonstreet i venstre rute og velger **BBS (Storbritannia)**-formatkonfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="fe902-373">On the **Configuration repository** page, in the configuration tree in the left pane, select the **BACS (UK)** format configuration.</span></span>
5. <span data-ttu-id="fe902-374">I **Versjoner**-hurtigkategorien velger du versjon **3.3** for den valgte ER-formatkonfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="fe902-374">On the **Versions** FastTab, select version **3.3** of the selected ER format configuration.</span></span>
6. <span data-ttu-id="fe902-375">Velg **Importer** for å laste ned den valgte versjonen fra det globale repositoriet til den gjeldende forekomsten av Finance.</span><span class="sxs-lookup"><span data-stu-id="fe902-375">Select **Import** to download the selected version from the Global repository to the current Finance instance.</span></span>

![Konfigurasjonsrepositorium-side](./media/er-quick-start2-import-solution2.png)

> [!TIP]
> <span data-ttu-id="fe902-377">Hvis du har problemer med å få tilgang til det [globale repositoriet](er-download-configurations-global-repo.md), kan du [laste ned konfigurasjoner](download-electronic-reporting-configuration-lcs.md) fra LCS i stedet.</span><span class="sxs-lookup"><span data-stu-id="fe902-377">If you have trouble accessing the [Global repository](er-download-configurations-global-repo.md), you can [download configurations](download-electronic-reporting-configuration-lcs.md) from LCS instead.</span></span>

### <a name="review-the-imported-er-format-configurations"></a><a id="ReviewImportedERFormat"></a><span data-ttu-id="fe902-378">Se gjennom importerte ER-formatkonfigurasjoner</span><span class="sxs-lookup"><span data-stu-id="fe902-378">Review the imported ER format configurations</span></span>

1. <span data-ttu-id="fe902-379">Gå til **Organisasjonsstyring** \> **Arbeidsområder** \> **Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="fe902-379">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="fe902-380">På siden **Lokaliseringskonfigurasjoner**, i delen **Konfigurasjoner**, velger du flisen **Rapporteringskonfigurasjoner**.</span><span class="sxs-lookup"><span data-stu-id="fe902-380">On the **Localization configurations** page, in the **Configurations** section, select the **Reporting configurations** tile.</span></span>
3. <span data-ttu-id="fe902-381">På **Konfigurasjoner**-siden, i konfigurasjonstreet i venstre rute, utvider du **Betalingsmodell** og velger **BBS (Storbritannia)**.</span><span class="sxs-lookup"><span data-stu-id="fe902-381">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**, and then select **BACS (UK)**.</span></span>
4. <span data-ttu-id="fe902-382">Velg versjon **3.3** på hurtigfanen **Versjoner**.</span><span class="sxs-lookup"><span data-stu-id="fe902-382">On the **Versions** FastTab, select version **3.3**.</span></span>
5. <span data-ttu-id="fe902-383">Velg **Utforming**.</span><span class="sxs-lookup"><span data-stu-id="fe902-383">Select **Designer**.</span></span>
6. <span data-ttu-id="fe902-384">På **Formatutforming**-siden utvider du **BACSReportsFolder**-formatelement.</span><span class="sxs-lookup"><span data-stu-id="fe902-384">On the **Format designer** page, expand the **BACSReportsFolder** format element.</span></span>
7.  <span data-ttu-id="fe902-385">Legg merke til at versjon 3.3 inneholder **PaymentAdviceReport**-formatelementet som brukes til å generere en betalingsmeldingsrapport når en leverandørbetaling behandles.</span><span class="sxs-lookup"><span data-stu-id="fe902-385">Notice that version 3.3 contains the **PaymentAdviceReport** format element that is used to generate a payment advice report when a vendor payment is processed.</span></span>

    ![PaymentAdviceReport-formatelement i ER-operasjonsutforming](./media/er-quick-start2-imported-solution2.png)

8. <span data-ttu-id="fe902-387">Lukk utformingssiden.</span><span class="sxs-lookup"><span data-stu-id="fe902-387">Close the designer page.</span></span>

## <a name="adopt-the-changes-in-the-new-version-of-an-imported-format-in-a-custom-format"></a><a id="AdoptNewBaseVersion"></a><span data-ttu-id="fe902-388">Ta i bruk endringene i den nye versjonen av et importert format i et egendefinert format</span><span class="sxs-lookup"><span data-stu-id="fe902-388">Adopt the changes in the new version of an imported format in a custom format</span></span>

### <a name="complete-the-current-draft-version-of-a-custom-format"></a><a id="CompleteDerivedFormat"></a><span data-ttu-id="fe902-389">Fullfør gjeldende utkastversjon av et egendefinert format</span><span class="sxs-lookup"><span data-stu-id="fe902-389">Complete the current draft version of a custom format</span></span>

<span data-ttu-id="fe902-390">Hvis du vil beholde gjeldende tilstand for det egendefinerte formatet, må du fullføre utkastversjonen 1.1.1 ved å endre statusen fra **Utkast** til **Fullført**.</span><span class="sxs-lookup"><span data-stu-id="fe902-390">If you want to keep the current state of your custom format, complete the draft version 1.1.1 by changing its status from **Draft** to **Completed**.</span></span>

1. <span data-ttu-id="fe902-391">Gå til **Organisasjonsstyring** \> **Arbeidsområder** \> **Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="fe902-391">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="fe902-392">På siden **Lokaliseringskonfigurasjoner**, i delen **Konfigurasjoner**, velger du flisen **Rapporteringskonfigurasjoner**.</span><span class="sxs-lookup"><span data-stu-id="fe902-392">On the **Localization configurations** page, in the **Configurations** section, select the **Reporting configurations** tile.</span></span>
3. <span data-ttu-id="fe902-393">På **Konfigurasjoner**-siden, i konfigurasjonstreet i venstre rute, utvider du **Betalingsmodell** og utvider **BBS (Storbritannia)** og velger **BBS (Storbritannia egendefinert)**.</span><span class="sxs-lookup"><span data-stu-id="fe902-393">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**, expand **BACS (UK)**, and then select **BACS (UK custom)**.</span></span>
4. <span data-ttu-id="fe902-394">I **Versjon**-hurtigfanen velger du **Endre status** \> **Fullført**, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="fe902-394">On the **Versions** FastTab, select **Change status** \> **Complete**, and then select **OK**.</span></span>

<span data-ttu-id="fe902-395">Statusen for versjon 1.1.1 endres fra **Utkast** til **Fullført**, og versjonen blir skrivebeskyttet.</span><span class="sxs-lookup"><span data-stu-id="fe902-395">The status of version 1.1.1 is changed from **Draft** to **Completed**, and the version becomes read-only.</span></span> <span data-ttu-id="fe902-396">En ny redigerbar versjon, 1.1.2, har blitt lagt til og har statusen **Utkast**.</span><span class="sxs-lookup"><span data-stu-id="fe902-396">A new editable version, 1.1.2, has been added and has a status of **Draft**.</span></span> <span data-ttu-id="fe902-397">Du kan bruke denne versjonen til å gjøre ytterligere endringer i det egendefinerte ER-formatet.</span><span class="sxs-lookup"><span data-stu-id="fe902-397">You can use this version to make further changes in your custom ER format.</span></span>

### <a name="rebase-a-custom-format-to-a-new-base-version"></a><a id="RebaseDerivedFormat"></a><span data-ttu-id="fe902-398">Rebasere et egendefinert format på nytt til en ny grunnversjon</span><span class="sxs-lookup"><span data-stu-id="fe902-398">Rebase a custom format to a new base version</span></span>

<span data-ttu-id="fe902-399">Hvis du vil begynne å bruke den nye funksjonaliteten i versjon 3.3 av **BBS (Storbritannia)**-formatet i tilpasningen, må du endre basiskonfigurasjonsversjonen for den egendefinerte konfigurasjonen, **BBS (Storbritannia egendefinert)**.</span><span class="sxs-lookup"><span data-stu-id="fe902-399">To start to use the new functionality of version 3.3 of the **BACS (UK)** format in your customization, you must change the base configuration version for the custom configuration, **BACS (UK custom)**.</span></span> <span data-ttu-id="fe902-400">Denne prosessen kalles [rebasering](general-electronic-reporting.md#upgrading-a-format-selecting-a-new-version-of-base-format-rebase).</span><span class="sxs-lookup"><span data-stu-id="fe902-400">This process is known as [rebasing](general-electronic-reporting.md#upgrading-a-format-selecting-a-new-version-of-base-format-rebase).</span></span> <span data-ttu-id="fe902-401">Bruk den nye versjon 3.3 i stedet for versjon 1.1 av **BBS (Storbritannia)**.</span><span class="sxs-lookup"><span data-stu-id="fe902-401">Instead of version 1.1 of **BACS (UK)**, use version 3.3.</span></span>

1. <span data-ttu-id="fe902-402">Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Konfigurasjoner**.</span><span class="sxs-lookup"><span data-stu-id="fe902-402">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="fe902-403">På **Konfigurasjoner**-siden, i konfigurasjonstreet i venstre rute, utvider du **Betalingsmodell** og velger **BBS (Storbritannia egendefinert)**.</span><span class="sxs-lookup"><span data-stu-id="fe902-403">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**, and then select **BACS (UK custom)**.</span></span>
3. <span data-ttu-id="fe902-404">På **Versjoner**-hurtigfanen velger du versjon **1.1.2** og deretter **Rebaser**.</span><span class="sxs-lookup"><span data-stu-id="fe902-404">On the **Versions** FastTab, select version **1.1.2**, and then select **Rebase**.</span></span>
4. <span data-ttu-id="fe902-405">I **Rebaser**-dialogboksen i **Målversjon**-feltet velger du versjon **3.3** av den grunnkonfigurasjonen for å bruke den som det nye grunnlaget, og bruker den til å oppdatere konfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="fe902-405">In the **Rebase** dialog box, in the **Target version** field, select version **3.3** of the base configuration to apply it as the new base and use it to update the configuration.</span></span>

    ![Dialogboksen Rebaser](./media/er-quick-start2-rebase1.png)

5. <span data-ttu-id="fe902-407">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="fe902-407">Select **OK**.</span></span>
6. <span data-ttu-id="fe902-408">Legg merke til at nummeret til utkastversjonen er endret fra **1.1.2** til **3.3.2** for å gjenspeile endringen i grunnversjonen.</span><span class="sxs-lookup"><span data-stu-id="fe902-408">Notice that the number of the draft version has been changed from **1.1.2** to **3.3.2** to reflect the change in the base version.</span></span>

    <span data-ttu-id="fe902-409">Når den egendefinerte versjonen og en ny grunnleggende versjon slås sammen, kan enkelte konflikter oppdages på grunn av formatendringer som ikke kan slås sammen automatisk.</span><span class="sxs-lookup"><span data-stu-id="fe902-409">When the custom version and a new base version are merged, some conflicts might be discovered because of format changes that can't be merged automatically.</span></span>

    ![Rebasert konfigurasjon med konflikter på Konfigurasjoner-siden](./media/er-quick-start2-rebase2.png)

    <span data-ttu-id="fe902-411">Hvis det oppdages konflikter, må de løses manuelt i formatutformingen.</span><span class="sxs-lookup"><span data-stu-id="fe902-411">If conflicts are discovered, they must be manually resolved in the format designer.</span></span>

7. <span data-ttu-id="fe902-412">Velg versjon **3.3.2** på hurtigfanen **Versjoner**.</span><span class="sxs-lookup"><span data-stu-id="fe902-412">On the **Versions** FastTab, select version **3.3.2**.</span></span>
8. <span data-ttu-id="fe902-413">Velg **Utforming**.</span><span class="sxs-lookup"><span data-stu-id="fe902-413">Select **Designer**.</span></span>
9. <span data-ttu-id="fe902-414">På **Formatutforming**-siden, på **Detaljer**-hurtigfanen, velger du en rebaseringskonfliktpost og velger **Bruk basisverdi**.</span><span class="sxs-lookup"><span data-stu-id="fe902-414">On the **Format designer** page, on the **Details** FastTab, select a rebase conflict record, and then select **Apply base value**.</span></span>

    ![Rebaseringskonfliktposten i ER-operasjonsutforming](./media/er-quick-start2-rebase3.png)

10. <span data-ttu-id="fe902-416">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="fe902-416">Select **Save**.</span></span>

    <span data-ttu-id="fe902-417">Rebaseringskonfliktposten skal ikke lenger vises i **Detaljer**-hurtigfanen.</span><span class="sxs-lookup"><span data-stu-id="fe902-417">The rebase conflict record should no longer appear on the **Details** FastTab.</span></span>

    ![Konflikt løst i ER-operasjonsutforming](./media/er-quick-start2-rebase4.png)

    > [!NOTE]
    > <span data-ttu-id="fe902-419">Du løste konflikten ved å bekrefte at versjon 3 av basismodellen må brukes i dette ER-formatet.</span><span class="sxs-lookup"><span data-stu-id="fe902-419">You resolved the conflict by confirming that version 3 of the base model must be used in this ER format.</span></span>

11. <span data-ttu-id="fe902-420">Utvid **BACSReportsFolder** \> **fil** \> **transaksjoner** \> **transaksjon**.</span><span class="sxs-lookup"><span data-stu-id="fe902-420">Expand **BACSReportsFolder** \> **file** \> **transactions** \> **transaction**.</span></span>
12. <span data-ttu-id="fe902-421">Legg merke til at versjon 3.3.2 av det egendefinerte formatet i **Tilordning**-fanen inneholder både tilpasningen (**vendBankSWIFT**-formatelementet og bindingen) og den nye funksjonaliteten til versjon 3.3 av basis-ER-formatet som ble levert av Microsoft (**PaymentAdviceReport**-formatelementet sammen med nestede og konfigurerte bindinger).</span><span class="sxs-lookup"><span data-stu-id="fe902-421">On the **Mapping** tab, notice that version 3.3.2 of your custom ER format contains both your customization (the **vendBankSWIFT** format element and its binding) and the new functionality of version 3.3 of the base ER format that was provided by Microsoft (the **PaymentAdviceReport** format element together with its nested elements and configured bindings).</span></span> <span data-ttu-id="fe902-422">Med bare noen få museklikk har du tatt i bruk endringene i en ny basisversjon ved å slå dem sammen med tilpasning.</span><span class="sxs-lookup"><span data-stu-id="fe902-422">In just a few mouse clicks, you adopted the modifications of a new base version by merging them with your customization.</span></span>

    ![Sammenslått format i ER-operasjonsutforming](./media/er-quick-start2-rebase5.png)

13. <span data-ttu-id="fe902-424">Lukk utformingssiden.</span><span class="sxs-lookup"><span data-stu-id="fe902-424">Close the designer page.</span></span>

> [!NOTE]
> <span data-ttu-id="fe902-425">Rebaseringshandlingen er reversibel.</span><span class="sxs-lookup"><span data-stu-id="fe902-425">The rebase action is reversible.</span></span> <span data-ttu-id="fe902-426">Hvis du vil avbryte denne rebaseringen, velger du **1.1.1** av **BBS (Storbritannia egendefinert)**-formatet i **Versjoner**-hurtigfanen, og deretter velger du **Hent denne versjonen**.</span><span class="sxs-lookup"><span data-stu-id="fe902-426">To cancel this rebase, select version **1.1.1** of the **BACS (UK custom)** format on the **Versions** FastTab, and then select **Get this version**.</span></span> <span data-ttu-id="fe902-427">Versjon 3.3.2 blir deretter omnummerert 1.1.2, og innholdet i utkastversjon 1.1.2 vil samsvare med innholdet i versjon 1.1.1.</span><span class="sxs-lookup"><span data-stu-id="fe902-427">Version 3.3.2 will then be renumbered 1.1.2, and the content of draft version 1.1.2 will match the content of version 1.1.1.</span></span>

### <a name="process-a-vendor-payment-by-using-a-rebased-er-format"></a><a id="ProcessPayment3"></a><span data-ttu-id="fe902-428">Behandle en leverandørbetaling ved hjelp av et rebasert ER-format</span><span class="sxs-lookup"><span data-stu-id="fe902-428">Process a vendor payment by using a rebased ER format</span></span>

1. <span data-ttu-id="fe902-429">Gå til **Leverandører** \> **Betalinger** \> **Leverandørbetalingsjournal**.</span><span class="sxs-lookup"><span data-stu-id="fe902-429">Go to **Accounts payable** \> **Payments** \> **Vendor payment journal**.</span></span>
2. <span data-ttu-id="fe902-430">På siden **Leverandørbetalingsjournal** velger du betalingsjournalen du opprettet tidligere.</span><span class="sxs-lookup"><span data-stu-id="fe902-430">On the **Vendor payment journal** page, select the payment journal that you created earlier.</span></span>
3. <span data-ttu-id="fe902-431">Velg **Linjer**.</span><span class="sxs-lookup"><span data-stu-id="fe902-431">Select **Lines**.</span></span>
4. <span data-ttu-id="fe902-432">På **Leverandørbetalinger**-siden velger du **Betalingsstatus** \> **Ingen** over rutenettet.</span><span class="sxs-lookup"><span data-stu-id="fe902-432">On the **Vendor payments** page, above the grid, select **Payment status** \> **None**.</span></span>
5. <span data-ttu-id="fe902-433">Velg **Generer betaling**.</span><span class="sxs-lookup"><span data-stu-id="fe902-433">Select **Generate payment**.</span></span>
6. <span data-ttu-id="fe902-434">Angi følgende informasjon i dialogboksen **Generer betalinger**:</span><span class="sxs-lookup"><span data-stu-id="fe902-434">In the **Generate payments** dialog box, enter the following information:</span></span>

    - <span data-ttu-id="fe902-435">Velg **Elektronisk** i feltet **Betalingsmåte**.</span><span class="sxs-lookup"><span data-stu-id="fe902-435">In the **Method of payment** field, select **Electronic**.</span></span>
    - <span data-ttu-id="fe902-436">Velg **GBSI OPER** i feltet **Bankkonto**.</span><span class="sxs-lookup"><span data-stu-id="fe902-436">In the **Bank account** field, select **GBSI OPER**.</span></span>

7. <span data-ttu-id="fe902-437">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="fe902-437">Select **OK**.</span></span>
8. <span data-ttu-id="fe902-438">Angi følgende informasjon i dialogboksen **Parametere for elektronisk rapportering**:</span><span class="sxs-lookup"><span data-stu-id="fe902-438">In the **Electronic report parameters** dialog box, enter the following information:</span></span>

    - <span data-ttu-id="fe902-439">Sett alternativet **Skriv ut kontrollrapport** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="fe902-439">Set the **Print control report** option to **Yes**.</span></span>
    - <span data-ttu-id="fe902-440">Sett alternativet **Skriv ut betalingsmelding** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="fe902-440">Set the **Print payment advice** option to **Yes**.</span></span>

    ![Dialogboksen Parametere for elektronisk rapport](./media/er-quick-start2-payment-dialog2.png)

    > [!NOTE]
    > <span data-ttu-id="fe902-442">I tillegg til betalingsfilen kan du nå generere både kontrollrapporten og betalingsmeldingsrapporten.</span><span class="sxs-lookup"><span data-stu-id="fe902-442">In addition to the payment file, you can now generate both the control report and the payment advice report.</span></span>

9. <span data-ttu-id="fe902-443">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="fe902-443">Select **OK**.</span></span>
10. <span data-ttu-id="fe902-444">Last ned zip-filen, og pakk deretter ut følgende filer:</span><span class="sxs-lookup"><span data-stu-id="fe902-444">Download the zip file, and then extract the following files from it:</span></span>

    - <span data-ttu-id="fe902-445">Kontrollrapporten i Excel-format</span><span class="sxs-lookup"><span data-stu-id="fe902-445">The control report in Excel format</span></span>
    - <span data-ttu-id="fe902-446">Betalingsmeldingsrapporten i Excel-format</span><span class="sxs-lookup"><span data-stu-id="fe902-446">The payment advice report in Excel format</span></span>

        ![Betalingsmeldingsrapport i Excel-format](./media/er-quick-start2-payment-advice-report.png)

    - <span data-ttu-id="fe902-448">Betalingsfilen i TXT-format</span><span class="sxs-lookup"><span data-stu-id="fe902-448">The payment file in TXT format</span></span>

        <span data-ttu-id="fe902-449">Legg merke til at betalingslinjen i den genererte filen nå starter med SWIFT-koden som ble angitt for bankkontoen til en leverandør som har utført betalingen.</span><span class="sxs-lookup"><span data-stu-id="fe902-449">Notice that the payment line in the generated file starts  with the SWIFT code that was entered for the bank account of a vendor whose payment has been processed.</span></span>

        ![Betalingsfil i TXT-format](./media/er-quick-start2-payment-file3.png)

## <a name="additional-resources"></a><a id="References"></a><span data-ttu-id="fe902-451">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="fe902-451">Additional resources</span></span>

- [<span data-ttu-id="fe902-452">Oversikt over elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="fe902-452">Electronic Reporting overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="fe902-453">Laste ned ER-konfigurasjoner fra Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="fe902-453">Download ER configurations from Lifecycle Services</span></span>](download-electronic-reporting-configuration-lcs.md)
- [<span data-ttu-id="fe902-454">Last ned ER-konfigurasjoner fra det globale repositoriet for konfigurasjonstjenesten</span><span class="sxs-lookup"><span data-stu-id="fe902-454">Download ER configurations from Global repository of Configuration service</span></span>](er-download-configurations-global-repo.md)