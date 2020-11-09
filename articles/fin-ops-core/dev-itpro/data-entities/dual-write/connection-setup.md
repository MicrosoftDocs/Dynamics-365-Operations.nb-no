---
title: Veiledning for hvordan du konfigurerer dobbel skriving
description: Dette emnet beskriver scenariene som støttes for oppsett av dobbel skriving.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 10/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 2d77a1458f3f4c79b231e6a6d7cc320b8ee1fad9
ms.sourcegitcommit: ee643d651d57560bccae2f99238faa39881f5c64
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/21/2020
ms.locfileid: "4088512"
---
# <a name="guidance-for-how-to-set-up-dual-write"></a><span data-ttu-id="4fb9f-103">Veiledning for hvordan du konfigurerer dobbel skriving</span><span class="sxs-lookup"><span data-stu-id="4fb9f-103">Guidance for how to set up dual-write</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="4fb9f-104">Du kan opprette en dobbelt skrive-tilkobling mellom et Finance and Operations-miljø og et Common Data Service-miljø.</span><span class="sxs-lookup"><span data-stu-id="4fb9f-104">You can set up a dual-write connection between a Finance and Operations environment and a Common Data Service environment.</span></span>

+ <span data-ttu-id="4fb9f-105">Et **Finance and Operations-miljø** gir den underliggende plattformen for **Finance and Operations-apper** (for eksempel Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management og Dynamics 365 Retail).</span><span class="sxs-lookup"><span data-stu-id="4fb9f-105">A **Finance and Operations environment** provides the underlying platform for **Finance and Operations apps** (for example, Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, and Dynamics 365 Retail).</span></span>
+ <span data-ttu-id="4fb9f-106">Et **Common Data Service-miljø** gir den underliggende plattformen for **kundeengasjementsapper** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 Field Service, Dynamics 365 Marketing og Dynamics 365 Project Service Automation).</span><span class="sxs-lookup"><span data-stu-id="4fb9f-106">A **Common Data Service environment** provides the underlying platform for **customer engagement apps** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 Field Service, Dynamics 365 Marketing, and Dynamics 365 Project Service Automation).</span></span>

>[!IMPORTANT]
><span data-ttu-id="4fb9f-107">Human Resources i Finance and Operations støtter tilkoblinger med dobbel skriving, men Dynamics 365 Human Resources-appen gjør ikke det.</span><span class="sxs-lookup"><span data-stu-id="4fb9f-107">Human Resources in Finance and Operations supports dual-write connections, but the Dynamics 365 Human Resources app doesn't.</span></span>

<span data-ttu-id="4fb9f-108">Installasjonsmekanismen varierer, avhengig av abonnementet og miljøet.</span><span class="sxs-lookup"><span data-stu-id="4fb9f-108">The setup mechanism varies, depending on your subscription and the environment.</span></span>

+ <span data-ttu-id="4fb9f-109">Når det gjelder nye forekomster av Finance and Operations-apper, begynner oppsettet av en tilkobling med dobbel skriving i Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="4fb9f-109">For new instances of Finance and Operations apps, the setup of a dual-write connection begins in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="4fb9f-110">Hvis du har en lisens for Power Platform, vil du få et nytt Common Data Service-miljø hvis leieren din ikke har et.</span><span class="sxs-lookup"><span data-stu-id="4fb9f-110">If you have a license for Power Platform, you will get a new Common Data Service environment if your tenant doesn't have one.</span></span>
+ <span data-ttu-id="4fb9f-111">For eksisterende forekomster av Finance and Operations-apper begynner oppsettet av en tilkobling med dobbel skriving i Finance and Operations-miljøet.</span><span class="sxs-lookup"><span data-stu-id="4fb9f-111">For existing instances Finance and Operations apps, the setup of a dual-write connection begins in the Finance and Operations environment.</span></span>

<span data-ttu-id="4fb9f-112">Før du starter med å skrive på en enhet, kan du kjøre en første synkronisering for å behandle eksisterende data på begge sider av Finance and Operations-apper og kundeengasjementsapper.</span><span class="sxs-lookup"><span data-stu-id="4fb9f-112">Before you start dual-write on an entity, you can run an initial sync to handle existing data on both sides of Finance and Operations apps and customer engagement apps.</span></span> <span data-ttu-id="4fb9f-113">Du kan hoppe over den innledende synkroniseringen hvis du ikke trenger å synkronisere data mellom de to miljøene.</span><span class="sxs-lookup"><span data-stu-id="4fb9f-113">You can skip the initial sync if you don't need to synchronize data between the two environments.</span></span>

<span data-ttu-id="4fb9f-114">Ved hjelp av en innledende synkronisering kan du kopiere eksisterende data fra én app til en annen toveis.</span><span class="sxs-lookup"><span data-stu-id="4fb9f-114">An initial sync lets you copy existing data from one app to another bidirectionally.</span></span> <span data-ttu-id="4fb9f-115">Det finnes flere forskjellige installasjonsscenarioer, avhengig av hvilke miljøer du allerede har, og hvilken type data som finnes i miljøene.</span><span class="sxs-lookup"><span data-stu-id="4fb9f-115">There are several different setup scenarios depending on which environments you already have and what type of data is in the environments.</span></span>

<span data-ttu-id="4fb9f-116">Følgende oppsettscenarier støttes:</span><span class="sxs-lookup"><span data-stu-id="4fb9f-116">The following setup scenarios are supported:</span></span>

+ [<span data-ttu-id="4fb9f-117">En ny Finance and Operations-appforekomst og en ny kundeengasjementsapp-forekomst</span><span class="sxs-lookup"><span data-stu-id="4fb9f-117">A new Finance and Operations app instance and a new customer engagement app instance</span></span>](#new-new)
+ [<span data-ttu-id="4fb9f-118">En ny Finance and Operations-appforekomst og en eksisterende kundeengasjementsapp-forekomst</span><span class="sxs-lookup"><span data-stu-id="4fb9f-118">A new Finance and Operations app instance and an existing customer engagement app instance</span></span>](#new-existing)
+ [<span data-ttu-id="4fb9f-119">En ny Finance and Operations-appforekomst som har data og en kundeengasjementsapp-forekomst</span><span class="sxs-lookup"><span data-stu-id="4fb9f-119">A new Finance and Operations app instance that has data and a new customer engagement app instance</span></span>](#new-data-new)
+ [<span data-ttu-id="4fb9f-120">En ny Finance and Operations-appforekomst som har data og en eksisterende kundeengasjementsapp-forekomst</span><span class="sxs-lookup"><span data-stu-id="4fb9f-120">A new Finance and Operations app instance that has data and an existing customer engagement app instance</span></span>](#new-data-existing)
+ [<span data-ttu-id="4fb9f-121">En eksisterende Finance and Operations-appforekomst og en ny kundeengasjementsapp-forekomst</span><span class="sxs-lookup"><span data-stu-id="4fb9f-121">An existing Finance and Operations app instance and a new customer engagement app instance</span></span>](#existing-new)
+ [<span data-ttu-id="4fb9f-122">En eksisterende Finance and Operations-appforekomst og en eksisterende kundeengasjementsapp-forekomst</span><span class="sxs-lookup"><span data-stu-id="4fb9f-122">An existing Finance and Operations app instance and an existing customer engagement app instance</span></span>](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="new-new"></a><span data-ttu-id="4fb9f-123">En ny Finance and Operations-appforekomst og en ny kundeengasjementsapp-forekomst</span><span class="sxs-lookup"><span data-stu-id="4fb9f-123">A new Finance and Operations app instance and a new customer engagement app instance</span></span>

<span data-ttu-id="4fb9f-124">Hvis du vil konfigurere en dobbel skriving-tilkobling mellom en ny forekomst av en Finance and Operations-app som ikke har noen data, og en ny kundeengasjementsapp-forekomst, følger du fremgangsmåten i [Oppsett av dobbel skriving fra Lifecycle Services](lcs-setup.md).</span><span class="sxs-lookup"><span data-stu-id="4fb9f-124">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and a new instance of a customer engagement app, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="4fb9f-125">Når tilkoblingsoppsettet er fullført, skjer følgende handlinger automatisk:</span><span class="sxs-lookup"><span data-stu-id="4fb9f-125">When the connection setup is completed, the following actions occur automatically:</span></span>

- <span data-ttu-id="4fb9f-126">Et nytt, tomt Finance and Operations-miljø er klargjort.</span><span class="sxs-lookup"><span data-stu-id="4fb9f-126">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="4fb9f-127">En ny, tom forekomst av en kundeengasjementsapp er klargjort, der CRM-hovedløsningen er installert.</span><span class="sxs-lookup"><span data-stu-id="4fb9f-127">A new, empty instance of a customer engagement app is provisioned, where the CRM prime solution is installed.</span></span>
- <span data-ttu-id="4fb9f-128">Det opprettes en dobbel skriving-tilkobling for DAT-firmadata.</span><span class="sxs-lookup"><span data-stu-id="4fb9f-128">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="4fb9f-129">Enhetstilordninger er aktivert for direkte synkronisering.</span><span class="sxs-lookup"><span data-stu-id="4fb9f-129">Entity maps are enabled for live synchronization.</span></span>

<span data-ttu-id="4fb9f-130">Begge miljøene er så klare for direkte synkronisering av data.</span><span class="sxs-lookup"><span data-stu-id="4fb9f-130">Both environments are then ready for live data synchronization.</span></span>

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="new-existing"></a><span data-ttu-id="4fb9f-131">En ny Finance and Operations-appforekomst og en eksisterende kundeengasjementsapp-forekomst</span><span class="sxs-lookup"><span data-stu-id="4fb9f-131">A new Finance and Operations app instance and an existing customer engagement app instance</span></span>

<span data-ttu-id="4fb9f-132">Hvis du vil konfigurere en dobbel skriving-tilkobling mellom en ny forekomst av en Finance and Operations-app som ikke har noen data, og en eksisterende kundeengasjementsapp-forekomst, følger du fremgangsmåten i [Oppsett av dobbel skriving fra Lifecycle Services](lcs-setup.md).</span><span class="sxs-lookup"><span data-stu-id="4fb9f-132">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and an existing instance of a customer engagement app, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="4fb9f-133">Når tilkoblingsoppsettet er fullført, skjer følgende handlinger automatisk:</span><span class="sxs-lookup"><span data-stu-id="4fb9f-133">When the connection setup is completed, the following actions occur automatically:</span></span>

- <span data-ttu-id="4fb9f-134">Et nytt, tomt Finance and Operations-miljø er klargjort.</span><span class="sxs-lookup"><span data-stu-id="4fb9f-134">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="4fb9f-135">Det opprettes en dobbel skriving-tilkobling for DAT-firmadata.</span><span class="sxs-lookup"><span data-stu-id="4fb9f-135">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="4fb9f-136">Enhetstilordninger er aktivert for direkte synkronisering.</span><span class="sxs-lookup"><span data-stu-id="4fb9f-136">Entity maps are enabled for live synchronization.</span></span>

<span data-ttu-id="4fb9f-137">Begge miljøene er så klare for direkte synkronisering av data.</span><span class="sxs-lookup"><span data-stu-id="4fb9f-137">Both environments are then ready for live data synchronization.</span></span>

<span data-ttu-id="4fb9f-138">Følg denne fremgangsmåten for å synkronisere de eksisterende Common Data Service-dataene med Finance and Operations-appen.</span><span class="sxs-lookup"><span data-stu-id="4fb9f-138">To sync the existing Common Data Service data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="4fb9f-139">Opprette et nytt firma i Finance and Operations-appen.</span><span class="sxs-lookup"><span data-stu-id="4fb9f-139">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="4fb9f-140">Legg til firmaet i oppsettet for dobbelt skriving-tilkobling.</span><span class="sxs-lookup"><span data-stu-id="4fb9f-140">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="4fb9f-141">[Starte opp](bootstrap-company-data.md) Common Data Service-dataene ved hjelp av en ISO-firmakode (International Organization for Standardization) på tre tegn.</span><span class="sxs-lookup"><span data-stu-id="4fb9f-141">[Bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter International Organization for Standardization (ISO) company code.</span></span>
4. <span data-ttu-id="4fb9f-142">Kjør **Innledende synkronisering** -funksjonaliteten for enhetene du vil synkronisere data for.</span><span class="sxs-lookup"><span data-stu-id="4fb9f-142">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

<span data-ttu-id="4fb9f-143">Hvis du vil ha et eksempel og en alternativ metode, se [Eksempel](#example).</span><span class="sxs-lookup"><span data-stu-id="4fb9f-143">For an example and alternative approach, see [Example](#example).</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-a-new-customer-engagement-app-instance"></a><a id="new-data-new"></a><span data-ttu-id="4fb9f-144">En ny Finance and Operations-appforekomst som har data og en kundeengasjementsapp-forekomst</span><span class="sxs-lookup"><span data-stu-id="4fb9f-144">A new Finance and Operations app instance that has data and a new customer engagement app instance</span></span>

<span data-ttu-id="4fb9f-145">Hvis du vil konfigurere en dobbel skriving-tilkobling mellom en ny forekomst av en Finance and Operations-app som har data og en ny forekomst av en kundeengasjementsapp, følger du fremgangsmåten i delen [En ny Finance and Operations-appforekomst og en ny kundeengasjementsapp-forekomst](#new-new) tidligere i dette emnet.</span><span class="sxs-lookup"><span data-stu-id="4fb9f-145">To set up a dual-write connection between a new instance of a Finance and Operations app that has data and a new instance of a customer engagement app, follow the steps in the [A new Finance and Operations app instance and a new customer engagement app instance](#new-new) section earlier in this topic.</span></span> <span data-ttu-id="4fb9f-146">Når tilkoblingsoppsettet er fullført, følger du denne fremgangsmåten hvis du vil synkronisere dataene med kundeengasjementsappen.</span><span class="sxs-lookup"><span data-stu-id="4fb9f-146">When the connection setup is completed, if you want to sync the data to the customer engagement app, follow these steps.</span></span>

1. <span data-ttu-id="4fb9f-147">Åpne Finance and Operations-appen fra LCS-siden, logg på og gå til **Databehandling \> Dobbel skriving**.</span><span class="sxs-lookup"><span data-stu-id="4fb9f-147">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="4fb9f-148">Kjør **Innledende synkronisering** -funksjonaliteten for enhetene du vil synkronisere data for.</span><span class="sxs-lookup"><span data-stu-id="4fb9f-148">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

<span data-ttu-id="4fb9f-149">Hvis du vil ha et eksempel og en alternativ metode, se [Eksempel](#example).</span><span class="sxs-lookup"><span data-stu-id="4fb9f-149">For an example and alternative approach, see [Example](#example).</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-an-existing-customer-engagement-app-instance"></a><a id="new-data-existing"></a><span data-ttu-id="4fb9f-150">En ny Finance and Operations-appforekomst som har data og en eksisterende kundeengasjementsapp-forekomst</span><span class="sxs-lookup"><span data-stu-id="4fb9f-150">A new Finance and Operations app instance that has data and an existing customer engagement app instance</span></span>

<span data-ttu-id="4fb9f-151">Hvis du vil konfigurere en dobbel skriving-tilkobling mellom en ny forekomst av en Finance and Operations-app som har data og en eksisterende forekomst av en kundeengasjementsapp, følger du fremgangsmåten i delen [En ny Finance and Operations-appforekomst og en eksisterende kundeengasjementsapp-forekomst](#new-existing) tidligere i dette emnet.</span><span class="sxs-lookup"><span data-stu-id="4fb9f-151">To set up a dual-write connection between a new instance of a Finance and Operations app that has data and an existing instance of a customer engagement app, follow the steps in the [A new Finance and Operations app instance and an existing customer engagement app instance](#new-existing) section earlier in this topic.</span></span> <span data-ttu-id="4fb9f-152">Når tilkoblingsoppsettet er fullført, følger du denne fremgangsmåten hvis du vil synkronisere dataene med kundeengasjementsappen.</span><span class="sxs-lookup"><span data-stu-id="4fb9f-152">When the connection setup is completed, if you want to sync the data to the customer engagement app, follow these steps.</span></span>

1. <span data-ttu-id="4fb9f-153">Åpne Finance and Operations-appen fra LCS-siden, logg på og gå til **Databehandling \> Dobbel skriving**.</span><span class="sxs-lookup"><span data-stu-id="4fb9f-153">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="4fb9f-154">Kjør **Innledende synkronisering** -funksjonaliteten for enhetene du vil synkronisere data for.</span><span class="sxs-lookup"><span data-stu-id="4fb9f-154">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

<span data-ttu-id="4fb9f-155">Følg denne fremgangsmåten for å synkronisere de eksisterende Common Data Service-dataene med Finance and Operations-appen.</span><span class="sxs-lookup"><span data-stu-id="4fb9f-155">To sync the existing Common Data Service data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="4fb9f-156">Opprette et nytt firma i Finance and Operations-appen.</span><span class="sxs-lookup"><span data-stu-id="4fb9f-156">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="4fb9f-157">Legg til firmaet i oppsettet for dobbelt skriving-tilkobling.</span><span class="sxs-lookup"><span data-stu-id="4fb9f-157">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="4fb9f-158">[Starte opp](bootstrap-company-data.md) Common Data Service-dataene ved hjelp av en ISO-firmakode på tre tegn.</span><span class="sxs-lookup"><span data-stu-id="4fb9f-158">[Bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter ISO company code.</span></span>
4. <span data-ttu-id="4fb9f-159">Kjør **Innledende synkronisering** -funksjonaliteten for enhetene du vil synkronisere data for.</span><span class="sxs-lookup"><span data-stu-id="4fb9f-159">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

<span data-ttu-id="4fb9f-160">Hvis du vil ha et eksempel og en alternativ metode, se [Eksempel](#example).</span><span class="sxs-lookup"><span data-stu-id="4fb9f-160">For an example and alternative approach, see [Example](#example).</span></span>

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="existing-new"></a><span data-ttu-id="4fb9f-161">En eksisterende Finance and Operations-appforekomst og en ny kundeengasjementsapp-forekomst</span><span class="sxs-lookup"><span data-stu-id="4fb9f-161">An existing Finance and Operations app instance and a new customer engagement app instance</span></span>

<span data-ttu-id="4fb9f-162">Oppsettet av en dobbel skriving-tilkobling mellom en eksisterende forekomst av en Finance and Operations-app og en ny forekomst av en kundeengasjementsapp forekommer i Finance and Operation-miljøet.</span><span class="sxs-lookup"><span data-stu-id="4fb9f-162">The setup of a dual-write connection between an existing instance of a Finance and Operations app and a new instance of a customer engagement app occurs in the Finance and Operation environment.</span></span>

1. <span data-ttu-id="4fb9f-163">[Angi tilkoblingen fra Finance and Operations-appen](enable-dual-write.md).</span><span class="sxs-lookup"><span data-stu-id="4fb9f-163">[Set up the connection from the Finance and Operations app](enable-dual-write.md).</span></span>
2. <span data-ttu-id="4fb9f-164">Kjør **Innledende synkronisering** -funksjonaliteten for enhetene du vil synkronisere data for.</span><span class="sxs-lookup"><span data-stu-id="4fb9f-164">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

<span data-ttu-id="4fb9f-165">Hvis du vil ha et eksempel og en alternativ metode, se [Eksempel](#example).</span><span class="sxs-lookup"><span data-stu-id="4fb9f-165">For an example and alternative approach, see [Example](#example).</span></span>

## <a name="an-existing-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="existing-existing"></a><span data-ttu-id="4fb9f-166">En eksisterende Finance and Operations-appforekomst og en eksisterende kundeengasjementsapp-forekomst</span><span class="sxs-lookup"><span data-stu-id="4fb9f-166">An existing Finance and Operations app instance and an existing customer engagement app instance</span></span>

<span data-ttu-id="4fb9f-167">Oppsettet av en dobbel skriving-tilkobling mellom en eksisterende forekomst av en Finance and Operations-app og en eksisterende forekomst av en kundeengasjementsapp forekommer i Finance and Operation-miljøet.</span><span class="sxs-lookup"><span data-stu-id="4fb9f-167">The setup of a dual-write connection between an existing instance of a Finance and Operations app and an existing instance of a customer engagement app  occurs in the Finance and Operation environment.</span></span>

1. <span data-ttu-id="4fb9f-168">Angi tilkoblingen fra Finance and Operations-appen.</span><span class="sxs-lookup"><span data-stu-id="4fb9f-168">Set up the connection from the Finance and Operations app.</span></span>
2. <span data-ttu-id="4fb9f-169">Hvis du vil synkronisere de eksisterende Common Data Service-dataene til Finance and Operations-appen, [starter du opp](bootstrap-company-data.md) Common Data Service-dataene ved hjelp av en ISO-firmakode på tre bokstaver.</span><span class="sxs-lookup"><span data-stu-id="4fb9f-169">To sync the existing Common Data Service data to the Finance and Operations app, [bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter ISO company code.</span></span>
3. <span data-ttu-id="4fb9f-170">Kjør **Innledende synkronisering** -funksjonaliteten for enhetene du vil synkronisere data for.</span><span class="sxs-lookup"><span data-stu-id="4fb9f-170">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

<span data-ttu-id="4fb9f-171">Hvis du vil ha et eksempel og en alternativ metode, se [Eksempel](#example).</span><span class="sxs-lookup"><span data-stu-id="4fb9f-171">For an example and alternative approach, see [Example](#example).</span></span>

## <a name="example"></a><span data-ttu-id="4fb9f-172">Eksempel</span><span class="sxs-lookup"><span data-stu-id="4fb9f-172">Example</span></span>

<span data-ttu-id="4fb9f-173">Hvis du vil ha et eksempel, se [Aktivere enhetstilordningen Kunder V3 til kontakter](enable-entity-map.md#example-enabling-the-customers-v3contacts-entity-map)</span><span class="sxs-lookup"><span data-stu-id="4fb9f-173">For an example, see [Enabling the Customers V3—Contacts entity map](enable-entity-map.md#example-enabling-the-customers-v3contacts-entity-map)</span></span>

<span data-ttu-id="4fb9f-174">Hvis du vil ha en alternativ tilnærming basert på datavolumer i hver enhet som må kjøre første synkronisering, kan du se [Hensyn ved innledende synkronisering](initial-sync-guidance.md).</span><span class="sxs-lookup"><span data-stu-id="4fb9f-174">For an alternative approach based on data volumes in each entity that need to run initial sync, see [Considerations for initial synchronization](initial-sync-guidance.md).</span></span>
