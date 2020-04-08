---
title: Definere ressursgruppe for stykkproduksjon
description: En ressursgruppe er et sett med operasjonsressurser som vanligvis tilsvarer den fysiske organiseringen av arbeidsceller, definert av gule linjer på produksjon-Shop Floor.
author: sorenva
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WrkCtrResourceGroup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 01b797aa97e73cbe112c37a1efcd1e759730bc24
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/18/2020
ms.locfileid: "3149119"
---
# <a name="define-discrete-manufacturing-resource-group"></a><span data-ttu-id="0f3a9-103">Definere ressursgruppe for stykkproduksjon</span><span class="sxs-lookup"><span data-stu-id="0f3a9-103">Define discrete manufacturing resource group</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0f3a9-104">En ressursgruppe er et sett med operasjonsressurser som vanligvis tilsvarer den fysiske organiseringen av arbeidsceller, definert av gule linjer på produksjon-Shop Floor.</span><span class="sxs-lookup"><span data-stu-id="0f3a9-104">A resource group is a set of operations resources that typically correspond to the physical organization of work cells, defined by yellow lines on the production shop floor.</span></span> <span data-ttu-id="0f3a9-105">Denne fremgangsmåten viser hvordan du definerer en ressursgruppe for bruk i atskilt produksjon.</span><span class="sxs-lookup"><span data-stu-id="0f3a9-105">This procedure shows you how to define a ressource group for use in discrete production.</span></span> <span data-ttu-id="0f3a9-106">Du kan gå gjennom denne fremgangsmåten i demonstrasjonsselskapet USMF eller ved hjelp av dine egne data.</span><span class="sxs-lookup"><span data-stu-id="0f3a9-106">You can walk through this procedure in demo data company USMF, or use your own data.</span></span>

1. <span data-ttu-id="0f3a9-107">Gå til Ressursgrupper.</span><span class="sxs-lookup"><span data-stu-id="0f3a9-107">Go to Resource groups.</span></span>
2. <span data-ttu-id="0f3a9-108">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="0f3a9-108">Click New.</span></span>
3. <span data-ttu-id="0f3a9-109">Skriv inn en verdi i Ressursgruppe-feltet.</span><span class="sxs-lookup"><span data-stu-id="0f3a9-109">In the Resource group field, type a value.</span></span>
4. <span data-ttu-id="0f3a9-110">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="0f3a9-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="0f3a9-111">Angi eller velg en verdi i Område-feltet.</span><span class="sxs-lookup"><span data-stu-id="0f3a9-111">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="0f3a9-112">Angi eller velg en verdi i Produksjonsenhet-feltet.</span><span class="sxs-lookup"><span data-stu-id="0f3a9-112">In the Production unit field, enter or select a value.</span></span>

## <a name="define-default-operational-parameters"></a><span data-ttu-id="0f3a9-113">Definere standardparametere for drift</span><span class="sxs-lookup"><span data-stu-id="0f3a9-113">Define default operational parameters</span></span>
1. <span data-ttu-id="0f3a9-114">Utvid delen Operasjon.</span><span class="sxs-lookup"><span data-stu-id="0f3a9-114">Expand the Operation section.</span></span>
2. <span data-ttu-id="0f3a9-115">Angi et nummer i Svinnprosent-feltet.</span><span class="sxs-lookup"><span data-stu-id="0f3a9-115">In the Scrap percentage field, enter a number.</span></span>
3. <span data-ttu-id="0f3a9-116">Angi eller velg en verdi i Oppsettkategori-feltet.</span><span class="sxs-lookup"><span data-stu-id="0f3a9-116">In the Setup category field, enter or select a value.</span></span>
4. <span data-ttu-id="0f3a9-117">Angi eller velg en verdi i Kjøretid-feltet.</span><span class="sxs-lookup"><span data-stu-id="0f3a9-117">In the Run time category field, enter or select a value.</span></span>
5. <span data-ttu-id="0f3a9-118">Angi et tall i prosentfeltet for grovplanlegging.</span><span class="sxs-lookup"><span data-stu-id="0f3a9-118">In the Operations scheduling percentage field, enter a number.</span></span>

## <a name="define-operating-hours"></a><span data-ttu-id="0f3a9-119">Definere operasjonstimer</span><span class="sxs-lookup"><span data-stu-id="0f3a9-119">Define operating hours</span></span>
1. <span data-ttu-id="0f3a9-120">Utvid seksjonen Kalendere.</span><span class="sxs-lookup"><span data-stu-id="0f3a9-120">Expand the Calendars section.</span></span>
2. <span data-ttu-id="0f3a9-121">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="0f3a9-121">Click Add.</span></span>
3. <span data-ttu-id="0f3a9-122">Angi eller velg en verdi i Kalender-feltet.</span><span class="sxs-lookup"><span data-stu-id="0f3a9-122">In the Calendar field, enter or select a value.</span></span>

## <a name="add-operations-resources"></a><span data-ttu-id="0f3a9-123">Legg til operasjonsressurser</span><span class="sxs-lookup"><span data-stu-id="0f3a9-123">Add operations resources</span></span>
1. <span data-ttu-id="0f3a9-124">Utvid seksjonen Ressurser.</span><span class="sxs-lookup"><span data-stu-id="0f3a9-124">Expand the Resources section.</span></span>
2. <span data-ttu-id="0f3a9-125">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="0f3a9-125">Click Add.</span></span>
3. <span data-ttu-id="0f3a9-126">Angi eller velg en verdi i Ressurs-feltet.</span><span class="sxs-lookup"><span data-stu-id="0f3a9-126">In the Resource field, enter or select a value.</span></span>
4. <span data-ttu-id="0f3a9-127">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="0f3a9-127">Click Add.</span></span>
5. <span data-ttu-id="0f3a9-128">Angi eller velg en verdi i Ressurs-feltet.</span><span class="sxs-lookup"><span data-stu-id="0f3a9-128">In the Resource field, enter or select a value.</span></span>
6. <span data-ttu-id="0f3a9-129">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="0f3a9-129">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="0f3a9-130">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="0f3a9-130">In the list, click the link in the selected row.</span></span>

