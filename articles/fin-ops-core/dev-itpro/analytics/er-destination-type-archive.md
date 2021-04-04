---
title: Arkivere ER-måltype
description: Dette emnet inneholder informasjon om hvordan du konfigurerer et arkivmål for hver MAPPE- eller FIL-komponent i et ER-format (Elektronisk rapportering).
author: NickSelin
manager: AnnBe
ms.date: 11/30/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 72b896ca692a54200ff79b14d0b5dc6ab4b0fe27
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562052"
---
# <a name="archive-er-destination-type"></a><span data-ttu-id="b7b5f-103">Arkivere ER-måltype</span><span class="sxs-lookup"><span data-stu-id="b7b5f-103">Archive ER destination type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b7b5f-104">Du kan konfigurere et arkivmål for hver **Mappe**- eller **Fil**-komponent i et elektronisk rapporteringsformat (ER) som er konfigurert til å generere utgående dokumenter.</span><span class="sxs-lookup"><span data-stu-id="b7b5f-104">You can configure an archive destination for each **Folder** or **File** component of an Electronic reporting (ER) format that is configured to generate outbound documents.</span></span> <span data-ttu-id="b7b5f-105">Basert på målinnstillingen lagres et generert dokument som et vedlegg til en oppføring i ER-jobblisten.</span><span class="sxs-lookup"><span data-stu-id="b7b5f-105">Based on the destination setting, a generated document is stored as an attachment of a record of the ER jobs list.</span></span> <span data-ttu-id="b7b5f-106">Hvis du vil vise resultatene, går du til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Arkiverte jobber for elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="b7b5f-106">To view the results, go to **Organization administration** \> **Electronic reporting** \> **Electronic reporting jobs**.</span></span>

<span data-ttu-id="b7b5f-107">Du kan bruke dette alternativet for å sende det genererte dokumentet til en Microsoft SharePoint-mappe eller Microsoft Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="b7b5f-107">You can use this option to send the generated document to a Microsoft SharePoint folder or Microsoft Azure Storage.</span></span> <span data-ttu-id="b7b5f-108">Sett **Aktivert** til **Ja** for å sende utdata til et mål som er definert av den valgte dokumenttypen.</span><span class="sxs-lookup"><span data-stu-id="b7b5f-108">Set **Enabled** to **Yes** to send output to a destination that is defined by the selected document type.</span></span> <span data-ttu-id="b7b5f-109">Bare dokumenttyper der gruppen er satt til **Fil** er tilgjengelige for valg.</span><span class="sxs-lookup"><span data-stu-id="b7b5f-109">Only document types where the group is set to **File** are available for selection.</span></span> <span data-ttu-id="b7b5f-110">Du definerer dokumentets [typer](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) under **Organisasjonsstyring** \> **Dokumentadministrering** \> **Dokumenttyper**.</span><span class="sxs-lookup"><span data-stu-id="b7b5f-110">You define document [types](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) at **Organization administration** \> **Document management** \> **Document types**.</span></span> <span data-ttu-id="b7b5f-111">Konfigurasjonen for ER-mål er den samme som konfigurasjonen for systemet for dokumentbehandling.</span><span class="sxs-lookup"><span data-stu-id="b7b5f-111">The configuration for ER destinations is the same as the configuration for the document management system.</span></span>

<span data-ttu-id="b7b5f-112">[![Siden Dokumenttyper](./media/ER_Destinations-SharePointDocuType.png)](./media/ER_Destinations-SharePointDocuType.png)</span><span class="sxs-lookup"><span data-stu-id="b7b5f-112">[![Document types page](./media/ER_Destinations-SharePointDocuType.png)](./media/ER_Destinations-SharePointDocuType.png)</span></span>

<span data-ttu-id="b7b5f-113">Plasseringen bestemmer hvor filen lagres.</span><span class="sxs-lookup"><span data-stu-id="b7b5f-113">The location determines where the file is saved.</span></span> <span data-ttu-id="b7b5f-114">Etter at **Arkiv**-målet er aktivert, kan resultatene lagres i jobbarkivet.</span><span class="sxs-lookup"><span data-stu-id="b7b5f-114">After the **Archive** destination is enabled, the results can be saved in the Job archive.</span></span> <span data-ttu-id="b7b5f-115">Du kan vise resultatene på **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Arkiverte jobber for elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="b7b5f-115">You can view the results at **Organization administration** \> **Electronic reporting** \> **Electronic reporting archived jobs**.</span></span>

> [!NOTE]
> <span data-ttu-id="b7b5f-116">Velg en dokumenttype for jobbarkivet ved å navigere til **Organisasjonsstyring** \> **Arbeidsområder** \> **Elektronisk rapportering** \> **Parametere for elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="b7b5f-116">Select a document type for the Job archive by navigating to **Organization administration** \> **Workspaces** \> **Electronic reporting** \> **Electronic reporting parameters**.</span></span> <span data-ttu-id="b7b5f-117">Hvis du vil ha mer informasjon, kan du se [Konfigurere rammeverket for elektronisk rapportering (ER)](electronic-reporting-er-configure-parameters.md#prerequisites-for-er-setup).</span><span class="sxs-lookup"><span data-stu-id="b7b5f-117">For more information, see [Configure the Electronic reporting (ER) framework](electronic-reporting-er-configure-parameters.md#prerequisites-for-er-setup).</span></span>

## <a name="sharepoint"></a><span data-ttu-id="b7b5f-118">SharePoint</span><span class="sxs-lookup"><span data-stu-id="b7b5f-118">SharePoint</span></span>

<span data-ttu-id="b7b5f-119">Du kan lagre en fil i en bestemt SharePoint-mappe.</span><span class="sxs-lookup"><span data-stu-id="b7b5f-119">You can save a file in a designated SharePoint folder.</span></span> <span data-ttu-id="b7b5f-120">Hvis du vil definere standard SharePoint-server, går du til **Organisasjonsstyring** \> **Dokumentadministrering** \> **Parametere for dokumentadministrering**.</span><span class="sxs-lookup"><span data-stu-id="b7b5f-120">To define the default SharePoint server, go to **Organization administration** \> **Document management** \> **Document management parameters**.</span></span> <span data-ttu-id="b7b5f-121">I **SharePoint**-fanen konfigurerer du SharePoint-mappen.</span><span class="sxs-lookup"><span data-stu-id="b7b5f-121">On the **SharePoint** tab, configure the SharePoint folder.</span></span> <span data-ttu-id="b7b5f-122">Deretter kan du velge den som mappen der ER-utdataene skal lagres.</span><span class="sxs-lookup"><span data-stu-id="b7b5f-122">Then, you can select it as the folder where the ER output will be saved.</span></span> <span data-ttu-id="b7b5f-123">**SharePoint**-plasseringen må velges i denne dokumenttypen.</span><span class="sxs-lookup"><span data-stu-id="b7b5f-123">The **SharePoint** location must be selected in this document type.</span></span>

<span data-ttu-id="b7b5f-124">[![Velge en SharePoint-mappe](./media/ER_Destinations-SharePointDocuTypeLocation.png)](./media/ER_Destinations-SharePointDocuTypeLocation.png)</span><span class="sxs-lookup"><span data-stu-id="b7b5f-124">[![Selecting a SharePoint folder](./media/ER_Destinations-SharePointDocuTypeLocation.png)](./media/ER_Destinations-SharePointDocuTypeLocation.png)</span></span>

## <a name="azure-storage"></a><span data-ttu-id="b7b5f-125">Azure Storage</span><span class="sxs-lookup"><span data-stu-id="b7b5f-125">Azure Storage</span></span>

<span data-ttu-id="b7b5f-126">Når type dokumentplasseringen er satt til **Azure Storage**, kan du lagre en fil i Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="b7b5f-126">When the document type location is set to **Azure storage**, you can save a file to Azure Storage.</span></span>

> [!NOTE] 
> <span data-ttu-id="b7b5f-127">ER-rammeverket lagrer filer i Azure Blob Storage permanent, i motsetning til databehandlingsrammeverket som bruker policyinnstillingen for oppbevaring i sju dager for dokumenter som må behandles.</span><span class="sxs-lookup"><span data-stu-id="b7b5f-127">The ER framework permanently stores files in Azure Blob storage unlike the Data management framework that applies the seven-day retention policy for documents that must be processed.</span></span> <span data-ttu-id="b7b5f-128">Hvis du vil ha mer informasjon, se [API for å hente meldingsstatus](../data-entities/recurring-integrations.md#api-for-getting-message-status) og [API for statuskontroll for API](../data-entities/data-management-api.md#status-check-api).</span><span class="sxs-lookup"><span data-stu-id="b7b5f-128">For more information, see [API for getting message status](../data-entities/recurring-integrations.md#api-for-getting-message-status) and [Status check API](../data-entities/data-management-api.md#status-check-api).</span></span> <span data-ttu-id="b7b5f-129">De ER-relaterte filene blir lagret i Azure Blob Storage som vedlegg til programtabellposter så lenge som nødvendig.</span><span class="sxs-lookup"><span data-stu-id="b7b5f-129">The ER-related files will be stored in Azure Blob storage as attachments of application table records as long as necessary.</span></span> <span data-ttu-id="b7b5f-130">En enkelt fil vil bli slettet fra Azure Blog Storage sammen med programtabellposten som denne filen var knyttet til.</span><span class="sxs-lookup"><span data-stu-id="b7b5f-130">A single file will be deleted from Azure Blob storage along with the application table record that this file was attached to.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b7b5f-131">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="b7b5f-131">Additional resources</span></span>

- [<span data-ttu-id="b7b5f-132">Oversikt over elektronisk rapportering (ER)</span><span class="sxs-lookup"><span data-stu-id="b7b5f-132">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="b7b5f-133">Mål for elektronisk rapportering (ER)</span><span class="sxs-lookup"><span data-stu-id="b7b5f-133">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)
- [<span data-ttu-id="b7b5f-134">Konfigurere dokumentstyring</span><span class="sxs-lookup"><span data-stu-id="b7b5f-134">Configure document management</span></span>](../../fin-ops/organization-administration/configure-document-management.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]