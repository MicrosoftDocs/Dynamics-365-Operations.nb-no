---
title: Oversikt over kanaler
description: Dette emnet viser en oversikt over kanaler i Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 099ccd9f769ea5c431c1a82532d8654cbbd082b1
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002364"
---
# <a name="channels-overview"></a><span data-ttu-id="1369f-103">Oversikt over kanaler</span><span class="sxs-lookup"><span data-stu-id="1369f-103">Channels overview</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="1369f-104">Dette emnet viser en oversikt over kanaler i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="1369f-104">This topic presents an overview of channels in Microsoft Dynamics 365 Commerce.</span></span> <span data-ttu-id="1369f-105">Den inneholder informasjon om oppgavene du må fullføre både før og etter at du har definert hver kanal.</span><span class="sxs-lookup"><span data-stu-id="1369f-105">It includes information about the tasks that you must complete both before and after you set up each channel.</span></span>

## <a name="types-of-channels"></a><span data-ttu-id="1369f-106">Typer kanaler</span><span class="sxs-lookup"><span data-stu-id="1369f-106">Types of Channels</span></span>

<span data-ttu-id="1369f-107">Dynamics 365 Commerce støtter tre ulike kanaltyper: detaljhandel, telefonsenter og Internett-kanaler.</span><span class="sxs-lookup"><span data-stu-id="1369f-107">Dynamics 365 Commerce supports three different channel types: retail, call center, and online channels.</span></span>

### <a name="retail-channels"></a><span data-ttu-id="1369f-108">Detaljhandelskanaler</span><span class="sxs-lookup"><span data-stu-id="1369f-108">Retail channels</span></span>

<span data-ttu-id="1369f-109">Detaljhandelskanaler representerer standard fysiske butikker.</span><span class="sxs-lookup"><span data-stu-id="1369f-109">Retail channels represent standard brick-and-mortar stores.</span></span> <span data-ttu-id="1369f-110">Hver detaljhandelsbutikk kan ha sine egne salgsstedsregistre, inntekts- og utgiftskontoer og ansatte.</span><span class="sxs-lookup"><span data-stu-id="1369f-110">Each store can have its own point of sale (POS) registers, income and expense accounts, and staff.</span></span> 

### <a name="call-center-channels"></a><span data-ttu-id="1369f-111">Telefonsenterkanaler</span><span class="sxs-lookup"><span data-stu-id="1369f-111">Call center channels</span></span>

<span data-ttu-id="1369f-112">Telefonsenterkanaler representerer ordre- og kundestyring i et telefonsenter.</span><span class="sxs-lookup"><span data-stu-id="1369f-112">Call center channels represent call center order and customer management.</span></span>

### <a name="online-channels"></a><span data-ttu-id="1369f-113">Internett-kanaler</span><span class="sxs-lookup"><span data-stu-id="1369f-113">Online channels</span></span>

<span data-ttu-id="1369f-114">Internett-kanaler representerer butikkfasader for e-handel på nettet.</span><span class="sxs-lookup"><span data-stu-id="1369f-114">Online channels represent online e-Commerce storefronts.</span></span> <span data-ttu-id="1369f-115">Når en Internett-kanal er opprettet, må det opprettes et område ved hjelp av Microsoft Dynamics 365 Commerce-områdebygger eller en annen tredjepartsløsning for e-handel.</span><span class="sxs-lookup"><span data-stu-id="1369f-115">Once an online channel is created, a site must be created using the Microsoft Dynamics 365 Commerce Site Builder tool or other third-party e-Commerce solution.</span></span>

## <a name="channel-setup-basics"></a><span data-ttu-id="1369f-116">Grunnleggende om kanaloppsett</span><span class="sxs-lookup"><span data-stu-id="1369f-116">Channel setup basics</span></span>

<span data-ttu-id="1369f-117">Kanaloppsett utføres i Commerce-verktøyet.</span><span class="sxs-lookup"><span data-stu-id="1369f-117">Channel set up is performed in the Commerce tool.</span></span> <span data-ttu-id="1369f-118">Hver kanal kan ha sine egne betalingsmåter, prisgrupper, produkthierarkier, sortimenter og produktsett.</span><span class="sxs-lookup"><span data-stu-id="1369f-118">Each channel can have its own payment methods, price groups, product hierarchies, assortments, and set of products.</span></span> <span data-ttu-id="1369f-119">Når du har opprettet en kanal, tilordner du produktene du vil den skal føre og selge.</span><span class="sxs-lookup"><span data-stu-id="1369f-119">After you create a channel, you assign the products that you want it to carry and sell.</span></span> <span data-ttu-id="1369f-120">Hver kanaltype har et unikt sett av funksjoner som kanskje må konfigureres.</span><span class="sxs-lookup"><span data-stu-id="1369f-120">Each channel type has a unique set of features that may need to be configured.</span></span> <span data-ttu-id="1369f-121">En detaljhandelskanal trenger for eksempel tilordnede ansatte, journaler og kunder.</span><span class="sxs-lookup"><span data-stu-id="1369f-121">For example, a retail channel needs assigned employees, registers, and customers.</span></span> <span data-ttu-id="1369f-122">Når en ny kanal er opprettet, må den tilordnes et organisasjonshierarki.</span><span class="sxs-lookup"><span data-stu-id="1369f-122">Once a new channel is created, it needs to be assigned to an organization hierarchy.</span></span>

## <a name="channel-setup-prerequisites"></a><span data-ttu-id="1369f-123">Forutsetninger for kanaloppsett</span><span class="sxs-lookup"><span data-stu-id="1369f-123">Channel setup prerequisites</span></span>

<span data-ttu-id="1369f-124">Før du kan definere en kanal, må du fullføre noen nødvendige oppgaver basert på kanaltypen.</span><span class="sxs-lookup"><span data-stu-id="1369f-124">Before you can set up a channel, you must complete some prerequisite tasks based on the channel type.</span></span> <span data-ttu-id="1369f-125">Hvis du vil ha mer informasjon, kan du se [Forutsetninger for kanaloppsett](channels-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="1369f-125">For more information, see [Channel setup prerequisites](channels-prerequisites.md).</span></span>

## <a name="set-up-a-channel"></a><span data-ttu-id="1369f-126">Definere en kanal</span><span class="sxs-lookup"><span data-stu-id="1369f-126">Set up a channel</span></span>

<span data-ttu-id="1369f-127">Når du har fullført de nødvendige oppgavene, bruker du følgende koblinger for ytterligere instruksjoner for installasjon.</span><span class="sxs-lookup"><span data-stu-id="1369f-127">After you complete the prerequisite tasks, for further setup instructions, use the following links.</span></span>

- [<span data-ttu-id="1369f-128">Definere en detaljhandelskanal</span><span class="sxs-lookup"><span data-stu-id="1369f-128">Set up a retail channel</span></span>](channel-setup-retail.md)
- [<span data-ttu-id="1369f-129">Definere en telefonsenterkanal</span><span class="sxs-lookup"><span data-stu-id="1369f-129">Set up a call center channel</span></span>](channel-setup-callcenter.md)
- [<span data-ttu-id="1369f-130">Definere en Internett-kanal</span><span class="sxs-lookup"><span data-stu-id="1369f-130">Set up an online channel</span></span>](channel-setup-online.md)

<!--
## Post-channel configuration

After you create a channel, you may need to complete some of the below tasks:

- [Add channel to an organizational hierarchy](add-channel-org-hierarchy.md)
- Set up fulfillment groups. (LINK TBD)
- Configure the POS registers for the store. (LINK TBD)
- Assign product assortments to the store. (LINK TBD)
- Process assortments to generate the list of products that are included in the assortment and to make the products available in the retail store. (LINK TBD)
- Send data such as number sequences, hardware profiles, and POS screen layouts to the Retail POS registers.(LINK TBD)
- Publish the retail store to send store data to Retail POS. (LINK TBD)
- Run the jobs to send the store data to Retail POS. (LINK TBD)
-->

## <a name="additional-resources"></a><span data-ttu-id="1369f-131">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="1369f-131">Additional resources</span></span>

[<span data-ttu-id="1369f-132">Forutsetninger for kanaloppsett</span><span class="sxs-lookup"><span data-stu-id="1369f-132">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="1369f-133">Definere en detaljhandelskanal</span><span class="sxs-lookup"><span data-stu-id="1369f-133">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="1369f-134">Definere en Internett-kanal</span><span class="sxs-lookup"><span data-stu-id="1369f-134">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="1369f-135">Definere en telefonsenterkanal</span><span class="sxs-lookup"><span data-stu-id="1369f-135">Set up a call center channel</span></span>](channel-setup-callcenter.md)

[<span data-ttu-id="1369f-136">Definere organisasjonshierarkier</span><span class="sxs-lookup"><span data-stu-id="1369f-136">Set up organization hierarchies</span></span>](channels-org-hierarchies.md)