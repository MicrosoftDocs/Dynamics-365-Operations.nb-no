---
title: Mottak av kombinerte skiltnumre
description: "Dette emnet beskriver hvordan du bruker mottak av kombinerte skiltnumre til å registrere og opprette arbeid for flere varer med en mobilenhet."
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSRFAutoConfirm
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: 48fbbf8f16facd2c364f34c4d6dee765da2b5594
ms.contentlocale: nb-no
ms.lasthandoff: 01/17/2018

---

# <a name="mixed-license-plate-receiving"></a><span data-ttu-id="f1a78-103">Mottak av kombinerte skiltnumre</span><span class="sxs-lookup"><span data-stu-id="f1a78-103">Mixed license plate receiving</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="f1a78-104">Med mottak av kombinerte nummerskilt kan du bygge et nummerskiltsom  består av flere varer før du kan registrere og opprette plasseringsarbeid.</span><span class="sxs-lookup"><span data-stu-id="f1a78-104">Mixed license plate receiving allows you to build a license plate consisting of multiple items before you register and create put-away work.</span></span> 

<span data-ttu-id="f1a78-105">Et nummerskilt som består av flere varer trenger ikke deles i mottakssonenf or at du skal kunne registrere av hver vare.</span><span class="sxs-lookup"><span data-stu-id="f1a78-105">A license plate that consists of multiple items does not have to be split at the receiving dock for you to register each item.</span></span> 

<span data-ttu-id="f1a78-106">Når du bruker en varerelaterte flyt til å identifisere kildedokumentlinjene, kan du skanne strekkoder på varekontrollen.</span><span class="sxs-lookup"><span data-stu-id="f1a78-106">When using an item-related flow to identify the source document lines, you can scan bar codes on the item control.</span></span> <span data-ttu-id="f1a78-107">Varen og antallet vil automatisk bli lagt til i det kombinerte nummerskiltet hvis strekkoden har et konfigurert antall og en enhet (åleenhet), og du kommer tilbake til skjermbildet til å skanne en annen vare.</span><span class="sxs-lookup"><span data-stu-id="f1a78-107">If the bar code has a quantity and a unit of measure (UOM) configured on it, the item and quantity will automatically be added to the mixed license plate, and you will be returned to the screen to scan another item.</span></span> <span data-ttu-id="f1a78-108">Dermed kan du raskt skanne alle varene uten å måtte bekrefte for hvert trinn.</span><span class="sxs-lookup"><span data-stu-id="f1a78-108">This allows you to quickly scan all the items without having to make a confirmation at each step.</span></span> 

<span data-ttu-id="f1a78-109">I flyten for mottak av kombinerte skiltnumre kan du vise listen over varer som allerede er skannet for nummerskiltet, og herfra kan du endre eller korrigere antallet for en vare.</span><span class="sxs-lookup"><span data-stu-id="f1a78-109">In the flow for mixed license plate receiving, you can display the list of items that are already scanned to the license plate and from here you can modify or correct the quantity of an item.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="f1a78-110">Der det er aktuelt</span><span class="sxs-lookup"><span data-stu-id="f1a78-110">Where it applies</span></span>

<span data-ttu-id="f1a78-111">Mottak av kombinerte skiltnumre er en mottaksflyt i en mobilenhet for å registrere og opprette arbeid for flere linjer/varer samtidig.</span><span class="sxs-lookup"><span data-stu-id="f1a78-111">Mixed license plate receiving is a mobile device receiving flow to register and create work for multiple lines/items at the same time.</span></span> <span data-ttu-id="f1a78-112">Dette er nyttig hvis du mottar innkommende nummerskilt med flere varer.</span><span class="sxs-lookup"><span data-stu-id="f1a78-112">This is useful if you receive inbound license plates with multiple items.</span></span> 

## <a name="how-to-set-up-mixed-license-plate-receiving"></a><span data-ttu-id="f1a78-113">Slik definerer du mottak av kombinerte skiltnumre</span><span class="sxs-lookup"><span data-stu-id="f1a78-113">How to set up mixed license plate receiving</span></span>
<span data-ttu-id="f1a78-114">Mottak av kombinerte skiltnumre defineres som et menyelement i en mobilenhet.</span><span class="sxs-lookup"><span data-stu-id="f1a78-114">Mixed license plate receiving is set up as a mobile device menu item.</span></span>

<span data-ttu-id="f1a78-115">Du må opprette et nytt menyelement med modus for arbeid som ikke bruker eksisterende arbeid, og som bruker en av følgende metoder:</span><span class="sxs-lookup"><span data-stu-id="f1a78-115">You need to create a new menu item with mode work that does not use existing work and use one of the following methods:</span></span>

- <span data-ttu-id="f1a78-116">Mottak av kombinerte skiltnumre</span><span class="sxs-lookup"><span data-stu-id="f1a78-116">Mixed license plate receiving</span></span>
- <span data-ttu-id="f1a78-117">Mottak og plassering av kombinerte skiltnumre</span><span class="sxs-lookup"><span data-stu-id="f1a78-117">Mixed license plate receiving and put away</span></span>

<span data-ttu-id="f1a78-118">Alternativene for å identifisere kildedokumentlinjene er bestillingsvare, bestillingslinje, returordre, overføringsordrevare og overføringsordrelinje.</span><span class="sxs-lookup"><span data-stu-id="f1a78-118">The options to identify the source document lines are purchase order item, purchase order line, return order, transfer order item, and transfer order line.</span></span> <span data-ttu-id="f1a78-119">Disse alternativene kan endre mottaksordren på et enkelt nummerskilt.</span><span class="sxs-lookup"><span data-stu-id="f1a78-119">These options can change the receiving order on a single license plate.</span></span> <span data-ttu-id="f1a78-120">Det siste alternativet er etter lastvare.</span><span class="sxs-lookup"><span data-stu-id="f1a78-120">The last option is by load item.</span></span> <span data-ttu-id="f1a78-121">Du kan legge til flere elementer i et nummerskilt, men du kan ikke bytte mellom flere laster.</span><span class="sxs-lookup"><span data-stu-id="f1a78-121">You can add multiple items to a license plate, but you cannot switch between multiple loads.</span></span>

