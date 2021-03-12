---
title: Konfigurere en kanal for å bruke et kanalnavigasjonshierarki
description: Dette emnet beskriver hvordan du konfigurerer en kanal for å bruke et kanalnavigeringshierarki i Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 3dcba743e6557b1bd366ac79ecb49ead831dceb4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "5001031"
---
# <a name="configure-a-channel-to-use-a-channel-navigation-hierarchy"></a><span data-ttu-id="b7381-103">Konfigurere en kanal for å bruke et kanalnavigasjonshierarki</span><span class="sxs-lookup"><span data-stu-id="b7381-103">Configure a channel to use a channel navigation hierarchy</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="b7381-104">Dette emnet beskriver hvordan du konfigurerer en kanal for å bruke et kanalnavigeringshierarki i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b7381-104">This topic describes how to configure a channel to use a channel navigation hierarchy in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="b7381-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="b7381-105">Overview</span></span>

<span data-ttu-id="b7381-106">Kanalnavigeringshierarkier organiserer produkter i kategorier, slik at produktene kan blas gjennom på et e-handelsområde eller på salgsstedet.</span><span class="sxs-lookup"><span data-stu-id="b7381-106">Channel navigation hierarchies organize products into categories so that the products can be browsed on an e-Commerce site or at points of sale (POS).</span></span> <span data-ttu-id="b7381-107">Detaljhandels- og nettkanaler må konfigureres med kanalnavigeringshierarkier.</span><span class="sxs-lookup"><span data-stu-id="b7381-107">Retail and online channels must be configured with channel navigation hierarchies.</span></span>

## <a name="configure-the-channel"></a><span data-ttu-id="b7381-108">Konfigurere kanalen</span><span class="sxs-lookup"><span data-stu-id="b7381-108">Configure the channel</span></span>

<span data-ttu-id="b7381-109">Følg denne fremgangsmåten for å konfigurere en kanal for å bruke et kanalnavigasjonshierarki:</span><span class="sxs-lookup"><span data-stu-id="b7381-109">To configure a channel to use a channel navigation hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="b7381-110">I navigasjonsruten går du til **Moduler \> Retail og Commerce \> Kanaloppsett \> Kanalkategorier og produktattributter**.</span><span class="sxs-lookup"><span data-stu-id="b7381-110">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Channel categories and product attributes**.</span></span>
1. <span data-ttu-id="b7381-111">Velg kanalen skal konfigureres.</span><span class="sxs-lookup"><span data-stu-id="b7381-111">Select the channel to configure.</span></span>
1. <span data-ttu-id="b7381-112">I handlingsruten velger du **Angi attributtmetadata**.</span><span class="sxs-lookup"><span data-stu-id="b7381-112">On the action pane, select **Set attribute metadata**.</span></span>
1. <span data-ttu-id="b7381-113">I rullegardinlisten **Kategorihierarki** velger du aktuelt kanalnavigeringshierarki.</span><span class="sxs-lookup"><span data-stu-id="b7381-113">In the **Category hierarchy** drop-down list, select the appropriate channel navigation hierarchy.</span></span>
1. <span data-ttu-id="b7381-114">Velg **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="b7381-114">On the action pane, select **Save**.</span></span>
1. <span data-ttu-id="b7381-115">Under **Attributtgruppe** legger du til eventuelle attributtgrupper som skal være globale attributter for alle noder.</span><span class="sxs-lookup"><span data-stu-id="b7381-115">Under **Attribute group**, add any attribute groups that will be global attributes for all nodes.</span></span>

<span data-ttu-id="b7381-116">Følgende bilde viser hvordan du konfigurerer en kanal for å bruke et kanalnavigasjonshierarki:</span><span class="sxs-lookup"><span data-stu-id="b7381-116">The following image shows how to configure a channel to use a channel navigation hierarchy.</span></span>

![Eksempel på kanalkonfigurasjon](media/configure-channel-hierarchy-1.png)

## <a name="set-attribute-metadata"></a><span data-ttu-id="b7381-118">Angi attributtmetadata</span><span class="sxs-lookup"><span data-stu-id="b7381-118">Set attribute metadata</span></span>

<span data-ttu-id="b7381-119">Ved å angi attributtmetadataene kan du konfigurere attributter for hver node.</span><span class="sxs-lookup"><span data-stu-id="b7381-119">Setting the attribute metadata will allow configuration of attributes on each node.</span></span>

<span data-ttu-id="b7381-120">Gjør følgende for å konfigurere attributtmetadata.</span><span class="sxs-lookup"><span data-stu-id="b7381-120">To set attribute metadata, follow these steps.</span></span>

1. <span data-ttu-id="b7381-121">I handlingsruten velger du **Angi attributtmetadata**.</span><span class="sxs-lookup"><span data-stu-id="b7381-121">On the action pane, select **Set attribute metadata**.</span></span>
1. <span data-ttu-id="b7381-122">For hver node velger du **Kanalproduktattributter**.</span><span class="sxs-lookup"><span data-stu-id="b7381-122">For each node select **Channel product attributes**.</span></span>
1. <span data-ttu-id="b7381-123">Sett **Vis attributter i kanal** til **Ja** og **Kan justeres** til **Ja** for å aktivere presiseringer i denne kanalen.</span><span class="sxs-lookup"><span data-stu-id="b7381-123">Set **Show attribute on channel** to **Yes** and **Can be refined** to **Yes**, to enable refiners on that channel.</span></span>
1. <span data-ttu-id="b7381-124">Når du har konfigurert hver node slik du ønsker, velger du **Lagre**-knappen i **handlingsruten** for å lagre.</span><span class="sxs-lookup"><span data-stu-id="b7381-124">After configuring each node as desired, on the **Action pane**, select the **Save** button to save.</span></span>
1. <span data-ttu-id="b7381-125">Velg **X** i øvre høyre hjørne for å avslutte dette skjermbildet og tilbake til siden **Kanalkategorier og produktattributter**.</span><span class="sxs-lookup"><span data-stu-id="b7381-125">Select the **X** in the top right corner to exit this screen back to the **Channel categories and product attributes** page.</span></span>

<span data-ttu-id="b7381-126">Følgende bilde viser et eksempelsett med kanalproduktattributter konfigurert på en kanalkategorinode.</span><span class="sxs-lookup"><span data-stu-id="b7381-126">The following image shows an example set of channel product attributes configured on a channel category node.</span></span>

![Kanalattributter på en kanalkategorinode](media/configure-channel-hierarchy-2.png)

## <a name="publish-changes"></a><span data-ttu-id="b7381-128">Publisere endringer</span><span class="sxs-lookup"><span data-stu-id="b7381-128">Publish changes</span></span>

<span data-ttu-id="b7381-129">Før endringene kan tre i kraft, må du publisere endringene.</span><span class="sxs-lookup"><span data-stu-id="b7381-129">For changes to take effect, you will need to publish the changes.</span></span>

<span data-ttu-id="b7381-130">Hvis du vil publisere endringer, gjør du følgende.</span><span class="sxs-lookup"><span data-stu-id="b7381-130">To publish changes, follow these steps.</span></span>

1. <span data-ttu-id="b7381-131">Velg **Publiser kanaloppdateringer** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="b7381-131">On the action pane, select **Publish channel updates**.</span></span>
1. <span data-ttu-id="b7381-132">Velg **OK** i **Publiser kanaloppdateringer**.</span><span class="sxs-lookup"><span data-stu-id="b7381-132">In the **Publish channel updates** pane, select **OK**.</span></span>

<span data-ttu-id="b7381-133">Bildet nedenfor viser hvordan du publiserer kanaloppdateringer.</span><span class="sxs-lookup"><span data-stu-id="b7381-133">The following image shows how to publish channel updates.</span></span>

![Publiser kanaloppdateringer](media/configure-channel-hierarchy-3.png)

## <a name="additional-resources"></a><span data-ttu-id="b7381-135">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="b7381-135">Additional resources</span></span>

[<span data-ttu-id="b7381-136">Opprette et kanalnavigasjonshierarki</span><span class="sxs-lookup"><span data-stu-id="b7381-136">Create a channel navigation hierarchy</span></span>](create-channel-hierarchy.md)


