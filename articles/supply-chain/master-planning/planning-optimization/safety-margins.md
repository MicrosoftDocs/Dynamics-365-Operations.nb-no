---
title: Sikkerhetsmarginer
description: Dette emnet beskriver hvordan sikkerhetsmarginer kan brukes med tillegget for planleggingsoptimalisering for Microsoft Dynamics 365 Supply Chain Management.
author: ChristianRytt
ms.date: 09/14/2020
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
ms.search.validFrom: 2020-9-14
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 7b66951b9c742af4aa11f681af8f9583a2d97d8a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5841869"
---
# <a name="safety-margins"></a><span data-ttu-id="a1589-103">Sikkerhetsmarginer</span><span class="sxs-lookup"><span data-stu-id="a1589-103">Safety margins</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a1589-104">Dette emnet beskriver hvordan sikkerhetsmarginer kan brukes med tillegget for planleggingsoptimalisering for Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="a1589-104">This topic describes how safety margins can be used with the Planning Optimization Add-in for Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="safety-margins-overview"></a><span data-ttu-id="a1589-105">Oversikt over sikkerhetsmarginer</span><span class="sxs-lookup"><span data-stu-id="a1589-105">Safety margins overview</span></span>

<span data-ttu-id="a1589-106">Formålet med sikkerhetsmarginer er å aktivere et oppsett som gir litt ekstra tid i tillegg til den normale leveringstiden.</span><span class="sxs-lookup"><span data-stu-id="a1589-106">The purpose of safety margins is to enable a setup that provides some buffer time beyond the normal lead time.</span></span> <span data-ttu-id="a1589-107">Når materialer for eksempel må pakkes ut eller kontrolleres etter at de kommer fra leverandøren, kan du ikke legge til den ekstra tiden i leveringstiden, fordi denne fremgangsmåten vil gi leverandøren en ekstra buffertid.</span><span class="sxs-lookup"><span data-stu-id="a1589-107">For example, when material must be unpacked or inspected after it arrives from the vendor, you can't just add the extra time to the purchase lead time, because this approach will give the additional buffer time to the supplier.</span></span> <span data-ttu-id="a1589-108">I dette eksemplet kan mottaksmarginen brukes til å sikre at leverandøren leverer tidligere.</span><span class="sxs-lookup"><span data-stu-id="a1589-108">In this example, the receipt margin can be used to ensure that the supplier delivers earlier.</span></span> <span data-ttu-id="a1589-109">Denne fremgangsmåten gir buffertid slik at varene kan håndteres internt.</span><span class="sxs-lookup"><span data-stu-id="a1589-109">This approach provides buffer time so that the goods can be handled internally.</span></span>

<span data-ttu-id="a1589-110">Det finnes tre typer sikkerhetsmarginer:</span><span class="sxs-lookup"><span data-stu-id="a1589-110">There are three types of safety margins:</span></span>

- <span data-ttu-id="a1589-111">**Gjenbestillingsmargin** – buffertiden for å plassere forsyningsordren</span><span class="sxs-lookup"><span data-stu-id="a1589-111">**Reorder margin** – The buffer time for placing the supply order</span></span>
- <span data-ttu-id="a1589-112">**Mottaksmargin** – buffertiden for håndtering av innkommende forsyninger</span><span class="sxs-lookup"><span data-stu-id="a1589-112">**Receipt margin** – The buffer time for handling incoming supply</span></span>
- <span data-ttu-id="a1589-113">**Avgangsmargin** – buffertiden for håndtering av forsendelser</span><span class="sxs-lookup"><span data-stu-id="a1589-113">**Issue margin** – The buffer time for handling shipments</span></span>

<span data-ttu-id="a1589-114">Illustrasjonen nedenfor viser hvordan disse sikkerhetsmarginene gjelder over tid.</span><span class="sxs-lookup"><span data-stu-id="a1589-114">The following illustration shows how these safety margins apply over time.</span></span>

![Sikkerhetsmarginer](media/safety-margins-1.png)

<span data-ttu-id="a1589-116">Alle marginer er definert i dager.</span><span class="sxs-lookup"><span data-stu-id="a1589-116">All margins are defined in days.</span></span> <span data-ttu-id="a1589-117">Standardverdien, *0* (null), angir at ingen margin er i bruk.</span><span class="sxs-lookup"><span data-stu-id="a1589-117">The default value, *0* (zero), indicates that no margin is applied.</span></span> <span data-ttu-id="a1589-118">Hvis du definerer flere marginer, legger de alle til den totale tiden fra forsyningens *ordredato* til etterspørselens *behovsdato*.</span><span class="sxs-lookup"><span data-stu-id="a1589-118">If you set up multiple margins, they all add to the total time from the supply *order date* to the demand *requirement date*.</span></span> <span data-ttu-id="a1589-119">Et oppsett har for eksempel ingen leveringstid, og alle tre margintypene er satt til én dag.</span><span class="sxs-lookup"><span data-stu-id="a1589-119">For example, a setup has no lead time, and all three margin types are set to one day.</span></span> <span data-ttu-id="a1589-120">I dette tilfellet vil det være tre dager mellom forsyningsordredatoen og etterspørselsbehovsdatoen, så hvis ordredatoen er 1. juli, vil behovsdatoen være 4. juli.</span><span class="sxs-lookup"><span data-stu-id="a1589-120">In this case, there will be three days between the supply order date and the demand requirement date, so if the order date is July 1, the requirement date would be July 4.</span></span>

### <a name="receipt-margin"></a><span data-ttu-id="a1589-121">Mottaksmargin</span><span class="sxs-lookup"><span data-stu-id="a1589-121">Receipt margin</span></span>

<span data-ttu-id="a1589-122">Mottaksmarginen er sannsynligvis den mest brukte av de tre sikkerhetsmarginene.</span><span class="sxs-lookup"><span data-stu-id="a1589-122">The receipt margin is probably the most used of the three safety margins.</span></span> <span data-ttu-id="a1589-123">Den brukes på *leveringsdatoen* og bakover fra *behovsdatoen*.</span><span class="sxs-lookup"><span data-stu-id="a1589-123">It's applied to the *delivery date* and backward from the *requirement date*.</span></span> <span data-ttu-id="a1589-124">Med andre ord bør produktene motta det angitte antallet mottaksmargindager før de er påkrevd.</span><span class="sxs-lookup"><span data-stu-id="a1589-124">In other words, the products should be received the specified number of receipt margin days before they are required.</span></span>

<span data-ttu-id="a1589-125">Illustrasjonen nedenfor uthever mottaksmargin.</span><span class="sxs-lookup"><span data-stu-id="a1589-125">The following illustration highlights the receipt margin.</span></span>

![Mottaksmargin](media/safety-margins-2.png)

<span data-ttu-id="a1589-127">Mottaksmarginen brukes vanligvis som en buffer for å sikre tiden for lagerregistrering eller andre tidkrevende prosesser som ikke blir registrert som en del av den generelle leveringstiden i systemet.</span><span class="sxs-lookup"><span data-stu-id="a1589-127">The receipt margin is typically used as a buffer to ensure time for warehouse registration or other time-consuming processes that aren't captured as part of the general lead time in the system.</span></span> <span data-ttu-id="a1589-128">For innkjøp er én fordel at *leveringsdatoen* for bestillingen flyttes videre fremover i henhold til dette.</span><span class="sxs-lookup"><span data-stu-id="a1589-128">For purchases, one benefit is that the *delivery date* of the purchase order is moved forward accordingly.</span></span> <span data-ttu-id="a1589-129">Hvis du øker leveringstiden i stedet for å bruke en sikkerhetsmargin, vil leverandøren likevel bli bedt om å levere i siste liten.</span><span class="sxs-lookup"><span data-stu-id="a1589-129">If you  increase the lead time instead of using a safety margin, the vendor will still be asked to deliver at the last minute.</span></span>

<span data-ttu-id="a1589-130">Legg merke til at mottaksmarginen ikke endrer *behovsdatoen* til forsyningen.</span><span class="sxs-lookup"><span data-stu-id="a1589-130">Notice that the receipt margin doesn't change the *requirement date* of the supply.</span></span> <span data-ttu-id="a1589-131">Derfor vil ikke mottaksmarginen være direkte synlig når behovsdatoer for etterspørsel og forsyning sammenlignes (for eksempel på siden **Nettobehov**).</span><span class="sxs-lookup"><span data-stu-id="a1589-131">Therefore, the receipt margin isn't directly visible when requirement dates for demand and supply are compared (for example, on the **Net requirements** page).</span></span> <span data-ttu-id="a1589-132">Hvis mottaksmarginen for eksempel er satt til fire dager, og en bestillingslinje er planlagt for mottak den 15. i måneden, beregner hovedplanleggingen den justerte mottaksdatoen som den 19. i måneden.</span><span class="sxs-lookup"><span data-stu-id="a1589-132">For example, if the receipt margin is set to four days, and a purchase order line is planned for receipt on the fifteenth of the month, master planning calculates the adjusted receipt date as the nineteenth of the month.</span></span>

<span data-ttu-id="a1589-133">Legg merke til at en mottaksmargin ikke brukes når lagerbeholdningen brukes som forsyningen.</span><span class="sxs-lookup"><span data-stu-id="a1589-133">Note that a receipt margin isn't applied when on-hand inventory is used as the supply.</span></span> <span data-ttu-id="a1589-134">Alle lagerbeholdninger antas å være tilgjengelige umiddelbart, uansett når de faktisk er mottatt.</span><span class="sxs-lookup"><span data-stu-id="a1589-134">All on-hand inventory is assumed to be available immediately, regardless of when it was actually received.</span></span>

### <a name="reorder-margin"></a><span data-ttu-id="a1589-135">Gjenbestillingsmargin</span><span class="sxs-lookup"><span data-stu-id="a1589-135">Reorder margin</span></span>

> [!NOTE]
> <span data-ttu-id="a1589-136">**Kommer snart:** Denne funksjonen støttes ennå ikke for planleggingsoptimalisering.</span><span class="sxs-lookup"><span data-stu-id="a1589-136">**Coming soon:** This feature isn't yet supported for Planning Optimization.</span></span> <span data-ttu-id="a1589-137">Før den støttes, vil alle verdier som angis for **Gjenbestillingsmargin lagt til vareleveringstiden**, behandles som *0* (null).</span><span class="sxs-lookup"><span data-stu-id="a1589-137">Until it's supported, all values that are entered for **Reorder margin added to item lead time** will be treated as *0* (zero).</span></span>

<span data-ttu-id="a1589-138">Illustrasjonen nedenfor uthever gjenbestillingsmarginen.</span><span class="sxs-lookup"><span data-stu-id="a1589-138">The following illustration highlights the reorder margin.</span></span>

![Gjenbestillingsmargin](media/safety-margins-3.png)

<span data-ttu-id="a1589-140">Gjenbestillingsmarginen legges til før varens leveringstid for alle planlagte ordrer under hovedplanlegging.</span><span class="sxs-lookup"><span data-stu-id="a1589-140">The reorder margin is added before the item lead time for all planned orders during master planning.</span></span> <span data-ttu-id="a1589-141">Derfor sikres tilleggstiden for en forsyningsordre.</span><span class="sxs-lookup"><span data-stu-id="a1589-141">Therefore, it ensures additional time for a supply order to be placed.</span></span> <span data-ttu-id="a1589-142">Denne marginen brukes vanligvis som en buffer for å sikre tiden for godkjenningsprosesser eller andre interne prosesser som kreves ved opprettingen av forsyningsordrer.</span><span class="sxs-lookup"><span data-stu-id="a1589-142">This margin is typically used as a buffer to ensure time for approval processes or other internal processes that are required during the creation of supply orders.</span></span> <span data-ttu-id="a1589-143">Gjenbestillingsmarginen plasseres mellom forsyningens *ordredato* og *startdato*.</span><span class="sxs-lookup"><span data-stu-id="a1589-143">The reorder margin is put between the supply *order date* and *start date*.</span></span>

### <a name="issue-margin"></a><span data-ttu-id="a1589-144">Avgangsmargin</span><span class="sxs-lookup"><span data-stu-id="a1589-144">Issue margin</span></span>

> [!NOTE]
> <span data-ttu-id="a1589-145">**Kommer snart:** Denne funksjonen støttes ennå ikke for planleggingsoptimalisering.</span><span class="sxs-lookup"><span data-stu-id="a1589-145">**Coming soon:** This feature isn't yet supported for Planning Optimization.</span></span> <span data-ttu-id="a1589-146">Før den støttes, vil alle verdier som angis for **Avgangsmargin trukket fra behovsdato**, behandles som *0* (null).</span><span class="sxs-lookup"><span data-stu-id="a1589-146">Until it's supported, all values that are entered for **Issue margin deducted from requirement date** will be treated as *0* (zero).</span></span>

<span data-ttu-id="a1589-147">Illustrasjonen nedenfor uthever avgangsmarginen.</span><span class="sxs-lookup"><span data-stu-id="a1589-147">The following illustration highlights the issue margin.</span></span>

![Avgangsmargin](media/safety-margins-4.png)

<span data-ttu-id="a1589-149">Avgangsmarginen trekkes fra etterspørselens behovsdato under hovedplanleggingen.</span><span class="sxs-lookup"><span data-stu-id="a1589-149">The issue margin is deducted from the demand requirement date during master planning.</span></span> <span data-ttu-id="a1589-150">Den bildrar til å sikre at du har tid til å respondere på og sende innkommende ordrer.</span><span class="sxs-lookup"><span data-stu-id="a1589-150">It helps ensure that you have time to react to and ship incoming demand orders.</span></span> <span data-ttu-id="a1589-151">Denne marginen brukes vanligvis som en buffer for å sikre tid for forsendelse og tilknyttede utgående lagerprosesser.</span><span class="sxs-lookup"><span data-stu-id="a1589-151">This margin is typically used as a buffer to ensure time for shipment and related outbound warehouse processes.</span></span>

<span data-ttu-id="a1589-152">Legg merke til at når det gjelder en avgangsmargin, samsvarer ikke relaterte forsyninger og etterspørselens behovsdatoer.</span><span class="sxs-lookup"><span data-stu-id="a1589-152">Notice that when an issue margin is applied, related supply and demand requirement dates don't match.</span></span> <span data-ttu-id="a1589-153">De avviker i stedet etter avgangsmarginen, fordi avgangsmarginen legges til mellom forsyningens *behovsdato* og etterspørselens *behovsdato*.</span><span class="sxs-lookup"><span data-stu-id="a1589-153">Instead, they differ by the issue margin, because the issue margin is added between the supply *requirement date* and the demand *requirement date*.</span></span>

## <a name="set-up-safety-margins"></a><span data-ttu-id="a1589-154">Definere sikkerhetsmarginer</span><span class="sxs-lookup"><span data-stu-id="a1589-154">Set up safety margins</span></span>

### <a name="turn-on-safety-margins-in-feature-management"></a><span data-ttu-id="a1589-155">Aktiver sikkerhetsmarginer i Funksjonsbehandling</span><span class="sxs-lookup"><span data-stu-id="a1589-155">Turn on safety margins in Feature management</span></span>

<span data-ttu-id="a1589-156">Før du kan bruke denne funksjonen med planleggingsoptimalisering, må den være aktivert i systemet.</span><span class="sxs-lookup"><span data-stu-id="a1589-156">Before you can use this feature with Planning Optimization, it must be turned on in your system.</span></span> <span data-ttu-id="a1589-157">Administratorer kan bruke [Funksjonsbehandling](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview)-arbeidsområdet til å kontrollere funksjonsstatusen og aktivere den hvis den kreves.</span><span class="sxs-lookup"><span data-stu-id="a1589-157">Admins can use the [Feature management](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="a1589-158">Funksjonen vises på følgende måte:</span><span class="sxs-lookup"><span data-stu-id="a1589-158">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="a1589-159">**Modul:** _Hovedplanlegging_</span><span class="sxs-lookup"><span data-stu-id="a1589-159">**Module:** _Master planning_</span></span>
- <span data-ttu-id="a1589-160">**Funksjonsnavn:** _Marginer for planleggingsoptimalisering_</span><span class="sxs-lookup"><span data-stu-id="a1589-160">**Feature name:** _Margins for Planning Optimization_</span></span>

### <a name="define-safety-margins"></a><span data-ttu-id="a1589-161">Definere sikkerhetsmarginer</span><span class="sxs-lookup"><span data-stu-id="a1589-161">Define safety margins</span></span>

<span data-ttu-id="a1589-162">Sikkerhetsmarginer har et fleksibelt oppsett.</span><span class="sxs-lookup"><span data-stu-id="a1589-162">Safety margins have a flexible setup.</span></span> <span data-ttu-id="a1589-163">De kan angis både for *dekningsgruppen* og *hovedplanen*.</span><span class="sxs-lookup"><span data-stu-id="a1589-163">They can be set on both the *coverage group* and the *master plan*.</span></span> <span data-ttu-id="a1589-164">Det er viktig at du forstår at marginene legges oppå hverandre.</span><span class="sxs-lookup"><span data-stu-id="a1589-164">It's important that you understand that the margins are added on top of each other.</span></span> <span data-ttu-id="a1589-165">En mottaksmargin på to dager i dekningsgruppen og tre dager i hovedplanen vil for eksempel produsere en effektiv mottaksmargin på fem dager.</span><span class="sxs-lookup"><span data-stu-id="a1589-165">For example, a receipt margin of two days on the coverage group and three days on the master plan will produce an effective receipt margin of five days.</span></span>

<span data-ttu-id="a1589-166">Muligheten til å angi marginen på hovedplanen kan være nyttig når du vil simulere lengre leveringstider eller -opplegg for en bestemt plan, men uten å påvirke den daglige planleggingen.</span><span class="sxs-lookup"><span data-stu-id="a1589-166">The ability to set the margin on the master plan can be useful when you want to simulate longer lead times or uncertainty for a specific plan, but without affecting the daily planning.</span></span>

#### <a name="coverage-group-safety-margins"></a><span data-ttu-id="a1589-167">Sikkerhetsmarginer for dekningsgruppe</span><span class="sxs-lookup"><span data-stu-id="a1589-167">Coverage group safety margins</span></span>

<span data-ttu-id="a1589-168">Hvis du vil bruke en sikkerhetsmargin for en dekningsgruppe, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="a1589-168">To apply a safety margin to a coverage group, follow these steps.</span></span>

1. <span data-ttu-id="a1589-169">Gå til **Hovedplanlegging \> Oppsett \> Dekningsgrupper**.</span><span class="sxs-lookup"><span data-stu-id="a1589-169">Go to **Master planning \> Setup \> Coverage groups**.</span></span>
1. <span data-ttu-id="a1589-170">I listeruten velger du ønsket dekningsgruppe.</span><span class="sxs-lookup"><span data-stu-id="a1589-170">In the list pane, select the desired coverage group.</span></span>
1. <span data-ttu-id="a1589-171">I delen **Sikkerhetsmarginer i dager** i hurtigfanen **Annet** bruker du følgende felt til å angi påkrevde sikkerhetsmarginer (i dager):</span><span class="sxs-lookup"><span data-stu-id="a1589-171">On the **Other** FastTab, in the **Safety margins in days** section, use the following fields to set the required safety margins (in days):</span></span>

    - <span data-ttu-id="a1589-172">Påslag dager lagt til i behovsdato</span><span class="sxs-lookup"><span data-stu-id="a1589-172">Receipt margin added to requirement date</span></span>
    - <span data-ttu-id="a1589-173">Sikkerhetsdager trukket fra behovsdato</span><span class="sxs-lookup"><span data-stu-id="a1589-173">Issue margin deducted from requirement date</span></span>
    - <span data-ttu-id="a1589-174">Respittid, gjenbestilling lagt til vareleveringstiden</span><span class="sxs-lookup"><span data-stu-id="a1589-174">Reorder margin added to item lead time</span></span>

#### <a name="master-plan-safety-margins"></a><span data-ttu-id="a1589-175">Sikkerhetsmarginer for hovedplan</span><span class="sxs-lookup"><span data-stu-id="a1589-175">Master plan safety margins</span></span>

<span data-ttu-id="a1589-176">Hvis du vil bruke en sikkerhetsmargin for en hovedplan, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="a1589-176">To apply a safety margin to a master plan, follow these steps.</span></span>

1. <span data-ttu-id="a1589-177">Gå til **Hovedplanlegging \> Oppsett \> Planer \> Hovedplaner**.</span><span class="sxs-lookup"><span data-stu-id="a1589-177">Go to **Master planning \> Setup \> Plans \> Master plans**.</span></span>
1. <span data-ttu-id="a1589-178">I listeruten velger du den ønskede hovedplanen.</span><span class="sxs-lookup"><span data-stu-id="a1589-178">In the list pane, select the desired master plan.</span></span>
1. <span data-ttu-id="a1589-179">I hurtigfanen **Sikkerhetsmarginer i dager** bruker du følgende felt til å angi påkrevde sikkerhetsmarginer (i dager):</span><span class="sxs-lookup"><span data-stu-id="a1589-179">On the **Safety margins in days** FastTab, use the following fields to set the required safety margins (in days):</span></span>

    - <span data-ttu-id="a1589-180">Påslag dager lagt til i behovsdato</span><span class="sxs-lookup"><span data-stu-id="a1589-180">Receipt margin added to requirement date</span></span>
    - <span data-ttu-id="a1589-181">Sikkerhetsdager trukket fra behovsdato</span><span class="sxs-lookup"><span data-stu-id="a1589-181">Issue margin deducted from requirement date</span></span>
    - <span data-ttu-id="a1589-182">Respittid, gjenbestilling lagt til vareleveringstiden</span><span class="sxs-lookup"><span data-stu-id="a1589-182">Reorder margin added to item lead time</span></span>

### <a name="define-whether-calculations-are-based-on-calendar-days-or-work-days"></a><span data-ttu-id="a1589-183">Definere om beregninger skal baseres på kalenderdager eller virkedager</span><span class="sxs-lookup"><span data-stu-id="a1589-183">Define whether calculations are based on calendar days or work days</span></span>

<span data-ttu-id="a1589-184">Du kan angi alle sikkerhetsmarginer slik at de beregnes på grunnlag av enten kalenderdager eller virkedager.</span><span class="sxs-lookup"><span data-stu-id="a1589-184">You can set all safety margins so that they are calculated based on either calendar days or work days.</span></span>

1. <span data-ttu-id="a1589-185">Gå til **Hovedplanlegging \> Oppsett \> Parametere for hovedplanlegging**.</span><span class="sxs-lookup"><span data-stu-id="a1589-185">Go to **Master planning \> Setup \> Master planning parameters**.</span></span>
1. <span data-ttu-id="a1589-186">I fanen **Generelt** i delen **Sikkerhetsmarginer i dager** setter du alternativet **virkedager** til *Ja* for å beregne marginer basert på virkedager.</span><span class="sxs-lookup"><span data-stu-id="a1589-186">On the **General** tab, in the **Safety margins in days** section, set the **Working days** option to *Yes* to calculate margins based on working days.</span></span> <span data-ttu-id="a1589-187">Sett alternativet til *Nei* for å beregne marginer basert på kalenderdager.</span><span class="sxs-lookup"><span data-stu-id="a1589-187">Set the option to *No* to calculate margins based on calendar days.</span></span>

<span data-ttu-id="a1589-188">En kalender kan for eksempel være åpen fra mandag til fredag og avsluttes fra lørdag til og med søndag.</span><span class="sxs-lookup"><span data-stu-id="a1589-188">For example, a calendar is open from Monday through Friday and closed from Saturday through Sunday.</span></span> <span data-ttu-id="a1589-189">Hvis det er en mottaksmargin på én dag, vil en behovsdato på en mandag generere en leveringsdato på forrige fredag, ettersom lørdag og søndag ikke er virkedager.</span><span class="sxs-lookup"><span data-stu-id="a1589-189">If there is a receipt margin of one day, a requirement date on a Monday produces a delivery date on the previous Friday, because Saturday and Sunday aren't working days.</span></span>

<span data-ttu-id="a1589-190">Kalenderen som brukes til å fastslå virkedagene, avhenger av oppsettet og forsyningstypen.</span><span class="sxs-lookup"><span data-stu-id="a1589-190">The calendar that is used to determine the working days depends on the setup and the supply type.</span></span> <span data-ttu-id="a1589-191">Den kan styres av kalenderne til dekningsgruppen, lageret og leverandøren.</span><span class="sxs-lookup"><span data-stu-id="a1589-191">It can be controlled by the calendars of the coverage group, the warehouse, and the vendor.</span></span>

> [!NOTE]
> <span data-ttu-id="a1589-192">Hvis *lageret* ikke er en del av dekningsdimensjonen (med andre ord er planlegging bare basert på *område*), brukes ikke lagerkalenderen.</span><span class="sxs-lookup"><span data-stu-id="a1589-192">If *warehouse* isn't part of the coverage dimension (in other words, planning is based only on *site*), the warehouse calendar isn't used.</span></span>

<span data-ttu-id="a1589-193">Systemet kan håndtere et oppsett der én eller flere kalendere er definert.</span><span class="sxs-lookup"><span data-stu-id="a1589-193">The system can handle a setup where one or more calendars are defined.</span></span> <span data-ttu-id="a1589-194">Underdelene nedenfor beskriver de mulige kombinasjonene som kan brukes til å kontrollere resultatet.</span><span class="sxs-lookup"><span data-stu-id="a1589-194">The following subsections describe the possible combinations that can be used to control the result.</span></span>

#### <a name="calendar-that-is-used-for-the-duration"></a><span data-ttu-id="a1589-195">Kalender som brukes for varigheten</span><span class="sxs-lookup"><span data-stu-id="a1589-195">Calendar that is used for the duration</span></span>

<span data-ttu-id="a1589-196">De definerte kalenderne styrer den faktiske totale leveringstiden i kalenderdager, fra forsyningens ordredato til etterspørselens behovsdato.</span><span class="sxs-lookup"><span data-stu-id="a1589-196">The defined calendars control the actual total lead time in calendar days, from the supply order date to the demand requirement date.</span></span> <span data-ttu-id="a1589-197">Følgende kalenderprioritering brukes:</span><span class="sxs-lookup"><span data-stu-id="a1589-197">The following calendar prioritization is used:</span></span>

- <span data-ttu-id="a1589-198">**Leveringstid for innkjøp** – bare dekningsgruppekalenderen vurderes.</span><span class="sxs-lookup"><span data-stu-id="a1589-198">**Purchase lead time** – Only the coverage group calendar is considered.</span></span>
- <span data-ttu-id="a1589-199">**Mottaksmargin** – dekningsgruppekalenderen brukes hvis den er definert.</span><span class="sxs-lookup"><span data-stu-id="a1589-199">**Receipt margin** – The coverage group calendar is used, if it's defined.</span></span> <span data-ttu-id="a1589-200">Ellers brukes lagerkalenderen.</span><span class="sxs-lookup"><span data-stu-id="a1589-200">Otherwise, the warehouse calendar is used.</span></span>
- <span data-ttu-id="a1589-201">**Avgangsmargin** – dekningsgruppekalenderen brukes hvis den er definert.</span><span class="sxs-lookup"><span data-stu-id="a1589-201">**Issue margin** – The coverage group calendar is used, if it's defined.</span></span> <span data-ttu-id="a1589-202">Ellers brukes lagerkalenderen.</span><span class="sxs-lookup"><span data-stu-id="a1589-202">Otherwise, the warehouse calendar is used.</span></span>
- <span data-ttu-id="a1589-203">**Ordremargin** – bare dekningsgruppekalenderen vurderes.</span><span class="sxs-lookup"><span data-stu-id="a1589-203">**Order margin** – Only the coverage group calendar is considered.</span></span>

#### <a name="calendar-that-is-used-for-the-final-date"></a><span data-ttu-id="a1589-204">Kalender som brukes for sluttdatoen</span><span class="sxs-lookup"><span data-stu-id="a1589-204">Calendar that is used for the final date</span></span>

<span data-ttu-id="a1589-205">Følgende regler brukes for å fastslå om planleggingsmotoren kan bruke en angitt dato for en bestemt datotype:</span><span class="sxs-lookup"><span data-stu-id="a1589-205">The following rules are applied to determine whether the planning engine can use a given date for a given date type:</span></span>

- <span data-ttu-id="a1589-206">**Mottaksdato for innkjøp** – leverandørkalenderen brukes hvis den er definert.</span><span class="sxs-lookup"><span data-stu-id="a1589-206">**Purchase receipt date** – The vendor calendar is used, if it's defined.</span></span> <span data-ttu-id="a1589-207">Ellers brukes dekningsgruppekalenderen hvis den er definert.</span><span class="sxs-lookup"><span data-stu-id="a1589-207">Otherwise, the coverage group calendar is used, if it's defined.</span></span> <span data-ttu-id="a1589-208">Hvis ingen av disse kalenderne er definert, brukes lagerkalenderen.</span><span class="sxs-lookup"><span data-stu-id="a1589-208">If neither of those calendars is defined, the warehouse calendar is used.</span></span>
- <span data-ttu-id="a1589-209">**Mottaksdato for overføring** – dekningsgruppekalenderen brukes hvis den er definert.</span><span class="sxs-lookup"><span data-stu-id="a1589-209">**Transfer receipt date** – The coverage group calendar is used, if it's defined.</span></span> <span data-ttu-id="a1589-210">Ellers brukes lagerkalenderen.</span><span class="sxs-lookup"><span data-stu-id="a1589-210">Otherwise, the warehouse calendar is used.</span></span>
- <span data-ttu-id="a1589-211">**Mottaksdato for produksjon** – dekningsgruppekalenderen brukes hvis den er definert.</span><span class="sxs-lookup"><span data-stu-id="a1589-211">**Production receipt date** – The coverage group calendar is used, if it's defined.</span></span> <span data-ttu-id="a1589-212">Ellers brukes lagerkalenderen.</span><span class="sxs-lookup"><span data-stu-id="a1589-212">Otherwise, the warehouse calendar is used.</span></span>
- <span data-ttu-id="a1589-213">**Åpen dag for etterspørselsbehov** – lagerkalenderen brukes hvis den er definert.</span><span class="sxs-lookup"><span data-stu-id="a1589-213">**Demand issue open day** – The warehouse calendar is used, if it's defined.</span></span> <span data-ttu-id="a1589-214">Ellers brukes dekningsgruppekalenderen.</span><span class="sxs-lookup"><span data-stu-id="a1589-214">Otherwise, the coverage group calendar is used.</span></span>
- <span data-ttu-id="a1589-215">**Åpen dag for ordre** – en kombinasjon (skjæringspunkt) av dekningsgruppekalenderen og leverandørkalenderen brukes.</span><span class="sxs-lookup"><span data-stu-id="a1589-215">**Order open day** – A combination (intersection) of the coverage group calendar and the vendor calendar is used.</span></span> <span data-ttu-id="a1589-216">Begge kalenderne må være åpne for å bruke datoen.</span><span class="sxs-lookup"><span data-stu-id="a1589-216">Both calendars must be open to use the date.</span></span> <span data-ttu-id="a1589-217">Hvis bare én av kalendrne er definert, brukes kun den kalenderen.</span><span class="sxs-lookup"><span data-stu-id="a1589-217">If only one of the calendars is defined, that calendar is used alone.</span></span>

#### <a name="calendar-setup-overview-matrix"></a><span data-ttu-id="a1589-218">Matrise for oversikt over kalenderoppsett</span><span class="sxs-lookup"><span data-stu-id="a1589-218">Calendar setup overview matrix</span></span>

<span data-ttu-id="a1589-219">Illustrasjonen nedenfor viser en matrise som oppsummerer hvilke kalendere som gjelder når det beregnes sikkerhetsmarginer.</span><span class="sxs-lookup"><span data-stu-id="a1589-219">The following illustration presents a matrix that summarizes which calendars apply when safety margins are calculated.</span></span> <span data-ttu-id="a1589-220">(Velg bildet for å åpne en høyoppløsningsversjon av det.) Følgende forkortelser og farger brukes til å angi hvor hver type kalender er angitt:</span><span class="sxs-lookup"><span data-stu-id="a1589-220">(Select the image to open a high-resolution version of it.) The following abbreviations and colors are used to indicate where each type of calendar is specified:</span></span>

- <span data-ttu-id="a1589-221">**Dekningsgruppe (CG):** Grønn</span><span class="sxs-lookup"><span data-stu-id="a1589-221">**Coverage group (CG):** Green</span></span>
- <span data-ttu-id="a1589-222">**Lager (WH):** Gul</span><span class="sxs-lookup"><span data-stu-id="a1589-222">**Warehouse (WH):** Yellow</span></span>
- <span data-ttu-id="a1589-223">**Leverandør (V):** Blå</span><span class="sxs-lookup"><span data-stu-id="a1589-223">**Vendor (V):** Blue</span></span>

<span data-ttu-id="a1589-224">[![Matrise for oversikt over kalenderoppsett](media/safety-margins-calendar-matrix.png)](media/safety-margins-calendar-matrix-high.png)</span><span class="sxs-lookup"><span data-stu-id="a1589-224">[![Calendar setup overview matrix](media/safety-margins-calendar-matrix.png)](media/safety-margins-calendar-matrix-high.png)</span></span>

## <a name="calculating-delays"></a><span data-ttu-id="a1589-225">Beregne forsinkelser</span><span class="sxs-lookup"><span data-stu-id="a1589-225">Calculating delays</span></span>

<span data-ttu-id="a1589-226">Alle tre typer sikkerhetsmarginer tas med når systemet fastslår om en ordre er forsinket.</span><span class="sxs-lookup"><span data-stu-id="a1589-226">All three types of safety margins are included when the system determines whether an order is delayed.</span></span>

<span data-ttu-id="a1589-227">En vare har for eksempel innledende tid på én dag og en mottaksmargin på tre dager.</span><span class="sxs-lookup"><span data-stu-id="a1589-227">For example, an item has lead time of one day and a receipt margin of three days.</span></span> <span data-ttu-id="a1589-228">En salgsordre for denne varen er angitt som nødvendig i dag.</span><span class="sxs-lookup"><span data-stu-id="a1589-228">A sales order for this item is set as required today.</span></span> <span data-ttu-id="a1589-229">I dette tilfellet blir forsinkelsen beregnet som *leveringstid* + *mottaksmargin* = fire dager.</span><span class="sxs-lookup"><span data-stu-id="a1589-229">In this case, the delay is calculated as *lead time* + *receipt margin* = four days.</span></span> <span data-ttu-id="a1589-230">Hvis i dag er 14. august, fører de fire dagene med forsinkelse til at leveringen blir 18. august.</span><span class="sxs-lookup"><span data-stu-id="a1589-230">Therefore, if today is August 14, the four days of delay produces a delivery on August 18.</span></span> <span data-ttu-id="a1589-231">Illustrasjonen nedenfor viser dette eksemplet.</span><span class="sxs-lookup"><span data-stu-id="a1589-231">The following illustration shows this example.</span></span>

![Eksempel på forsinkelsesberegning](media/safety-margins-delays.png)

## <a name="additional-resources"></a><span data-ttu-id="a1589-233">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="a1589-233">Additional resources</span></span>

[<span data-ttu-id="a1589-234">Komme i gang med planleggingsoptimalisering</span><span class="sxs-lookup"><span data-stu-id="a1589-234">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="a1589-235">Analyse for tilpassing av planleggingsoptimalisering</span><span class="sxs-lookup"><span data-stu-id="a1589-235">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]