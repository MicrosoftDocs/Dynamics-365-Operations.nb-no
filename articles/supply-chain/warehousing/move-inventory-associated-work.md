---
title: Flytting av beholdning med tilknyttet arbeid i Lagerstyring
description: Dette emnet beskriver hvordan du definerer og bruker stykkplukkingsbekreftelse fra en mobilenhet.
author: Mirzaab
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorker
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3b58678ada7d6c3a2fb2af131418d2bb97ee5512
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5226033"
---
# <a name="movement-of-inventory-with-associated-work-in-warehouse-management"></a><span data-ttu-id="ad8f2-103">Flytting av beholdning med tilknyttet arbeid i Lagerstyring</span><span class="sxs-lookup"><span data-stu-id="ad8f2-103">Movement of inventory with associated work in Warehouse management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ad8f2-104">Ved hjelp av flytting av beholdning kan du bestemme hvilke lagermedarbeidere som har tillatelse til å flytte reservert beholdning.</span><span class="sxs-lookup"><span data-stu-id="ad8f2-104">Using movement of inventory, you can decide which warehouse workers are allowed to move reserved inventory.</span></span> <span data-ttu-id="ad8f2-105">Dette gir en fleksibilitet i regulerte lagre der du kan velge å ikke la en arbeider velge en ny plukklokasjon for plukkarbeid som allerede er opprettet.</span><span class="sxs-lookup"><span data-stu-id="ad8f2-105">This provides a flexibility in regulated warehouses where you can decide to not allow a worker to choose a new pick location for pick work that is already created.</span></span> <span data-ttu-id="ad8f2-106">Det kan også la en lagersjef styre hvilke funksjoner noen mindre erfarne arbeidere skal ha.</span><span class="sxs-lookup"><span data-stu-id="ad8f2-106">It also allows a warehouse manager to control which capabilities some less experienced workers should have.</span></span>

<span data-ttu-id="ad8f2-107">Fleksibilitet til å administrere lagerarbeidernes daglige oppgaver kan være nyttig i scenarier som disse:</span><span class="sxs-lookup"><span data-stu-id="ad8f2-107">The flexibility to manage the daily operations of warehouse workers can be useful in scenarios such as these:</span></span>

## <a name="scenario-1"></a><span data-ttu-id="ad8f2-108">Scenario 1</span><span class="sxs-lookup"><span data-stu-id="ad8f2-108">Scenario 1</span></span>
<span data-ttu-id="ad8f2-109">Et firma har et relativt lite mottaksområde, og det er overbelastet med paller og esker som venter på å bli plassert.</span><span class="sxs-lookup"><span data-stu-id="ad8f2-109">A company has a relatively small receiving area, and it’s congested with pallets and boxes awaiting put away.</span></span> <span data-ttu-id="ad8f2-110">Det forventes en stor forsendelse samme dag, så mottaksassistenten bestemmer seg for å rydde opp mottaksområdet ved å flytte noen av pallene til et sekundært innkommende oppsamlingsområde.</span><span class="sxs-lookup"><span data-stu-id="ad8f2-110">A large shipment is expected on the current day, so the receiving clerk decides to clear up the receiving area by moving some of the pallets to a secondary inbound staging area.</span></span>

## <a name="scenario-2"></a><span data-ttu-id="ad8f2-111">Scenario 2</span><span class="sxs-lookup"><span data-stu-id="ad8f2-111">Scenario 2</span></span>
<span data-ttu-id="ad8f2-112">En erfaren lagermedarbeider ser en salgsmulighet i et lager til å konsolidere varer på ett sted i stedet for å holde dem fordelt over 3 i lokasjoner nær hverandre med lite antall på hver.</span><span class="sxs-lookup"><span data-stu-id="ad8f2-112">An experienced warehouse worker notices an opportunity in a warehouse to consolidate items in one location instead of having them divided across 3 nearby locations with little quantity on each.</span></span> <span data-ttu-id="ad8f2-113">Arbeideren ønsker å konsolidere antallet ved å flytte varer fra hver av disse lokasjonen til den samme lokasjonen og på det samme nummerskiltet.</span><span class="sxs-lookup"><span data-stu-id="ad8f2-113">The worker wants to consolidate the quantity by moving items from each of these locations into the same location and onto the same license plate.</span></span>

## <a name="scenario-3"></a><span data-ttu-id="ad8f2-114">Scenario 3</span><span class="sxs-lookup"><span data-stu-id="ad8f2-114">Scenario 3</span></span>
<span data-ttu-id="ad8f2-115">En pall som venter på forsendelse på en oppsamlingslokasjon, for eksempel STADIUM01, som er nær RAMPEDØR01.</span><span class="sxs-lookup"><span data-stu-id="ad8f2-115">A pallet is awaiting shipment in a staging location, such as STAGE01, which is near BAYDOOR01.</span></span> <span data-ttu-id="ad8f2-116">På grunn av en endring i planene er imidlertid trucken satt til å ankomme RAMPEDØR04.</span><span class="sxs-lookup"><span data-stu-id="ad8f2-116">However, due to a change of plans the truck is scheduled to arrive at BAYDOOR04.</span></span> <span data-ttu-id="ad8f2-117">Forsendelsesassistenten er klar over dette, og må være forsikre seg om at trucken ikke må vente på å bli lastet fra STADIUM01.</span><span class="sxs-lookup"><span data-stu-id="ad8f2-117">The shipping clerk is aware of this and needs to ensure that the truck does not have to wait to be loaded from STAGE01.</span></span> <span data-ttu-id="ad8f2-118">Forsendelsesassistenten bestemmer seg for å flytte varene i den forsendelsen fra STADIUM01 til STADIUM04, som er nærmere til den nye plasseringen.</span><span class="sxs-lookup"><span data-stu-id="ad8f2-118">The shipping clerk decides to move the items in that shipment from STAGE01 to STAGE04, which is closer to the new destination.</span></span>

### <a name="current-limitations"></a><span data-ttu-id="ad8f2-119">Gjeldende begrensninger</span><span class="sxs-lookup"><span data-stu-id="ad8f2-119">Current limitations</span></span>

<span data-ttu-id="ad8f2-120">Arbeidsreservasjonene som du kan flytte, er begrenset til ordre, avgang for overføringsordre, mottak for overføringsordre, bestillinge og etterfyllingsarbeid.</span><span class="sxs-lookup"><span data-stu-id="ad8f2-120">The work reservations that you can move are limited to Sales order, Transfer order issue, Transfer order receipt, Purchase order, and Replenishment work.</span></span>

<span data-ttu-id="ad8f2-121">Flytting av varer er begrenset for å forhindre deling av arbeidslinjer.</span><span class="sxs-lookup"><span data-stu-id="ad8f2-121">Moving items is restricted to prevent splitting of work lines.</span></span> <span data-ttu-id="ad8f2-122">Dette betyr at hvis du har en arbeidslinje for 100 stk. av vare A fra lokasjon Lok1, kan du ikke flytte bare 30 stk. av vare A derfra til et annet sted.</span><span class="sxs-lookup"><span data-stu-id="ad8f2-122">This means that if you have a work line for 100 pcs of item A from location Loc1, you won’t be able to move only 30 pcs of item A from there to another location.</span></span> <span data-ttu-id="ad8f2-123">Dette vil føre til en deling av den eksisternde arbeidslinjen til 30 og 70 fordi lokasjonene nå er forskjellige.</span><span class="sxs-lookup"><span data-stu-id="ad8f2-123">This would lead to a split of the existing work line to 30 and 70, because the locations are now different.</span></span>

<span data-ttu-id="ad8f2-124">For oppsamlingsscenarier, der nummerskiltet du flytter varene fra eller nummerskiltet du flytter varene til, er angit som målnummerkilt for en arbeidsordre, er bare flytting av hele nummerskiltet tillatt, for å unngå å dele opp målnummerskiltet.</span><span class="sxs-lookup"><span data-stu-id="ad8f2-124">For staging scenarios, where the license plate you move the goods from or the license plate you move the goods to, are set as a Target LP for a work order, only movement of the entire LP is allowed, so as not to break up the Target LP.</span></span>
<span data-ttu-id="ad8f2-125">For tiden støttes bare ad hoc-bevegelser.</span><span class="sxs-lookup"><span data-stu-id="ad8f2-125">Only the ad hoc movement is currently supported.</span></span> <span data-ttu-id="ad8f2-126">Det betyr at du ikke vil kunne flytte reservert beholdning gjennom menyelementet Flytting etter mal i mobilenheten.</span><span class="sxs-lookup"><span data-stu-id="ad8f2-126">That means that you will not be able to move reserved inventory through the movement by template mobile device menu items.</span></span>

### <a name="set-up-permission-to-move-reserved-inventory-for-individual-workers"></a><span data-ttu-id="ad8f2-127">Konfigurer tillatelse til å flytte reservert inventar til enkelte arbeidstakere</span><span class="sxs-lookup"><span data-stu-id="ad8f2-127">Set up permission to move reserved inventory for individual workers</span></span>

<span data-ttu-id="ad8f2-128">For arbeideren som skal ha tillatelse til å flytte reservert beholdning, merker du av for **Tillat flytting av beholdning med tilknyttet arbeid** under **Lagerstyring** > **Oppsett** > **Arbeider**.</span><span class="sxs-lookup"><span data-stu-id="ad8f2-128">For the worker who should be allowed to move reserved inventory, select the **Allow movement of inventory with work associated** check box under **Warehouse management** > **Setup** > **Worker**.</span></span>  

### <a name="backported"></a><span data-ttu-id="ad8f2-129">Tilbakeføring</span><span class="sxs-lookup"><span data-stu-id="ad8f2-129">Backported</span></span>

<span data-ttu-id="ad8f2-130">Denne funksjonen er også tilbakeført til Microsoft Dynamics AX 2012 R3 og er tilgjengelig som en del av CU12.</span><span class="sxs-lookup"><span data-stu-id="ad8f2-130">This feature has also been back-ported to Microsoft Dynamics AX 2012 R3 and will be available as part of CU12.</span></span>
<span data-ttu-id="ad8f2-131">Den kan også lastes ned alene gjennom KB-nummer 3192548.</span><span class="sxs-lookup"><span data-stu-id="ad8f2-131">It can also be downloaded individually through KB number 3192548.</span></span> 



[!INCLUDE[footer-include](../../includes/footer-banner.md)]