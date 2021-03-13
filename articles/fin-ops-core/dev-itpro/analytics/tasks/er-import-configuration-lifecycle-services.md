---
title: Importere en konfigurasjon fra Lifecycle Services
description: Dette emnet beskriver hvordan du importerer en ny versjon av en ER-konfigurasjon (Elektronisk rapportering) fra Microsoft Dynamics Lifecycle Services (LCS).
author: NickSelin
manager: AnnBe
ms.date: 09/14/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 602886b0dd729b8ec52940f42bd1c393dac8acda
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093701"
---
# <a name="import-a-configuration-from-lifecycle-services"></a><span data-ttu-id="c2eb3-103">Importere en konfigurasjon fra Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="c2eb3-103">Import a configuration from Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c2eb3-104">Dette emnet forklarer hvordan en bruker i rollen Systemansvarlig eller Utvikler av elektronisk rapportering kan importere en ny versjon av en [konfigurasjon for elektronisk rapportering (ER)](../general-electronic-reporting.md#Configuration) fra [aktivabiblioteket på prosjektnivå](../../lifecycle-services/asset-library.md) i Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="c2eb3-104">This topic explains how a user in the System administrator or Electronic reporting developer role can import a new version of an [Electronic reporting (ER) configuration](../general-electronic-reporting.md#Configuration) from the [project-level Asset library](../../lifecycle-services/asset-library.md) in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

<span data-ttu-id="c2eb3-105">I dette eksemplet skal du velge ønsket versjon av ER-konfigurasjonen og importere den for et eksempelfirma med navnet Litware, Inc. Denne fremgangsmåten kan fullføres i alle firmaer, ettersom ER-konfigurasjoner deles mellom firmaer.</span><span class="sxs-lookup"><span data-stu-id="c2eb3-105">In this example, you will select the desired version of the ER configuration and import it for a sample company that is named Litware, Inc. These steps can be completed in any company, because ER configurations are shared among companies.</span></span> <span data-ttu-id="c2eb3-106">For å fullføre disse trinnene må du først fullføre trinnene i [Laste opp en ER-konfigurasjon til Lifecycle Services](er-upload-configuration-into-lifecycle-services.md).</span><span class="sxs-lookup"><span data-stu-id="c2eb3-106">To complete these steps, you must first complete the steps in [Upload a configuration into Lifecycle Services](er-upload-configuration-into-lifecycle-services.md).</span></span> <span data-ttu-id="c2eb3-107">Tilgang til LCS er også nødvendig.</span><span class="sxs-lookup"><span data-stu-id="c2eb3-107">Access to LCS is also required.</span></span>

1. <span data-ttu-id="c2eb3-108">Logg på programmet med én av følgende roller:</span><span class="sxs-lookup"><span data-stu-id="c2eb3-108">Sign in to the application by using one of the following roles:</span></span>

    - <span data-ttu-id="c2eb3-109">Utvikler av elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="c2eb3-109">Electronic reporting developer</span></span>
    - <span data-ttu-id="c2eb3-110">Systemansvarlig</span><span class="sxs-lookup"><span data-stu-id="c2eb3-110">System administrator</span></span>

2. <span data-ttu-id="c2eb3-111">Gå til **Organisasjonsstyring** \> **Arbeidsområder** \> **Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="c2eb3-111">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="c2eb3-112">Velg **Konfigurasjoner**.</span><span class="sxs-lookup"><span data-stu-id="c2eb3-112">Select **Configurations**.</span></span>

<a name="accessconditions"></a>
> [!NOTE]
> <span data-ttu-id="c2eb3-113">Kontroller at den gjeldende Dynamics 365 Finance-brukeren er medlem av LCS-prosjektet som inneholder aktivabiblioteket som brukeren vil [bruke](../../lifecycle-services/asset-library.md#asset-library-support) for å importere ER-konfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="c2eb3-113">Make sure that the current Dynamics 365 Finance user is a member of the LCS project that contains the Asset library that the user wants to [access](../../lifecycle-services/asset-library.md#asset-library-support) to import ER configurations.</span></span>
>
> <span data-ttu-id="c2eb3-114">Du kan ikke få tilgang til et LCS-prosjekt fra et ER-repositorium som representerer et annet domene enn domenet som brukes i Finance.</span><span class="sxs-lookup"><span data-stu-id="c2eb3-114">You can't access an LCS project from an ER repository that represents a different domain than the domain that is used in Finance.</span></span> <span data-ttu-id="c2eb3-115">Hvis du prøver, vises det en tom liste over LCS-prosjekter, og du kan ikke importere ER-konfigurasjonene fra aktivabiblioteket på prosjektnivå i LCS.</span><span class="sxs-lookup"><span data-stu-id="c2eb3-115">If you try, an empty list of LCS projects will be shown, and you won't be able to import ER configurations from the project-level Asset library in LCS.</span></span> <span data-ttu-id="c2eb3-116">Hvis du vil ha tilgang til aktivabiblioteker på prosjektnivå fra et ER-repositorium som brukes til å importere ER-konfigurasjoner, logger du på Finance-modulen ved hjelp av legitimasjonen til en bruker som tilhører leieren (domenet) som gjeldende Finance-forekomst er klargjort for.</span><span class="sxs-lookup"><span data-stu-id="c2eb3-116">To access project-level Asset libraries from an ER repository that is used to import ER configurations, sign in to Finance by using the credentials of a user who belongs to the tenant (domain) that the current Finance instance has been provisioned for.</span></span>

## <a name="delete-a-shared-version-of-a-data-model-configuration"></a><span data-ttu-id="c2eb3-117">Slette en delt versjon av en datamodellkonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="c2eb3-117">Delete a shared version of a data model configuration</span></span>

1. <span data-ttu-id="c2eb3-118">På siden **Konfigurasjoner** i konfigurasjonstreet velger du **Eksempelmodellkonfigurasjon**.</span><span class="sxs-lookup"><span data-stu-id="c2eb3-118">On the **Configurations** page, in the configurations tree, select **Sample model configuration**.</span></span>

    <span data-ttu-id="c2eb3-119">Du opprettet den første versjonen av en konfigurasjon for eksempeldatamodell og publiserte den i LCS da du fullførte fremgangsmåten i [Laste opp en konfigurasjon til Lifecycle Services](er-upload-configuration-into-lifecycle-services.md).</span><span class="sxs-lookup"><span data-stu-id="c2eb3-119">You created the first version of a sample data model configuration and published it to LCS when you completed the steps in [Upload a configuration into Lifecycle Services](er-upload-configuration-into-lifecycle-services.md).</span></span> <span data-ttu-id="c2eb3-120">I denne fremgangsmåten sletter du den versjonen av ER-konfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="c2eb3-120">In this procedure, you will delete that version of the ER configuration.</span></span> <span data-ttu-id="c2eb3-121">Du skal deretter importere denne versjonen fra LCS senere i dette emnet.</span><span class="sxs-lookup"><span data-stu-id="c2eb3-121">You will then import that version from LCS later in this topic.</span></span>

2. <span data-ttu-id="c2eb3-122">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="c2eb3-122">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="c2eb3-123">For dette eksemplet velger du versjonen av konfigurasjonen som har statusen **Delt**.</span><span class="sxs-lookup"><span data-stu-id="c2eb3-123">For this example, select the version of the configuration that has a status of **Shared**.</span></span> <span data-ttu-id="c2eb3-124">Denne statusen angir at konfigurasjonen er publisert til LCS.</span><span class="sxs-lookup"><span data-stu-id="c2eb3-124">This status indicates that the configuration has been published to LCS.</span></span>

3. <span data-ttu-id="c2eb3-125">Velg **Endre status**.</span><span class="sxs-lookup"><span data-stu-id="c2eb3-125">Select **Change status**.</span></span>
4. <span data-ttu-id="c2eb3-126">Velg **Avslutt**.</span><span class="sxs-lookup"><span data-stu-id="c2eb3-126">Select **Discontinue**.</span></span>

    <span data-ttu-id="c2eb3-127">Ved å endre statusen for den valgte versjonen fra **Delt** til **Avsluttet**, gjør du versjonen tilgjengelig for sletting.</span><span class="sxs-lookup"><span data-stu-id="c2eb3-127">By changing the status of the selected version from **Shared** to **Discontinued**, you make the version available for deletion.</span></span>

5. <span data-ttu-id="c2eb3-128">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="c2eb3-128">Select **OK**.</span></span>
6. <span data-ttu-id="c2eb3-129">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="c2eb3-129">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="c2eb3-130">For dette eksemplet velger du versjonen av konfigurasjonen som har statusen **Avsluttet**.</span><span class="sxs-lookup"><span data-stu-id="c2eb3-130">For this example, select the version of the configuration that has a status of **Discontinued**.</span></span>

7. <span data-ttu-id="c2eb3-131">Velg **Slett**.</span><span class="sxs-lookup"><span data-stu-id="c2eb3-131">Select **Delete**.</span></span>
8. <span data-ttu-id="c2eb3-132">Velg **Ja**.</span><span class="sxs-lookup"><span data-stu-id="c2eb3-132">Select **Yes**.</span></span>

    <span data-ttu-id="c2eb3-133">Legg merke til at bare utkastversjon 2 av den valgte datamodellkonfigurasjonen nå er tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="c2eb3-133">Notice that the only draft version 2 of the selected data model configuration is now available.</span></span>

9. <span data-ttu-id="c2eb3-134">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="c2eb3-134">Close the page.</span></span>

## <a name="import-a-shared-version-of-a-data-model-configuration-from-lcs"></a><span data-ttu-id="c2eb3-135">Importere en delt versjon av en datamodellkonfigurasjon fra LCS</span><span class="sxs-lookup"><span data-stu-id="c2eb3-135">Import a shared version of a data model configuration from LCS</span></span>

1. <span data-ttu-id="c2eb3-136">Gå til **Organisasjonsstyring \> Arbeidsområder \> Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="c2eb3-136">Go to **Organization administration \> Workspaces \> Electronic reporting**.</span></span>

2. <span data-ttu-id="c2eb3-137">I delen **Konfigurasjonsleverandører** velger du **Litware, Inc.**-flisen.</span><span class="sxs-lookup"><span data-stu-id="c2eb3-137">In the **Configuration providers** section, select the **Litware, Inc.** tile.</span></span>

3. <span data-ttu-id="c2eb3-138">På **Litware, Inc.**-flisen velger du **Repositorier**.</span><span class="sxs-lookup"><span data-stu-id="c2eb3-138">On the **Litware, Inc.** tile, select **Repositories**.</span></span>

    <span data-ttu-id="c2eb3-139">Nå kan du åpne listen over repositorier for konfigurasjonsleverandøren Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="c2eb3-139">You can now open the list of repositories for the Litware, Inc. configuration provider.</span></span>

4. <span data-ttu-id="c2eb3-140">Velg **Åpne**.</span><span class="sxs-lookup"><span data-stu-id="c2eb3-140">Select **Open**.</span></span>

    <span data-ttu-id="c2eb3-141">I dette eksemplet velger du repositoriet **LCS** og åpner det.</span><span class="sxs-lookup"><span data-stu-id="c2eb3-141">For this example, select the **LCS** repository, and open it.</span></span> <span data-ttu-id="c2eb3-142">Du må ha [tilgang](#accessconditions) til LCS-prosjektet og aktivabiblioteket som brukes av det valgte ER-repositoriet.</span><span class="sxs-lookup"><span data-stu-id="c2eb3-142">You must have [access](#accessconditions) to the LCS project and to the Asset library that is accessed by the selected ER repository.</span></span>

5. <span data-ttu-id="c2eb3-143">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="c2eb3-143">In the list, mark the selected row.</span></span>

    <span data-ttu-id="c2eb3-144">For dette eksemplet velger du den første versjonen av **Eksempelmodellkonfigurasjon** i versjonslisten.</span><span class="sxs-lookup"><span data-stu-id="c2eb3-144">For this example, select the first version of **Sample model configuration** in the version list.</span></span>

6. <span data-ttu-id="c2eb3-145">Velg **Import**.</span><span class="sxs-lookup"><span data-stu-id="c2eb3-145">Select **Import**.</span></span>
7. <span data-ttu-id="c2eb3-146">Velg **Ja** for å bekrefte importen av den valgte versjonen fra LCS.</span><span class="sxs-lookup"><span data-stu-id="c2eb3-146">Select **Yes** to confirm the import of the selected version from LCS.</span></span>

    <span data-ttu-id="c2eb3-147">En informasjonsmelding bekrefter at den valgte versjonen er importert.</span><span class="sxs-lookup"><span data-stu-id="c2eb3-147">An informational message confirms that the selected version was successfully imported.</span></span>

8. <span data-ttu-id="c2eb3-148">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="c2eb3-148">Close the page.</span></span>
9. <span data-ttu-id="c2eb3-149">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="c2eb3-149">Close the page.</span></span>
10. <span data-ttu-id="c2eb3-150">Velg **Konfigurasjoner**.</span><span class="sxs-lookup"><span data-stu-id="c2eb3-150">Select **Configurations**.</span></span>
11. <span data-ttu-id="c2eb3-151">Velg **Eksempelmodellkonfigurasjon** i treet.</span><span class="sxs-lookup"><span data-stu-id="c2eb3-151">In the tree, select **Sample model configuration**.</span></span>
12. <span data-ttu-id="c2eb3-152">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="c2eb3-152">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="c2eb3-153">For dette eksemplet velger du versjonen av konfigurasjonen som har statusen **Delt**.</span><span class="sxs-lookup"><span data-stu-id="c2eb3-153">For this example, select the version of the configuration that has a status of **Shared**.</span></span>

    <span data-ttu-id="c2eb3-154">Legg merke til at delt versjon 1 av den valgte datamodellkonfigurasjonen nå også er tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="c2eb3-154">Notice that shared version 1 of the selected data model configuration is also available now.</span></span>
