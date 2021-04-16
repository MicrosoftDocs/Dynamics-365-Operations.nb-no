---
title: Opprette en arbeidsklasse
description: Denne fremgangsmåten viser hvordan du setter opp en arbeidsklasse.
author: ShylaThompson
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWorkClass
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: be2c037ccc8f5cafc94d9fdee9647605889d0599
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5830984"
---
# <a name="create-a-work-class"></a><span data-ttu-id="b5b05-103">Opprette en arbeidsklasse</span><span class="sxs-lookup"><span data-stu-id="b5b05-103">Create a work class</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b5b05-104">Denne fremgangsmåten viser hvordan du setter opp en arbeidsklasse.</span><span class="sxs-lookup"><span data-stu-id="b5b05-104">This procedure shows you how to set up a work class.</span></span> <span data-ttu-id="b5b05-105">Arbeidsklasser brukes til å styre og/eller begrense typen arbeidsordrelinjer som en lagermedarbeider kan behandle på en mobil enhet.</span><span class="sxs-lookup"><span data-stu-id="b5b05-105">Work classes are used to direct and/or limit the type of work order lines that a warehouse worker can process on a mobile device.</span></span> <span data-ttu-id="b5b05-106">Linjene som en arbeider kan behandle, bestemmes fra arbeidsklassene på menyelementene for mobilenhet som Lagermedarbeideren har tilgang til og arbeidsklassen som er angitt på arbeidslinjene.</span><span class="sxs-lookup"><span data-stu-id="b5b05-106">The lines that a worker can process are determined from the work classes on the mobile device menu items that the warehouse worker has access to and the work class that's specified on the work lines.</span></span> <span data-ttu-id="b5b05-107">Arbeidsklasser kan også brukes til å validere plasseringslokasjon for en arbeidsordrelinje.</span><span class="sxs-lookup"><span data-stu-id="b5b05-107">Work classes can also be used to validate the put location for a work order line.</span></span> <span data-ttu-id="b5b05-108">Du kan kjøre denne fremgangsmåten i demonstrasjonsselskapet USMF eller ved hjelp av dine egne data.</span><span class="sxs-lookup"><span data-stu-id="b5b05-108">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="b5b05-109">Denne fremgangsmåten er ment for lagersjef.</span><span class="sxs-lookup"><span data-stu-id="b5b05-109">This procedure is intended for the warehouse manager.</span></span>

1. <span data-ttu-id="b5b05-110">Gå til Lagerstyring > Oppsett > Arbeid > Arbeidsklasser.</span><span class="sxs-lookup"><span data-stu-id="b5b05-110">Go to Warehouse management > Setup > Work > Work classes.</span></span>
2. <span data-ttu-id="b5b05-111">Klikk på Ny.</span><span class="sxs-lookup"><span data-stu-id="b5b05-111">Click New.</span></span>
3. <span data-ttu-id="b5b05-112">Skriv inn en verdi i feltet Arbeidsklasse-ID.</span><span class="sxs-lookup"><span data-stu-id="b5b05-112">In the Work class ID field, type a value.</span></span>
4. <span data-ttu-id="b5b05-113">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="b5b05-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="b5b05-114">Velg et alternativ i feltet Arbeidsordretype.</span><span class="sxs-lookup"><span data-stu-id="b5b05-114">In the Work order type field, select an option.</span></span>
6. <span data-ttu-id="b5b05-115">Klikk på Ny.</span><span class="sxs-lookup"><span data-stu-id="b5b05-115">Click New.</span></span>
7. <span data-ttu-id="b5b05-116">Skriv inn en verdi i feltet Lokasjonstype.</span><span class="sxs-lookup"><span data-stu-id="b5b05-116">In the Location type field, type a value.</span></span>
    * <span data-ttu-id="b5b05-117">Hvis du velger en lokasjonstype, angir dette en begrensning på hvor varene kan plasseres når de har blitt plukket.</span><span class="sxs-lookup"><span data-stu-id="b5b05-117">If you select a location type, this sets a restriction on where items can be put after they've been picked.</span></span> <span data-ttu-id="b5b05-118">Denne innstillingen brukes når et lokasjonsdirektiv forsøker å løse lokasjonen, eller hvis lagermedarbeider angir lokasjonen for menyelementet for mobil enhet manuelt.</span><span class="sxs-lookup"><span data-stu-id="b5b05-118">This setting is used when a location directive tries to resolve the location, or if a warehouse worker manually provides the location for the mobile device menu item.</span></span>  
8. <span data-ttu-id="b5b05-119">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="b5b05-119">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]