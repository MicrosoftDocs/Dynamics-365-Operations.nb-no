---
title: Feilsøke planleggingsoptimalisering
description: Dette emnet beskriver hvordan du løser problemer som kan oppstå mens du arbeider med planleggingsoptimalisering.
author: ChristianRytt
ms.date: 05/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-5-7
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 2100235fadabe6af87849aab7d9ec55d85ea66fa
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5812889"
---
# <a name="troubleshoot-planning-optimization"></a><span data-ttu-id="5bce1-103">Feilsøke planleggingsoptimalisering</span><span class="sxs-lookup"><span data-stu-id="5bce1-103">Troubleshoot Planning Optimization</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5bce1-104">Dette emnet beskriver hvordan du løser vanlige problemer som kan oppstå mens du arbeider med planleggingsoptimalisering.</span><span class="sxs-lookup"><span data-stu-id="5bce1-104">This topic describes how to fix common issues that you might encounter while working with Planning Optimization.</span></span>

## <a name="installation-of-the-planning-optimization-add-in-doesnt-complete"></a><span data-ttu-id="5bce1-105">Installasjon av tillegget for planleggingsoptimaliseringen fullføres ikke</span><span class="sxs-lookup"><span data-stu-id="5bce1-105">Installation of the Planning Optimization add-in doesn't complete</span></span>

<span data-ttu-id="5bce1-106">Planleggingsoptimalisering krever at et LCS-miljø (Lifecycle Services) er aktivert med høy tilgjengelighet, lag 2 eller høyere (ikke et OneBox-miljø), med Dynamics 365 Supply Chain Management versjon 10.0.7 eller nyere.</span><span class="sxs-lookup"><span data-stu-id="5bce1-106">Planning Optimization requires a Lifecycle Services (LCS) enabled, high-availability environment, tier 2 or higher (not a OneBox environment), with Dynamics 365 Supply Chain Management version 10.0.7 or later.</span></span> <span data-ttu-id="5bce1-107">Hvis du prøver å installere tillegget i et OneBox-miljø, vil ikke installasjonen fullføres.</span><span class="sxs-lookup"><span data-stu-id="5bce1-107">If you try to install the add-in on a OneBox environment, the installation won't complete.</span></span>

<span data-ttu-id="5bce1-108">**Løsning**: Avbryt installasjonen og bruk et miljø med høy tilgjengelighet, lag 2 eller høyere (ikke et Onebox-miljø).</span><span class="sxs-lookup"><span data-stu-id="5bce1-108">**Fix**: Cancel the installation and use a high-availability environment, tier 2 or higher (not a OneBox environment).</span></span>

## <a name="planning-of-batch-jobs-fails-when-planning-optimization-is-enabled"></a><span data-ttu-id="5bce1-109">Planlegging av satsvise jobber mislykkes når planleggingsoptimalisering aktiveres</span><span class="sxs-lookup"><span data-stu-id="5bce1-109">Planning of batch jobs fails when Planning Optimization is enabled</span></span>

<span data-ttu-id="5bce1-110">Når du aktiverer planleggingsoptimalisering, deaktiveres den innebygde hovedplanleggingsmotoren automatisk.</span><span class="sxs-lookup"><span data-stu-id="5bce1-110">When you enable Planning Optimization, the built-in master planning engine is automatically disabled.</span></span> <span data-ttu-id="5bce1-111">Satsvise jobber for hovedplanlegging som ble opprettet for den innebygde planleggingsmotoren i Supply Chain Management, vil mislykkes hvis de blir utløst mens planleggingsoptimalisering er aktivert.</span><span class="sxs-lookup"><span data-stu-id="5bce1-111">Master planning batch jobs that were created for the built-in Supply Chain Management planning engine will fail if they are triggered while Planning Optimization is enabled.</span></span> <span data-ttu-id="5bce1-112">Du kan få en feilmelding, for eksempel *Denne operasjonen utløste hovedplanlegging som ikke støttes når planleggingsoptimalisering er aktivert*.</span><span class="sxs-lookup"><span data-stu-id="5bce1-112">You may receive an error message such as *This operation triggered master planning that isn't supported when Planning Optimization is enabled*.</span></span>

<span data-ttu-id="5bce1-113">**Løsning**: Avbryt alle satsvise jobber for hovedplanlegging som ble opprettet for den innebygde planleggingsmotoren for Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="5bce1-113">**Fix**: Cancel all master planning batch jobs that were created for the built-in Supply Chain Management planning engine.</span></span>

## <a name="planning-optimization-results-are-different-from-earlier-results"></a><span data-ttu-id="5bce1-114">Resultatene av planleggingsoptimalisering er forskjellige fra tidligere resultater</span><span class="sxs-lookup"><span data-stu-id="5bce1-114">Planning Optimization results are different from earlier results</span></span>

<span data-ttu-id="5bce1-115">Planleggingsoptimalisering er forskjellig fra den innebygde hovedplanleggingsutformingen i noen områder.</span><span class="sxs-lookup"><span data-stu-id="5bce1-115">Planning Optimization differs from the built-in master planning design in some areas.</span></span> <span data-ttu-id="5bce1-116">Dette kan også skyldes ventende funksjoner.</span><span class="sxs-lookup"><span data-stu-id="5bce1-116">This can also be caused by pending features.</span></span>

<span data-ttu-id="5bce1-117">**Løsning**: Kjør analyse for tilpassing av planleggingsoptimalisering, og analyser deretter resultatene ved henvisning til den relaterte dokumentasjonen for å forstå virkningen.</span><span class="sxs-lookup"><span data-stu-id="5bce1-117">**Fix**: Run Planning Optimization fit analysis and then analyze the results while referring to the related documentation to understand the impact.</span></span> <span data-ttu-id="5bce1-118">Hvis du vil ha mer informasjon, se [Tilpassingsanalyse av planleggingsoptimalisering](planning-optimization-fit-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="5bce1-118">For more information, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

## <a name="cant-enable-planning-optimization"></a><span data-ttu-id="5bce1-119">Kan ikke aktivere planleggingsoptimalisering</span><span class="sxs-lookup"><span data-stu-id="5bce1-119">Can't enable Planning Optimization</span></span>

<span data-ttu-id="5bce1-120">**Tilkoblingsstatusen** må være **Tilkoblet** før du kan sette **Bruk planleggingsoptimalisering** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="5bce1-120">The **Connection status** must be **Connected** before you can set **Use Planning Optimization** to **Yes**.</span></span> <span data-ttu-id="5bce1-121">Hvis du vil ha mer informasjon, se [Kom i gang med planleggingsoptimalisering](get-started.md).</span><span class="sxs-lookup"><span data-stu-id="5bce1-121">For more information, see [Get started with Planning Optimization](get-started.md).</span></span>

<span data-ttu-id="5bce1-122">**Løsning**: Kontroller at tillegget for planleggingsoptimalisering ble installert.</span><span class="sxs-lookup"><span data-stu-id="5bce1-122">**Fix**: Make sure that the Planning Optimization add-in was installed successfully.</span></span>

## <a name="error-message-is-shown-during-ctp"></a><span data-ttu-id="5bce1-123">Det vises en feilmelding under CTP</span><span class="sxs-lookup"><span data-stu-id="5bce1-123">Error message is shown during CTP</span></span>

<span data-ttu-id="5bce1-124">Hvis du prøver å kjøre leveringskapasitet (CTP) fra en salgsordre når planleggingsoptimalisering er aktivert, får du følgende feil melding: *Denne operasjonen utløste hovedplanlegging som ikke støttes når planleggingsoptimaliseringen er aktivert*.</span><span class="sxs-lookup"><span data-stu-id="5bce1-124">If you try to run capable to promise (CTP) from a sales order when Planning Optimization is enabled, you will receive the following error message: *This operation triggered master planning that isn't supported when the Planning Optimization is enabled*.</span></span>

<span data-ttu-id="5bce1-125">Dette er knyttet til en ventende funksjon som er planlagt som en del av støtten for produksjonsordrer.</span><span class="sxs-lookup"><span data-stu-id="5bce1-125">This is related to a pending feature that is planned as part of the support for production orders.</span></span>

<span data-ttu-id="5bce1-126">**Løsning:** Unngå CTP-beregninger når planleggingsoptimalisering er aktivert til CTP-støtte er tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="5bce1-126">**Fix:** Avoid CTP calculations when Planning Optimization is enabled until CTP support is available.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5bce1-127">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="5bce1-127">Additional resources</span></span>

[<span data-ttu-id="5bce1-128">Komme i gang med planleggingsoptimalisering</span><span class="sxs-lookup"><span data-stu-id="5bce1-128">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="5bce1-129">Analyse for tilpassing av planleggingsoptimalisering</span><span class="sxs-lookup"><span data-stu-id="5bce1-129">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]