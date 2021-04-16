---
title: Definere tillatelser for bestilling av produkter på vegne av andre
description: Dette emnet forklarer hvordan du gir arbeidere tillatelse til å klargjøre innkjøpsrekvisisjoner på vegne av andre arbeidere.
author: kamaybac
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchReqAuthorization, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d0408085d401a34a409bfe46bc6845a9c81a2eea
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5811900"
---
# <a name="set-up-permissions-for-ordering-products-on-behalf-of-someone-else"></a><span data-ttu-id="eac21-103">Definere tillatelser for bestilling av produkter på vegne av andre</span><span class="sxs-lookup"><span data-stu-id="eac21-103">Set up permissions for ordering products on behalf of someone else</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="eac21-104">Dette emnet forklarer hvordan du gir arbeidere tillatelse til å klargjøre innkjøpsrekvisisjoner på vegne av andre arbeidere.</span><span class="sxs-lookup"><span data-stu-id="eac21-104">This topic explains how to grant workers permission to prepare purchase requisitions on behalf of other workers.</span></span> <span data-ttu-id="eac21-105">Med andre ord kan en innkjøpsrekvisisjonsklargjører opprette en rekvisisjon for en annen "bestiller".</span><span class="sxs-lookup"><span data-stu-id="eac21-105">In other words, a purchase requisition "preparer" can create a requisition for another "requester."</span></span> <span data-ttu-id="eac21-106">Prosedyren viser også hvordan du kan gi arbeidere tillatelse til å bestille varer og tjenester i andre juridiske enheter eller driftsenheter.</span><span class="sxs-lookup"><span data-stu-id="eac21-106">The procedure also shows how to grant a worker permission to order items and services in different legal entities or operating units.</span></span> <span data-ttu-id="eac21-107">Disse oppgavene utføres vanligvis av en innkjøpssjef.</span><span class="sxs-lookup"><span data-stu-id="eac21-107">Typically, these tasks are performed by a purchasing manager.</span></span> <span data-ttu-id="eac21-108">Du kan bruke denne fremgangsmåten i demonstrasjonsdatafirmaet USMF eller på dine egne data.</span><span class="sxs-lookup"><span data-stu-id="eac21-108">You can use this procedure either on data for the USMF demo company or on your own data.</span></span>


## <a name="grant-permission-to-enter-purchase-requisitions-on-behalf-of-another-worker"></a><span data-ttu-id="eac21-109">Gi tillatelser til å registrere innkjøpsrekvisisjoner på vegne av en annen arbeider</span><span class="sxs-lookup"><span data-stu-id="eac21-109">Grant permission to enter purchase requisitions on behalf of another worker</span></span>
1. <span data-ttu-id="eac21-110">I navigasjonsruten går du til **Moduler > Innkjøp og leverandører > Oppsett > Policyer > Innkjøpsrekvisisjonstillatelser**.</span><span class="sxs-lookup"><span data-stu-id="eac21-110">In the navigation pane, go to **Modules > Procurement and sourcing > Setup > Policies > Purchase requisition permissions**.</span></span> <span data-ttu-id="eac21-111">Kontroller at feltet **Gjeldende visning** er satt til **Etter klargjører**.</span><span class="sxs-lookup"><span data-stu-id="eac21-111">Make sure that the **Current view** field is set to **By preparer**.</span></span> <span data-ttu-id="eac21-112">Listen i ruten til venstre, viser personene som kan gis tillatelse til å klargjøre rekvisisjoner på vegne av andre.</span><span class="sxs-lookup"><span data-stu-id="eac21-112">The list in the left pane shows the people who can be granted permission to prepare requisitions on behalf of other people.</span></span>  
2. <span data-ttu-id="eac21-113">Velg personen som skal gis tilgang (klargjøreren).</span><span class="sxs-lookup"><span data-stu-id="eac21-113">Select the person to grant permission to (the preparer).</span></span>
3. <span data-ttu-id="eac21-114">Velg **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="eac21-114">Select **Add**.</span></span>
4. <span data-ttu-id="eac21-115">Finn og velg personen som skal legges til som en bestiller.</span><span class="sxs-lookup"><span data-stu-id="eac21-115">Find and select the person to add as a requester.</span></span>
    - <span data-ttu-id="eac21-116">Bestilleren er personen som klargjøreren kan opprette rekvisisjoner på vegne av.</span><span class="sxs-lookup"><span data-stu-id="eac21-116">The requester is the person that the preparer can create requisitions on behalf of.</span></span>  
    - <span data-ttu-id="eac21-117">I feltet **Autorisasjon**, velger du **Bestemte** hvis klargjøreren skal kunne opprette innkjøpsrekvisisjoner på vegne av den valgte arbeideren.</span><span class="sxs-lookup"><span data-stu-id="eac21-117">In the **Authorization** field, select **Specific** if the preparer should be able to create purchase requisitions on behalf of the selected worker.</span></span> <span data-ttu-id="eac21-118">Velg **Rapportering** hvis klargjøreren også skal kunne opprette innkjøpsrekvisisjoner på vegne av alle arbeidere som rapporterer til denne arbeideren.</span><span class="sxs-lookup"><span data-stu-id="eac21-118">Select **Reporting** if the preparer should also be able to create purchase requisitions on behalf of all workers who report to that worker.</span></span>  
5. <span data-ttu-id="eac21-119">Angi en dato i **Gyldig**-feltet.</span><span class="sxs-lookup"><span data-stu-id="eac21-119">In the **Effective** field, enter a date.</span></span>
6. <span data-ttu-id="eac21-120">Angi en dato i **Utløp**-feltet.</span><span class="sxs-lookup"><span data-stu-id="eac21-120">In the **Expiration** field, enter a date.</span></span>

## <a name="view-preparers-who-have-permission-to-create-purchase-requisitions-for-a-selected-worker"></a><span data-ttu-id="eac21-121">Vise klargjørerne som har tillatelse til å opprette innkjøpsrekvisisjoner for en valgt arbeider</span><span class="sxs-lookup"><span data-stu-id="eac21-121">View preparers who have permission to create purchase requisitions for a selected worker</span></span>
1. <span data-ttu-id="eac21-122">Velg **Etter bestiller** i feltet **Gjeldende visning**.</span><span class="sxs-lookup"><span data-stu-id="eac21-122">In the **Current view** field, select **By requester**.</span></span> <span data-ttu-id="eac21-123">Denne visningen viser en liste over klargjørere som er gitt tillatelse til å opprette innkjøpsrekvisisjoner på vegne av en valgt arbeider.</span><span class="sxs-lookup"><span data-stu-id="eac21-123">This view shows a list of preparers who have been granted permission to create purchase requisitions on behalf of a selected worker.</span></span>  
2. <span data-ttu-id="eac21-124">Bruk dette hurtigfilteret til å finne arbeideren som du nettopp la til som bestiller.</span><span class="sxs-lookup"><span data-stu-id="eac21-124">Use the Quick Filter to find the worker that you just added as the requester.</span></span>
3. <span data-ttu-id="eac21-125">Velg bestilleren.</span><span class="sxs-lookup"><span data-stu-id="eac21-125">Select the requester.</span></span> <span data-ttu-id="eac21-126">Klargjørerlisten viser personene som har tillatelse til å bestille varer på vegne av bestilleren, som er valgt i ruten til venstre.</span><span class="sxs-lookup"><span data-stu-id="eac21-126">The Preparer list shows the people who have permission to order items on behalf of the requester who is selected in the left pane.</span></span>  <span data-ttu-id="eac21-127">Du kan legge til flere klargjørerne her.</span><span class="sxs-lookup"><span data-stu-id="eac21-127">You can add additional preparers here.</span></span> <span data-ttu-id="eac21-128">Denne visningen lar deg også gi bestilleren tillatelse til å opprette rekvisisjoner i juridiske enheter og driftsenheter som ikke er primær juridisk enhet eller driftsenhet for den aktuelle personen.</span><span class="sxs-lookup"><span data-stu-id="eac21-128">This view also lets you grant the requester permission to create requisitions in legal entities and operating units that aren't that person's primary legal entity or operating unit.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]