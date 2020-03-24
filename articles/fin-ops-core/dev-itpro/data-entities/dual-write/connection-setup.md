---
title: Scenarier som støttes for oppsett av dobbel skriving
description: Dette emnet beskriver scenariene som støttes for oppsett av dobbel skriving.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/06/2020
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
ms.openlocfilehash: 1319f1228b635e207754f7c2516cb2b5353a9edd
ms.sourcegitcommit: 48c39c0c0949fe48b3536d9d2d0e451d561ff5c6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/09/2020
ms.locfileid: "3112493"
---
# <a name="supported-scenarios-for-dual-write-setup"></a><span data-ttu-id="03389-103">Scenarier som støttes for oppsett av dobbel skriving</span><span class="sxs-lookup"><span data-stu-id="03389-103">Supported scenarios for dual-write setup</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="03389-104">Du kan opprette en dobbelt skrive-tilkobling mellom et Finance and Operations-miljø og et Common Data Service-miljø.</span><span class="sxs-lookup"><span data-stu-id="03389-104">You can set up a dual-write connection between a Finance and Operations environment and a Common Data Service environment.</span></span>

+ <span data-ttu-id="03389-105">Et **Finance and Operations-miljø** gir den underliggende plattformen for **Finance and Operations-apper** (for eksempel Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Retail og Dynamics 365 Human Resources).</span><span class="sxs-lookup"><span data-stu-id="03389-105">A **Finance and Operations environment** provides the underlying platform for **Finance and Operations apps** (for example, Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Retail, and Dynamics 365 Human Resources).</span></span>
+ <span data-ttu-id="03389-106">Et **Common Data Service-miljø** gir den underliggende plattformen for **modelldrevne apper i Dynamics 365** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 Field Service, Dynamics 365 Marketing og Dynamics 365 Project Service Automation).</span><span class="sxs-lookup"><span data-stu-id="03389-106">A **Common Data Service environment** provides the underlying platform for **model-driven apps in Dynamics 365** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 Field Service, Dynamics 365 Marketing, and Dynamics 365 Project Service Automation).</span></span>

<span data-ttu-id="03389-107">Installasjonsmekanismen varierer, avhengig av abonnementet og miljøet.</span><span class="sxs-lookup"><span data-stu-id="03389-107">The setup mechanism varies, depending on your subscription and the environment.</span></span>

+ <span data-ttu-id="03389-108">Når det gjelder nye forekomster av Finance and Operations-apper, begynner oppsettet av en tilkobling med dobbel skriving i Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="03389-108">For new instances of Finance and Operations apps, the setup of a dual-write connection begins in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="03389-109">Hvis du har en lisens for Microsoft Power Platform, vil du få et nytt Common Data Service-miljø hvis leieren din ikke har et.</span><span class="sxs-lookup"><span data-stu-id="03389-109">If you have a license for Microsoft Power Platform, you will get a new Common Data Service environment if your tenant doesn't have one.</span></span>
+ <span data-ttu-id="03389-110">For eksisterende forekomster av Finance and Operations-apper begynner oppsettet av en tilkobling med dobbel skriving i Finance and Operations-miljøet.</span><span class="sxs-lookup"><span data-stu-id="03389-110">For existing instances Finance and Operations apps, the setup of a dual-write connection begins in the Finance and Operations environment.</span></span>

<span data-ttu-id="03389-111">Følgende oppsettscenarier støttes:</span><span class="sxs-lookup"><span data-stu-id="03389-111">The following setup scenarios are supported:</span></span>

+ [<span data-ttu-id="03389-112">En ny Finance and Operations-appforekomst og en ny modelldrevet appforekomst</span><span class="sxs-lookup"><span data-stu-id="03389-112">A new Finance and Operations app instance and a new model-driven app instance</span></span>](#new-new)
+ [<span data-ttu-id="03389-113">En ny Finance and Operations-appforekomst og en eksisterende modelldrevet appforekomst</span><span class="sxs-lookup"><span data-stu-id="03389-113">A new Finance and Operations app instance and an existing model-driven app instance</span></span>](#new-existing)
+ [<span data-ttu-id="03389-114">En ny Finance and Operations-appforekomst som har demodata og en ny modelldrevet appforekomst</span><span class="sxs-lookup"><span data-stu-id="03389-114">A new Finance and Operations app instance that has demo data and a new model-driven app instance</span></span>](#new-demo-new)
+ [<span data-ttu-id="03389-115">En ny Finance and Operations-appforekomst som har demodata og en eksisterende modelldrevet appforekomst</span><span class="sxs-lookup"><span data-stu-id="03389-115">A new Finance and Operations app instance that has demo data and an existing model-driven app instance</span></span>](#new-demo-existing)
+ [<span data-ttu-id="03389-116">En eksisterende Finance and Operations-appforekomst og en ny eller eksisterende modelldrevet appforekomst</span><span class="sxs-lookup"><span data-stu-id="03389-116">An existing Finance and Operations app instance and a new or existing model-driven app instance</span></span>](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-model-driven-app-instance"></a><a id="new-new"></a><span data-ttu-id="03389-117">En ny Finance and Operations-appforekomst og en ny modelldrevet appforekomst</span><span class="sxs-lookup"><span data-stu-id="03389-117">A new Finance and Operations app instance and a new model-driven app instance</span></span>

<span data-ttu-id="03389-118">Hvis du vil konfigurere en dobbel skriving-tilkobling mellom en ny forekomst av en Finance and Operations-app som ikke har noen data, og en ny forekomst av en modelldrevet app i Dynamics 365, følger du fremgangsmåten i [Oppsett av dobbel skriving fra Lifecycle Services](lcs-setup.md).</span><span class="sxs-lookup"><span data-stu-id="03389-118">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and a new instance of a model-driven app in Dynamics 365, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="03389-119">Når tilkoblingsoppsettet er fullført, skjer følgende handlinger automatisk:</span><span class="sxs-lookup"><span data-stu-id="03389-119">When the connection setup is completed, the following actions occur automatically:</span></span>

- <span data-ttu-id="03389-120">Et nytt, tomt Finance and Operations-miljø er klargjort.</span><span class="sxs-lookup"><span data-stu-id="03389-120">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="03389-121">En ny, tom forekomst av en modelldrevet app er klargjort, der CRM-hovedløsningen er installert.</span><span class="sxs-lookup"><span data-stu-id="03389-121">A new, empty instance of a model-driven app is provisioned, where the CRM prime solution is installed.</span></span>
- <span data-ttu-id="03389-122">Det opprettes en dobbel skriving-tilkobling for DAT-firmadata.</span><span class="sxs-lookup"><span data-stu-id="03389-122">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="03389-123">Enhetstilordninger er aktivert for direkte synkronisering.</span><span class="sxs-lookup"><span data-stu-id="03389-123">Entity maps are enabled for live synchronization.</span></span>

<span data-ttu-id="03389-124">Begge miljøene er så klare for direkte synkronisering av data.</span><span class="sxs-lookup"><span data-stu-id="03389-124">Both environments are then ready for live data synchronization.</span></span>

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-model-driven-app-instance"></a><a id="new-existing"></a><span data-ttu-id="03389-125">En ny Finance and Operations-appforekomst og en eksisterende modelldrevet appforekomst</span><span class="sxs-lookup"><span data-stu-id="03389-125">A new Finance and Operations app instance and an existing model-driven app instance</span></span>

<span data-ttu-id="03389-126">Hvis du vil konfigurere en dobbel skriving-tilkobling mellom en ny forekomst av en Finance and Operations-app som ikke har noen data, og en eksisterende forekomst av en modelldrevet app i Dynamics 365, følger du fremgangsmåten i [Oppsett av dobbel skriving fra Lifecycle Services](lcs-setup.md).</span><span class="sxs-lookup"><span data-stu-id="03389-126">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and an existing instance of a model-driven app in Dynamics 365, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="03389-127">Når tilkoblingsoppsettet er fullført, skjer følgende handlinger automatisk:</span><span class="sxs-lookup"><span data-stu-id="03389-127">When the connection setup is completed, the following actions occur automatically:</span></span>

- <span data-ttu-id="03389-128">Et nytt, tomt Finance and Operations-miljø er klargjort.</span><span class="sxs-lookup"><span data-stu-id="03389-128">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="03389-129">Det opprettes en dobbel skriving-tilkobling for DAT-firmadata.</span><span class="sxs-lookup"><span data-stu-id="03389-129">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="03389-130">Enhetstilordninger er aktivert for direkte synkronisering.</span><span class="sxs-lookup"><span data-stu-id="03389-130">Entity maps are enabled for live synchronization.</span></span>

<span data-ttu-id="03389-131">Begge miljøene er så klare for direkte synkronisering av data.</span><span class="sxs-lookup"><span data-stu-id="03389-131">Both environments are then ready for live data synchronization.</span></span>

<span data-ttu-id="03389-132">Følg denne fremgangsmåten for å synkronisere de eksisterende Common Data Service-dataene med Finance and Operations-appen.</span><span class="sxs-lookup"><span data-stu-id="03389-132">To sync the existing Common Data Service data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="03389-133">Opprette et nytt firma i Finance and Operations-appen.</span><span class="sxs-lookup"><span data-stu-id="03389-133">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="03389-134">Legg til firmaet i oppsettet for dobbelt skriving-tilkobling.</span><span class="sxs-lookup"><span data-stu-id="03389-134">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="03389-135">[Starte opp](bootstrap-company-data.md) Common Data Service-dataene ved hjelp av en ISO-firmakode (International Organization for Standardization) på tre tegn.</span><span class="sxs-lookup"><span data-stu-id="03389-135">[Bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter International Organization for Standardization (ISO) company code.</span></span>

<span data-ttu-id="03389-136">Fordi dobbel skriving er i modus for direkte synkronisering, begynner dataene fra Common Data Service å strømme til Finance and Operations-appen automatisk.</span><span class="sxs-lookup"><span data-stu-id="03389-136">Because dual-write is in live synchronization mode, the data from Common Data Service automatically starts to flow to the Finance and Operations app.</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-demo-data-and-a-new-model-driven-app-instance"></a><a id="new-demo-new"></a><span data-ttu-id="03389-137">En ny Finance and Operations-appforekomst som har demodata og en ny modelldrevet appforekomst</span><span class="sxs-lookup"><span data-stu-id="03389-137">A new Finance and Operations app instance that has demo data and a new model-driven app instance</span></span>

<span data-ttu-id="03389-138">Hvis du vil konfigurere en dobbel skriving-tilkobling mellom en ny forekomst av en Finance and Operations-app som har demodata og en ny forekomst av en modelldrevet app i Dynamics 365, følger du fremgangsmåten i delen [En ny Finance and Operations-appforekomst og en ny modelldrevet appforekomst](#new-new) tidligere i dette emnet.</span><span class="sxs-lookup"><span data-stu-id="03389-138">To set up a dual-write connection between a new instance of a Finance and Operations app that has demo data and a new instance of a model-driven app in Dynamics 365, follow the steps in the [A new Finance and Operations app instance and a new model-driven app instance](#new-new) section earlier in this topic.</span></span> <span data-ttu-id="03389-139">Når tilkoblingsoppsettet er fullført, følger du denne fremgangsmåten hvis du vil synkronisere demonstrasjonsdataene med den modelldrevne appen.</span><span class="sxs-lookup"><span data-stu-id="03389-139">When the connection setup is completed, if you want to sync the demo data to the model-driven app, follow these steps.</span></span>

1. <span data-ttu-id="03389-140">Åpne Finance and Operations-appen fra LCS-siden, logg på og gå til **Databehandling \> Dobbel skriving**.</span><span class="sxs-lookup"><span data-stu-id="03389-140">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="03389-141">Kjør **Innledende synkronisering**-funksjonaliteten for enhetene du vil synkronisere data for.</span><span class="sxs-lookup"><span data-stu-id="03389-141">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-demo-data-and-an-existing-model-driven-app-instance"></a><span data-ttu-id="03389-142">E<a id="new-demo-existing"></a>En ny Finance and Operations-appforekomst som har demodata og en eksisterende modelldrevet appforekomst</span><span class="sxs-lookup"><span data-stu-id="03389-142"><a id="new-demo-existing"></a>A new Finance and Operations app instance that has demo data and an existing model-driven app instance</span></span>

<span data-ttu-id="03389-143">Hvis du vil konfigurere en dobbel skriving-tilkobling mellom en ny forekomst av en Finance and Operations-app som har en eksisterende forekomst av en modelldrevet app i Dynamics 365, følger du fremgangsmåten i delen [En ny Finance and Operations-appforekomst og en eksisterende modelldrevet appforekomst](#new-existing) tidligere i dette emnet.</span><span class="sxs-lookup"><span data-stu-id="03389-143">To set up a dual-write connection between a new instance of a Finance and Operations app that has demo data and an existing instance of a model-driven app in Dynamics 365, follow the steps in the [A new Finance and Operations app instance and an existing model-driven app instance](#new-existing) section earlier in this topic.</span></span> <span data-ttu-id="03389-144">Når tilkoblingsoppsettet er fullført, følger du denne fremgangsmåten hvis du vil synkronisere demonstrasjonsdataene med den modelldrevne appen.</span><span class="sxs-lookup"><span data-stu-id="03389-144">When the connection setup is completed, if you want to sync the demo data to the model-driven app, follow these steps.</span></span>

1. <span data-ttu-id="03389-145">Åpne Finance and Operations-appen fra LCS-siden, logg på og gå til **Databehandling \> Dobbel skriving**.</span><span class="sxs-lookup"><span data-stu-id="03389-145">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="03389-146">Kjør **Innledende synkronisering**-funksjonaliteten for enhetene du vil synkronisere data for.</span><span class="sxs-lookup"><span data-stu-id="03389-146">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

<span data-ttu-id="03389-147">Følg denne fremgangsmåten for å synkronisere de eksisterende Common Data Service-dataene med Finance and Operations-appen.</span><span class="sxs-lookup"><span data-stu-id="03389-147">To sync the existing Common Data Service data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="03389-148">Opprette et nytt firma i Finance and Operations-appen.</span><span class="sxs-lookup"><span data-stu-id="03389-148">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="03389-149">Legg til firmaet i oppsettet for dobbelt skriving-tilkobling.</span><span class="sxs-lookup"><span data-stu-id="03389-149">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="03389-150">[Starte opp](bootstrap-company-data.md) Common Data Service-dataene ved hjelp av en ISO-firmakode på tre tegn.</span><span class="sxs-lookup"><span data-stu-id="03389-150">[Bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter ISO company code.</span></span>

<span data-ttu-id="03389-151">Fordi dobbel skriving er i modus for direkte synkronisering, begynner dataene fra Common Data Service å strømme til Finance and Operations-appen automatisk.</span><span class="sxs-lookup"><span data-stu-id="03389-151">Because dual-write is in live synchronization mode, the data from Common Data Service automatically starts to flow to the Finance and Operations app.</span></span>

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-or-existing-model-driven-app-instance"></a><a id="existing-existing"></a><span data-ttu-id="03389-152">En eksisterende Finance and Operations-appforekomst og en ny eller eksisterende modelldrevet appforekomst</span><span class="sxs-lookup"><span data-stu-id="03389-152">An existing Finance and Operations app instance and a new or existing model-driven app instance</span></span>

<span data-ttu-id="03389-153">Oppsettet av en dobbel skriving-tilkobling mellom en eksisterende forekomst av en Finance and Operations-app og en ny eller eksisterende forekomst av en modelldrevet app i Dynamics 365 forekommer i Finance and Operation-miljøet.</span><span class="sxs-lookup"><span data-stu-id="03389-153">The setup of a dual-write connection between an existing instance of a Finance and Operations app and a new or existing instance of a model-driven app in Dynamics 365 occurs in the Finance and Operation environment.</span></span>

1. <span data-ttu-id="03389-154">Angi tilkoblingen fra Finance and Operations-appen.</span><span class="sxs-lookup"><span data-stu-id="03389-154">Set up the connection from the Finance and Operations app.</span></span>
2. <span data-ttu-id="03389-155">Hvis du vil synkronisere de eksisterende Common Data Service-dataene til Finance and Operations-appen, [starter du opp](bootstrap-company-data.md) Common Data Service-dataene ved hjelp av en ISO-firmakode på tre bokstaver.</span><span class="sxs-lookup"><span data-stu-id="03389-155">To sync the existing Common Data Service data to the Finance and Operations app, [bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter ISO company code.</span></span>

<span data-ttu-id="03389-156">Fordi dobbel skriving er i modus for direkte synkronisering, begynner dataene fra Common Data Service å strømme til Finance and Operations-appen automatisk.</span><span class="sxs-lookup"><span data-stu-id="03389-156">Because dual-write is in live synchronization mode, the data from Common Data Service automatically starts to flow to the Finance and Operations app.</span></span>
