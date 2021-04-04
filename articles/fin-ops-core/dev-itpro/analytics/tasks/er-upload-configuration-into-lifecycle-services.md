---
title: Laste opp en konfigurasjon til Lifecycle Services
description: Dette emnet forklarer hvordan du oppretter en ny konfigurasjon for elektronisk rapportering (ER) og laster den opp til Microsoft Dynamics Lifecycle Services (LCS).
author: NickSelin
manager: AnnBe
ms.date: 09/14/2020
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
ms.openlocfilehash: 6f17763236594092d04dfe2d2f9912e764b4f8d4
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562643"
---
# <a name="upload-a-configuration-into-lifecycle-services"></a><span data-ttu-id="f2853-103">Laste opp en konfigurasjon til Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="f2853-103">Upload a configuration into Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f2853-104">Dette emnet forklarer hvordan en bruker i rollen Systemansvarlig eller Utvikler av elektronisk rapportering kan opprette en ny [konfigurasjon for elektronisk rapportering (ER)](../general-electronic-reporting.md#Configuration) og laste den opp til [aktivabiblioteket på prosjektnivå](../../lifecycle-services/asset-library.md) i Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="f2853-104">This topic explains how a user in the System administrator or Electronic reporting developer role can create a new [Electronic reporting (ER) configuration](../general-electronic-reporting.md#Configuration) and upload it into the [project-level Asset library](../../lifecycle-services/asset-library.md) in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

<span data-ttu-id="f2853-105">I dette eksemplet skal du opprette en konfigurasjon og laste den opp til LCS for et eksempelfirma med navnet Litware, Inc. Denne fremgangsmåten kan fullføres i alle firmaer ettersom ER-konfigurasjoner deles mellom alle firmaer.</span><span class="sxs-lookup"><span data-stu-id="f2853-105">In this example, you will create a configuration and upload it into LCS for a sample company that is named Litware, Inc. These steps can be completed in any company, because ER configurations are shared among companies.</span></span> <span data-ttu-id="f2853-106">For å fullføre disse trinnene må du først fullføre trinnene i [Opprette konfigurasjonsleverandører og merke dem som aktive](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="f2853-106">To complete these steps, you must first complete the steps in [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> <span data-ttu-id="f2853-107">Tilgang til LCS er også nødvendig.</span><span class="sxs-lookup"><span data-stu-id="f2853-107">Access to LCS is also required.</span></span>

1. <span data-ttu-id="f2853-108">Logg på programmet med én av følgende roller:</span><span class="sxs-lookup"><span data-stu-id="f2853-108">Sign in to the application by using one of the following roles:</span></span>

    - <span data-ttu-id="f2853-109">Utvikler av elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="f2853-109">Electronic reporting developer</span></span>
    - <span data-ttu-id="f2853-110">Systemansvarlig</span><span class="sxs-lookup"><span data-stu-id="f2853-110">System administrator</span></span>

2. <span data-ttu-id="f2853-111">Gå til **Organisasjonsstyring** \> **Arbeidsområder** \> **Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="f2853-111">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="f2853-112">Velg **Litware, Inc.** og merk som **Aktiv**.</span><span class="sxs-lookup"><span data-stu-id="f2853-112">Select **Litware, Inc.**, and mark it as **Active**.</span></span>
4. <span data-ttu-id="f2853-113">Velg **Konfigurasjoner**.</span><span class="sxs-lookup"><span data-stu-id="f2853-113">Select **Configurations**.</span></span>

<a name="accessconditions"></a>
> [!NOTE]
> <span data-ttu-id="f2853-114">Kontroller at den gjeldende Dynamics 365 Finance-brukeren er medlem av LCS-prosjektet som inneholder [aktivabiblioteket](../../lifecycle-services/asset-library.md#asset-library-support) som brukes til å importere ER-konfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="f2853-114">Make sure that the current Dynamics 365 Finance user is a member of the LCS project that contains the [Asset library](../../lifecycle-services/asset-library.md#asset-library-support) that is used to import ER configurations.</span></span>
>
> <span data-ttu-id="f2853-115">Du kan ikke få tilgang til et LCS-prosjekt fra et ER-repositorium som representerer et annet domene enn domenet som brukes i Finance.</span><span class="sxs-lookup"><span data-stu-id="f2853-115">You can't access an LCS project from an ER repository that represents a different domain than the domain that is used in Finance.</span></span> <span data-ttu-id="f2853-116">Hvis du prøver, vises det en tom liste over LCS-prosjekter, og du kan ikke importere ER-konfigurasjonene fra aktivabiblioteket på prosjektnivå i LCS.</span><span class="sxs-lookup"><span data-stu-id="f2853-116">If you try, an empty list of LCS projects will be shown, and you won't be able to import ER configurations from the project-level Asset library in LCS.</span></span> <span data-ttu-id="f2853-117">Hvis du vil ha tilgang til aktivabiblioteker på prosjektnivå fra et ER-repositorium som brukes til å importere ER-konfigurasjoner, logger du på Finance-modulen ved hjelp av legitimasjonen til en bruker som tilhører leieren (domenet) som gjeldende Finance-forekomst er klargjort for.</span><span class="sxs-lookup"><span data-stu-id="f2853-117">To access project-level Asset libraries from an ER repository that is used to import ER configurations, sign in to Finance by using the credentials of a user who belongs to the tenant (domain) that the current Finance instance has been provisioned for.</span></span>

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="f2853-118">Opprett en ny datamodellkonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="f2853-118">Create a new data model configuration</span></span>

1. <span data-ttu-id="f2853-119">Gå til **Organisasjonsstyring \> Elektronisk rapportering \> Konfigurasjoner**.</span><span class="sxs-lookup"><span data-stu-id="f2853-119">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="f2853-120">På siden **Konfigurasjoner** velger du **Opprett konfigurasjon** for å åpne dialogboksen med rullegardinliste.</span><span class="sxs-lookup"><span data-stu-id="f2853-120">On the **Configurations** page, select **Create configuration** to open the drop-down dialog box.</span></span>

    <span data-ttu-id="f2853-121">I dette eksemplet skal du opprette en konfigurasjon som inneholder en eksempeldatamodell for elektroniske dokumenter.</span><span class="sxs-lookup"><span data-stu-id="f2853-121">In this example, you will create a configuration that contains a sample data model for electronic documents.</span></span> <span data-ttu-id="f2853-122">Denne datamodellkonfigurasjonen lastes inn i LCS senere.</span><span class="sxs-lookup"><span data-stu-id="f2853-122">This data model configuration will be uploaded into LCS later.</span></span>

3. <span data-ttu-id="f2853-123">I feltet **Navn** angir du **Eksempelmodellkonfigurasjon**.</span><span class="sxs-lookup"><span data-stu-id="f2853-123">In the **Name** field, enter **Sample model configuration**.</span></span>
4. <span data-ttu-id="f2853-124">I feltet **Beskrivelse** angir du **Eksempelmodellkonfigurasjon**.</span><span class="sxs-lookup"><span data-stu-id="f2853-124">In the **Description** field, enter **Sample model configuration**.</span></span>
5. <span data-ttu-id="f2853-125">Velg **Opprett konfigurasjon**.</span><span class="sxs-lookup"><span data-stu-id="f2853-125">Select **Create configuration**.</span></span>
6. <span data-ttu-id="f2853-126">Velg **Modellutforming**.</span><span class="sxs-lookup"><span data-stu-id="f2853-126">Select **Model designer**.</span></span>
7. <span data-ttu-id="f2853-127">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="f2853-127">Select **New**.</span></span>
8. <span data-ttu-id="f2853-128">I **Navn**-feltet angir du **Inngangspunkt**.</span><span class="sxs-lookup"><span data-stu-id="f2853-128">In the **Name** field, enter **Entry point**.</span></span>
9. <span data-ttu-id="f2853-129">Velg **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="f2853-129">Select **Add**.</span></span>
10. <span data-ttu-id="f2853-130">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="f2853-130">Select **Save**.</span></span>
11. <span data-ttu-id="f2853-131">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="f2853-131">Close the page.</span></span>
12. <span data-ttu-id="f2853-132">Velg **Endre status**.</span><span class="sxs-lookup"><span data-stu-id="f2853-132">Select **Change status**.</span></span>
13. <span data-ttu-id="f2853-133">Velg **Fullfør**.</span><span class="sxs-lookup"><span data-stu-id="f2853-133">Select **Complete**.</span></span>
14. <span data-ttu-id="f2853-134">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="f2853-134">Select **OK**.</span></span>
15. <span data-ttu-id="f2853-135">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="f2853-135">Close the page.</span></span>

## <a name="register-a-new-repository"></a><span data-ttu-id="f2853-136">Registrere et nytt repositorium</span><span class="sxs-lookup"><span data-stu-id="f2853-136">Register a new repository</span></span>

1. <span data-ttu-id="f2853-137">Gå til **Organisasjonsstyring \> Arbeidsområder \> Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="f2853-137">Go to **Organization administration \> Workspaces \> Electronic reporting**.</span></span>

2. <span data-ttu-id="f2853-138">I delen **Konfigurasjonsleverandører** velger du **Litware, Inc.**-flisen.</span><span class="sxs-lookup"><span data-stu-id="f2853-138">In the **Configuration providers** section, select the **Litware, Inc.** tile.</span></span>

3. <span data-ttu-id="f2853-139">På **Litware, Inc.**-flisen velger du **Repositorier**.</span><span class="sxs-lookup"><span data-stu-id="f2853-139">On the **Litware, Inc.** tile, select **Repositories**.</span></span>

    <span data-ttu-id="f2853-140">Nå kan du åpne listen over repositorier for konfigurasjonsleverandøren Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="f2853-140">You can now open the list of repositories for the Litware, Inc. configuration provider.</span></span>

4. <span data-ttu-id="f2853-141">Velg **Legg til** for å åpne dialogboksen med rullegardinliste.</span><span class="sxs-lookup"><span data-stu-id="f2853-141">Select **Add** to open the drop-down dialog box.</span></span>

    <span data-ttu-id="f2853-142">Du kan nå legge til et nytt repositorium.</span><span class="sxs-lookup"><span data-stu-id="f2853-142">You can now add a new repository.</span></span>

5. <span data-ttu-id="f2853-143">I feltet **Konfigurasjonsrepositorium** velger du **LCS**.</span><span class="sxs-lookup"><span data-stu-id="f2853-143">In the **Configuration repository enter** field, select **LCS**.</span></span>
6. <span data-ttu-id="f2853-144">Velg **Opprett repositorium**.</span><span class="sxs-lookup"><span data-stu-id="f2853-144">Select **Create repository**.</span></span>
7. <span data-ttu-id="f2853-145">Angi eller velg en verdi i feltet **Prosjekt**.</span><span class="sxs-lookup"><span data-stu-id="f2853-145">In the **Project** field, enter or select a value.</span></span>

    <span data-ttu-id="f2853-146">I dette eksemplet velger du det ønskede LCS-prosjektet.</span><span class="sxs-lookup"><span data-stu-id="f2853-146">For this example, select the desired LCS project.</span></span> <span data-ttu-id="f2853-147">Du må ha [tilgang](#accessconditions) til prosjektet.</span><span class="sxs-lookup"><span data-stu-id="f2853-147">You must have [access](#accessconditions) to the project.</span></span>

8. <span data-ttu-id="f2853-148">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="f2853-148">Select **OK**.</span></span>

    <span data-ttu-id="f2853-149">Fullfør en ny oppføring i repositoriet.</span><span class="sxs-lookup"><span data-stu-id="f2853-149">Complete a new repository entry.</span></span>

9. <span data-ttu-id="f2853-150">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="f2853-150">In the list, mark the selected row.</span></span>

    <span data-ttu-id="f2853-151">I dette eksemplet velger du repositoriumposten i **LCS**.</span><span class="sxs-lookup"><span data-stu-id="f2853-151">For this example, select the **LCS** repository record.</span></span>

    <span data-ttu-id="f2853-152">Vær oppmerksom på at et registrert repositorium er merket med gjeldende leverandør.</span><span class="sxs-lookup"><span data-stu-id="f2853-152">Note that a registered repository is marked by the current provider.</span></span> <span data-ttu-id="f2853-153">Det er med andre ord bare konfigurasjoner som eies av denne leverandøren, som kan plasseres i repositoriet og som derfor lastes opp til det valgte LCS-prosjektet.</span><span class="sxs-lookup"><span data-stu-id="f2853-153">In other words, only configurations that are owned by that provider can be put in this repository and therefore uploaded into the selected LCS project.</span></span>

10. <span data-ttu-id="f2853-154">Velg **Åpne**.</span><span class="sxs-lookup"><span data-stu-id="f2853-154">Select **Open**.</span></span>

    <span data-ttu-id="f2853-155">Du åpner repositoriet for å vise listen over ER-konfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="f2853-155">You open the repository to view the list of ER configurations.</span></span> <span data-ttu-id="f2853-156">Hvis det valgte prosjektet ennå ikke er brukt for deling av ER-konfigurasjoner, vil listen være tom.</span><span class="sxs-lookup"><span data-stu-id="f2853-156">If the selected project hasn't yet been used for ER configurations sharing, the list will be empty.</span></span>

11. <span data-ttu-id="f2853-157">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="f2853-157">Close the page.</span></span>
12. <span data-ttu-id="f2853-158">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="f2853-158">Close the page.</span></span>

## <a name="upload-a-configuration-into-lcs"></a><span data-ttu-id="f2853-159">Laste opp en konfigurasjon til LCS</span><span class="sxs-lookup"><span data-stu-id="f2853-159">Upload a configuration into LCS</span></span>

1. <span data-ttu-id="f2853-160">Gå til **Organisasjonsstyring \> Elektronisk rapportering \> Konfigurasjoner**.</span><span class="sxs-lookup"><span data-stu-id="f2853-160">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="f2853-161">På siden **Konfigurasjoner** i konfigurasjonstreet velger du **Eksempelmodellkonfigurasjon**.</span><span class="sxs-lookup"><span data-stu-id="f2853-161">On the **Configurations** page, in the configurations tree, select **Sample model configuration**.</span></span>

    <span data-ttu-id="f2853-162">Du må velge en opprettet konfigurasjon som allerede er fullført.</span><span class="sxs-lookup"><span data-stu-id="f2853-162">You must select a created configuration that has been already completed.</span></span>

3. <span data-ttu-id="f2853-163">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="f2853-163">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="f2853-164">For dette eksemplet velger du versjonen av den valgte konfigurasjonen som har statusen **Fullført**.</span><span class="sxs-lookup"><span data-stu-id="f2853-164">For this example, select the version of the selected configuration that has a status of **Completed**.</span></span>

4. <span data-ttu-id="f2853-165">Velg **Endre status**.</span><span class="sxs-lookup"><span data-stu-id="f2853-165">Select **Change status**.</span></span>
5. <span data-ttu-id="f2853-166">Velg **Del**.</span><span class="sxs-lookup"><span data-stu-id="f2853-166">Select **Share**.</span></span>

    <span data-ttu-id="f2853-167">Statusen for konfigurasjonen endres fra **Fullført** til **Delt** når konfigurasjonen er publisert i LCS.</span><span class="sxs-lookup"><span data-stu-id="f2853-167">The status of the configuration is changed from **Completed** to **Shared** when the configuration is published in LCS.</span></span>

6. <span data-ttu-id="f2853-168">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="f2853-168">Select **OK**.</span></span>
7. <span data-ttu-id="f2853-169">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="f2853-169">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="f2853-170">For dette eksemplet velger du konfigurasjonsversjonen som har statusen **Delt**.</span><span class="sxs-lookup"><span data-stu-id="f2853-170">For this example, select the configuration version that has a status of **Shared**.</span></span>

    <span data-ttu-id="f2853-171">Vær oppmerksom på at statusen for den valgte versjonen ble endret fra **Fullført** til **Delt**.</span><span class="sxs-lookup"><span data-stu-id="f2853-171">Note that the status of the selected version was changed from **Completed** to **Shared**.</span></span>

8. <span data-ttu-id="f2853-172">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="f2853-172">Close the page.</span></span>
9. <span data-ttu-id="f2853-173">Velg **Repositorier**.</span><span class="sxs-lookup"><span data-stu-id="f2853-173">Select **Repositories**.</span></span>

    <span data-ttu-id="f2853-174">Nå kan du åpne listen over repositorier for konfigurasjonsleverandøren Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="f2853-174">You can now open the list of repositories for the Litware, Inc. configuration provider.</span></span>

10. <span data-ttu-id="f2853-175">Velg **Åpne**.</span><span class="sxs-lookup"><span data-stu-id="f2853-175">Select **Open**.</span></span>

    <span data-ttu-id="f2853-176">I dette eksemplet velger du repositoriet **LCS** og åpner det.</span><span class="sxs-lookup"><span data-stu-id="f2853-176">For this example, select the **LCS** repository, and open it.</span></span>

    <span data-ttu-id="f2853-177">Vær oppmerksom på at den valgte konfigurasjonen vises som et anleggsmiddel for det valgte LCS-prosjektet.</span><span class="sxs-lookup"><span data-stu-id="f2853-177">Notice that the selected configuration is shown as an asset of the selected LCS project.</span></span>

11. <span data-ttu-id="f2853-178">Åpne LCS ved å gå til <https://lcs.dynamics.com>.</span><span class="sxs-lookup"><span data-stu-id="f2853-178">Open LCS by going to <https://lcs.dynamics.com>.</span></span>
12. <span data-ttu-id="f2853-179">Åpne et prosjekt som ble brukt tidligere til registrering av repositorium.</span><span class="sxs-lookup"><span data-stu-id="f2853-179">Open a project that was used earlier for repository registration.</span></span>
13. <span data-ttu-id="f2853-180">Åpne aktivabiblioteket for prosjektet.</span><span class="sxs-lookup"><span data-stu-id="f2853-180">Open the Asset library of the project.</span></span>
14. <span data-ttu-id="f2853-181">Velg aktivatypen **GER-konfigurasjon**.</span><span class="sxs-lookup"><span data-stu-id="f2853-181">Select the **GER configuration** asset type.</span></span>

    <span data-ttu-id="f2853-182">ER-konfigurasjonen du lastet opp, bør nå vises.</span><span class="sxs-lookup"><span data-stu-id="f2853-182">The ER configuration that you uploaded should be listed.</span></span>

    <span data-ttu-id="f2853-183">Vær oppmerksom på at den opplastede LCS-konfigurasjonen kan importeres til en annen forekomst hvis leverandører har tilgang til dette LCS-prosjektet.</span><span class="sxs-lookup"><span data-stu-id="f2853-183">Note that the uploaded LCS configuration can be imported into another instance if providers have access to this LCS project.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]