---
title: Importere en konfigurasjon fra Lifecycle Services
description: Dette emnet beskriver hvordan du importerer en ny versjon av en ER-konfigurasjon (Elektronisk rapportering) fra Microsoft Dynamics Lifecycle Services (LCS).
author: NickSelin
ms.date: 06/17/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b58ecb8a7d6f52631dbca7642a4acbcf6ff895a3
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/17/2021
ms.locfileid: "6270843"
---
# <a name="import-a-configuration-from-lifecycle-services"></a><span data-ttu-id="3e698-103">Importere en konfigurasjon fra Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="3e698-103">Import a configuration from Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3e698-104">Dette emnet forklarer hvordan en bruker i rollen Systemansvarlig eller Utvikler av elektronisk rapportering kan importere en ny versjon av en [konfigurasjon for elektronisk rapportering (ER)](../general-electronic-reporting.md#Configuration) fra [aktivabiblioteket på prosjektnivå](../../lifecycle-services/asset-library.md) i Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="3e698-104">This topic explains how a user in the System administrator or Electronic reporting developer role can import a new version of an [Electronic reporting (ER) configuration](../general-electronic-reporting.md#Configuration) from the [project-level Asset library](../../lifecycle-services/asset-library.md) in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3e698-105">Bruken av Lifecycle Services (LCS) som et lagringsrepositorium for konfigurasjoner for elektronisk rapportering (ER) blir [avskrevet](../../../../finance/get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release).</span><span class="sxs-lookup"><span data-stu-id="3e698-105">The use of LCS as a storage repository for ER configurations is being [deprecated](../../../../finance/get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release).</span></span> <span data-ttu-id="3e698-106">Hvis du vil ha mer informasjon, se [Regulatory Configuration Service (RCS) – avskrivning av lager for Lifecycle Services (LCS)](../../../../finance/localizations/rcs-lcs-repo-dep-faq.md).</span><span class="sxs-lookup"><span data-stu-id="3e698-106">For more information, see [Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) storage deprecation](../../../../finance/localizations/rcs-lcs-repo-dep-faq.md).</span></span>

<span data-ttu-id="3e698-107">I dette eksemplet skal du velge ønsket versjon av ER-konfigurasjonen og importere den for et eksempelfirma med navnet Litware, Inc. Denne fremgangsmåten kan fullføres i alle firmaer, ettersom ER-konfigurasjoner deles mellom firmaer.</span><span class="sxs-lookup"><span data-stu-id="3e698-107">In this example, you will select the desired version of the ER configuration and import it for a sample company that is named Litware, Inc. These steps can be completed in any company, because ER configurations are shared among companies.</span></span> <span data-ttu-id="3e698-108">For å fullføre disse trinnene må du først fullføre trinnene i [Laste opp en ER-konfigurasjon til Lifecycle Services](er-upload-configuration-into-lifecycle-services.md).</span><span class="sxs-lookup"><span data-stu-id="3e698-108">To complete these steps, you must first complete the steps in [Upload a configuration into Lifecycle Services](er-upload-configuration-into-lifecycle-services.md).</span></span> <span data-ttu-id="3e698-109">Tilgang til LCS er også nødvendig.</span><span class="sxs-lookup"><span data-stu-id="3e698-109">Access to LCS is also required.</span></span>

1. <span data-ttu-id="3e698-110">Logg på programmet med én av følgende roller:</span><span class="sxs-lookup"><span data-stu-id="3e698-110">Sign in to the application by using one of the following roles:</span></span>

    - <span data-ttu-id="3e698-111">Utvikler av elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="3e698-111">Electronic reporting developer</span></span>
    - <span data-ttu-id="3e698-112">Systemansvarlig</span><span class="sxs-lookup"><span data-stu-id="3e698-112">System administrator</span></span>

2. <span data-ttu-id="3e698-113">Gå til **Organisasjonsstyring** \> **Arbeidsområder** \> **Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="3e698-113">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="3e698-114">Velg **Konfigurasjoner**.</span><span class="sxs-lookup"><span data-stu-id="3e698-114">Select **Configurations**.</span></span>

<a name="accessconditions"></a>
> [!NOTE]
> <span data-ttu-id="3e698-115">Kontroller at den gjeldende Dynamics 365 Finance-brukeren er medlem av LCS-prosjektet som inneholder aktivabiblioteket som brukeren vil [bruke](../../lifecycle-services/asset-library.md#asset-library-support) for å importere ER-konfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="3e698-115">Make sure that the current Dynamics 365 Finance user is a member of the LCS project that contains the Asset library that the user wants to [access](../../lifecycle-services/asset-library.md#asset-library-support) to import ER configurations.</span></span>
>
> <span data-ttu-id="3e698-116">Du kan ikke få tilgang til et LCS-prosjekt fra et ER-repositorium som representerer et annet domene enn domenet som brukes i Finance.</span><span class="sxs-lookup"><span data-stu-id="3e698-116">You can't access an LCS project from an ER repository that represents a different domain than the domain that is used in Finance.</span></span> <span data-ttu-id="3e698-117">Hvis du prøver, vises det en tom liste over LCS-prosjekter, og du kan ikke importere ER-konfigurasjonene fra aktivabiblioteket på prosjektnivå i LCS.</span><span class="sxs-lookup"><span data-stu-id="3e698-117">If you try, an empty list of LCS projects will be shown, and you won't be able to import ER configurations from the project-level Asset library in LCS.</span></span> <span data-ttu-id="3e698-118">Hvis du vil ha tilgang til aktivabiblioteker på prosjektnivå fra et ER-repositorium som brukes til å importere ER-konfigurasjoner, logger du på Finance-modulen ved hjelp av legitimasjonen til en bruker som tilhører leieren (domenet) som gjeldende Finance-forekomst er klargjort for.</span><span class="sxs-lookup"><span data-stu-id="3e698-118">To access project-level Asset libraries from an ER repository that is used to import ER configurations, sign in to Finance by using the credentials of a user who belongs to the tenant (domain) that the current Finance instance has been provisioned for.</span></span>

## <a name="delete-a-shared-version-of-a-data-model-configuration"></a><span data-ttu-id="3e698-119">Slette en delt versjon av en datamodellkonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="3e698-119">Delete a shared version of a data model configuration</span></span>

1. <span data-ttu-id="3e698-120">På siden **Konfigurasjoner** i konfigurasjonstreet velger du **Eksempelmodellkonfigurasjon**.</span><span class="sxs-lookup"><span data-stu-id="3e698-120">On the **Configurations** page, in the configurations tree, select **Sample model configuration**.</span></span>

    <span data-ttu-id="3e698-121">Du opprettet den første versjonen av en konfigurasjon for eksempeldatamodell og publiserte den i LCS da du fullførte fremgangsmåten i [Laste opp en konfigurasjon til Lifecycle Services](er-upload-configuration-into-lifecycle-services.md).</span><span class="sxs-lookup"><span data-stu-id="3e698-121">You created the first version of a sample data model configuration and published it to LCS when you completed the steps in [Upload a configuration into Lifecycle Services](er-upload-configuration-into-lifecycle-services.md).</span></span> <span data-ttu-id="3e698-122">I denne fremgangsmåten sletter du den versjonen av ER-konfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="3e698-122">In this procedure, you will delete that version of the ER configuration.</span></span> <span data-ttu-id="3e698-123">Du skal deretter importere denne versjonen fra LCS senere i dette emnet.</span><span class="sxs-lookup"><span data-stu-id="3e698-123">You will then import that version from LCS later in this topic.</span></span>

2. <span data-ttu-id="3e698-124">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="3e698-124">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="3e698-125">For dette eksemplet velger du versjonen av konfigurasjonen som har statusen **Delt**.</span><span class="sxs-lookup"><span data-stu-id="3e698-125">For this example, select the version of the configuration that has a status of **Shared**.</span></span> <span data-ttu-id="3e698-126">Denne statusen angir at konfigurasjonen er publisert til LCS.</span><span class="sxs-lookup"><span data-stu-id="3e698-126">This status indicates that the configuration has been published to LCS.</span></span>

3. <span data-ttu-id="3e698-127">Velg **Endre status**.</span><span class="sxs-lookup"><span data-stu-id="3e698-127">Select **Change status**.</span></span>
4. <span data-ttu-id="3e698-128">Velg **Avslutt**.</span><span class="sxs-lookup"><span data-stu-id="3e698-128">Select **Discontinue**.</span></span>

    <span data-ttu-id="3e698-129">Ved å endre statusen for den valgte versjonen fra **Delt** til **Avsluttet**, gjør du versjonen tilgjengelig for sletting.</span><span class="sxs-lookup"><span data-stu-id="3e698-129">By changing the status of the selected version from **Shared** to **Discontinued**, you make the version available for deletion.</span></span>

5. <span data-ttu-id="3e698-130">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="3e698-130">Select **OK**.</span></span>
6. <span data-ttu-id="3e698-131">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="3e698-131">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="3e698-132">For dette eksemplet velger du versjonen av konfigurasjonen som har statusen **Avsluttet**.</span><span class="sxs-lookup"><span data-stu-id="3e698-132">For this example, select the version of the configuration that has a status of **Discontinued**.</span></span>

7. <span data-ttu-id="3e698-133">Velg **Slett**.</span><span class="sxs-lookup"><span data-stu-id="3e698-133">Select **Delete**.</span></span>
8. <span data-ttu-id="3e698-134">Velg **Ja**.</span><span class="sxs-lookup"><span data-stu-id="3e698-134">Select **Yes**.</span></span>

    <span data-ttu-id="3e698-135">Legg merke til at bare utkastversjon 2 av den valgte datamodellkonfigurasjonen nå er tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="3e698-135">Notice that the only draft version 2 of the selected data model configuration is now available.</span></span>

9. <span data-ttu-id="3e698-136">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="3e698-136">Close the page.</span></span>

## <a name="import-a-shared-version-of-a-data-model-configuration-from-lcs"></a><span data-ttu-id="3e698-137">Importere en delt versjon av en datamodellkonfigurasjon fra LCS</span><span class="sxs-lookup"><span data-stu-id="3e698-137">Import a shared version of a data model configuration from LCS</span></span>

1. <span data-ttu-id="3e698-138">Gå til **Organisasjonsstyring \> Arbeidsområder \> Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="3e698-138">Go to **Organization administration \> Workspaces \> Electronic reporting**.</span></span>

2. <span data-ttu-id="3e698-139">I delen **Konfigurasjonsleverandører** velger du **Litware, Inc.**-flisen.</span><span class="sxs-lookup"><span data-stu-id="3e698-139">In the **Configuration providers** section, select the **Litware, Inc.** tile.</span></span>

3. <span data-ttu-id="3e698-140">På **Litware, Inc.**-flisen velger du **Repositorier**.</span><span class="sxs-lookup"><span data-stu-id="3e698-140">On the **Litware, Inc.** tile, select **Repositories**.</span></span>

    <span data-ttu-id="3e698-141">Nå kan du åpne listen over repositorier for konfigurasjonsleverandøren Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="3e698-141">You can now open the list of repositories for the Litware, Inc. configuration provider.</span></span>

4. <span data-ttu-id="3e698-142">Velg **Åpne**.</span><span class="sxs-lookup"><span data-stu-id="3e698-142">Select **Open**.</span></span>

    <span data-ttu-id="3e698-143">I dette eksemplet velger du repositoriet **LCS** og åpner det.</span><span class="sxs-lookup"><span data-stu-id="3e698-143">For this example, select the **LCS** repository, and open it.</span></span> <span data-ttu-id="3e698-144">Du må ha [tilgang](#accessconditions) til LCS-prosjektet og aktivabiblioteket som brukes av det valgte ER-repositoriet.</span><span class="sxs-lookup"><span data-stu-id="3e698-144">You must have [access](#accessconditions) to the LCS project and to the Asset library that is accessed by the selected ER repository.</span></span>

5. <span data-ttu-id="3e698-145">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="3e698-145">In the list, mark the selected row.</span></span>

    <span data-ttu-id="3e698-146">For dette eksemplet velger du den første versjonen av **Eksempelmodellkonfigurasjon** i versjonslisten.</span><span class="sxs-lookup"><span data-stu-id="3e698-146">For this example, select the first version of **Sample model configuration** in the version list.</span></span>

6. <span data-ttu-id="3e698-147">Velg **Import**.</span><span class="sxs-lookup"><span data-stu-id="3e698-147">Select **Import**.</span></span>
7. <span data-ttu-id="3e698-148">Velg **Ja** for å bekrefte importen av den valgte versjonen fra LCS.</span><span class="sxs-lookup"><span data-stu-id="3e698-148">Select **Yes** to confirm the import of the selected version from LCS.</span></span>

    <span data-ttu-id="3e698-149">En informasjonsmelding bekrefter at den valgte versjonen er importert.</span><span class="sxs-lookup"><span data-stu-id="3e698-149">An informational message confirms that the selected version was successfully imported.</span></span>

8. <span data-ttu-id="3e698-150">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="3e698-150">Close the page.</span></span>
9. <span data-ttu-id="3e698-151">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="3e698-151">Close the page.</span></span>
10. <span data-ttu-id="3e698-152">Velg **Konfigurasjoner**.</span><span class="sxs-lookup"><span data-stu-id="3e698-152">Select **Configurations**.</span></span>
11. <span data-ttu-id="3e698-153">Velg **Eksempelmodellkonfigurasjon** i treet.</span><span class="sxs-lookup"><span data-stu-id="3e698-153">In the tree, select **Sample model configuration**.</span></span>
12. <span data-ttu-id="3e698-154">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="3e698-154">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="3e698-155">For dette eksemplet velger du versjonen av konfigurasjonen som har statusen **Delt**.</span><span class="sxs-lookup"><span data-stu-id="3e698-155">For this example, select the version of the configuration that has a status of **Shared**.</span></span>

    <span data-ttu-id="3e698-156">Legg merke til at delt versjon 1 av den valgte datamodellkonfigurasjonen nå også er tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="3e698-156">Notice that shared version 1 of the selected data model configuration is also available now.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
