---
title: Konfigurere selvbetjening for ansatte
description: I Microsoft Dynamics 365 Human Resources kan du konfigurere fliser for navigasjon på øverste nivå i Ansattselvbetjening.
author: andreabichsel
manager: tfehr
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c4fe8f7afd4b77636ce77e58a2e75196fddae132
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/17/2021
ms.locfileid: "5466116"
---
# <a name="configure-employee-self-service"></a><span data-ttu-id="f9e6f-103">Konfigurere selvbetjening for ansatte</span><span class="sxs-lookup"><span data-stu-id="f9e6f-103">Configure employee self service</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="f9e6f-104">I Microsoft Dynamics 365 Human Resources kan du konfigurere fliser for navigasjon på øverste nivå i Ansattselvbetjening.</span><span class="sxs-lookup"><span data-stu-id="f9e6f-104">In Microsoft Dynamics 365 Human Resources, you can configure tiles for top-level navigation in Employee self service.</span></span> <span data-ttu-id="f9e6f-105">Fordelsplanfliser dirigerer brukere til fordelsplaner de er berettiget for.</span><span class="sxs-lookup"><span data-stu-id="f9e6f-105">Benefit plan tiles direct users to benefit plans that they're eligible for.</span></span>

## <a name="set-up-a-benefit-plans-tile"></a><span data-ttu-id="f9e6f-106">Definere en fordelsplanflis</span><span class="sxs-lookup"><span data-stu-id="f9e6f-106">Set up a benefit plans tile</span></span>

1. <span data-ttu-id="f9e6f-107">I arbeidsområdet **Fordelsbehandling**, under **Oppsett**, velger du **Parametere for Ansattselvbetjening**.</span><span class="sxs-lookup"><span data-stu-id="f9e6f-107">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="f9e6f-108">Velg kategorien **Oppsett av fordelsplanflis**, og velg deretter **Ny**.</span><span class="sxs-lookup"><span data-stu-id="f9e6f-108">Select the **Benefit plans tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="f9e6f-109">Angi verdier for de følgende feltene:</span><span class="sxs-lookup"><span data-stu-id="f9e6f-109">Specify values for the following fields:</span></span>

   | <span data-ttu-id="f9e6f-110">Felt</span><span class="sxs-lookup"><span data-stu-id="f9e6f-110">Field</span></span> | <span data-ttu-id="f9e6f-111">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="f9e6f-111">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="f9e6f-112">**Flis-ID**</span><span class="sxs-lookup"><span data-stu-id="f9e6f-112">**Tile ID**</span></span> | <span data-ttu-id="f9e6f-113">Den unike ID-en for flisen.</span><span class="sxs-lookup"><span data-stu-id="f9e6f-113">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="f9e6f-114">**Etikettekst for flis**</span><span class="sxs-lookup"><span data-stu-id="f9e6f-114">**Tile label text**</span></span> | <span data-ttu-id="f9e6f-115">Teksten som vises for flisen i selvbetjeningen.</span><span class="sxs-lookup"><span data-stu-id="f9e6f-115">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="f9e6f-116">**Beskrivelse**</span><span class="sxs-lookup"><span data-stu-id="f9e6f-116">**Description**</span></span> | <span data-ttu-id="f9e6f-117">En beskrivelse av flisen.</span><span class="sxs-lookup"><span data-stu-id="f9e6f-117">A description of the tile.</span></span> |
   | <span data-ttu-id="f9e6f-118">**Internett-adresse**</span><span class="sxs-lookup"><span data-stu-id="f9e6f-118">**Internet address**</span></span> | <span data-ttu-id="f9e6f-119">Skriv inn URL-adressen til siden Ansattselvbetjening.</span><span class="sxs-lookup"><span data-stu-id="f9e6f-119">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="f9e6f-120">**Flisstørrelse**</span><span class="sxs-lookup"><span data-stu-id="f9e6f-120">**Tile size**</span></span> | <span data-ttu-id="f9e6f-121">Størrelsen på flisen: liten, middels eller stor.</span><span class="sxs-lookup"><span data-stu-id="f9e6f-121">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="f9e6f-122">**Mål**</span><span class="sxs-lookup"><span data-stu-id="f9e6f-122">**Target**</span></span> | <span data-ttu-id="f9e6f-123">Angir om siden skal åpnes i et nytt vindu eller det gjeldende vinduet.</span><span class="sxs-lookup"><span data-stu-id="f9e6f-123">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="f9e6f-124">**Bilde for flisbakgrunn**</span><span class="sxs-lookup"><span data-stu-id="f9e6f-124">**Tile background image**</span></span> | <span data-ttu-id="f9e6f-125">URL-adressen for bildet som skal brukes for flisen (valgfritt).</span><span class="sxs-lookup"><span data-stu-id="f9e6f-125">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="f9e6f-126">**Start**</span><span class="sxs-lookup"><span data-stu-id="f9e6f-126">**Start**</span></span> | <span data-ttu-id="f9e6f-127">Startdatoen og klokkeslettet flisen skal være tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="f9e6f-127">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="f9e6f-128">**End**</span><span class="sxs-lookup"><span data-stu-id="f9e6f-128">**End**</span></span> | <span data-ttu-id="f9e6f-129">Sluttdatoen og klokkeslettet flisen skal være tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="f9e6f-129">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="f9e6f-130">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="f9e6f-130">Select **Save**.</span></span>

## <a name="set-up-a-flex-credit-plan-tile"></a><span data-ttu-id="f9e6f-131">Definere en flis for fleksibel kredittplan</span><span class="sxs-lookup"><span data-stu-id="f9e6f-131">Set up a flex credit plan tile</span></span>

1. <span data-ttu-id="f9e6f-132">I arbeidsområdet **Fordelsbehandling**, under **Oppsett**, velger du **Parametere for Ansattselvbetjening**.</span><span class="sxs-lookup"><span data-stu-id="f9e6f-132">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="f9e6f-133">Velg kategorien **Oppsett av flis for fleksibel kredittplan**, og velg deretter **Ny**.</span><span class="sxs-lookup"><span data-stu-id="f9e6f-133">Select the **Flex credit plan tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="f9e6f-134">Angi verdier for de følgende feltene:</span><span class="sxs-lookup"><span data-stu-id="f9e6f-134">Specify values for the following fields:</span></span>

   | <span data-ttu-id="f9e6f-135">Felt</span><span class="sxs-lookup"><span data-stu-id="f9e6f-135">Field</span></span> | <span data-ttu-id="f9e6f-136">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="f9e6f-136">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="f9e6f-137">**Flis-ID**</span><span class="sxs-lookup"><span data-stu-id="f9e6f-137">**Tile ID**</span></span> | <span data-ttu-id="f9e6f-138">Den unike ID-en for flisen.</span><span class="sxs-lookup"><span data-stu-id="f9e6f-138">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="f9e6f-139">**Etikettekst for flis**</span><span class="sxs-lookup"><span data-stu-id="f9e6f-139">**Tile label text**</span></span> | <span data-ttu-id="f9e6f-140">Teksten som vises for flisen i selvbetjeningen.</span><span class="sxs-lookup"><span data-stu-id="f9e6f-140">The text that will appear for the tile on Self service.</span></span> |
   | <span data-ttu-id="f9e6f-141">**Beskrivelse**</span><span class="sxs-lookup"><span data-stu-id="f9e6f-141">**Description**</span></span> | <span data-ttu-id="f9e6f-142">En beskrivelse av flisen.</span><span class="sxs-lookup"><span data-stu-id="f9e6f-142">A description of the tile.</span></span> |
   | <span data-ttu-id="f9e6f-143">**Internett-adresse**</span><span class="sxs-lookup"><span data-stu-id="f9e6f-143">**Internet address**</span></span> | <span data-ttu-id="f9e6f-144">Skriv inn URL-adressen til siden Ansattselvbetjening.</span><span class="sxs-lookup"><span data-stu-id="f9e6f-144">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="f9e6f-145">**Flisstørrelse**</span><span class="sxs-lookup"><span data-stu-id="f9e6f-145">**Tile size**</span></span> | <span data-ttu-id="f9e6f-146">Størrelsen på flisen: liten, middels eller stor.</span><span class="sxs-lookup"><span data-stu-id="f9e6f-146">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="f9e6f-147">**Mål**</span><span class="sxs-lookup"><span data-stu-id="f9e6f-147">**Target**</span></span> | <span data-ttu-id="f9e6f-148">Angir om siden skal åpnes i et nytt vindu eller det gjeldende vinduet.</span><span class="sxs-lookup"><span data-stu-id="f9e6f-148">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="f9e6f-149">**Bilde for flisbakgrunn**</span><span class="sxs-lookup"><span data-stu-id="f9e6f-149">**Tile background image**</span></span> | <span data-ttu-id="f9e6f-150">URL-adressen for bildet som skal brukes for flisen (valgfritt).</span><span class="sxs-lookup"><span data-stu-id="f9e6f-150">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="f9e6f-151">**Start**</span><span class="sxs-lookup"><span data-stu-id="f9e6f-151">**Start**</span></span> | <span data-ttu-id="f9e6f-152">Startdatoen og klokkeslettet flisen skal være tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="f9e6f-152">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="f9e6f-153">**End**</span><span class="sxs-lookup"><span data-stu-id="f9e6f-153">**End**</span></span> | <span data-ttu-id="f9e6f-154">Sluttdatoen og klokkeslettet flisen skal være tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="f9e6f-154">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="f9e6f-155">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="f9e6f-155">Select **Save**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]