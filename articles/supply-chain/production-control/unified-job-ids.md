---
title: Enhetlig nummerserie for jobb-ID-er
description: Denne funksjonen gir en enkelt, felles nummerserie som genererer jobb-ID-er for produksjonskontrollen, produksjonsutførelsen og tids- og fremmøtemodulene.
author: johanhoffmann
ms.date: 03/25/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-03-05
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 00212803c46d898a39eafbc5c62016eb829535e2
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5824948"
---
# <a name="unified-number-sequence-for-job-ids"></a><span data-ttu-id="40537-103">Enhetlig nummerserie for jobb-ID-er</span><span class="sxs-lookup"><span data-stu-id="40537-103">Unified number sequence for job IDs</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="40537-104">Denne funksjonen gir en enkelt, felles nummerserie som genererer jobb-ID-er for produksjonskontrollen, produksjonsutførelsen og tids- og fremmøtemodulene.</span><span class="sxs-lookup"><span data-stu-id="40537-104">This feature provides a single, unified number sequence that generates job IDs for the Production control, Manufacturing execution, and Time and attendance modules.</span></span> <span data-ttu-id="40537-105">Tidligere kunne du velge en forskjellig nummerserie for hver av disse modulene, noe som kunne føre til konflikt mellom jobb-ID-er hvis to eller flere av disse sekvensene brukte et identisk format.</span><span class="sxs-lookup"><span data-stu-id="40537-105">Previously, you were able to choose a different number sequence for each of these modules, which could result in conflicting job IDs if two or more of these sequences used an identical format.</span></span> <span data-ttu-id="40537-106">En slik konflikt kan føre til at data blir skadet.</span><span class="sxs-lookup"><span data-stu-id="40537-106">Such a conflict can cause data corruption.</span></span>

## <a name="turn-on-this-feature-for-your-system"></a><span data-ttu-id="40537-107">Aktivere denne funksjonen for systemet</span><span class="sxs-lookup"><span data-stu-id="40537-107">Turn on this feature for your system</span></span>

<span data-ttu-id="40537-108">Hvis systemet ikke allerede inneholder funksjonen som er beskrevet i dette emnet, kan du gå til [Funksjonsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) og aktivere funksjonen *Enhetlig nummerserie for jobb-ID-er*.</span><span class="sxs-lookup"><span data-stu-id="40537-108">If your system doesn't already include the feature described in this topic, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) and turn on the *Unified number sequence for job IDs* feature.</span></span>

## <a name="set-up-the-unified-number-sequence-for-job-ids"></a><span data-ttu-id="40537-109">Konfigurer den enhetlige nummerserien for jobb-ID-er</span><span class="sxs-lookup"><span data-stu-id="40537-109">Set up the unified number sequence for job IDs</span></span>

<span data-ttu-id="40537-110">Når denne funksjonen er aktivert, vil de eksisterende **Jobbidentifikasjon**-nummersekvensinnstillingene på parametersiden for modulene Produksjonskontroll, Produksjonsutførelse og Tid og fremmøte bli avskrevet, og et nytt felt, **Enhetlig jobb-ID**, blir lagt til.</span><span class="sxs-lookup"><span data-stu-id="40537-110">After enabling this feature, the existing **Job identification** number-sequence settings located on the parameters pages for the Production control, Manufacturing execution, and Time and attendance modules will be deprecated and a new **Unified job ID** field will be added.</span></span> <span data-ttu-id="40537-111">Verdien for **Enhetlig jobb-ID** deles av alle de tre modulene, slik at alle modulene refererer til samme nummerserie.</span><span class="sxs-lookup"><span data-stu-id="40537-111">The **Unified job ID** value is shared by all three modules, thus ensuring that all modules reference the same number sequence.</span></span> <span data-ttu-id="40537-112">Jobb-ID-er vil derfor være unike i alle de tre modulene, og det vil aldri oppstå en konflikt.</span><span class="sxs-lookup"><span data-stu-id="40537-112">Job IDs will therefore be unique across all three modules and a conflict will never occur.</span></span>

<span data-ttu-id="40537-113">Slik konfigurerer du den enhetlige nummerserien for jobb-ID-er:</span><span class="sxs-lookup"><span data-stu-id="40537-113">To set up the unified number sequence for job IDs:</span></span>

1. <span data-ttu-id="40537-114">Slå på funksjonen som beskrevet i den forrige delen.</span><span class="sxs-lookup"><span data-stu-id="40537-114">Turn on the feature as described in the previous section.</span></span>
1. <span data-ttu-id="40537-115">Du kan enten identifisere nummerserien du vil bruke for de enhetlige jobb-ID-ene, eller opprette en ny.</span><span class="sxs-lookup"><span data-stu-id="40537-115">Either identify the number sequence you want to use for your unified job IDs, or create a new one.</span></span> <span data-ttu-id="40537-116">Hvis du vil ha mer informasjon, kan du se [Oversikt over nummerserier](../../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md).</span><span class="sxs-lookup"><span data-stu-id="40537-116">For more information, see [Number sequences overview](../../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md).</span></span>
1. <span data-ttu-id="40537-117">Gå til siden **Parametere for produksjonskontroll**, **Parametere for produksjonsutførelse** eller **Parametere for timeregistrering**.</span><span class="sxs-lookup"><span data-stu-id="40537-117">Go to the **Production control parameters**, **Manufacturing execution parameters**, or **Time and attendance parameters** page.</span></span> <span data-ttu-id="40537-118">Det har ingen betydning hvilken du velger, fordi når du angir denne innstillingen på en av disse sidene, vil alle de andre sidene oppdateres automatisk.</span><span class="sxs-lookup"><span data-stu-id="40537-118">It doesn't matter which one you choose because when you make this setting on any of those pages, all of the other pages will update automatically.</span></span>
1. <span data-ttu-id="40537-119">Åpne **Nummerserier**-fanen på den valgte parametersiden.</span><span class="sxs-lookup"><span data-stu-id="40537-119">Open the **Number sequences** tab on your selected parameters page.</span></span>
1. <span data-ttu-id="40537-120">Tilordne **nummerseriekoden** som du identifiserte tidligere, til raden **Enhetlige jobb-ID-er** i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="40537-120">Assign the **Number sequence code** that you identified previously to the **Unified job IDs** row of the grid.</span></span>
