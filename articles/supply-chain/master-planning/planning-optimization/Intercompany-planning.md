---
title: Konsernintern planlegging
description: Dette emnet beskriver konsernintern planlegging og forklarer hvordan du konfigurerer konsernintern planlegging med planleggingsoptimalisering i Microsoft Dynamics 365 Supply Chain Management.
author: ChristianRytt
manager: tfehr
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 25c80ce27498131c6eb92174ab14a592bfa9915a
ms.sourcegitcommit: fe21a3a98dcf6fe4eb9351941493f2c0443d8696
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/04/2020
ms.locfileid: "4672200"
---
# <a name="intercompany-planning"></a><span data-ttu-id="37771-103">Konsernintern planlegging</span><span class="sxs-lookup"><span data-stu-id="37771-103">Intercompany planning</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="37771-104">For noen organisasjoner er logistikkoperasjoner avhengige av andre juridiske enheter (firmaer) i organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="37771-104">For some organizations, logistics operations depend on other legal entities (companies) in the organization.</span></span> <span data-ttu-id="37771-105">Disse operasjonene håndteres ved hjelp av konserninterne salg og innkjøp, fordi hver juridiske enhet har en egen kontoplan.</span><span class="sxs-lookup"><span data-stu-id="37771-105">These operations are handled by using intercompany sales and purchases, because each legal entity has a separate chart of accounts.</span></span>

<span data-ttu-id="37771-106">Dette emnet beskriver konsernintern planlegging og forklarer hvordan du konfigurerer konsernintern planlegging med planleggingsoptimalisering i Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="37771-106">This topic describes intercompany planning and explains how to configure intercompany planning with Planning Optimization in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="37771-107">Dette emnet bruker følgende viktige, konserninterne vilkår:</span><span class="sxs-lookup"><span data-stu-id="37771-107">This topic uses the following important intercompany terms:</span></span>

- <span data-ttu-id="37771-108">**Oppstrøms** – En relativ referanse i en autorisasjons- eller forsyningskjede.</span><span class="sxs-lookup"><span data-stu-id="37771-108">**Upstream** – A relative reference in a firm or supply chain.</span></span> <span data-ttu-id="37771-109">Den viser bevegelse i retningen til råvareleverandøren.</span><span class="sxs-lookup"><span data-stu-id="37771-109">It indicates movement in the direction of the raw material supplier.</span></span>
- <span data-ttu-id="37771-110">**Nedstrøms** – En relativ referanse i en autorisasjons- eller forsyningskjede.</span><span class="sxs-lookup"><span data-stu-id="37771-110">**Downstream** – A relative reference in a firm or supply chain.</span></span> <span data-ttu-id="37771-111">Den viser bevegelse i retningen til kunden.</span><span class="sxs-lookup"><span data-stu-id="37771-111">It indicates movement in the direction of the customer.</span></span>
- <span data-ttu-id="37771-112">**Planlagt konsernintern etterspørsel** – Planlagt etterspørsel for et produkt i et firma, basert på planlagt etterspørsel for produktet fra et nedstrømsfirma.</span><span class="sxs-lookup"><span data-stu-id="37771-112">**Planned intercompany demand** – Planned demand for a product in a company, based on planned demand for the product from a downstream company.</span></span>

<span data-ttu-id="37771-113">I hovedplanlegging kan en plan i ett firma omfatte planlagt konsernintern etterspørsel som er knyttet til planlagte ordrer fra en plan i et annet firma.</span><span class="sxs-lookup"><span data-stu-id="37771-113">In master planning, a plan in one company can include planned intercompany demand that is related to planned orders from a plan in another company.</span></span> <span data-ttu-id="37771-114">Denne muligheten er nyttig, fordi den gir full oversikt over planlagte ordrer på tvers av firmaer.</span><span class="sxs-lookup"><span data-stu-id="37771-114">This capability is useful, because it provides full visibility into planned orders across companies.</span></span> <span data-ttu-id="37771-115">Det sikrer også at alle nødvendige planlagte forsyningsordrer opprettes, men uten at det kreves at planlagte ordrer autoriseres for den konsernintern etterspørselen.</span><span class="sxs-lookup"><span data-stu-id="37771-115">It also ensures that all required planned supply orders are created, but without requiring that planned orders be firmed for the intercompany demand.</span></span>

<span data-ttu-id="37771-116">Hvis du kjører hovedplanlegging fra en hovedplan som inkluderer planlagt nedstrømsetterspørsel, vil planlagte ordrer fra de relaterte konserninterne leverandørene bli tatt med i planen som etterspørsel.</span><span class="sxs-lookup"><span data-stu-id="37771-116">If you run master planning from a master plan that includes planned downstream demand, planned purchase orders from the related intercompany vendors will be included in the plan as demand.</span></span>

## <a name="required-setup"></a><span data-ttu-id="37771-117">Obligatorisk oppsett</span><span class="sxs-lookup"><span data-stu-id="37771-117">Required setup</span></span>

<span data-ttu-id="37771-118">Hvis du vil bruke konsernintern planlegging, må du klargjøre systemet på følgende måte:</span><span class="sxs-lookup"><span data-stu-id="37771-118">To use intercompany planning, you must prepare your system in the following way:</span></span>

1. <span data-ttu-id="37771-119">De relevante produktene må frigis i alle de relevante firmaene.</span><span class="sxs-lookup"><span data-stu-id="37771-119">The relevant products must be released in all the relevant companies.</span></span> <span data-ttu-id="37771-120">Hvis du vil ha mer informasjon, kan du se [Konfigurer og bruk konsernintern handel i Dynamics 365 Supply Chain Management ](https://docs.microsoft.com/learn/modules/configure-use-intercompany-trade-dyn365-supply-chain-mgmt/) på Microsoft Learn.</span><span class="sxs-lookup"><span data-stu-id="37771-120">For more information, see [Configure and use intercompany trade in Dynamics 365 Supply Chain Management ](https://docs.microsoft.com/learn/modules/configure-use-intercompany-trade-dyn365-supply-chain-mgmt/) on Microsoft Learn.</span></span>
1. <span data-ttu-id="37771-121">Nedstrømsetterspørsel må dekkes av innkjøp fra en leverandør som har en konsernintern relasjon til oppstrømsfirmaet, og relevante standard lagerdimensjoner (område og lager) på kunden.</span><span class="sxs-lookup"><span data-stu-id="37771-121">Downstream demand must be covered by purchases from a vendor that has an intercompany relation to the upstream company and relevant default inventory dimensions (site and warehouse) on the customer.</span></span> <span data-ttu-id="37771-122">Hvis du vil ha mer informasjon, kan du se [Konfigurer og bruk konsernintern handel i Dynamics 365 Supply Chain Management ](https://docs.microsoft.com/learn/modules/configure-use-intercompany-trade-dyn365-supply-chain-mgmt/) på Microsoft Learn.</span><span class="sxs-lookup"><span data-stu-id="37771-122">For more information, see [Configure and use intercompany trade in Dynamics 365 Supply Chain Management ](https://docs.microsoft.com/learn/modules/configure-use-intercompany-trade-dyn365-supply-chain-mgmt/) on Microsoft Learn.</span></span>
1. <span data-ttu-id="37771-123">Hovedplanen i oppstrømsfirmaet må inkludere planlagt nedstrømsetterspørsel, og det relevante firmaet og hovedplanen må være angitt i nedstrømsplanene.</span><span class="sxs-lookup"><span data-stu-id="37771-123">The master plan in the upstream company must include planned downstream demand, and the relevant company and master plan must be specified in the downstream plans.</span></span>

## <a name="include-planned-downstream-demand"></a><span data-ttu-id="37771-124">Inkluder planlagt nedstrøms etterspørsel</span><span class="sxs-lookup"><span data-stu-id="37771-124">Include planned downstream demand</span></span>

<span data-ttu-id="37771-125">Følg denne fremgangsmåten for å konfigurere hovedplanen slik at den inneholder planlagt nedstrømsetterspørsel.</span><span class="sxs-lookup"><span data-stu-id="37771-125">Follow these steps to configure your master plan so that it includes planned downstream demand.</span></span>

1. <span data-ttu-id="37771-126">Gå til **Hovedplanlegging \> Oppsett \> Planer \> Hovedplaner**.</span><span class="sxs-lookup"><span data-stu-id="37771-126">Go to **Master planning \> Setup \> Plans \> Master plans**.</span></span>
1. <span data-ttu-id="37771-127">Velg eller opprett en hovedplan.</span><span class="sxs-lookup"><span data-stu-id="37771-127">Select or create a master plan.</span></span>
1. <span data-ttu-id="37771-128">Angi følgende felt i hurtigfanen **Konsertintern planlegging**:</span><span class="sxs-lookup"><span data-stu-id="37771-128">On the **Intercompany planning** FastTab, set the following fields:</span></span>

    - <span data-ttu-id="37771-129">**Inkluder planlagt nedstrømsetterspørsel** – Sett dette alternativet til *Ja* for å aktivere konsernintern planlegging for hovedplanen.</span><span class="sxs-lookup"><span data-stu-id="37771-129">**Include planned downstream demand** – Set this option to *Yes* to enable intercompany planning for the master plan.</span></span>
    - <span data-ttu-id="37771-130">**Nedstrømsplaner** – Hvis du setter alternativet **Inkluder planlagt nedstrømsetterspørsel** til *Ja*, bruker du verktøylinjen og rutenettet til å legge til de ønskede hovedplanene fra andre firmaer.</span><span class="sxs-lookup"><span data-stu-id="37771-130">**Downstream plans** – If you set the **Include planned downstream demand** option to *Yes*, use the toolbar and grid to add the desired master plans from other companies.</span></span>

## <a name="peg-across-companies-by-using-multilevel-pegging"></a><span data-ttu-id="37771-131">Utlign på tvers av firmaer ved bruk av flernivå utligning</span><span class="sxs-lookup"><span data-stu-id="37771-131">Peg across companies by using multilevel pegging</span></span>

<span data-ttu-id="37771-132">I utligning på flere nivåer kan du vise utligning på tvers av firmaer for å se den innledende kilden for etterspørsel som dekkes av en forsyning.</span><span class="sxs-lookup"><span data-stu-id="37771-132">In multilevel pegging, you can view pegging across companies to see the initial source of demand that is being covered by a supply.</span></span>

<span data-ttu-id="37771-133">Følg disse trinnene for å vise informasjon om utligning på flere nivåer.</span><span class="sxs-lookup"><span data-stu-id="37771-133">To view multilevel pegging information, follow these steps.</span></span>

1. <span data-ttu-id="37771-134">Gå til **Hovedplanlegging \> Hovedplanlegging \> Planlagte ordrer**.</span><span class="sxs-lookup"><span data-stu-id="37771-134">Go to **Master planning \> Master planning \> Planned orders**.</span></span>
1. <span data-ttu-id="37771-135">Velg eller åpne en planlagt ordre.</span><span class="sxs-lookup"><span data-stu-id="37771-135">Select or open a planned order.</span></span>
1. <span data-ttu-id="37771-136">På handlingsruten, i kategorien **Vis** i **Krav**-gruppen, velger du **Utligning på flere nivåer**.</span><span class="sxs-lookup"><span data-stu-id="37771-136">On the Action Pane, on the **View** tab, in the **Requirements** group, select **Multilevel pegging**.</span></span>

### <a name="intercompany-example-that-involves-two-companies"></a><span data-ttu-id="37771-137">Konserninternt eksempel som omfatter to firmaer</span><span class="sxs-lookup"><span data-stu-id="37771-137">Intercompany example that involves two companies</span></span>

<span data-ttu-id="37771-138">I dette eksemplet opprettes det en produksjonsordre i USMF-firmaet for å dekke en salgsordre i DEMF-firmaet.</span><span class="sxs-lookup"><span data-stu-id="37771-138">For this example, a planned production order is created in the USMF company to cover a sales order in the DEMF company.</span></span> <span data-ttu-id="37771-139">I USMF er direkte etterspørsel planlagt konsernintern etterspørsel.</span><span class="sxs-lookup"><span data-stu-id="37771-139">In USMF, the direct demand is planned intercompany demand.</span></span> <span data-ttu-id="37771-140">Hvis du vil at denne forespørselen skal vises i USMF, kjøres hovedplanlegging først i DEMF og deretter i USMF.</span><span class="sxs-lookup"><span data-stu-id="37771-140">To make this demand appear in USMF, master planning is run first in DEMF and then in USMF.</span></span>

<span data-ttu-id="37771-141">Illustrasjonen nedenfor viser hvordan dette eksemplet kan vises på siden **Utligning med flere nivåer** for den planlagte produksjonsordren.</span><span class="sxs-lookup"><span data-stu-id="37771-141">The following illustration shows how this example might appear on the **Multilevel pegging** page for the planned production order.</span></span>

![Konserninternt eksempel som omfatter to firmaer](media/IntercompanyPlanning1.png)

### <a name="intercompany-example-that-involves-three-companies"></a><span data-ttu-id="37771-143">Konserninternt eksempel som omfatter tre firmaer</span><span class="sxs-lookup"><span data-stu-id="37771-143">Intercompany example that involves three companies</span></span>

<span data-ttu-id="37771-144">I dette eksemplet opprettes det et bestillingsforslag i USMF-firmaet for å dekke en salgsordre i FRRT-firmaet.</span><span class="sxs-lookup"><span data-stu-id="37771-144">For this example, a planned purchase order is created in the USMF company to cover a sales order in the FRRT company.</span></span> <span data-ttu-id="37771-145">I DEMF- og USMF-firmaer er direkte etterspørsel planlagt konsernintern etterspørsel.</span><span class="sxs-lookup"><span data-stu-id="37771-145">In the DEMF and USMF companies, the direct demand is planned intercompany demand.</span></span> <span data-ttu-id="37771-146">Hvis du vil at denne etterspørselen skal vises i USMF, kjøres hovedplanlegging først i FRRT, deretter i DEMF og til slutt USMF.</span><span class="sxs-lookup"><span data-stu-id="37771-146">To make this demand appear in USMF, master planning is run first in FRRT, then in DEMF, and finally in USMF.</span></span>

<span data-ttu-id="37771-147">Illustrasjonen nedenfor viser hvordan dette eksemplet kan vises på siden **Utligning med flere nivåer** for den planlagte produksjonsordren.</span><span class="sxs-lookup"><span data-stu-id="37771-147">The following illustration shows how this example might appear on the **Multilevel pegging** page for the planned production order.</span></span>

![Konserninternt eksempel som omfatter tre firmaer](media/IntercompanyPlanning2.png)
