---
title: Posteringsdefinisjoner
description: "Denne artikkelen inneholder informasjon om posteringsdefinisjoner og hvordan du definerer og kobler dem. Når det gjelder støttede posteringstyper og dokumenter, kan du bruke posteringsdefinisjoner i stedet for posteringsprofiler til å klassifisere hovedkontoer og finansdimensjoner i regnskapsoppføringer."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: JournalizingDefinition, JournalizingDefinitionTrans, LedgerParameters
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 15741
ms.assetid: 1495e7e0-2e39-464c-8da9-f55b1ca1c6bb
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: aa80976e539e88af8b157257d043d410ede49e8d
ms.contentlocale: nb-no
ms.lasthandoff: 04/13/2018

---

# <a name="posting-definitions"></a><span data-ttu-id="3276b-104">Posteringsdefinisjoner</span><span class="sxs-lookup"><span data-stu-id="3276b-104">Posting definitions</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="3276b-105">Denne artikkelen inneholder informasjon om posteringsdefinisjoner og hvordan du definerer og kobler dem.</span><span class="sxs-lookup"><span data-stu-id="3276b-105">This article provides information about posting definitions, and how to define and link them.</span></span> <span data-ttu-id="3276b-106">Når det gjelder støttede posteringstyper og dokumenter, kan du bruke posteringsdefinisjoner i stedet for posteringsprofiler til å klassifisere hovedkontoer og finansdimensjoner i regnskapsoppføringer.</span><span class="sxs-lookup"><span data-stu-id="3276b-106">For supported posting types and documents, you can use posting definitions instead of posting profiles to classify main accounts and financial dimensions on accounting entries.</span></span>

<span data-ttu-id="3276b-107">Når det gjelder støttede posteringstyper og dokumenter, kan du bruke posteringsdefinisjoner i stedet for posteringsprofiler til å klassifisere hovedkontoer og finansdimensjoner i regnskapsoppføringer.</span><span class="sxs-lookup"><span data-stu-id="3276b-107">For supported posting types and documents, you can use posting definitions instead of posting profiles to classify main accounts and financial dimensions on accounting entries.</span></span> <span data-ttu-id="3276b-108">Du kan vise de støttede dokumentene og posteringstypene på siden **Definisjoner for transaksjonspostering**.</span><span class="sxs-lookup"><span data-stu-id="3276b-108">You can view the supported documents and posting types on the **Transaction posting definitions** page.</span></span> 

<span data-ttu-id="3276b-109">Hvis du vil begynne å bruke posteringsdefinisjoner, velger du alternativet **Bruk posteringsdefinisjoner** på **Økonomiparametere**-siden.</span><span class="sxs-lookup"><span data-stu-id="3276b-109">To start using posting definitions, select the **Use posting definitions** option on the **General ledger parameters** page.</span></span> <span data-ttu-id="3276b-110">Selv når du bruker posteringsdefinisjoner, må du definere posteringsprofiler for de opprinnelige oppføringene og posteringstyper og dokumenter som ikke støttes.</span><span class="sxs-lookup"><span data-stu-id="3276b-110">Even when you use posting definitions, you must still define posting profiles for the originating entries and non-supported posting types and documents.</span></span> 

<span data-ttu-id="3276b-111">Du må bruke posteringsdefinisjoner for å kunne aktivere disposisjonsregnskap for bestillinger og forhåndsdisposisjonsregnskap for innkjøpsrekvisisjoner.</span><span class="sxs-lookup"><span data-stu-id="3276b-111">You must use posting definitions in order to enable encumbrance accounting for purchase orders and pre-encumbrance accounting for purchase requisitions.</span></span>

## <a name="defining-posting-definitions"></a><span data-ttu-id="3276b-112">Definere posteringsdefinisjoner</span><span class="sxs-lookup"><span data-stu-id="3276b-112">Defining posting definitions</span></span>
<span data-ttu-id="3276b-113">Bruk **Posteringsdefinisjoner**-siden for å angi treffvilkårene og definere oppføringene som skal genereres når det oppstår et treff.</span><span class="sxs-lookup"><span data-stu-id="3276b-113">Use the **Posting definitions** page to specify the match criteria and define the entries that should be generated when a match occurs.</span></span> <span data-ttu-id="3276b-114">Treffvilkårene evalueres for de opprinnelige oppføringene som regnskapsdistribusjoner.</span><span class="sxs-lookup"><span data-stu-id="3276b-114">The match criteria are evaluated for the originating entries as accounting distributions.</span></span> 

<span data-ttu-id="3276b-115">På **Posteringsdefinisjoner**-siden kan du også tilordne prioritetsnumre til oppføringslinjer for å kontrollere rekkefølgen linjene evalueres i.</span><span class="sxs-lookup"><span data-stu-id="3276b-115">On the **Posting definitions** page, you can also assign priority numbers to entry lines to control the order in which the lines are evaluated.</span></span> <span data-ttu-id="3276b-116">Linjene som har det laveste prioritetsnummeret, evalueres først.</span><span class="sxs-lookup"><span data-stu-id="3276b-116">The lines that have the lowest priority number are evaluated first.</span></span> <span data-ttu-id="3276b-117">Et eksempel er at alle linjer som har prioriteten 1, blir evaluert, og deretter linjer som har prioriteten 2 og så videre.</span><span class="sxs-lookup"><span data-stu-id="3276b-117">For example, all lines that have a priority of 1 are evaluated, and then lines that have a priority of 2, and so on.</span></span> <span data-ttu-id="3276b-118">Når et treff blir funnet, ignoreres de andre treffvilkårene.</span><span class="sxs-lookup"><span data-stu-id="3276b-118">When a match is found, the other match criteria are ignored.</span></span> <span data-ttu-id="3276b-119">I tillegg er det bare kriteriene i gruppen som samsvarer med den opprinnelige transaksjonen, som oppretter genererte oppføringer.</span><span class="sxs-lookup"><span data-stu-id="3276b-119">Additionally, only the criteria in the group that match the originating transaction create generated entries.</span></span> 

<span data-ttu-id="3276b-120">Du kan validere posteringsdefinisjonene ved å bruke veiviseren **Test posteringsdefinisjon**.</span><span class="sxs-lookup"><span data-stu-id="3276b-120">You can validate your posting definitions by using the **Test posting definition** wizard.</span></span> <span data-ttu-id="3276b-121">Når du har definert en opprinnelig eksempeloppføring for en posteringsdefinisjon, ser du de genererte oppføringene.</span><span class="sxs-lookup"><span data-stu-id="3276b-121">After you define a sample originating entry for a posting definition, you'll see the generated entries.</span></span> 

<span data-ttu-id="3276b-122">Du kan bruke posteringsdefinisjonsversjoner med gyldighetsdatoer.</span><span class="sxs-lookup"><span data-stu-id="3276b-122">You can use posting definition versions together with effective dates.</span></span> <span data-ttu-id="3276b-123">Du kan for eksempel opprette en fremtidig versjon av en posteringsdefinisjon for å postere til en annen finanskonto i et nytt regnskapsår.</span><span class="sxs-lookup"><span data-stu-id="3276b-123">For example, you can create a future version of a posting definition to post to a different ledger account in a new fiscal year.</span></span> 

<span data-ttu-id="3276b-124">Bruk siden **Definisjoner for transaksjonspostering** til å tilordne posteringsdefinisjoner til transaksjonstyper.</span><span class="sxs-lookup"><span data-stu-id="3276b-124">Use the **Transaction posting definitions** page to assign posting definitions to transaction types.</span></span>

## <a name="linking-posting-definitions"></a><span data-ttu-id="3276b-125">Koble posteringsdefinisjoner</span><span class="sxs-lookup"><span data-stu-id="3276b-125">Linking posting definitions</span></span>
<span data-ttu-id="3276b-126">Du kan koble fra én posteringsdefinisjon til en annen når du oppretter posteringsdefinisjoner.</span><span class="sxs-lookup"><span data-stu-id="3276b-126">You can link from one posting definition to another when you create posting definitions.</span></span> <span data-ttu-id="3276b-127">Kriteriene for definisjonen du koblet til, vurderes deretter i tillegg til kriteriene for den gjeldende posteringsdefinisjonen.</span><span class="sxs-lookup"><span data-stu-id="3276b-127">The criteria for the definition that you linked to are then considered in addition to the criteria for the current posting definition.</span></span> <span data-ttu-id="3276b-128">Denne funksjonen er tidsbesparende fordi du ikke trenger å angi kriterier på nytt i hurtigfanen **Oppføringer** på **Posteringsdefinisjoner**-siden for den gjeldende posteringsdefinisjonen hvis du allerede har angitt disse linjene for en annen definisjon.</span><span class="sxs-lookup"><span data-stu-id="3276b-128">This feature helps save you time, because you don't have to reenter criteria on the **Entries** FastTab on the **Posting definitions** page for the current posting definition if you already entered those lines for another definition.</span></span> 

<span data-ttu-id="3276b-129">Ta med koblinger du kanskje kommer til å bruke, i diagrammer eller tabeller.</span><span class="sxs-lookup"><span data-stu-id="3276b-129">In the diagrams or tables, include any links that you might use.</span></span> <span data-ttu-id="3276b-130">Du kan unngå konflikter med gjeldende posteringsdefinisjon ved å sikre at linjene i enhver posteringsdefinisjon du kobler til, er unik.</span><span class="sxs-lookup"><span data-stu-id="3276b-130">To avoid conflicts with the current posting definition, make sure that the lines in any posting definitions that you link to are unique.</span></span> 

<span data-ttu-id="3276b-131">Følgende begrensninger gjelder når du oppretter koblinger i posteringsdefinisjoner:</span><span class="sxs-lookup"><span data-stu-id="3276b-131">The following restrictions apply when you create links in posting definitions:</span></span>

-   <span data-ttu-id="3276b-132">En gitt posteringsdefinisjon kan enten kobles til en annen posteringsdefinisjon eller kobles til fra en annen posteringsdefinisjon, men ikke begge.</span><span class="sxs-lookup"><span data-stu-id="3276b-132">A given posting definition can either link to another posting definition or be linked to from another posting definition, but not both.</span></span> <span data-ttu-id="3276b-133">En posteringsdefinisjon kan imidlertid koble til flere posteringsdefinisjoner.</span><span class="sxs-lookup"><span data-stu-id="3276b-133">However, a posting definition can link to multiple posting definitions.</span></span>
-   <span data-ttu-id="3276b-134">Du kan bare definere koblinger blant posteringsdefinisjoner som er i samme modul.</span><span class="sxs-lookup"><span data-stu-id="3276b-134">You can set up links only among posting definitions that are in the same module.</span></span>
-   <span data-ttu-id="3276b-135">Du kan tilordne en posteringsdefinisjon til en hvilken som helst transaksjonstype, men transaksjonstypen må være i samme modul som posteringsdefinisjonen.</span><span class="sxs-lookup"><span data-stu-id="3276b-135">You can assign a posting definition to any transaction type, but the transaction type must be in the same module as the posting definition.</span></span> <span data-ttu-id="3276b-136">Bruk siden **Definisjoner for transaksjonspostering** for å se hvilken modul en transaksjonstype er i.</span><span class="sxs-lookup"><span data-stu-id="3276b-136">Use the **Transaction posting definitions** page to see what module a transaction type is in.</span></span>


<span data-ttu-id="3276b-137">Hvis du vil ha mer informasjon, kan du se [Eksempler på posteringsdefinisjoner](example-posting-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="3276b-137">For more information, see [Posting definitions examples](example-posting-definitions.md).</span></span> 



