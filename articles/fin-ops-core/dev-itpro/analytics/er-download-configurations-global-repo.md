---
title: Last ned ER-konfigurasjoner fra det globale repositoriet for konfigurasjonstjenesten
description: Dette emnet forklarer hvordan du laster ned elektroniske rapporteringskonfigurasjoner (ER) fra det globale repositoriet for konfigurasjonstjenesten.
author: NickSelin
ms.date: 06/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionImport, ERWorkspace, ERSolutionRepositoryTable
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 6f74602cafe3f0848a9e03f17300ca6242fe1545
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/13/2021
ms.locfileid: "5893986"
---
# <a name="download-er-configurations-from-the-global-repository-of-configuration-service"></a><span data-ttu-id="a91a7-103">Last ned ER-konfigurasjoner fra det globale repositoriet for konfigurasjonstjenesten</span><span class="sxs-lookup"><span data-stu-id="a91a7-103">Download ER configurations from the Global repository of Configuration service</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a91a7-104">Dette emnet forklarer hvordan du laster ned [elektroniske rapporteringskonfigurasjoner (ER)](general-electronic-reporting.md#Configuration) fra det globale repositoriet for konfigurasjonstjenesten.</span><span class="sxs-lookup"><span data-stu-id="a91a7-104">This topic explains how to download [Electronic reporting (ER) configurations](general-electronic-reporting.md#Configuration) from the Global repository of configuration service.</span></span> <span data-ttu-id="a91a7-105">Hvis du vil ha mer informasjon, kan du se [Microsoft Dynamics 365 for Finance and Operations – Regulatory Services, konfigurasjonstjeneste](/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration).</span><span class="sxs-lookup"><span data-stu-id="a91a7-105">For more information, see [Microsoft Dynamics 365 for Finance and Operations - Regulatory Services, Configuration service](/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration).</span></span>

## <a name="open-configurations-repository"></a><span data-ttu-id="a91a7-106">Åpne konfigurasjonsrepositoriet</span><span class="sxs-lookup"><span data-stu-id="a91a7-106">Open configurations repository</span></span>

1. <span data-ttu-id="a91a7-107">Logg på Dynamics 365 Finance-programmet med én av følgende roller:</span><span class="sxs-lookup"><span data-stu-id="a91a7-107">Sign in to the Dynamics 365 Finance application using one of the following roles:</span></span>

    - <span data-ttu-id="a91a7-108">Utvikler av elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="a91a7-108">Electronic reporting developer</span></span>
    - <span data-ttu-id="a91a7-109">Funksjonell konsulent for elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="a91a7-109">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="a91a7-110">Systemansvarlig</span><span class="sxs-lookup"><span data-stu-id="a91a7-110">System administrator</span></span>

2. <span data-ttu-id="a91a7-111">Gå til **Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="a91a7-111">Go to **Organization administration > Workspaces > Electronic reporting**.</span></span>
3. <span data-ttu-id="a91a7-112">I delen **Konfigurasjonsleverandører** velger du **Microsoft**-flisen.</span><span class="sxs-lookup"><span data-stu-id="a91a7-112">In the **Configuration providers** section, select the **Microsoft** tile.</span></span>
3. <span data-ttu-id="a91a7-113">På **Microsoft**-flisen velger du **Repositorier**.</span><span class="sxs-lookup"><span data-stu-id="a91a7-113">On the **Microsoft** tile, select **Repositories**.</span></span>

    ![Arbeidsområdet Elektronisk rapportering](./media/er-download-configurations-global-repo-er-workspace.png)

4. <span data-ttu-id="a91a7-115">På **Konfigurasjonsrepositorier**-siden i rutenettet velger du det eksisterende repositoriet for **Global**-typen.</span><span class="sxs-lookup"><span data-stu-id="a91a7-115">On the **Configuration repositories** page, in the grid, select the existing repository of the **Global** type.</span></span> <span data-ttu-id="a91a7-116">Hvis dette repositoriet ikke vises i rutenettet, gjør du følgende:</span><span class="sxs-lookup"><span data-stu-id="a91a7-116">If this repository doesn't appear in the grid, follow these steps:</span></span>

    1. <span data-ttu-id="a91a7-117">Velg **Legg til** for å legge til et nytt repositorium.</span><span class="sxs-lookup"><span data-stu-id="a91a7-117">Select **Add** to add a new repository.</span></span>
    2. <span data-ttu-id="a91a7-118">Velg **Global** som repositoriumstype, og velg deretter **Opprett repositorium**.</span><span class="sxs-lookup"><span data-stu-id="a91a7-118">Select **Global** as the repository type, and then select **Create repository**.</span></span>
    3. <span data-ttu-id="a91a7-119">Hvis du blir bedt om det, følger du autorisasjonsinstruksjonene.</span><span class="sxs-lookup"><span data-stu-id="a91a7-119">If prompted, follow the authorization instructions.</span></span>
    4. <span data-ttu-id="a91a7-120">Skriv inn et navn og en beskrivelse for repositoriet, og velg deretter **OK** for å bekrefte det nye repositoriet.</span><span class="sxs-lookup"><span data-stu-id="a91a7-120">Enter a name and description for the repository and then select **OK** to confirm the new repository entry.</span></span>
    5. <span data-ttu-id="a91a7-121">I rutenettet velger du det nye repositoriet i **Global**-typen.</span><span class="sxs-lookup"><span data-stu-id="a91a7-121">In the grid, select the new repository of the **Global** type.</span></span>

5. <span data-ttu-id="a91a7-122">Velg **Åpne** for å vise listen over ER-konfigurasjoner for det valgte repositoriet.</span><span class="sxs-lookup"><span data-stu-id="a91a7-122">Select **Open** to view the list of ER configurations for the selected repository.</span></span>

    ![Konfigurasjonsrepositorier-side](./media/er-download-configurations-global-repo-repositories-list.png)

## <a name="import-a-single-configuration"></a><span data-ttu-id="a91a7-124">Importere én enkelt konfigurasjon</span><span class="sxs-lookup"><span data-stu-id="a91a7-124">Import a single configuration</span></span>

1. <span data-ttu-id="a91a7-125">På **Konfigurasjonsrepositorier**-siden går du til konfigurasjonstreet og velger den ønskede ER-konfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="a91a7-125">On the **Configuration repositories** page, in the configurations tree, select the ER configuration that you want.</span></span>
2. <span data-ttu-id="a91a7-126">I **Versjoner**-hurtigkategorien velger du den nødvendige versjonen av den valgte ER-konfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="a91a7-126">On the **Versions** FastTab, select the required version of the selected ER configuration.</span></span>
3. <span data-ttu-id="a91a7-127">Velg **Importer** for å laste ned den valgte versjonen fra det globale repositoriet til den gjeldende forekomsten av Finance.</span><span class="sxs-lookup"><span data-stu-id="a91a7-127">Select **Import** to download the selected version from Global repository to the current Finance instance.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a91a7-128">**Importer**-knappen er ikke tilgjengelig for ER-konfigurasjonsversjoner som allerede finnes i den gjeldende Finance-forekomsten.</span><span class="sxs-lookup"><span data-stu-id="a91a7-128">The **Import** button is unavailable for ER configuration versions that are already present in the current Finance instance.</span></span>

    ![Konfigurasjonsrepositorium-side](./media/er-download-configurations-global-repo-repository-content.png)

## <a name="import-filtered-configurations"></a><span data-ttu-id="a91a7-130">Importere filtrerte konfigurasjoner</span><span class="sxs-lookup"><span data-stu-id="a91a7-130">Import filtered configurations</span></span>

1. <span data-ttu-id="a91a7-131">På **Konfigurasjonsrepositorier**-siden går du til konfigurasjonstreet og utvider **Filter**-hurtigkategorien.</span><span class="sxs-lookup"><span data-stu-id="a91a7-131">On the **Configuration repositories** page, in the configurations tree, expand the **Filter** FastTab.</span></span>
2. <span data-ttu-id="a91a7-132">I **Koder**-rutenettet legger du til eventuelle koder som kreves.</span><span class="sxs-lookup"><span data-stu-id="a91a7-132">In the **Tags** grid, add any tags that are needed.</span></span>
3. <span data-ttu-id="a91a7-133">I **Relevans for land-/område**-feltet velger du de aktuelle lands-/områdekodene, og velger **Bruk filter**.</span><span class="sxs-lookup"><span data-stu-id="a91a7-133">In the **Country/region applicability** field, select the appropriate country/region codes, and then select  **Apply filter**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a91a7-134">I **Konfigurasjoner**-hurtigkategorien ser du alle konfigurasjonene som oppfyller de angitte utvalgsbetingelsene.</span><span class="sxs-lookup"><span data-stu-id="a91a7-134">The **Configurations** FastTab shows all the configurations that satisfy the specified selection conditions.</span></span>

4. <span data-ttu-id="a91a7-135">I **Konfigurasjoner**-hurtigkategorien velger du **Importer** for å laste ned de filtrerte konfigurasjonene fra det globale repositoriet til den gjeldende forekomsten.</span><span class="sxs-lookup"><span data-stu-id="a91a7-135">On the **Configurations** FastTab, select **Import** to download the filtered configurations from the Global repository to the current instance.</span></span>
5. <span data-ttu-id="a91a7-136">I **Konfigurasjoner**-hurtigkategorien velger du **Nullstill filter** for å tømme de angitte utvalgsbetingelsene.</span><span class="sxs-lookup"><span data-stu-id="a91a7-136">On the **Configurations** FastTab, select **Reset filter** to clean up the specified selection conditions.</span></span>

    ![Konfigurasjonsrepositorium-side](./media/er-download-configurations-global-repo-filtered-configurations.png)

> [!NOTE]
> <span data-ttu-id="a91a7-138">Avhengig av ER-innstillingene valideres konfigurasjonene når de er importert.</span><span class="sxs-lookup"><span data-stu-id="a91a7-138">Depending on the ER settings, configurations are validated after they are imported.</span></span> <span data-ttu-id="a91a7-139">Du kan få beskjed om eventuelle problemer som oppdages.</span><span class="sxs-lookup"><span data-stu-id="a91a7-139">You might be notified about any inconsistency issues that are discovered.</span></span> <span data-ttu-id="a91a7-140">Du må løse problemene før du kan bruke den importerte konfigurasjonsversjonen.</span><span class="sxs-lookup"><span data-stu-id="a91a7-140">Before you can use the imported configuration version, you must resolve the issues.</span></span> <span data-ttu-id="a91a7-141">Hvis du vil ha mer informasjon, se listen over relaterte ressurser for dette emnet.</span><span class="sxs-lookup"><span data-stu-id="a91a7-141">For more information, see the list of related resources for this topic.</span></span>

> [!NOTE]
> <span data-ttu-id="a91a7-142">ER-konfigurasjoner kan konfigureres som avhengige av andre konfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="a91a7-142">ER configurations can be configured as being dependent on other configurations.</span></span> <span data-ttu-id="a91a7-143">Sammen med en valgt konfigurasjon kan derfor også andre konfigurasjoner importeres automatisk.</span><span class="sxs-lookup"><span data-stu-id="a91a7-143">Therefore, along with a selected configuration, other configurations might be automatically imported.</span></span> <span data-ttu-id="a91a7-144">Hvis du vil ha mer informasjon om avhengigheter, se [Definere avhengigheten for ER-konfigurasjoner på andre komponenter](tasks/er-define-dependency-er-configurations-from-other-components-july-2017.md).</span><span class="sxs-lookup"><span data-stu-id="a91a7-144">For more about configuration dependencies, see [Define the dependency of ER configurations on other components](tasks/er-define-dependency-er-configurations-from-other-components-july-2017.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a91a7-145">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="a91a7-145">Additional resources</span></span>

[<span data-ttu-id="a91a7-146">Oversikt over elektronisk rapportering (ER)</span><span class="sxs-lookup"><span data-stu-id="a91a7-146">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]