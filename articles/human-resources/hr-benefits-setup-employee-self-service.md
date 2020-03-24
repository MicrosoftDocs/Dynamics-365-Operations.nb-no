---
title: Konfigurere selvbetjening for ansatte
description: I Microsoft Dynamics 365 Human Resources kan du konfigurere fliser for navigasjon på øverste nivå i Ansattselvbetjening.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 17918fc7b894929c92c54b59b7440ab8aef980bd
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092666"
---
# <a name="configure-employee-self-service"></a><span data-ttu-id="02716-103">Konfigurere selvbetjening for ansatte</span><span class="sxs-lookup"><span data-stu-id="02716-103">Configure employee self service</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="02716-104">I Microsoft Dynamics 365 Human Resources kan du konfigurere fliser for navigasjon på øverste nivå i Ansattselvbetjening.</span><span class="sxs-lookup"><span data-stu-id="02716-104">In Microsoft Dynamics 365 Human Resources, you can configure tiles for top-level navigation in Employee self service.</span></span> <span data-ttu-id="02716-105">Fordelsplanfliser dirigerer brukere til fordelsplaner de er berettiget til å registrere seg i.</span><span class="sxs-lookup"><span data-stu-id="02716-105">Benefit plan tiles direct users to benefit plans that they are eligible to enroll in.</span></span>

## <a name="set-up-a-role-center-tile"></a><span data-ttu-id="02716-106">Definere en rollesenterflis</span><span class="sxs-lookup"><span data-stu-id="02716-106">Set up a role center tile</span></span>

1. <span data-ttu-id="02716-107">I arbeidsområdet **Fordelsbehandling**, under **Oppsett**, velger du **Parametere for Ansattselvbetjening**.</span><span class="sxs-lookup"><span data-stu-id="02716-107">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="02716-108">Velg kategorien **Oppsett av rollesenterflis**, og velg deretter **Ny**.</span><span class="sxs-lookup"><span data-stu-id="02716-108">Select the **Role center tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="02716-109">Angi verdier for de følgende feltene:</span><span class="sxs-lookup"><span data-stu-id="02716-109">Specify values for the following fields:</span></span>

   | <span data-ttu-id="02716-110">Felt</span><span class="sxs-lookup"><span data-stu-id="02716-110">Field</span></span> | <span data-ttu-id="02716-111">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="02716-111">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="02716-112">Flis-ID</span><span class="sxs-lookup"><span data-stu-id="02716-112">Tile ID</span></span> | <span data-ttu-id="02716-113">Den unike ID-en for flisen.</span><span class="sxs-lookup"><span data-stu-id="02716-113">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="02716-114">Etikettekst for flis</span><span class="sxs-lookup"><span data-stu-id="02716-114">Tile label text</span></span> | <span data-ttu-id="02716-115">Teksten som vises for flisen i selvbetjeningen.</span><span class="sxs-lookup"><span data-stu-id="02716-115">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="02716-116">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="02716-116">Description</span></span> | <span data-ttu-id="02716-117">En beskrivelse av flisen.</span><span class="sxs-lookup"><span data-stu-id="02716-117">A description of the tile.</span></span> |
   | <span data-ttu-id="02716-118">Internett-adresse</span><span class="sxs-lookup"><span data-stu-id="02716-118">Internet address</span></span> | <span data-ttu-id="02716-119">Skriv inn URL-adressen til siden Ansattselvbetjening.</span><span class="sxs-lookup"><span data-stu-id="02716-119">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="02716-120">Flisstørrelse</span><span class="sxs-lookup"><span data-stu-id="02716-120">Tile size</span></span> | <span data-ttu-id="02716-121">Størrelsen på flisen: liten, middels eller stor.</span><span class="sxs-lookup"><span data-stu-id="02716-121">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="02716-122">Mål</span><span class="sxs-lookup"><span data-stu-id="02716-122">Target</span></span> | <span data-ttu-id="02716-123">Angir om siden skal åpnes i et nytt vindu eller det gjeldende vinduet.</span><span class="sxs-lookup"><span data-stu-id="02716-123">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="02716-124">Bilde for flisbakgrunn</span><span class="sxs-lookup"><span data-stu-id="02716-124">Tile background image</span></span> | <span data-ttu-id="02716-125">URL-adressen for bildet som skal brukes for flisen (valgfritt).</span><span class="sxs-lookup"><span data-stu-id="02716-125">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="02716-126">Start</span><span class="sxs-lookup"><span data-stu-id="02716-126">Start</span></span> | <span data-ttu-id="02716-127">Startdatoen og klokkeslettet flisen skal være tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="02716-127">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="02716-128">End</span><span class="sxs-lookup"><span data-stu-id="02716-128">End</span></span> | <span data-ttu-id="02716-129">Sluttdatoen og klokkeslettet flisen skal være tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="02716-129">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="02716-130">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="02716-130">Select **Save**.</span></span>

## <a name="set-up-a-benefit-plans-tile"></a><span data-ttu-id="02716-131">Definere en fordelsplanflis</span><span class="sxs-lookup"><span data-stu-id="02716-131">Set up a benefit plans tile</span></span>

1. <span data-ttu-id="02716-132">I arbeidsområdet **Fordelsbehandling**, under **Oppsett**, velger du **Parametere for Ansattselvbetjening**.</span><span class="sxs-lookup"><span data-stu-id="02716-132">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="02716-133">Velg kategorien **Oppsett av fordelsplanflis**, og velg deretter **Ny**.</span><span class="sxs-lookup"><span data-stu-id="02716-133">Select the **Benefit plans tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="02716-134">Angi verdier for de følgende feltene:</span><span class="sxs-lookup"><span data-stu-id="02716-134">Specify values for the following fields:</span></span>

   | <span data-ttu-id="02716-135">Felt</span><span class="sxs-lookup"><span data-stu-id="02716-135">Field</span></span> | <span data-ttu-id="02716-136">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="02716-136">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="02716-137">Flis-ID</span><span class="sxs-lookup"><span data-stu-id="02716-137">Tile ID</span></span> | <span data-ttu-id="02716-138">Den unike ID-en for flisen.</span><span class="sxs-lookup"><span data-stu-id="02716-138">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="02716-139">Etikettekst for flis</span><span class="sxs-lookup"><span data-stu-id="02716-139">Tile label text</span></span> | <span data-ttu-id="02716-140">Teksten som vises for flisen i selvbetjeningen.</span><span class="sxs-lookup"><span data-stu-id="02716-140">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="02716-141">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="02716-141">Description</span></span> | <span data-ttu-id="02716-142">En beskrivelse av flisen.</span><span class="sxs-lookup"><span data-stu-id="02716-142">A description of the tile.</span></span> |
   | <span data-ttu-id="02716-143">Internett-adresse</span><span class="sxs-lookup"><span data-stu-id="02716-143">Internet address</span></span> | <span data-ttu-id="02716-144">Skriv inn URL-adressen til siden Ansattselvbetjening.</span><span class="sxs-lookup"><span data-stu-id="02716-144">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="02716-145">Flisstørrelse</span><span class="sxs-lookup"><span data-stu-id="02716-145">Tile size</span></span> | <span data-ttu-id="02716-146">Størrelsen på flisen: liten, middels eller stor.</span><span class="sxs-lookup"><span data-stu-id="02716-146">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="02716-147">Mål</span><span class="sxs-lookup"><span data-stu-id="02716-147">Target</span></span> | <span data-ttu-id="02716-148">Angir om siden skal åpnes i et nytt vindu eller det gjeldende vinduet.</span><span class="sxs-lookup"><span data-stu-id="02716-148">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="02716-149">Bilde for flisbakgrunn</span><span class="sxs-lookup"><span data-stu-id="02716-149">Tile background image</span></span> | <span data-ttu-id="02716-150">URL-adressen for bildet som skal brukes for flisen (valgfritt).</span><span class="sxs-lookup"><span data-stu-id="02716-150">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="02716-151">Start</span><span class="sxs-lookup"><span data-stu-id="02716-151">Start</span></span> | <span data-ttu-id="02716-152">Startdatoen og klokkeslettet flisen skal være tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="02716-152">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="02716-153">End</span><span class="sxs-lookup"><span data-stu-id="02716-153">End</span></span> | <span data-ttu-id="02716-154">Sluttdatoen og klokkeslettet flisen skal være tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="02716-154">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="02716-155">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="02716-155">Select **Save**.</span></span>

## <a name="set-up-a-flex-credit-plan-tile"></a><span data-ttu-id="02716-156">Definere en flis for fleksibel kredittplan</span><span class="sxs-lookup"><span data-stu-id="02716-156">Set up a flex credit plan tile</span></span>

1. <span data-ttu-id="02716-157">I arbeidsområdet **Fordelsbehandling**, under **Oppsett**, velger du **Parametere for Ansattselvbetjening**.</span><span class="sxs-lookup"><span data-stu-id="02716-157">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="02716-158">Velg kategorien **Oppsett av flis for fleksibel kredittplan**, og velg deretter **Ny**.</span><span class="sxs-lookup"><span data-stu-id="02716-158">Select the **Flex credit plan tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="02716-159">Angi verdier for de følgende feltene:</span><span class="sxs-lookup"><span data-stu-id="02716-159">Specify values for the following fields:</span></span>

   | <span data-ttu-id="02716-160">Felt</span><span class="sxs-lookup"><span data-stu-id="02716-160">Field</span></span> | <span data-ttu-id="02716-161">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="02716-161">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="02716-162">Flis-ID</span><span class="sxs-lookup"><span data-stu-id="02716-162">Tile ID</span></span> | <span data-ttu-id="02716-163">Den unike ID-en for flisen.</span><span class="sxs-lookup"><span data-stu-id="02716-163">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="02716-164">Etikettekst for flis</span><span class="sxs-lookup"><span data-stu-id="02716-164">Tile label text</span></span> | <span data-ttu-id="02716-165">Teksten som vises for flisen i selvbetjeningen.</span><span class="sxs-lookup"><span data-stu-id="02716-165">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="02716-166">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="02716-166">Description</span></span> | <span data-ttu-id="02716-167">En beskrivelse av flisen.</span><span class="sxs-lookup"><span data-stu-id="02716-167">A description of the tile.</span></span> |
   | <span data-ttu-id="02716-168">Internett-adresse</span><span class="sxs-lookup"><span data-stu-id="02716-168">Internet address</span></span> | <span data-ttu-id="02716-169">Skriv inn URL-adressen til siden Ansattselvbetjening.</span><span class="sxs-lookup"><span data-stu-id="02716-169">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="02716-170">Flisstørrelse</span><span class="sxs-lookup"><span data-stu-id="02716-170">Tile size</span></span> | <span data-ttu-id="02716-171">Størrelsen på flisen: liten, middels eller stor.</span><span class="sxs-lookup"><span data-stu-id="02716-171">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="02716-172">Mål</span><span class="sxs-lookup"><span data-stu-id="02716-172">Target</span></span> | <span data-ttu-id="02716-173">Angir om siden skal åpnes i et nytt vindu eller det gjeldende vinduet.</span><span class="sxs-lookup"><span data-stu-id="02716-173">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="02716-174">Bilde for flisbakgrunn</span><span class="sxs-lookup"><span data-stu-id="02716-174">Tile background image</span></span> | <span data-ttu-id="02716-175">URL-adressen for bildet som skal brukes for flisen (valgfritt).</span><span class="sxs-lookup"><span data-stu-id="02716-175">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="02716-176">Start</span><span class="sxs-lookup"><span data-stu-id="02716-176">Start</span></span> | <span data-ttu-id="02716-177">Startdatoen og klokkeslettet flisen skal være tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="02716-177">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="02716-178">End</span><span class="sxs-lookup"><span data-stu-id="02716-178">End</span></span> | <span data-ttu-id="02716-179">Sluttdatoen og klokkeslettet flisen skal være tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="02716-179">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="02716-180">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="02716-180">Select **Save**.</span></span>
