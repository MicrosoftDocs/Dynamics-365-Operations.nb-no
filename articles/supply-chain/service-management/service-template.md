---
title: Servicemaler
description: Du kan definere en serviceavtale som en mal, og senere kopiere linjene i malen til andre serviceavtaler eller til en serviceordre.
author: YuyuScheller
manager: AnnBe
ms.date: 02/19/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAAgreementTable
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
ms.sourcegitcommit: 09f2da382cd7f3e0e3d4bfa389e9cdf74f00b501
ms.openlocfilehash: ade518095b77141fb31b597a955dd23aaae119d7
ms.contentlocale: nb-no
ms.lasthandoff: 02/27/2018

---

# <a name="service-templates"></a><span data-ttu-id="30d51-103">Servicemaler</span><span class="sxs-lookup"><span data-stu-id="30d51-103">Service templates</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="30d51-104">Du kan definere en serviceavtale som en mal, og senere kopiere linjene i malen til andre serviceavtaler eller til en serviceordre.</span><span class="sxs-lookup"><span data-stu-id="30d51-104">You can define a service agreement as a template and copy the lines of the template later into another service agreement or into a service order.</span></span>

## <a name="example"></a><span data-ttu-id="30d51-105">Eksempel</span><span class="sxs-lookup"><span data-stu-id="30d51-105">Example</span></span>

<span data-ttu-id="30d51-106">En kunde som du tilbyr en tjeneste, har identiske heiser på fem forskjellige steder.</span><span class="sxs-lookup"><span data-stu-id="30d51-106">A customer for whom you provide service has identical service elevators at five different locations.</span></span>

<span data-ttu-id="30d51-107">Du vil angi fem serviceavtaler for kunden, én for hvert sted.</span><span class="sxs-lookup"><span data-stu-id="30d51-107">You want to set up five service agreements for the customer, one for each site.</span></span>
<span data-ttu-id="30d51-108">For å begrense gjentakende oppsett og å sørge for at oppsettinformasjonen i serviceavtalene er identiske kan du opprette en serviceavtale og angi den som en mal for vedlikeholdsarbeid på heisene.</span><span class="sxs-lookup"><span data-stu-id="30d51-108">To limit repetitive setup work, and to make sure that the setup information in the service agreements is identical, you create a service agreement and specify it as a template for the service work on the elevators.</span></span>

<span data-ttu-id="30d51-109">Du kan nå kopiere mallinjene til de fem nye serviceavtalene slik at hver serviceavtale fylles med linjer fra malen.</span><span class="sxs-lookup"><span data-stu-id="30d51-109">You can now copy the template lines into the five new service agreements, so that each service agreement is populated with the lines from the template.</span></span>

## <a name="create-a-template"></a><span data-ttu-id="30d51-110">Opprett en mal</span><span class="sxs-lookup"><span data-stu-id="30d51-110">Create a template</span></span>

<span data-ttu-id="30d51-111">Når du oppretter en servicemal, oppretter du en serviceavtale, oppretter deretter de obligatoriske linjene og knytter en serviceavtale til en servicemalgruppe.</span><span class="sxs-lookup"><span data-stu-id="30d51-111">When you create a service template, you create a service agreement, create the required lines on it, and attach the service agreement to a service-template group.</span></span>

> [!NOTE]
> <span data-ttu-id="30d51-112">En serviceavtalen kan bare defineres som en mal hvis den ikke har en tilknyttet serviceordre.</span><span class="sxs-lookup"><span data-stu-id="30d51-112">A service agreement can be defined as a template only if it has no service orders attached to it.</span></span> <span data-ttu-id="30d51-113">En serviceordre kan heller ikke genereres fra en serviceavtale som er definert som en mal.</span><span class="sxs-lookup"><span data-stu-id="30d51-113">Also, no service orders can be generated from a service agreement that is defined as a template.</span></span>

## <a name="copy-template-lines"></a><span data-ttu-id="30d51-114">Kopier mallinjer</span><span class="sxs-lookup"><span data-stu-id="30d51-114">Copy template lines</span></span>

<span data-ttu-id="30d51-115">Du kan kopiere mallinjer fra en servicemal til en annen serviceavtale eller til en serviceordre.</span><span class="sxs-lookup"><span data-stu-id="30d51-115">You can copy template lines from a service template into another service agreement or into a service order.</span></span>

<span data-ttu-id="30d51-116">Når du kopierer mallinjer til serviceordrene eller serviceavtalene, vises malgruppene i en trevisning der hver gruppe kan utvides.</span><span class="sxs-lookup"><span data-stu-id="30d51-116">When you copy template lines into your service orders or service agreements, your template groups are displayed in a tree view in which each group can be expanded.</span></span> <span data-ttu-id="30d51-117">I denne visningen kan du se hver mal og mallinje.</span><span class="sxs-lookup"><span data-stu-id="30d51-117">This display lets you view each template and template line.</span></span>

<span data-ttu-id="30d51-118">Det er enklere å bestemme servicemallinjene som du vil kopiere, hvis du har gruppert malene under navn som reflekterer bruken til malene.</span><span class="sxs-lookup"><span data-stu-id="30d51-118">It is easier to determine the service-template lines that you want to copy if you have grouped the templates under names that reflect the use of the templates.</span></span>

## <a name="related-topics"></a><span data-ttu-id="30d51-119">Relaterte emner</span><span class="sxs-lookup"><span data-stu-id="30d51-119">Related topics</span></span>

[<span data-ttu-id="30d51-120">Kopiere servicemallinjer</span><span class="sxs-lookup"><span data-stu-id="30d51-120">Copy service templates lines</span></span>](copy-service-template-lines.md)
