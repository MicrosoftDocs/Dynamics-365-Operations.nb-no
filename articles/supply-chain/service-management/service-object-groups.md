---
title: Serviceobjektgrupper
description: "Objektgrupper er nyttige for å kunne sortere og filtrere data til bruk i rapporter og statistikk."
author: ShylaThompson
manager: AnnBe
ms.date: 05/11/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceObjectGroups
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: bc5b1bf93deaf60a3c6384671ad575c73871eb35
ms.contentlocale: nb-no
ms.lasthandoff: 08/07/2018

---

# <a name="service-object-groups"></a><span data-ttu-id="a4c94-103">Serviceobjektgrupper</span><span class="sxs-lookup"><span data-stu-id="a4c94-103">Service object groups</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a4c94-104">Objektgrupper er nyttige for å kunne sortere og filtrere data til bruk i rapporter og statistikk.</span><span class="sxs-lookup"><span data-stu-id="a4c94-104">Object groups are useful for sorting and filtering the data about objects for reports and statistics.</span></span> <span data-ttu-id="a4c94-105">Du kan for eksempel gruppere objekter etter geografisk plassering eller etter type.</span><span class="sxs-lookup"><span data-stu-id="a4c94-105">For example, you can group objects by geographical location or by type.</span></span>

## <a name="group-by-geographical-location"></a><span data-ttu-id="a4c94-106">Grupper etter geografisk plassering</span><span class="sxs-lookup"><span data-stu-id="a4c94-106">Group by geographical location</span></span>

<span data-ttu-id="a4c94-107">Du kan bruke denne grupperingsmetoden for å vise hvor de ulike objektene som firmaet utfører tjenester for, befinner seg.</span><span class="sxs-lookup"><span data-stu-id="a4c94-107">You can use this grouping method to show where the various different objects that your company services are located.</span></span> <span data-ttu-id="a4c94-108">Gruppering av objekter etter geografisk plassering kan også være nyttig hvis du for eksempel må identifisere objektene som firmaet allerede utfører tjenester for, i et bestemt land eller område.</span><span class="sxs-lookup"><span data-stu-id="a4c94-108">Grouping objects by geographical location can also be useful if, for example, you must identify the objects that your company already provides services for in a particular country/region.</span></span>

## <a name="example"></a><span data-ttu-id="a4c94-109">Eksempel</span><span class="sxs-lookup"><span data-stu-id="a4c94-109">Example</span></span>

<span data-ttu-id="a4c94-110">En kunde fra Belgia ringer ditt servicecenter og vil opprette en en serviceavtale for et objekt, ABC.</span><span class="sxs-lookup"><span data-stu-id="a4c94-110">A customer from Belgium calls your service center and wants to create a service agreement for an object, ABC.</span></span> <span data-ttu-id="a4c94-111">Du har tilknyttet en objektgruppe for geografisk plassering, Belgia, til alle objekter som betjenes i Belgia.</span><span class="sxs-lookup"><span data-stu-id="a4c94-111">You have attached an object group for geographical location, Belgium, to all objects that are serviced in Belgium.</span></span> <span data-ttu-id="a4c94-112">Ved å bruke denne gruppen som et filter, kan du raskt søke for å se om du allerede har en post for ABC i programmet ditt, eller om du må definere et nytt objekt.</span><span class="sxs-lookup"><span data-stu-id="a4c94-112">By using this group as a filter, you can quickly search to see whether you already have a record for ABC in the program, or whether you must set up a new object.</span></span> 

## <a name="group-by-type"></a><span data-ttu-id="a4c94-113">Grupper etter type</span><span class="sxs-lookup"><span data-stu-id="a4c94-113">Group by type</span></span>

<span data-ttu-id="a4c94-114">Du kan bruke denne grupperingsmetoden for å vise hvilke typer av objekter firmaet ditt utfører tjenester for.</span><span class="sxs-lookup"><span data-stu-id="a4c94-114">You can use this grouping method to show the types of objects that your company services.</span></span> <span data-ttu-id="a4c94-115">Gruppering av objekter etter type kan også være nyttig hvis du for eksempel vil opprette et nytt objekt basert på liknende objekter som allerede finnes i programmet.</span><span class="sxs-lookup"><span data-stu-id="a4c94-115">Grouping objects by type can also be useful if, for example, you want to create a new object based on similar objects that already exist in the program.</span></span>

## <a name="example"></a><span data-ttu-id="a4c94-116">Eksempel</span><span class="sxs-lookup"><span data-stu-id="a4c94-116">Example</span></span>

<span data-ttu-id="a4c94-117">En kunde ringer og vil opprette en serviceavtale for en luftkondisjoneringsmaskin, HIJ.</span><span class="sxs-lookup"><span data-stu-id="a4c94-117">A customer calls and wants to set up a service agreement for an air conditioning machine, HIJ.</span></span> <span data-ttu-id="a4c94-118">Du har ikke allerede en oppføring for denne maskinen.</span><span class="sxs-lookup"><span data-stu-id="a4c94-118">You do not already have a record for this machine.</span></span> <span data-ttu-id="a4c94-119">Men du har satt opp en objektgruppe som heter Luftkondisjonering, og du har knyttet denne gruppen til alle luftkondisjoneringsobjekter.</span><span class="sxs-lookup"><span data-stu-id="a4c94-119">However, you have set up an object group titled Air Conditioners, and you have attached this group to all air conditioning objects.</span></span> <span data-ttu-id="a4c94-120">Derfor kan du raskt søke etter og identifisere alle andre luftkondisjoneringsmaskiner og bruke malinformasjonen fra disse objektene til å opprette serviceavtalelinjer for HIJ.</span><span class="sxs-lookup"><span data-stu-id="a4c94-120">Therefore, you can quickly search for and identify all other air conditioning machines and use the template information from these objects to create service agreement lines for HIJ.</span></span> <span data-ttu-id="a4c94-121">Ved å bruke objektgrupper på denne måten, kan du raskt definere nye objekter og avgjøre hvilke serviceoppgaver som må utføres på dem.</span><span class="sxs-lookup"><span data-stu-id="a4c94-121">By using object groups in this manner, you can quickly set up new objects and determine the service tasks that must be performed on them.</span></span> 

## <a name="create-service-object-groups"></a><span data-ttu-id="a4c94-122">Opprette serviceobjektgrupper</span><span class="sxs-lookup"><span data-stu-id="a4c94-122">Create service object groups</span></span>

<span data-ttu-id="a4c94-123">Opprett grupper som du kan tilordne serviceobjekter til.</span><span class="sxs-lookup"><span data-stu-id="a4c94-123">Create groups that you can assign service objects to.</span></span> <span data-ttu-id="a4c94-124">Serviceobjekter er lagervarer og andre produkter som det utføres tjenester for.</span><span class="sxs-lookup"><span data-stu-id="a4c94-124">Service objects are inventory items and other products for which services are performed.</span></span> <span data-ttu-id="a4c94-125">Når du grupperer serviceobjekter, kan du opprette rapporter for lignende og relaterte serviceobjekter.</span><span class="sxs-lookup"><span data-stu-id="a4c94-125">By grouping service objects, you can create reports for similar and related service objects.</span></span> <span data-ttu-id="a4c94-126">En serviceobjektgruppe kan for eksempel bestå av to serviceobjekter: ett serviceobjekt er et sett, og det andre serviceobjektet er tjenesten som skal installere settet.</span><span class="sxs-lookup"><span data-stu-id="a4c94-126">For example, a service object group might consist of two service objects: One service object is a kit, and the second service object is the service to install the kit.</span></span>

<span data-ttu-id="a4c94-127">Hvis du vil opprette serviceobjektgrupper, gjør du følgende:</span><span class="sxs-lookup"><span data-stu-id="a4c94-127">To create service object groups, follow these steps:</span></span>

1. <span data-ttu-id="a4c94-128">Klikk **Servicestyring > Oppsett > Serviceobjekter > Serviceobjektgrupper**.</span><span class="sxs-lookup"><span data-stu-id="a4c94-128">Click **Service management > Setup > Service objects > Service object groups**.</span></span>

2. <span data-ttu-id="a4c94-129">Klikk **Ny** for å opprette en ny serviceobjektgruppe.</span><span class="sxs-lookup"><span data-stu-id="a4c94-129">Click **New** to create a new service object group.</span></span>

3. <span data-ttu-id="a4c94-130">Angi et unikt navn for serviceobjektgruppen, og eventuelt en beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="a4c94-130">Enter a unique name for the service object group and, optionally, a description.</span></span>

<span data-ttu-id="a4c94-131">Du kan tilordne serviceobjekter til gruppen ved hjelp av **Serviceobjekter**-skjemaet.</span><span class="sxs-lookup"><span data-stu-id="a4c94-131">You can assign service objects to the group by using the **Service objects** form.</span></span> 

## <a name="see-also"></a><span data-ttu-id="a4c94-132">Se også</span><span class="sxs-lookup"><span data-stu-id="a4c94-132">See also</span></span>

[<span data-ttu-id="a4c94-133">Opprette serviceobjekter</span><span class="sxs-lookup"><span data-stu-id="a4c94-133">Create service objects</span></span>](create-service-objects.md)



