---
title: Opprette konfigurasjonsregler
description: Denne prosedyren oppretter konfigurasjonsregler som kan brukes til dimensjonsbasert konfigurasjon for å fremtvinge eller nekte bestemte kombinasjoner av stykklistelinjer.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BOMTable, BOMConfigRule, ConfigItemIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 21cdca1c33b106bd153a436a7fec4f0eeaa0d620
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5820064"
---
# <a name="create-configuration-rules"></a><span data-ttu-id="c5f8c-103">Opprette konfigurasjonsregler</span><span class="sxs-lookup"><span data-stu-id="c5f8c-103">Create configuration rules</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c5f8c-104">Denne prosedyren oppretter konfigurasjonsregler som kan brukes til dimensjonsbasert konfigurasjon for å fremtvinge eller nekte bestemte kombinasjoner av stykklistelinjer.</span><span class="sxs-lookup"><span data-stu-id="c5f8c-104">This procedure creates configuration rules that can be used for dimension-based configuration to enforce or prevent certain combinations of BOM lines.</span></span> <span data-ttu-id="c5f8c-105">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="c5f8c-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="c5f8c-106">Dette er den sjuende fremgangsmåten av åtte som forklarer hvordan du bygger kombinasjoner for dimensjonsbasert konfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="c5f8c-106">This is the seventh procedure out of eight that explains how to build combinations for dimension-based configuration.</span></span>

1. <span data-ttu-id="c5f8c-107">Gå til Behandling av produktinformasjon > Stykklister og formler > Stykklister.</span><span class="sxs-lookup"><span data-stu-id="c5f8c-107">Go to Product information management > Bills of materials and formulas > Bills of materials.</span></span>
2. <span data-ttu-id="c5f8c-108">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="c5f8c-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="c5f8c-109">Søk etter og velg stykklisten for den dimensjonsbaserte konfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="c5f8c-109">Find and select the BOM for the dimension-based configuration.</span></span>  
3. <span data-ttu-id="c5f8c-110">Klikk på Alternativer i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="c5f8c-110">On the Action Pane, click Options.</span></span>
4. <span data-ttu-id="c5f8c-111">Klikk på Bytt visning.</span><span class="sxs-lookup"><span data-stu-id="c5f8c-111">Click Change view.</span></span>
5. <span data-ttu-id="c5f8c-112">Klikk på Hodevisning.</span><span class="sxs-lookup"><span data-stu-id="c5f8c-112">Click Header view.</span></span>
    * <span data-ttu-id="c5f8c-113">Åpne hodevisningen for å få tilgang til hurtigfanen Konfigurasjonsrute.</span><span class="sxs-lookup"><span data-stu-id="c5f8c-113">Open the header view to access the Configuration route FastTab.</span></span>  
6. <span data-ttu-id="c5f8c-114">Vis eller skjul delen Konfigurasjonsrute.</span><span class="sxs-lookup"><span data-stu-id="c5f8c-114">Expand or collapse the Configuration route section.</span></span>
    * <span data-ttu-id="c5f8c-115">Hurtigfanen Konfigurasjonsrute må være i utvidet modus.</span><span class="sxs-lookup"><span data-stu-id="c5f8c-115">The Configuration route FastTab must be in the expanded mode.</span></span>  
7. <span data-ttu-id="c5f8c-116">Klikk på Konfigurasjonsregler.</span><span class="sxs-lookup"><span data-stu-id="c5f8c-116">Click Configuration rules.</span></span>
8. <span data-ttu-id="c5f8c-117">Klikk på Ny.</span><span class="sxs-lookup"><span data-stu-id="c5f8c-117">Click New.</span></span>
9. <span data-ttu-id="c5f8c-118">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="c5f8c-118">In the list, mark the selected row.</span></span>
10. <span data-ttu-id="c5f8c-119">Klikk på rullegardinknappen i Varenummer-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="c5f8c-119">In the Item number field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="c5f8c-120">Varene i den gjeldende konfigurasjonsgruppen vises.</span><span class="sxs-lookup"><span data-stu-id="c5f8c-120">The items in the current configuration group are displayed.</span></span> <span data-ttu-id="c5f8c-121">Velg den som representerer betingelsen i regelen.</span><span class="sxs-lookup"><span data-stu-id="c5f8c-121">Select the one that represents the condition in the rule.</span></span>  
11. <span data-ttu-id="c5f8c-122">Klikk på koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="c5f8c-122">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="c5f8c-123">Velg et alternativ i Metode-feltet.</span><span class="sxs-lookup"><span data-stu-id="c5f8c-123">In the Method field, select an option.</span></span>
    * <span data-ttu-id="c5f8c-124">Det er mulig å fremtvinge et valg eller en opphevelse av valg av en vare fra en annen konfigurasjonsgruppe.</span><span class="sxs-lookup"><span data-stu-id="c5f8c-124">It is possible to enforce either a selection or a deselection of an item from another configuration group.</span></span>  
13. <span data-ttu-id="c5f8c-125">Klikk på rullegardinknappen i feltet Avledet gruppe for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="c5f8c-125">In the Derived group field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="c5f8c-126">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="c5f8c-126">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="c5f8c-127">Klikk på koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="c5f8c-127">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="c5f8c-128">Velg ønsket konfigurasjonsgruppe.</span><span class="sxs-lookup"><span data-stu-id="c5f8c-128">Select the desired configuration group.</span></span>  
16. <span data-ttu-id="c5f8c-129">Klikk på rullegardinknappen i feltet Avledet varenummer for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="c5f8c-129">In the Derived item number field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="c5f8c-130">Klikk på koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="c5f8c-130">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="c5f8c-131">Velg varenummeret som enten skal velges eller oppheves avhengig av den valgte metoden.</span><span class="sxs-lookup"><span data-stu-id="c5f8c-131">Select the item number that will be either selected or deselected depending on the chosen method.</span></span>  
18. <span data-ttu-id="c5f8c-132">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="c5f8c-132">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]