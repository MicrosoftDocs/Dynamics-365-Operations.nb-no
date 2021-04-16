---
title: Automatisk autorisasjon med planleggingsoptimalisering
description: Dette emnet beskriver hvordan du bruker automatisk autorisasjon med planleggingsoptimalisering.
author: ChristianRytt
ms.date: 11/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-11-30
ms.dyn365.ops.version: AX 10.0.7
ms.openlocfilehash: 3542e343de29c9fd9d19ed99cab4b4eebacd2899
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5813009"
---
# <a name="autofirming-with-planning-optimization"></a><span data-ttu-id="31f24-103">Automatisk autorisasjon med planleggingsoptimalisering</span><span class="sxs-lookup"><span data-stu-id="31f24-103">Autofirming with Planning Optimization</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="31f24-104">Automatisk autorisasjon gjør det mulig å autorisere planlagte bestillinger som en del av hovedplanlegging-prosessen.</span><span class="sxs-lookup"><span data-stu-id="31f24-104">Automatic firming lets you firm (that is, release) planned orders as part of the master planning process.</span></span> <span data-ttu-id="31f24-105">Når planlagte bestillinger autoriseres, blir de omgjort til faktiske bestillinger, overføringsordrer eller produksjonsordrer.</span><span class="sxs-lookup"><span data-stu-id="31f24-105">When planned orders are firmed, they are transformed into actual purchase orders, transfer orders, or production orders.</span></span> <span data-ttu-id="31f24-106">Når planleggingsoptimalisering brukes, blir planlagte bestillinger autorisert under en hovedplanlegging som kjøres når ordredatoen (det vil si startdatoen) er innenfor tidshorisonten for autorisasjon.</span><span class="sxs-lookup"><span data-stu-id="31f24-106">When Planning Optimization is used, planned orders are firmed during a master planning run when the order date (that is, the start date) is within the time fence for firming.</span></span>

> [!NOTE]
> <span data-ttu-id="31f24-107">Automatisk autorisasjon av et bestillingsforslag kan bare skje hvis varen er knyttet til en leverandør.</span><span class="sxs-lookup"><span data-stu-id="31f24-107">Auto-firming of a planned purchase order can occur only if the item is associated with a vendor.</span></span>
> 
> <span data-ttu-id="31f24-108">Autoriserte avledede ordrer (bestillinger fra underleverandør) viser statusen *Til vurdering* når sporing av saksendringer er aktivert.</span><span class="sxs-lookup"><span data-stu-id="31f24-108">Firmed derived orders (subcontract purchase orders) will show a status of *In-review* when case change tracking is enabled.</span></span>

## <a name="turn-on-autofirming"></a><span data-ttu-id="31f24-109">Aktivere automatisk autorisering</span><span class="sxs-lookup"><span data-stu-id="31f24-109">Turn on autofirming</span></span>

<span data-ttu-id="31f24-110">Følg denne fremgangs måten for å aktivere automatisk autorisering.</span><span class="sxs-lookup"><span data-stu-id="31f24-110">To turn on autofirming, follow these steps.</span></span>

1. <span data-ttu-id="31f24-111">I arbeidsområdet **Funksjonsbehandling** i **Ny**-fanen velger du **Automatisk autorisasjon med planleggingsoptimalisering** i listen.</span><span class="sxs-lookup"><span data-stu-id="31f24-111">In the **Feature management** workspace, on the **New** tab, select **Auto-firming for Planning Optimization** in the list.</span></span> <span data-ttu-id="31f24-112">Hvis funksjonen ikke vises i **Ny**-fanen, ser du i fanene **Ikke aktivert** og **Alle**.</span><span class="sxs-lookup"><span data-stu-id="31f24-112">If the feature doesn't appear on the **New** tab, look on the **Not enabled** and **All** tabs.</span></span>
1. <span data-ttu-id="31f24-113">Velg **Aktiver nå**.</span><span class="sxs-lookup"><span data-stu-id="31f24-113">Select **Enable now**.</span></span> <span data-ttu-id="31f24-114">Du kan også velge **Tidsplan**, og deretter velge tidspunktet når du vil at funksjonen skal aktiveres.</span><span class="sxs-lookup"><span data-stu-id="31f24-114">Alternatively, select **Schedule**, and then select the time when you want the feature to be turned on.</span></span>

## <a name="set-up-the-firming-time-fence"></a><span data-ttu-id="31f24-115">Definer autorisasjonshorisonten</span><span class="sxs-lookup"><span data-stu-id="31f24-115">Set up the firming time fence</span></span>

<span data-ttu-id="31f24-116">Autorisasjonshorisonten beregnes fremover fra og med kjøringsdatoen for hovedplanlegging.</span><span class="sxs-lookup"><span data-stu-id="31f24-116">The firming time fence is calculated forward from the master planning run date.</span></span> <span data-ttu-id="31f24-117">Den er definert av antall dager du angir.</span><span class="sxs-lookup"><span data-stu-id="31f24-117">It's defined by the number of days that you enter.</span></span> <span data-ttu-id="31f24-118">Du kan styre autorisasjonshorisonten på følgende måter:</span><span class="sxs-lookup"><span data-stu-id="31f24-118">You can control the firming time fence in the following ways:</span></span>

- <span data-ttu-id="31f24-119">Hvis du vil definere standard autorisasjonshorisonten for en dekningsgruppe, går du til **Hovedplanlegging** \> **Oppsett** \> **Dekning** \> **Dekningsgrupper**, og velger en dekningsgruppe.</span><span class="sxs-lookup"><span data-stu-id="31f24-119">To define the default firming time fence for a coverage group, go to **Master planning** \> **Setup** \> **Coverage** \> **Coverage groups**, and select a coverage group.</span></span> <span data-ttu-id="31f24-120">Deretter angir du antall dager i feltet **Horisont for automatisk autorisasjon (dager)** i hurtigfanen **Annet**.</span><span class="sxs-lookup"><span data-stu-id="31f24-120">Then, on the **Other** FastTab, in the **Automatic firming time fence (days)** field, enter the number of days.</span></span>
- <span data-ttu-id="31f24-121">Hvis du vil overskrive autorisasjonshorisonten som er definert for dekningsgruppen for en bestemt vare, går du til **Behandling av produktinformasjon** \> **Frigitte produkter**, og deretter velger du **Plan** og **Varedekning** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="31f24-121">To overwrite the firming time fence that is defined for the coverage group for a specific item, go to **Product information management** \> **Released products**, then from the Action Pane select **Plan** and then select **Item coverage**.</span></span> <span data-ttu-id="31f24-122">I fanen **Generelt** velger du deretter **Overstyr horisont** og angir antall dager i feltet **Horisont for automatisk autorisasjon (dager)**.</span><span class="sxs-lookup"><span data-stu-id="31f24-122">Then, on the **General** tab, select **Override time fence** and in the **Automatic firming time fence (days)** field, enter the number of days.</span></span>
- <span data-ttu-id="31f24-123">Hvis du vil overskrive autorisasjonshorisonten som er definert for dekningsgruppen og varedekningen for en bestemt hovedplan, går du til **Hovedplanlegging** \> **Oppsett** \> **Hovedplanlegging**, og velger en hovedplan.</span><span class="sxs-lookup"><span data-stu-id="31f24-123">To overwrite the firming time fence that is defined for the coverage group and item coverage for a specific master plan, go to **Master planning** \> **Setup** \> **Master plans**, and select a Master plan.</span></span> <span data-ttu-id="31f24-124">Deretter setter du **Autorisasjon** til **Ja** i hurtigfanen **Horisont i antall dager**, og angir antall dager.</span><span class="sxs-lookup"><span data-stu-id="31f24-124">Then, on the **Time fence in days** FastTab, set **Firming** to **Yes**, and enter the number of days.</span></span>

<span data-ttu-id="31f24-125">Hvis automatisk autorisering er aktivert for en kjøring av hovedplanlegging som bruker planleggingsoptimalisering, utføres automatisk autorisering i henhold til oppsettet for automatisk autorisasjon.</span><span class="sxs-lookup"><span data-stu-id="31f24-125">If autofirming is turned on for a master planning run that uses Planning Optimization, the autofirming process is done according to the autofirming setup.</span></span> <span data-ttu-id="31f24-126">Hvis automatisk autorisering ikke er aktivert, eller hvis planlegging startes fra **Nettobehov** -siden, hoppes den automatiske autorisasjonsprosessen over.</span><span class="sxs-lookup"><span data-stu-id="31f24-126">If autofirming isn't turned on, or if planning is started from the **Net requirements** page, the autofirming process is skipped.</span></span>

## <a name="planning-optimization-vs-the-built-in-supply-chain-management-planning-engine"></a><span data-ttu-id="31f24-127">Planleggingsoptimalisering vs. den innebygde planleggingsmotoren Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="31f24-127">Planning Optimization vs. the built-in Supply Chain Management planning engine</span></span>

<span data-ttu-id="31f24-128">Både planleggingsoptimalisering og planleggingsmotoren som er innebygd i Microsoft Dynamics 365 Supply Chain Management, kan brukes til automatisk autorisering av planlagte bestillinger.</span><span class="sxs-lookup"><span data-stu-id="31f24-128">Both Planning Optimization and the planning engine that is built into Microsoft Dynamics 365 Supply Chain Management can be used to autofirm planned orders.</span></span> <span data-ttu-id="31f24-129">Det er imidlertid noen viktige forskjeller.</span><span class="sxs-lookup"><span data-stu-id="31f24-129">However, there are some important differences.</span></span> <span data-ttu-id="31f24-130">Mens planleggingsoptimalisering for eksempel bruker ordredatoen (det vil si startdatoen) for å bestemme hvilke planlagte bestillinger som skal autoriseres, bruker den innebygde planleggingsmotoren Supply Chain Management behovsdatoen (det vil si sluttdatoen).</span><span class="sxs-lookup"><span data-stu-id="31f24-130">For example, whereas Planning Optimization uses the order date (that is, the start date) to determine which planned orders to firm, the built-in Supply Chain Management planning engine uses the requirement date (that is, the end date).</span></span> <span data-ttu-id="31f24-131">Her er et sammendrag av forskjellene.</span><span class="sxs-lookup"><span data-stu-id="31f24-131">Here is a summary of the differences.</span></span>

<span data-ttu-id="31f24-132">**Planleggingsoptimalisering**</span><span class="sxs-lookup"><span data-stu-id="31f24-132">**Planning Optimization**</span></span>

- <span data-ttu-id="31f24-133">Automatisk autorisasjon er basert på ordredatoen (startdato).</span><span class="sxs-lookup"><span data-stu-id="31f24-133">Autofirming is based on the order date (start date).</span></span>
- <span data-ttu-id="31f24-134">Fordi ordredatoen (Startdato) utløser autorisering, trenger du ikke å ta hensyn til leveringstiden som en del av autorisasjonshorisonten.</span><span class="sxs-lookup"><span data-stu-id="31f24-134">Because the order date (start date) triggers the firming, you don't have to consider the lead time as part of the firming time fence.</span></span>
- <span data-ttu-id="31f24-135">Hvis du vil autorisere alle ordrer som må starte i løpet av den gjeldende uken, må autorisasjonshorisonten være én uke.</span><span class="sxs-lookup"><span data-stu-id="31f24-135">If you want to firm all orders that must start during the current week, the firming time fence must be one week.</span></span>

<span data-ttu-id="31f24-136">**Innebygd planleggingsmotor for Supply Chain Management**</span><span class="sxs-lookup"><span data-stu-id="31f24-136">**Built-in Supply Chain Management planning engine**</span></span>

- <span data-ttu-id="31f24-137">Automatisk autorisasjon er basert på behovsdatoen (sluttdato).</span><span class="sxs-lookup"><span data-stu-id="31f24-137">Autofirming is based on the requirement date (end date).</span></span>
- <span data-ttu-id="31f24-138">Hvis du vil ha hjelp til å sikre at ordrer blir autorisert innen forfallstid, må autorisasjonshorisonten være lenger enn leveringstiden.</span><span class="sxs-lookup"><span data-stu-id="31f24-138">To help guarantee that orders are firmed in due time, the firming time fence must be longer than the lead time.</span></span>
- <span data-ttu-id="31f24-139">Hvis du vil autorisere alle ordrer som må starte i løpet av den gjeldende uken, må autorisasjonshorisonten være leveringstiden pluss én uke.</span><span class="sxs-lookup"><span data-stu-id="31f24-139">If you want to firm all orders that must start during the current week, the firming time fence must be the lead time plus one week.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
