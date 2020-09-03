---
title: Bekreft utgående forsendelser fra satsvise jobber
description: Dette emnet beskriver hvordan du konfigurerer en satsvis jobb som automatisk bekrefter utgående overføringsordreforsendelser for laster som er klare til levering.
author: perlynne
manager: tfehr
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 41dbfb90b7b19c964e725ee0a4c769402414fb17
ms.sourcegitcommit: 27233e0fda61dac541c5210ca8d94ab4ba74966f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/03/2020
ms.locfileid: "3652256"
---
# <a name="confirm-outbound-shipments-from-batch-jobs"></a><span data-ttu-id="c394d-103">Bekreft utgående forsendelser fra satsvise jobber</span><span class="sxs-lookup"><span data-stu-id="c394d-103">Confirm outbound shipments from batch jobs</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c394d-104">Dette emnet beskriver hvordan du konfigurerer en satsvis jobb som automatisk bekrefter utgående overføringsordreforsendelser for laster som er klare til levering.</span><span class="sxs-lookup"><span data-stu-id="c394d-104">This topic describes how to set up a batch job that automatically confirms outbound transfer-order shipments for ready-to-ship loads.</span></span> <span data-ttu-id="c394d-105">Den satsvise jobben som beskrives her, gjelder bare for overføringsordreforsendelser, ikke salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="c394d-105">The batch job described here only applies to transfer order shipments, not to sales orders.</span></span>

## <a name="enable-the-confirm-outbound-shipments-from-batch-jobs-feature"></a><span data-ttu-id="c394d-106">Aktivere funksjonen Bekreft utgående forsendelser fra satsvise jobber</span><span class="sxs-lookup"><span data-stu-id="c394d-106">Enable the Confirm outbound shipments from batch jobs feature</span></span>

<span data-ttu-id="c394d-107">Før du kan bruke denne funksjonen, må du aktivere den i systemet.</span><span class="sxs-lookup"><span data-stu-id="c394d-107">Before you can use this feature, it must be enabled on your system.</span></span> <span data-ttu-id="c394d-108">Administratorer kan bruke siden [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til å kontrollere funksjonsstatusen og aktivere den hvis det er nødvendig.</span><span class="sxs-lookup"><span data-stu-id="c394d-108">Administrators can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) page to check the feature status and enable it if needed.</span></span> <span data-ttu-id="c394d-109">Funksjonen er oppført som:</span><span class="sxs-lookup"><span data-stu-id="c394d-109">The feature is listed as:</span></span>

- <span data-ttu-id="c394d-110">**Modul** - *Lagerstyring*</span><span class="sxs-lookup"><span data-stu-id="c394d-110">**Module** - *Warehouse management*</span></span>
- <span data-ttu-id="c394d-111">**Funksjonsnavn** - *Bekreft utgående forsendelser fra satsvise jobber*</span><span class="sxs-lookup"><span data-stu-id="c394d-111">**Feature name** - *Confirm outbound shipments from batch jobs*</span></span>

## <a name="process-outbound-shipments"></a><span data-ttu-id="c394d-112">Behandle utgående forsendelser</span><span class="sxs-lookup"><span data-stu-id="c394d-112">Process outbound shipments</span></span>

<span data-ttu-id="c394d-113">Slik setter du opp en planlagt satsvis jobb for å kjøre den utgående forsendelsesbekreftelsen for laster som er klare til levering:</span><span class="sxs-lookup"><span data-stu-id="c394d-113">To set up a scheduled batch job to run the outbound shipment confirmation for loads that are ready to ship:</span></span>

1. <span data-ttu-id="c394d-114">Gå til **Lagerstyring \> Periodiske oppgaver \> Behandle utgående forsendelser**.</span><span class="sxs-lookup"><span data-stu-id="c394d-114">Go to **Warehouse management \> Periodic tasks \> Process outbound shipments**.</span></span>
1. <span data-ttu-id="c394d-115">Dialogboksen **Bekreft forsendelse** åpnes.</span><span class="sxs-lookup"><span data-stu-id="c394d-115">The **Confirm shipment** dialog box opens.</span></span> <span data-ttu-id="c394d-116">Velg **Filtrer** i hurtigfanen **Poster som skal inkluderes** .</span><span class="sxs-lookup"><span data-stu-id="c394d-116">On the **Records to include** FastTab, select **Filter**.</span></span>
1. <span data-ttu-id="c394d-117">Dialogboksen for redigeringsprogram for spørring åpnes.</span><span class="sxs-lookup"><span data-stu-id="c394d-117">The query editor dialog box opens.</span></span> <span data-ttu-id="c394d-118">På **Område**-fanen legger du til en tabell med følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="c394d-118">On the **Range** tab, add a row with the following values:</span></span>
    - <span data-ttu-id="c394d-119">**Tabell** - *Laster*</span><span class="sxs-lookup"><span data-stu-id="c394d-119">**Table** - *Loads*</span></span>
    - <span data-ttu-id="c394d-120">**Utledet tabell** - *Laster*</span><span class="sxs-lookup"><span data-stu-id="c394d-120">**Derived table** - *Loads*</span></span>
    - <span data-ttu-id="c394d-121">**Felt** - *Laststatus*</span><span class="sxs-lookup"><span data-stu-id="c394d-121">**Field** - *Load status*</span></span>
    - <span data-ttu-id="c394d-122">**Vilkår** - *Lastet*</span><span class="sxs-lookup"><span data-stu-id="c394d-122">**Criteria** - *Loaded*</span></span>
1. <span data-ttu-id="c394d-123">Velg **OK** for å gå tilbake til dialogboksen **Bekreft forsendelse**.</span><span class="sxs-lookup"><span data-stu-id="c394d-123">Select **OK** to return to the **Confirm shipment** dialog box.</span></span>
1. <span data-ttu-id="c394d-124">På hurtigfanen **Kjør i bakgrunnen** setter du **Satsvis behandling** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="c394d-124">On the **Run in the background** FastTab, set **Batch processing** to **Yes**.</span></span>
1. <span data-ttu-id="c394d-125">På hurtigfanen **Kjør i bakgrunnen** velger du **Regelmessighet**.</span><span class="sxs-lookup"><span data-stu-id="c394d-125">On the **Run in the background** FastTab, select **Recurrence**.</span></span>
1. <span data-ttu-id="c394d-126">Dialogboksen **Definer regelmessighet** åpnes.</span><span class="sxs-lookup"><span data-stu-id="c394d-126">The **Define recurrence** dialog box opens.</span></span> <span data-ttu-id="c394d-127">Angi kjøretidsplanen etter behov for firmaet.</span><span class="sxs-lookup"><span data-stu-id="c394d-127">Set the run schedule as needed for your business.</span></span>
1. <span data-ttu-id="c394d-128">Velg **OK** for å gå tilbake til dialogboksen **Bekreft forsendelse**.</span><span class="sxs-lookup"><span data-stu-id="c394d-128">Select **OK** to return to the **Confirm shipment** dialog box.</span></span>
1. <span data-ttu-id="c394d-129">Velg **OK** i dialogboksen **Bekreft forsendelse** for å legge til den satsvise jobben i den satsvise køen.</span><span class="sxs-lookup"><span data-stu-id="c394d-129">Select **OK** on the **Confirm shipment** dialog box to add the batch job to the batch queue.</span></span>

<span data-ttu-id="c394d-130">Hvis du vil ha mer informasjon, kan du se [Oversikt over satsvis behandling](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md).</span><span class="sxs-lookup"><span data-stu-id="c394d-130">For more information, see [Batch processing overview](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md).</span></span>