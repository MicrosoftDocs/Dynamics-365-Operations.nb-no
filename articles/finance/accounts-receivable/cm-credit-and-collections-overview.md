---
title: Oversikt over kreditt og innkreving
description: Dette emnet gir en oversikt over funksjonen for kreditt og innkreving.
author: mikefalkner
manager: AnnBe
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 2fdfe05483d577819d64bdf7a4ebfe5d37cd414c
ms.sourcegitcommit: 6a70f9ac296158edd065d52a12703b3ce85ce5ee
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/03/2020
ms.locfileid: "3015332"
---
# <a name="credit-and-collections-overview"></a><span data-ttu-id="323fc-103">Oversikt over kreditt og innkreving</span><span class="sxs-lookup"><span data-stu-id="323fc-103">Credit and collections overview</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="323fc-104">Du kan administrere kredittgrenser for kundene og utføre innkrevingsaktiviteter når det blir nødvendig.</span><span class="sxs-lookup"><span data-stu-id="323fc-104">You can manage credit limits for your customers and perform collection activities when they become necessary.</span></span>

## <a name="credit-management"></a><span data-ttu-id="323fc-105">Kredittbehandling</span><span class="sxs-lookup"><span data-stu-id="323fc-105">Credit management</span></span>

<span data-ttu-id="323fc-106">Ved hjelp av kundekredittstyring kan du håndtere kredittgrenser og kontrollere flyten av salgsordrer gjennom posteringsprosessen, basert på kredittregler du oppretter.</span><span class="sxs-lookup"><span data-stu-id="323fc-106">Customer credit management lets you manage credit limits and control the flow of sales orders through the posting process, based on credit rules that you create.</span></span>

<span data-ttu-id="323fc-107">Kredittbehandlingsprosessen kan inneholde hvilke som helst av følgende trinn:</span><span class="sxs-lookup"><span data-stu-id="323fc-107">The credit management process can include any of the following steps:</span></span>

- <span data-ttu-id="323fc-108">Oppdater kredittattributter for kunder for å gi mer informasjon om deres kredittverdighet.</span><span class="sxs-lookup"><span data-stu-id="323fc-108">Update credit attributes for customers to provide additional information about their credit worthiness.</span></span>
- <span data-ttu-id="323fc-109">Opprett kredittgrenser for kunder ved hjelp av kredittgrensejusteringer.</span><span class="sxs-lookup"><span data-stu-id="323fc-109">Create credit limits for customers by using credit limit adjustments.</span></span>
- <span data-ttu-id="323fc-110">Opprett midlertidige kredittgrenser for kunder ved hjelp av kredittgrensejusteringer.</span><span class="sxs-lookup"><span data-stu-id="323fc-110">Create temporary credit limits for customers by using credit limit adjustments.</span></span> <span data-ttu-id="323fc-111">På denne måten kan du midlertidig øke eller redusere kundekredittgrenser, basert på forretningsbehov.</span><span class="sxs-lookup"><span data-stu-id="323fc-111">In this way, you can temporarily increase or decrease customer credit limits, based on business requirements.</span></span>
- <span data-ttu-id="323fc-112">Legg til informasjon som kan påvirke kredittgrensen, for eksempel informasjon om forsikring og garantier.</span><span class="sxs-lookup"><span data-stu-id="323fc-112">Add information that can affect the credit limit, such as information about insurance and guarantees.</span></span>
- <span data-ttu-id="323fc-113">Opprett kundekredittgrupper som kobler kunder sammen, slik at de deler én enkelt kredittgrense.</span><span class="sxs-lookup"><span data-stu-id="323fc-113">Create customer credit groups that link customers together so that they share a single credit limit.</span></span>
- <span data-ttu-id="323fc-114">Tilordne risikopoeng til kunder, og bruk deretter poengene til automatisk å generere kredittgrenser for disse kundene via kredittgrensejusteringer.</span><span class="sxs-lookup"><span data-stu-id="323fc-114">Assign risk scores to customers, and then use the scores to automatically generate credit limits for those customers through credit limit adjustments.</span></span>
- <span data-ttu-id="323fc-115">Opprett blokkeringsregler som setter en ordre på vent under én eller flere posteringsprosesser, basert på faktorer som risiko, betalingsbetingelser, kredittgrenser, forfalte beløp og prosentandelen av kredittgrensen som er brukt.</span><span class="sxs-lookup"><span data-stu-id="323fc-115">Create blocking rules that put an order on hold during one or more posting processes, based on factors such as risk, payment terms, credit limits, overdue amounts, and the percentage of the credit limit that has been used.</span></span>
- <span data-ttu-id="323fc-116">Administrer en liste over salgsordrer som er på vent, gå gjennom årsakene til sperringen, og begrens problemer.</span><span class="sxs-lookup"><span data-stu-id="323fc-116">Manage a list of sales orders that are on hold, review the reasons for the hold, and mitigate issues.</span></span>
- <span data-ttu-id="323fc-117">Frigi salgsordrer slik at de fortsetter gjennom posteringsprosessen.</span><span class="sxs-lookup"><span data-stu-id="323fc-117">Release sales orders so that they continue through the posting process.</span></span>
- <span data-ttu-id="323fc-118">Definer en arbeidsflyt for å administrere godkjenning av kredittgrenseendringer og salgsordrefrigivelser.</span><span class="sxs-lookup"><span data-stu-id="323fc-118">Set up a workflow to manage the approval of credit limit changes and sales order releases.</span></span>

## <a name="collections-management"></a><span data-ttu-id="323fc-119">Innkrevingsbehandling</span><span class="sxs-lookup"><span data-stu-id="323fc-119">Collections management</span></span>

<span data-ttu-id="323fc-120">Siden **Innkrevinger** gir en sentral visning av der informasjon om kundeinnkrevinger håndteres.</span><span class="sxs-lookup"><span data-stu-id="323fc-120">The **Collections** page provides a centralized view where accounts receivable collections information is managed.</span></span> <span data-ttu-id="323fc-121">Ledere for innkreving kan bruke denne sentrale visningen til å administrere innkreving.</span><span class="sxs-lookup"><span data-stu-id="323fc-121">Collections managers can use this centralized view to manage collections.</span></span> <span data-ttu-id="323fc-122">Innkrevingsagenter kan begynne innkrevingsprosessen enten fra kundelister som genereres ved hjelp av forhåndsdefinerte innkrevingskriterier, eller fra **Kunder**-siden.</span><span class="sxs-lookup"><span data-stu-id="323fc-122">Collections agents can begin the collections process either from customer lists that are generated by using predefined collection criteria or from the **Customers** page.</span></span>

<span data-ttu-id="323fc-123">Før du begynner å sette opp eller arbeide med samlinger, bør du forstår disse begrepene:</span><span class="sxs-lookup"><span data-stu-id="323fc-123">Before you start to set up or work with collections, you should understand the following concepts:</span></span>

- <span data-ttu-id="323fc-124">Øyeblikksbilder av aldersfordeling for kunder inneholder informasjon på et bestemt tidspunkt.</span><span class="sxs-lookup"><span data-stu-id="323fc-124">Customer aging snapshots contain aged balance information at a specific point in time.</span></span>
- <span data-ttu-id="323fc-125">Innkrevingskundepuljer hjelper med å organisere arbeidet.</span><span class="sxs-lookup"><span data-stu-id="323fc-125">Collections customer pools help you organize your work.</span></span>
- <span data-ttu-id="323fc-126">Innkrevingsagenter kan ha sine egne kundepuljer.</span><span class="sxs-lookup"><span data-stu-id="323fc-126">Collections agents can have their own customer pools.</span></span>
- <span data-ttu-id="323fc-127">Listesider organiserer innkrevingskunder, aktiviteter og saker.</span><span class="sxs-lookup"><span data-stu-id="323fc-127">List pages organize collections customers, activities, and cases.</span></span>
- <span data-ttu-id="323fc-128">All innkrevingsinformasjon for en kunde er på én side, og du kan foreta en handling fra denne siden.</span><span class="sxs-lookup"><span data-stu-id="323fc-128">All collections information for a customer is on one page, and you can take action from that page.</span></span>
- <span data-ttu-id="323fc-129">Renter og gebyrer kan frafalles, gjenopptas eller reverseres i ett trinn.</span><span class="sxs-lookup"><span data-stu-id="323fc-129">Interest and fees can be waived, reinstated, or reversed in one step.</span></span>
- <span data-ttu-id="323fc-130">Avskrivningstransaksjoner kan opprettes i ett trinn.</span><span class="sxs-lookup"><span data-stu-id="323fc-130">Write-off transactions can be created in one step.</span></span>
- <span data-ttu-id="323fc-131">Betaling uten dekning kan behandles i ett trinn.</span><span class="sxs-lookup"><span data-stu-id="323fc-131">Not sufficient funds (NSF) payments can be processed in one step.</span></span>

<span data-ttu-id="323fc-132">Du finner beskrivelser av disse konseptene under [Nøkkelbegreper for innkrevingsbehandling](./cm-collections-concepts.md).</span><span class="sxs-lookup"><span data-stu-id="323fc-132">For descriptions of these concepts, see [Collections management key concepts](./cm-collections-concepts.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="323fc-133">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="323fc-133">Additional resources</span></span>

[<span data-ttu-id="323fc-134">Oppsett av parametere for kundekredittbehandling</span><span class="sxs-lookup"><span data-stu-id="323fc-134">Customer credit management parameters setup</span></span>](./cm-credit-mgmt-setup.md)

[<span data-ttu-id="323fc-135">Informasjon om oppsett av kundekredittbehandling</span><span class="sxs-lookup"><span data-stu-id="323fc-135">Customer credit management setup information</span></span>](./cm-setup-information.md)

[<span data-ttu-id="323fc-136">Legge til kredittbehandlingsinformasjon for en kunde</span><span class="sxs-lookup"><span data-stu-id="323fc-136">Add credit management information for a customer</span></span>](./cm-add-credit-mgmt-information-customer.md)

[<span data-ttu-id="323fc-137">Kundekredittgrupper</span><span class="sxs-lookup"><span data-stu-id="323fc-137">Customer credit groups</span></span>](./cm-customer-credit-groups.md)

[<span data-ttu-id="323fc-138">Kundekredittgrensejusteringer</span><span class="sxs-lookup"><span data-stu-id="323fc-138">Customer credit limit adjustments</span></span>](./cm-credit-limit-adjustments.md)

[<span data-ttu-id="323fc-139">Kredittsperrer for salgsordrer</span><span class="sxs-lookup"><span data-stu-id="323fc-139">Credit holds for sales orders</span></span>](./cm-sales-order-credit-holds.md)

[<span data-ttu-id="323fc-140">Periodiske oppgaver for kundekredittbehandling</span><span class="sxs-lookup"><span data-stu-id="323fc-140">Customer credit management periodic tasks</span></span>](./cm-periodic-tasks.md)