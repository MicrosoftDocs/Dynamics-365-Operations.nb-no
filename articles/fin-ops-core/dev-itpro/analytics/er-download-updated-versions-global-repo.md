---
title: Importere oppdaterte versjoner av ER-konfigurasjoner
description: Dette emnet forklarer hvordan du importerer oppdaterte versjoner av elektroniske rapporteringskonfigurasjoner (ER) fra det globale repositoriet for konfigurasjonstjenesten.
author: NickSelin
manager: AnnBe
ms.date: 06/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionImport, ERWorkspace, ERSolutionRepositoryTable
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 4f167a0209713b5bca0cefe0135abd46a149a515
ms.sourcegitcommit: 1e6a7b50596eaf9d965e0155f3f2c50f7f50747e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/22/2020
ms.locfileid: "3498108"
---
# <a name="import-updated-versions-of-er-configurations"></a><span data-ttu-id="45398-103">Importere oppdaterte versjoner av ER-konfigurasjoner</span><span class="sxs-lookup"><span data-stu-id="45398-103">Import updated versions of ER configurations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="45398-104">[Repositorier](general-electronic-reporting.md#Repository) for elektronisk rapportering (ER) brukes til å dele [ER-konfigurasjoner](general-electronic-reporting.md#Configuration).</span><span class="sxs-lookup"><span data-stu-id="45398-104">Electronic reporting (ER) [repositories](general-electronic-reporting.md#Repository) are used to share [ER configurations](general-electronic-reporting.md#Configuration).</span></span> <span data-ttu-id="45398-105">Du kan [importere](download-electronic-reporting-configuration-lcs.md) ER-konfigurasjonene fra forskjellige repositorier til din forekomst av Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="45398-105">You can [import](download-electronic-reporting-configuration-lcs.md) ER configurations from different repositories into your instance of Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="45398-106">Når du importerer ER-konfigurasjoner, [kan konfigurasjonsleverandører](general-electronic-reporting.md#Provider) publisere nye [versjoner](general-electronic-reporting.md#component-versioning) av repositorier, slik at de kan deles.</span><span class="sxs-lookup"><span data-stu-id="45398-106">When you import ER configurations, [configuration providers](general-electronic-reporting.md#Provider) can publish new [versions](general-electronic-reporting.md#component-versioning) repositories so that they can be shared.</span></span>

<span data-ttu-id="45398-107">Dette emnet forklarer hvordan du importerer oppdaterte versjoner av ER-konfigurasjoner fra det globale repositoriet for konfigurasjonstjenesten.</span><span class="sxs-lookup"><span data-stu-id="45398-107">This topic explains how to import updated versions of ER configurations from the Global repository of the Configuration service.</span></span> <span data-ttu-id="45398-108">Hvis du vil ha mer informasjon, kan du se [Microsoft Dynamics 365 for Finance and Operations – Regulatory Services, konfigurasjonstjeneste](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration).</span><span class="sxs-lookup"><span data-stu-id="45398-108">For more information, see [Microsoft Dynamics 365 for Finance and Operations - Regulatory Services, Configuration service](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration).</span></span>

## <a name="review-the-available-updated-versions"></a><span data-ttu-id="45398-109">Se gjennom tilgjengelige oppdaterte versjoner</span><span class="sxs-lookup"><span data-stu-id="45398-109">Review the available updated versions</span></span>

1. <span data-ttu-id="45398-110">Logg på Finance med én av følgende roller:</span><span class="sxs-lookup"><span data-stu-id="45398-110">Sign in to Finance by using one of the following roles:</span></span>

    - <span data-ttu-id="45398-111">Utvikler av elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="45398-111">Electronic reporting developer</span></span>
    - <span data-ttu-id="45398-112">Funksjonell konsulent for elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="45398-112">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="45398-113">Systemansvarlig</span><span class="sxs-lookup"><span data-stu-id="45398-113">System administrator</span></span>

2. <span data-ttu-id="45398-114">Gå til **Organisasjonsstyring** \> **Arbeidsområder** \> **Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="45398-114">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="45398-115">På siden **Lokaliseringskonfigurasjoner**, i delen **Relaterte koblinger**, velger du flisen **Importer versjonsoppdateringer av konfigurasjoner**.</span><span class="sxs-lookup"><span data-stu-id="45398-115">On the **Localization configurations** page, in the **Related links** section, select **Import configurations versions updates**.</span></span>

    ![Side for lokaliseringskonfigurasjoner](./media/er-download-updated-versions-global-repo1.png)

4. <span data-ttu-id="45398-117">I dialogboksen **Importer versjonsoppdateringer for elektroniske rapporteringskonfigurasjoner**, i **Kjøremodus**-feltet, velger du **Vis bare tilgjengelige oppdateringer**.</span><span class="sxs-lookup"><span data-stu-id="45398-117">In the **Import electronic reporting configurations versions updates** dialog box, in the **Run mode** field, select **Only show available updates**.</span></span> <span data-ttu-id="45398-118">Velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="45398-118">Then select **OK**.</span></span> 

    ![Kjøremodus-feltet satt til Bare vis tilgjengelige oppdateringer](./media/er-download-updated-versions-global-repo2.png)

5. <span data-ttu-id="45398-120">Se gjennom meldingene du mottar.</span><span class="sxs-lookup"><span data-stu-id="45398-120">Review the messages that you receive.</span></span> <span data-ttu-id="45398-121">Disse meldingene inneholder følgende informasjon om ER-konfigurasjonene i gjeldende Finance-forekomst, og hvordan de sammenlignes med innholdet i det globale repositoriet:</span><span class="sxs-lookup"><span data-stu-id="45398-121">These messages provide the following information about the ER configurations in the current Finance instance and how they compare to the content of the Global repository:</span></span>

    - <span data-ttu-id="45398-122">Totalt antall ER-konfigurasjoner</span><span class="sxs-lookup"><span data-stu-id="45398-122">The total number of ER configurations</span></span>
    - <span data-ttu-id="45398-123">ER-konfigurasjoner som ikke finnes i det globale repositoriet</span><span class="sxs-lookup"><span data-stu-id="45398-123">ER configurations that aren't present in the Global repository</span></span>
    - <span data-ttu-id="45398-124">ER-konfigurasjoner der den nyeste versjonen allerede er tilgjengelig i gjeldende Finance-forekomst. (Hvis du vil vise hele listen over disse ER-konfigurasjonene, velger du **Meldingsdetaljer**-koblingen.)</span><span class="sxs-lookup"><span data-stu-id="45398-124">ER configurations for which the latest version is already available in the current Finance instance (To view the full list of these ER configurations, select the **Message details** link.)</span></span>

        ![Meldingen «Nyeste versjoner av følgende konfigurasjoner er allerede importert» og meldingsdetaljer](./media/er-download-updated-versions-global-repo3.png)

    - <span data-ttu-id="45398-126">ER-konfigurasjoner der den nyeste versjonen er tilgjengelig i det globale repositoriet og kan importeres til gjeldende Finance-forekomst. (Hvis du vil vise hele listen over disse ER-konfigurasjonene, velger du **Meldingsdetaljer**-koblingen.)</span><span class="sxs-lookup"><span data-stu-id="45398-126">ER configurations for which the latest version is available in the Global repository and can be imported into the current Finance instance (To view the full list of these ER configurations, select the **Message details** link.)</span></span>

        ![Meldingen «Tilgjengelige oppdateringer» og meldingsdetaljer](./media/er-download-updated-versions-global-repo4.png)

## <a name="import-available-updated-versions"></a><span data-ttu-id="45398-128">Importer tilgjengelige oppdaterte versjoner</span><span class="sxs-lookup"><span data-stu-id="45398-128">Import available updated versions</span></span>

1. <span data-ttu-id="45398-129">Logg på Finance med én av følgende roller:</span><span class="sxs-lookup"><span data-stu-id="45398-129">Sign in to Finance by using one of the following roles:</span></span>

    - <span data-ttu-id="45398-130">Utvikler av elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="45398-130">Electronic reporting developer</span></span>
    - <span data-ttu-id="45398-131">Funksjonell konsulent for elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="45398-131">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="45398-132">Systemansvarlig</span><span class="sxs-lookup"><span data-stu-id="45398-132">System administrator</span></span>

2. <span data-ttu-id="45398-133">Gå til **Organisasjonsstyring** \> **Arbeidsområder** \> **Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="45398-133">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="45398-134">På siden **Lokaliseringskonfigurasjoner**, i delen **Relaterte koblinger**, velger du flisen **Importer versjonsoppdateringer av konfigurasjoner**.</span><span class="sxs-lookup"><span data-stu-id="45398-134">On the **Localization configurations** page, in the **Related links** section, select **Import configurations versions updates**.</span></span>
4. <span data-ttu-id="45398-135">I dialogboksen **Importer versjonsoppdateringer for elektroniske rapporteringskonfigurasjoner**, i **Kjøremodus**-feltet velger du **Importer nyeste oppdateringer** for å importere de nyeste versjonene av ER-konfigurasjoner fra det globale repositoriet til gjeldende Finance-forekomst.</span><span class="sxs-lookup"><span data-stu-id="45398-135">In the **Import electronic reporting configurations versions updates** dialog box, in the **Run mode** field, select **Import latest updates** to import the latest versions of ER configurations from the Global repository into the current Finance instance.</span></span>
5. <span data-ttu-id="45398-136">Hvis du vil planlegge en satsvis jobb for importen, angir du **Satsvis behandling**-alternativet til **Ja** i **Kjør i bakgrunnen**-hurtigfanen.</span><span class="sxs-lookup"><span data-stu-id="45398-136">To schedule a batch job for the import, on the **Run in the background** FastTab, set the **Batch processing** option to **Yes**.</span></span> <span data-ttu-id="45398-137">Hvis du vil gjenta importen regelmessig, kan du konfigurere den nødvendige gjentakelsen.</span><span class="sxs-lookup"><span data-stu-id="45398-137">If you want to repeat the import periodically, configure the required recurrence.</span></span>

    ![Kjøre modus-feltet satt til Importer nyeste oppdateringer](./media/er-download-updated-versions-global-repo5.png)

6. <span data-ttu-id="45398-139">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="45398-139">Select **OK**.</span></span>
7. <span data-ttu-id="45398-140">Følg ett av disse trinnene for å finne ut hvilke konfigurasjonsversjoner som er importert:</span><span class="sxs-lookup"><span data-stu-id="45398-140">To learn what configuration versions have been imported, follow one of these steps:</span></span>

    - <span data-ttu-id="45398-141">Hvis du kjører importen interaktivt i stedet for å bruke en satsvis jobb, kan du se gjennom meldingene du mottar.</span><span class="sxs-lookup"><span data-stu-id="45398-141">If you run the import interactively instead of using a batch job, review the messages that you receive.</span></span>

        ![Meldinger mottatt under en interaktiv importkjøring](./media/er-download-updated-versions-global-repo6.png)

    - <span data-ttu-id="45398-143">Hvis du kjører importen i satsvis modus, følger du denne fremgangsmåten:</span><span class="sxs-lookup"><span data-stu-id="45398-143">If you run the import in batch mode, follow these steps:</span></span>

        1. <span data-ttu-id="45398-144">Gå til **Felles** \> **Forespørsler** \> **Satsvise jobber** \> **Mine satsvise jobber**.</span><span class="sxs-lookup"><span data-stu-id="45398-144">Go to **Common** \> **Inquiries** \> **Batch jobs** \> **My batch jobs**.</span></span>
        2. <span data-ttu-id="45398-145">Finn og velg jobben **Importer versjonsoppdateringer for elektroniske rapporteringskonfigurasjoner**, og velg **Logg over satsvis jobb** i handlingsruten i **Satsvis jobb**-fanen for å vise jobbloggen.</span><span class="sxs-lookup"><span data-stu-id="45398-145">Find and select the **Import electronic reporting configurations versions updates** job, and then, on the Action Pane, on the **Batch job** tab, select **Batch job history** to view the job history.</span></span>
        3. <span data-ttu-id="45398-146">På **Logg for satsvis jobb**-siden velger du **Logg**.</span><span class="sxs-lookup"><span data-stu-id="45398-146">On the **Batch job history** page, select **Log**.</span></span> <span data-ttu-id="45398-147">Velg **Meldingsdetaljer**-koblingen i meldingen du mottar, for å vise jobbloggen.</span><span class="sxs-lookup"><span data-stu-id="45398-147">Then, in the message that you receive, select the **Message details** link to view the job log.</span></span>

        ![Jobblogg](./media/er-download-updated-versions-global-repo7.png)

> [!IMPORTANT]
> <span data-ttu-id="45398-149">Vi anbefaler ikke at du planlegger en regelmessig satsvis jobb for å importere oppdaterte versjoner av ER-konfigurasjoner direkte fra det globale repositoriet til et produksjonsmiljø, fordi de importerte versjonene umiddelbart vil være tilgjengelige for bruk.</span><span class="sxs-lookup"><span data-stu-id="45398-149">We don't recommend that you schedule a recurring batch job to import updated versions of ER configurations directly from the Global repository into a production environment, because the imported versions will immediately be available for use.</span></span> <span data-ttu-id="45398-150">Bruk i stedet denne fremgangsmåten til å distribuere versjoner av ER-konfigurasjoner til et sandkassemiljø.</span><span class="sxs-lookup"><span data-stu-id="45398-150">Instead, use this approach to deploy versions of ER configurations to a sandbox environment.</span></span> <span data-ttu-id="45398-151">De kan evalueres i sandkassemiljøet før de distribueres til et produksjonsmiljø.</span><span class="sxs-lookup"><span data-stu-id="45398-151">They can then be evaluated in the sandbox environment before they are deployed to a production environment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="45398-152">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="45398-152">Additional resources</span></span>

- [<span data-ttu-id="45398-153">Oversikt over elektronisk rapportering (ER)</span><span class="sxs-lookup"><span data-stu-id="45398-153">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="45398-154">Last ned ER-konfigurasjoner fra det globale repositoriet for konfigurasjonstjenesten</span><span class="sxs-lookup"><span data-stu-id="45398-154">Download ER configurations from the Global repository of Configuration service</span></span>](er-download-configurations-global-repo.md)
