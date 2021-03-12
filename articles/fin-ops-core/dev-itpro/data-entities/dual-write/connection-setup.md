---
title: Veiledning for oppsett av dobbel skriving
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
ms.openlocfilehash: 78a7cdc18476a1c523c83c92ca6f354c3ba806dc
ms.sourcegitcommit: 7e1be696894731e1c58074d9b5e9c5b3acf7e52a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/17/2020
ms.locfileid: "4744859"
---
# <a name="guidance-for-dual-write-setup"></a><span data-ttu-id="9626a-103">Veiledning for oppsett av dobbel skriving</span><span class="sxs-lookup"><span data-stu-id="9626a-103">Guidance for dual-write setup</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="9626a-104">Du kan opprette en dobbelt skrive-tilkobling mellom et Finance and Operations-miljø og et Dataverse-miljø.</span><span class="sxs-lookup"><span data-stu-id="9626a-104">You can set up a dual-write connection between a Finance and Operations environment and a Dataverse environment.</span></span>

+ <span data-ttu-id="9626a-105">Et **Finance and Operations-miljø** gir den underliggende plattformen for **Finance and Operations-apper** (for eksempel Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce og Dynamics 365 Human Resources).</span><span class="sxs-lookup"><span data-stu-id="9626a-105">A **Finance and Operations environment** provides the underlying platform for **Finance and Operations apps** (for example, Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce, and Dynamics 365 Human Resources).</span></span>
+ <span data-ttu-id="9626a-106">Et **Dataverse-miljø** gir den underliggende plattformen for **kundeengasjementsapper** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 column Service, Dynamics 365 Marketing og Dynamics 365 Project Service Automation).</span><span class="sxs-lookup"><span data-stu-id="9626a-106">A **Dataverse environment** provides the underlying platform for **customer engagement apps** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 column Service, Dynamics 365 Marketing, and Dynamics 365 Project Service Automation).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9626a-107">Personale-modulen i Dynamics 365 Finance støtter tilkoblinger med dobbel skriving, men det gjør ikke appen Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="9626a-107">The Human Resources module in Dynamics 365 Finance supports dual-write connections, but the Dynamics 365 Human Resources app doesn't.</span></span>

<span data-ttu-id="9626a-108">Oppsettmekanismen varierer, avhengig av abonnementet og miljøet:</span><span class="sxs-lookup"><span data-stu-id="9626a-108">The setup mechanism varies, depending on your subscription and the environment:</span></span>

+ <span data-ttu-id="9626a-109">Når det gjelder nye forekomster av Finance and Operations-apper, begynner oppsettet av en tilkobling med dobbel skriving i Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="9626a-109">For new instances of Finance and Operations apps, the setup of a dual-write connection begins in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="9626a-110">Hvis du har en lisens for Microsoft Power Platform, vil du få et nytt Dataverse-miljø hvis leieren din ikke har et.</span><span class="sxs-lookup"><span data-stu-id="9626a-110">If you have a license for Microsoft Power Platform, you will get a new Dataverse environment if your tenant doesn't have one.</span></span>
+ <span data-ttu-id="9626a-111">For eksisterende forekomster av Finance and Operations-apper begynner oppsettet av en tilkobling med dobbel skriving i Finance and Operations-miljøet.</span><span class="sxs-lookup"><span data-stu-id="9626a-111">For existing instances Finance and Operations apps, the setup of a dual-write connection begins in the Finance and Operations environment.</span></span>

<span data-ttu-id="9626a-112">Før du starter dobbel skriving på en enhet, kan du kjøre en første synkronisering for å behandle eksisterende data på begge sider: Finance and Operations-apper og kundeengasjementsapper.</span><span class="sxs-lookup"><span data-stu-id="9626a-112">Before you start dual-write on an entity, you can run an initial synchronization to handle existing data on both sides: Finance and Operations apps and customer engagement apps.</span></span> <span data-ttu-id="9626a-113">Du kan hoppe over den innledende synkroniseringen hvis du ikke må synkronisere data mellom de to miljøene.</span><span class="sxs-lookup"><span data-stu-id="9626a-113">You can skip the initial synchronization if you don't have to sync data between the two environments.</span></span>

<span data-ttu-id="9626a-114">En innledende synkronisering gjør at du kan kopiere eksisterende data fra én app til en annen begge veier.</span><span class="sxs-lookup"><span data-stu-id="9626a-114">An initial synchronization lets you copy existing data from one app to another bidirectionally.</span></span> <span data-ttu-id="9626a-115">Det finnes flere forskjellige oppsettscenarioer, avhengig av miljøene du allerede har, og typen som finnes i dem.</span><span class="sxs-lookup"><span data-stu-id="9626a-115">There are several setup scenarios, depending on the environments that you already have and the type of data in them.</span></span>

<span data-ttu-id="9626a-116">Følgende oppsettscenarier støttes:</span><span class="sxs-lookup"><span data-stu-id="9626a-116">The following setup scenarios are supported:</span></span>

+ [<span data-ttu-id="9626a-117">En ny Finance and Operations-appforekomst og en ny kundeengasjementsapp-forekomst</span><span class="sxs-lookup"><span data-stu-id="9626a-117">A new Finance and Operations app instance and a new customer engagement app instance</span></span>](#new-new)
+ [<span data-ttu-id="9626a-118">En ny Finance and Operations-appforekomst og en eksisterende kundeengasjementsapp-forekomst</span><span class="sxs-lookup"><span data-stu-id="9626a-118">A new Finance and Operations app instance and an existing customer engagement app instance</span></span>](#new-existing)
+ [<span data-ttu-id="9626a-119">En ny Finance and Operations-appforekomst som har data og en kundeengasjementsapp-forekomst</span><span class="sxs-lookup"><span data-stu-id="9626a-119">A new Finance and Operations app instance that has data and a new customer engagement app instance</span></span>](#new-data-new)
+ [<span data-ttu-id="9626a-120">En ny Finance and Operations-appforekomst som har data og en eksisterende kundeengasjementsapp-forekomst</span><span class="sxs-lookup"><span data-stu-id="9626a-120">A new Finance and Operations app instance that has data and an existing customer engagement app instance</span></span>](#new-data-existing)
+ [<span data-ttu-id="9626a-121">En eksisterende Finance and Operations-appforekomst og en ny kundeengasjementsapp-forekomst</span><span class="sxs-lookup"><span data-stu-id="9626a-121">An existing Finance and Operations app instance and a new customer engagement app instance</span></span>](#existing-new)
+ [<span data-ttu-id="9626a-122">En eksisterende Finance and Operations-appforekomst og en eksisterende kundeengasjementsapp-forekomst</span><span class="sxs-lookup"><span data-stu-id="9626a-122">An existing Finance and Operations app instance and an existing customer engagement app instance</span></span>](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="new-new"></a><span data-ttu-id="9626a-123">En ny Finance and Operations-appforekomst og en ny kundeengasjementsapp-forekomst</span><span class="sxs-lookup"><span data-stu-id="9626a-123">A new Finance and Operations app instance and a new customer engagement app instance</span></span>

<span data-ttu-id="9626a-124">Hvis du vil konfigurere en dobbel skriving-tilkobling mellom en ny forekomst av en Finance and Operations-app som ikke har noen data, og en ny kundeengasjementsapp-forekomst, følger du fremgangsmåten i [Oppsett av dobbel skriving fra Lifecycle Services](lcs-setup.md).</span><span class="sxs-lookup"><span data-stu-id="9626a-124">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and a new instance of a customer engagement app, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="9626a-125">Når tilkoblingsoppsettet er fullført, skjer følgende handlinger automatisk:</span><span class="sxs-lookup"><span data-stu-id="9626a-125">When the connection setup is completed, the following actions automatically occur:</span></span>

- <span data-ttu-id="9626a-126">Et nytt, tomt Finance and Operations-miljø er klargjort.</span><span class="sxs-lookup"><span data-stu-id="9626a-126">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="9626a-127">En ny, tom forekomst av en kundeengasjementsapp er klargjort, der CRM-hovedløsningen er installert.</span><span class="sxs-lookup"><span data-stu-id="9626a-127">A new, empty instance of a customer engagement app is provisioned, where the CRM prime solution is installed.</span></span>
- <span data-ttu-id="9626a-128">Det opprettes en dobbel skriving-tilkobling for DAT-firmadata.</span><span class="sxs-lookup"><span data-stu-id="9626a-128">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="9626a-129">Tabelltilordninger er aktivert for direkte synkronisering.</span><span class="sxs-lookup"><span data-stu-id="9626a-129">Table maps are enabled for live synchronization.</span></span>

<span data-ttu-id="9626a-130">Begge miljøene er så klare for direkte synkronisering av data.</span><span class="sxs-lookup"><span data-stu-id="9626a-130">Both environments are then ready for live data synchronization.</span></span>

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="new-existing"></a><span data-ttu-id="9626a-131">En ny Finance and Operations-appforekomst og en eksisterende kundeengasjementsapp-forekomst</span><span class="sxs-lookup"><span data-stu-id="9626a-131">A new Finance and Operations app instance and an existing customer engagement app instance</span></span>

<span data-ttu-id="9626a-132">Hvis du vil konfigurere en dobbel skriving-tilkobling mellom en ny forekomst av en Finance and Operations-app som ikke har noen data, og en eksisterende kundeengasjementsapp-forekomst, følger du fremgangsmåten i [Oppsett av dobbel skriving fra Lifecycle Services](lcs-setup.md).</span><span class="sxs-lookup"><span data-stu-id="9626a-132">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and an existing instance of a customer engagement app, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="9626a-133">Når tilkoblingsoppsettet er fullført, skjer følgende handlinger automatisk:</span><span class="sxs-lookup"><span data-stu-id="9626a-133">When the connection setup is completed, the following actions automatically occur:</span></span>

- <span data-ttu-id="9626a-134">Et nytt, tomt Finance and Operations-miljø er klargjort.</span><span class="sxs-lookup"><span data-stu-id="9626a-134">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="9626a-135">Det opprettes en dobbel skriving-tilkobling for DAT-firmadata.</span><span class="sxs-lookup"><span data-stu-id="9626a-135">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="9626a-136">Tabelltilordninger er aktivert for direkte synkronisering.</span><span class="sxs-lookup"><span data-stu-id="9626a-136">Table maps are enabled for live synchronization.</span></span>

<span data-ttu-id="9626a-137">Begge miljøene er så klare for direkte synkronisering av data.</span><span class="sxs-lookup"><span data-stu-id="9626a-137">Both environments are then ready for live data synchronization.</span></span>

<span data-ttu-id="9626a-138">Følg denne fremgangsmåten for å synkronisere de eksisterende Dataverse-dataene med Finance and Operations-appen.</span><span class="sxs-lookup"><span data-stu-id="9626a-138">To sync the existing Dataverse data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="9626a-139">Opprette et nytt firma i Finance and Operations-appen.</span><span class="sxs-lookup"><span data-stu-id="9626a-139">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="9626a-140">Legg til firmaet i oppsettet for dobbelt skriving-tilkobling.</span><span class="sxs-lookup"><span data-stu-id="9626a-140">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="9626a-141">[Starte opp](bootstrap-company-data.md) Dataverse-dataene ved hjelp av en ISO-firmakode (International Organization for Standardization) på tre tegn.</span><span class="sxs-lookup"><span data-stu-id="9626a-141">[Bootstrap](bootstrap-company-data.md) the Dataverse data by using a three-letter International Organization for Standardization (ISO) company code.</span></span>
4. <span data-ttu-id="9626a-142">Kjør funksjonaliteten **Innledende synkronisering** for tabellen du vil synkronisere data for.</span><span class="sxs-lookup"><span data-stu-id="9626a-142">Run the **Initial sync** functionality for the tables that you want to sync data for.</span></span>

<span data-ttu-id="9626a-143">Hvis du vil ha koblinger til et eksempel og en alternativ tilnærming, kan du se [Eksempel](#example)-delen senere i dette emnet.</span><span class="sxs-lookup"><span data-stu-id="9626a-143">For links to an example and an alternative approach, see the [Example](#example) section later in this topic.</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-a-new-customer-engagement-app-instance"></a><a id="new-data-new"></a><span data-ttu-id="9626a-144">En ny Finance and Operations-appforekomst som har data og en kundeengasjementsapp-forekomst</span><span class="sxs-lookup"><span data-stu-id="9626a-144">A new Finance and Operations app instance that has data and a new customer engagement app instance</span></span>

<span data-ttu-id="9626a-145">Hvis du vil konfigurere en dobbel skriving-tilkobling mellom en ny forekomst av en Finance and Operations-app som har data og en ny forekomst av en kundeengasjementsapp, følger du fremgangsmåten i delen [En ny Finance and Operations-appforekomst og en ny kundeengasjementsapp-forekomst](#new-new) tidligere i dette emnet.</span><span class="sxs-lookup"><span data-stu-id="9626a-145">To set up a dual-write connection between a new instance of a Finance and Operations app that has data and a new instance of a customer engagement app, follow the steps in the [A new Finance and Operations app instance and a new customer engagement app instance](#new-new) section earlier in this topic.</span></span> <span data-ttu-id="9626a-146">Når tilkoblingsoppsettet er fullført, følger du denne fremgangsmåten hvis du vil synkronisere dataene med kundeengasjementsappen.</span><span class="sxs-lookup"><span data-stu-id="9626a-146">When the connection setup is completed, if you want to sync the data to the customer engagement app, follow these steps.</span></span>

1. <span data-ttu-id="9626a-147">Åpne Finance and Operations-appen fra LCS-siden, logg på og gå til **Databehandling \> Dobbel skriving**.</span><span class="sxs-lookup"><span data-stu-id="9626a-147">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="9626a-148">Kjør funksjonaliteten **Innledende synkronisering** for tabellen du vil synkronisere data for.</span><span class="sxs-lookup"><span data-stu-id="9626a-148">Run the **Initial sync** functionality for the tables that you want to sync data for.</span></span>

<span data-ttu-id="9626a-149">Hvis du vil ha koblinger til et eksempel og en alternativ tilnærming, kan du se [Eksempel](#example)-delen.</span><span class="sxs-lookup"><span data-stu-id="9626a-149">For links to an example and an alternative approach, see the [Example](#example) section.</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-an-existing-customer-engagement-app-instance"></a><a id="new-data-existing"></a><span data-ttu-id="9626a-150">En ny Finance and Operations-appforekomst som har data og en eksisterende kundeengasjementsapp-forekomst</span><span class="sxs-lookup"><span data-stu-id="9626a-150">A new Finance and Operations app instance that has data and an existing customer engagement app instance</span></span>

<span data-ttu-id="9626a-151">Hvis du vil konfigurere en dobbel skriving-tilkobling mellom en ny forekomst av en Finance and Operations-app som har data og en eksisterende forekomst av en kundeengasjementsapp, følger du fremgangsmåten i delen [En ny Finance and Operations-appforekomst og en eksisterende kundeengasjementsapp-forekomst](#new-existing) tidligere i dette emnet.</span><span class="sxs-lookup"><span data-stu-id="9626a-151">To set up a dual-write connection between a new instance of a Finance and Operations app that has data and an existing instance of a customer engagement app, follow the steps in the [A new Finance and Operations app instance and an existing customer engagement app instance](#new-existing) section earlier in this topic.</span></span> <span data-ttu-id="9626a-152">Når tilkoblingsoppsettet er fullført, følger du denne fremgangsmåten hvis du vil synkronisere dataene med kundeengasjementsappen.</span><span class="sxs-lookup"><span data-stu-id="9626a-152">When the connection setup is completed, if you want to sync the data to the customer engagement app, follow these steps.</span></span>

1. <span data-ttu-id="9626a-153">Åpne Finance and Operations-appen fra LCS-siden, logg på og gå til **Databehandling \> Dobbel skriving**.</span><span class="sxs-lookup"><span data-stu-id="9626a-153">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="9626a-154">Kjør funksjonaliteten **Innledende synkronisering** for tabellen du vil synkronisere data for.</span><span class="sxs-lookup"><span data-stu-id="9626a-154">Run the **Initial sync** functionality for the tables that you want to sync data for.</span></span>

<span data-ttu-id="9626a-155">Følg denne fremgangsmåten for å synkronisere de eksisterende Dataverse-dataene med Finance and Operations-appen.</span><span class="sxs-lookup"><span data-stu-id="9626a-155">To sync the existing Dataverse data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="9626a-156">Opprette et nytt firma i Finance and Operations-appen.</span><span class="sxs-lookup"><span data-stu-id="9626a-156">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="9626a-157">Legg til firmaet i oppsettet for dobbelt skriving-tilkobling.</span><span class="sxs-lookup"><span data-stu-id="9626a-157">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="9626a-158">[Starte opp](bootstrap-company-data.md) Dataverse-dataene ved hjelp av en ISO-firmakode på tre tegn.</span><span class="sxs-lookup"><span data-stu-id="9626a-158">[Bootstrap](bootstrap-company-data.md) the Dataverse data by using a three-letter ISO company code.</span></span>
4. <span data-ttu-id="9626a-159">Kjør funksjonaliteten **Innledende synkronisering** for tabellen du vil synkronisere data for.</span><span class="sxs-lookup"><span data-stu-id="9626a-159">Run the **Initial sync** functionality for the tables that you want to sync data for.</span></span>

<span data-ttu-id="9626a-160">Hvis du vil ha koblinger til et eksempel og en alternativ tilnærming, kan du se [Eksempel](#example)-delen.</span><span class="sxs-lookup"><span data-stu-id="9626a-160">For links to an example and an alternative approach, see the [Example](#example) section.</span></span>

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="existing-new"></a><span data-ttu-id="9626a-161">En eksisterende Finance and Operations-appforekomst og en ny kundeengasjementsapp-forekomst</span><span class="sxs-lookup"><span data-stu-id="9626a-161">An existing Finance and Operations app instance and a new customer engagement app instance</span></span>

<span data-ttu-id="9626a-162">Oppsettet av en dobbel skriving-tilkobling mellom en eksisterende forekomst av en Finance and Operations-app og en ny forekomst av en kundeengasjementsapp forekommer i Finance and Operation-miljøet.</span><span class="sxs-lookup"><span data-stu-id="9626a-162">The setup of a dual-write connection between an existing instance of a Finance and Operations app and a new instance of a customer engagement app occurs in the Finance and Operation environment.</span></span>

1. <span data-ttu-id="9626a-163">[Angi tilkoblingen fra Finance and Operations-appen](enable-dual-write.md).</span><span class="sxs-lookup"><span data-stu-id="9626a-163">[Set up the connection from the Finance and Operations app](enable-dual-write.md).</span></span>
2. <span data-ttu-id="9626a-164">Kjør funksjonaliteten **Innledende synkronisering** for tabellen du vil synkronisere data for.</span><span class="sxs-lookup"><span data-stu-id="9626a-164">Run the **Initial sync** functionality for the tables that you want to sync data for.</span></span>

<span data-ttu-id="9626a-165">Hvis du vil ha koblinger til et eksempel og en alternativ tilnærming, kan du se [Eksempel](#example)-delen.</span><span class="sxs-lookup"><span data-stu-id="9626a-165">For links to an example and an alternative approach, see the [Example](#example) section.</span></span>

## <a name="an-existing-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="existing-existing"></a><span data-ttu-id="9626a-166">En eksisterende Finance and Operations-appforekomst og en eksisterende kundeengasjementsapp-forekomst</span><span class="sxs-lookup"><span data-stu-id="9626a-166">An existing Finance and Operations app instance and an existing customer engagement app instance</span></span>

<span data-ttu-id="9626a-167">Oppsettet av en dobbel skriving-tilkobling mellom en eksisterende forekomst av en Finance and Operations-app og en eksisterende forekomst av en kundeengasjementsapp forekommer i Finance and Operation-miljøet.</span><span class="sxs-lookup"><span data-stu-id="9626a-167">The setup of a dual-write connection between an existing instance of a Finance and Operations app and an existing instance of a customer engagement app occurs in the Finance and Operation environment.</span></span>

1. <span data-ttu-id="9626a-168">[Angi tilkoblingen fra Finance and Operations-appen](enable-dual-write.md).</span><span class="sxs-lookup"><span data-stu-id="9626a-168">[Set up the connection from the Finance and Operations app](enable-dual-write.md).</span></span>
2. <span data-ttu-id="9626a-169">Hvis du vil synkronisere de eksisterende Dataverse-dataene til Finance and Operations-appen, [starter du opp](bootstrap-company-data.md) Dataverse-dataene ved hjelp av en ISO-firmakode på tre bokstaver.</span><span class="sxs-lookup"><span data-stu-id="9626a-169">To sync the existing Dataverse data to the Finance and Operations app, [bootstrap](bootstrap-company-data.md) the Dataverse data by using a three-letter ISO company code.</span></span>
3. <span data-ttu-id="9626a-170">Kjør funksjonaliteten **Innledende synkronisering** for tabellen du vil synkronisere data for.</span><span class="sxs-lookup"><span data-stu-id="9626a-170">Run the **Initial sync** functionality for the tables that you want to sync data for.</span></span>

<span data-ttu-id="9626a-171">Hvis du vil ha koblinger til et eksempel og en alternativ tilnærming, kan du se [Eksempel](#example)-delen.</span><span class="sxs-lookup"><span data-stu-id="9626a-171">For links to an example and an alternative approach, see the [Example](#example) section.</span></span>

## <a name="example"></a><span data-ttu-id="9626a-172">Eksempel</span><span class="sxs-lookup"><span data-stu-id="9626a-172">Example</span></span>

<span data-ttu-id="9626a-173">Hvis du vil ha et eksempel, kan du se [Aktivere tabelltilordningen Kunder V3 til kontakter](enable-entity-map.md#enable-table-map)</span><span class="sxs-lookup"><span data-stu-id="9626a-173">For an example, see [Enabling the Customers V3—Contacts table map](enable-entity-map.md#enable-table-map)</span></span>

<span data-ttu-id="9626a-174">Hvis du vil ha en alternativ tilnærming som er basert på datavolumer i hver enhet som må kjøre en innledende synkronisering, kan du se [Hensyn ved innledende synkronisering](initial-sync-guidance.md).</span><span class="sxs-lookup"><span data-stu-id="9626a-174">For an alternative approach that is based on data volumes in each entity that must run an initial synchronization, see [Considerations for initial synchronization](initial-sync-guidance.md).</span></span>
