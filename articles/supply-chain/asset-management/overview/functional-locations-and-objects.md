---
title: Arbeidssteder og aktiva
description: Dette emnet beskriver arbeidssteder og aktiva i Aktivastyring. Aktivastyring er en avansert modul for håndtering av aktiva og vedlikeholdsjobber i Dynamics 365 Supply Chain Management.
author: josaw1
manager: tfehr
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 53091f2e3c159f73f11b3dfcefd597f2c1494d19
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5253092"
---
# <a name="functional-locations-and-assets"></a><span data-ttu-id="fd424-104">Arbeidssteder og aktiva</span><span class="sxs-lookup"><span data-stu-id="fd424-104">Functional locations and assets</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="fd424-105">Dette emnet beskriver arbeidssteder og aktiva i Aktivastyring.</span><span class="sxs-lookup"><span data-stu-id="fd424-105">This topic describes functional locations and assets in Asset Management.</span></span> <span data-ttu-id="fd424-106">Aktivastyring er en avansert modul for håndtering av aktiva og vedlikeholdsjobber i Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="fd424-106">Asset Management is an advanced module for managing assets and maintenance jobs in Dynamics 365 Supply Chain Management.</span></span>

## <a name="overview"></a><span data-ttu-id="fd424-107">Oversikt</span><span class="sxs-lookup"><span data-stu-id="fd424-107">Overview</span></span>

<span data-ttu-id="fd424-108">Aktivastyring er integrert sømløst med flere moduler i andre Finance and Operations-apper.</span><span class="sxs-lookup"><span data-stu-id="fd424-108">Asset Management is integrated seamlessly with several modules with other Finance and Operations apps.</span></span> <span data-ttu-id="fd424-109">Illustrasjonen nedenfor viser grensesnittene med andre moduler.</span><span class="sxs-lookup"><span data-stu-id="fd424-109">The following illustration shows the interfaces with other modules.</span></span>

![Diagram som viser hvordan Aktivastyring har grensesnitt til andre moduler](media/01-overview-image.png)

<span data-ttu-id="fd424-111">Med Aktivastyring kan du effektivt administrere og utføre alle oppgaver som er knyttet til administrasjon og vedlikehold av mange typer utstyr i firmaet.</span><span class="sxs-lookup"><span data-stu-id="fd424-111">Asset Management lets you efficiently manage and perform all tasks that are related to managing and servicing many types of equipment in your company.</span></span> <span data-ttu-id="fd424-112">Dette utstyret omfatter maskiner, produksjonsutstyr og kjøretøyer.</span><span class="sxs-lookup"><span data-stu-id="fd424-112">This equipment includes machines, production equipment, and vehicles.</span></span> <span data-ttu-id="fd424-113">Aktivastyring støtter også løsninger på tvers av en rekke bransjer.</span><span class="sxs-lookup"><span data-stu-id="fd424-113">Asset Management also supports solutions across numerous industries.</span></span>

<span data-ttu-id="fd424-114">Illustrasjonen nedenfor viser en oversikt over de viktigste funksjonene som dekkes av Aktivastyring.</span><span class="sxs-lookup"><span data-stu-id="fd424-114">The following illustration shows an overview of the main functionality that is covered by Asset Management.</span></span>

![Diagram som viser hovedfunksjonaliteten i Aktivastyring](media/02-overview-image.png)

## <a name="functional-locations-and-assets"></a><span data-ttu-id="fd424-116">Arbeidssteder og aktiva</span><span class="sxs-lookup"><span data-stu-id="fd424-116">Functional locations and assets</span></span>

<span data-ttu-id="fd424-117">Arbeidssteder brukes til å administrere aktiva på steder.</span><span class="sxs-lookup"><span data-stu-id="fd424-117">Functional locations are used to manage assets on locations.</span></span> <span data-ttu-id="fd424-118">Denne administrasjonen inkluderer sporing av aktivakostnader på arbeidssteder.</span><span class="sxs-lookup"><span data-stu-id="fd424-118">This management includes tracking of asset costs on functional locations.</span></span> <span data-ttu-id="fd424-119">Arbeidssteder er strukturert hierarkisk, og steder kan ha underordnede steder.</span><span class="sxs-lookup"><span data-stu-id="fd424-119">Functional locations are structured hierarchically, and locations can have sub-locations.</span></span> <span data-ttu-id="fd424-120">Strukturen til arbeidssteder er statisk.</span><span class="sxs-lookup"><span data-stu-id="fd424-120">The structure of functional locations is static.</span></span> <span data-ttu-id="fd424-121">Med andre ord, steder kan ikke endre plass.</span><span class="sxs-lookup"><span data-stu-id="fd424-121">In other words, locations can't change place.</span></span> <span data-ttu-id="fd424-122">Aktiva kan installeres på arbeidssteder, og etter behov kan de installeres på andre arbeidssteder senere.</span><span class="sxs-lookup"><span data-stu-id="fd424-122">Assets can be installed on functional locations and, as required, can be installed on other functional locations later.</span></span>

<span data-ttu-id="fd424-123">Aktivakostnader følger alltid plasseringen av aktivumet.</span><span class="sxs-lookup"><span data-stu-id="fd424-123">Asset costs always follow the location of the asset.</span></span> <span data-ttu-id="fd424-124">Med andre ord, hvis du installerer et aktivum på et nytt arbeidssted, bruker aktivumet automatisk finansdimensjonene som er knyttet til det nye arbeidsstedet.</span><span class="sxs-lookup"><span data-stu-id="fd424-124">In other words, if you install an asset on a new functional location, the asset automatically uses the financial dimensions that are related to the new functional location.</span></span> <span data-ttu-id="fd424-125">Derfor er aktivakostnader alltid knyttet til arbeidsstedet som aktivumet er installert på.</span><span class="sxs-lookup"><span data-stu-id="fd424-125">Therefore, asset costs are always related to the functional location that the asset is  currently installed on.</span></span> <span data-ttu-id="fd424-126">Denne automatiske håndteringen av finansdimensjoner bidrar til å sikre fullstendig sporing av kostnader når firmaet utfører prosjektkontroll og rapportering på arbeidssteder.</span><span class="sxs-lookup"><span data-stu-id="fd424-126">This automatic handling of financial dimensions helps guarantee complete tracking of costs when your company does project controlling and reporting on functional locations.</span></span>

<span data-ttu-id="fd424-127">Måten du bygger hierarkiet av arbeidssteder på, avhenger av firmaets krav for å opprettholde internt utstyr eller betjene kundeutstyr.</span><span class="sxs-lookup"><span data-stu-id="fd424-127">The way that you build your hierarchy of functional locations depends on your company's requirements for maintaining internal equipment or servicing customer equipment.</span></span> <span data-ttu-id="fd424-128">Den følgende illustrasjonen viser et eksempel på arbeidssteder som er basert på geografiske lokasjoner.</span><span class="sxs-lookup"><span data-stu-id="fd424-128">The following figure shows an example of functional locations that are based on geographical locations.</span></span>

![Diagram som viser arbeidssteder basert på geografiske steder](media/03-overview-image.png)

<span data-ttu-id="fd424-130">Den følgende illustrasjonen viser et eksempel på arbeidssteder som er basert på kunder.</span><span class="sxs-lookup"><span data-stu-id="fd424-130">The following figure shows an example of functional locations that are based on customers.</span></span>

![Diagram som viser arbeidssteder basert på kunder](media/04-overview-image.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]