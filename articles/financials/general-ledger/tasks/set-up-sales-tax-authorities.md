--- 
title: Definere skattemyndigheter
description: Skattemyndighetene er enheter som innsamlet merverdiavgift skal rapporteres og betales til.
author: twheeloc
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 3c5c8f8b01b1e48856b45e3c81df5671a1a36935
ms.contentlocale: nb-no
ms.lasthandoff: 04/13/2018

---
# <a name="set-up-sales-tax-authorities"></a><span data-ttu-id="f9401-103">Definere skattemyndigheter</span><span class="sxs-lookup"><span data-stu-id="f9401-103">Set up sales tax authorities</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f9401-104">Skattemyndighetene er enheter som innsamlet merverdiavgift skal rapporteres og betales til.</span><span class="sxs-lookup"><span data-stu-id="f9401-104">Sales tax authorities are entities to which collected sales tax needs to be reported and paid.</span></span> <span data-ttu-id="f9401-105">Du kan betale merverdiavgift til myndigheten direkte eller via en leverandørkonto som du oppretter for skattemyndigheten.</span><span class="sxs-lookup"><span data-stu-id="f9401-105">You can pay sales taxes to the authority directly or through a vendor account that you create for the sales tax authority.</span></span> <span data-ttu-id="f9401-106">Hvis du gjør dette, kan firmaet bruke sine vanlige betalingsrutiner til å betale skattemyndigheten til rett tid.</span><span class="sxs-lookup"><span data-stu-id="f9401-106">If you do this, the company can use its usual payment routines to pay the sales tax authority on time.</span></span> <span data-ttu-id="f9401-107">Hvis du ikke angir skattemyndigheten som en leverandør, må noen klargjøre en manuell betaling til skattemyndigheten på riktig forfallsdato.</span><span class="sxs-lookup"><span data-stu-id="f9401-107">If you do not set up the tax authority as a vendor, someone must prepare a manual payment to the tax authority on the appropriate due date.</span></span> <span data-ttu-id="f9401-108">Denne oppgaven bruker demonstrasjonsfirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="f9401-108">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="f9401-109">Gå til Avgift > Indirekte avgifter > Merverdiavgift > Skattemyndigheter.</span><span class="sxs-lookup"><span data-stu-id="f9401-109">Go to Tax > Indirect taxes > Sales tax > Sales tax authorities.</span></span>
2. <span data-ttu-id="f9401-110">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="f9401-110">Click New.</span></span>
3. <span data-ttu-id="f9401-111">Skriv inn en verdi i Skattemyndighet-feltet.</span><span class="sxs-lookup"><span data-stu-id="f9401-111">In the Authority field, type a value.</span></span>
4. <span data-ttu-id="f9401-112">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="f9401-112">In the Name field, type a value.</span></span>
5. <span data-ttu-id="f9401-113">Klikk rullegardinknappen i Leverandørkonto-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="f9401-113">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="f9401-114">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="f9401-114">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="f9401-115">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="f9401-115">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="f9401-116">Velg rapportoppsettet for ditt land/din region hvis det er aktuelt.</span><span class="sxs-lookup"><span data-stu-id="f9401-116">Select the report layout for your country/region, if one is available.</span></span> <span data-ttu-id="f9401-117">Hvis rapportoppsettene ikke samsvarer med kravene til skattemyndighetene, kan du bruke standardoppsett.</span><span class="sxs-lookup"><span data-stu-id="f9401-117">If the report layouts do not correspond to the requirements of the sales tax authority, use default layout.</span></span>
9. <span data-ttu-id="f9401-118">Angi verdier i avrundingsformen og avrundingsfeltene for å angi hvordan det totale avgiftsbeløpet som skal betales, skal avrundes.</span><span class="sxs-lookup"><span data-stu-id="f9401-118">Enter values in the Rounding form and the Round-off fields to specify how the tax total amount to be paid should be rounded.</span></span> <span data-ttu-id="f9401-119">Alle avrundingsdifferanser skal posteres til Kontoer for automatiske transaksjoner angitt i Økonomimodul.</span><span class="sxs-lookup"><span data-stu-id="f9401-119">Any rounding differences will be posted to Accounts for automatic transactions set up in General ledger.</span></span>
10. <span data-ttu-id="f9401-120">Angi et tall i Avrund-feltet.</span><span class="sxs-lookup"><span data-stu-id="f9401-120">In the Round-off field, enter a number.</span></span>
11. <span data-ttu-id="f9401-121">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="f9401-121">Click Save.</span></span>


