---
title: Kopiere en formel
description: Denne prosedyren fokuserer på å opprette en formel som inneholder de samme ingrediensene som en eksisterende formel, men med små forskjeller.
author: ShylaThompson
manager: tfehr
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 26524f886a8af545869bacef4d57bfc14c0ed225
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/10/2020
ms.locfileid: "3979166"
---
# <a name="copy-a-formula"></a><span data-ttu-id="a7e79-103">Kopiere en formel</span><span class="sxs-lookup"><span data-stu-id="a7e79-103">Copy a formula</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a7e79-104">Denne prosedyren fokuserer på å opprette en formel som inneholder de samme ingrediensene som en eksisterende formel, men med små forskjeller.</span><span class="sxs-lookup"><span data-stu-id="a7e79-104">This procedure focuses on creating a formula that includes the same ingredients as an existing formula, but with minor differences.</span></span> <span data-ttu-id="a7e79-105">Når du skal opprette formellinjene, kan du bruke kopieringsfunksjonen til å kopiere en eksisterende formel som har de fleste av ingrediensene som du trenger.</span><span class="sxs-lookup"><span data-stu-id="a7e79-105">To create the formula lines, you can use the Copy function to copy an existing formula that has most of the ingredients that you need.</span></span> <span data-ttu-id="a7e79-106">Du kan deretter gjøre eventuelle nødvendige endringer i enkeltlinjene i den nye versjonen.</span><span class="sxs-lookup"><span data-stu-id="a7e79-106">You can then make any necessary changes to the individual lines in the new version.</span></span> <span data-ttu-id="a7e79-107">Ved hjelp av funksjonen Kopier, behøver du ikke å opprette flere formler som er nesten identiske.</span><span class="sxs-lookup"><span data-stu-id="a7e79-107">By using the Copy function, you do not have to create multiple formulas that are almost identical.</span></span> <span data-ttu-id="a7e79-108">Demonstrasjonsdatafirmaet USP2 brukes til å opprette denne oppgaven.</span><span class="sxs-lookup"><span data-stu-id="a7e79-108">The demo data company used to create this task is USP2.</span></span>


## <a name="create-a-formula"></a><span data-ttu-id="a7e79-109">Opprette en formel</span><span class="sxs-lookup"><span data-stu-id="a7e79-109">Create a formula</span></span>
1. <span data-ttu-id="a7e79-110">Gå til Behandling av produktinformasjon > Stykklister og formler > Formler.</span><span class="sxs-lookup"><span data-stu-id="a7e79-110">Go to Product information management > Bills of materials and formulas > Formulas.</span></span>
2. <span data-ttu-id="a7e79-111">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="a7e79-111">Click New.</span></span>
3. <span data-ttu-id="a7e79-112">Skriv inn en verdi i feltet Formel.</span><span class="sxs-lookup"><span data-stu-id="a7e79-112">In the Formula field, type a value.</span></span>
4. <span data-ttu-id="a7e79-113">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="a7e79-113">In the Name field, type a value.</span></span>
    * <span data-ttu-id="a7e79-114">Skriv inn et relevant navn for formelen.</span><span class="sxs-lookup"><span data-stu-id="a7e79-114">Type a meaningful name for the formula.</span></span>  
5. <span data-ttu-id="a7e79-115">Klikk rullegardinknappen i Område-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="a7e79-115">In the Site field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="a7e79-116">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="a7e79-116">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="a7e79-117">Klikk rullegardinknappen i feltet Varegruppe for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="a7e79-117">In the Item group field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="a7e79-118">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="a7e79-118">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="a7e79-119">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="a7e79-119">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="a7e79-120">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="a7e79-120">Click Save.</span></span>

## <a name="copy-formula-lines"></a><span data-ttu-id="a7e79-121">Kopier formellinjer</span><span class="sxs-lookup"><span data-stu-id="a7e79-121">Copy formula lines</span></span>
1. <span data-ttu-id="a7e79-122">Klikk Formel i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="a7e79-122">On the Action Pane, click Formula.</span></span>
2. <span data-ttu-id="a7e79-123">Klikk Kopier.</span><span class="sxs-lookup"><span data-stu-id="a7e79-123">Click Copy.</span></span>
3. <span data-ttu-id="a7e79-124">Klikk rullegardinknappen i Varenummer-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="a7e79-124">In the Item number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="a7e79-125">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="a7e79-125">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="a7e79-126">Klikk rullegardinknappen i feltet Formelversjon for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="a7e79-126">In the Formula version field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="a7e79-127">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="a7e79-127">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="a7e79-128">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="a7e79-128">Click OK.</span></span>

## <a name="adjust-copied-formula-lines"></a><span data-ttu-id="a7e79-129">Juster kopierte formellinjer</span><span class="sxs-lookup"><span data-stu-id="a7e79-129">Adjust copied formula lines</span></span>
1. <span data-ttu-id="a7e79-130">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="a7e79-130">In the list, mark the selected row.</span></span>
2. <span data-ttu-id="a7e79-131">Klikk Slett.</span><span class="sxs-lookup"><span data-stu-id="a7e79-131">Click Delete.</span></span>
3. <span data-ttu-id="a7e79-132">Klikk Ja.</span><span class="sxs-lookup"><span data-stu-id="a7e79-132">Click Yes.</span></span>

## <a name="approve-formula"></a><span data-ttu-id="a7e79-133">Godkjenn formel</span><span class="sxs-lookup"><span data-stu-id="a7e79-133">Approve formula</span></span>
1. <span data-ttu-id="a7e79-134">Klikk Formel i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="a7e79-134">On the Action Pane, click Formula.</span></span>
2. <span data-ttu-id="a7e79-135">Klikk Godkjenn formel.</span><span class="sxs-lookup"><span data-stu-id="a7e79-135">Click Approve formula.</span></span>
3. <span data-ttu-id="a7e79-136">Klikk rullegardinknappen i Godkjent av-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="a7e79-136">In the Approved by field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="a7e79-137">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="a7e79-137">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="a7e79-138">Klikk Velg.</span><span class="sxs-lookup"><span data-stu-id="a7e79-138">Click Select.</span></span>
6. <span data-ttu-id="a7e79-139">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="a7e79-139">Click OK.</span></span>

