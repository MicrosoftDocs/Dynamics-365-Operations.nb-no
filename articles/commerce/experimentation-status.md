---
title: Se gjennom statusen for et eksperiment
description: Dette emnet beskriver hvilken status et eksperiment har i livssyklusen for eksperimentering i Dynamics 365 Commerce.
author: sushma-rao
manager: AnnBe
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: eea67ddc1718902198b74614ee1a910fc6e29c1d
ms.sourcegitcommit: cd83f2bc0e52e13071ad306e07e4c255fc65cb03
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/22/2020
ms.locfileid: "4414785"
---
# <a name="review-the-status-of-an-experiment"></a><span data-ttu-id="a08ff-103">Se gjennom statusen for et eksperiment</span><span class="sxs-lookup"><span data-stu-id="a08ff-103">Review the status of an experiment</span></span>
<span data-ttu-id="a08ff-104">Det er mange trinn i forbindelse med konfigurering og kjøring av et eksperiment i Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="a08ff-104">There are many steps involved in setting up and running an experiment in Dynamics 365 Commerce.</span></span> <span data-ttu-id="a08ff-105">Hvis du vil ha informasjon om livssyklusen for eksperimentering, kan du se [Eksperimentering i Dynamics 365 Commerce](experimentation-overview.md).</span><span class="sxs-lookup"><span data-stu-id="a08ff-105">For information about the experimentation lifecycle, see [Experimentation in Dynamics 365 Commerce](experimentation-overview.md).</span></span>

<span data-ttu-id="a08ff-106">Hvis du vil vite hvor et eksperimenter er i livssyklusen, velger du **Eksperimenter** i den venstre navisjonsruten i Commerce-områdebygger.</span><span class="sxs-lookup"><span data-stu-id="a08ff-106">To learn where an experiment is in the lifecycle, in Commerce site builder select **Experiments** in the left navigation pane.</span></span> <span data-ttu-id="a08ff-107">En liste over eksperimenter vises med statusen for hvert eksperiment i både Commerce og tredjepartstjenesten som brukes til å gjøre det mulig å opprette eksperimenter, tilordne variasjoner og analysere data.</span><span class="sxs-lookup"><span data-stu-id="a08ff-107">A list of experiments is displayed with the status of each experiment in both Commerce and the third-party service that is being used to enable the creation of experiments, assign variations, and analyze data.</span></span>

<span data-ttu-id="a08ff-108">I kolonnen **Commerce-status** kan du vise verdiene nedenfor.</span><span class="sxs-lookup"><span data-stu-id="a08ff-108">In the **Commerce status** column, the following values may be displayed.</span></span> 
- <span data-ttu-id="a08ff-109">**Utkast** – Eksperimentet er koblet til en side eller et fragment i Commerce og redigeres.</span><span class="sxs-lookup"><span data-stu-id="a08ff-109">**Draft** - The experiment is connected to a page or fragment in Commerce and is being edited.</span></span>
- <span data-ttu-id="a08ff-110">**Publisert** – Eksperimentvariasjonene er klare for visning på nettstedet.</span><span class="sxs-lookup"><span data-stu-id="a08ff-110">**Published** - The experiment variations are ready to be displayed on your website.</span></span> <span data-ttu-id="a08ff-111">Hvis eksperimentet kjører i tredjepartstjenesten, vil brukere av nettstedet se en variasjon av siden eller fragmentet som er valgt av tredjepartstjenesten.</span><span class="sxs-lookup"><span data-stu-id="a08ff-111">If the experiment is running in the third-party service, website users will see a variation of the page or fragment as selected by the third-party service.</span></span>
- <span data-ttu-id="a08ff-112">**Ikke publisert** – Eksperimentet er ikke lenger tilgjengelig på nettstedet.</span><span class="sxs-lookup"><span data-stu-id="a08ff-112">**Unpublished** - The experiment is no longer available on your website.</span></span> <span data-ttu-id="a08ff-113">Brukere av nettstedet ser bare standardversjonen av siden eller fragmentet selv om eksperimentet kjører i tredjepartstjenesten.</span><span class="sxs-lookup"><span data-stu-id="a08ff-113">Website users will only see the default version of the page or fragment even if the experiment is running in the third-party service.</span></span>
- <span data-ttu-id="a08ff-114">**Fullført** - Eksperimentet er fullført, og en variasjon ble fremmet til å være aktiv for alle brukere av nettstedet.</span><span class="sxs-lookup"><span data-stu-id="a08ff-114">**Completed** - The experiment has run its course and a variation was promoted to live for all website users.</span></span>

<span data-ttu-id="a08ff-115">På samme måte kan følgende verdier vises i kolonnen for **status for tredjepart** for å angi statusen for eksperimentene i tredjepartstjenesten.</span><span class="sxs-lookup"><span data-stu-id="a08ff-115">Similarly, in the **third-party status** column, the following values may be displayed to indicate what status the experiments are in the third-party service.</span></span>
- <span data-ttu-id="a08ff-116">**Utkast** – Eksperimentet er konfigurert i tredjepartstjenesten, men er ikke startet.</span><span class="sxs-lookup"><span data-stu-id="a08ff-116">**Draft** - The experiment is set up in the third-party service but hasn't been started.</span></span>
- <span data-ttu-id="a08ff-117">**Kjører** – Eksperimentet er startet i tredjepartstjenesten og samler inn data.</span><span class="sxs-lookup"><span data-stu-id="a08ff-117">**Running** - The experiment was started in the third-party service and is collecting data.</span></span>
- <span data-ttu-id="a08ff-118">**Stoppet midlertidig** – Eksperimentet er stoppet midlertidig og samler ikke inn data.</span><span class="sxs-lookup"><span data-stu-id="a08ff-118">**Paused** - The experiment is paused and not collecting data.</span></span> <span data-ttu-id="a08ff-119">Du må fortsette eksperimentet for at det skal fortsette å samle inn data.</span><span class="sxs-lookup"><span data-stu-id="a08ff-119">You must resume the experiment for it to collect data again.</span></span>
- <span data-ttu-id="a08ff-120">**Arkivert** – Eksperimentet er fullført, og det har blitt katalogisert i tredjepartstjenesten for fremtidig referanse.</span><span class="sxs-lookup"><span data-stu-id="a08ff-120">**Archived** - The experiment has run its course and has been cataloged in the third-party service for future reference.</span></span>

<span data-ttu-id="a08ff-121">Diagrammet nedenfor viser begge settene med statuser og hvordan de er relatert til hverandre.</span><span class="sxs-lookup"><span data-stu-id="a08ff-121">The diagram below shows both sets of statuses and how they relate to each other.</span></span>

<span data-ttu-id="a08ff-122">[ ![Statuser for eksperimentering](./media/experimentation_statuses.svg) ](./media/experimentation_statuses.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="a08ff-122">[ ![Experimentation statuses](./media/experimentation_statuses.svg) ](./media/experimentation_statuses.svg#lightbox)</span></span>
