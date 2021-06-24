---
title: Forbedre forutsigelsesmodellen (forhåndsversjon)
description: Dette emnet beskriver funksjoner du kan bruke til å forbedre ytelsen til forutsigelsesmodeller.
author: ShivamPandey-msft
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 184a1cb5d3851e26b41340b711c51ef38e06eb53
ms.sourcegitcommit: ebcd9019cbb88a7f2afd9e701812e222566fd43d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/04/2021
ms.locfileid: "6186648"
---
# <a name="improve-the-prediction-model-preview"></a><span data-ttu-id="72cbd-103">Forbedre forutsigelsesmodellen (forhåndsversjon)</span><span class="sxs-lookup"><span data-stu-id="72cbd-103">Improve the prediction model (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="72cbd-104">Dette emnet beskriver funksjoner du kan bruke til å forbedre ytelsen til forutsigelsesmodeller.</span><span class="sxs-lookup"><span data-stu-id="72cbd-104">This topic describes features that you can use to improve the performance of prediction models.</span></span> <span data-ttu-id="72cbd-105">Du begynner å forbedre modellen i arbeidsområdet **Kundebetalingsforutsigelser** i Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="72cbd-105">You start to improve your model in the **Customer payment predictions** workspace in Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="72cbd-106">Forbedringstrinnene fullføres deretter i AI Builder.</span><span class="sxs-lookup"><span data-stu-id="72cbd-106">The improvement steps are then completed in AI Builder.</span></span>

## <a name="select-historical-outcomes"></a><span data-ttu-id="72cbd-107">Velge historiske resultater</span><span class="sxs-lookup"><span data-stu-id="72cbd-107">Select historical outcomes</span></span>

<span data-ttu-id="72cbd-108">Du velger først ett eller flere av de tre mulige resultatene for fakturaer: **Til planlagt tid**, **Forsinket** og **Svært sent**.</span><span class="sxs-lookup"><span data-stu-id="72cbd-108">You first select one or more of the three possible outcomes for invoices: **On time**, **Late**, and **Very late**.</span></span> <span data-ttu-id="72cbd-109">Alle de tre resultatene bør velges.</span><span class="sxs-lookup"><span data-stu-id="72cbd-109">All three outcomes should be selected.</span></span> <span data-ttu-id="72cbd-110">Hvis du fjerner merkingen av noen av resultatene, blir fakturaene filtrert ut av opplæringsprosessen, og nøyaktigheten til forutsigelsen blir redusert.</span><span class="sxs-lookup"><span data-stu-id="72cbd-110">If you clear the selection of any of the outcomes, invoices will be filtered out of the training process and the accuracy of the prediction will be reduced.</span></span>

<span data-ttu-id="72cbd-111">[![Bekrefte resultater](./media/confirm-3-outcomes.png)](./media/confirm-3-outcomes.png)</span><span class="sxs-lookup"><span data-stu-id="72cbd-111">[![Confirming outcomes](./media/confirm-3-outcomes.png)](./media/confirm-3-outcomes.png)</span></span>

<span data-ttu-id="72cbd-112">Hvis organisasjonen bare krever to resultater, endrer du de **Forsinket**- og **Svært sent**-terskelene til 0 (null) dager.</span><span class="sxs-lookup"><span data-stu-id="72cbd-112">If your organization requires only two outcomes, change the **Late** and **Very late** thresholds to 0 (zero) days.</span></span> <span data-ttu-id="72cbd-113">På denne måten kan du effektivt skjule forutsigelsen til en binær tilstand **Til planlagt tid** eller **Forsinket**.</span><span class="sxs-lookup"><span data-stu-id="72cbd-113">In this way, you effectively collapse the prediction to a binary state of **On time** or **Late**.</span></span>

## <a name="select-fields"></a><span data-ttu-id="72cbd-114">Velg felter</span><span class="sxs-lookup"><span data-stu-id="72cbd-114">Select fields</span></span>

<span data-ttu-id="72cbd-115">Når du velger felt som skal tas med i modellen, må du være oppmerksom på at listen inneholder alle tilgjengelige felt i Microsoft Dataverse-tabellen som er tilordnet dataene i Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="72cbd-115">When you're selecting fields to include in the model, be aware that the list includes all available fields in the Microsoft Dataverse table that is mapped to the data in the Azure data lake.</span></span> <span data-ttu-id="72cbd-116">Noen av disse feltene bør **ikke** velges.</span><span class="sxs-lookup"><span data-stu-id="72cbd-116">Some of these fields should **not** be selected.</span></span> <span data-ttu-id="72cbd-117">Feltene som ikke bør velges, faller inn i én av tre kategorier:</span><span class="sxs-lookup"><span data-stu-id="72cbd-117">The fields that should not be selected fall into one of three categories:</span></span>

- <span data-ttu-id="72cbd-118">Feltet er obligatorisk for Dataverse-tabellen, men det finnes ingen sikkerhetskopi av dataene i Data Lake.</span><span class="sxs-lookup"><span data-stu-id="72cbd-118">The field is required for the Dataverse table, but there is no backing data for it in the data lake.</span></span>
- <span data-ttu-id="72cbd-119">Feltet er en ID og gir derfor ingen mening for en maskinlæringsfunksjon.</span><span class="sxs-lookup"><span data-stu-id="72cbd-119">The field is an ID and therefore doesn't make sense for a machine learning feature.</span></span>
- <span data-ttu-id="72cbd-120">Feltet representerer informasjon som ikke vil være tilgjengelig under forutsigelse.</span><span class="sxs-lookup"><span data-stu-id="72cbd-120">The field represents information that won't be available during prediction.</span></span>

<span data-ttu-id="72cbd-121">De følgende delene viser feltene som er tilgjengelige for faktura- og kundeenhetene, og viser feltene som **ikke** må velges for opplæring.</span><span class="sxs-lookup"><span data-stu-id="72cbd-121">The following sections show the fields that are available for the invoice and customer entities, and list the fields that should **not** be selected for training.</span></span> <span data-ttu-id="72cbd-122">Kategorien som er angitt for hvert av disse feltene, refererer til kategoriene i listen ovenfor.</span><span class="sxs-lookup"><span data-stu-id="72cbd-122">The category that is specified for each of those fields refers to the categories in the preceding list.</span></span>
 
### <a name="invoice-dataverse-table"></a><span data-ttu-id="72cbd-123">Dataverse-tabellen for faktura</span><span class="sxs-lookup"><span data-stu-id="72cbd-123">Invoice Dataverse table</span></span>

<span data-ttu-id="72cbd-124">Følgende illustrasjon viser feltene som er tilgjengelig for fakturatabellen.</span><span class="sxs-lookup"><span data-stu-id="72cbd-124">The following illustration shows the fields that are available for the invoice table.</span></span>

<span data-ttu-id="72cbd-125">[![Tilgjengelige felt for fakturatabellen](./media/available-fields.png)](./media/available-fields.png)</span><span class="sxs-lookup"><span data-stu-id="72cbd-125">[![Available fields for the invoice table](./media/available-fields.png)](./media/available-fields.png)</span></span>

<span data-ttu-id="72cbd-126">Følgende felt bør ikke velges for opplæring:</span><span class="sxs-lookup"><span data-stu-id="72cbd-126">The following fields should not be selected for training:</span></span>

- <span data-ttu-id="72cbd-127">**Fakturakonto** (kategori 2)</span><span class="sxs-lookup"><span data-stu-id="72cbd-127">**Invoice Account** (category 2)</span></span>
- <span data-ttu-id="72cbd-128">**Er lukket** (kategori 3) – Dette feltet brukes til å filtrere fakturaer for læring (lukket) og forutsigelse (ikke lukket).</span><span class="sxs-lookup"><span data-stu-id="72cbd-128">**Is closed** (category 3) – This field is used to filter invoices for training (closed) and prediction (not closed).</span></span>
- <span data-ttu-id="72cbd-129">**Navn** (kategori 1)</span><span class="sxs-lookup"><span data-stu-id="72cbd-129">**Name** (category 1)</span></span>
- <span data-ttu-id="72cbd-130">**Kilde-ID** (kategori 2)</span><span class="sxs-lookup"><span data-stu-id="72cbd-130">**Source Id** (category 2)</span></span>
- <span data-ttu-id="72cbd-131">**Kildepost** (kategori 2)</span><span class="sxs-lookup"><span data-stu-id="72cbd-131">**Source record** (category 2)</span></span>
- <span data-ttu-id="72cbd-132">**Kildetabell** (kategori 2)</span><span class="sxs-lookup"><span data-stu-id="72cbd-132">**Source table** (category 2)</span></span>

### <a name="customer-dataverse-table"></a><span data-ttu-id="72cbd-133">Dataverse-tabell for kunde</span><span class="sxs-lookup"><span data-stu-id="72cbd-133">Customer Dataverse table</span></span>

<span data-ttu-id="72cbd-134">Følgende illustrasjon viser feltene som er tilgjengelige for kundetabellen.</span><span class="sxs-lookup"><span data-stu-id="72cbd-134">The following illustration shows the fields that are available for the customer table.</span></span>

<span data-ttu-id="72cbd-135">[![Tilgjengelige felt for kundetabellen](./media/related-entities.png)](./media/related-entities.png)</span><span class="sxs-lookup"><span data-stu-id="72cbd-135">[![Available fields for the customer table](./media/related-entities.png)](./media/related-entities.png)</span></span>

<span data-ttu-id="72cbd-136">Følgende felt bør ikke velges for opplæring:</span><span class="sxs-lookup"><span data-stu-id="72cbd-136">The following field should not be selected for training:</span></span>

- <span data-ttu-id="72cbd-137">**Unik nøkkel for rad** (kategori 2)</span><span class="sxs-lookup"><span data-stu-id="72cbd-137">**Row Unique Key** (category 2)</span></span>

## <a name="filters"></a><span data-ttu-id="72cbd-138">Filtre</span><span class="sxs-lookup"><span data-stu-id="72cbd-138">Filters</span></span>

<span data-ttu-id="72cbd-139">Filtrene støtter for øyeblikket ikke scenarioet med kundebetalingsforutsigelse.</span><span class="sxs-lookup"><span data-stu-id="72cbd-139">The filters don't currently support the Customer payment predictor scenario.</span></span> <span data-ttu-id="72cbd-140">Velg derfor **Hopp over dette trinnet**, og fortsett til sammendragssiden.</span><span class="sxs-lookup"><span data-stu-id="72cbd-140">Therefore, select **Skip this step**, and continue to the summary page.</span></span>

<span data-ttu-id="72cbd-141">[![Fokusmodell med filtre](./media/focus-model-with-filters.png)](./media/focus-model-with-filters.png)</span><span class="sxs-lookup"><span data-stu-id="72cbd-141">[![Focus model with filters](./media/focus-model-with-filters.png)](./media/focus-model-with-filters.png)</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
