---
title: Lokasjonsprofilen sperrer negativ beholdning, men negativ lagerbeholdning er tillatt
description: Alternativet Tillat negativ beholdning for lokasjonsprofilen er satt til Nei, men systemet tillater likevel negativ lagerbeholdning.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WHSLocationProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: shawan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 356d2dd7853bf93250e14eb9bd28a8a145794584
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026777"
---
# <a name="location-profile-disallows-negative-inventory-but-negative-on-hand-inventory-is-permitted"></a><span data-ttu-id="0502b-103">Lokasjonsprofilen sperrer negativ beholdning, men negativ lagerbeholdning er tillatt</span><span class="sxs-lookup"><span data-stu-id="0502b-103">Location profile disallows negative inventory, but negative on-hand inventory is permitted</span></span>

<span data-ttu-id="0502b-104">KB-nummer: 4613622</span><span class="sxs-lookup"><span data-stu-id="0502b-104">KB number: 4613622</span></span>

## <a name="symptoms"></a><span data-ttu-id="0502b-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="0502b-105">Symptoms</span></span>

<span data-ttu-id="0502b-106">Alternativet **Tillat negativ beholdning** for lokasjonsprofilen er satt til *Nei*, men systemet tillater likevel negativ lagerbeholdning.</span><span class="sxs-lookup"><span data-stu-id="0502b-106">The **Allow negative inventory** option for the location profile is set to *No*, but the system still allows negative on-hand inventory.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="0502b-107">Eksempelscenario</span><span class="sxs-lookup"><span data-stu-id="0502b-107">Example scenario</span></span>

<span data-ttu-id="0502b-108">For transaksjoner som er regulert av offentlige myndigheter, må systemet kunne registrere negativ beholdning for bokført tap.</span><span class="sxs-lookup"><span data-stu-id="0502b-108">For government-regulated transactions, the system must be able to record negative inventory to book losses.</span></span> <span data-ttu-id="0502b-109">Du vil at en vare skal kunne vise negativ beholdning, men bare på angitte lokasjoner, for eksempel tanker.</span><span class="sxs-lookup"><span data-stu-id="0502b-109">You want an item to be able to show negative inventory, but only in designated locations, such as tanks.</span></span> <span data-ttu-id="0502b-110">Hvis imidlertid varemodellgruppen tillater negativ beholdning, finner du ut at det ikke har noen betydning om lokasjonen er angitt til å tillate negativ beholdning.</span><span class="sxs-lookup"><span data-stu-id="0502b-110">However, if the item model group allows negative inventory, you find that it doesn't matter whether the location is set to allow negative inventory.</span></span> <span data-ttu-id="0502b-111">Hvis varen er konfigurert slik at negativ beholdning ikke er tillatt, har det ingen betydning hvordan lokasjonsprofilen er satt opp.</span><span class="sxs-lookup"><span data-stu-id="0502b-111">If the item is set up so that negative inventory isn't allowed, it doesn't matter how the location profile is set up.</span></span>

## <a name="resolution"></a><span data-ttu-id="0502b-112">Oppløsning</span><span class="sxs-lookup"><span data-stu-id="0502b-112">Resolution</span></span>

<span data-ttu-id="0502b-113">Innstillingen **Tillat negativt lager** fra lokasjonsprofilen gjelder bare for lagerprosesser, for eksempel plukking.</span><span class="sxs-lookup"><span data-stu-id="0502b-113">The **Allow negative inventory** setting from the location profile applies only to warehouse processes, such as picking.</span></span> <span data-ttu-id="0502b-114">Men varemodellgrupper som er angitt for å tillate negativ beholdning, påvirker alle prosesser fra lagerstyrings- og lagerstyringsmodulene, og lokasjonsprofilen vil ikke overstyre innstillingen.</span><span class="sxs-lookup"><span data-stu-id="0502b-114">However, item model groups that are set to allow negative inventory affect all processes from the Inventory management and Warehouse management modules, and the location profile won't override the setting.</span></span>

<span data-ttu-id="0502b-115">Du kan styre om et lager kan tillate negativt beholdning.</span><span class="sxs-lookup"><span data-stu-id="0502b-115">You can control whether a warehouse is allowed to carry negative inventory.</span></span> <span data-ttu-id="0502b-116">Angi at varemodellgruppene skal sperre negativ fysisk beholdning, og angi bare relevant lager, slik at negativ beholdning tillates.</span><span class="sxs-lookup"><span data-stu-id="0502b-116">Set your item model groups to disallow negative physical inventory, and set only the relevant warehouse to allow negative inventory.</span></span>
