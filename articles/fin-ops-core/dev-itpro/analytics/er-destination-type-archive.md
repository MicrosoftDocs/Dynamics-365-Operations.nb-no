---
title: Arkivere ER-måltype
description: Dette emnet inneholder informasjon om hvordan du konfigurerer et arkivmål for hver MAPPE- eller FIL-komponent i et elektronisk rapporteringsformat (ER) som er konfigurert til å generere utgående dokumenter.
author: NickSelin
manager: AnnBe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 15611a4f0000ca5ccb0ac3f4012251d5bf5689ec
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019928"
---
# <span data-ttu-id="4f41a-103"><a name="ArchiveDestinationType">Arkivmål</a></span><span class="sxs-lookup"><span data-stu-id="4f41a-103"><a name="ArchiveDestinationType">Archive destination</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4f41a-104">Du kan konfigurere et arkivmål for hver MAPPE- eller FIL-komponent i et elektronisk rapporteringsformat (ER) som er konfigurert til å generere utgående dokumenter.</span><span class="sxs-lookup"><span data-stu-id="4f41a-104">You can configure an archive destination for each FOLDER or FILE component of an Electronic reporting (ER) format that is configured to generate outbound documents.</span></span> <span data-ttu-id="4f41a-105">Basert på målinnstillingen lagres et generert dokument som et vedlegg til en oppføring i ER-jobblisten.</span><span class="sxs-lookup"><span data-stu-id="4f41a-105">Based on the destination setting, a generated document is stored as an attachment of a record of the ER jobs list.</span></span>

<span data-ttu-id="4f41a-106">Du kan bruke dette alternativet for å sende det genererte dokumentet til en Microsoft SharePoint-mappe eller Microsoft Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="4f41a-106">You can use this option to send the generated document to a Microsoft SharePoint folder or Microsoft Azure Storage.</span></span> <span data-ttu-id="4f41a-107">Sett **Aktivert** til **Ja** for å sende utdata til et mål som er definert av den valgte dokumenttypen.</span><span class="sxs-lookup"><span data-stu-id="4f41a-107">Set **Enabled** to **Yes** to send output to a destination that is defined by the selected document type.</span></span> <span data-ttu-id="4f41a-108">Bare dokumenttyper der gruppen er satt til **Fil** er tilgjengelige for valg.</span><span class="sxs-lookup"><span data-stu-id="4f41a-108">Only document types where the group is set to **File** are available for selection.</span></span> <span data-ttu-id="4f41a-109">Du definerer dokumentets [typer](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) under **Organisasjonsstyring** \> **Dokumentadministrering** \> **Dokumenttyper**.</span><span class="sxs-lookup"><span data-stu-id="4f41a-109">You define document [types](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) at **Organization administration** \> **Document management** \> **Document types**.</span></span> <span data-ttu-id="4f41a-110">Konfigurasjonen for ER-mål er den samme som konfigurasjonen for systemet for dokumentbehandling.</span><span class="sxs-lookup"><span data-stu-id="4f41a-110">The configuration for ER destinations is the same as the configuration for the document management system.</span></span>

<span data-ttu-id="4f41a-111">[![Siden Dokumenttyper](./media/ER_Destinations-SharePointDocuType.png)](./media/ER_Destinations-SharePointDocuType.png)</span><span class="sxs-lookup"><span data-stu-id="4f41a-111">[![Document types page](./media/ER_Destinations-SharePointDocuType.png)](./media/ER_Destinations-SharePointDocuType.png)</span></span>

<span data-ttu-id="4f41a-112">Plasseringen bestemmer hvor filen lagres.</span><span class="sxs-lookup"><span data-stu-id="4f41a-112">The location determines where the file is saved.</span></span> <span data-ttu-id="4f41a-113">Etter at **Arkiv**-målet er aktivert, kan resultatene lagres i jobbarkivet.</span><span class="sxs-lookup"><span data-stu-id="4f41a-113">After the **Archive** destination is enabled, the results can be saved in the Job archive.</span></span> <span data-ttu-id="4f41a-114">Du kan vise resultatene på **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Arkiverte jobber for elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="4f41a-114">You can view the results at **Organization administration** \> **Electronic reporting** \> **Electronic reporting archived jobs**.</span></span>

> [!NOTE]
> <span data-ttu-id="4f41a-115">Velg en dokumenttype for jobbarkivet ved å navigere til **Organisasjonsstyring** \> **Arbeidsområder** \> **Elektronisk rapportering** \> **Parametere for elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="4f41a-115">Select a document type for the Job archive by navigating to **Organization administration** \> **Workspaces** \> **Electronic reporting** \> **Electronic reporting parameters**.</span></span> <span data-ttu-id="4f41a-116">Hvis du vil ha mer informasjon, kan du se [Konfigurere rammeverket for elektronisk rapportering (ER)](electronic-reporting-er-configure-parameters.md#prerequisites-for-er-setup).</span><span class="sxs-lookup"><span data-stu-id="4f41a-116">For more information, [Configure the Electronic reporting (ER) framework](electronic-reporting-er-configure-parameters.md#prerequisites-for-er-setup).</span></span>

## <a name="sharepoint"></a><span data-ttu-id="4f41a-117">SharePoint</span><span class="sxs-lookup"><span data-stu-id="4f41a-117">SharePoint</span></span>

<span data-ttu-id="4f41a-118">Du kan lagre en fil i en bestemt SharePoint-mappe.</span><span class="sxs-lookup"><span data-stu-id="4f41a-118">You can save a file in a designated SharePoint folder.</span></span> <span data-ttu-id="4f41a-119">Hvis du vil definere standard SharePoint-server, går du til **Organisasjonsstyring** \> **Dokumentadministrering** \> **Parametere for dokumentadministrering**.</span><span class="sxs-lookup"><span data-stu-id="4f41a-119">To define the default SharePoint server, go to **Organization administration** \> **Document management** \> **Document management parameters**.</span></span> <span data-ttu-id="4f41a-120">I **SharePoint**-fanen konfigurerer du SharePoint-mappen.</span><span class="sxs-lookup"><span data-stu-id="4f41a-120">On the **SharePoint** tab, configure the SharePoint folder.</span></span> <span data-ttu-id="4f41a-121">Deretter kan du velge den som mappen der ER-utdataene skal lagres.</span><span class="sxs-lookup"><span data-stu-id="4f41a-121">Then, you can select it as the folder where the ER output will be saved.</span></span> <span data-ttu-id="4f41a-122">**SharePoint**-plasseringen må velges i denne dokumenttypen.</span><span class="sxs-lookup"><span data-stu-id="4f41a-122">The **SharePoint** location must be selected in this document type.</span></span>

<span data-ttu-id="4f41a-123">[![Velge en SharePoint-mappe](./media/ER_Destinations-SharePointDocuTypeLocation.png)](./media/ER_Destinations-SharePointDocuTypeLocation.png)</span><span class="sxs-lookup"><span data-stu-id="4f41a-123">[![Selecting a SharePoint folder](./media/ER_Destinations-SharePointDocuTypeLocation.png)](./media/ER_Destinations-SharePointDocuTypeLocation.png)</span></span>

## <a name="azure-storage"></a><span data-ttu-id="4f41a-124">Azure Storage</span><span class="sxs-lookup"><span data-stu-id="4f41a-124">Azure Storage</span></span>

<span data-ttu-id="4f41a-125">Når type dokumentplasseringen er satt til **Azure Storage**, kan du lagre en fil i Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="4f41a-125">When the document type location is set to **Azure storage**, you can save a file to Azure Storage.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4f41a-126">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="4f41a-126">Additional resources</span></span>

- [<span data-ttu-id="4f41a-127">Oversikt over elektronisk rapportering (ER)</span><span class="sxs-lookup"><span data-stu-id="4f41a-127">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="4f41a-128">Mål for elektronisk rapportering (ER)</span><span class="sxs-lookup"><span data-stu-id="4f41a-128">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)
- [<span data-ttu-id="4f41a-129">Konfigurere dokumentstyring</span><span class="sxs-lookup"><span data-stu-id="4f41a-129">Configure document management</span></span>](../../fin-ops/organization-administration/configure-document-management.md)
