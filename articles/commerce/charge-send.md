---
title: Sende ordrer fra et annet lager ved hjelp av sendefunksjonen Tillegg
description: Dette emnet beskriver sendefunksjonen Tillegg.
author: ashishmsft
manager: AnnBe
ms.date: 10/10/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-10-10
ms.dyn365.ops.version: Retail July 2017 update
ms.openlocfilehash: 0bbebcc7b2ab89bf2f5db7294acfca1d8a5ad96e
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023510"
---
# <a name="ship-orders-from-another-store-by-using-the-charge-send-feature"></a><span data-ttu-id="c11b2-103">Sende ordrer fra et annet lager ved hjelp av sendefunksjonen Tillegg</span><span class="sxs-lookup"><span data-stu-id="c11b2-103">Ship orders from another store by using the Charge send feature</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c11b2-104">Med sendefunksjonen Tillegg i Commerce kan kundeordrer registreres i én butikk og sendes fra en annen butikk.</span><span class="sxs-lookup"><span data-stu-id="c11b2-104">With the Charge send feature in Commerce, customer orders can be placed in one store and shipped from another store.</span></span>

<span data-ttu-id="c11b2-105">Kundeordrer i salgsstedsklienten støtter flere fullføringsalternativer.</span><span class="sxs-lookup"><span data-stu-id="c11b2-105">Customer orders in the point of sale (POS) client support multiple fulfillment options.</span></span> <span data-ttu-id="c11b2-106">Eksempler på fullføringsalternativer:</span><span class="sxs-lookup"><span data-stu-id="c11b2-106">Some examples of fulfillment options include:</span></span>

- <span data-ttu-id="c11b2-107">Henting fra samme butikk på en annen dato.</span><span class="sxs-lookup"><span data-stu-id="c11b2-107">Pick up from the same store on a different date.</span></span>
- <span data-ttu-id="c11b2-108">Henting fra en annen butikk på samme eller en annen dato.</span><span class="sxs-lookup"><span data-stu-id="c11b2-108">Pick up from a different store on the same date or a different date.</span></span>
- <span data-ttu-id="c11b2-109">Sending fra standard leveringslager som er tilordnet til butikken, og levering på en bestemt dato.</span><span class="sxs-lookup"><span data-stu-id="c11b2-109">Ship from the default shipping warehouse that is assigned to the store, and deliver on a specific date.</span></span>

<span data-ttu-id="c11b2-110">Sendefunksjonen Tillegg bruker følgende POS-operasjoner: Lever alle produkter og lever valgte produkter.</span><span class="sxs-lookup"><span data-stu-id="c11b2-110">The Charge send feature uses the following POS operations: Ship all products and Ship selected products.</span></span> <span data-ttu-id="c11b2-111">Dette lar butikkbetjeningen velge "send fra"-lokasjon som ordren eller ordrelinjen kan fullføres fra.</span><span class="sxs-lookup"><span data-stu-id="c11b2-111">This allows the store clerk to select the "ship from" location that the order or order line can be fulfilled from.</span></span> <span data-ttu-id="c11b2-112">Som standard er "send fra"-lokasjonen leveringslageret som er tilknyttet butikken.</span><span class="sxs-lookup"><span data-stu-id="c11b2-112">By default, the "ship from" location is the shipping warehouse that is associated with the store.</span></span> <span data-ttu-id="c11b2-113">Butikkbetjeningen kan imidlertid endre denne lokasjonen og velge alle butikker som er definert i butikklokatorgruppen som er tilordnet butikken.</span><span class="sxs-lookup"><span data-stu-id="c11b2-113">However, the store clerk can change this location and select any store that is defined in the store locator group that is assigned to the store.</span></span>

<span data-ttu-id="c11b2-114">Muligheten til å velge "send til"-adresser forblir uendret.</span><span class="sxs-lookup"><span data-stu-id="c11b2-114">The ability to select "ship to" addresses remains unchanged.</span></span>

<span data-ttu-id="c11b2-115">Leveringsmetodene som kan brukes til å tilfredsstille ordrelinjen, er basert på konfigurasjonen av gyldig leveringsmåter for produkter og adresser.</span><span class="sxs-lookup"><span data-stu-id="c11b2-115">The shipping methods that can be used to fulfill the order line are based on the configuration of valid modes of delivery for products and addresses.</span></span> <span data-ttu-id="c11b2-116">Fordi reglene om gyldig av leveringsmåter vedlikeholdes i hovedkontoret, utfører POS-klienten kall i sanntid for å hente de gyldige leveringsmåtene for en leveringslinje.</span><span class="sxs-lookup"><span data-stu-id="c11b2-116">Because the rules about valid of modes of delivery are maintained only in the Headquarters (HQ), the POS client makes a real-time call to fetch the valid modes of delivery for a ship line.</span></span>