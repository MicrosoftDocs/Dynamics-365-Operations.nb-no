---
title: Godkjenn planlagte ordrer
description: Dette emnet beskriver godkjenning av planlagte ordrer som støttes i planleggingsoptimalisering.
author: ChristianRytt
manager: tfehr
ms.date: 08/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-08-21
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: b7975088be898ccecceb1f7be009cecff107f6e6
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4434381"
---
# <a name="approve-planned-orders"></a><span data-ttu-id="0e52a-103">Godkjenn planlagte ordrer</span><span class="sxs-lookup"><span data-stu-id="0e52a-103">Approve planned orders</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0e52a-104">Dette emnet inneholder informasjon om hvordan du oppdaterer statusen for planlagte ordrer i planleggingsoptimalisering.</span><span class="sxs-lookup"><span data-stu-id="0e52a-104">This topic provides information about how to update the status of planned orders in Planning Optimization.</span></span>

<span data-ttu-id="0e52a-105">Merk deg at godkjenning av planlagte ordrer er et valgfritt trinn for å opprette en autorisert ordre fra en planlagt ordre.</span><span class="sxs-lookup"><span data-stu-id="0e52a-105">Note that approval of planned orders is an optional step, on the way to create a firmed order from a planned order.</span></span> <span data-ttu-id="0e52a-106">Det anbefales at du godkjenner endrede planlagte ordrer, ellers blir redigeringene ignorert og overskrevet av neste planleggingskjøring.</span><span class="sxs-lookup"><span data-stu-id="0e52a-106">It is recommended to approve modified planned orders, otherwise the edits will be ignored and overwritten by the next planning run.</span></span>

![Planlagt ordreflyt](media/approved-planned-orders-1.png)

<span data-ttu-id="0e52a-108">**Status**-feltet hjelper med å spore fremdriften ved hjelp av følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="0e52a-108">The **Status** field helps you tack your progress using the following values:</span></span>

- <span data-ttu-id="0e52a-109">**Ubehandlet:** Når hovedplanlegging genererer planlagte ordrer, har de planlagte ordrene statusen *Ubehandlet*.</span><span class="sxs-lookup"><span data-stu-id="0e52a-109">**Unprocessed:** When master planning generates planned orders, the planned orders have a status of *Unprocessed*.</span></span> <span data-ttu-id="0e52a-110">Planlagte ordrer med denne statusen blir slettet under neste planleggingskjøring.</span><span class="sxs-lookup"><span data-stu-id="0e52a-110">Planned orders with this status will be deleted during the next planning run.</span></span>
- <span data-ttu-id="0e52a-111">**Fullført:** Hvis du bestemmer deg for ikke å autorisere en planlagt ordre, kan du endre statusen til *Fullført* for å angi at du har fullført evalueringen av denne planlagte ordren.</span><span class="sxs-lookup"><span data-stu-id="0e52a-111">**Completed:** If you decide not to firm a planned order, you can change the status to *Completed* to indicate that you completed evaluating this planned order.</span></span> <span data-ttu-id="0e52a-112">Legg merke til at statusen for *Ubehandlet* og *Fullført* behandles på samme måte av systemet.</span><span class="sxs-lookup"><span data-stu-id="0e52a-112">Note that a status of *Unprocessed* and *Completed* are treated the same by the system.</span></span>
- <span data-ttu-id="0e52a-113">**Godkjent:** Hvis du vil beholde endringer eller planlegge å bekrefte en planlagt ordre, endrer du statusen til *Godkjent*.</span><span class="sxs-lookup"><span data-stu-id="0e52a-113">**Approved:** If you want to keep edits or are planning to firm a planned order, change the status to *Approved*.</span></span> <span data-ttu-id="0e52a-114">Planlagte ordrer med *Godkjent*-status anses som faste, og det forventes forsyning via hovedplanlegging. Demed blir de ikke endret eller slettet under senere panleggingskjøringer.</span><span class="sxs-lookup"><span data-stu-id="0e52a-114">Planned orders with *Approved* status are considered as fixed and expected supply by master planning, so they are not modified or deleted during later master planning runs.</span></span> <span data-ttu-id="0e52a-115">For å oppnå dette kopierer planleggingslogikken de *godkjente* planlagte bestillingene fra den gamle planversjonen til den nye planversjonen under hovedplanlegging.</span><span class="sxs-lookup"><span data-stu-id="0e52a-115">To achieve this, the planning logic copies the *Approved* planned orders from the old plan version to the new plan version during master planning.</span></span> <span data-ttu-id="0e52a-116">Legg merke til at planlaget ordrer med statusen *Godkjente* bare regnes som forsyning i den bestemte hovedplanen.</span><span class="sxs-lookup"><span data-stu-id="0e52a-116">Note that *Approved* planned orders are only considered supply within the specific master plan.</span></span>

<span data-ttu-id="0e52a-117">Du kan administrere planlagte ordrer fra arbeidsområdet **Hovedplanlegging**, listen **Planlagt ordre** eller listene **Planlagte produksjonsordrer**, **Planlagte bestillinger** og **Planlagt overføring**.</span><span class="sxs-lookup"><span data-stu-id="0e52a-117">You can manage planned orders from the  **Master planning**  workspace, the  **Planned order**  list, or the  **Planned production orders**,  **Planned purchase orders**, and  **Planned transfer**  lists.</span></span>
