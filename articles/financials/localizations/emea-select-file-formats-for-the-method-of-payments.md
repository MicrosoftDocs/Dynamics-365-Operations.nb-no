---
title: "Filformater for betalingsmåter"
description: "Dette emnet beskriver to metoder for å få filformater du kan bruke for betalingsmåter."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustPaymMode, VendPaymMode
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 262514
ms.search.region: Belgium, France, Germany, Norway, Spain, Sweden, Switzerland
ms.author: v-lenest
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 3e0122d6e61efa012722c707ac4ca74c619e5a20
ms.openlocfilehash: 2981fae40e43dec96b4e5b6c812e96ee3e959a9d
ms.contentlocale: nb-no
ms.lasthandoff: 07/31/2017

---

# <a name="file-formats-for-methods-of-payment"></a><span data-ttu-id="a3160-103">Filformater for betalingsmåter</span><span class="sxs-lookup"><span data-stu-id="a3160-103">File formats for methods of payment</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="a3160-104">Dette emnet beskriver to metoder for å få filformater du kan bruke for betalingsmåter.</span><span class="sxs-lookup"><span data-stu-id="a3160-104">This topic describes the two methods for getting file formats that you can use for methods of payment.</span></span>

<span data-ttu-id="a3160-105">Det finnes to metoder du kan bruke til å få filformater for bruk med betalingsmåten, ER-filformater (elektronisk rapportering) eller et X ++-filformater.</span><span class="sxs-lookup"><span data-stu-id="a3160-105">There are two methods that you can use to get file formats for use with methods of payment, electronic reporting (ER) file formats or X++ file formats.</span></span> <span data-ttu-id="a3160-106">Når du setter opp en betalingsmåte for en kunde eller leverandør, angir du hvilke filformater og standarder som skal brukes for betalinger og hvordan betalinger vil bli behandlet.</span><span class="sxs-lookup"><span data-stu-id="a3160-106">When you set up a method of payment for a customer or vendor, you indicate which file formats and standards should be used for payments and how payments will be processed.</span></span> <span data-ttu-id="a3160-107">Du kan velge blant følgende typer formater:</span><span class="sxs-lookup"><span data-stu-id="a3160-107">You can select from the following types of formats:</span></span>

-   <span data-ttu-id="a3160-108">Eksporter</span><span class="sxs-lookup"><span data-stu-id="a3160-108">Export</span></span>
-   <span data-ttu-id="a3160-109">Importer</span><span class="sxs-lookup"><span data-stu-id="a3160-109">Import</span></span>
-   <span data-ttu-id="a3160-110">Retur</span><span class="sxs-lookup"><span data-stu-id="a3160-110">Return</span></span>
-   <span data-ttu-id="a3160-111">Remittering</span><span class="sxs-lookup"><span data-stu-id="a3160-111">Remittance</span></span>

### <a name="method-1-electronic-reporting-file-formats"></a><span data-ttu-id="a3160-112">Metode 1: formater for elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="a3160-112">Method 1: Electronic reporting file formats</span></span>

<span data-ttu-id="a3160-113">For filformater som er basert på ER-konfigurasjoner, må du importere konfigurasjonene fra Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="a3160-113">For file formats that are based on ER configurations, you must import the configurations from Lifecycle Services (LCS).</span></span> <span data-ttu-id="a3160-114">Hvis du vil ha mer informasjon, kan du se [Laste ned elektroniske rapporteringskonfigurasjoner fra Lifecycle Services](/dynamics365/unified-operations/dev-itpro/analytics/download-electronic-reporting-configuration-lcs).</span><span class="sxs-lookup"><span data-stu-id="a3160-114">For more information, see [Download Electronic reporting configurations from Lifecycle Services](/dynamics365/unified-operations/dev-itpro/analytics/download-electronic-reporting-configuration-lcs).</span></span> <span data-ttu-id="a3160-115">Når du har importert rapporteringskonfigurasjoner for disse filformatene, kan du velge de importerte formatene på siden **Betalingsmåter**.</span><span class="sxs-lookup"><span data-stu-id="a3160-115">After you import reporting configurations for those file formats, the imported formats will be available to select on the **Methods of payment** page.</span></span> <span data-ttu-id="a3160-116">Prosessen med å importere og velge filformater for Europa ligner på fremgangsmåten for Japan.</span><span class="sxs-lookup"><span data-stu-id="a3160-116">The process for importing and selecting file formats for Europe is similar to the procedure for Japan.</span></span> <span data-ttu-id="a3160-117">Hvis du vil ha mer informasjon, se [Aktivere JBA-betalingsfilformatet](/dynamics365/unified-operations/financials/localizations/tasks/jba-payment-file-format)</span><span class="sxs-lookup"><span data-stu-id="a3160-117">For more details, see [Enable the JBA payment file format](/dynamics365/unified-operations/financials/localizations/tasks/jba-payment-file-format)</span></span>

### <a name="method-2-x-file-formats"></a><span data-ttu-id="a3160-118">Metode 2: X++-filformater</span><span class="sxs-lookup"><span data-stu-id="a3160-118">Method 2: X++ file formats</span></span>

<span data-ttu-id="a3160-119">For å velge filformatene som er basert på X++-kode, kan du fullføre trinnene nedenfor.</span><span class="sxs-lookup"><span data-stu-id="a3160-119">To select file formats that are based on X++ code, complete the following steps.</span></span>

1.  <span data-ttu-id="a3160-120">Gå til siden **Betalingsmåter**.</span><span class="sxs-lookup"><span data-stu-id="a3160-120">Go to the **Methods of payment** page.</span></span>
2.  <span data-ttu-id="a3160-121">På **Filformater**-hurtigfanen klikker du **Oppsett**.</span><span class="sxs-lookup"><span data-stu-id="a3160-121">On the **File formats** FastTab, click **Setup**.</span></span>
3.  <span data-ttu-id="a3160-122">Velg kategorien som samsvarer med filformattypen.</span><span class="sxs-lookup"><span data-stu-id="a3160-122">Select the tab that corresponds with the file format type.</span></span>
4.  <span data-ttu-id="a3160-123">Velg et filformat fra **Tilgjengelig**-listen og flytt det til **Valgt**-listen med pilkontrollen.</span><span class="sxs-lookup"><span data-stu-id="a3160-123">Select a file format from the **Available** list and move it to the **Selected** list with the arrow control.</span></span>
5.  <span data-ttu-id="a3160-124">Lukk siden **Filformater for betalingsmåter**.</span><span class="sxs-lookup"><span data-stu-id="a3160-124">Close the **File formats for methods of payment** page.</span></span>
6.  <span data-ttu-id="a3160-125">På **Filformater**-hurtigfanen velger du filformatet som skal brukes for betalingsmåten, fra det aktuelle filformatfeltet.</span><span class="sxs-lookup"><span data-stu-id="a3160-125">On the **File formats** FastTab, select the file format to use for the method of payment from the appropriate file format field.</span></span> <span data-ttu-id="a3160-126">Alternativene for generell elektronisk rapportering skal settes til **Ingen** for X++-filformater.</span><span class="sxs-lookup"><span data-stu-id="a3160-126">The General electronic reporting options should be set to **No** for X++ file formats.</span></span>





