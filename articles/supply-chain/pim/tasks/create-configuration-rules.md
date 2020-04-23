---
title: Opprette konfigurasjonsregler
description: Denne prosedyren oppretter konfigurasjonsregler som kan brukes til dimensjonsbasert konfigurasjon for å fremtvinge eller nekte bestemte kombinasjoner av stykklistelinjer.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMTable, BOMConfigRule, ConfigItemIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c53ea2eea7dfe3c02d1b21964decc6630d3a41cf
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/02/2020
ms.locfileid: "3208277"
---
# <a name="create-configuration-rules"></a><span data-ttu-id="3904f-103">Opprette konfigurasjonsregler</span><span class="sxs-lookup"><span data-stu-id="3904f-103">Create configuration rules</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3904f-104">Denne prosedyren oppretter konfigurasjonsregler som kan brukes til dimensjonsbasert konfigurasjon for å fremtvinge eller nekte bestemte kombinasjoner av stykklistelinjer.</span><span class="sxs-lookup"><span data-stu-id="3904f-104">This procedure creates configuration rules that can be used for dimension-based configuration to enforce or prevent certain combinations of BOM lines.</span></span> <span data-ttu-id="3904f-105">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="3904f-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="3904f-106">Dette er den sjuende fremgangsmåten av åtte som forklarer hvordan du bygger kombinasjoner for dimensjonsbasert konfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="3904f-106">This is the seventh procedure out of eight that explains how to build combinations for dimension-based configuration.</span></span>

1. <span data-ttu-id="3904f-107">Gå til Behandling av produktinformasjon > Stykklister og formler > Stykklister.</span><span class="sxs-lookup"><span data-stu-id="3904f-107">Go to Product information management > Bills of materials and formulas > Bills of materials.</span></span>
2. <span data-ttu-id="3904f-108">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="3904f-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="3904f-109">Søk etter og velg stykklisten for den dimensjonsbaserte konfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="3904f-109">Find and select the BOM for the dimension-based configuration.</span></span>  
3. <span data-ttu-id="3904f-110">Klikk Alternativer i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="3904f-110">On the Action Pane, click Options.</span></span>
4. <span data-ttu-id="3904f-111">Klikk Bytt visning.</span><span class="sxs-lookup"><span data-stu-id="3904f-111">Click Change view.</span></span>
5. <span data-ttu-id="3904f-112">Klikk Hodevisning.</span><span class="sxs-lookup"><span data-stu-id="3904f-112">Click Header view.</span></span>
    * <span data-ttu-id="3904f-113">Åpne hodevisningen for å få tilgang til hurtigkategorien Konfigurasjonsrute.</span><span class="sxs-lookup"><span data-stu-id="3904f-113">Open the header view to access the Configuration route FastTab.</span></span>  
6. <span data-ttu-id="3904f-114">Vis eller skjul delen Konfigurasjonsrute.</span><span class="sxs-lookup"><span data-stu-id="3904f-114">Expand or collapse the Configuration route section.</span></span>
    * <span data-ttu-id="3904f-115">Hurtigkategorien Konfigurasjonsrute må være i utvidet modus.</span><span class="sxs-lookup"><span data-stu-id="3904f-115">The Configuration route FastTab must be in the expanded mode.</span></span>  
7. <span data-ttu-id="3904f-116">Klikk Konfigurasjonsregler.</span><span class="sxs-lookup"><span data-stu-id="3904f-116">Click Configuration rules.</span></span>
8. <span data-ttu-id="3904f-117">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="3904f-117">Click New.</span></span>
9. <span data-ttu-id="3904f-118">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="3904f-118">In the list, mark the selected row.</span></span>
10. <span data-ttu-id="3904f-119">Klikk rullegardinknappen i Varenummer-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="3904f-119">In the Item number field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="3904f-120">Varene i den gjeldende konfigurasjonsgruppen vises.</span><span class="sxs-lookup"><span data-stu-id="3904f-120">The items in the current configuration group are displayed.</span></span> <span data-ttu-id="3904f-121">Velg den som representerer betingelsen i regelen.</span><span class="sxs-lookup"><span data-stu-id="3904f-121">Select the one that represents the condition in the rule.</span></span>  
11. <span data-ttu-id="3904f-122">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="3904f-122">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="3904f-123">Velg et alternativ i Metode-feltet.</span><span class="sxs-lookup"><span data-stu-id="3904f-123">In the Method field, select an option.</span></span>
    * <span data-ttu-id="3904f-124">Det er mulig å fremtvinge et valg eller en opphevelse av valg av en vare fra en annen konfigurasjonsgruppe.</span><span class="sxs-lookup"><span data-stu-id="3904f-124">It is possible to enforce either a selection or a deselection of an item from another configuration group.</span></span>  
13. <span data-ttu-id="3904f-125">Klikk rullegardinknappen i feltet Avledet gruppe for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="3904f-125">In the Derived group field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="3904f-126">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="3904f-126">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="3904f-127">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="3904f-127">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="3904f-128">Velg ønsket konfigurasjonsgruppe.</span><span class="sxs-lookup"><span data-stu-id="3904f-128">Select the desired configuration group.</span></span>  
16. <span data-ttu-id="3904f-129">Klikk rullegardinknappen i feltet Avledet varenummer for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="3904f-129">In the Derived item number field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="3904f-130">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="3904f-130">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="3904f-131">Velg varenummeret som enten skal velges eller oppheves avhengig av den valgte metoden.</span><span class="sxs-lookup"><span data-stu-id="3904f-131">Select the item number that will be either selected or deselected depending on the chosen method.</span></span>  
18. <span data-ttu-id="3904f-132">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="3904f-132">Close the page.</span></span>

