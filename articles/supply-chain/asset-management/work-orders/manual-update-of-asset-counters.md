---
title: Manuell oppdatering av anleggsmiddeltellere
description: Dette emnet beskriver manuell oppdatering av aktivatellere i Aktivastyring.
author: johanhoffmann
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetCounter
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 4618ff2d6880f478683fbed0ed716af5ab8d4d9c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5842255"
---
# <a name="manual-update-of-asset-counters"></a><span data-ttu-id="358f3-103">Manuell oppdatering av anleggsmiddeltellere</span><span class="sxs-lookup"><span data-stu-id="358f3-103">Manual update of asset counters</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="358f3-104">Tellere brukes til å opprette registreringer for aktiva, for eksempel registreringer om antall timer som aktivumet har vært i operasjon, eller antallet som er produsert.</span><span class="sxs-lookup"><span data-stu-id="358f3-104">Counters are used to create registrations on an asset, such as registrations about the number of hours that the asset has been in operation or the quantity that has been produced.</span></span>

<span data-ttu-id="358f3-105">Tellertypen som er valgt for en teller, kan være satt til å arve tellerverdier.</span><span class="sxs-lookup"><span data-stu-id="358f3-105">The counter type that is selected for a counter might be set to inherit counter values.</span></span> <span data-ttu-id="358f3-106">Med andre ord er alternativet **Arv aktivatellerverdier** satt til **Ja** i hurtigfanen **Generelt** på siden **Tellere** (**Aktivabehandling** > **Oppsett** > **Aktivatyper** > **Tellere**).</span><span class="sxs-lookup"><span data-stu-id="358f3-106">In other words, the **Inherit asset counter values** option is set to **Yes** on the **General** FastTab of the **Counters** page (**Asset management** > **Setup** > **Asset types** > **Counters**).</span></span> <span data-ttu-id="358f3-107">I dette tilfellet oppdateres alle underordnede aktiva som bruker den samme tellertypen, automatisk når du oppretter en ny tellerlinje av denne typen.</span><span class="sxs-lookup"><span data-stu-id="358f3-107">In this case, when you create a new counter line of that type, every child asset that uses the same counter type is automatically updated.</span></span>

<span data-ttu-id="358f3-108">På siden **Alle aktiva** oppretter du tellerregistreringer for timer eller antall for et aktivum basert på avlesningene for aktivumet.</span><span class="sxs-lookup"><span data-stu-id="358f3-108">On the **All assets** page, you create hours or quantity counter registrations on an asset, based on your readings on the asset.</span></span>

1. <span data-ttu-id="358f3-109">Velg **Aktivastyring** > **Felles** > **Aktiva** > **Alle aktiva**.</span><span class="sxs-lookup"><span data-stu-id="358f3-109">Select **Asset management** > **Common** > **Assets** > **All assets**.</span></span>

2. <span data-ttu-id="358f3-110">Velg aktivumet, og deretter velger du **Tellere**, i handlingsruten, fanen **Aktiva** i gruppen **Forebyggende**.</span><span class="sxs-lookup"><span data-stu-id="358f3-110">Select the asset, and then, on the Action Pane, on the **Asset** tab, in the **Preventive** group, select **Counters**.</span></span> <span data-ttu-id="358f3-111">Siden **Aktivatellere** viser en liste over alle tidligere tellerregistreringer som er gjort for det valgte aktivumet.</span><span class="sxs-lookup"><span data-stu-id="358f3-111">The **Asset counters** page shows a list of all previous counter registrations that have been made on the selected asset.</span></span>

3. <span data-ttu-id="358f3-112">Velg **Ny** for å opprette en registrering.</span><span class="sxs-lookup"><span data-stu-id="358f3-112">Select **New** to create a registration.</span></span> <span data-ttu-id="358f3-113">Aktiva-ID angis automatisk i **Aktiva**-feltet.</span><span class="sxs-lookup"><span data-stu-id="358f3-113">The asset ID is automatically entered in the **Asset** field.</span></span>

4. <span data-ttu-id="358f3-114">Velg den aktuelle telleren i **Teller**-feltet.</span><span class="sxs-lookup"><span data-stu-id="358f3-114">In the **Counter** field, select the relevant counter.</span></span> <span data-ttu-id="358f3-115">Bare tellere som er relatert til aktivatypen som er valgt i aktivumet, er tilgjengelige for valg.</span><span class="sxs-lookup"><span data-stu-id="358f3-115">Only counters that are related to the asset type selected on the asset are available for selection.</span></span> <span data-ttu-id="358f3-116">Den aktuelle enheten settes inn automatisk i **Enhet**-feltet.</span><span class="sxs-lookup"><span data-stu-id="358f3-116">The related unit is automatically entered in the **Unit** field.</span></span>

5. <span data-ttu-id="358f3-117">I feltet **Registrert** velger du dato og klokkeslett for tellerregistreringen.</span><span class="sxs-lookup"><span data-stu-id="358f3-117">In the **Registered** field, select the date and time for the counter registration.</span></span>

6. <span data-ttu-id="358f3-118">I feltet **Verdi** angir du tallet siden den forrige tellerregistreringen.</span><span class="sxs-lookup"><span data-stu-id="358f3-118">In the **Value** field, enter the number since the last counter registration.</span></span> <span data-ttu-id="358f3-119">Du kan også angi samlet tellerantall i feltet **Aggregert verdi**.</span><span class="sxs-lookup"><span data-stu-id="358f3-119">Alternatively, in the **Aggregated value** field, enter the total count number.</span></span>

<span data-ttu-id="358f3-120">Merk følgende punkt:</span><span class="sxs-lookup"><span data-stu-id="358f3-120">Note the following points:</span></span>

- <span data-ttu-id="358f3-121">Hvis du fysisk installerer en ny teller på et aktivum, må du registrere endringen i aktivumet på siden **Aktivatellere**.</span><span class="sxs-lookup"><span data-stu-id="358f3-121">If you physically install a new counter on an asset, you must register the change on the asset on the **Asset counters** page.</span></span> <span data-ttu-id="358f3-122">Deretter må du opprette to registreringslinjer som har identiske tidsstempler.</span><span class="sxs-lookup"><span data-stu-id="358f3-122">Next, you must create two registration lines that have identical timestamps.</span></span> <span data-ttu-id="358f3-123">Den første linjen må være for telleren du erstatter.</span><span class="sxs-lookup"><span data-stu-id="358f3-123">The first line must be for the counter that you're replacing.</span></span> <span data-ttu-id="358f3-124">I linjen som er knyttet til den nye telleren, merker du av for **Tilbakestill teller**.</span><span class="sxs-lookup"><span data-stu-id="358f3-124">On the line that is related to the new counter, select the **Counter reset** check box.</span></span> <span data-ttu-id="358f3-125">I **Total**-feltet er totalt antall summen av tellertotalene for alle registrerte verdier på denne tellertypen.</span><span class="sxs-lookup"><span data-stu-id="358f3-125">In the **Totals** field, the total count number is the sum of the counter totals of all registered values on that counter type.</span></span>

- <span data-ttu-id="358f3-126">Hvis det er merket av for **Tilbakestill teller** for et aktivum ved hjelp av en vedlikeholdsplan med intervalltypen Én gang fra... eller Når nådd..., er telleren fremdeles aktiv på den nye tellerlinjen fordi du oppretter en egen tellerlinje og begynner på nytt med en ny teller.</span><span class="sxs-lookup"><span data-stu-id="358f3-126">If the **Counter reset** check box is selected on an asset using a maintenance plan that has a "Once from..." or "Once reached..." interval type, the counter is still active on the new counter line, because you create a separate counter line and start over with a new counter.</span></span>

<span data-ttu-id="358f3-127">Illustrasjonen nedenfor viser et eksempel på siden **Aktivatellere**.</span><span class="sxs-lookup"><span data-stu-id="358f3-127">The illustration below shows an example of the **Asset counters** page.</span></span>

![Figur 1](media/11-work-orders.png)

<span data-ttu-id="358f3-129">På siden **Aktivatellere** (**Aktivabehandling** > **Forespørsler** > **Aktiva** > **Aktivatellere**) kan du utføre tellerregistreringer for flere aktivumer samtidig etter behov.</span><span class="sxs-lookup"><span data-stu-id="358f3-129">On the **Asset counters** page (**Asset management** > **Inquiries** > **Assets** > **Asset counters**), you can make counter registrations on several assets at the same time, as you require.</span></span>

>[!NOTE]
><span data-ttu-id="358f3-130">Du kan definere et område for å definere avvik i manuelle tellerregistreringer.</span><span class="sxs-lookup"><span data-stu-id="358f3-130">You can set up a range to define deviations in manual counter registrations.</span></span> <span data-ttu-id="358f3-131">Du kan også angi hvilken type melding som skal vises hvis registreringer er utenfor det definerte området.</span><span class="sxs-lookup"><span data-stu-id="358f3-131">You can also specify the type of message that is shown if registrations are outside the defined range.</span></span> <span data-ttu-id="358f3-132">Hvis du vil ha informasjon om hvordan du definerer tellere, se [Tellere](../setup-for-objects/counters.md).</span><span class="sxs-lookup"><span data-stu-id="358f3-132">For more information about how to set up counters, see [Counters](../setup-for-objects/counters.md).</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]