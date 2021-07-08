---
title: Du får en feilmelding når du kjører den innebygde hovedplanleggingsmotoren
description: Nrå du kjører den avskrevne innebygde hovedplanleggingsmotoren, mottar du en feilmelding.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: Dialog_ReqCalcScheduleItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 9c950292a4f43319d21a7deafdfb341b7bef15d8
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294147"
---
# <a name="you-receive-an-error-when-running-the-built-in-master-planning-engine"></a><span data-ttu-id="551da-103">Du får en feilmelding når du kjører den innebygde hovedplanleggingsmotoren</span><span class="sxs-lookup"><span data-stu-id="551da-103">You receive an error when running the built-in master planning engine</span></span>

<span data-ttu-id="551da-104">Feilkode: ReqCalcScheduleItemTablePlanningOptimizationFitError</span><span class="sxs-lookup"><span data-stu-id="551da-104">Error code: ReqCalcScheduleItemTablePlanningOptimizationFitError</span></span>

## <a name="symptoms"></a><span data-ttu-id="551da-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="551da-105">Symptoms</span></span>

<span data-ttu-id="551da-106">Nrå du kjører hovedplanlegging ved å bruke den avskrevne innebygde hovedplanleggingsmotoren, mottar du følgende feilmelding:</span><span class="sxs-lookup"><span data-stu-id="551da-106">When you run master planning by using the deprecated built-in master planning engine, you receive the following error message:</span></span>

> <span data-ttu-id="551da-107">Du får denne feilmeldingen fordi den innebygde hovedplanleggingsmotoren ble brukt til scenarioer som støttes av planleggingsoptimalisering.</span><span class="sxs-lookup"><span data-stu-id="551da-107">You receive this error message because the built-in master planning engine was used for scenarios supported by Planning Optimization.</span></span> <span data-ttu-id="551da-108">Du bør overføre til planleggingsoptimalisering nå, fordi den gjeldende innebygde hovedplanleggingen vil bli avskrevet.</span><span class="sxs-lookup"><span data-stu-id="551da-108">You should migrate to Planning Optimization now, as the current built-in master planning will be deprecated.</span></span> <span data-ttu-id="551da-109">Legg merke til at denne hovedplanleggingskjøringen ble fullført.</span><span class="sxs-lookup"><span data-stu-id="551da-109">Note that this master planning run did complete successfully.</span></span> <span data-ttu-id="551da-110">I tilfelle overføringen har sterke avhengigheter for ventende funksjoner, kan du be om et unntak for fortsatt bruk av den innebygde hovedplanleggingsmotoren.</span><span class="sxs-lookup"><span data-stu-id="551da-110">In case your migration has strong dependencies on pending features, an exception to continued usage of the built-in master planning engine can be requested.</span></span> <span data-ttu-id="551da-111">Fyll ut følgende spørreskjema for å komme i gang, og hvis det er relevant, forespør et unntak fra overføring til planleggingsoptimalisering.</span><span class="sxs-lookup"><span data-stu-id="551da-111">Please complete the following questionnaire to get started and, if relevant, request an exception from migration to Planning Optimization.</span></span> [<span data-ttu-id="551da-112">Spørreskjemaet om migrering og unntak i Planleggingsoptimalisering</span><span class="sxs-lookup"><span data-stu-id="551da-112">Planning Optimization migration and exception questionnaire</span></span>](https://go.microsoft.com/fwlink/?linkid=2144962)

## <a name="cause"></a><span data-ttu-id="551da-113">Årsak</span><span class="sxs-lookup"><span data-stu-id="551da-113">Cause</span></span>

<span data-ttu-id="551da-114">Hvis du kjører planlegging og ikke bruker funksjoner for produksjonskontroll, bør du vurdere å migrere til Planleggingsoptimalisering.</span><span class="sxs-lookup"><span data-stu-id="551da-114">If you run planning and don't use production control features, you should consider migrating to Planning Optimization.</span></span> <span data-ttu-id="551da-115">Den innebygde hovedplanleggingsmotoren blir avskrevet.</span><span class="sxs-lookup"><span data-stu-id="551da-115">The built-in master planning engine is being deprecated.</span></span> <span data-ttu-id="551da-116">Hvis du vil fortsette å bruke det uten å motta feilmeldingen, må du derfor søke om et unntak fra Microsoft.</span><span class="sxs-lookup"><span data-stu-id="551da-116">Therefore, if you want to continue to use it without receiving the error message, you must apply for an exception from Microsoft.</span></span>

## <a name="resolution"></a><span data-ttu-id="551da-117">Løsning</span><span class="sxs-lookup"><span data-stu-id="551da-117">Resolution</span></span>

<span data-ttu-id="551da-118">Hvis du vil ha mer informasjon om hvordan du migrerer til Planleggingsoptimalisering, eller hvordan du søker etter et unntak, slik at du kan fortsette å bruke den avkrevne, innebygde planleggingsmotoren i stedet, kan du se [Overføring til planleggingsoptimalisering for hovedplanlegging](/dynamics365/supply-chain/master-planning/new-master-planning-engine).</span><span class="sxs-lookup"><span data-stu-id="551da-118">For more information about how to migrate to Planning Optimization, or how to apply for an exception so that you can continue to use the deprecated built-in planning engine instead, see [Migration to Planning Optimization for master planning](/dynamics365/supply-chain/master-planning/new-master-planning-engine).</span></span>
