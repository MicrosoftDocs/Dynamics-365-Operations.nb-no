---
title: Tilordne dimensjonsmedlemmer for kostnadselement til et felles sett med dimensjonsmedlemmer
description: Ved tilordning av forskjellige medlemmer av kostnadselementdimensjon til et felles sett med medlemmer av kostnadselementdimensjoner, slår du sammen data i et felles format for analyseformål.
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension, CAMDimensionMember, CAMDimensionMapping
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 223234
ms.assetid: 4c66a231-aed2-48b5-9727-b3eb4fe6e6aa
ms.search.region: global
ms.author: roschlom
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: c6a9618a762d3af840beb05d86518b3588118e80
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/10/2020
ms.locfileid: "3976361"
---
# <a name="map-cost-element-dimension-members-to-a-common-set-of-dimension-members"></a><span data-ttu-id="e1c7f-103">Tilordne dimensjonsmedlemmer for kostnadselement til et felles sett med dimensjonsmedlemmer</span><span class="sxs-lookup"><span data-stu-id="e1c7f-103">Map cost element dimension members to a common set of dimension members</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e1c7f-104">Ved tilordning av forskjellige medlemmer av kostnadselementdimensjon til et felles sett med medlemmer av kostnadselementdimensjoner, slår du sammen data i et felles format for analyseformål.</span><span class="sxs-lookup"><span data-stu-id="e1c7f-104">By mapping different cost element dimension members to a common set of cost element dimension members, you merge data into a common format for analysis purposes.</span></span>

<span data-ttu-id="e1c7f-105">Hvis du er et globalt selskap og overholder lovbestemte regnskapsmessige krav, kan du bruke flere kontoplaner.</span><span class="sxs-lookup"><span data-stu-id="e1c7f-105">If you're a global company and comply with statutory accounting requirements, you might use multiple charts of accounts.</span></span> <span data-ttu-id="e1c7f-106">Når du importerer medlemmer av kostnadelementdimensjoner fra ulike kontoplaner, kan du ende opp med en blanding av kontoer.</span><span class="sxs-lookup"><span data-stu-id="e1c7f-106">When you import cost element dimension members from different charts of accounts, you can end up with a mix of accounts.</span></span> <span data-ttu-id="e1c7f-107">Disse kontoene har imidlertid faktisk samme egenskap, og du vil kanskje analysere og fordele kostnader for dem ved hjelp av et felles format.</span><span class="sxs-lookup"><span data-stu-id="e1c7f-107">However, these accounts might actually have the same nature, and you might want to analyze and allocate costs for them by using a common format.</span></span>

## <a name="map-cost-element-dimension-members-to-a-common-format"></a><span data-ttu-id="e1c7f-108">Tilordne medlemmer av kostnadelementdimensjoner til et vanlig format</span><span class="sxs-lookup"><span data-stu-id="e1c7f-108">Map cost element dimension members to a common format</span></span>
<span data-ttu-id="e1c7f-109">Eksemplet nedenfor viser hvordan du, som kostnadskontrollør, kan opprette en ny kostnadselementdimensjon i kostnadsregnskap som tilordner medlemmer av kostnadelementdimensjoner fra den amerikanske og franske kontoplanstrukturen til et felles sett med medlemmer av kostnadelementdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="e1c7f-109">The following example shows how you, as a cost controller, can create a new cost element dimension in Cost accounting that maps cost element dimension members from the US chart of accounts structure and the French chart of accounts structure to a common set of cost element dimension members.</span></span> <span data-ttu-id="e1c7f-110">Du kan deretter bruke det felles settet med medlemmer av kostnadelementdimensjoner til å analysere kostnadsdata fra de to juridiske enhetene i en finanskonto for kostnadsregnskap.</span><span class="sxs-lookup"><span data-stu-id="e1c7f-110">You can then use the common set of cost element dimension members to analyze cost data from the two legal entities in a cost accounting ledger.</span></span>

| <span data-ttu-id="e1c7f-111">Kilde: amerikansk kontoplanstruktur</span><span class="sxs-lookup"><span data-stu-id="e1c7f-111">Source: US chart of accounts</span></span>                                          | <span data-ttu-id="e1c7f-112">Kilde: fransk kontoplanstruktur</span><span class="sxs-lookup"><span data-stu-id="e1c7f-112">Source: French chart of accounts</span></span>                                          | <span data-ttu-id="e1c7f-113">Nytt felles sett med medlemmer av kostnadelementdimensjoner</span><span class="sxs-lookup"><span data-stu-id="e1c7f-113">New common set of cost element dimension members</span></span>                        |
|-----------------------------------------------------------------------|---------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="e1c7f-114">Importerte medlemmer av kostnadelementdimensjoner fra den amerikanske kontoplanen</span><span class="sxs-lookup"><span data-stu-id="e1c7f-114">Imported cost element dimension members from the US chart of accounts</span></span> | <span data-ttu-id="e1c7f-115">Importerte medlemmer av kostnadelementdimensjoner fra den franske kontoplanen</span><span class="sxs-lookup"><span data-stu-id="e1c7f-115">Imported cost element dimension members from the French chart of accounts</span></span> | <span data-ttu-id="e1c7f-116">Tilordning av amerikanske og fransk medlemmer av kostnadselementdimensjoner til et felles sett</span><span class="sxs-lookup"><span data-stu-id="e1c7f-116">Mapping of US and French cost element dimension members to a common set</span></span> |
| <span data-ttu-id="e1c7f-117">5001: Salg</span><span class="sxs-lookup"><span data-stu-id="e1c7f-117">5001: Sales</span></span>                                                           | <span data-ttu-id="e1c7f-118">5001: Salg og markedsføring</span><span class="sxs-lookup"><span data-stu-id="e1c7f-118">5001: Sales and advertising</span></span>                                               | <span data-ttu-id="e1c7f-119">5000: Salg og markedsføring</span><span class="sxs-lookup"><span data-stu-id="e1c7f-119">5000: Sales and advertising</span></span>                                             |
| <span data-ttu-id="e1c7f-120">5030: Reklame</span><span class="sxs-lookup"><span data-stu-id="e1c7f-120">5030: Advertising</span></span>                                                     | <span data-ttu-id="e1c7f-121">6390: Lagerinnkjøp\*</span><span class="sxs-lookup"><span data-stu-id="e1c7f-121">6390: Stock purchase\*</span></span>                                                    | <span data-ttu-id="e1c7f-122">7000: Renholdsutgifter</span><span class="sxs-lookup"><span data-stu-id="e1c7f-122">7000: Cleaning expenses</span></span>                                                 |
| <span data-ttu-id="e1c7f-123">7001: Renholdsutgifter</span><span class="sxs-lookup"><span data-stu-id="e1c7f-123">7001: Cleaning expenses</span></span>                                               | <span data-ttu-id="e1c7f-124">7001: Reiseutgifter</span><span class="sxs-lookup"><span data-stu-id="e1c7f-124">7001: Travel expense</span></span>                                                      | <span data-ttu-id="e1c7f-125">7001: Reiseutgifter</span><span class="sxs-lookup"><span data-stu-id="e1c7f-125">7001: Travel expenses</span></span>                                                   |

<span data-ttu-id="e1c7f-126">\*Lagerinnkjøp for franske medlem av kostnadselementdimensjon er ikke tilordnet.</span><span class="sxs-lookup"><span data-stu-id="e1c7f-126">\*The Stock purchase French cost element dimension member isn't mapped.</span></span>

## <a name="currency-conversion"></a><span data-ttu-id="e1c7f-127">Valutaomregning</span><span class="sxs-lookup"><span data-stu-id="e1c7f-127">Currency conversion</span></span>
<span data-ttu-id="e1c7f-128">De ulike kontoplanene som du bruker, kan være konfigurert til å bruke ulike valutaer.</span><span class="sxs-lookup"><span data-stu-id="e1c7f-128">The various charts of accounts that you use might be set up to use different currencies.</span></span> <span data-ttu-id="e1c7f-129">I så fall må du huske å angi en valutaomregning, slik at kostnadsdata behandles ved hjelp av riktig valuta, som definert i kostnadsregnskapsfinans der medlemmene av kostnadselementdimensjonen er brukt.</span><span class="sxs-lookup"><span data-stu-id="e1c7f-129">In this case, be sure to specify a currency conversion, so that cost data is processed by using the correct currency, as defined in the cost accounting ledger where the cost element dimension members are used.</span></span> <span data-ttu-id="e1c7f-130">Hvis Amerikanske dollar (USD) brukes i kostnadsregnskapsfinans i eksemplet ovenfor, må du opprette en valutaomregning fra USD til euro (EUR) for å behandle transaksjoner for de tilordnede medlemmene av kostnadselementdimensjonen.</span><span class="sxs-lookup"><span data-stu-id="e1c7f-130">In the preceding example, if US dollars (USD) are used in the cost accounting ledger, you must create a currency conversion from USD to euros (EUR) to process transactions for the mapped cost element dimension members.</span></span>

## <a name="update-mappings-at-any-time"></a><span data-ttu-id="e1c7f-131">Oppdater tilordninger når som helst</span><span class="sxs-lookup"><span data-stu-id="e1c7f-131">Update mappings at any time</span></span>
<span data-ttu-id="e1c7f-132">Du kan oppdatere tilordningsdefinisjonene for en kostnadselementdimensjon når som helst.</span><span class="sxs-lookup"><span data-stu-id="e1c7f-132">You can update the mapping definitions for a cost element dimension at any time.</span></span> <span data-ttu-id="e1c7f-133">Siden tilordningene ikke er datoeffektive, brukes endringene neste gang du behandler kostnadstransaksjoner eller kjøre kostnadsberegninger.</span><span class="sxs-lookup"><span data-stu-id="e1c7f-133">Because mappings aren't date-effective, changes are applied the next time that you process cost transactions or run cost calculations.</span></span>



