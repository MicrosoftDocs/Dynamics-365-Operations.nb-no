---
title: Opprette serviceobjektrelasjoner
description: Dette emnet beskriver hvordan du oppretter serviceobjektforbindelser for en serviceavtale og en serviceordre.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 44ca8920619ff4b0ae45293c997a8c385cfbd091
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5234903"
---
# <a name="create-service-object-relations"></a><span data-ttu-id="b3a3f-103">Opprette serviceobjektrelasjoner</span><span class="sxs-lookup"><span data-stu-id="b3a3f-103">Create service object relations</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="b3a3f-104">Dette emnet beskriver hvordan du oppretter serviceobjektforbindelser for en serviceavtale og en serviceordre.</span><span class="sxs-lookup"><span data-stu-id="b3a3f-104">This topic describes how to create service object relations for a service agreement and a service order.</span></span> <span data-ttu-id="b3a3f-105">Når du oppretter en serviceobjektrelasjon, knytter du serviceobjektet til en serviceavtale eller serviceordre.</span><span class="sxs-lookup"><span data-stu-id="b3a3f-105">When you a create service object relation, you associate the service object to a service agreement or service order.</span></span> <span data-ttu-id="b3a3f-106">Når en kunde ber om service for en vare som er et serviceobjekt, kan du velge serviceobjektet fra listen over serviceobjektrelasjoner.</span><span class="sxs-lookup"><span data-stu-id="b3a3f-106">When a customer requests service for an item that is a service object, you can select the service object from the list of service object relations.</span></span>

## <a name="create-a-service-object-relation-for-a-service-agreement"></a><span data-ttu-id="b3a3f-107">Opprette en serviceobjektrelasjon for en serviceavtale</span><span class="sxs-lookup"><span data-stu-id="b3a3f-107">Create a service object relation for a service agreement</span></span>

<span data-ttu-id="b3a3f-108">Bruk følgende fremgangsmåte for opprette en serviceobjektrelasjon for en serviceavtale:</span><span class="sxs-lookup"><span data-stu-id="b3a3f-108">Use the following steps to create a service object relation for a service agreement:</span></span>

1.  <span data-ttu-id="b3a3f-109">Klikk på **Servicestyring** \> **Felles** \> **Serviceavtaler** \> **Serviceavtaler**.</span><span class="sxs-lookup"><span data-stu-id="b3a3f-109">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="b3a3f-110">Velg en eksisterende serviceavtale i **Serviceavtaler**-listen, eller klikk **Ny** hvis du vil opprette en ny serviceavtale.</span><span class="sxs-lookup"><span data-stu-id="b3a3f-110">In the **Service agreements** list, select an existing service agreement, or click **New** to create a new service agreement.</span></span>

3.  <span data-ttu-id="b3a3f-111">På skjemaet **Serviceavtaler**, i **handlingsruten**, på fanen **Serviceavtale**, i **Relasjoner**-gruppen, klikker du på **Serviceobjekter**.</span><span class="sxs-lookup"><span data-stu-id="b3a3f-111">In the **Service agreements** form, on the **Action Pane**, on the **Service agreement** tab, in the **Relations** group, click **Service objects**.</span></span>

4.  <span data-ttu-id="b3a3f-112">Klikk på **Ny** i **Serviceobjekter**-skjemaet, og velg deretter et serviceobjekt for denne serviceavtalen.</span><span class="sxs-lookup"><span data-stu-id="b3a3f-112">In the **Service objects** form, click **New**, and then select a service object for this service agreement.</span></span>

5.  <span data-ttu-id="b3a3f-113">Hvis du vil tilordne en malstykkliste til serviceavtalen, klikker du **Funksjoner**, og deretter velger du **Tilknytt malstykkliste**.</span><span class="sxs-lookup"><span data-stu-id="b3a3f-113">To assign a template bill of materials (BOM) to the service agreement, click **Functions**, and then select **Attach template BOM**.</span></span> <span data-ttu-id="b3a3f-114">Velg en mal i feltet **Malstykkliste** i skjemaet **Velg malstykkliste**.</span><span class="sxs-lookup"><span data-stu-id="b3a3f-114">In the **Select template BOM** form, in the **Template BOM** field, select a template.</span></span> 

## <a name="create-a-service-object-relation-for-a-service-order"></a><span data-ttu-id="b3a3f-115">Opprette en serviceobjektrelasjon for en serviceordre</span><span class="sxs-lookup"><span data-stu-id="b3a3f-115">Create a service object relation for a service order</span></span>

<span data-ttu-id="b3a3f-116">Bruk følgende fremgangsmåte for opprette en serviceobjektrelasjon for en serviceordre:</span><span class="sxs-lookup"><span data-stu-id="b3a3f-116">Use the following steps to create a service object relation for a service order:</span></span>

1.  <span data-ttu-id="b3a3f-117">Klikk på **Servicestyring** \> **Felles** \> **Serviceordrer** \> **Serviceordrer**.</span><span class="sxs-lookup"><span data-stu-id="b3a3f-117">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="b3a3f-118">Velg en eksisterende serviceordre i **Serviceordrer**-listen, eller opprett en ny serviceordre.</span><span class="sxs-lookup"><span data-stu-id="b3a3f-118">In the **Service orders** list, select an existing service order, or create a new service order.</span></span>

3.  <span data-ttu-id="b3a3f-119">På skjemaet **Serviceordrer**, i **handlingsruten**, på fanen **Serviceordre**, i **Relasjoner**-gruppen, klikker du på **Serviceobjekter**.</span><span class="sxs-lookup"><span data-stu-id="b3a3f-119">In the **Service orders** form, on the **Action Pane**, on the **Service order** tab, in the **Relations** group, click **Service objects**.</span></span>

4.  <span data-ttu-id="b3a3f-120">Klikk på **Ny** i **Serviceobjekter**-skjemaet, og velg deretter et serviceobjekt for denne serviceordren.</span><span class="sxs-lookup"><span data-stu-id="b3a3f-120">In the **Service objects** form, click **New**, and then select a service object for this service order.</span></span>

5.  <span data-ttu-id="b3a3f-121">Hvis du vil tilordne en malstykkliste til serviceavtalen, klikker du **Funksjoner**, og deretter velger du **Tilknytt malstykkliste**.</span><span class="sxs-lookup"><span data-stu-id="b3a3f-121">To assign a template BOM to the service agreement, click **Functions**, and then select **Attach template BOM**.</span></span> <span data-ttu-id="b3a3f-122">Velg en mal i feltet **Malstykkliste** i skjemaet **Velg malstykkliste**.</span><span class="sxs-lookup"><span data-stu-id="b3a3f-122">In the **Select template BOM** form, in the **Template BOM** field, select a template.</span></span> 


## <a name="see-also"></a><span data-ttu-id="b3a3f-123">Se også</span><span class="sxs-lookup"><span data-stu-id="b3a3f-123">See also</span></span>

[<span data-ttu-id="b3a3f-124">Oversikt over serviceobjekter</span><span class="sxs-lookup"><span data-stu-id="b3a3f-124">Service objects overview</span></span>](service-objects.md)

[<span data-ttu-id="b3a3f-125">Serviceobjektrelasjoner</span><span class="sxs-lookup"><span data-stu-id="b3a3f-125">Service object relations</span></span>](service-object-relations.md)

[<span data-ttu-id="b3a3f-126">Malstykklister</span><span class="sxs-lookup"><span data-stu-id="b3a3f-126">Template BOMs</span></span>](template-boms.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]