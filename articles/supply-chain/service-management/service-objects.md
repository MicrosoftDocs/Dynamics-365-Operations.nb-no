---
title: Oversikt over serviceobjekter
description: Serviceobjekter er en kundes aktiva og produkter som du kan utføre en tjeneste for.
author: ShylaThompson
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceObjectTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 29d2cf6a496fed8d9932d5c6d49f4560d7eabbbb
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/10/2020
ms.locfileid: "3979118"
---
# <a name="service-objects-overview"></a><span data-ttu-id="8aa37-103">Oversikt over serviceobjekter</span><span class="sxs-lookup"><span data-stu-id="8aa37-103">Service objects overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8aa37-104">Serviceobjekter er en kundes aktiva og produkter som du kan utføre en tjeneste for.</span><span class="sxs-lookup"><span data-stu-id="8aa37-104">Service objects are a customer’s assets and products for which you can perform a service.</span></span> <span data-ttu-id="8aa37-105">Avhengig av servicetypen du tilbyr, kan objekter være materielle eller immaterielle:</span><span class="sxs-lookup"><span data-stu-id="8aa37-105">Depending on the type of service you provide, objects can be tangible or intangible:</span></span>

-  <span data-ttu-id="8aa37-106">Konkrete objekter er gjenstander, for eksempel en maskin eller en bygning, som du kan utføre en fysisk serviceoppgave på.</span><span class="sxs-lookup"><span data-stu-id="8aa37-106">Tangible objects are things, such as a machine or a building, on which you can perform a physical service task.</span></span>

    <span data-ttu-id="8aa37-107">Et materielt serviceobjekt kan også være en lagervare du oppretter i skjemaet Detaljer om frigitt produkt.</span><span class="sxs-lookup"><span data-stu-id="8aa37-107">A tangible service object can also be an inventory item that you create in the Released product details form.</span></span> <span data-ttu-id="8aa37-108">Avhengig av lagerdimensjonsgruppen du har tilknyttet varen, kan du opprette et serviceobjektet på et detaljnivå som inneholder varens serienummer.</span><span class="sxs-lookup"><span data-stu-id="8aa37-108">Depending on the inventory dimension group that you attach to the item, you can create a service object to a level of detail that includes the item serial number.</span></span> <span data-ttu-id="8aa37-109">Dette er nyttig når du må vite nøyaktig hvilken vare som serviceobjektet representerer.</span><span class="sxs-lookup"><span data-stu-id="8aa37-109">This is useful when you must keep track of the exact item that the service object represents.</span></span>

    <span data-ttu-id="8aa37-110">Et materielt serviceobjekt kan imidlertid også være en vare som ikke er direkte relatert til den direkte produksjonen eller forsyningskjeden til et firma.</span><span class="sxs-lookup"><span data-stu-id="8aa37-110">A tangible service object can also be an item that is not directly related to a company's direct production or supply chain.</span></span> <span data-ttu-id="8aa37-111">Et verktøysett som brukes til reparasjoner i en serviceordre kan for eksempel være et serviceobjekt som ikke er inkludert i lageret.</span><span class="sxs-lookup"><span data-stu-id="8aa37-111">For example, a tool kit that is used for repairs in a service order can be a service object that is not included in inventory.</span></span> <span data-ttu-id="8aa37-112">I dette tilfellet registrere du den ikke som en lagervare.</span><span class="sxs-lookup"><span data-stu-id="8aa37-112">In this case, you don’t register it as an inventory item.</span></span>

-  <span data-ttu-id="8aa37-113">Immaterielle objekter er ikke-fysiske ting, for eksempel et sett med kontoer eller et juridisk dokument, som du kan utføre serviceoppgaver på.</span><span class="sxs-lookup"><span data-stu-id="8aa37-113">Intangible objects are nonphysical things, such as a set of accounts or a legal document, on which you can perform a service task.</span></span>

## <a name="example-of-an-intangible-service-object"></a><span data-ttu-id="8aa37-114">Eksempel på et immaterielt serviceobjekt</span><span class="sxs-lookup"><span data-stu-id="8aa37-114">Example of an intangible service object</span></span>

<span data-ttu-id="8aa37-115">Firma A opprettholder finanspostene for flere små firmaer.</span><span class="sxs-lookup"><span data-stu-id="8aa37-115">Company A maintains the financial records for several small companies.</span></span> <span data-ttu-id="8aa37-116">En av kundene til firma A er det lokale fotballaget, og firma A fører ukentlig bokføring og årlig revisjon for klubbens kontoer.</span><span class="sxs-lookup"><span data-stu-id="8aa37-116">One of Company A's clients is the local football team, for which Company A does the weekly bookkeeping and annual audit of the club's accounts.</span></span> <span data-ttu-id="8aa37-117">Lagets kontoer er definert i Serviceobjekter-skjemaet og angitt som objektet i serviceavtalen.</span><span class="sxs-lookup"><span data-stu-id="8aa37-117">The club's accounts are set up in the Service objects form and specified as the object in the service agreement.</span></span> <span data-ttu-id="8aa37-118">Det er to serviceavtalelinjer for objektet.</span><span class="sxs-lookup"><span data-stu-id="8aa37-118">There are two service agreement lines for the object.</span></span> <span data-ttu-id="8aa37-119">Linje 1 er ukentlig bokføring med et ukentlig intervall som er tilordnet til linjen, og linje 2 er årlig revisjon med et årlig intervall som er tilordnet.</span><span class="sxs-lookup"><span data-stu-id="8aa37-119">Line 1 is weekly bookkeeping with a weekly interval assigned to the line, and line 2 is the annual audit with a yearly interval assigned to it.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8aa37-120">Relaterte emner</span><span class="sxs-lookup"><span data-stu-id="8aa37-120">Related topics</span></span>

[<span data-ttu-id="8aa37-121">Opprette serviceobjekter</span><span class="sxs-lookup"><span data-stu-id="8aa37-121">Create service objects</span></span>](create-service-objects.md)

