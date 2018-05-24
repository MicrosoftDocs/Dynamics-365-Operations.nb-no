---
title: Serviceordrestadier
description: "Når du definerer stadiene for en serviceordre og tilordner dem til arbeidere, kan du styre flyten i en serviceordre gjennom oppgavene som ulike personer utfører i serviceorganisasjonen."
author: YuyuScheller
manager: AnnBe
ms.date: 04/30/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable, SMAStageTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 9aa90dfcfc4b30d6cb4fa7ed4e6faaf505548d41
ms.contentlocale: nb-no
ms.lasthandoff: 05/08/2018

---

# <a name="service-order-stages"></a><span data-ttu-id="b6d35-103">Serviceordrestadier</span><span class="sxs-lookup"><span data-stu-id="b6d35-103">Service order stages</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="b6d35-104">Du kan opprette stadier for en serviceordre for å definere oppgavene som må fullføres, rekkefølgen de skal fullføres i, og arbeiderne som er ansvarlige for å fullføre dem.</span><span class="sxs-lookup"><span data-stu-id="b6d35-104">You can set up stages for a service order to define the tasks that must be completed, the order in which they are completed, and the workers who are responsible for completing them.</span></span> <span data-ttu-id="b6d35-105">Når du definerer stadiene for en serviceordre og tilordner dem til arbeidere, kan du styre flyten i en serviceordre gjennom oppgavene som ulike personer utfører i serviceorganisasjonen.</span><span class="sxs-lookup"><span data-stu-id="b6d35-105">By defining the stages for a service order and assigning them to workers, you can control the flow of a service order through the tasks that various people perform in the service organization.</span></span> <span data-ttu-id="b6d35-106">Stadienes rekkefølge må inneholde et innledende stadium.</span><span class="sxs-lookup"><span data-stu-id="b6d35-106">The sequence of stages must include an initial stage.</span></span>

<span data-ttu-id="b6d35-107">Du kan også definere hvilke handlinger som skal tillates på hvert stadium.</span><span class="sxs-lookup"><span data-stu-id="b6d35-107">You can also define the actions that are permitted at each stage.</span></span> <span data-ttu-id="b6d35-108">Hvis du for eksempel fjerner merket for **Poster** for alle stadier unntatt det siste stadiet, hindrer du at serviceordrer posteres før serviceordrene er behandlet i hele sekvensen av stadier.</span><span class="sxs-lookup"><span data-stu-id="b6d35-108">For example, if you clear the **Post** check box for all stages except the final stage, you prevent any service orders from being posted before the service orders are processed through the complete sequence of stages.</span></span>

## <a name="branching-in-service-order-stages"></a><span data-ttu-id="b6d35-109">Forgrening i serviceordrestadier</span><span class="sxs-lookup"><span data-stu-id="b6d35-109">Branching in service order stages</span></span>

<span data-ttu-id="b6d35-110">Når du oppretter et servicestadium, kan du opprette flere alternativer, eller grener, som du kan velge blant for det neste servicestadiet.</span><span class="sxs-lookup"><span data-stu-id="b6d35-110">When you set up a service stage, you can create multiple options, or branches, to select from for the next service stage.</span></span> <span data-ttu-id="b6d35-111">Alle grenene du oppretter, er tilgjengelige for valg når det innledende stadiet er fullført.</span><span class="sxs-lookup"><span data-stu-id="b6d35-111">All the branches that you create are available to select from when the initial stage is completed.</span></span> <span data-ttu-id="b6d35-112">La oss si at du definerer **Planlegging** som et første stadium.</span><span class="sxs-lookup"><span data-stu-id="b6d35-112">For example, you set up **Planning** as an initial stage.</span></span> <span data-ttu-id="b6d35-113">Du oppretter to stadier kalt **Pågår** og **Avbryt**, og velger deretter **Planlegging** som overordnet for dem.</span><span class="sxs-lookup"><span data-stu-id="b6d35-113">You create two stages named **In process** and **Cancel**, and then select **Planning** as the parent for them.</span></span> <span data-ttu-id="b6d35-114">Du tilordner **Planlegging**-stadiet til salgsordren.</span><span class="sxs-lookup"><span data-stu-id="b6d35-114">You assign the **Planning** stage to sales order.</span></span> <span data-ttu-id="b6d35-115">Når planleggingsstadiet for salgsordren er fullført, kan du velge stadiet **Pågår** hvis salgsordren er klar til å bli arbeidet med, eller du kan velge stadiet **Avbryt** hvis salgsordren er avbrutt.</span><span class="sxs-lookup"><span data-stu-id="b6d35-115">When the planning stage for the sales order is completed, you can select the **In process** stage if the sales order is ready to work on, or you can select the **Cancel** stage if the sales order is canceled.</span></span>

## <a name="see-also"></a><span data-ttu-id="b6d35-116">Se også</span><span class="sxs-lookup"><span data-stu-id="b6d35-116">See also</span></span>

[<span data-ttu-id="b6d35-117">Definer serviceordrestadier</span><span class="sxs-lookup"><span data-stu-id="b6d35-117">Set up service order stages</span></span>](set-up-service-order-stages.md)

[<span data-ttu-id="b6d35-118">Endre serviceordrestadiet</span><span class="sxs-lookup"><span data-stu-id="b6d35-118">Change the service order stage</span></span>](change-service-order-stage.md)

  



