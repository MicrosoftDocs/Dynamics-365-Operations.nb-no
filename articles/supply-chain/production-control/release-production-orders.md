---
title: Frigi produksjonsordrer
description: En frigitt produksjonsordre er en ordre som har blitt autorisert for produksjon. Begrepet frigitt brukes til å beskrive en tilstand i livssyklusen til produksjonsordren, der produksjonsordren er tilgjengelig for utføring på produksjonsgulvet og for lagerprosesser.
author: johanhoffmann
manager: tfehr
ms.date: 03/02/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdParmRelease
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2414
ms.assetid: 50c2257b-2924-44f5-b7c1-11f498092053
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4ee20983209b9900037a46d56b6213d47bf852e4
ms.sourcegitcommit: 105f65468b45799761c26e5d0ad9df4ff162c38d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/04/2021
ms.locfileid: "5487705"
---
# <a name="release-production-orders"></a><span data-ttu-id="93041-104">Frigi produksjonsordrer</span><span class="sxs-lookup"><span data-stu-id="93041-104">Release production orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="93041-105">En frigitt produksjonsordre er en ordre som har blitt autorisert for produksjon.</span><span class="sxs-lookup"><span data-stu-id="93041-105">A released production order is an order that has been authorized for production.</span></span> <span data-ttu-id="93041-106">Begrepet frigitt brukes til å beskrive en tilstand i livssyklusen til produksjonsordren, der produksjonsordren er tilgjengelig for utføring på produksjonsgulvet og for lagerprosesser.</span><span class="sxs-lookup"><span data-stu-id="93041-106">The term Released is used to describe a state in the production order life cycle, where the production order is available for execution on the production shop floor and for warehouse processes.</span></span>

## <a name="characteristics-of-the-released-state"></a><span data-ttu-id="93041-107">Egenskapene for tilstanden Frigitt</span><span class="sxs-lookup"><span data-stu-id="93041-107">Characteristics of the Released state</span></span>

<span data-ttu-id="93041-108">**Frigitt** er én tilstand i livssyklusen til produksjonsordren.</span><span class="sxs-lookup"><span data-stu-id="93041-108">The **Released** state is one state in the production order life cycle.</span></span> <span data-ttu-id="93041-109">Produksjonsordrer som har tilstanden **Frigitt**, er tilgjengelige for kjøring i produksjons- og lagerprosesser.</span><span class="sxs-lookup"><span data-stu-id="93041-109">Production orders that are in the **Released** state are available for execution on the production shop floor and for warehouse processes.</span></span> <span data-ttu-id="93041-110">**Frigitt**-tilstanden har følgende egenskaper:</span><span class="sxs-lookup"><span data-stu-id="93041-110">The **Released** state has the following characteristics:</span></span>

- <span data-ttu-id="93041-111">En produksjonsordre kan endres til tilstanden **Frigitt** fra produksjonsordren eller ved hjelp av en partiprosess.</span><span class="sxs-lookup"><span data-stu-id="93041-111">A production order can be changed to the **Released** state either from the production order or by using a batch process.</span></span> <span data-ttu-id="93041-112">Produksjonsordren kan også oppdateres automatisk fra planlagte produksjonsordrer som er autorisert ved hjelp av feltet **Autorisasjonshorisont** på **Hovedplan**-siden.</span><span class="sxs-lookup"><span data-stu-id="93041-112">The production order can also be updated automatically from planned production orders that are firmed by using the **Firming time fence** field on the **Master plan** page.</span></span>
- <span data-ttu-id="93041-113">Tilstanden **Frigitt** er tegnet for shop floor-operatørene på at de kan starte kjøring av produksjonsjobber i shop floor.</span><span class="sxs-lookup"><span data-stu-id="93041-113">The **Released** state is the signal for the shop floor operators (operators) to start executing the production jobs on the shop floor.</span></span>
- <span data-ttu-id="93041-114">Produksjonspapirer, for eksempel rutekort, rutejobber og jobbkort, gir informasjon om produksjonsjobbene og kan utstedes.</span><span class="sxs-lookup"><span data-stu-id="93041-114">Production papers, such as route cards, route jobs, and jobs cards provide information about production jobs and can be issued.</span></span>
- <span data-ttu-id="93041-115">For materialer som er fysisk reservert, genereres lagerarbeid for å plukke materialer til produksjonsordren.</span><span class="sxs-lookup"><span data-stu-id="93041-115">For materials that are physically reserved, warehouse work is generated to pick materials for the production order.</span></span>

## <a name="releasing-jobs-to-the-shop-floor"></a><span data-ttu-id="93041-116">Frigi jobber til shop floor</span><span class="sxs-lookup"><span data-stu-id="93041-116">Releasing jobs to the shop floor</span></span>

<span data-ttu-id="93041-117">Når en produksjonsordre er frigitt, blir produksjonsjobber som er knyttet til ordren, synlige og klar for registrering.</span><span class="sxs-lookup"><span data-stu-id="93041-117">After a production order is released, production jobs that are related to the order are visible and ready for registration.</span></span> <span data-ttu-id="93041-118">Operatørene kan utføre jobbregistreringer, for eksempel Start, Stopp og Fullføring, på siden **Jobbkortterminal** eller **Jobbkortenhet**.</span><span class="sxs-lookup"><span data-stu-id="93041-118">The operators can make job registrations, such as Start, Stop, and Completion, on either the **Job card terminal** page or the **Job card device** page.</span></span> <span data-ttu-id="93041-119">Registrert tid og antall overføres automatisk fra registreringsidene til produksjonsjournaler for å holde oversikt over forbruk av tid og antall.</span><span class="sxs-lookup"><span data-stu-id="93041-119">The registered time and quantity are automatically transferred from the registration pages to production journals to keep track of the consumed time and quantity.</span></span>

## <a name="route-cards"></a><span data-ttu-id="93041-120">Rutekort</span><span class="sxs-lookup"><span data-stu-id="93041-120">Route cards</span></span>

<span data-ttu-id="93041-121">Et rutekort gir en oversikt over informasjon som kommer fra rute- og operasjonsoppsett og fra operasjons- og jobbplanleggingsmetoder.</span><span class="sxs-lookup"><span data-stu-id="93041-121">A route card provides an overview of information that comes from route and operation setups, and from operation and job scheduling methods.</span></span>

## <a name="route-jobs"></a><span data-ttu-id="93041-122">Jobber for ruten</span><span class="sxs-lookup"><span data-stu-id="93041-122">Route jobs</span></span>

<span data-ttu-id="93041-123">En rutejobb gir detaljert informasjon om hver jobb i en operasjon, og inkluderer tider for oppsett, prosess, kø og transport.</span><span class="sxs-lookup"><span data-stu-id="93041-123">A route job lists each job of an operation in detail, and includes setup, process, queue, and transportation times.</span></span> <span data-ttu-id="93041-124">En maleoperasjon krever for eksempel individuelle jobber som oppsettstid, kjøretid for maleprosessen og køtid for tørking.</span><span class="sxs-lookup"><span data-stu-id="93041-124">For example, an operation such as painting might require individual jobs, such as setup time, run time for the painting process, and queue time for drying.</span></span>

## <a name="job-cards"></a><span data-ttu-id="93041-125">Jobbkort</span><span class="sxs-lookup"><span data-stu-id="93041-125">Job cards</span></span>

<span data-ttu-id="93041-126">Et jobbkort viser de individuelle jobbnumrene til en bestemt operasjon.</span><span class="sxs-lookup"><span data-stu-id="93041-126">A job card lists the individual job numbers of a particular operation.</span></span> <span data-ttu-id="93041-127">Én jobb vises på hver side.</span><span class="sxs-lookup"><span data-stu-id="93041-127">One job appears on each page.</span></span> <span data-ttu-id="93041-128">Jobbene på et jobbkort, og estimert tid, kommer fra informasjonen om ruten og operasjonsoppsettet.</span><span class="sxs-lookup"><span data-stu-id="93041-128">The jobs that are included on a job card, and their estimated times, come from the route and operation setup information.</span></span> <span data-ttu-id="93041-129">Du kan åpne siden **Produksjonsjournallinjer**, **jobbkort** fra et jobbkort.</span><span class="sxs-lookup"><span data-stu-id="93041-129">From a job card, you can open the **Production journal lines**, **job card** page.</span></span> <span data-ttu-id="93041-130">De som driver operasjonsressurser, kan gi tilbakemelding om produksjonsprosessen.</span><span class="sxs-lookup"><span data-stu-id="93041-130">People who run operations resources can provide feedback about the production process.</span></span> <span data-ttu-id="93041-131">Det er felt der du kan angi forbruksstatistikk og informasjon som antall feil.</span><span class="sxs-lookup"><span data-stu-id="93041-131">There are fields where you can enter consumption statistics and information such as the error quantity.</span></span>

## <a name="warehouse-work-for-raw-material-picking"></a><span data-ttu-id="93041-132">Lagerarbeid for råvareplukking</span><span class="sxs-lookup"><span data-stu-id="93041-132">Warehouse work for raw material picking</span></span>

<span data-ttu-id="93041-133">Arbeid for råvareplukking genereres under frigivelsen.</span><span class="sxs-lookup"><span data-stu-id="93041-133">Work for raw material picking is generated during release.</span></span> <span data-ttu-id="93041-134">Arbeid genereres bare for materialmengden som er fysisk reservert for produksjonsordren før ordren ble frigitt.</span><span class="sxs-lookup"><span data-stu-id="93041-134">Work is generated only for the quantity of materials that was physically reserved for the production order before the order was released.</span></span> <span data-ttu-id="93041-135">Følgende oppsett er nødvendig for å generere lagerarbeid for plukking av råvarer:</span><span class="sxs-lookup"><span data-stu-id="93041-135">The following setup is required to generate warehouse work for raw material picking:</span></span>

- <span data-ttu-id="93041-136">Et lokasjonsdirektiv for råvareplukking som bestemmer lagerlokasjonen materialene skal plukkes fra</span><span class="sxs-lookup"><span data-stu-id="93041-136">A location directive for raw materials picking that determines which warehouse location to pick the materials in</span></span>
- <span data-ttu-id="93041-137">En bølgemal for råmaterialer, der policyer konfigureres for utførelse av lagerarbeid</span><span class="sxs-lookup"><span data-stu-id="93041-137">A wave template for raw materials, where policies for the execution of warehouse work are configured</span></span>
- <span data-ttu-id="93041-138">Et produksjonsinnleveringssted som bestemmer hvor materialene plasseres</span><span class="sxs-lookup"><span data-stu-id="93041-138">A production input location that determines where materials are put</span></span>

<span data-ttu-id="93041-139">Ved bruk av nummerskiltkontrollerte lokasjoner kan du velge om det bestilte antallet eller hele antallet som er tilgjengelig for varen, skal plukkes under behandling av råvareplukkingsarbeidet.</span><span class="sxs-lookup"><span data-stu-id="93041-139">When using license plate controlled locations, you can choose whether the ordered quantity or the full quantity available for the item should be picked while processing the raw material picking work.</span></span> <span data-ttu-id="93041-140">Slik konfigurerer du dette alternativet:</span><span class="sxs-lookup"><span data-stu-id="93041-140">To set this option:</span></span>

1. <span data-ttu-id="93041-141">Gå til **Behandling av produktinformasjon \> Produkter \> Frigitte produkter** og åpne den relevante varen.</span><span class="sxs-lookup"><span data-stu-id="93041-141">Go to **Product information management \> Products \> Released products** and open the relevant item.</span></span>
1. <span data-ttu-id="93041-142">Vis hurtigfanen **Lager**.</span><span class="sxs-lookup"><span data-stu-id="93041-142">Expand the **Warehouse** FastTab.</span></span>
1. <span data-ttu-id="93041-143">Velg ett av følgende alternativer for feltet **Materialplukking på nummerskiltplasseringer**:</span><span class="sxs-lookup"><span data-stu-id="93041-143">Select one of the following options for the  **Material picking in license plate locations** field:</span></span>
    - <span data-ttu-id="93041-144">*Ordreplukking*: Bare det bestilte antallet skal plukkes.</span><span class="sxs-lookup"><span data-stu-id="93041-144">*Order picking*: Only the ordered quantity should be picked.</span></span>
    - <span data-ttu-id="93041-145">*Oppsamling*: Når det er mulig skal hele antallet som er tilgjengelig for nummerskiltet, plukkes.</span><span class="sxs-lookup"><span data-stu-id="93041-145">*Staging*: Whenever possible, the full quantity available at the license plate should be picked.</span></span> <span data-ttu-id="93041-146">Hvis en arbeider skal kunne plukke hele nummerskiltantallet, må nummerskiltet inneholde et blandet utvalg varer og må ikke ha kombinerte dimensjoner.</span><span class="sxs-lookup"><span data-stu-id="93041-146">For a worker to be able to pick the full license plate quantity, the license plate must not contain mixed items and must not have mixed dimensions.</span></span> <span data-ttu-id="93041-147">Hvis nummerskiltet inneholder kombinerte dimensjoner eller varer, fortsetter plukkingen som om den var satt til *Ordreplukking*.</span><span class="sxs-lookup"><span data-stu-id="93041-147">If the license plate contains mixed dimensions or items, the pick will proceed as if it were set to *Order picking*.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]