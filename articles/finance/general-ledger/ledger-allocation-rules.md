---
title: Finansfordelingsregler
description: Denne artikkelen gir generell informasjon om finanstildelingsregler. Den beskriver de ulike komponentene i disse tildelingsreglene og tildelingsmetodene som kan brukes for dem.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerAllocation, LedgerAllocationBasisRule, LedgerAllocationRequest, LedgerAllocationRule
audience: Application User
ms.reviewer: roschlom
ms.custom: 15402
ms.assetid: 8147e148-7c11-45ef-95c6-f9889a875b54
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 31e01046d22c3b7a598386d5621d020339f44cb4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5249005"
---
# <a name="ledger-allocation-rules"></a><span data-ttu-id="88464-104">Finansfordelingsregler</span><span class="sxs-lookup"><span data-stu-id="88464-104">Ledger allocation rules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="88464-105">Denne artikkelen gir generell informasjon om finanstildelingsregler.</span><span class="sxs-lookup"><span data-stu-id="88464-105">This article provides information about ledger allocation rules.</span></span> <span data-ttu-id="88464-106">Den beskriver de ulike komponentene i disse tildelingsreglene og tildelingsmetodene som kan brukes for dem.</span><span class="sxs-lookup"><span data-stu-id="88464-106">It describes the various components of these allocation rules and the allocation methods that can be used for them.</span></span>

<span data-ttu-id="88464-107">Finansfordelingsregler brukes til automatisk å beregne og generere tildelingsjournaler og poster for fordeling av finanssaldoer eller faste beløp.</span><span class="sxs-lookup"><span data-stu-id="88464-107">Ledger allocation rules are used to automatically calculate and generate allocation journals and account entries for the allocation of ledger balances or fixed amounts.</span></span> <span data-ttu-id="88464-108">Tildelingsmetoder kan være variable eller faste.</span><span class="sxs-lookup"><span data-stu-id="88464-108">Allocation methods can be variable or fixed.</span></span> <span data-ttu-id="88464-109">Følgende tildelingsmetoder kan brukes for fordelingsregler for finans:</span><span class="sxs-lookup"><span data-stu-id="88464-109">The following allocation methods can be used for ledger allocation rules:</span></span>

-   <span data-ttu-id="88464-110">**Basis** – denne variable metoden brukes når tildelingen er avhengig av den faktiske finanssaldoen, basert på filterkriteriene.</span><span class="sxs-lookup"><span data-stu-id="88464-110">**Basis** – This variable method is used when the allocation depends on the actual ledger balance, based on filter criteria.</span></span> <span data-ttu-id="88464-111">Du kan for eksempel tildele reklameutgifter basert på salget til hver avdeling i forhold til hele avdelingssalget.</span><span class="sxs-lookup"><span data-stu-id="88464-111">For example, advertising expenses can be allocated based on each department's sales in proportion to the total departmental sales.</span></span>
-   <span data-ttu-id="88464-112">**Fast prosent** og **Fast vekt** – For disse metodene defineres tildelingsprosent eller vekt direkte for regelen.</span><span class="sxs-lookup"><span data-stu-id="88464-112">**Fixed percentage** and **Fixed weight** – For these methods, the allocation percentage or weight is defined directly for the rule.</span></span> <span data-ttu-id="88464-113">Reklameutgifter kan for eksempel tildeles slik at avdeling A får 70 prosent av reklameutgiftene, og avdeling B får 30 prosent.</span><span class="sxs-lookup"><span data-stu-id="88464-113">For example, advertising expenses can be allocated so that Department A receives 70 percent of the advertising expense and Department B receives 30 percent.</span></span>
-   <span data-ttu-id="88464-114">**Likt** – denne metoden fordeler beløpet likt til alle definerte mål.</span><span class="sxs-lookup"><span data-stu-id="88464-114">**Equally** – This method distributes the amount equally to each defined destination.</span></span> <span data-ttu-id="88464-115">Hvis mål for eksempel er definert for avdeling A og B avdeling, kan reklameutgifter tildeles slik at både avdeling A og avdeling B får 50 prosent av reklameutgiftene.</span><span class="sxs-lookup"><span data-stu-id="88464-115">For example, if destinations are defined for Department A and Department B, advertising expenses can be allocated so that both Department A and Department B receive 50 percent of the advertising expense.</span></span>

<span data-ttu-id="88464-116">Hvis Basis brukes som tildelingsmetoden for en tildelingsregel , må du også definer en separate basisregler for finanstildeling.</span><span class="sxs-lookup"><span data-stu-id="88464-116">If Basis is used as the allocation method for an allocation rule, you must also define separate ledger allocation basis rules.</span></span> <span data-ttu-id="88464-117">Ved hjelp av prosessen "Behandle tildelingsforespørsel" kan brukerne behandle finansfordelingsregelen og forhåndsvise de resulterende tildelingspostene for journalen før de posterer eller sletter de beregnede tildelingene.</span><span class="sxs-lookup"><span data-stu-id="88464-117">The "Process allocation request" process lets users process the ledger allocation rule and preview the resulting allocation journal entries before they either post or delete the calculated allocations.</span></span>

## <a name="components-of-ledger-allocation-rules"></a><span data-ttu-id="88464-118">Komponenter for finansfordelingsregler</span><span class="sxs-lookup"><span data-stu-id="88464-118">Components of ledger allocation rules</span></span>
<span data-ttu-id="88464-119">Hver fordelingsregel har fire komponenter: generelt, kilde, mål og forskyvning.</span><span class="sxs-lookup"><span data-stu-id="88464-119">Each allocation rule has four components: general, source, destination, and offset.</span></span> <span data-ttu-id="88464-120">En tilleggskomponent, regler for finansfordelingsbasis, er nødvendig hvis Basis brukes som fordelingsmetode.</span><span class="sxs-lookup"><span data-stu-id="88464-120">An additional component, ledger allocation bases rules, is required if Basis is used as the allocation method.</span></span> <span data-ttu-id="88464-121">Hver komponent gir en viktig del av informasjonen som kreves for å behandle fordelinger.</span><span class="sxs-lookup"><span data-stu-id="88464-121">Each component provides a critical piece of the information that is required in order to process allocations.</span></span>

-   <span data-ttu-id="88464-122">**Generelt** – Denne komponenten er der brukeren angir alternativ som omfatter, men ikke er begrenset til, tildelingsmetode og konsernintern regelinnstillinger samt angir om regelen er aktiv eller ikke.</span><span class="sxs-lookup"><span data-stu-id="88464-122">**General** – This component is where the user specifies options such as the allocation method, intercompany rule settings, and whether the rule is active.</span></span>
-   <span data-ttu-id="88464-123">**Kilde** – Denne komponenten er der brukeren angir kildedata for tildelingen.</span><span class="sxs-lookup"><span data-stu-id="88464-123">**Source** – This component is where the user specifies the source data for the allocation.</span></span> <span data-ttu-id="88464-124">Tildelingen kan være basert på finanssaldoer (**Datakilde** = **Finans**) eller faste beløp (**Datakilde** = **Fast verdi**).</span><span class="sxs-lookup"><span data-stu-id="88464-124">Allocation can be based on ledger balances (**Data source** = **Ledger**) or fixed amounts (**Data source** = **Fixed value**).</span></span> <span data-ttu-id="88464-125">Når **Datakilde** er satt til **Finans**, må kildefilterkriterier defineres for finansfordelingsregelen (for eksempel for reklameutgiftene).</span><span class="sxs-lookup"><span data-stu-id="88464-125">When **Data source** is set to **Ledger**, source filter criteria must be defined for the ledger allocation rule (for example, for the advertising expenses).</span></span>
-   <span data-ttu-id="88464-126">**Mål** – Denne komponenten definerer hvordan resultatet til tildelingsberegningen skal distribueres og beregnes.</span><span class="sxs-lookup"><span data-stu-id="88464-126">**Destination** – This component defines how the result of the allocation calculation should be distributed and accounted for.</span></span> <span data-ttu-id="88464-127">Det kan for eksempel være én mållinje for hver avdeling.</span><span class="sxs-lookup"><span data-stu-id="88464-127">For example, there can be one destination line for each department.</span></span>
-   <span data-ttu-id="88464-128">**Forskyvning** – Denne komponenten definerer hvordan hovedkontoer og dimensjoner skal bestemmes for motoppføringene som balanserer måloppføringene.</span><span class="sxs-lookup"><span data-stu-id="88464-128">**Offset** – This component defines how main accounts and dimensions should be determined for the offset entries that balance the destination entries.</span></span> <span data-ttu-id="88464-129">Brukerdefinerte alternativer brukes vanligvis i stedet for kontoene og dimensjonene som er basert på kilden.</span><span class="sxs-lookup"><span data-stu-id="88464-129">User-defined options are typically used instead of accounts and dimensions that are based on the source.</span></span> <span data-ttu-id="88464-130">Når **datakilden** er satt til **Fast verdi**, kan ikke **Kilde** brukes som et alternativ.</span><span class="sxs-lookup"><span data-stu-id="88464-130">When **Data source** is set to **Fixed value**, **Source** can't be used as an option.</span></span>
-   <span data-ttu-id="88464-131">**Basisregler for finanstildeling** – Disse reglene bruker egne kildefilterkriterier for å bestemme hvilke finanssaldoer som skal brukes for tildeling (for eksempel omsetning per avdeling).</span><span class="sxs-lookup"><span data-stu-id="88464-131">**Ledger allocation basis rules** – These rules use their own source filter criteria to determine which ledger balances should be used for allocation (for example, the revenue per department).</span></span> <span data-ttu-id="88464-132">Hver fordelingsbasisregel kan brukes med flere fordelingsregler.</span><span class="sxs-lookup"><span data-stu-id="88464-132">Each allocation basis rule can be used with multiple allocation rules.</span></span>






[!INCLUDE[footer-include](../../includes/footer-banner.md)]