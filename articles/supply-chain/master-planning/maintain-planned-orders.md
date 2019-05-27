---
title: Vedlikeholde planlagte ordrer
description: Dette emnet gir informasjon om hvordan du behandler planlagte ordrer. Den beskriver hvordan du kan oppdatere statusen for planlagte ordrer, autorisere dem og filtrere etter planlagte ordrer som har samme status som en valgt planlagt ordre.
author: roxanadiaconu
manager: AnnBe
ms.date: 10/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19151
ms.assetid: 54123f4c-b4ca-4ce4-9358-b067aa04c968
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bf578d98abc4825c5607ec031da6ab6737c3183a
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1560378"
---
# <a name="maintain-planned-orders"></a><span data-ttu-id="56306-104">Vedlikeholde planlagte ordrer</span><span class="sxs-lookup"><span data-stu-id="56306-104">Maintain planned orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="56306-105">Dette emnet gir informasjon om hvordan du behandler planlagte ordrer.</span><span class="sxs-lookup"><span data-stu-id="56306-105">This topic provides information about how to manage planned orders.</span></span> <span data-ttu-id="56306-106">Den beskriver hvordan du kan oppdatere statusen for planlagte ordrer, autorisere dem og filtrere etter planlagte ordrer som har samme status som en valgt planlagt ordre.</span><span class="sxs-lookup"><span data-stu-id="56306-106">It describes how you can update the status of planned orders, firm them, and filter for planned orders that have the same status as a selected planned order.</span></span>

<span data-ttu-id="56306-107">Du kan administrere planlagte bestillinger fra arbeidsområdet **Hovedplanlegging**, listen **Planlagt bestilling** eller listene **Planlagte produksjonsordrer**, **Planlagte bestillinger** og **Overføringsforslag**.</span><span class="sxs-lookup"><span data-stu-id="56306-107">You can manage planned orders from the **Master planning** workspace, the **Planned order** list, or the **Planned production orders**, **Planned purchase orders**, and **Planned transfer** lists.</span></span> <span data-ttu-id="56306-108">Du kan bruke **Status**-feltet til å spore fremdriften.</span><span class="sxs-lookup"><span data-stu-id="56306-108">You can use the **Status** field to help track your progress.</span></span> <span data-ttu-id="56306-109">Følgende verdier brukes:</span><span class="sxs-lookup"><span data-stu-id="56306-109">The following values are used:</span></span>

-   <span data-ttu-id="56306-110">Når hovedplanlegging genererer planlagte ordrer, har de planlagte ordrene statusen **Ubehandlet**.</span><span class="sxs-lookup"><span data-stu-id="56306-110">When master planning generates planned orders, the planned orders have a status of **Unprocessed**.</span></span>
-   <span data-ttu-id="56306-111">Hvis du velger ikke å autorisere en planlagt bestilling, kan du gi den statusen **Fullført**.</span><span class="sxs-lookup"><span data-stu-id="56306-111">If you decide not to firm a planned order, you can give it a status of **Completed**.</span></span>
-   <span data-ttu-id="56306-112">Når du velger å autorisere en planlagt bestilling, kan du gi den statusen **Godkjent**.</span><span class="sxs-lookup"><span data-stu-id="56306-112">When you decide to firm a planned order, you can give it a status of **Approved**.</span></span> <span data-ttu-id="56306-113">Denne statusen innebærer at du godkjenner autoriseringen av den planlagte bestillingen, men den er ikke autorisert ennå.</span><span class="sxs-lookup"><span data-stu-id="56306-113">This status indicates that you approve firming of the planned order, but it isn't firmed yet.</span></span>

<span data-ttu-id="56306-114">**Obs!** En godkjent planlagt bestilling overføres i gjeldende tilstand til neste hovedplanberegning.</span><span class="sxs-lookup"><span data-stu-id="56306-114">**Note:** An approved planned order is transferred, in its current state, to the next master planning calculation.</span></span> <span data-ttu-id="56306-115">Du kan autorisere planlagte bestillinger ved å klikke **Autoriser**.</span><span class="sxs-lookup"><span data-stu-id="56306-115">You can firm planned orders by clicking **Firm**.</span></span> <span data-ttu-id="56306-116">Du kan autorisere følgende planlagte bestillinger:</span><span class="sxs-lookup"><span data-stu-id="56306-116">You can firm the following planned orders:</span></span>

-   <span data-ttu-id="56306-117">Den planlagte bestillingen som er merket.</span><span class="sxs-lookup"><span data-stu-id="56306-117">The planned order that is selected.</span></span>
-   <span data-ttu-id="56306-118">Flere planlagte bestillinger.</span><span class="sxs-lookup"><span data-stu-id="56306-118">Multiple planned orders.</span></span>
-   <span data-ttu-id="56306-119">Planlagte bestillinger som genereres gjennom en nedbryting fra siden **Nedbryting**.</span><span class="sxs-lookup"><span data-stu-id="56306-119">Planned orders that are generated by an explosion from the **Explosion** page.</span></span> <span data-ttu-id="56306-120">Klikk **Planlagte bestillinger**, merk den planlagte bestillingen, og klikk deretter **Autoriser**.</span><span class="sxs-lookup"><span data-stu-id="56306-120">Click **Planned orders**, select the planned order, and then click **Firm**.</span></span>

<span data-ttu-id="56306-121">Når en planlagt bestilling autoriseres, flyttes den til bestillingsdelen i den aktuelle modulen.</span><span class="sxs-lookup"><span data-stu-id="56306-121">When a planned order is firmed, it's moved to the orders section of the relevant module.</span></span> 

<a name="additional-resources"></a><span data-ttu-id="56306-122">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="56306-122">Additional resources</span></span>
--------

[<span data-ttu-id="56306-123">Hovedplaner</span><span class="sxs-lookup"><span data-stu-id="56306-123">Master plans</span></span>](master-plans.md)



