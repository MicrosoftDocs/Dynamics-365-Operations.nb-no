---
title: Konfigurere ansattselvbetjening
description: ''
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
ms.openlocfilehash: e44a35071b8d0987e6c949fb11312204317b44a1
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010081"
---
# <a name="configure-employee-self-service"></a><span data-ttu-id="42eba-102">Konfigurere ansattselvbetjening</span><span class="sxs-lookup"><span data-stu-id="42eba-102">Configure employee self service</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="42eba-103">I Microsoft Dynamics 365 Human Resources kan du konfigurere fliser for navigasjon på øverste nivå i Ansattselvbetjening.</span><span class="sxs-lookup"><span data-stu-id="42eba-103">In Microsoft Dynamics 365 Human Resources, you can configure tiles for top-level navigation in Employee self service.</span></span> <span data-ttu-id="42eba-104">Fordelsplanfliser dirigerer brukere til fordelsplaner de er berettiget til å registrere seg i.</span><span class="sxs-lookup"><span data-stu-id="42eba-104">Benefit plan tiles direct users to benefit plans that they are eligible to enroll in.</span></span>

## <a name="set-up-a-role-center-tile"></a><span data-ttu-id="42eba-105">Definere en rollesenterflis</span><span class="sxs-lookup"><span data-stu-id="42eba-105">Set up a role center tile</span></span>

1. <span data-ttu-id="42eba-106">I arbeidsområdet **Fordelsbehandling**, under **Oppsett**, velger du **Parametere for Ansattselvbetjening**.</span><span class="sxs-lookup"><span data-stu-id="42eba-106">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="42eba-107">Velg kategorien **Oppsett av rollesenterflis**, og velg deretter **Ny**.</span><span class="sxs-lookup"><span data-stu-id="42eba-107">Select the **Role center tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="42eba-108">Angi verdier for de følgende feltene:</span><span class="sxs-lookup"><span data-stu-id="42eba-108">Specify values for the following fields:</span></span>

   | <span data-ttu-id="42eba-109">Felt</span><span class="sxs-lookup"><span data-stu-id="42eba-109">Field</span></span> | <span data-ttu-id="42eba-110">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="42eba-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="42eba-111">Flis-ID</span><span class="sxs-lookup"><span data-stu-id="42eba-111">Tile ID</span></span> | <span data-ttu-id="42eba-112">Den unike ID-en for flisen.</span><span class="sxs-lookup"><span data-stu-id="42eba-112">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="42eba-113">Etikettekst for flis</span><span class="sxs-lookup"><span data-stu-id="42eba-113">Tile label text</span></span> | <span data-ttu-id="42eba-114">Teksten som vises for flisen i selvbetjeningen.</span><span class="sxs-lookup"><span data-stu-id="42eba-114">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="42eba-115">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="42eba-115">Description</span></span> | <span data-ttu-id="42eba-116">En beskrivelse av flisen.</span><span class="sxs-lookup"><span data-stu-id="42eba-116">A description of the tile.</span></span> |
   | <span data-ttu-id="42eba-117">Internett-adresse</span><span class="sxs-lookup"><span data-stu-id="42eba-117">Internet address</span></span> | <span data-ttu-id="42eba-118">Skriv inn URL-adressen til siden Ansattselvbetjening.</span><span class="sxs-lookup"><span data-stu-id="42eba-118">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="42eba-119">Flisstørrelse</span><span class="sxs-lookup"><span data-stu-id="42eba-119">Tile size</span></span> | <span data-ttu-id="42eba-120">Størrelsen på flisen: liten, middels eller stor.</span><span class="sxs-lookup"><span data-stu-id="42eba-120">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="42eba-121">Mål</span><span class="sxs-lookup"><span data-stu-id="42eba-121">Target</span></span> | <span data-ttu-id="42eba-122">Angir om siden skal åpnes i et nytt vindu eller det gjeldende vinduet.</span><span class="sxs-lookup"><span data-stu-id="42eba-122">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="42eba-123">Bilde for flisbakgrunn</span><span class="sxs-lookup"><span data-stu-id="42eba-123">Tile background image</span></span> | <span data-ttu-id="42eba-124">URL-adressen for bildet som skal brukes for flisen (valgfritt).</span><span class="sxs-lookup"><span data-stu-id="42eba-124">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="42eba-125">Start</span><span class="sxs-lookup"><span data-stu-id="42eba-125">Start</span></span> | <span data-ttu-id="42eba-126">Startdatoen og klokkeslettet flisen skal være tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="42eba-126">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="42eba-127">End</span><span class="sxs-lookup"><span data-stu-id="42eba-127">End</span></span> | <span data-ttu-id="42eba-128">Sluttdatoen og klokkeslettet flisen skal være tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="42eba-128">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="42eba-129">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="42eba-129">Select **Save**.</span></span>

## <a name="set-up-a-benefit-plans-tile"></a><span data-ttu-id="42eba-130">Definere en fordelsplanflis</span><span class="sxs-lookup"><span data-stu-id="42eba-130">Set up a benefit plans tile</span></span>

1. <span data-ttu-id="42eba-131">I arbeidsområdet **Fordelsbehandling**, under **Oppsett**, velger du **Parametere for Ansattselvbetjening**.</span><span class="sxs-lookup"><span data-stu-id="42eba-131">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="42eba-132">Velg kategorien **Oppsett av fordelsplanflis**, og velg deretter **Ny**.</span><span class="sxs-lookup"><span data-stu-id="42eba-132">Select the **Benefit plans tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="42eba-133">Angi verdier for de følgende feltene:</span><span class="sxs-lookup"><span data-stu-id="42eba-133">Specify values for the following fields:</span></span>

   | <span data-ttu-id="42eba-134">Felt</span><span class="sxs-lookup"><span data-stu-id="42eba-134">Field</span></span> | <span data-ttu-id="42eba-135">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="42eba-135">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="42eba-136">Flis-ID</span><span class="sxs-lookup"><span data-stu-id="42eba-136">Tile ID</span></span> | <span data-ttu-id="42eba-137">Den unike ID-en for flisen.</span><span class="sxs-lookup"><span data-stu-id="42eba-137">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="42eba-138">Etikettekst for flis</span><span class="sxs-lookup"><span data-stu-id="42eba-138">Tile label text</span></span> | <span data-ttu-id="42eba-139">Teksten som vises for flisen i selvbetjeningen.</span><span class="sxs-lookup"><span data-stu-id="42eba-139">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="42eba-140">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="42eba-140">Description</span></span> | <span data-ttu-id="42eba-141">En beskrivelse av flisen.</span><span class="sxs-lookup"><span data-stu-id="42eba-141">A description of the tile.</span></span> |
   | <span data-ttu-id="42eba-142">Internett-adresse</span><span class="sxs-lookup"><span data-stu-id="42eba-142">Internet address</span></span> | <span data-ttu-id="42eba-143">Skriv inn URL-adressen til siden Ansattselvbetjening.</span><span class="sxs-lookup"><span data-stu-id="42eba-143">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="42eba-144">Flisstørrelse</span><span class="sxs-lookup"><span data-stu-id="42eba-144">Tile size</span></span> | <span data-ttu-id="42eba-145">Størrelsen på flisen: liten, middels eller stor.</span><span class="sxs-lookup"><span data-stu-id="42eba-145">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="42eba-146">Mål</span><span class="sxs-lookup"><span data-stu-id="42eba-146">Target</span></span> | <span data-ttu-id="42eba-147">Angir om siden skal åpnes i et nytt vindu eller det gjeldende vinduet.</span><span class="sxs-lookup"><span data-stu-id="42eba-147">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="42eba-148">Bilde for flisbakgrunn</span><span class="sxs-lookup"><span data-stu-id="42eba-148">Tile background image</span></span> | <span data-ttu-id="42eba-149">URL-adressen for bildet som skal brukes for flisen (valgfritt).</span><span class="sxs-lookup"><span data-stu-id="42eba-149">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="42eba-150">Start</span><span class="sxs-lookup"><span data-stu-id="42eba-150">Start</span></span> | <span data-ttu-id="42eba-151">Startdatoen og klokkeslettet flisen skal være tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="42eba-151">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="42eba-152">End</span><span class="sxs-lookup"><span data-stu-id="42eba-152">End</span></span> | <span data-ttu-id="42eba-153">Sluttdatoen og klokkeslettet flisen skal være tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="42eba-153">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="42eba-154">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="42eba-154">Select **Save**.</span></span>

## <a name="set-up-a-flex-credit-plan-tile"></a><span data-ttu-id="42eba-155">Definere en flis for fleksibel kredittplan</span><span class="sxs-lookup"><span data-stu-id="42eba-155">Set up a flex credit plan tile</span></span>

1. <span data-ttu-id="42eba-156">I arbeidsområdet **Fordelsbehandling**, under **Oppsett**, velger du **Parametere for Ansattselvbetjening**.</span><span class="sxs-lookup"><span data-stu-id="42eba-156">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="42eba-157">Velg kategorien **Oppsett av flis for fleksibel kredittplan**, og velg deretter **Ny**.</span><span class="sxs-lookup"><span data-stu-id="42eba-157">Select the **Flex credit plan tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="42eba-158">Angi verdier for de følgende feltene:</span><span class="sxs-lookup"><span data-stu-id="42eba-158">Specify values for the following fields:</span></span>

   | <span data-ttu-id="42eba-159">Felt</span><span class="sxs-lookup"><span data-stu-id="42eba-159">Field</span></span> | <span data-ttu-id="42eba-160">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="42eba-160">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="42eba-161">Flis-ID</span><span class="sxs-lookup"><span data-stu-id="42eba-161">Tile ID</span></span> | <span data-ttu-id="42eba-162">Den unike ID-en for flisen.</span><span class="sxs-lookup"><span data-stu-id="42eba-162">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="42eba-163">Etikettekst for flis</span><span class="sxs-lookup"><span data-stu-id="42eba-163">Tile label text</span></span> | <span data-ttu-id="42eba-164">Teksten som vises for flisen i selvbetjeningen.</span><span class="sxs-lookup"><span data-stu-id="42eba-164">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="42eba-165">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="42eba-165">Description</span></span> | <span data-ttu-id="42eba-166">En beskrivelse av flisen.</span><span class="sxs-lookup"><span data-stu-id="42eba-166">A description of the tile.</span></span> |
   | <span data-ttu-id="42eba-167">Internett-adresse</span><span class="sxs-lookup"><span data-stu-id="42eba-167">Internet address</span></span> | <span data-ttu-id="42eba-168">Skriv inn URL-adressen til siden Ansattselvbetjening.</span><span class="sxs-lookup"><span data-stu-id="42eba-168">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="42eba-169">Flisstørrelse</span><span class="sxs-lookup"><span data-stu-id="42eba-169">Tile size</span></span> | <span data-ttu-id="42eba-170">Størrelsen på flisen: liten, middels eller stor.</span><span class="sxs-lookup"><span data-stu-id="42eba-170">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="42eba-171">Mål</span><span class="sxs-lookup"><span data-stu-id="42eba-171">Target</span></span> | <span data-ttu-id="42eba-172">Angir om siden skal åpnes i et nytt vindu eller det gjeldende vinduet.</span><span class="sxs-lookup"><span data-stu-id="42eba-172">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="42eba-173">Bilde for flisbakgrunn</span><span class="sxs-lookup"><span data-stu-id="42eba-173">Tile background image</span></span> | <span data-ttu-id="42eba-174">URL-adressen for bildet som skal brukes for flisen (valgfritt).</span><span class="sxs-lookup"><span data-stu-id="42eba-174">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="42eba-175">Start</span><span class="sxs-lookup"><span data-stu-id="42eba-175">Start</span></span> | <span data-ttu-id="42eba-176">Startdatoen og klokkeslettet flisen skal være tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="42eba-176">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="42eba-177">End</span><span class="sxs-lookup"><span data-stu-id="42eba-177">End</span></span> | <span data-ttu-id="42eba-178">Sluttdatoen og klokkeslettet flisen skal være tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="42eba-178">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="42eba-179">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="42eba-179">Select **Save**.</span></span>
