--- 
title: Opprette et nytt menyelement for en mobilenhet for nummerskiltkonsolidering
description: "Denne fremgangsmåten viser hvordan du oppretter et menyelement for mobilenhet for nummerskiltkonsolideringsarbeid."
author: ShylaThompson
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: fc3c6e0d48cd4f8135aa710ae86affd7b7098421
ms.contentlocale: nb-no
ms.lasthandoff: 09/11/2018

---
# <a name="create-a-mobile-device-menu-item-for-license-plate-consolidation"></a><span data-ttu-id="be0c0-103">Opprette et nytt menyelement for en mobilenhet for nummerskiltkonsolidering</span><span class="sxs-lookup"><span data-stu-id="be0c0-103">Create a mobile device menu item for license plate consolidation</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="be0c0-104">Denne fremgangsmåten viser hvordan du oppretter et menyelement for mobilenhet for nummerskiltkonsolideringsarbeid.</span><span class="sxs-lookup"><span data-stu-id="be0c0-104">This procedure shows you how to create a mobile device menu item for license plate consolidation work.</span></span> <span data-ttu-id="be0c0-105">Dette gjør at lagermedarbeidere kan konsolidere varer på ett skilt med varer på et annet skilt på samme lokasjon.</span><span class="sxs-lookup"><span data-stu-id="be0c0-105">This enables warehouse workers to consolidate items on one license plate with items on another license place within the same location.</span></span> <span data-ttu-id="be0c0-106">De kan for eksempel bruke dette hvis etterfølgende trinn er de samme på begge arbeidsordrene, slik at arbeidet bare må utføres én gang for de sammenslåtte varene.</span><span class="sxs-lookup"><span data-stu-id="be0c0-106">For example, they might use this if subsequent staging steps were the same on both work orders, so that the work only needs to be performed once for the merged items.</span></span> <span data-ttu-id="be0c0-107">Du kan bruke prosedyren i demonstrasjonsdataselskapet USMF.</span><span class="sxs-lookup"><span data-stu-id="be0c0-107">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="be0c0-108">Denne oppgaven vil vanligvis utføres av en lagersjef.</span><span class="sxs-lookup"><span data-stu-id="be0c0-108">The task would typically be carried out by a warehouse manager.</span></span> <span data-ttu-id="be0c0-109">Denne fremgangsmåten gjelder for en funksjon som ble lagt til i Dynamics 365 for Operations, versjon 1611.</span><span class="sxs-lookup"><span data-stu-id="be0c0-109">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>

1. <span data-ttu-id="be0c0-110">Gå til Lagerstyring > Oppsett > Mobilenhet > Menyelementer på mobilenheten.</span><span class="sxs-lookup"><span data-stu-id="be0c0-110">Go to Warehouse management > Setup > Mobile device > Mobile device menu items.</span></span>
2. <span data-ttu-id="be0c0-111">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="be0c0-111">Click New.</span></span>
3. <span data-ttu-id="be0c0-112">Skriv inn en verdi i feltet Menyelementnavn.</span><span class="sxs-lookup"><span data-stu-id="be0c0-112">In the Menu item name field, type a value.</span></span>
4. <span data-ttu-id="be0c0-113">Skriv inn en verdi i Tittel-feltet.</span><span class="sxs-lookup"><span data-stu-id="be0c0-113">In the Title field, type a value.</span></span>
5. <span data-ttu-id="be0c0-114">Velg Indirekte i feltet Modus.</span><span class="sxs-lookup"><span data-stu-id="be0c0-114">In the Mode field, select 'Indirect'.</span></span>
6. <span data-ttu-id="be0c0-115">Velg Konsolider skiltnummer i Aktivitetskode-feltet.</span><span class="sxs-lookup"><span data-stu-id="be0c0-115">In the Activity code field, select 'Consolidate license plates'.</span></span>


