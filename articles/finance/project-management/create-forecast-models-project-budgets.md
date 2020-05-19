---
title: Opprette prognosemodeller for prosjektbudsjetter
description: Dette emnet beskriver hvordan du oppretter en prognosemodell for gjenstående budsjetter.
author: RadhikaRS
manager: AnnBe
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 07e540f23a668b40a54906a67d87552fe991825a
ms.sourcegitcommit: 5de75c61c33e57c813944f1ab6100aceb020d432
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/29/2020
ms.locfileid: "3321785"
---
# <a name="create-forecast-models-for-project-budgets"></a><span data-ttu-id="7b6c9-103">Opprette prognosemodeller for prosjektbudsjetter</span><span class="sxs-lookup"><span data-stu-id="7b6c9-103">Create forecast models for project budgets</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7b6c9-104">Dette emnet beskriver hvordan du oppretter en prognosemodell for gjenstående budsjetter.</span><span class="sxs-lookup"><span data-stu-id="7b6c9-104">This topic describes how to create a forecast model for remaining budgets.</span></span> <span data-ttu-id="7b6c9-105">Et prosjekt som skal gjennomgå budsjettkontroll, bruker to typer budsjetter: opprinnelig budsjett og gjenstående budsjett.</span><span class="sxs-lookup"><span data-stu-id="7b6c9-105">A project that is subject to budget control uses two types of budgets: original and remaining.</span></span> <span data-ttu-id="7b6c9-106">Når du oppretter et prosjektbudsjett, må du angi prognosemodellene for opprinnelig og gjenstående budsjett som ble opprettet på siden **Prognosemodeller**.</span><span class="sxs-lookup"><span data-stu-id="7b6c9-106">When you create a project budget, you must specify the original and remaining budget forecast models that were created in the **Forecast models** page.</span></span> <span data-ttu-id="7b6c9-107">Prosjektbudsjetter som er basert på angitte modeller, opprettes når du igangsetter prosjektbudsjettet.</span><span class="sxs-lookup"><span data-stu-id="7b6c9-107">Project budgets based on the specified models are created when you commit the project budget.</span></span>

> [!NOTE]
> <span data-ttu-id="7b6c9-108">En prognosemodell som brukes til budsjettkontroll, kan ikke ha en undermodell og kan ikke brukes som en undermodell.</span><span class="sxs-lookup"><span data-stu-id="7b6c9-108">A forecast model that is used for budget control can’t have a submodel or be used as a submodel.</span></span>

1. <span data-ttu-id="7b6c9-109">Velg **Prosjektstyring og regnskap** > **Oppsett** > **Prognoser**  > **Prognosemodeller**.</span><span class="sxs-lookup"><span data-stu-id="7b6c9-109">Select **Project management and accounting** > **Setup** > **Forecasts**  > **Forecast models**.</span></span>
2. <span data-ttu-id="7b6c9-110">Velg **Ny** for å opprette en ny prognosemodell, og angi deretter et modell-ID-nummer og et navn for den nye modellen.</span><span class="sxs-lookup"><span data-stu-id="7b6c9-110">Select **New** to create a new forecast model, and then enter a model ID number and name for the new model.</span></span> 
3. <span data-ttu-id="7b6c9-111">Sett alternativet **Stoppet** til **Ja** for å hindre eventuelle endringer i prognoselinjer for prognosemodellen.</span><span class="sxs-lookup"><span data-stu-id="7b6c9-111">Set the **Stopped** option to **Yes** to prevent any changes to the forecast lines for the forecast model.</span></span> 
4. <span data-ttu-id="7b6c9-112">Hvis prognoselinjene som modellen er tilknyttet, skal generere kontantstrømprognoser i økonomimodulen, setter du **Inkluder i kontantstrømprognoser** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="7b6c9-112">If the forecast lines that the model is associated with should generate cash flow forecasts in the general ledger, set **Include in Cash flow forecasts** to **Yes.**</span></span> 
5. <span data-ttu-id="7b6c9-113">Hvis du vil bruke prosjektdatoen som fakturadato, setter du valget for **prognosefakturadato** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="7b6c9-113">To use the project date as the invoice date, set **Forecast Invoice date** to **Yes**.</span></span> 
6. <span data-ttu-id="7b6c9-114">I **Budgettype**-feltet velger du én av følgende modelltyper:</span><span class="sxs-lookup"><span data-stu-id="7b6c9-114">In the **Budget type** field, select one of the following model types:</span></span>

   - <span data-ttu-id="7b6c9-115">**Opprinnelig budsjett**: Bruk de opprinnelige budsjettbeløpene som igangsettes når det opprinnelige budsjettet opprettes og godkjennes.</span><span class="sxs-lookup"><span data-stu-id="7b6c9-115">**Original budget**: Use the original budget amounts that are committed when the initial budget is created and approved.</span></span>
   - <span data-ttu-id="7b6c9-116">**Gjenstående budsjett**: Bruk de gjenstående budsjettbeløpene mens prosjektet pågår.</span><span class="sxs-lookup"><span data-stu-id="7b6c9-116">**Remaining budget**: Use the remaining budget amounts during the life of the project.</span></span> <span data-ttu-id="7b6c9-117">Saldoene i denne prognosemodellen reduseres av faktiske transaksjoner og økes eller reduseres av budsjettendringer.</span><span class="sxs-lookup"><span data-stu-id="7b6c9-117">The balances in this forecast model are reduced by actual transactions and increased or decreased by budget revisions.</span></span>
   - <span data-ttu-id="7b6c9-118">**Overført budsjett**: Bruk de overførte budsjettbeløpene for prosjektet.</span><span class="sxs-lookup"><span data-stu-id="7b6c9-118">**Carry-forward**: Use the carry-forward budget amounts for the project.</span></span> <span data-ttu-id="7b6c9-119">Overføring er en valgfri prosess som kan kjøres for å overføre ubrukte budsjettbeløp fra ett regnskapsår til et annet.</span><span class="sxs-lookup"><span data-stu-id="7b6c9-119">Carry-forward is an optional process that can be run to transfer unused budget amounts from one fiscal year to another.</span></span>

7. <span data-ttu-id="7b6c9-120">Angi følgende alternativer etter behov:</span><span class="sxs-lookup"><span data-stu-id="7b6c9-120">Set the following options as required:</span></span>

   - <span data-ttu-id="7b6c9-121">Aktiver **Prognosefakturadato** for å bruke prosjektdatoen som fakturadato.</span><span class="sxs-lookup"><span data-stu-id="7b6c9-121">Enable **Forecast invoice date** to use the project date as the invoice date.</span></span>
   - <span data-ttu-id="7b6c9-122">Aktiver **Prognose med VIA** for prognosebasert på varer i arbeid (VIA), og velg deretter typen VIA.</span><span class="sxs-lookup"><span data-stu-id="7b6c9-122">Enable **Forecast with WIP** to forecast based on work in progress (WIP), and then select the type of WIP.</span></span> 
   - <span data-ttu-id="7b6c9-123">Du kan beholde standard **Budsjettype** som **Ingen** eller angi en ny type.</span><span class="sxs-lookup"><span data-stu-id="7b6c9-123">You can keep the default **Budget type** as **None** or enter a new type.</span></span> <span data-ttu-id="7b6c9-124">Budsjettypen kan ikke endres etter at du har endret en post.</span><span class="sxs-lookup"><span data-stu-id="7b6c9-124">The budget type can't be changed after you change a record.</span></span>     
    > [!NOTE]
    > <span data-ttu-id="7b6c9-125">Hvis du endrer standard budsjettype, blir alle andre alternativer ikke tilgjengelig for oppdateringer, og du kan ikke bruke denne prognosemodellen på nytt.</span><span class="sxs-lookup"><span data-stu-id="7b6c9-125">If you change the default budget type, all other options will become unavailable for updates, and you can't reuse this forecast model.</span></span> 
   


 

