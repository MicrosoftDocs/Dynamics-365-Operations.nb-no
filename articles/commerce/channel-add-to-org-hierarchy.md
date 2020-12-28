---
title: Legge til en kanal i et organisasjonshierarki
description: Dette emnet beskriver hvordan du legger til en kanal i et organisasjonshierarki i Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 701c90e8e28b4419422cddde698e9c9862a588a2
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4414607"
---
# <a name="add-a-channel-to-an-organizational-hierarchy"></a><span data-ttu-id="49aac-103">Legge til en kanal i et organisasjonshierarki</span><span class="sxs-lookup"><span data-stu-id="49aac-103">Add a channel to an organizational hierarchy</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="49aac-104">Dette emnet beskriver hvordan du legger til en kanal i et organisasjonshierarki i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="49aac-104">This topic describes how to add a channel to an organizational hierarchy in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="49aac-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="49aac-105">Overview</span></span>

<span data-ttu-id="49aac-106">Kanaler må knyttes til ett eller flere organisasjonshierarkier.</span><span class="sxs-lookup"><span data-stu-id="49aac-106">Channels need to be associated with one or more organizational hierarchies.</span></span> <span data-ttu-id="49aac-107">Før du oppretter kanaler, må du kontrollere at organisasjonshierarkiene er definert.</span><span class="sxs-lookup"><span data-stu-id="49aac-107">Before creating channels, you need to confirm that your organizational hierarchies have been set up.</span></span>  

<span data-ttu-id="49aac-108">Se [Organisasjonshierarkier](channels-org-hierarchies.md) for mer informasjon om hvordan du oppretter organisasjonshierarkier.</span><span class="sxs-lookup"><span data-stu-id="49aac-108">See [Organizational hierarchies](channels-org-hierarchies.md) for more details on how to create organizational hierarchies.</span></span>

## <a name="select-a-hierarchy"></a><span data-ttu-id="49aac-109">Velge et hierarki</span><span class="sxs-lookup"><span data-stu-id="49aac-109">Select a hierarchy</span></span>

<span data-ttu-id="49aac-110">Følg denne fremgangsmåten for å velge et hierarki.</span><span class="sxs-lookup"><span data-stu-id="49aac-110">To select a hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="49aac-111">I navigasjonsruten går du til **Moduler \> Detaljhandel og handel \> Kanaloppsett \> Organisasjonshierarkier**.</span><span class="sxs-lookup"><span data-stu-id="49aac-111">In the navigation pane, go to **Modules \> Retail and commerce \> Channel Setup \> Organization hierarchies**.</span></span>
1. <span data-ttu-id="49aac-112">Velg organisasjonshierarkiet du vil legge til kanalen i, fra listen.</span><span class="sxs-lookup"><span data-stu-id="49aac-112">From the list, select the organization hierarchy that you'll be adding the channel to.</span></span>
1. <span data-ttu-id="49aac-113">I handlingsruten velger du **Vis** for å vise hierarkidetaljer.</span><span class="sxs-lookup"><span data-stu-id="49aac-113">On the action pane, select **View** to view hierarchy details.</span></span>

<span data-ttu-id="49aac-114">Følgende bilde viser detaljer om organisasjonshierarki for det valgte hierarkiet.</span><span class="sxs-lookup"><span data-stu-id="49aac-114">The following image shows organizational hierarchy details for the selected hierarchy.</span></span>

![Detaljer om organisasjonshierarki for det valgte hierarkiet](media/channel-add-to-org-hierarchy-1.png)

## <a name="add-a-channel-to-a-hierachy-node"></a><span data-ttu-id="49aac-116">Legge til en kanal i en hierarkinode</span><span class="sxs-lookup"><span data-stu-id="49aac-116">Add a channel to a hierachy node</span></span>

<span data-ttu-id="49aac-117">Hvis du vil legge til en kanal i en hierarkinode, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="49aac-117">To add a channel to a hierachy node, follow these steps.</span></span>

1. <span data-ttu-id="49aac-118">I handlingsruten velger du **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="49aac-118">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="49aac-119">Velg hierarkinoden du vil at kanalen skal legges til i, og gå deretter til rullegardinlisten **Sett inn** og velg **Detaljhandelskanal**.</span><span class="sxs-lookup"><span data-stu-id="49aac-119">Select the hierachy node you want the channel added to, then from the **Insert** drop-down list, select **Retail Channel**.</span></span> 
1. <span data-ttu-id="49aac-120">Velg kanalen som skal legges til, og klikk deretter **OK**-knappen.</span><span class="sxs-lookup"><span data-stu-id="49aac-120">Select the channel to add, then select the **OK** button.</span></span>
1. <span data-ttu-id="49aac-121">Velg **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="49aac-121">On the action pane, select **Save**.</span></span>
1. <span data-ttu-id="49aac-122">Velg **Publiser** i handlingsruten, og oppgi en **gyldig dato** i fortiden for at denne handlingen skal tre i kraft umiddelbart.</span><span class="sxs-lookup"><span data-stu-id="49aac-122">On the action pane, select **Publish** and provide an **Effective date** in the past to have this action go into effect immediately.</span></span>

<span data-ttu-id="49aac-123">Bildet nedenfor viser hvordan du velger en kanal som skal legges til i en hierarkinode.</span><span class="sxs-lookup"><span data-stu-id="49aac-123">The following image shows how to select a channel to add to a hierarchy node.</span></span>

![Velge en kanal som skal legges til i en hierarkinode](media/channel-add-to-org-hierarchy-2.png)

<span data-ttu-id="49aac-125">Det følgende bildet viser et hierarki der ulike kanaler er lagt til.</span><span class="sxs-lookup"><span data-stu-id="49aac-125">The following image shows a hierarchy with various channels added.</span></span>

![Et hierarki med ulike kanaler lagt til](media/channel-add-to-org-hierarchy-3.png)

## <a name="additional-resources"></a><span data-ttu-id="49aac-127">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="49aac-127">Additional resources</span></span>

[<span data-ttu-id="49aac-128">Oversikt over kanaler</span><span class="sxs-lookup"><span data-stu-id="49aac-128">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="49aac-129">Forutsetninger for kanaloppsett</span><span class="sxs-lookup"><span data-stu-id="49aac-129">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="49aac-130">Oversikt over organisasjoner og organisasjonshierarkier</span><span class="sxs-lookup"><span data-stu-id="49aac-130">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="49aac-131">Planlegge organisasjonshierarkiet</span><span class="sxs-lookup"><span data-stu-id="49aac-131">Plan your organizational hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="49aac-132">Organisasjonshierarkier</span><span class="sxs-lookup"><span data-stu-id="49aac-132">Organization hierarchies</span></span>](channels-org-hierarchies.md)

[<span data-ttu-id="49aac-133">Definere en detaljhandelskanal</span><span class="sxs-lookup"><span data-stu-id="49aac-133">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="49aac-134">Definere en Internett-kanal</span><span class="sxs-lookup"><span data-stu-id="49aac-134">Set up an online channel</span></span>](channel-setup-online.md)
