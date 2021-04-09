---
title: Forbedret håndtering av varer med partisporing
description: Dette emnet beskriver forbedringene som er gjort i håndteringen av partier for varer med partisporing under posteringsprosessen for utdrag.
author: josaw1
ms.date: 11/04/2019
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-05-28
ms.dyn365.ops.version: 10
ms.openlocfilehash: 2453ed711d47e062c82d3888ff471b770b5bb2ef
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799715"
---
# <a name="improved-handling-of-batch-tracked-items"></a><span data-ttu-id="09f23-103">Forbedret håndtering av varer med partisporing</span><span class="sxs-lookup"><span data-stu-id="09f23-103">Improved handling of batch-tracked items</span></span>


[!include [banner](includes/banner.md)]


<span data-ttu-id="09f23-104">På salgsstedet kan ikke partinumre registreres for varer med partisporing på salgstidspunktet.</span><span class="sxs-lookup"><span data-stu-id="09f23-104">In Point of Sale (POS), batch numbers can't be captured for batch-tracked items at the time of sale.</span></span> <span data-ttu-id="09f23-105">For bestemte konfigurasjoner imidlertid, når salg posteres på hovedkontoret via kundeordrer eller utdragspostering, forventer Microsoft Dynamics-systemet at det finnes gyldige partinumre for varer med partisporing, og at de skal brukes under faktureringen.</span><span class="sxs-lookup"><span data-stu-id="09f23-105">However, for specific configurations, when sales are posted in the headquarters through customer orders or statement posting, the Microsoft Dynamics system expects that valid batch numbers for batch-tracked items exist, and that they will be used during the invoicing process.</span></span>

<span data-ttu-id="09f23-106">Hvis det finnes gyldige partinumre for produktene, brukes de i kundeordrefaktureringen og salgsordrefaktureringen fra utdragspostering.</span><span class="sxs-lookup"><span data-stu-id="09f23-106">If valid batch numbers are available for products, the customer order invoicing process and the sales order invoicing process from statement posting use them.</span></span> <span data-ttu-id="09f23-107">Ellers kan ikke kundeordrefaktureringen postere, og salgsstedsbrukeren får en feilmelding.</span><span class="sxs-lookup"><span data-stu-id="09f23-107">Otherwise, the customer order invoicing process can't post, and the POS user receives an error message.</span></span> <span data-ttu-id="09f23-108">Utdragspostering går deretter inn i en feiltilstand.</span><span class="sxs-lookup"><span data-stu-id="09f23-108">Statement posting then goes into an error state.</span></span> <span data-ttu-id="09f23-109">Denne feiltilstanden forekommer selv om negativ beholdning er aktivert for produktene.</span><span class="sxs-lookup"><span data-stu-id="09f23-109">This error state occurs even when negative inventory has been turned on for the products.</span></span>

<span data-ttu-id="09f23-110">Når negativ beholdning er aktivert for varer med partisporing, sikrer forbedringene som er gjort i Retail versjon 10.0.4 og senere, at kundeordrefakturering og salgsordrefakturering via utdragspostering ikke blokkeres for disse varene hvis beholdningen er 0 (null) eller det ikke finnes et partinummer.</span><span class="sxs-lookup"><span data-stu-id="09f23-110">Improvements that have been made in Retail version 10.0.4 and later help guarantee that, when negative inventory is turned on for batch-tracked items, customer order invoicing and sales order invoicing through statement posting aren't blocked for those items if the inventory is 0 (zero) or a batch number isn't available.</span></span> <span data-ttu-id="09f23-111">Den nye funksjonaliteten bruker en standard parti-ID for salgslinjene når partinumre ikke er tilgjengelige.</span><span class="sxs-lookup"><span data-stu-id="09f23-111">The new functionality uses a default batch ID for the sales lines when batch numbers aren't available.</span></span>

<span data-ttu-id="09f23-112">Hvis du vil definere standard parti-ID som brukes for kundeordrer, angir du feltet **Standard parti-ID** i hurtigfanen **Ordre** i fanen **Kundeordrer** på siden **Handelsparametere**.</span><span class="sxs-lookup"><span data-stu-id="09f23-112">To define the default batch ID that is used for customer orders, on the **Commerce parameters** page, on the **Customer orders** tab, on the **Order** FastTab, set the **Default batch id** field.</span></span>

<span data-ttu-id="09f23-113">Hvis du vil definere standard parti-ID som brukes for salgsordrefakturering via utdragspostering, angir du feltet **Standard parti-ID** i hurtigfanen **Lageroppdatering** i fanen **Postering** på siden **Handelsparametere**.</span><span class="sxs-lookup"><span data-stu-id="09f23-113">To define the default batch ID that is used for sales order invoicing through statement posting, on the **Commerce parameters** page, on the **Posting** tab, on the **Inventory update** FastTab, set the **Default batch id** field.</span></span>

> [!NOTE]
> <span data-ttu-id="09f23-114">Denne funksjonaliteten er bare tilgjengelig når avanserte lageraktiviteter er aktivert for det spesifikke butikklageret og varene.</span><span class="sxs-lookup"><span data-stu-id="09f23-114">This functionality is available only when advanced warehousing is turned on for the specific store warehouse and items.</span></span> <span data-ttu-id="09f23-115">I en senere versjon vil funksjonaliteten også støttes for scenarioer der avansert lagerstyring ikke brukes.</span><span class="sxs-lookup"><span data-stu-id="09f23-115">In a later release, the functionality will also be supported for scenarios where advanced warehouse management isn't used.</span></span>

> [!NOTE]
> <span data-ttu-id="09f23-116">Støtte for forbedret håndtering av satsvise varer under utdragspostering for ikke-avanserte lagerstyringsscenarier ble innført i Retail versjon 10.0.5.</span><span class="sxs-lookup"><span data-stu-id="09f23-116">Support for improved handling of batch-tracked items during statement posting for non-advanced warehouse management scenarios was introduced in Retail version 10.0.5.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]