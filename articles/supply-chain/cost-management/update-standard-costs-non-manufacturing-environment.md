---
title: "Oppdatere standardkostnader i et ikke-produksjonsmiljø"
description: "Denne artikkelen gir råd for å oppdatere standardkostnader i et ikke-produksjonsmiljø."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CostingVersion, InventItemPrice
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 79723
ms.assetid: 7ba0c408-2450-4042-9542-6fdf83c12e6c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 0386ca1e5e7bf6e578ba2abf1b2c9eefe4dd2a02
ms.contentlocale: nb-no
ms.lasthandoff: 11/03/2017

---

# <a name="update-standard-costs-in-a-non-manufacturing-environment"></a><span data-ttu-id="67093-103">Oppdatere standardkostnader i et ikke-produksjonsmiljø</span><span class="sxs-lookup"><span data-stu-id="67093-103">Update standard costs in a non-manufacturing environment</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="67093-104">Denne artikkelen gir råd for å oppdatere standardkostnader i et ikke-produksjonsmiljø.</span><span class="sxs-lookup"><span data-stu-id="67093-104">This article provides guidance for updating standard costs in a non-manufacturing environment.</span></span>

<span data-ttu-id="67093-105">Retningslinjene antar at du bruker en toversjons tilnærming til å oppdatere standardkostnad.</span><span class="sxs-lookup"><span data-stu-id="67093-105">The following guidelines assume that you use a two-version approach to update standard cost.</span></span> <span data-ttu-id="67093-106">I denne fremgangsmåten, inneholder én etterkalkuleringsversjon standardkostnader som opprinnelig ble definert for den frosne perioden, og den andre etterkalkuleringsversjonen inneholder de inkrementelle oppdateringene.</span><span class="sxs-lookup"><span data-stu-id="67093-106">In this approach, one costing version contains the standard costs that were originally defined for the frozen period, and the second costing version contains the incremental updates.</span></span> <span data-ttu-id="67093-107">Hver oppdatering angis som en kostnadspost som er vedlagt i den andre etterkalkuleringsversjonen, og til slutt den er aktivert.</span><span class="sxs-lookup"><span data-stu-id="67093-107">Each update is entered as a cost record that is enclosed in the second costing version, and eventually it's enabled.</span></span> <span data-ttu-id="67093-108">En alternativ fremgangsmåte med én versjon bruker settet med standardkostnader som opprinnelig var definert.</span><span class="sxs-lookup"><span data-stu-id="67093-108">An alternative, one-version approach uses the set of standard costs that was originally defined.</span></span> <span data-ttu-id="67093-109">Toversjonsmåten krever at du definerer enda en etterkalkuleringsversjon.</span><span class="sxs-lookup"><span data-stu-id="67093-109">The two-version approach requires that you define a second costing version.</span></span> <span data-ttu-id="67093-110">Her følger retningslinjene for å definere denne etterkalkuleringsversjonen:</span><span class="sxs-lookup"><span data-stu-id="67093-110">Here are the guidelines for defining this costing version:</span></span>

-   <span data-ttu-id="67093-111">Tilordne en etterkalkuleringstype for **standardkostnader**.</span><span class="sxs-lookup"><span data-stu-id="67093-111">Assign a costing type of **Standard costs**.</span></span>
-   <span data-ttu-id="67093-112">Tilordne en meningsfull identifikator som identifiserer innholdet i etterkalkuleringsversjonen, for eksempel **2016-OPPDATERINGER**.</span><span class="sxs-lookup"><span data-stu-id="67093-112">Assign a meaningful identifier that indicates the contents of the costing version, such as **2016-UPDATES**.</span></span>
-   <span data-ttu-id="67093-113">Kontroller at innholdet omfatter kostprisposter.</span><span class="sxs-lookup"><span data-stu-id="67093-113">Make sure that the content includes cost records.</span></span>
-   <span data-ttu-id="67093-114">Tillat innlegging av kostnadsposter for alle områder.</span><span class="sxs-lookup"><span data-stu-id="67093-114">Allow cost records to be entered for all sites.</span></span> <span data-ttu-id="67093-115">Hvis du angir et område, kan kostnadsposter angis bare for dette området.</span><span class="sxs-lookup"><span data-stu-id="67093-115">If you specify a site, cost records can be entered only for that site.</span></span>
-   <span data-ttu-id="67093-116">Angi tilbakefallsprinsippet **Ingen**.</span><span class="sxs-lookup"><span data-stu-id="67093-116">Indicate a fallback principle of **None**.</span></span> <span data-ttu-id="67093-117">Tilbakefallsprinsippet gjelder bare kostnadsberegninger for produserte varer.</span><span class="sxs-lookup"><span data-stu-id="67093-117">The fallback principle applies only to cost calculations for manufactured items.</span></span>

<span data-ttu-id="67093-118">Hvis du skal rette, justere eller oppdatere standardkostnader for mye varer, gjør du følgende.</span><span class="sxs-lookup"><span data-stu-id="67093-118">To correct, adjust, or update standard costs for new items, follow these steps.</span></span>

1.  <span data-ttu-id="67093-119">Bruk **Etterkalkuleringsversjon**-**oppsett**siden for å aktivere kostnadsdata som skal angis i den andre etterkalkuleringsversjonen.</span><span class="sxs-lookup"><span data-stu-id="67093-119">Use the **Costing version** **setup** page to enable cost data to be entered into the second costing version.</span></span> <span data-ttu-id="67093-120">Alternativt kan du forhindre aktiveringen av uavsluttede kostpriser, slik at aktiveringen vil bli tillatt etter at de uavsluttede kostprisene er fullført og korrekt definert.</span><span class="sxs-lookup"><span data-stu-id="67093-120">Optionally, prevent the activation of pending costs, so that activation will be allowed after pending costs have been completely and accurately defined.</span></span> <span data-ttu-id="67093-121">Du kan også angi en dato i **Fra dato**-feltet.</span><span class="sxs-lookup"><span data-stu-id="67093-121">You can also optionally enter a date in the **From date** field.</span></span> <span data-ttu-id="67093-122">Som en generell retningslinje kan du bruke datoen når du planlegger å aktivere de inkrementelle oppdateringene.</span><span class="sxs-lookup"><span data-stu-id="67093-122">As a general guideline, use the date when you intend to enable the incremental updates.</span></span> <span data-ttu-id="67093-123">Du kan også la **Fra dato**-feltet være tomt for etterkalkuleringsversjonen og angi en dato i **Fra dato**-feltet for hver kostnadsoppføring.</span><span class="sxs-lookup"><span data-stu-id="67093-123">Alternatively, leave the **From date** field blank for the costing version, and then enter a date in the **From date** field for each cost record.</span></span>
2.  <span data-ttu-id="67093-124">Bruk **Varepris**-siden for å angi oppdateringer som varekostnadsposter som er vedlagt i den andre etterkalkuleringsversjonen.</span><span class="sxs-lookup"><span data-stu-id="67093-124">Use the **Item price** page to enter updates as item cost records that are enclosed in the second costing version.</span></span>
3.  <span data-ttu-id="67093-125">Bruk **Varepriser**-rapporten for å bekrefte at varekostnadspostene som er vedlagt den andre etterkalkuleringsversjonen, er fullført og nøyaktige.</span><span class="sxs-lookup"><span data-stu-id="67093-125">Use the **Item prices** report to verify the completeness and accuracy of the item cost records that are enclosed in the second costing version.</span></span>
4.  <span data-ttu-id="67093-126">Bruk siden **Vedlikehold av etterkalkuleringsversjon** for å endre blokkeringsflagget for å tillate aktivering av ventende kostnadsposter som er vedlagt den andre etterkalkuleringsversjonen.</span><span class="sxs-lookup"><span data-stu-id="67093-126">Use the **Costing version maintenance** page to change the blocking flag to allow activation of the pending cost records that are enclosed in the second costing version.</span></span>
5.  <span data-ttu-id="67093-127">Bruk siden **Aktiver priser** (som du åpner fra siden **Vedlikehold av etterkalkuleringsversjon** for å aktivere alle ventende varekostnadsposter som er vedlagt den andre etterkalkuleringsversjonen.</span><span class="sxs-lookup"><span data-stu-id="67093-127">Use the **Activate prices** page (which you open from the **Costing version maintenance** page) to activate all pending item cost records that are enclosed in the second costing version.</span></span> <span data-ttu-id="67093-128">Du kan også aktivere de ventende kostnadspostene for enkelte varer ved å klikke knappen **Aktiver ventende pris** på **Varepris**-siden.</span><span class="sxs-lookup"><span data-stu-id="67093-128">You can also activate the pending cost records for individual items by clicking the **Activate pending price** button on the **Item price** page.</span></span>
6.  <span data-ttu-id="67093-129">For å unngå ytterligere datavedlikehold kan du bruke siden **Oppsett av etterkalkuleringsversjon** til å endre blokkeringsflaggene som er vedlagt den andre etterkalkuleringsversjonen.</span><span class="sxs-lookup"><span data-stu-id="67093-129">To prevent additional data maintenance, use the **Costing version setup** page to change the blocking flags that are enclosed in the second costing version.</span></span> <span data-ttu-id="67093-130">Blokkeringspolicyene forhindrer innlegging av nye uavsluttede kostnader og aktivering av uavsluttede kostpriser.</span><span class="sxs-lookup"><span data-stu-id="67093-130">The blocking policies will prevent the entry of new pending costs and the activation of pending costs.</span></span>





