---
title: Laste ned elektroniske rapporteringskonfigurasjoner fra Lifecycle Services
description: Dette emnet forklarer hvordan du laster ned konfigurasjoner for elektronisk rapportering (ER) fra Microsoft Dynamics Lifecycle Services (LCS).
author: NickSelin
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionImport, ERWorkspace
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 8686d2639a3ab7f2e79944cc5eed51571d463261
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "315757"
---
# <a name="download-electronic-reporting-configurations-from-lifecycle-services"></a><span data-ttu-id="4334e-103">Laste ned konfigurasjoner for elektronisk rapportering fra Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="4334e-103">Download Electronic reporting configurations from Lifecycle Services</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4334e-104">Dette emnet forklarer hvordan du laster ned konfigurasjoner for elektronisk rapportering (ER) fra Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="4334e-104">This topic explains how to download Electronic reporting (ER) configurations from Microsoft Dynamics Lifecycle Services (LCS).</span></span>

<span data-ttu-id="4334e-105">Denne opplæringen leder deg gjennom prosessen med å laste ned nyeste versjon av konfigurasjoner for elektronisk rapportering (ER) fra Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="4334e-105">This tutorial guides you through the process of downloading the newest version of Electronic reporting (ER) configurations from Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="4334e-106">Logg på Finance and Operations med én av følgende roller:</span><span class="sxs-lookup"><span data-stu-id="4334e-106">Sign in to Finance and Operations by using one of the following roles:</span></span>

    - <span data-ttu-id="4334e-107">Utvikler av elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="4334e-107">Electronic reporting developer</span></span>
    - <span data-ttu-id="4334e-108">Funksjonell konsulent for elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="4334e-108">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="4334e-109">Systemansvarlig</span><span class="sxs-lookup"><span data-stu-id="4334e-109">System administrator</span></span>

2. <span data-ttu-id="4334e-110">Gå til **Organisasjonsstyring** &gt; **Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="4334e-110">Go to **Organization administration** &gt; **Electronic reporting**.</span></span>
3. <span data-ttu-id="4334e-111">I delen **Konfigurasjonsleverandører** velger du **Microsoft**-flisen.</span><span class="sxs-lookup"><span data-stu-id="4334e-111">In the **Configuration providers** section, select the **Microsoft** tile.</span></span>
4. <span data-ttu-id="4334e-112">I **Microsoft**-flisen klikker du **Repositorier**.</span><span class="sxs-lookup"><span data-stu-id="4334e-112">On the **Microsoft** tile, click **Repositories**.</span></span>

    <span data-ttu-id="4334e-113">[![oppdatere-er-fra-lcs-for-ms-åpen-ms-repositorier-liste](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)</span><span class="sxs-lookup"><span data-stu-id="4334e-113">[![update-er-from-lcs-for-ms-open-ms-repositories-list](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)</span></span>

5. <span data-ttu-id="4334e-114">På **Konfigurasjonsrepositorier**-siden i rutenettet velger du det eksisterende repositoriet for **LCS**-typen.</span><span class="sxs-lookup"><span data-stu-id="4334e-114">On the **Configuration repositories** page, in the grid, select the existing repository of the **LCS** type.</span></span> <span data-ttu-id="4334e-115">Hvis dette repositoriet ikke vises i rutenettet, gjør du følgende:</span><span class="sxs-lookup"><span data-stu-id="4334e-115">If this repository doesn't appear in the grid, follow these steps:</span></span>

    1. <span data-ttu-id="4334e-116">Klikk **Legg til** for å legge til et nytt repositorium.</span><span class="sxs-lookup"><span data-stu-id="4334e-116">Click **Add** to add a new repository.</span></span>
    2. <span data-ttu-id="4334e-117">Velg **LCS** som type repositorium.</span><span class="sxs-lookup"><span data-stu-id="4334e-117">Select **LCS** as the repository type.</span></span>
    3. <span data-ttu-id="4334e-118">Klikk **Opprett repositorium**.</span><span class="sxs-lookup"><span data-stu-id="4334e-118">Click **Create repository**.</span></span>
    4. <span data-ttu-id="4334e-119">Hvis du blir bedt om det, følger du autorisasjonsinstruksjonene.</span><span class="sxs-lookup"><span data-stu-id="4334e-119">If prompted, follow the authorization instructions.</span></span>
    5. <span data-ttu-id="4334e-120">Angi et navn og en beskrivelse for repositoriet.</span><span class="sxs-lookup"><span data-stu-id="4334e-120">Enter a name and description for the repository.</span></span>
    6. <span data-ttu-id="4334e-121">Klikk **OK** for å bekrefte den nye repositoriumoppføringen.</span><span class="sxs-lookup"><span data-stu-id="4334e-121">Click **OK** to confirm the new repository entry.</span></span>
    7. <span data-ttu-id="4334e-122">I rutenettet velger du det nye repositoriet i **LCS**-typen.</span><span class="sxs-lookup"><span data-stu-id="4334e-122">In the grid, select the new repository of the **LCS** type.</span></span>

6. <span data-ttu-id="4334e-123">Klikk **Åpne** for å vise listen over ER-konfigurasjoner for det valgte repositoriet.</span><span class="sxs-lookup"><span data-stu-id="4334e-123">Click **Open** to view the list of ER configurations for the selected repository.</span></span>

    <span data-ttu-id="4334e-124">[![Oppdatere-er-fra-LCS-for-MS-merke-LCS-repositorium](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)</span><span class="sxs-lookup"><span data-stu-id="4334e-124">[![update-er-from-lcs-for-ms-make-lcs-repository](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)</span></span>

7. <span data-ttu-id="4334e-125">Velg ER-konfigurasjonen du må ha, i konfigurasjonstreet i den venstre ruten.</span><span class="sxs-lookup"><span data-stu-id="4334e-125">In the configurations tree in the left pane, select the ER configuration that you require.</span></span>
8. <span data-ttu-id="4334e-126">I **Versjoner**-hurtigkategorien velger du den nødvendige versjonen av den valgte ER-konfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="4334e-126">On the **Versions** FastTab, select the required version of the selected ER configuration.</span></span>
9. <span data-ttu-id="4334e-127">Klikk **Importer** for å laste ned den valgte versjonen fra LCS til den gjeldende forekomsten av Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="4334e-127">Click **Import** to download the selected version from LCS to the current Finance and Operations instance.</span></span>

    > [!NOTE]
    > <span data-ttu-id="4334e-128">**Importer**-knappen er ikke tilgjengelig for ER-konfigurasjonsversjoner som allerede finnes i den gjeldende forekomsten av Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="4334e-128">The **Import** button is unavailable for ER configuration versions that are already present in the current Finance and Operations instance.</span></span>

    <span data-ttu-id="4334e-129">[![oppdatere-er-fra-lcs-for-ms-nedlasting-konfigurasjon](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)</span><span class="sxs-lookup"><span data-stu-id="4334e-129">[![update-er-from-lcs-for-ms-download-configuration](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)</span></span>

> [!NOTE]
> <span data-ttu-id="4334e-130">Avhengig av ER-innstillingene valideres konfigurasjonene når de er importert.</span><span class="sxs-lookup"><span data-stu-id="4334e-130">Depending on the ER settings, configurations are validated after they are imported.</span></span> <span data-ttu-id="4334e-131">Du kan få beskjed om eventuelle problemer som oppdages.</span><span class="sxs-lookup"><span data-stu-id="4334e-131">You might be notified about any inconsistency issues that are discovered.</span></span> <span data-ttu-id="4334e-132">Du må løse disse problemene før du kan bruke den importerte konfigurasjonsversjonen.</span><span class="sxs-lookup"><span data-stu-id="4334e-132">You must resolve those issues before you can use the imported configuration version.</span></span> <span data-ttu-id="4334e-133">Hvis du vil ha mer informasjon, se listen over relaterte artikler for dette emnet.</span><span class="sxs-lookup"><span data-stu-id="4334e-133">For more information, see the list of related articles for this topic.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4334e-134">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="4334e-134">Additional resources</span></span>

[<span data-ttu-id="4334e-135">Oversikt over elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="4334e-135">Electronic reporting overview</span></span>](general-electronic-reporting.md)
