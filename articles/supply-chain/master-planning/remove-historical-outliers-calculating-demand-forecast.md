---
title: Fjerne utestående fra historiske transaksjonsdata ved beregning av en behovsprognose
description: Denne artikkelen beskriver hvordan du utelater utestående fra de historiske dataene som brukes til å beregne en behovsprognose. Ved å ekskludere utestående kan du forbedre nøyaktighet av prognosen.
author: roxanadiaconu
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanForecastParameters, ReqDemPlanOutlierQuerySetup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 72621
ms.assetid: 88a964af-14eb-4c5c-945b-388e5908362c
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f8593b0f55e899a32f2407fcb668d8bcb0ff8431
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/02/2020
ms.locfileid: "3213452"
---
# <a name="remove-outliers-from-historical-transaction-data-when-calculating-a-demand-forecast"></a><span data-ttu-id="91a69-104">Fjerne utestående fra historiske transaksjonsdata ved beregning av en behovsprognose</span><span class="sxs-lookup"><span data-stu-id="91a69-104">Remove outliers from historical transaction data when calculating a demand forecast</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="91a69-105">Denne artikkelen beskriver hvordan du utelater utestående fra de historiske dataene som brukes til å beregne en behovsprognose.</span><span class="sxs-lookup"><span data-stu-id="91a69-105">This article describes how to exclude outliers from the historical data that is used to calculate a demand forecast.</span></span> <span data-ttu-id="91a69-106">Ved å ekskludere utestående kan du forbedre nøyaktighet av prognosen.</span><span class="sxs-lookup"><span data-stu-id="91a69-106">By excluding outliers, you can improve forecast accuracy.</span></span>

<span data-ttu-id="91a69-107">Du kan utelate utestående for å forbedre nøyaktighet av prognosen.</span><span class="sxs-lookup"><span data-stu-id="91a69-107">You can exclude outliers to improve forecast accuracy.</span></span> <span data-ttu-id="91a69-108">Denne oppgaven er valgfri.</span><span class="sxs-lookup"><span data-stu-id="91a69-108">This is an optional task.</span></span> <span data-ttu-id="91a69-109">Her er en oversikt over prosessen:</span><span class="sxs-lookup"><span data-stu-id="91a69-109">Here is an overview of the process:</span></span>

1.  <span data-ttu-id="91a69-110">Klikk **Hovedplanlegging** &gt; **Oppsett** &gt; **Behovsprognose** &gt; **Fjerning av utestående** for å åpne **Fjerning av utestående**-siden der du kan bruke en spørring for å velge transaksjonen som skal ekskluderes.</span><span class="sxs-lookup"><span data-stu-id="91a69-110">Click **Master planning** &gt; **Setup** &gt; **Demand forecasting** &gt; **Outlier removal** to open the **Outlier removal** page, where you can use a query to select the transactions to exclude.</span></span>
2.  <span data-ttu-id="91a69-111">Velg firmaet som spørringen gjelder for, og skriv inn et navn og en beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="91a69-111">Select the company that the query applies to, and then enter a name and description.</span></span> <span data-ttu-id="91a69-112">**Spørringsdato**-feltet settes automatisk til den gjeldende datoen.</span><span class="sxs-lookup"><span data-stu-id="91a69-112">The **Query date** field is automatically set to the current date.</span></span>
3.  <span data-ttu-id="91a69-113">Merk av for **Aktiv** for å utelate transaksjoner som blir funnet av spørringen, fra historiske data.</span><span class="sxs-lookup"><span data-stu-id="91a69-113">Select the **Active** check box to exclude the transactions that the query finds from the historical data.</span></span> <span data-ttu-id="91a69-114">Denne innstillingen trer i kraft når du oppretter en basislinjeprognose.</span><span class="sxs-lookup"><span data-stu-id="91a69-114">This setting will take effect when you create a baseline forecast.</span></span>
4.  <span data-ttu-id="91a69-115">På **Spørring etter fjerning av utestående**-siden kan du legge til, fjerne og velge kriteriene som definerer hvilke transaksjoner som skal utelates når basislinjeprognosen beregnes.</span><span class="sxs-lookup"><span data-stu-id="91a69-115">On the **Outlier removal query** page, you can add, remove, and select the criteria that define which transactions will be excluded when the baseline forecast is calculated.</span></span> <span data-ttu-id="91a69-116">Velg for eksempel en bestemt vare eller ordretransaksjon som skal ekskluderes.</span><span class="sxs-lookup"><span data-stu-id="91a69-116">For example, select a specific item or order transaction to exclude.</span></span>
5.  <span data-ttu-id="91a69-117">Klikk **Vis transaksjoner**.</span><span class="sxs-lookup"><span data-stu-id="91a69-117">Click **Display transactions**.</span></span> <span data-ttu-id="91a69-118">**Utestående transaksjoner**-siden viser transaksjonene som oppfyller kriteriene som du definerte i spørringen, og som utelates fra historiske data når behovsprognosen beregnes.</span><span class="sxs-lookup"><span data-stu-id="91a69-118">The **Outlier transactions** page lists the transactions that meet the criteria that you defined in the query, and that will be excluded from the historical data when the demand forecast is calculated.</span></span>

<span data-ttu-id="91a69-119">**Merk:** Du kan også opprette en spørring som er basert på en eksisterende spørring.</span><span class="sxs-lookup"><span data-stu-id="91a69-119">**Note:** You can also create a query that is based on an existing query.</span></span> <span data-ttu-id="91a69-120">Velg spørringen du vil kopiere, og klikk deretter **Duplikat**.</span><span class="sxs-lookup"><span data-stu-id="91a69-120">Select the query to copy, and then click **Duplicate**.</span></span> <span data-ttu-id="91a69-121">**Spørringsdato**-feltet identifiserer versjonen.</span><span class="sxs-lookup"><span data-stu-id="91a69-121">The **Query date** field identifies the version.</span></span> <span data-ttu-id="91a69-122">Du kan bruke spørringen som den er, eller du kan klikke **Rediger spørring** for å endre vilkårene.</span><span class="sxs-lookup"><span data-stu-id="91a69-122">You can use the query as it is, or you can click **Edit query** to modify the criteria.</span></span> <span data-ttu-id="91a69-123">Du kan også endre navnet og beskrivelsen av den nye spørringen.</span><span class="sxs-lookup"><span data-stu-id="91a69-123">You can optionally modify the name and description of the new query.</span></span>

<a name="additional-resources"></a><span data-ttu-id="91a69-124">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="91a69-124">Additional resources</span></span>
--------

[<span data-ttu-id="91a69-125">Oversikt over behovsprognose</span><span class="sxs-lookup"><span data-stu-id="91a69-125">Demand forecasting overview</span></span>](introduction-demand-forecasting.md)

[<span data-ttu-id="91a69-126">Overvåke prognosenøyaktighet</span><span class="sxs-lookup"><span data-stu-id="91a69-126">Monitor forecast accuracy</span></span>](monitor-forecast-accuracy.md)



