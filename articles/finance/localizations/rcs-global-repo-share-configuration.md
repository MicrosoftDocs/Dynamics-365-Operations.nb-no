---
title: Dele ER-konfigurasjoner i RCS/det globale repositoriet med eksterne organisasjoner
description: Dette emnet forklarer hvordan du deler konfigurasjoner for elektronisk rapportering (ER) i Microsoft RCS (Regulatory Configuration Services) eller det globale repositoriet direkte med eksterne organisasjoner.
author: JaneA07
manager: AnnBe
ms.date: 05/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace, RCS
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: e7ec24ddc532ee3b87108d076d5103538be903be
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5218836"
---
# <a name="share-electronic-reporting-er-configurations-in-regulatory-configuration-services-rcs-global-repository-with-external-organizations"></a><span data-ttu-id="a96c0-103">Dele konfigurasjoner for elektronisk rapportering (ER) i RCS(Regulatory Configuration Services) eller det globale repositoriet med eksterne organisasjoner</span><span class="sxs-lookup"><span data-stu-id="a96c0-103">Share Electronic reporting (ER) configurations in Regulatory Configuration Services (RCS) Global repository with external organizations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a96c0-104">Du kan bruke Microsoft Regulatory Configuration Services (RCS) til å dele konfigurasjoner for elektronisk rapportering (ER) og deretter publisere dem til eksterne organisasjoner.</span><span class="sxs-lookup"><span data-stu-id="a96c0-104">You can use Microsoft Regulatory Configuration Services (RCS) to share Electronic reporting (ER) configurations and then publish them to external organizations.</span></span>

<span data-ttu-id="a96c0-105">Følgende fremgangsmåter forklarer hvordan en RCS-bruker kan dele en versjon av en ER-konfigurasjon som er konfigurert i en RCS-forekomst, med en ekstern organisasjon.</span><span class="sxs-lookup"><span data-stu-id="a96c0-105">The following procedures explain how an RCS user can share a version of an ER configuration that has been configured in an RCS instance with an external organization.</span></span> <span data-ttu-id="a96c0-106">Før du kan fullføre de prosedyrene, må du gjøre følgende:</span><span class="sxs-lookup"><span data-stu-id="a96c0-106">Before you can complete those procedures, you must complete the following prerequisites:</span></span>

- <span data-ttu-id="a96c0-107">Åpne en RCS-forekomst.</span><span class="sxs-lookup"><span data-stu-id="a96c0-107">Access an RCS instance.</span></span>
- <span data-ttu-id="a96c0-108">Opprette en aktiv konfigurasjonsleverandør.</span><span class="sxs-lookup"><span data-stu-id="a96c0-108">Create an active configuration provider.</span></span> <span data-ttu-id="a96c0-109">Hvis du ha mer informasjon, kan du se [Opprette konfigurasjonsleverandører og merke dem som aktive](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="a96c0-109">For more information, see [Create configuration providers and mark them as active](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>
- <span data-ttu-id="a96c0-110">Opprett og last opp en ny versjon av en ER-konfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="a96c0-110">Create and upload a new version of an ER configuration.</span></span> <span data-ttu-id="a96c0-111">Hvis du vil ha mer informasjon, kan du se [Opprette og laste opp en ny versjon av en konfigurasjon for elektronisk rapportering (ER)](rcs-global-repo-upload.md).</span><span class="sxs-lookup"><span data-stu-id="a96c0-111">For more information, see [Create and upload a new version of an Electronic reporting (ER) configuration](rcs-global-repo-upload.md).</span></span>

<span data-ttu-id="a96c0-112">Du må også kontrollere at det er klargjort et RCS-miljø for firmaet ditt.</span><span class="sxs-lookup"><span data-stu-id="a96c0-112">You must also make sure that an RCS environment is provisioned for your company.</span></span>

1. <span data-ttu-id="a96c0-113">I en Finance and Operations-app går du til **Organisasjonsstyring** \> **Arbeidsområder** \> **Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="a96c0-113">In a Finance and Operations app, go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="a96c0-114">Hvis et RCS-miljø ikke er klargjort for firmaet ditt, velger du **Regulatory Services – Ekstern konfigurasjon**, og deretter følger du instruksjonene for å klargjøre en.</span><span class="sxs-lookup"><span data-stu-id="a96c0-114">If no RCS environment is provisioned for your company, select **Regulatory services – Configuration external**, and then follow the instructions to provision one.</span></span>

<span data-ttu-id="a96c0-115">Hvis et RCS-miljø allerede er klargjort for ditt firma, bruker du URL-adressen for siden til å få tilgang til den ved å velge alternativet for pålogging.</span><span class="sxs-lookup"><span data-stu-id="a96c0-115">If an RCS environment has been already provisioned for your company, use the page URL to access it by selecting the sign-in option.</span></span>

## <a name="verify-the-configuration-that-you-want-to-share"></a><span data-ttu-id="a96c0-116">Kontrollere konfigurasjonen du vil dele</span><span class="sxs-lookup"><span data-stu-id="a96c0-116">Verify the configuration that you want to share</span></span>

<span data-ttu-id="a96c0-117">Følg denne fremgangsmåten for å kontrollere at konfigurasjonen du vil dele, allerede er lastet opp til det globale repositoriet.</span><span class="sxs-lookup"><span data-stu-id="a96c0-117">Follow these steps to verify that the configuration that you want to share has already been uploaded to the Global repository.</span></span>

1. <span data-ttu-id="a96c0-118">I arbeidsområdet **Elektronisk rapportering** velger du **Repositorier** for konfigurasjonsleverandøren.</span><span class="sxs-lookup"><span data-stu-id="a96c0-118">In the **Electronic reporting** workspace, select **Repositories** for your configuration provider.</span></span>

    ![Konfigurasjonsleverandører](media/1_RCS_Repo_for_config_provider.JPG)

2. <span data-ttu-id="a96c0-120">Velg **Globalt repositorium** \> **Åpne**.</span><span class="sxs-lookup"><span data-stu-id="a96c0-120">Select **Global repository** \> **Open**.</span></span>
3. <span data-ttu-id="a96c0-121">Søk etter konfigurasjonen du vil dele.</span><span class="sxs-lookup"><span data-stu-id="a96c0-121">Search for the configuration that you want to share.</span></span> <span data-ttu-id="a96c0-122">Du kan bruke filtreringsfeltet til å begrense søket.</span><span class="sxs-lookup"><span data-stu-id="a96c0-122">You can use the filter field to narrow your search.</span></span> <span data-ttu-id="a96c0-123">Hvis du ikke finner konfigurasjonen i det globale repositoriet, følger du fremgangsmåten under [Opprette og laste opp en ny versjon av en konfigurasjon for elektronisk rapportering (ER)](rcs-global-repo-upload.md).</span><span class="sxs-lookup"><span data-stu-id="a96c0-123">If you can't find the configuration in the Global repository, follow the steps in [Create and upload a new version of an Electronic reporting (ER) configuration](rcs-global-repo-upload.md).</span></span>

## <a name="share-er-configurations-with-external-organizations"></a><span data-ttu-id="a96c0-124">Dele ER-konfigurasjoner med eksterne organisasjoner</span><span class="sxs-lookup"><span data-stu-id="a96c0-124">Share ER configurations with external organizations</span></span>

<span data-ttu-id="a96c0-125">Når en konfigurasjon er opprettet under konfigurasjonsleverandøren, kan du dele den direkte med eksterne organisasjoner ved hjelp av hurtigkategorien **Delt med** på siden **Globalt konfigurasjonsrepositorium**.</span><span class="sxs-lookup"><span data-stu-id="a96c0-125">After a configuration has been created under your configuration provider, you can share it directly with external organizations by using the **Shared with** FastTab on the **Global configuration repository** page.</span></span>

1. <span data-ttu-id="a96c0-126">I arbeidsområdet **Elektronisk rapportering** velger du **Repositorier** for konfigurasjonsleverandøren.</span><span class="sxs-lookup"><span data-stu-id="a96c0-126">In the **Electronic reporting** workspace, select **Repositories** for your configuration provider.</span></span>
2. <span data-ttu-id="a96c0-127">Velg **Globalt repositorium** \> **Åpne**.</span><span class="sxs-lookup"><span data-stu-id="a96c0-127">Select **Global repository** \> **Open**.</span></span> 
3. <span data-ttu-id="a96c0-128">Velg konfigurasjonen du vil dele.</span><span class="sxs-lookup"><span data-stu-id="a96c0-128">Select the configuration that you want to share.</span></span>
4. <span data-ttu-id="a96c0-129">I hurtigkategorien **Delt med** velger du **Organisasjon**.</span><span class="sxs-lookup"><span data-stu-id="a96c0-129">On the **Shared with** FastTab, select **Organization**.</span></span>

    ![Delt med hurtigkategori](media/1_RCS_Repo_for_Share_with_org.JPG)

5. <span data-ttu-id="a96c0-131">I dialogboksen angir du domenenavnet for den eksterne organisasjonen, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="a96c0-131">In the dialog box, enter the domain name for the external organization, and then select **OK**.</span></span>

    ![Dele konfigurasjonsversjon med dialogboksen Ekstern organisasjon](media/1_RCS_Repo_for_Share_with_form.JPG)

<span data-ttu-id="a96c0-133">Konfigurasjonen deles med den eksterne organisasjonen, og er tilgjengelig for den organisasjonen i det globale repositoriet.</span><span class="sxs-lookup"><span data-stu-id="a96c0-133">The configuration is shared with the external organization and is available to that organization in the Global repository.</span></span> <span data-ttu-id="a96c0-134">Derfra kan den importeres til organisasjonens forekomst av RCS eller i forekomstene av Finance and Operations-apper.</span><span class="sxs-lookup"><span data-stu-id="a96c0-134">From there, it can be imported into the organization's instance of RCS or into its instances of Finance and Operations apps.</span></span>

6. <span data-ttu-id="a96c0-135">Hvis du vil oppheve deling av en konfigurasjon som tidligere er delt med en ekstern organisasjon, velger du konfigurasjonen og klikker **Opphev deling**, og deretter velger du **OK**</span><span class="sxs-lookup"><span data-stu-id="a96c0-135">To unshare a configuration that has been previously shared with an external organization, select the configuration and click **Unshare**, and then select **OK**</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]