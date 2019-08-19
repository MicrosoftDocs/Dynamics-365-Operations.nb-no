---
title: Opprette et nytt menyelement for en mobilenhet for nummerskiltkonsolidering
description: Denne fremgangsmåten viser hvordan du oppretter et menyelement for mobilenhet for nummerskiltkonsolideringsarbeid.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cc610a16f4b0e574b5d5e7f8fc9ecf1e12534645
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/01/2019
ms.locfileid: "1847309"
---
# <a name="create-a-mobile-device-menu-item-for-license-plate-consolidation"></a><span data-ttu-id="2d6a9-103">Opprette et nytt menyelement for en mobilenhet for nummerskiltkonsolidering</span><span class="sxs-lookup"><span data-stu-id="2d6a9-103">Create a mobile device menu item for license plate consolidation</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2d6a9-104">Denne fremgangsmåten viser hvordan du oppretter et menyelement for mobilenhet for nummerskiltkonsolideringsarbeid.</span><span class="sxs-lookup"><span data-stu-id="2d6a9-104">This procedure shows you how to create a mobile device menu item for license plate consolidation work.</span></span> <span data-ttu-id="2d6a9-105">Dette gjør at lagermedarbeidere kan konsolidere varer på ett skilt med varer på et annet skilt på samme lokasjon.</span><span class="sxs-lookup"><span data-stu-id="2d6a9-105">This enables warehouse workers to consolidate items on one license plate with items on another license place within the same location.</span></span> <span data-ttu-id="2d6a9-106">De kan for eksempel bruke dette hvis etterfølgende trinn er de samme på begge arbeidsordrene, slik at arbeidet bare må utføres én gang for de sammenslåtte varene.</span><span class="sxs-lookup"><span data-stu-id="2d6a9-106">For example, they might use this if subsequent staging steps were the same on both work orders, so that the work only needs to be performed once for the merged items.</span></span> <span data-ttu-id="2d6a9-107">Du kan bruke prosedyren i demonstrasjonsdataselskapet USMF.</span><span class="sxs-lookup"><span data-stu-id="2d6a9-107">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="2d6a9-108">Denne oppgaven vil vanligvis utføres av en lagersjef.</span><span class="sxs-lookup"><span data-stu-id="2d6a9-108">The task would typically be carried out by a warehouse manager.</span></span> <span data-ttu-id="2d6a9-109">Denne fremgangsmåten gjelder for en funksjon som ble lagt til i Dynamics 365 for Operations, versjon 1611.</span><span class="sxs-lookup"><span data-stu-id="2d6a9-109">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>

1. <span data-ttu-id="2d6a9-110">Gå til Lagerstyring > Oppsett > Mobilenhet > Menyelementer på mobilenheten.</span><span class="sxs-lookup"><span data-stu-id="2d6a9-110">Go to Warehouse management > Setup > Mobile device > Mobile device menu items.</span></span>
2. <span data-ttu-id="2d6a9-111">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="2d6a9-111">Click New.</span></span>
3. <span data-ttu-id="2d6a9-112">Skriv inn en verdi i feltet Menyelementnavn.</span><span class="sxs-lookup"><span data-stu-id="2d6a9-112">In the Menu item name field, type a value.</span></span>
4. <span data-ttu-id="2d6a9-113">Skriv inn en verdi i Tittel-feltet.</span><span class="sxs-lookup"><span data-stu-id="2d6a9-113">In the Title field, type a value.</span></span>
5. <span data-ttu-id="2d6a9-114">Velg Indirekte i feltet Modus.</span><span class="sxs-lookup"><span data-stu-id="2d6a9-114">In the Mode field, select 'Indirect'.</span></span>
6. <span data-ttu-id="2d6a9-115">Velg Konsolider skiltnummer i Aktivitetskode-feltet.</span><span class="sxs-lookup"><span data-stu-id="2d6a9-115">In the Activity code field, select 'Consolidate license plates'.</span></span>

