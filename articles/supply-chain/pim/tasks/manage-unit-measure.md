---
title: Administrere måleenhet
description: Denne fremgangsmåten beskriver hvordan du definerer en målenhet, angir oversettelser for enheten og beskrivelsen og definerer omregningsreglene for relaterte enheter.
author: sorenva
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, UnitOfMeasure, UnitOfMeasureReportingTranslation, UnitOfMeasureTranslation, UnitOfMeasureConversion, UnitOfMeasureConversionEditOrCreate, UnitOfMeasureLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3e208b7f1faab77f2b97ff7b440a228656684fca
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "358928"
---
# <a name="manage-unit-of-measure"></a><span data-ttu-id="101f9-103">Administrere måleenhet</span><span class="sxs-lookup"><span data-stu-id="101f9-103">Manage unit of measure</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="101f9-104">Denne fremgangsmåten beskriver hvordan du definerer en målenhet, angir oversettelser for enheten og beskrivelsen og definerer omregningsreglene for relaterte enheter.</span><span class="sxs-lookup"><span data-stu-id="101f9-104">This procedure shows how to define a unit of measure, provide translations for the unit and it's description, and define conversion rules for related units.</span></span> <span data-ttu-id="101f9-105">Du kan gå gjennom denne fremgangsmåten ved hjelp av demonstrasjonsdata eller ved hjelp av dine egne data.</span><span class="sxs-lookup"><span data-stu-id="101f9-105">You can walk through this procedure using demo data, or using your own data.</span></span>

1. <span data-ttu-id="101f9-106">Gå til Vedlikehold av frigitt produkt.</span><span class="sxs-lookup"><span data-stu-id="101f9-106">Go to Released product maintenance.</span></span>
2. <span data-ttu-id="101f9-107">Velg enheter.</span><span class="sxs-lookup"><span data-stu-id="101f9-107">Click Units.</span></span>

## <a name="create-a-unit-of-measure"></a><span data-ttu-id="101f9-108">Opprett en måleenhet</span><span class="sxs-lookup"><span data-stu-id="101f9-108">Create a unit of measure</span></span>
1. <span data-ttu-id="101f9-109">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="101f9-109">Click New.</span></span>
2. <span data-ttu-id="101f9-110">Skriv inn en verdi i feltet Enhet.</span><span class="sxs-lookup"><span data-stu-id="101f9-110">In the Unit field, type a value.</span></span>
    * <span data-ttu-id="101f9-111">Angi ID eller symbol som skal brukes ved referanse til måleenheten.</span><span class="sxs-lookup"><span data-stu-id="101f9-111">Enter the ID or symbol to use when referring to the unit of measure.</span></span>  
3. <span data-ttu-id="101f9-112">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="101f9-112">In the Description field, type a value.</span></span>
    * <span data-ttu-id="101f9-113">Angi et beskrivende navn for måleenheten på systemspråket.</span><span class="sxs-lookup"><span data-stu-id="101f9-113">Enter a descriptive name for the unit of measure in the system language.</span></span>  
4. <span data-ttu-id="101f9-114">Velg et alternativ i feltet Enhetsklasse.</span><span class="sxs-lookup"><span data-stu-id="101f9-114">In the Unit class field, select an option.</span></span>
    * <span data-ttu-id="101f9-115">Enhetsklassen definerer hvilken logisk gruppering, for eksempel område, masse eller antall, måleenheten er en del av.</span><span class="sxs-lookup"><span data-stu-id="101f9-115">The unit class defines what logical grouping, such as area, mass, or quantity, the unit of measure is part of.</span></span>  
5. <span data-ttu-id="101f9-116">Angi et tall i feltet Desimalpresisjon.</span><span class="sxs-lookup"><span data-stu-id="101f9-116">In the Decimal precision field, enter a number.</span></span>
    * <span data-ttu-id="101f9-117">Angi antallet desimaler som den konverterte måleenheten må avrundes til når en beregning er fullført for måleenheten.</span><span class="sxs-lookup"><span data-stu-id="101f9-117">Specify the number of decimals that the converted unit of measure must be rounded to when a calculation is completed for the unit of measure.</span></span>  
6. <span data-ttu-id="101f9-118">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="101f9-118">Click Save.</span></span>

## <a name="define-unit-translations"></a><span data-ttu-id="101f9-119">Definer enhetsoversettelser</span><span class="sxs-lookup"><span data-stu-id="101f9-119">Define unit translations</span></span>
1. <span data-ttu-id="101f9-120">Klikk Enhetstekster.</span><span class="sxs-lookup"><span data-stu-id="101f9-120">Click Unit texts.</span></span>
2. <span data-ttu-id="101f9-121">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="101f9-121">Click New.</span></span>
    * <span data-ttu-id="101f9-122">Bruk enhetsteksten til å opprette en oversettelse av ID-en eller et symbol som representerer måleenheten for bruk på eksterne dokumenter på kunde- eller leverandørspesifikke språk.</span><span class="sxs-lookup"><span data-stu-id="101f9-122">Use unit text to create a translation of the ID or a symbol representing the unit of measure for use on external documents in customer- or vendor-specific languages.</span></span>  
3. <span data-ttu-id="101f9-123">Angi eller velg en verdi i feltet Språk.</span><span class="sxs-lookup"><span data-stu-id="101f9-123">In the Language field, enter or select a value.</span></span>
4. <span data-ttu-id="101f9-124">Skriv inn en verdi i Tekst-feltet.</span><span class="sxs-lookup"><span data-stu-id="101f9-124">In the Text field, type a value.</span></span>
5. <span data-ttu-id="101f9-125">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="101f9-125">Click Save.</span></span>
6. <span data-ttu-id="101f9-126">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="101f9-126">Close the page.</span></span>
7. <span data-ttu-id="101f9-127">Klikk Oversatte enhetsbeskrivelser.</span><span class="sxs-lookup"><span data-stu-id="101f9-127">Click Translated unit descriptions.</span></span>
8. <span data-ttu-id="101f9-128">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="101f9-128">Click New.</span></span>
    * <span data-ttu-id="101f9-129">Definer språkspesifikke beskrivelser for måleenheten.</span><span class="sxs-lookup"><span data-stu-id="101f9-129">Define language-specific descriptions for the unit of measure.</span></span>  
9. <span data-ttu-id="101f9-130">Angi eller velg en verdi i feltet Språk.</span><span class="sxs-lookup"><span data-stu-id="101f9-130">In the Language field, enter or select a value.</span></span>
10. <span data-ttu-id="101f9-131">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="101f9-131">In the Description field, type a value.</span></span>
11. <span data-ttu-id="101f9-132">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="101f9-132">Click Save.</span></span>
12. <span data-ttu-id="101f9-133">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="101f9-133">Close the page.</span></span>

## <a name="define-unit-conversion-rules"></a><span data-ttu-id="101f9-134">Definer enhetsomregningsregler</span><span class="sxs-lookup"><span data-stu-id="101f9-134">Define unit conversion rules</span></span>
1. <span data-ttu-id="101f9-135">Klikk Enhetsomregninger.</span><span class="sxs-lookup"><span data-stu-id="101f9-135">Click Unit conversions.</span></span>
    * <span data-ttu-id="101f9-136">Definere regler for å konvertere måleenheten til og fra andre enheter i den valgte enhetsklassen.</span><span class="sxs-lookup"><span data-stu-id="101f9-136">Define rules for converting the unit of measure to and from other units of measure in the selected unit class.</span></span>  
2. <span data-ttu-id="101f9-137">Klikk Ny for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="101f9-137">Click New to open the drop dialog.</span></span>
3. <span data-ttu-id="101f9-138">Angi et tall i feltet Faktor.</span><span class="sxs-lookup"><span data-stu-id="101f9-138">In the Factor field, enter a number.</span></span>
    * <span data-ttu-id="101f9-139">Omregningsfaktor mellom fra-enheten og til-enheten.</span><span class="sxs-lookup"><span data-stu-id="101f9-139">Conversion factor between the From unit and the To unit.</span></span> <span data-ttu-id="101f9-140">Omregningsfaktoren fra centimeter til meter er for eksempel 100, fordi det er 100 centimeter i én meter.</span><span class="sxs-lookup"><span data-stu-id="101f9-140">For example, the conversion factor from centimeter to meter is 100 because there are 100 centimeters in one meter.</span></span>  
4. <span data-ttu-id="101f9-141">Angi eller velg en verdi i feltet Til enhet.</span><span class="sxs-lookup"><span data-stu-id="101f9-141">In the To unit field, enter or select a value.</span></span>
5. <span data-ttu-id="101f9-142">Velg et alternativ i feltet Avrunding.</span><span class="sxs-lookup"><span data-stu-id="101f9-142">In the Rounding field, select an option.</span></span>
    * <span data-ttu-id="101f9-143">Definer hvordan den omregnede verdien skal avrundes.</span><span class="sxs-lookup"><span data-stu-id="101f9-143">Define how the converted value should be rounded.</span></span>  
6. <span data-ttu-id="101f9-144">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="101f9-144">Click OK.</span></span>
7. <span data-ttu-id="101f9-145">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="101f9-145">Close the page.</span></span>

