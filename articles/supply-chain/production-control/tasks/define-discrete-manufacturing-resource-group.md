---
title: Definere ressursgruppe for stykkproduksjon
description: En ressursgruppe er et sett med operasjonsressurser som vanligvis tilsvarer den fysiske organiseringen av arbeidsceller, definert av gule linjer på produksjon-Shop Floor.
author: sorenva
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WrkCtrResourceGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 95a8e1c6daa78250118a8a16010ef4cc1b1ae693
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5811540"
---
# <a name="define-discrete-manufacturing-resource-group"></a><span data-ttu-id="4e358-103">Definere ressursgruppe for stykkproduksjon</span><span class="sxs-lookup"><span data-stu-id="4e358-103">Define discrete manufacturing resource group</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4e358-104">En ressursgruppe er et sett med operasjonsressurser som vanligvis tilsvarer den fysiske organiseringen av arbeidsceller, definert av gule linjer på produksjon-Shop Floor.</span><span class="sxs-lookup"><span data-stu-id="4e358-104">A resource group is a set of operations resources that typically correspond to the physical organization of work cells, defined by yellow lines on the production shop floor.</span></span> <span data-ttu-id="4e358-105">Denne fremgangsmåten viser hvordan du definerer en ressursgruppe for bruk i atskilt produksjon.</span><span class="sxs-lookup"><span data-stu-id="4e358-105">This procedure shows you how to define a ressource group for use in discrete production.</span></span> <span data-ttu-id="4e358-106">Du kan gå gjennom denne fremgangsmåten i demonstrasjonsselskapet USMF eller ved hjelp av dine egne data.</span><span class="sxs-lookup"><span data-stu-id="4e358-106">You can walk through this procedure in demo data company USMF, or use your own data.</span></span>

1. <span data-ttu-id="4e358-107">Gå til Ressursgrupper.</span><span class="sxs-lookup"><span data-stu-id="4e358-107">Go to Resource groups.</span></span>
2. <span data-ttu-id="4e358-108">Klikk på Ny.</span><span class="sxs-lookup"><span data-stu-id="4e358-108">Click New.</span></span>
3. <span data-ttu-id="4e358-109">Skriv inn en verdi i Ressursgruppe-feltet.</span><span class="sxs-lookup"><span data-stu-id="4e358-109">In the Resource group field, type a value.</span></span>
4. <span data-ttu-id="4e358-110">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="4e358-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="4e358-111">Angi eller velg en verdi i Område-feltet.</span><span class="sxs-lookup"><span data-stu-id="4e358-111">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="4e358-112">Angi eller velg en verdi i Produksjonsenhet-feltet.</span><span class="sxs-lookup"><span data-stu-id="4e358-112">In the Production unit field, enter or select a value.</span></span>

## <a name="define-default-operational-parameters"></a><span data-ttu-id="4e358-113">Definere standardparametere for drift</span><span class="sxs-lookup"><span data-stu-id="4e358-113">Define default operational parameters</span></span>
1. <span data-ttu-id="4e358-114">Utvid delen Operasjon.</span><span class="sxs-lookup"><span data-stu-id="4e358-114">Expand the Operation section.</span></span>
2. <span data-ttu-id="4e358-115">Angi et nummer i Svinnprosent-feltet.</span><span class="sxs-lookup"><span data-stu-id="4e358-115">In the Scrap percentage field, enter a number.</span></span>
3. <span data-ttu-id="4e358-116">Angi eller velg en verdi i Oppsettkategori-feltet.</span><span class="sxs-lookup"><span data-stu-id="4e358-116">In the Setup category field, enter or select a value.</span></span>
4. <span data-ttu-id="4e358-117">Angi eller velg en verdi i Kjøretid-feltet.</span><span class="sxs-lookup"><span data-stu-id="4e358-117">In the Run time category field, enter or select a value.</span></span>
5. <span data-ttu-id="4e358-118">Angi et tall i prosentfeltet for grovplanlegging.</span><span class="sxs-lookup"><span data-stu-id="4e358-118">In the Operations scheduling percentage field, enter a number.</span></span>

## <a name="define-operating-hours"></a><span data-ttu-id="4e358-119">Definere operasjonstimer</span><span class="sxs-lookup"><span data-stu-id="4e358-119">Define operating hours</span></span>
1. <span data-ttu-id="4e358-120">Utvid seksjonen Kalendere.</span><span class="sxs-lookup"><span data-stu-id="4e358-120">Expand the Calendars section.</span></span>
2. <span data-ttu-id="4e358-121">Klikk på Legg til.</span><span class="sxs-lookup"><span data-stu-id="4e358-121">Click Add.</span></span>
3. <span data-ttu-id="4e358-122">Angi eller velg en verdi i Kalender-feltet.</span><span class="sxs-lookup"><span data-stu-id="4e358-122">In the Calendar field, enter or select a value.</span></span>

## <a name="add-operations-resources"></a><span data-ttu-id="4e358-123">Legg til operasjonsressurser</span><span class="sxs-lookup"><span data-stu-id="4e358-123">Add operations resources</span></span>
1. <span data-ttu-id="4e358-124">Utvid seksjonen Ressurser.</span><span class="sxs-lookup"><span data-stu-id="4e358-124">Expand the Resources section.</span></span>
2. <span data-ttu-id="4e358-125">Klikk på Legg til.</span><span class="sxs-lookup"><span data-stu-id="4e358-125">Click Add.</span></span>
3. <span data-ttu-id="4e358-126">Angi eller velg en verdi i Ressurs-feltet.</span><span class="sxs-lookup"><span data-stu-id="4e358-126">In the Resource field, enter or select a value.</span></span>
4. <span data-ttu-id="4e358-127">Klikk på Legg til.</span><span class="sxs-lookup"><span data-stu-id="4e358-127">Click Add.</span></span>
5. <span data-ttu-id="4e358-128">Angi eller velg en verdi i Ressurs-feltet.</span><span class="sxs-lookup"><span data-stu-id="4e358-128">In the Resource field, enter or select a value.</span></span>
6. <span data-ttu-id="4e358-129">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="4e358-129">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="4e358-130">Klikk på koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="4e358-130">In the list, click the link in the selected row.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]