---
title: Scenarier som støttes for oppsett av dobbel skriving
description: Dette emnet beskriver scenariene som støttes for oppsett av dobbel skriving.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 08/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: b4f69e7933bc5a50cccad6911c99cf08d2768578
ms.sourcegitcommit: b3df62842e62234e8eaa16992375582518976131
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/17/2020
ms.locfileid: "3818602"
---
# <a name="supported-scenarios-for-dual-write-setup"></a><span data-ttu-id="f1b58-103">Scenarier som støttes for oppsett av dobbel skriving</span><span class="sxs-lookup"><span data-stu-id="f1b58-103">Supported scenarios for dual-write setup</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="f1b58-104">Du kan opprette en dobbelt skrive-tilkobling mellom et Finance and Operations-miljø og et Common Data Service-miljø.</span><span class="sxs-lookup"><span data-stu-id="f1b58-104">You can set up a dual-write connection between a Finance and Operations environment and a Common Data Service environment.</span></span>

+ <span data-ttu-id="f1b58-105">Et **Finance and Operations-miljø** gir den underliggende plattformen for **Finance and Operations-apper** (for eksempel Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management og Dynamics 365 Retail).</span><span class="sxs-lookup"><span data-stu-id="f1b58-105">A **Finance and Operations environment** provides the underlying platform for **Finance and Operations apps** (for example, Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, and Dynamics 365 Retail).</span></span>
+ <span data-ttu-id="f1b58-106">Et **Common Data Service-miljø** gir den underliggende plattformen for **modelldrevne apper i Dynamics 365** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 Field Service, Dynamics 365 Marketing og Dynamics 365 Project Service Automation).</span><span class="sxs-lookup"><span data-stu-id="f1b58-106">A **Common Data Service environment** provides the underlying platform for **model-driven apps in Dynamics 365** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 Field Service, Dynamics 365 Marketing, and Dynamics 365 Project Service Automation).</span></span>

>[!IMPORTANT]
><span data-ttu-id="f1b58-107">Human Resources i Finance and Operations støtter tilkoblinger med dobbel skriving, men Dynamics 365 Human Resources-appen gjør ikke det.</span><span class="sxs-lookup"><span data-stu-id="f1b58-107">Human Resources in Finance and Operations supports dual-write connections, but the Dynamics 365 Human Resources app doesn't.</span></span>

<span data-ttu-id="f1b58-108">Installasjonsmekanismen varierer, avhengig av abonnementet og miljøet.</span><span class="sxs-lookup"><span data-stu-id="f1b58-108">The setup mechanism varies, depending on your subscription and the environment.</span></span>

+ <span data-ttu-id="f1b58-109">Når det gjelder nye forekomster av Finance and Operations-apper, begynner oppsettet av en tilkobling med dobbel skriving i Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="f1b58-109">For new instances of Finance and Operations apps, the setup of a dual-write connection begins in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="f1b58-110">Hvis du har en lisens for Power Platform, vil du få et nytt Common Data Service-miljø hvis leieren din ikke har et.</span><span class="sxs-lookup"><span data-stu-id="f1b58-110">If you have a license for Power Platform, you will get a new Common Data Service environment if your tenant doesn't have one.</span></span>
+ <span data-ttu-id="f1b58-111">For eksisterende forekomster av Finance and Operations-apper begynner oppsettet av en tilkobling med dobbel skriving i Finance and Operations-miljøet.</span><span class="sxs-lookup"><span data-stu-id="f1b58-111">For existing instances Finance and Operations apps, the setup of a dual-write connection begins in the Finance and Operations environment.</span></span>

<span data-ttu-id="f1b58-112">Følgende oppsettscenarier støttes:</span><span class="sxs-lookup"><span data-stu-id="f1b58-112">The following setup scenarios are supported:</span></span>

+ [<span data-ttu-id="f1b58-113">En ny Finance and Operations-appforekomst og en ny modelldrevet appforekomst</span><span class="sxs-lookup"><span data-stu-id="f1b58-113">A new Finance and Operations app instance and a new model-driven app instance</span></span>](#new-new)
+ [<span data-ttu-id="f1b58-114">En ny Finance and Operations-appforekomst og en eksisterende modelldrevet appforekomst</span><span class="sxs-lookup"><span data-stu-id="f1b58-114">A new Finance and Operations app instance and an existing model-driven app instance</span></span>](#new-existing)
+ [<span data-ttu-id="f1b58-115">En ny Finance and Operations-appforekomst som har demodata og en ny modelldrevet appforekomst</span><span class="sxs-lookup"><span data-stu-id="f1b58-115">A new Finance and Operations app instance that has demo data and a new model-driven app instance</span></span>](#new-demo-new)
+ [<span data-ttu-id="f1b58-116">En ny Finance and Operations-appforekomst som har demodata og en eksisterende modelldrevet appforekomst</span><span class="sxs-lookup"><span data-stu-id="f1b58-116">A new Finance and Operations app instance that has demo data and an existing model-driven app instance</span></span>](#new-demo-existing)
+ [<span data-ttu-id="f1b58-117">En eksisterende Finance and Operations-appforekomst og en ny eller eksisterende modelldrevet appforekomst</span><span class="sxs-lookup"><span data-stu-id="f1b58-117">An existing Finance and Operations app instance and a new or existing model-driven app instance</span></span>](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-model-driven-app-instance"></a><a id="new-new"></a><span data-ttu-id="f1b58-118">En ny Finance and Operations-appforekomst og en ny modelldrevet appforekomst</span><span class="sxs-lookup"><span data-stu-id="f1b58-118">A new Finance and Operations app instance and a new model-driven app instance</span></span>

<span data-ttu-id="f1b58-119">Hvis du vil konfigurere en dobbel skriving-tilkobling mellom en ny forekomst av en Finance and Operations-app som ikke har noen data, og en ny forekomst av en modelldrevet app i Dynamics 365, følger du fremgangsmåten i [Oppsett av dobbel skriving fra Lifecycle Services](lcs-setup.md).</span><span class="sxs-lookup"><span data-stu-id="f1b58-119">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and a new instance of a model-driven app in Dynamics 365, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="f1b58-120">Når tilkoblingsoppsettet er fullført, skjer følgende handlinger automatisk:</span><span class="sxs-lookup"><span data-stu-id="f1b58-120">When the connection setup is completed, the following actions occur automatically:</span></span>

- <span data-ttu-id="f1b58-121">Et nytt, tomt Finance and Operations-miljø er klargjort.</span><span class="sxs-lookup"><span data-stu-id="f1b58-121">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="f1b58-122">En ny, tom forekomst av en modelldrevet app er klargjort, der CRM-hovedløsningen er installert.</span><span class="sxs-lookup"><span data-stu-id="f1b58-122">A new, empty instance of a model-driven app is provisioned, where the CRM prime solution is installed.</span></span>
- <span data-ttu-id="f1b58-123">Det opprettes en dobbel skriving-tilkobling for DAT-firmadata.</span><span class="sxs-lookup"><span data-stu-id="f1b58-123">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="f1b58-124">Enhetstilordninger er aktivert for direkte synkronisering.</span><span class="sxs-lookup"><span data-stu-id="f1b58-124">Entity maps are enabled for live synchronization.</span></span>

<span data-ttu-id="f1b58-125">Begge miljøene er så klare for direkte synkronisering av data.</span><span class="sxs-lookup"><span data-stu-id="f1b58-125">Both environments are then ready for live data synchronization.</span></span>

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-model-driven-app-instance"></a><a id="new-existing"></a><span data-ttu-id="f1b58-126">En ny Finance and Operations-appforekomst og en eksisterende modelldrevet appforekomst</span><span class="sxs-lookup"><span data-stu-id="f1b58-126">A new Finance and Operations app instance and an existing model-driven app instance</span></span>

<span data-ttu-id="f1b58-127">Hvis du vil konfigurere en dobbel skriving-tilkobling mellom en ny forekomst av en Finance and Operations-app som ikke har noen data, og en eksisterende forekomst av en modelldrevet app i Dynamics 365, følger du fremgangsmåten i [Oppsett av dobbel skriving fra Lifecycle Services](lcs-setup.md).</span><span class="sxs-lookup"><span data-stu-id="f1b58-127">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and an existing instance of a model-driven app in Dynamics 365, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="f1b58-128">Når tilkoblingsoppsettet er fullført, skjer følgende handlinger automatisk:</span><span class="sxs-lookup"><span data-stu-id="f1b58-128">When the connection setup is completed, the following actions occur automatically:</span></span>

- <span data-ttu-id="f1b58-129">Et nytt, tomt Finance and Operations-miljø er klargjort.</span><span class="sxs-lookup"><span data-stu-id="f1b58-129">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="f1b58-130">Det opprettes en dobbel skriving-tilkobling for DAT-firmadata.</span><span class="sxs-lookup"><span data-stu-id="f1b58-130">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="f1b58-131">Enhetstilordninger er aktivert for direkte synkronisering.</span><span class="sxs-lookup"><span data-stu-id="f1b58-131">Entity maps are enabled for live synchronization.</span></span>

<span data-ttu-id="f1b58-132">Begge miljøene er så klare for direkte synkronisering av data.</span><span class="sxs-lookup"><span data-stu-id="f1b58-132">Both environments are then ready for live data synchronization.</span></span>

<span data-ttu-id="f1b58-133">Følg denne fremgangsmåten for å synkronisere de eksisterende Common Data Service-dataene med Finance and Operations-appen.</span><span class="sxs-lookup"><span data-stu-id="f1b58-133">To sync the existing Common Data Service data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="f1b58-134">Opprette et nytt firma i Finance and Operations-appen.</span><span class="sxs-lookup"><span data-stu-id="f1b58-134">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="f1b58-135">Legg til firmaet i oppsettet for dobbelt skriving-tilkobling.</span><span class="sxs-lookup"><span data-stu-id="f1b58-135">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="f1b58-136">[Starte opp](bootstrap-company-data.md) Common Data Service-dataene ved hjelp av en ISO-firmakode (International Organization for Standardization) på tre tegn.</span><span class="sxs-lookup"><span data-stu-id="f1b58-136">[Bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter International Organization for Standardization (ISO) company code.</span></span>

<span data-ttu-id="f1b58-137">Fordi dobbel skriving er i modus for direkte synkronisering, begynner dataene fra Common Data Service å strømme til Finance and Operations-appen automatisk.</span><span class="sxs-lookup"><span data-stu-id="f1b58-137">Because dual-write is in live synchronization mode, the data from Common Data Service automatically starts to flow to the Finance and Operations app.</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-demo-data-and-a-new-model-driven-app-instance"></a><a id="new-demo-new"></a><span data-ttu-id="f1b58-138">En ny Finance and Operations-appforekomst som har demodata og en ny modelldrevet appforekomst</span><span class="sxs-lookup"><span data-stu-id="f1b58-138">A new Finance and Operations app instance that has demo data and a new model-driven app instance</span></span>

<span data-ttu-id="f1b58-139">Hvis du vil konfigurere en dobbel skriving-tilkobling mellom en ny forekomst av en Finance and Operations-app som har demodata og en ny forekomst av en modelldrevet app i Dynamics 365, følger du fremgangsmåten i delen [En ny Finance and Operations-appforekomst og en ny modelldrevet appforekomst](#new-new) tidligere i dette emnet.</span><span class="sxs-lookup"><span data-stu-id="f1b58-139">To set up a dual-write connection between a new instance of a Finance and Operations app that has demo data and a new instance of a model-driven app in Dynamics 365, follow the steps in the [A new Finance and Operations app instance and a new model-driven app instance](#new-new) section earlier in this topic.</span></span> <span data-ttu-id="f1b58-140">Når tilkoblingsoppsettet er fullført, følger du denne fremgangsmåten hvis du vil synkronisere demonstrasjonsdataene med den modelldrevne appen.</span><span class="sxs-lookup"><span data-stu-id="f1b58-140">When the connection setup is completed, if you want to sync the demo data to the model-driven app, follow these steps.</span></span>

1. <span data-ttu-id="f1b58-141">Åpne Finance and Operations-appen fra LCS-siden, logg på og gå til **Databehandling \> Dobbel skriving**.</span><span class="sxs-lookup"><span data-stu-id="f1b58-141">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="f1b58-142">Kjør **Innledende synkronisering**-funksjonaliteten for enhetene du vil synkronisere data for.</span><span class="sxs-lookup"><span data-stu-id="f1b58-142">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-demo-data-and-an-existing-model-driven-app-instance"></a><span data-ttu-id="f1b58-143">E<a id="new-demo-existing"></a>En ny Finance and Operations-appforekomst som har demodata og en eksisterende modelldrevet appforekomst</span><span class="sxs-lookup"><span data-stu-id="f1b58-143"><a id="new-demo-existing"></a>A new Finance and Operations app instance that has demo data and an existing model-driven app instance</span></span>

<span data-ttu-id="f1b58-144">Hvis du vil konfigurere en dobbel skriving-tilkobling mellom en ny forekomst av en Finance and Operations-app som har en eksisterende forekomst av en modelldrevet app i Dynamics 365, følger du fremgangsmåten i delen [En ny Finance and Operations-appforekomst og en eksisterende modelldrevet appforekomst](#new-existing) tidligere i dette emnet.</span><span class="sxs-lookup"><span data-stu-id="f1b58-144">To set up a dual-write connection between a new instance of a Finance and Operations app that has demo data and an existing instance of a model-driven app in Dynamics 365, follow the steps in the [A new Finance and Operations app instance and an existing model-driven app instance](#new-existing) section earlier in this topic.</span></span> <span data-ttu-id="f1b58-145">Når tilkoblingsoppsettet er fullført, følger du denne fremgangsmåten hvis du vil synkronisere demonstrasjonsdataene med den modelldrevne appen.</span><span class="sxs-lookup"><span data-stu-id="f1b58-145">When the connection setup is completed, if you want to sync the demo data to the model-driven app, follow these steps.</span></span>

1. <span data-ttu-id="f1b58-146">Åpne Finance and Operations-appen fra LCS-siden, logg på og gå til **Databehandling \> Dobbel skriving**.</span><span class="sxs-lookup"><span data-stu-id="f1b58-146">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="f1b58-147">Kjør **Innledende synkronisering**-funksjonaliteten for enhetene du vil synkronisere data for.</span><span class="sxs-lookup"><span data-stu-id="f1b58-147">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

<span data-ttu-id="f1b58-148">Følg denne fremgangsmåten for å synkronisere de eksisterende Common Data Service-dataene med Finance and Operations-appen.</span><span class="sxs-lookup"><span data-stu-id="f1b58-148">To sync the existing Common Data Service data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="f1b58-149">Opprette et nytt firma i Finance and Operations-appen.</span><span class="sxs-lookup"><span data-stu-id="f1b58-149">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="f1b58-150">Legg til firmaet i oppsettet for dobbelt skriving-tilkobling.</span><span class="sxs-lookup"><span data-stu-id="f1b58-150">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="f1b58-151">[Starte opp](bootstrap-company-data.md) Common Data Service-dataene ved hjelp av en ISO-firmakode på tre tegn.</span><span class="sxs-lookup"><span data-stu-id="f1b58-151">[Bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter ISO company code.</span></span>

<span data-ttu-id="f1b58-152">Fordi dobbel skriving er i modus for direkte synkronisering, begynner dataene fra Common Data Service å strømme til Finance and Operations-appen automatisk.</span><span class="sxs-lookup"><span data-stu-id="f1b58-152">Because dual-write is in live synchronization mode, the data from Common Data Service automatically starts to flow to the Finance and Operations app.</span></span>

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-or-existing-model-driven-app-instance"></a><a id="existing-existing"></a><span data-ttu-id="f1b58-153">En eksisterende Finance and Operations-appforekomst og en ny eller eksisterende modelldrevet appforekomst</span><span class="sxs-lookup"><span data-stu-id="f1b58-153">An existing Finance and Operations app instance and a new or existing model-driven app instance</span></span>

<span data-ttu-id="f1b58-154">Oppsettet av en dobbel skriving-tilkobling mellom en eksisterende forekomst av en Finance and Operations-app og en ny eller eksisterende forekomst av en modelldrevet app i Dynamics 365 forekommer i Finance and Operation-miljøet.</span><span class="sxs-lookup"><span data-stu-id="f1b58-154">The setup of a dual-write connection between an existing instance of a Finance and Operations app and a new or existing instance of a model-driven app in Dynamics 365 occurs in the Finance and Operation environment.</span></span>

1. <span data-ttu-id="f1b58-155">Angi tilkoblingen fra Finance and Operations-appen.</span><span class="sxs-lookup"><span data-stu-id="f1b58-155">Set up the connection from the Finance and Operations app.</span></span>
2. <span data-ttu-id="f1b58-156">Hvis du vil synkronisere de eksisterende Common Data Service-dataene til Finance and Operations-appen, [starter du opp](bootstrap-company-data.md) Common Data Service-dataene ved hjelp av en ISO-firmakode på tre bokstaver.</span><span class="sxs-lookup"><span data-stu-id="f1b58-156">To sync the existing Common Data Service data to the Finance and Operations app, [bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter ISO company code.</span></span>

<span data-ttu-id="f1b58-157">Fordi dobbel skriving er i modus for direkte synkronisering, begynner dataene fra Common Data Service å strømme til Finance and Operations-appen automatisk.</span><span class="sxs-lookup"><span data-stu-id="f1b58-157">Because dual-write is in live synchronization mode, the data from Common Data Service automatically starts to flow to the Finance and Operations app.</span></span>
