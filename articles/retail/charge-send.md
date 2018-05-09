---
title: Sende en ordre fra en annen butikk
description: Dette emnet beskriver sendefunksjonen Tillegg.
author: ashishmsft
manager: AnnBe
ms.date: 10/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-10-10
ms.dyn365.ops.version: Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 2796ef1a9c312f86c878dd72fa26dcb45c88ed88
ms.contentlocale: nb-no
ms.lasthandoff: 05/08/2018

---

# <a name="ship-an-order-from-a-different-store"></a><span data-ttu-id="79f0a-103">Sende en ordre fra en annen butikk</span><span class="sxs-lookup"><span data-stu-id="79f0a-103">Ship an order from a different store</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="79f0a-104">Med sendefunksjonen Tillegg i Dynamics 365 for Retail kan kundeordrer registreres i én butikk og sendes fra en annen butikk.</span><span class="sxs-lookup"><span data-stu-id="79f0a-104">With the Charge send feature in Dynamics 365 for Retail, customer orders can be placed in one store and shipped from another store.</span></span> <span data-ttu-id="79f0a-105">Kundeordrer i salgsstedsklienten støtter flere fullføringsalternativer.</span><span class="sxs-lookup"><span data-stu-id="79f0a-105">Customer orders in the point of sale (POS) client support multiple fulfillment options.</span></span> <span data-ttu-id="79f0a-106">Eksempler på fullføringsalternativer:</span><span class="sxs-lookup"><span data-stu-id="79f0a-106">Some examples of fulfillment options include:</span></span>
-   <span data-ttu-id="79f0a-107">Henting fra samme butikk på en annen dato.</span><span class="sxs-lookup"><span data-stu-id="79f0a-107">Pick up from the same store on a different date.</span></span>
-   <span data-ttu-id="79f0a-108">Henting fra en annen butikk på samme eller en annen dato.</span><span class="sxs-lookup"><span data-stu-id="79f0a-108">Pick up from a different store on the same date or a different date.</span></span>
-   <span data-ttu-id="79f0a-109">Sending fra standard leveringslager som er tilordnet til butikken, og levering på en bestemt dato.</span><span class="sxs-lookup"><span data-stu-id="79f0a-109">Ship from the default shipping warehouse that is assigned to the store, and deliver on a specific date.</span></span>

<span data-ttu-id="79f0a-110">Sendefunksjonen Tillegg bruker følgende POS-operasjoner: Lever alle produkter og lever valgte produkter.</span><span class="sxs-lookup"><span data-stu-id="79f0a-110">The Charge send feature uses the following POS operations: Ship all products and Ship selected products.</span></span> <span data-ttu-id="79f0a-111">Dette lar butikkbetjeningen velge "send fra"-lokasjon som ordren eller ordrelinjen kan fullføres fra.</span><span class="sxs-lookup"><span data-stu-id="79f0a-111">This allows the store clerk to select the “ship from” location that the order or order line can be fulfilled from.</span></span> <span data-ttu-id="79f0a-112">Som standard er "send fra"-lokasjonen leveringslageret som er tilknyttet butikken.</span><span class="sxs-lookup"><span data-stu-id="79f0a-112">By default, the “ship from” location is the shipping warehouse that is associated with the store.</span></span> <span data-ttu-id="79f0a-113">Butikkbetjeningen kan imidlertid endre denne lokasjonen og velge alle butikker som er definert i butikklokatorgruppen som er tilordnet butikken.</span><span class="sxs-lookup"><span data-stu-id="79f0a-113">However, the store clerk can change this location and select any store that is defined in the store locator group that is assigned to the store.</span></span> 

<span data-ttu-id="79f0a-114">Muligheten til å velge "send til"-adresser forblir uendret.</span><span class="sxs-lookup"><span data-stu-id="79f0a-114">The ability to select “ship to” addresses remains unchanged.</span></span> 

<span data-ttu-id="79f0a-115">Leveringsmetodene som kan brukes til å tilfredsstille ordrelinjen, er basert på konfigurasjonen av gyldig leveringsmåter for produkter og adresser.</span><span class="sxs-lookup"><span data-stu-id="79f0a-115">The shipping methods that can be used to fulfill the order line are based on the configuration of valid modes of delivery for products and addresses.</span></span> <span data-ttu-id="79f0a-116">Fordi reglene om gyldig av leveringsmåter vedlikeholdes i Detaljhandel hovedkontor, utfører POS-klienten kall i sanntid for å hente de gyldige leveringsmåtene for en leveringslinje.</span><span class="sxs-lookup"><span data-stu-id="79f0a-116">Because the rules about valid of modes of delivery are maintained only in the Retail headquarters (HQ), the POS client makes a real-time call to fetch the valid modes of delivery for a ship line.</span></span> 


