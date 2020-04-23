---
title: Stykkplukkingsbekreftelse
description: Dette emnet beskriver hvordan du definerer og bruker stykkplukkingsbekreftelse fra en mobilenhet.
author: Mirzaab
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFAutoConfirm, WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ed63245066799d7d8f14362ab6c9193c0cda7c4a
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215612"
---
# <a name="piece-picking-confirmation"></a><span data-ttu-id="a17ee-103">Stykkplukkingsbekreftelse</span><span class="sxs-lookup"><span data-stu-id="a17ee-103">Piece picking confirmation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a17ee-104">Med stykkplukking kan du bekrefte hver del av lagerbeholdningen gjennom plukkings- og tellingsarbeid på en mobil enhet.</span><span class="sxs-lookup"><span data-stu-id="a17ee-104">Piece picking allows you to confirm each piece of inventory through picking or counting work on a mobile device.</span></span> <span data-ttu-id="a17ee-105">For plukking kan du kontrollere hvor mye arbeid som skal behandles opptil antallet som er angitt på arbeid som skal plukkes.</span><span class="sxs-lookup"><span data-stu-id="a17ee-105">For picks, you can confirm the quantity of work to be processed up to the quantity that is specified on work to be picked.</span></span> <span data-ttu-id="a17ee-106">For opptellingsarbeid kan du skanne lageret du teller opp, og spore totalbeløpet.</span><span class="sxs-lookup"><span data-stu-id="a17ee-106">For counting work, you can scan the inventory that you are counting and track the total amount.</span></span>

<span data-ttu-id="a17ee-107">Når du aktiverer stykkplukking, velges produktbekreftelse automatisk.</span><span class="sxs-lookup"><span data-stu-id="a17ee-107">When you enable piece picking, product confirmation is automatically selected.</span></span> <span data-ttu-id="a17ee-108">For arbeidstypen plukk aktiveres et maksimalt antall stykker.</span><span class="sxs-lookup"><span data-stu-id="a17ee-108">For work-type picks, a maximum number of pieces is enabled.</span></span> <span data-ttu-id="a17ee-109">Dette gjør at du kan angi et maksimalt antall enheter som må bekreftes under arbeidsprosessen.</span><span class="sxs-lookup"><span data-stu-id="a17ee-109">This allows you to set a maximum to the number of pieces that must be confirmed during the work process.</span></span> <span data-ttu-id="a17ee-110">Maksimalt antall er basert på den gjeldende arbeidsenheten som behandles.</span><span class="sxs-lookup"><span data-stu-id="a17ee-110">The maximum quantity is based on the current work unit that is being processed.</span></span> <span data-ttu-id="a17ee-111">Opptellingsarbeidstypen tillater ikke et maksimum.</span><span class="sxs-lookup"><span data-stu-id="a17ee-111">The counting work type does not allow a maximum.</span></span>

<span data-ttu-id="a17ee-112">Du kan også bruke antall og måleenhet som er tilknyttet en skannet strekkode.</span><span class="sxs-lookup"><span data-stu-id="a17ee-112">You can also use the quantity and unit of measure (UOM) that is associated with a scanned bar code.</span></span> <span data-ttu-id="a17ee-113">Dette vil fungere for mottak på innkommende flyter inkludert mottak av kombinerte skiltnumre, bestillingsvare, overføringsordrevare og lastvare.</span><span class="sxs-lookup"><span data-stu-id="a17ee-113">This will work for receiving on inbound flows including mixed license plate receiving, purchase order item, transfer order item, and load item.</span></span> <span data-ttu-id="a17ee-114">Det fungerer også for stykkplukking der skanning av strekkoden vil legge til antallet i totalt antall bekreftede stykker som er konvertert mellom måleenheten på strekkoden og arbeidsenheten.</span><span class="sxs-lookup"><span data-stu-id="a17ee-114">It also works for piece picking where scanning the bar code will add the quantity to the total number of confirmed pieces converting between the UOM on the bar code and the work unit.</span></span> <span data-ttu-id="a17ee-115">Hvis det, ved telling av måleenheten på strekkoden, bekreftes at antallet er tillatt for opptelling på sekvensgruppen, legges antallet til totalantallet.</span><span class="sxs-lookup"><span data-stu-id="a17ee-115">If, when counting the UOM on the bar code, it is confirmed that the quantity is allowed for counting on the sequence group, the quantity will be added to the total count.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="a17ee-116">Der det er aktuelt</span><span class="sxs-lookup"><span data-stu-id="a17ee-116">Where it applies</span></span>

<span data-ttu-id="a17ee-117">Stykkplukking fungerer for alt opptellingsarbeid og for første plukking for alle typer arbeid.</span><span class="sxs-lookup"><span data-stu-id="a17ee-117">Piece picking works for all counting work and for the initial pick for any type of work.</span></span> <span data-ttu-id="a17ee-118">Stykkplukking gjelder ikke hvis varen styres av serienumre eller hvis det er en produksjons- eller kanbanplukking fra en nummerskiltlokasjon og varen er satt til oppsamling.</span><span class="sxs-lookup"><span data-stu-id="a17ee-118">Piece picking does not apply if the item is controlled by serial numbers or if it is a production or kanban pick from a license plate (LP) location and the item is set to staging.</span></span>

## <a name="set-up-piece-picking"></a><span data-ttu-id="a17ee-119">Definer stykkplukking</span><span class="sxs-lookup"><span data-stu-id="a17ee-119">Set up piece picking</span></span>

1.  <span data-ttu-id="a17ee-120">Åpne oppsettskjemaet for arbeidsbekreftelse på et menyelement for mobilenhet: Lagerstyring > **Lagerstyring** > **Oppsett** > **Mobilenhet** > **Menyelementer på mobilenheten**.</span><span class="sxs-lookup"><span data-stu-id="a17ee-120">On a mobile device menu item, open the setup form for work confirmation: Warehouse management > **Warehouse management** > **Setup** > **Mobile device** > **Mobile device menu items**.</span></span> 
2. <span data-ttu-id="a17ee-121">Åpne Arbeidsbekreftelsesoppsett fra menyelement for mobilenhet.</span><span class="sxs-lookup"><span data-stu-id="a17ee-121">From the mobile device menu item, open Work confirmation setup.</span></span>

<span data-ttu-id="a17ee-122">Følgende alternativer blir tilgjengelige når arbeidstypen er plukking og opptelling.</span><span class="sxs-lookup"><span data-stu-id="a17ee-122">The following options become available for selection when the work type is pick or counting.</span></span>


|           <span data-ttu-id="a17ee-123">Alternativ</span><span class="sxs-lookup"><span data-stu-id="a17ee-123">Option</span></span>           |                                                                            <span data-ttu-id="a17ee-124">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="a17ee-124">Description</span></span>                                                                            |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a17ee-125">Stykkplukkingsbekreftelse</span><span class="sxs-lookup"><span data-stu-id="a17ee-125">Piece picking confirmation</span></span> | <span data-ttu-id="a17ee-126">Tilgjengelig for arbeidstypene plukking og opptelling.</span><span class="sxs-lookup"><span data-stu-id="a17ee-126">Available for pick and counting work types.</span></span> <span data-ttu-id="a17ee-127">Produktbekreftelse velges automatisk.</span><span class="sxs-lookup"><span data-stu-id="a17ee-127">Product confirmation is automatically selected.</span></span> <span data-ttu-id="a17ee-128">Lar deg bekrefte hver del av beholdningen fra den mobile enheten.</span><span class="sxs-lookup"><span data-stu-id="a17ee-128">Allows you to confirm each piece of inventory from the mobile device.</span></span> |
|  <span data-ttu-id="a17ee-129">Maksimalt antall enheter</span><span class="sxs-lookup"><span data-stu-id="a17ee-129">Maximum number of pieces</span></span>  |                   <span data-ttu-id="a17ee-130">Tilgjengelig for plukkarbeid hvis stykkplukkingsbekreftelse er aktivert.</span><span class="sxs-lookup"><span data-stu-id="a17ee-130">Available for pick work if piece picking confirmation is enabled.</span></span> <span data-ttu-id="a17ee-131">Angir en grense for hvor mange enheter som du må bekrefte.</span><span class="sxs-lookup"><span data-stu-id="a17ee-131">Sets a limit to the number of pieces that you must confirm.</span></span>                   |

