---
title: Manuell oppdatering av anleggsmiddeltellere
description: Dette emnet beskriver manuell oppdatering av aktivatellere i Aktivastyring.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1e7c5ec288404c18b00f9dcd0e66f50744d0aa2f
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875821"
---
# <a name="manual-update-of-asset-counters"></a><span data-ttu-id="4e0d4-103">Manuell oppdatering av anleggsmiddeltellere</span><span class="sxs-lookup"><span data-stu-id="4e0d4-103">Manual update of asset counters</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="4e0d4-104">Tellere brukes til å opprette registreringer for et anleggsmiddel angående for eksempel antall timer i drift eller produsert antall.</span><span class="sxs-lookup"><span data-stu-id="4e0d4-104">Counters are used to create registrations on an asset regarding, for example, number of hours in operation, or the number of quantities produced.</span></span>

<span data-ttu-id="4e0d4-105">Hvis tellertypen som er valgt for en teller, er satt til Arv tellerverdier (**Aktivastyring** > **Oppsett** > **Aktivatyper** > **Tellere** > **Generelt**-hurtigfanen > **Arv aktivatellerverdier**-veksleknappen satt til Ja), da, når du oppretter en ny tellerlinje av denne typen, oppdateres automatisk alle underordnede anleggsmidler som bruker samme tellertype.</span><span class="sxs-lookup"><span data-stu-id="4e0d4-105">If the counter type selected for a counter is set to inherit counter values (**Asset management** > **Setup** > **Asset types** > **Counters** > **General** FastTab > **Inherit asset counter values** toggle button set to "Yes"), then, when you create a new counter line of that type, every child asset that uses the same counter type is automatically updated.</span></span>

<span data-ttu-id="4e0d4-106">I **Alle aktiva** oppretter du tellerregistreringer for timer eller antall for et aktivum basert på avlesningene for aktivaet.</span><span class="sxs-lookup"><span data-stu-id="4e0d4-106">In **All assets**, you create hours or quantity counter registrations on an asset, based on your readings on the asset.</span></span>

1. <span data-ttu-id="4e0d4-107">Klikk på **Aktivastyring** > **Felles** > **Aktiva** > **Alle aktiva**.</span><span class="sxs-lookup"><span data-stu-id="4e0d4-107">Click **Asset management** > **Common** > **Assets** > **All assets**.</span></span>

2. <span data-ttu-id="4e0d4-108">Velg aktivaet i listen, og klikk på **Tellere**.</span><span class="sxs-lookup"><span data-stu-id="4e0d4-108">Select the asset in the list, and click **Counters**.</span></span> <span data-ttu-id="4e0d4-109">I skjemaet **Aktivatellere** ser du en liste over alle tidligere tellerregistreringer for det valgte anleggsmidlet.</span><span class="sxs-lookup"><span data-stu-id="4e0d4-109">In the **Asset counters** form, you see a list of all previous counter registrations on the selected asset.</span></span>

3. <span data-ttu-id="4e0d4-110">Klikk på **Ny** for å opprette en ny registrering.</span><span class="sxs-lookup"><span data-stu-id="4e0d4-110">Click **New** to create a new registration.</span></span> <span data-ttu-id="4e0d4-111">Anleggsmiddel-ID-en settes inn automatisk.</span><span class="sxs-lookup"><span data-stu-id="4e0d4-111">The asset ID is automatically inserted.</span></span>

4. <span data-ttu-id="4e0d4-112">Velg den aktuelle telleren i **Teller**-feltet.</span><span class="sxs-lookup"><span data-stu-id="4e0d4-112">In the **Counter** field, select the relevant counter.</span></span> <span data-ttu-id="4e0d4-113">Bare tellere for anleggsmiddeltypen som er valgt i anleggsmiddelet, er tilgjengelige.</span><span class="sxs-lookup"><span data-stu-id="4e0d4-113">Only counters related to the asset type selected on the asset are available.</span></span> <span data-ttu-id="4e0d4-114">Den aktuelle enheten settes inn automatisk i **Enhet**-feltet.</span><span class="sxs-lookup"><span data-stu-id="4e0d4-114">The related unit is automatically inserted in the **Unit** field.</span></span>

5. <span data-ttu-id="4e0d4-115">Velg dato og klokkeslett for tellerregistreringen.</span><span class="sxs-lookup"><span data-stu-id="4e0d4-115">Select date and time for the counter registration.</span></span>

6. <span data-ttu-id="4e0d4-116">I **Verdi**-feltet setter du inn antallet siden den siste tellerregistreringen, eller setter inn totalt antall i **Aggregert verdi**-feltet.</span><span class="sxs-lookup"><span data-stu-id="4e0d4-116">In the **Value** field, insert the number since the last counter registration, or, in the **Aggregated value** field, insert the total count number.</span></span>

- <span data-ttu-id="4e0d4-117">Hvis du fysisk installerer en ny teller på et anleggsmiddel, må du registrere endringen i anleggsmiddelet i **Aktivatellere**.</span><span class="sxs-lookup"><span data-stu-id="4e0d4-117">If you physically install a new counter on an asset, you need to register the change on the asset in **Asset counters**.</span></span> <span data-ttu-id="4e0d4-118">Deretter må du opprette to registreringslinjer med identiske tidsstempler, og på linjen som gjelder den nye telleren, merker du av for **Tilbakestill teller**.</span><span class="sxs-lookup"><span data-stu-id="4e0d4-118">Next, you must create two registration lines with identical timestamps, and on the line regarding the new counter, you select the **Counter reset** check box.</span></span> <span data-ttu-id="4e0d4-119">Når du oppretter de to registreringslinjene, må den første linjen være for telleren du erstatter.</span><span class="sxs-lookup"><span data-stu-id="4e0d4-119">When you create the two registration lines, the first line must be for the counter that you are replacing.</span></span> <span data-ttu-id="4e0d4-120">I **Total**-feltet er totalt antall summen av tellertotalen for alle registrerte verdier på denne tellertypen.</span><span class="sxs-lookup"><span data-stu-id="4e0d4-120">In the **Totals** field, the total count number is the sum of the counter total of all registered values on that counter type.</span></span>  
- <span data-ttu-id="4e0d4-121">Hvis det er merket av for **Tilbakestill teller** for et anleggsmiddel ved hjelp av en vedlikeholdsplan med intervalltypen Én gang fra... eller Når nådd..., er telleren fremdeles aktiv på den nye tellerlinjen fordi du oppretter en egen tellerlinje og begynner på nytt med en ny teller.</span><span class="sxs-lookup"><span data-stu-id="4e0d4-121">If the **Counter reset** check box is selected on an asset using a maintenance plan with a "Once from..." or "Once reached..." interval type, the counter is still active on the new counter line because you create a separate counter line and start over with a new counter.</span></span>

![Figur 1](media/11-work-orders.png)


<span data-ttu-id="4e0d4-123">Hvis du vil foreta tellerregistreringer på flere aktiva, kan du gjøre dette i **Aktivastyring** > **Forespørsler** > **Aktiva** > **Aktivatellere**.</span><span class="sxs-lookup"><span data-stu-id="4e0d4-123">If you need to make counter registrations on several assets, that can be done in **Asset management** > **Inquiries** > **Assets** > **Asset counters**.</span></span>

>[!NOTE]
><span data-ttu-id="4e0d4-124">Du kan angi et område for å definere avvik i manuelle tellerregistreringer, og typen melding som skal vises hvis registreringer er utenfor det definerte området.</span><span class="sxs-lookup"><span data-stu-id="4e0d4-124">You can set up a range to define deviations in manual counter registrations, and the type of message that should be displayed if registrations are outside the defined range.</span></span> <span data-ttu-id="4e0d4-125">Se emnet [Tellere](../setup-for-objects/counters.md) om oppsett av tellere.</span><span class="sxs-lookup"><span data-stu-id="4e0d4-125">Refer to the [Counters](../setup-for-objects/counters.md) topic regarding setup of counters.</span></span>
