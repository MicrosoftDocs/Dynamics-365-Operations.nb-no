---
title: Laste ned elektroniske rapporteringskonfigurasjoner fra Lifecycle Services
description: Dette emnet forklarer hvordan du laster ned konfigurasjoner for elektronisk rapportering (ER) fra Microsoft Dynamics Lifecycle Services (LCS).
author: NickSelin
ms.date: 08/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionImport, ERWorkspace
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 14f0f2b1a4d63101d432b1361379c61a70ac9345
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271189"
---
# <a name="download-electronic-reporting-configurations-from-lifecycle-services"></a><span data-ttu-id="e91e4-103">Laste ned konfigurasjoner for elektronisk rapportering fra Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="e91e4-103">Download Electronic reporting configurations from Lifecycle Services</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e91e4-104">Dette emnet forklarer hvordan du laster ned den nyeste versjonen av [Konfigurasjoner for elektronisk rapportering (ER)](general-electronic-reporting.md#Configuration) fra [Delt aktivabibliotek](../lifecycle-services/asset-library.md) i Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="e91e4-104">This topic explains how to download the newest version of [Electronic reporting (ER) configurations](general-electronic-reporting.md#Configuration) from the [Shared asset library](../lifecycle-services/asset-library.md) in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e91e4-105">Bruken av Lifecycle Services (LCS) som et lagringsrepositorium for konfigurasjoner for elektronisk rapportering (ER) blir [avskrevet](../../../finance/get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release).</span><span class="sxs-lookup"><span data-stu-id="e91e4-105">The use of LCS as a storage repository for ER configurations is being [deprecated](../../../finance/get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release).</span></span> <span data-ttu-id="e91e4-106">Hvis du vil ha mer informasjon, se [Regulatory Configuration Service (RCS) – avskrivning av lager for Lifecycle Services (LCS)](../../../finance/localizations/rcs-lcs-repo-dep-faq.md).</span><span class="sxs-lookup"><span data-stu-id="e91e4-106">For more information, see [Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) storage deprecation](../../../finance/localizations/rcs-lcs-repo-dep-faq.md).</span></span>

1. <span data-ttu-id="e91e4-107">Logg på programmet med én av følgende roller:</span><span class="sxs-lookup"><span data-stu-id="e91e4-107">Sign in to the application by using one of the following roles:</span></span>

    - <span data-ttu-id="e91e4-108">Utvikler av elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="e91e4-108">Electronic reporting developer</span></span>
    - <span data-ttu-id="e91e4-109">Funksjonell konsulent for elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="e91e4-109">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="e91e4-110">Systemansvarlig</span><span class="sxs-lookup"><span data-stu-id="e91e4-110">System administrator</span></span>

2. <span data-ttu-id="e91e4-111">Gå til **Organisasjonsstyring** &gt; **Arbeidsområder** &gt; **Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="e91e4-111">Go to **Organization administration** &gt; **Workspaces** &gt; **Electronic reporting**.</span></span>
3. <span data-ttu-id="e91e4-112">I delen **Konfigurasjonsleverandører** velger du **Microsoft**-flisen.</span><span class="sxs-lookup"><span data-stu-id="e91e4-112">In the **Configuration providers** section, select the **Microsoft** tile.</span></span>
4. <span data-ttu-id="e91e4-113">På **Microsoft**-flisen velger du **Repositorier**.</span><span class="sxs-lookup"><span data-stu-id="e91e4-113">On the **Microsoft** tile, select **Repositories**.</span></span>

    <span data-ttu-id="e91e4-114">[![Microsoft-flis på siden Lokaliseringskonfigurasjon](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)</span><span class="sxs-lookup"><span data-stu-id="e91e4-114">[![Microsoft tile on the Localization configurations page](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)</span></span>

5. <span data-ttu-id="e91e4-115">På **Konfigurasjonsrepositorier**-siden i rutenettet velger du det eksisterende repositoriet for **LCS**-typen.</span><span class="sxs-lookup"><span data-stu-id="e91e4-115">On the **Configuration repositories** page, in the grid, select the existing repository of the **LCS** type.</span></span> <span data-ttu-id="e91e4-116">Hvis dette repositoriet ikke vises i rutenettet, gjør du følgende:</span><span class="sxs-lookup"><span data-stu-id="e91e4-116">If this repository doesn't appear in the grid, follow these steps:</span></span>

    1. <span data-ttu-id="e91e4-117">Velg **Legg til** for å legge til et repositorium.</span><span class="sxs-lookup"><span data-stu-id="e91e4-117">Select **Add** to add a repository.</span></span>
    2. <span data-ttu-id="e91e4-118">Velg **LCS** som type repositorium.</span><span class="sxs-lookup"><span data-stu-id="e91e4-118">Select **LCS** as the repository type.</span></span>
    3. <span data-ttu-id="e91e4-119">Velg **Opprett repositorium**.</span><span class="sxs-lookup"><span data-stu-id="e91e4-119">Select **Create repository**.</span></span>
    4. <span data-ttu-id="e91e4-120">Hvis du blir spurt om godkjenning, følger du instruksjonene på skjermen.</span><span class="sxs-lookup"><span data-stu-id="e91e4-120">If you're prompted about authorization, follow the on-screen instructions.</span></span>
    5. <span data-ttu-id="e91e4-121">Angi et navn og en beskrivelse for repositoriet.</span><span class="sxs-lookup"><span data-stu-id="e91e4-121">Enter a name and description for the repository.</span></span>
    6. <span data-ttu-id="e91e4-122">Velg **OK** for å bekrefte den nye repositoriumoppføringen.</span><span class="sxs-lookup"><span data-stu-id="e91e4-122">Select **OK** to confirm the new repository entry.</span></span>
    7. <span data-ttu-id="e91e4-123">I rutenettet velger du det nye repositoriet i **LCS**-typen.</span><span class="sxs-lookup"><span data-stu-id="e91e4-123">In the grid, select the new repository of the **LCS** type.</span></span>

6. <span data-ttu-id="e91e4-124">Velg **Åpne** for å vise listen over ER-konfigurasjoner for det valgte repositoriet.</span><span class="sxs-lookup"><span data-stu-id="e91e4-124">Select **Open** to view the list of ER configurations for the selected repository.</span></span>

    <span data-ttu-id="e91e4-125">[![Konfigurasjonsrepositorier-side](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)</span><span class="sxs-lookup"><span data-stu-id="e91e4-125">[![Configuration repositories page](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)</span></span>

    > [!TIP]
    > <span data-ttu-id="e91e4-126">Hvis du har problemer med å få tilgang til LCS-repositoriet for å laste ned konfigurasjoner fra det delte aktivabiblioteket i LCS, kan i stedet du laste ned konfigurasjoner fra [Globalt repositorium](er-download-configurations-global-repo.md).</span><span class="sxs-lookup"><span data-stu-id="e91e4-126">If you have trouble accessing the LCS repository to download configurations from the Shared asset library in LCS, you can download configurations from the [Global repository](er-download-configurations-global-repo.md) instead.</span></span>

7. <span data-ttu-id="e91e4-127">Velg den obligatoriske ER-konfigurasjonen i konfigurasjonstreet i den venstre ruten.</span><span class="sxs-lookup"><span data-stu-id="e91e4-127">In the configurations tree in the left pane, select the required ER configuration.</span></span>
8. <span data-ttu-id="e91e4-128">I **Versjoner**-hurtigkategorien velger du den nødvendige versjonen av den valgte ER-konfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="e91e4-128">On the **Versions** FastTab, select the required version of the selected ER configuration.</span></span>
9. <span data-ttu-id="e91e4-129">Velg **Importer** for å laste ned den valgte versjonen fra LCS til den gjeldende forekomsten.</span><span class="sxs-lookup"><span data-stu-id="e91e4-129">Select **Import** to download the selected version from LCS to the current instance.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e91e4-130">**Importer**-knappen er ikke tilgjengelig for ER-konfigurasjonsversjoner som allerede finnes i den gjeldende forekomsten.</span><span class="sxs-lookup"><span data-stu-id="e91e4-130">The **Import** button is unavailable for ER configuration versions that are already present in the current instance.</span></span>

    <span data-ttu-id="e91e4-131">[![Konfigurasjonsrepositorium-side](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)</span><span class="sxs-lookup"><span data-stu-id="e91e4-131">[![Configuration repository page](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)</span></span>

> [!NOTE]
> <span data-ttu-id="e91e4-132">Avhengig av ER-innstillingene valideres konfigurasjonene når de er importert.</span><span class="sxs-lookup"><span data-stu-id="e91e4-132">Depending on the ER settings, configurations are validated after they are imported.</span></span> <span data-ttu-id="e91e4-133">Du kan få beskjed om eventuelle problemer som oppdages.</span><span class="sxs-lookup"><span data-stu-id="e91e4-133">You might be notified about any inconsistency issues that are discovered.</span></span> <span data-ttu-id="e91e4-134">Du må løse disse problemene før du kan bruke den importerte konfigurasjonsversjonen.</span><span class="sxs-lookup"><span data-stu-id="e91e4-134">You must resolve those issues before you can use the imported configuration version.</span></span> <span data-ttu-id="e91e4-135">Hvis du vil ha mer informasjon, se listen over relaterte emner for dette emnet.</span><span class="sxs-lookup"><span data-stu-id="e91e4-135">For more information, see the list of related topics for this topic.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e91e4-136">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="e91e4-136">Additional resources</span></span>

[<span data-ttu-id="e91e4-137">Oversikt over elektronisk rapportering (ER)</span><span class="sxs-lookup"><span data-stu-id="e91e4-137">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="e91e4-138">Last ned ER-konfigurasjoner fra det globale repositoriet for konfigurasjonstjenesten</span><span class="sxs-lookup"><span data-stu-id="e91e4-138">Download ER configurations from the Global repository of Configuration service</span></span>](er-download-configurations-global-repo.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
