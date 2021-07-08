---
title: Laste opp en konfigurasjon til Lifecycle Services
description: Dette emnet forklarer hvordan du oppretter en ny konfigurasjon for elektronisk rapportering (ER) og laster den opp til Microsoft Dynamics Lifecycle Services (LCS).
author: NickSelin
ms.date: 06/17/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 41a8fcf2592bde4901aba703e0cd124b1155dac6
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/17/2021
ms.locfileid: "6270565"
---
# <a name="upload-a-configuration-into-lifecycle-services"></a><span data-ttu-id="97162-103">Laste opp en konfigurasjon til Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="97162-103">Upload a configuration into Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="97162-104">Dette emnet forklarer hvordan en bruker i rollen Systemansvarlig eller Utvikler av elektronisk rapportering kan opprette en ny [konfigurasjon for elektronisk rapportering (ER)](../general-electronic-reporting.md#Configuration) og laste den opp til [aktivabiblioteket på prosjektnivå](../../lifecycle-services/asset-library.md) i Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="97162-104">This topic explains how a user in the System administrator or Electronic reporting developer role can create a new [Electronic reporting (ER) configuration](../general-electronic-reporting.md#Configuration) and upload it into the [project-level Asset library](../../lifecycle-services/asset-library.md) in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="97162-105">Bruken av Lifecycle Services (LCS) som et lagringsrepositorium for konfigurasjoner for elektronisk rapportering (ER) blir [avskrevet](../../../../finance/get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release).</span><span class="sxs-lookup"><span data-stu-id="97162-105">The use of LCS as a storage repository for ER configurations is being [deprecated](../../../../finance/get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release).</span></span> <span data-ttu-id="97162-106">Hvis du vil ha mer informasjon, se [Regulatory Configuration Service (RCS) – avskrivning av lager for Lifecycle Services (LCS)](../../../../finance/localizations/rcs-lcs-repo-dep-faq.md).</span><span class="sxs-lookup"><span data-stu-id="97162-106">For more information, see [Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) storage deprecation](../../../../finance/localizations/rcs-lcs-repo-dep-faq.md).</span></span>

<span data-ttu-id="97162-107">I dette eksemplet skal du opprette en konfigurasjon og laste den opp til LCS for et eksempelfirma med navnet Litware, Inc. Denne fremgangsmåten kan fullføres i alle firmaer ettersom ER-konfigurasjoner deles mellom alle firmaer.</span><span class="sxs-lookup"><span data-stu-id="97162-107">In this example, you will create a configuration and upload it into LCS for a sample company that is named Litware, Inc. These steps can be completed in any company, because ER configurations are shared among companies.</span></span> <span data-ttu-id="97162-108">For å fullføre disse trinnene må du først fullføre trinnene i [Opprette konfigurasjonsleverandører og merke dem som aktive](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="97162-108">To complete these steps, you must first complete the steps in [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> <span data-ttu-id="97162-109">Tilgang til LCS er også nødvendig.</span><span class="sxs-lookup"><span data-stu-id="97162-109">Access to LCS is also required.</span></span>

1. <span data-ttu-id="97162-110">Logg på programmet med én av følgende roller:</span><span class="sxs-lookup"><span data-stu-id="97162-110">Sign in to the application by using one of the following roles:</span></span>

    - <span data-ttu-id="97162-111">Utvikler av elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="97162-111">Electronic reporting developer</span></span>
    - <span data-ttu-id="97162-112">Systemansvarlig</span><span class="sxs-lookup"><span data-stu-id="97162-112">System administrator</span></span>

2. <span data-ttu-id="97162-113">Gå til **Organisasjonsstyring** \> **Arbeidsområder** \> **Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="97162-113">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="97162-114">Velg **Litware, Inc.** og merk som **Aktiv**.</span><span class="sxs-lookup"><span data-stu-id="97162-114">Select **Litware, Inc.**, and mark it as **Active**.</span></span>
4. <span data-ttu-id="97162-115">Velg **Konfigurasjoner**.</span><span class="sxs-lookup"><span data-stu-id="97162-115">Select **Configurations**.</span></span>

<a name="accessconditions"></a>
> [!NOTE]
> <span data-ttu-id="97162-116">Kontroller at den gjeldende Dynamics 365 Finance-brukeren er medlem av LCS-prosjektet som inneholder [aktivabiblioteket](../../lifecycle-services/asset-library.md#asset-library-support) som brukes til å importere ER-konfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="97162-116">Make sure that the current Dynamics 365 Finance user is a member of the LCS project that contains the [Asset library](../../lifecycle-services/asset-library.md#asset-library-support) that is used to import ER configurations.</span></span>
>
> <span data-ttu-id="97162-117">Du kan ikke få tilgang til et LCS-prosjekt fra et ER-repositorium som representerer et annet domene enn domenet som brukes i Finance.</span><span class="sxs-lookup"><span data-stu-id="97162-117">You can't access an LCS project from an ER repository that represents a different domain than the domain that is used in Finance.</span></span> <span data-ttu-id="97162-118">Hvis du prøver, vises det en tom liste over LCS-prosjekter, og du kan ikke importere ER-konfigurasjonene fra aktivabiblioteket på prosjektnivå i LCS.</span><span class="sxs-lookup"><span data-stu-id="97162-118">If you try, an empty list of LCS projects will be shown, and you won't be able to import ER configurations from the project-level Asset library in LCS.</span></span> <span data-ttu-id="97162-119">Hvis du vil ha tilgang til aktivabiblioteker på prosjektnivå fra et ER-repositorium som brukes til å importere ER-konfigurasjoner, logger du på Finance-modulen ved hjelp av legitimasjonen til en bruker som tilhører leieren (domenet) som gjeldende Finance-forekomst er klargjort for.</span><span class="sxs-lookup"><span data-stu-id="97162-119">To access project-level Asset libraries from an ER repository that is used to import ER configurations, sign in to Finance by using the credentials of a user who belongs to the tenant (domain) that the current Finance instance has been provisioned for.</span></span>

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="97162-120">Opprett en ny datamodellkonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="97162-120">Create a new data model configuration</span></span>

1. <span data-ttu-id="97162-121">Gå til **Organisasjonsstyring \> Elektronisk rapportering \> Konfigurasjoner**.</span><span class="sxs-lookup"><span data-stu-id="97162-121">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="97162-122">På siden **Konfigurasjoner** velger du **Opprett konfigurasjon** for å åpne dialogboksen med rullegardinliste.</span><span class="sxs-lookup"><span data-stu-id="97162-122">On the **Configurations** page, select **Create configuration** to open the drop-down dialog box.</span></span>

    <span data-ttu-id="97162-123">I dette eksemplet skal du opprette en konfigurasjon som inneholder en eksempeldatamodell for elektroniske dokumenter.</span><span class="sxs-lookup"><span data-stu-id="97162-123">In this example, you will create a configuration that contains a sample data model for electronic documents.</span></span> <span data-ttu-id="97162-124">Denne datamodellkonfigurasjonen lastes inn i LCS senere.</span><span class="sxs-lookup"><span data-stu-id="97162-124">This data model configuration will be uploaded into LCS later.</span></span>

3. <span data-ttu-id="97162-125">I feltet **Navn** angir du **Eksempelmodellkonfigurasjon**.</span><span class="sxs-lookup"><span data-stu-id="97162-125">In the **Name** field, enter **Sample model configuration**.</span></span>
4. <span data-ttu-id="97162-126">I feltet **Beskrivelse** angir du **Eksempelmodellkonfigurasjon**.</span><span class="sxs-lookup"><span data-stu-id="97162-126">In the **Description** field, enter **Sample model configuration**.</span></span>
5. <span data-ttu-id="97162-127">Velg **Opprett konfigurasjon**.</span><span class="sxs-lookup"><span data-stu-id="97162-127">Select **Create configuration**.</span></span>
6. <span data-ttu-id="97162-128">Velg **Modellutforming**.</span><span class="sxs-lookup"><span data-stu-id="97162-128">Select **Model designer**.</span></span>
7. <span data-ttu-id="97162-129">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="97162-129">Select **New**.</span></span>
8. <span data-ttu-id="97162-130">I **Navn**-feltet angir du **Inngangspunkt**.</span><span class="sxs-lookup"><span data-stu-id="97162-130">In the **Name** field, enter **Entry point**.</span></span>
9. <span data-ttu-id="97162-131">Velg **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="97162-131">Select **Add**.</span></span>
10. <span data-ttu-id="97162-132">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="97162-132">Select **Save**.</span></span>
11. <span data-ttu-id="97162-133">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="97162-133">Close the page.</span></span>
12. <span data-ttu-id="97162-134">Velg **Endre status**.</span><span class="sxs-lookup"><span data-stu-id="97162-134">Select **Change status**.</span></span>
13. <span data-ttu-id="97162-135">Velg **Fullfør**.</span><span class="sxs-lookup"><span data-stu-id="97162-135">Select **Complete**.</span></span>
14. <span data-ttu-id="97162-136">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="97162-136">Select **OK**.</span></span>
15. <span data-ttu-id="97162-137">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="97162-137">Close the page.</span></span>

## <a name="register-a-new-repository"></a><span data-ttu-id="97162-138">Registrere et nytt repositorium</span><span class="sxs-lookup"><span data-stu-id="97162-138">Register a new repository</span></span>

1. <span data-ttu-id="97162-139">Gå til **Organisasjonsstyring \> Arbeidsområder \> Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="97162-139">Go to **Organization administration \> Workspaces \> Electronic reporting**.</span></span>

2. <span data-ttu-id="97162-140">I delen **Konfigurasjonsleverandører** velger du **Litware, Inc.**-flisen.</span><span class="sxs-lookup"><span data-stu-id="97162-140">In the **Configuration providers** section, select the **Litware, Inc.** tile.</span></span>

3. <span data-ttu-id="97162-141">På **Litware, Inc.**-flisen velger du **Repositorier**.</span><span class="sxs-lookup"><span data-stu-id="97162-141">On the **Litware, Inc.** tile, select **Repositories**.</span></span>

    <span data-ttu-id="97162-142">Nå kan du åpne listen over repositorier for konfigurasjonsleverandøren Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="97162-142">You can now open the list of repositories for the Litware, Inc. configuration provider.</span></span>

4. <span data-ttu-id="97162-143">Velg **Legg til** for å åpne dialogboksen med rullegardinliste.</span><span class="sxs-lookup"><span data-stu-id="97162-143">Select **Add** to open the drop-down dialog box.</span></span>

    <span data-ttu-id="97162-144">Du kan nå legge til et nytt repositorium.</span><span class="sxs-lookup"><span data-stu-id="97162-144">You can now add a new repository.</span></span>

5. <span data-ttu-id="97162-145">I feltet **Konfigurasjonsrepositorium** velger du **LCS**.</span><span class="sxs-lookup"><span data-stu-id="97162-145">In the **Configuration repository enter** field, select **LCS**.</span></span>
6. <span data-ttu-id="97162-146">Velg **Opprett repositorium**.</span><span class="sxs-lookup"><span data-stu-id="97162-146">Select **Create repository**.</span></span>
7. <span data-ttu-id="97162-147">Angi eller velg en verdi i feltet **Prosjekt**.</span><span class="sxs-lookup"><span data-stu-id="97162-147">In the **Project** field, enter or select a value.</span></span>

    <span data-ttu-id="97162-148">I dette eksemplet velger du det ønskede LCS-prosjektet.</span><span class="sxs-lookup"><span data-stu-id="97162-148">For this example, select the desired LCS project.</span></span> <span data-ttu-id="97162-149">Du må ha [tilgang](#accessconditions) til prosjektet.</span><span class="sxs-lookup"><span data-stu-id="97162-149">You must have [access](#accessconditions) to the project.</span></span>

8. <span data-ttu-id="97162-150">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="97162-150">Select **OK**.</span></span>

    <span data-ttu-id="97162-151">Fullfør en ny oppføring i repositoriet.</span><span class="sxs-lookup"><span data-stu-id="97162-151">Complete a new repository entry.</span></span>

9. <span data-ttu-id="97162-152">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="97162-152">In the list, mark the selected row.</span></span>

    <span data-ttu-id="97162-153">I dette eksemplet velger du repositoriumposten i **LCS**.</span><span class="sxs-lookup"><span data-stu-id="97162-153">For this example, select the **LCS** repository record.</span></span>

    <span data-ttu-id="97162-154">Vær oppmerksom på at et registrert repositorium er merket med gjeldende leverandør.</span><span class="sxs-lookup"><span data-stu-id="97162-154">Note that a registered repository is marked by the current provider.</span></span> <span data-ttu-id="97162-155">Det er med andre ord bare konfigurasjoner som eies av denne leverandøren, som kan plasseres i repositoriet og som derfor lastes opp til det valgte LCS-prosjektet.</span><span class="sxs-lookup"><span data-stu-id="97162-155">In other words, only configurations that are owned by that provider can be put in this repository and therefore uploaded into the selected LCS project.</span></span>

10. <span data-ttu-id="97162-156">Velg **Åpne**.</span><span class="sxs-lookup"><span data-stu-id="97162-156">Select **Open**.</span></span>

    <span data-ttu-id="97162-157">Du åpner repositoriet for å vise listen over ER-konfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="97162-157">You open the repository to view the list of ER configurations.</span></span> <span data-ttu-id="97162-158">Hvis det valgte prosjektet ennå ikke er brukt for deling av ER-konfigurasjoner, vil listen være tom.</span><span class="sxs-lookup"><span data-stu-id="97162-158">If the selected project hasn't yet been used for ER configurations sharing, the list will be empty.</span></span>

11. <span data-ttu-id="97162-159">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="97162-159">Close the page.</span></span>
12. <span data-ttu-id="97162-160">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="97162-160">Close the page.</span></span>

## <a name="upload-a-configuration-into-lcs"></a><span data-ttu-id="97162-161">Laste opp en konfigurasjon til LCS</span><span class="sxs-lookup"><span data-stu-id="97162-161">Upload a configuration into LCS</span></span>

1. <span data-ttu-id="97162-162">Gå til **Organisasjonsstyring \> Elektronisk rapportering \> Konfigurasjoner**.</span><span class="sxs-lookup"><span data-stu-id="97162-162">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="97162-163">På siden **Konfigurasjoner** i konfigurasjonstreet velger du **Eksempelmodellkonfigurasjon**.</span><span class="sxs-lookup"><span data-stu-id="97162-163">On the **Configurations** page, in the configurations tree, select **Sample model configuration**.</span></span>

    <span data-ttu-id="97162-164">Du må velge en opprettet konfigurasjon som allerede er fullført.</span><span class="sxs-lookup"><span data-stu-id="97162-164">You must select a created configuration that has been already completed.</span></span>

3. <span data-ttu-id="97162-165">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="97162-165">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="97162-166">For dette eksemplet velger du versjonen av den valgte konfigurasjonen som har statusen **Fullført**.</span><span class="sxs-lookup"><span data-stu-id="97162-166">For this example, select the version of the selected configuration that has a status of **Completed**.</span></span>

4. <span data-ttu-id="97162-167">Velg **Endre status**.</span><span class="sxs-lookup"><span data-stu-id="97162-167">Select **Change status**.</span></span>
5. <span data-ttu-id="97162-168">Velg **Del**.</span><span class="sxs-lookup"><span data-stu-id="97162-168">Select **Share**.</span></span>

    <span data-ttu-id="97162-169">Statusen for konfigurasjonen endres fra **Fullført** til **Delt** når konfigurasjonen er publisert i LCS.</span><span class="sxs-lookup"><span data-stu-id="97162-169">The status of the configuration is changed from **Completed** to **Shared** when the configuration is published in LCS.</span></span>

6. <span data-ttu-id="97162-170">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="97162-170">Select **OK**.</span></span>
7. <span data-ttu-id="97162-171">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="97162-171">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="97162-172">For dette eksemplet velger du konfigurasjonsversjonen som har statusen **Delt**.</span><span class="sxs-lookup"><span data-stu-id="97162-172">For this example, select the configuration version that has a status of **Shared**.</span></span>

    <span data-ttu-id="97162-173">Vær oppmerksom på at statusen for den valgte versjonen ble endret fra **Fullført** til **Delt**.</span><span class="sxs-lookup"><span data-stu-id="97162-173">Note that the status of the selected version was changed from **Completed** to **Shared**.</span></span>

8. <span data-ttu-id="97162-174">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="97162-174">Close the page.</span></span>
9. <span data-ttu-id="97162-175">Velg **Repositorier**.</span><span class="sxs-lookup"><span data-stu-id="97162-175">Select **Repositories**.</span></span>

    <span data-ttu-id="97162-176">Nå kan du åpne listen over repositorier for konfigurasjonsleverandøren Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="97162-176">You can now open the list of repositories for the Litware, Inc. configuration provider.</span></span>

10. <span data-ttu-id="97162-177">Velg **Åpne**.</span><span class="sxs-lookup"><span data-stu-id="97162-177">Select **Open**.</span></span>

    <span data-ttu-id="97162-178">I dette eksemplet velger du repositoriet **LCS** og åpner det.</span><span class="sxs-lookup"><span data-stu-id="97162-178">For this example, select the **LCS** repository, and open it.</span></span>

    <span data-ttu-id="97162-179">Vær oppmerksom på at den valgte konfigurasjonen vises som et anleggsmiddel for det valgte LCS-prosjektet.</span><span class="sxs-lookup"><span data-stu-id="97162-179">Notice that the selected configuration is shown as an asset of the selected LCS project.</span></span>

11. <span data-ttu-id="97162-180">Åpne LCS ved å gå til <https://lcs.dynamics.com>.</span><span class="sxs-lookup"><span data-stu-id="97162-180">Open LCS by going to <https://lcs.dynamics.com>.</span></span>
12. <span data-ttu-id="97162-181">Åpne et prosjekt som ble brukt tidligere til registrering av repositorium.</span><span class="sxs-lookup"><span data-stu-id="97162-181">Open a project that was used earlier for repository registration.</span></span>
13. <span data-ttu-id="97162-182">Åpne aktivabiblioteket for prosjektet.</span><span class="sxs-lookup"><span data-stu-id="97162-182">Open the Asset library of the project.</span></span>
14. <span data-ttu-id="97162-183">Velg aktivatypen **GER-konfigurasjon**.</span><span class="sxs-lookup"><span data-stu-id="97162-183">Select the **GER configuration** asset type.</span></span>

    <span data-ttu-id="97162-184">ER-konfigurasjonen du lastet opp, bør nå vises.</span><span class="sxs-lookup"><span data-stu-id="97162-184">The ER configuration that you uploaded should be listed.</span></span>

    <span data-ttu-id="97162-185">Vær oppmerksom på at den opplastede LCS-konfigurasjonen kan importeres til en annen forekomst hvis leverandører har tilgang til dette LCS-prosjektet.</span><span class="sxs-lookup"><span data-stu-id="97162-185">Note that the uploaded LCS configuration can be imported into another instance if providers have access to this LCS project.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
