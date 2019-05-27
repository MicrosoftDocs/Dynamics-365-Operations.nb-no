---
title: Serviceobjekter
description: Serviceobjekter er en kundes aktiva og produkter som du kan utføre en tjeneste for.
author: ShylaThompson
manager: AnnBe
ms.date: 02/21/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceObjectTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5641077de84b6702d2c5621edef74783f2f104fd
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1562329"
---
# <a name="service-objects"></a><span data-ttu-id="23092-103">Serviceobjekter</span><span class="sxs-lookup"><span data-stu-id="23092-103">Service objects</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="23092-104">Serviceobjekter er en kundes aktiva og produkter som du kan utføre en tjeneste for.</span><span class="sxs-lookup"><span data-stu-id="23092-104">Service objects are a customer’s assets and products for which you can perform a service.</span></span> <span data-ttu-id="23092-105">Avhengig av servicetypen du tilbyr, kan objekter være materielle eller immaterielle:</span><span class="sxs-lookup"><span data-stu-id="23092-105">Depending on the type of service you provide, objects can be tangible or intangible:</span></span>

-  <span data-ttu-id="23092-106">Konkrete objekter er gjenstander, for eksempel en maskin eller en bygning, som du kan utføre en fysisk serviceoppgave på.</span><span class="sxs-lookup"><span data-stu-id="23092-106">Tangible objects are things, such as a machine or a building, on which you can perform a physical service task.</span></span>

    <span data-ttu-id="23092-107">Et materielt serviceobjekt kan også være en lagervare du oppretter i skjemaet Detaljer om frigitt produkt.</span><span class="sxs-lookup"><span data-stu-id="23092-107">A tangible service object can also be an inventory item that you create in the Released product details form.</span></span> <span data-ttu-id="23092-108">Avhengig av lagerdimensjonsgruppen du har tilknyttet varen, kan du opprette et serviceobjektet på et detaljnivå som inneholder varens serienummer.</span><span class="sxs-lookup"><span data-stu-id="23092-108">Depending on the inventory dimension group that you attach to the item, you can create a service object to a level of detail that includes the item serial number.</span></span> <span data-ttu-id="23092-109">Dette er nyttig når du må vite nøyaktig hvilken vare som serviceobjektet representerer.</span><span class="sxs-lookup"><span data-stu-id="23092-109">This is useful when you must keep track of the exact item that the service object represents.</span></span>

    <span data-ttu-id="23092-110">Et materielt serviceobjekt kan imidlertid også være en vare som ikke er direkte relatert til den direkte produksjonen eller forsyningskjeden til et firma.</span><span class="sxs-lookup"><span data-stu-id="23092-110">A tangible service object can also be an item that is not directly related to a company's direct production or supply chain.</span></span> <span data-ttu-id="23092-111">Et verktøysett som brukes til reparasjoner i en serviceordre kan for eksempel være et serviceobjekt som ikke er inkludert i lageret.</span><span class="sxs-lookup"><span data-stu-id="23092-111">For example, a tool kit that is used for repairs in a service order can be a service object that is not included in inventory.</span></span> <span data-ttu-id="23092-112">I dette tilfellet registrere du den ikke som en lagervare.</span><span class="sxs-lookup"><span data-stu-id="23092-112">In this case, you don’t register it as an inventory item.</span></span>

-  <span data-ttu-id="23092-113">Immaterielle objekter er ikke-fysiske ting, for eksempel et sett med kontoer eller et juridisk dokument, som du kan utføre serviceoppgaver på.</span><span class="sxs-lookup"><span data-stu-id="23092-113">Intangible objects are nonphysical things, such as a set of accounts or a legal document, on which you can perform a service task.</span></span>

## <a name="example-of-an-intangible-service-object"></a><span data-ttu-id="23092-114">Eksempel på et immaterielt serviceobjekt</span><span class="sxs-lookup"><span data-stu-id="23092-114">Example of an intangible service object</span></span>

<span data-ttu-id="23092-115">Firma A opprettholder finanspostene for flere små firmaer.</span><span class="sxs-lookup"><span data-stu-id="23092-115">Company A maintains the financial records for several small companies.</span></span> <span data-ttu-id="23092-116">En av kundene til firma A er det lokale fotballaget, og firma A fører ukentlig bokføring og årlig revisjon for klubbens kontoer.</span><span class="sxs-lookup"><span data-stu-id="23092-116">One of Company A's clients is the local football team, for which Company A does the weekly bookkeeping and annual audit of the club's accounts.</span></span> <span data-ttu-id="23092-117">Lagets kontoer er definert i Serviceobjekter-skjemaet og angitt som objektet i serviceavtalen.</span><span class="sxs-lookup"><span data-stu-id="23092-117">The club's accounts are set up in the Service objects form and specified as the object in the service agreement.</span></span> <span data-ttu-id="23092-118">Det er to serviceavtalelinjer for objektet.</span><span class="sxs-lookup"><span data-stu-id="23092-118">There are two service agreement lines for the object.</span></span> <span data-ttu-id="23092-119">Linje 1 er ukentlig bokføring med et ukentlig intervall som er tilordnet til linjen, og linje 2 er årlig revisjon med et årlig intervall som er tilordnet.</span><span class="sxs-lookup"><span data-stu-id="23092-119">Line 1 is weekly bookkeeping with a weekly interval assigned to the line, and line 2 is the annual audit with a yearly interval assigned to it.</span></span>

## <a name="related-topics"></a><span data-ttu-id="23092-120">Relaterte emner</span><span class="sxs-lookup"><span data-stu-id="23092-120">Related topics</span></span>

[<span data-ttu-id="23092-121">Opprette serviceobjekter</span><span class="sxs-lookup"><span data-stu-id="23092-121">Create service objects</span></span>](create-service-objects.md)

