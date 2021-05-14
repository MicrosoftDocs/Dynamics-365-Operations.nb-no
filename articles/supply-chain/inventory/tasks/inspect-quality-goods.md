---
title: Kontrollere varekvaliteten
description: Dette emnet beskriver hvordan du behandler kvalitetsordre.
author: perlynne
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventQualityOrderTable, InventQualityOrderLineResults, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ec67e7864db12178c0f3cfe8b93d510a46e8a0d4
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956140"
---
# <a name="inspect-the-quality-of-goods"></a><span data-ttu-id="d0a84-103">Kontrollere varekvaliteten</span><span class="sxs-lookup"><span data-stu-id="d0a84-103">Inspect the quality of goods</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d0a84-104">Dette emnet beskriver hvordan du behandler kvalitetsordre.</span><span class="sxs-lookup"><span data-stu-id="d0a84-104">This topic describes how to process quality orders.</span></span> <span data-ttu-id="d0a84-105">Kvalitetsinspeksjoner utføres vanligvis av en kvalitetsassistent.</span><span class="sxs-lookup"><span data-stu-id="d0a84-105">Quality inspections are typically done by a quality clerk.</span></span>

<span data-ttu-id="d0a84-106">Hvis standard demodata er installert, kan du bruke dem til å fullføre prosedyrene i dette emnet.</span><span class="sxs-lookup"><span data-stu-id="d0a84-106">If the standard demo data is installed, you can use it to complete the procedures in this topic.</span></span> <span data-ttu-id="d0a84-107">For å bruke demodata velger du den juridiske enheten *USMF* før du begynner.</span><span class="sxs-lookup"><span data-stu-id="d0a84-107">To use the demo data, select the *USMF* legal entity before you begin.</span></span> <span data-ttu-id="d0a84-108">Deretter må du bekrefte bestillingen *000016* og postere et produktmottak.</span><span class="sxs-lookup"><span data-stu-id="d0a84-108">You must then confirm purchase order *000016* and post a product receipt.</span></span> <span data-ttu-id="d0a84-109">En kvalitetsordre genereres automatisk.</span><span class="sxs-lookup"><span data-stu-id="d0a84-109">A quality order is automatically generated.</span></span>

## <a name="step-1-select-a-quality-order"></a><span data-ttu-id="d0a84-110">Trinn 1: Velge en kvalitetsordre</span><span class="sxs-lookup"><span data-stu-id="d0a84-110">Step 1: Select a quality order</span></span>

<span data-ttu-id="d0a84-111">For å velge en kvalitetsordre følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="d0a84-111">To select a quality order, follow these steps.</span></span>

1. <span data-ttu-id="d0a84-112">Gå til **Lagerstyring \> Periodiske oppgaver \> Kvalitetsstyring \> Kvalitetsordrer**.</span><span class="sxs-lookup"><span data-stu-id="d0a84-112">Go to **Inventory management \> Periodic tasks \> Quality management \> Quality orders**.</span></span>
1. <span data-ttu-id="d0a84-113">Velg kvalitetsordren som ble generert før du startet denne prosedyren.</span><span class="sxs-lookup"><span data-stu-id="d0a84-113">Select the quality order that was generated before you started this procedure.</span></span>

## <a name="step-2-record-test-results"></a><span data-ttu-id="d0a84-114">Trinn 2: Registere testresultater</span><span class="sxs-lookup"><span data-stu-id="d0a84-114">Step 2: Record test results</span></span>

<span data-ttu-id="d0a84-115">Følg disse trinnene for å registrere testresultater.</span><span class="sxs-lookup"><span data-stu-id="d0a84-115">To record test results, follow these steps.</span></span>

1. <span data-ttu-id="d0a84-116">Velg **Resultater**.</span><span class="sxs-lookup"><span data-stu-id="d0a84-116">Select **Results**.</span></span>
1. <span data-ttu-id="d0a84-117">Velg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="d0a84-117">Select **Edit**.</span></span>
1. <span data-ttu-id="d0a84-118">Angi et tall i **Resultatantall**-feltet.</span><span class="sxs-lookup"><span data-stu-id="d0a84-118">In the **Result quantity** field, enter a number.</span></span>
1. <span data-ttu-id="d0a84-119">Velg ønsket oppføring i feltet **Resultat**.</span><span class="sxs-lookup"><span data-stu-id="d0a84-119">In the **Outcome** field, select the desired record.</span></span> <span data-ttu-id="d0a84-120">I dette eksemplet er resultatet basert på et forhåndsdefinert resultat.</span><span class="sxs-lookup"><span data-stu-id="d0a84-120">In this example, the result is based on a predefined outcome.</span></span> <span data-ttu-id="d0a84-121">Vanligvis vil du registrere et mer spesifikt testresultat, for eksempel en størrelse eller annen dimensjon.</span><span class="sxs-lookup"><span data-stu-id="d0a84-121">Usually, you will record a more specific test result, such as a size or other dimension.</span></span>
1. <span data-ttu-id="d0a84-122">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="d0a84-122">Select **Save**.</span></span>
1. <span data-ttu-id="d0a84-123">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="d0a84-123">Close the page.</span></span>

## <a name="step-3-validate-the-quality-order"></a><span data-ttu-id="d0a84-124">Trinn 3: Valider kvalitetsordren</span><span class="sxs-lookup"><span data-stu-id="d0a84-124">Step 3: Validate the quality order</span></span>

<span data-ttu-id="d0a84-125">For å validere kvalitetsordren følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="d0a84-125">To validate the quality order, follow these steps.</span></span>

1. <span data-ttu-id="d0a84-126">Velg **Valider**.</span><span class="sxs-lookup"><span data-stu-id="d0a84-126">Select **Validate**.</span></span>
1. <span data-ttu-id="d0a84-127">Velg brukeren som gjennomfører inspeksjonen, i feltet **Godkjent av**.</span><span class="sxs-lookup"><span data-stu-id="d0a84-127">In the **Validated by** field, select the user who is doing the inspection.</span></span>
1. <span data-ttu-id="d0a84-128">Velg **Velg**.</span><span class="sxs-lookup"><span data-stu-id="d0a84-128">Select **Select**.</span></span>
1. <span data-ttu-id="d0a84-129">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="d0a84-129">Select **OK**.</span></span>
1. <span data-ttu-id="d0a84-130">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="d0a84-130">Close the page.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
