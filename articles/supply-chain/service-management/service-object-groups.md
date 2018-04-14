---
title: Serviceobjektgrupper
description: "Objektgrupper er nyttige for å kunne sortere og filtrere data til bruk i rapporter og statistikk."
author: YuyuScheller
manager: AnnBe
ms.date: 02/21/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceObjectGroups
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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: e539d92753bbbc4ac0ca88cec83c4d15135c388b
ms.contentlocale: nb-no
ms.lasthandoff: 04/13/2018

---

# <a name="service-object-groups"></a><span data-ttu-id="15976-103">Serviceobjektgrupper</span><span class="sxs-lookup"><span data-stu-id="15976-103">Service object groups</span></span> 

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="15976-104">Objektgrupper er nyttige for å kunne sortere og filtrere data til bruk i rapporter og statistikk.</span><span class="sxs-lookup"><span data-stu-id="15976-104">Object groups are useful for sorting and filtering the data about objects for reports and statistics.</span></span> <span data-ttu-id="15976-105">Du kan for eksempel gruppere objekter etter geografisk plassering eller etter type.</span><span class="sxs-lookup"><span data-stu-id="15976-105">For example, you can group objects by geographical location or by type.</span></span>

## <a name="group-by-geographical-location"></a><span data-ttu-id="15976-106">Grupper etter geografisk plassering</span><span class="sxs-lookup"><span data-stu-id="15976-106">Group by geographical location</span></span>

<span data-ttu-id="15976-107">Du kan bruke denne grupperingsmetoden for å vise hvor de ulike objektene som firmaet utfører tjenester for, befinner seg.</span><span class="sxs-lookup"><span data-stu-id="15976-107">You can use this grouping method to show where the various different objects that your company services are located.</span></span> <span data-ttu-id="15976-108">Gruppering av objekter etter geografisk plassering kan også være nyttig hvis du for eksempel må identifisere objektene som firmaet allerede utfører tjenester for, i et bestemt land eller område.</span><span class="sxs-lookup"><span data-stu-id="15976-108">Grouping objects by geographical location can also be useful if, for example, you must identify the objects that your company already provides services for in a particular country/region.</span></span>

## <a name="example"></a><span data-ttu-id="15976-109">Eksempel</span><span class="sxs-lookup"><span data-stu-id="15976-109">Example</span></span>

<span data-ttu-id="15976-110">En kunde fra Belgia ringer ditt servicecenter og vil opprette en en serviceavtale for et objekt, ABC.</span><span class="sxs-lookup"><span data-stu-id="15976-110">A customer from Belgium calls your service center and wants to create a service agreement for an object, ABC.</span></span> <span data-ttu-id="15976-111">Du har tilknyttet en objektgruppe for geografisk plassering, Belgia, til alle objekter som betjenes i Belgia.</span><span class="sxs-lookup"><span data-stu-id="15976-111">You have attached an object group for geographical location, Belgium, to all objects that are serviced in Belgium.</span></span> <span data-ttu-id="15976-112">Ved å bruke denne gruppen som et filter, kan du raskt søke for å se om du allerede har en post for ABC i programmet ditt, eller om du må definere et nytt objekt.</span><span class="sxs-lookup"><span data-stu-id="15976-112">By using this group as a filter, you can quickly search to see whether you already have a record for ABC in the program, or whether you must set up a new object.</span></span> 

## <a name="group-by-type"></a><span data-ttu-id="15976-113">Grupper etter type</span><span class="sxs-lookup"><span data-stu-id="15976-113">Group by type</span></span>

<span data-ttu-id="15976-114">Du kan bruke denne grupperingsmetoden for å vise hvilke typer av objekter firmaet ditt utfører tjenester for.</span><span class="sxs-lookup"><span data-stu-id="15976-114">You can use this grouping method to show the types of objects that your company services.</span></span> <span data-ttu-id="15976-115">Gruppering av objekter etter type kan også være nyttig hvis du for eksempel vil opprette et nytt objekt basert på liknende objekter som allerede finnes i programmet.</span><span class="sxs-lookup"><span data-stu-id="15976-115">Grouping objects by type can also be useful if, for example, you want to create a new object based on similar objects that already exist in the program.</span></span>

## <a name="example"></a><span data-ttu-id="15976-116">Eksempel</span><span class="sxs-lookup"><span data-stu-id="15976-116">Example</span></span>

<span data-ttu-id="15976-117">En kunde ringer og vil opprette en serviceavtale for en luftkondisjoneringsmaskin, HIJ.</span><span class="sxs-lookup"><span data-stu-id="15976-117">A customer calls and wants to set up a service agreement for an air conditioning machine, HIJ.</span></span> <span data-ttu-id="15976-118">Du har ikke allerede en oppføring for denne maskinen.</span><span class="sxs-lookup"><span data-stu-id="15976-118">You do not already have a record for this machine.</span></span> <span data-ttu-id="15976-119">Men du har satt opp en objektgruppe som heter Luftkondisjonering, og du har knyttet denne gruppen til alle luftkondisjoneringsobjekter.</span><span class="sxs-lookup"><span data-stu-id="15976-119">However, you have set up an object group titled Air Conditioners, and you have attached this group to all air conditioning objects.</span></span> <span data-ttu-id="15976-120">Derfor kan du raskt søke etter og identifisere alle andre luftkondisjoneringsmaskiner og bruke malinformasjonen fra disse objektene til å opprette serviceavtalelinjer for HIJ.</span><span class="sxs-lookup"><span data-stu-id="15976-120">Therefore, you can quickly search for and identify all other air conditioning machines and use the template information from these objects to create service agreement lines for HIJ.</span></span> <span data-ttu-id="15976-121">Ved å bruke objektgrupper på denne måten, kan du raskt definere nye objekter og avgjøre hvilke serviceoppgaver som må utføres på dem.</span><span class="sxs-lookup"><span data-stu-id="15976-121">By using object groups in this manner, you can quickly set up new objects and determine the service tasks that must be performed on them.</span></span> 




