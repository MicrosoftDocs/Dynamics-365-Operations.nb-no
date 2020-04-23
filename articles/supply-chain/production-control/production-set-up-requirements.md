---
title: Krav til produksjonsoppsett
description: Denne artikkelen inneholder informasjon om krav til oppsett før du kan arbeide med produksjonskontroll.
author: johanhoffmann
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdParameters, RouteOpr, RouteOprTable, WorkCalendarTable, WorkTimeTable, WrkCtrTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 55561
ms.assetid: 1953059f-478d-4706-b461-25b89ace5fc3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 55820d7376750c210d2b7f214f705ffcb222c6cd
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/02/2020
ms.locfileid: "3212509"
---
# <a name="production-setup-requirements"></a><span data-ttu-id="72dea-103">Krav til produksjonsoppsett</span><span class="sxs-lookup"><span data-stu-id="72dea-103">Production setup requirements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="72dea-104">Denne artikkelen inneholder informasjon om krav til oppsett før du kan arbeide med produksjonskontroll.</span><span class="sxs-lookup"><span data-stu-id="72dea-104">This article provides information about setup requirements before you can work with Production control.</span></span> 

<span data-ttu-id="72dea-105">Produksjonskontroll er integrert med funksjonene i andre moduler.</span><span class="sxs-lookup"><span data-stu-id="72dea-105">Production control is integrated with features in other modules.</span></span> <span data-ttu-id="72dea-106">Denne egenskapen gjør det mulig å endre produksjonsordrer samtidig som de oppdateres automatisk i alle andre tilknyttede prosesser og beregninger i systemet.</span><span class="sxs-lookup"><span data-stu-id="72dea-106">This interconnectivity lets you change production orders and make sure that they are automatically updated in all other related processes and calculations in the system.</span></span> <span data-ttu-id="72dea-107">Følgende oppsettprosesser er ført opp i rekkefølgen de bør fullføres i.</span><span class="sxs-lookup"><span data-stu-id="72dea-107">The following setup processes are listed in the order that you should complete them in.</span></span>

## <a name="required-baseline-setup-in-other-modules"></a><span data-ttu-id="72dea-108">Påkrevd basislinjekonfigurasjon i andre moduler</span><span class="sxs-lookup"><span data-stu-id="72dea-108">Required baseline setup in other modules</span></span>
<span data-ttu-id="72dea-109">Før du kan arbeide med Produksjonskontroll må du konfigurere informasjon i andre moduler.</span><span class="sxs-lookup"><span data-stu-id="72dea-109">Information in other modules must be set up before you can work with Production control.</span></span> <span data-ttu-id="72dea-110">Dette oppsettet omfatter følgende oppgaver:</span><span class="sxs-lookup"><span data-stu-id="72dea-110">This setup includes the following tasks:</span></span>

-   <span data-ttu-id="72dea-111">Konfigurer generell firmainformasjon.</span><span class="sxs-lookup"><span data-stu-id="72dea-111">Set up general company information.</span></span>
-   <span data-ttu-id="72dea-112">Konfigurer økonomi.</span><span class="sxs-lookup"><span data-stu-id="72dea-112">Set up the general ledger.</span></span>
-   <span data-ttu-id="72dea-113">Definer varegrupper.</span><span class="sxs-lookup"><span data-stu-id="72dea-113">Define item groups.</span></span>
-   <span data-ttu-id="72dea-114">Konfigurer finanskontoer for varegrupper.</span><span class="sxs-lookup"><span data-stu-id="72dea-114">Set up ledger accounts for item groups.</span></span>
-   <span data-ttu-id="72dea-115">Konfigurer lagervaretabellen i Lagerstyring.</span><span class="sxs-lookup"><span data-stu-id="72dea-115">Set up the inventory item table in Inventory management.</span></span>
-   <span data-ttu-id="72dea-116">Opprett stykklister og stykklisteversjoner i Lagerstyring.</span><span class="sxs-lookup"><span data-stu-id="72dea-116">Create bills of materials (BOMs) and BOM versions in Inventory management.</span></span>

## <a name="required-calendar-and-resource-setup"></a><span data-ttu-id="72dea-117">Påkrevd konfigurasjon av kalender og ressurs</span><span class="sxs-lookup"><span data-stu-id="72dea-117">Required calendar and resource setup</span></span>
<span data-ttu-id="72dea-118">Før du tar i bruk Produksjonskontroll må du åpne Organisasjonsstyring og opprette og definere kalender- og operasjonsressurser i følgende rekkefølge:</span><span class="sxs-lookup"><span data-stu-id="72dea-118">Before you use Production control, open Organization administration, and create and define the calendar and operations resources in the following order:</span></span>

1.  <span data-ttu-id="72dea-119">**Driftstidsmaler** – Konfigurer driftstidsmaler for å definere hvilke tider som er tilgjengelige for produksjonsplanlegging.</span><span class="sxs-lookup"><span data-stu-id="72dea-119">**Working time templates** – Set up working time templates to define the times that are available for production scheduling.</span></span>
2.  <span data-ttu-id="72dea-120">**Kalendere** – Konfigurer driftstidskalendere for å definere hvilke dager i året som er tilgjengelige for produksjonsplanlegging.</span><span class="sxs-lookup"><span data-stu-id="72dea-120">**Calendars** – Set up working time calendars to define the days of the year that are available for production scheduling.</span></span>
3.  <span data-ttu-id="72dea-121">**Ressursgrupper** – Konfigurer ressursgrupper for å gruppere operasjonsressurser slik at du kan få en oversikt over all ledig kapasitet når du kjører planlegging.</span><span class="sxs-lookup"><span data-stu-id="72dea-121">**Resource groups** – Set up resource groups to group the operations resources, so that you can get an overview of any free capacity when you run scheduling.</span></span> <span data-ttu-id="72dea-122">Du trenger ikke definere ressursgrupper før du setter opp operasjonsressurser.</span><span class="sxs-lookup"><span data-stu-id="72dea-122">You don't have to set up resource groups before you set up operations resources.</span></span> <span data-ttu-id="72dea-123">Vi anbefaler at du forstår hvordan du vil gruppere ressurser når du konfigurerer Produksjonskontroll.</span><span class="sxs-lookup"><span data-stu-id="72dea-123">However, we recommend that you understand how to group resources when you set up Production control.</span></span>
4.  <span data-ttu-id="72dea-124">**Ressurser** – Konfigurer operasjonsressurser for å definere ressursene som brukes for å fullføre produksjonsprosessen og planlegge kapasiteten.</span><span class="sxs-lookup"><span data-stu-id="72dea-124">**Resources** – Set up operations resources to define the resources that are used to complete the production process and plan for capacity.</span></span>

## <a name="required-production-parameters-setup"></a><span data-ttu-id="72dea-125">Påkrevd konfigurasjon av produksjonsparametere</span><span class="sxs-lookup"><span data-stu-id="72dea-125">Required production parameters setup</span></span>
<span data-ttu-id="72dea-126">**Parametere for produksjonskontroll** – Konfigurer grunnleggende produksjonsparametere for å definere hvordan systemet håndterer og behandler produksjonsordrer.</span><span class="sxs-lookup"><span data-stu-id="72dea-126">**Production control parameters** – Set up basic production parameters to define how the system handles and processes production orders.</span></span> <span data-ttu-id="72dea-127">Definer hvordan produksjonsordrer skal opprettes, estimeres, planlegges og forbrukes.</span><span class="sxs-lookup"><span data-stu-id="72dea-127">Define how production orders are created, estimated, scheduled, and consumed.</span></span> <span data-ttu-id="72dea-128">Du kan også velge hvilken type tilbakemeldinger du vil ha, og hvordan kostnadsregnskapet skal utføres.</span><span class="sxs-lookup"><span data-stu-id="72dea-128">You can also select what kind of feedback you want and how cost accounting is done.</span></span>

## <a name="required-journal-name-identification"></a><span data-ttu-id="72dea-129">Påkrevd identifikasjon av journalnavn</span><span class="sxs-lookup"><span data-stu-id="72dea-129">Required journal name identification</span></span>
<span data-ttu-id="72dea-130">**Produksjonsjournalnavn** – Angi produksjonsjournalnavn som brukes til å registrere og postere transaksjoner.</span><span class="sxs-lookup"><span data-stu-id="72dea-130">**Production journal names** – Specify the production journal names that are used to record and post transactions.</span></span>

## <a name="setup-if-you-use-operations"></a><span data-ttu-id="72dea-131">Hvis du bruker operasjoner</span><span class="sxs-lookup"><span data-stu-id="72dea-131">Setup if you use operations</span></span>
<span data-ttu-id="72dea-132">Operasjoner viser til de bestemte aktivitetene som fullføres for å produsere det ferdige produktet.</span><span class="sxs-lookup"><span data-stu-id="72dea-132">Operations represent the specific activities that are completed to produce the finished product.</span></span> <span data-ttu-id="72dea-133">**Merk:** Du må vite hvilke typer aktiviteter som kreves for å produsere varen, og rekkefølgen og prioritetene for aktivitetene.</span><span class="sxs-lookup"><span data-stu-id="72dea-133">**Note:** You must know the types of activities that are required in order to produce your item, and the order and priorities of those activities.</span></span> <span data-ttu-id="72dea-134">Du må også vite hvilke ressurser som er involvert, og hvor mange.</span><span class="sxs-lookup"><span data-stu-id="72dea-134">You must also know which resources are involved, and how many.</span></span>

1.  <span data-ttu-id="72dea-135">**Operasjoner** – Konfigurer operasjoner som skal representere oppgavene som må fullføres for å produsere det ferdige produktet.</span><span class="sxs-lookup"><span data-stu-id="72dea-135">**Operations** – Set up operations to represent the tasks that must be completed to produce the finished item.</span></span>
2.  <span data-ttu-id="72dea-136">**Relasjoner** – Konfigurer operasjonsrelasjoner for å fastsette detaljerte egenskaper.</span><span class="sxs-lookup"><span data-stu-id="72dea-136">**Relations** – Set up operation relations to establish detailed properties.</span></span> <span data-ttu-id="72dea-137">For å definere operasjonsrelasjoner klikk **Relasjoner** på siden **Operasjoner**.</span><span class="sxs-lookup"><span data-stu-id="72dea-137">To define operation relations, click **Relations** on the **Operations** page.</span></span>

## <a name="setup-if-you-use-routes"></a><span data-ttu-id="72dea-138">Hvis du bruker ruter</span><span class="sxs-lookup"><span data-stu-id="72dea-138">Setup if you use routes</span></span>
<span data-ttu-id="72dea-139">Hvis du arbeider med ruter, må du definere operasjoner for hver produksjonsrute du definerer.</span><span class="sxs-lookup"><span data-stu-id="72dea-139">If you're working with routes, operations must be defined for every production route that you set up.</span></span> <span data-ttu-id="72dea-140">Ruten representerer banen varen tar fra operasjon til operasjon, fra begynnelsen til slutten av produksjonsprosessen.</span><span class="sxs-lookup"><span data-stu-id="72dea-140">The route represents the path that the item takes from operation to operation, from the start of the production process to the end.</span></span>

1.  <span data-ttu-id="72dea-141">**Kostnadskategorier** – Konfigurer kostnadskategorier for å definere kostnadene per time for bestemte prosesser og oppstillingstider.</span><span class="sxs-lookup"><span data-stu-id="72dea-141">**Cost categories** – Set up cost categories to define the cost per hour of specified processes and setup times.</span></span>
2.  <span data-ttu-id="72dea-142">**Kostgrupper** – Konfigurer kostgrupper for å opprette og vedlikeholde forskjellige typer etterkalkulering.</span><span class="sxs-lookup"><span data-stu-id="72dea-142">**Cost groups** – Set up cost groups to create and maintain different types of costing.</span></span>
3.  <span data-ttu-id="72dea-143">**Rutegrupper** – Konfigurer rutegrupper for å definere parametere som er relatert til grupper av ruter.</span><span class="sxs-lookup"><span data-stu-id="72dea-143">**Route groups** – Set up route groups to define parameters that are related to groups of routes.</span></span> <span data-ttu-id="72dea-144">Du må konfigurere rutegruppene før du oppretter produksjonsruter.</span><span class="sxs-lookup"><span data-stu-id="72dea-144">You must set up route groups before you can create production routes.</span></span>
4.  <span data-ttu-id="72dea-145">**Ruter** – Konfigurer produksjonsruter, og definer standardinnstillinger for å styre planlegging, etterkalkulering og prissetting av ruteoperasjoner samt rapport om fremdrift.</span><span class="sxs-lookup"><span data-stu-id="72dea-145">**Routes** – Set up production routes, and define default settings to control scheduling, costing, and pricing of route operations, and to control progress reporting.</span></span>
5.  <span data-ttu-id="72dea-146">**Ruter** – Konfigurer ruteversjoner for å aktivere varevariasjoner i produksjonen.</span><span class="sxs-lookup"><span data-stu-id="72dea-146">**Routes** – Set up route versions to enable item variations in production.</span></span>

## <a name="optional-advanced-settings"></a><span data-ttu-id="72dea-147">Valgfrie, avanserte innstillinger</span><span class="sxs-lookup"><span data-stu-id="72dea-147">Optional advanced settings</span></span>
1.  <span data-ttu-id="72dea-148">**Produksjonsgrupper** – Konfigurer produksjonsgrupper for å fastsette forhold mellom produksjonsordren og finanskontoene.</span><span class="sxs-lookup"><span data-stu-id="72dea-148">**Production groups** – Set up production groups to establish relationships between the production order and ledger accounts.</span></span> <span data-ttu-id="72dea-149">Finanskontoene brukes til å postere eller gruppere ordrene for rapportering.</span><span class="sxs-lookup"><span data-stu-id="72dea-149">The ledger accounts are used to post or group orders for reporting.</span></span>
2.  <span data-ttu-id="72dea-150">**Produksjonspuljer** – Opprett produksjonspuljer for å gruppere produksjonsordrer slik at du kan behandle produksjonsordrer det haster med, eller for å slette og postere grupper av ordrer.</span><span class="sxs-lookup"><span data-stu-id="72dea-150">**Production pools** – Create production pools to group production orders so that you can process urgent production orders, or delete and post groups of orders.</span></span>
3.  <span data-ttu-id="72dea-151">**Egenskaper** – Definer egenskaper for å opprette spesielle attributter som du kan tilordne til ressursene for å kontrollere rekkefølgen på produksjoner.</span><span class="sxs-lookup"><span data-stu-id="72dea-151">**Properties** – Define properties to create special attributes that you can assign to your resources to control the order of productions.</span></span> <span data-ttu-id="72dea-152">Disse attributtene er knyttet til driftstidsmalen.</span><span class="sxs-lookup"><span data-stu-id="72dea-152">These attributes are connected to the working time template.</span></span>




