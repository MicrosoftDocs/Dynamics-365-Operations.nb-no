---
title: Komme i gang med kostnadsregnskaptjenesten
description: Dette emnet inneholder lisensdetaljer og installasjonsinstruksjoner for tjenesten for kostnadsregnskap.
author: AndersGirke
manager: tfehr
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-17
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: cbbce7eaac264973bf0b95ad5175bf70ed2b4ae9
ms.sourcegitcommit: e06da171b9cba8163893e30244c52a9ce0901146
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/21/2020
ms.locfileid: "3276948"
---
# <a name="get-started-with-the-cost-accounting-service"></a><span data-ttu-id="d7a6a-103">Komme i gang med kostnadsregnskaptjenesten</span><span class="sxs-lookup"><span data-stu-id="d7a6a-103">Get started with the cost accounting service</span></span>

[!INCLUDE [banner](../includes/banner.md)]

> [!IMPORTANT]
> <span data-ttu-id="d7a6a-104">Funksjonaliteten som er nevnt i dette emnet, er tilgjengelige som en del av en privat forhåndsversjon.</span><span class="sxs-lookup"><span data-stu-id="d7a6a-104">The functionality that is described in this topic is available as part of a private preview release.</span></span> <span data-ttu-id="d7a6a-105">Innholdet i dette emnet og funksjonaliteten det beskriver, kan endres.</span><span class="sxs-lookup"><span data-stu-id="d7a6a-105">The content of this topic and the functionality that it describes are subject to change.</span></span> <span data-ttu-id="d7a6a-106">Hvis du vil ha mer informasjon om forhåndsvisning versjoner, kan du se [Vanlige spørsmål om oppdatering av én versjonstjeneste](../../fin-ops-core/fin-ops/get-started/one-version.md).</span><span class="sxs-lookup"><span data-stu-id="d7a6a-106">For more information about preview releases, see [One version service updates FAQ](../../fin-ops-core/fin-ops/get-started/one-version.md).</span></span>

<span data-ttu-id="d7a6a-107">Ved hjelp av tjenesten for kostnadsberegning kan du utføre flere lagerregnskapsforekomster i kostnadsregnskapsfinansene du har definert.</span><span class="sxs-lookup"><span data-stu-id="d7a6a-107">The cost accounting service lets you do multiple inventory accounting in the cost accounting ledgers that you've set up.</span></span> <span data-ttu-id="d7a6a-108">Du knytter hver kostnadsregnskapsfinans til en *konvensjon*.</span><span class="sxs-lookup"><span data-stu-id="d7a6a-108">You associate each cost accounting ledger with a *convention*.</span></span> <span data-ttu-id="d7a6a-109">En konvensjon er en samling av følgende typer regnskapspolicyer:</span><span class="sxs-lookup"><span data-stu-id="d7a6a-109">A convention is a collection of the following types of accounting policies:</span></span>

- <span data-ttu-id="d7a6a-110">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="d7a6a-110">Cost object</span></span>
- <span data-ttu-id="d7a6a-111">Målingsgrunnlag for inndata</span><span class="sxs-lookup"><span data-stu-id="d7a6a-111">Input measurement basis</span></span>
- <span data-ttu-id="d7a6a-112">Kostnadsflytforutsetning</span><span class="sxs-lookup"><span data-stu-id="d7a6a-112">Cost flow assumption</span></span>
- <span data-ttu-id="d7a6a-113">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="d7a6a-113">Cost element</span></span>

> [!NOTE]
> <span data-ttu-id="d7a6a-114">Selv etter at du har aktivert tjenesten for kostnadsregnskap, kan du fremdeles utføre lagerregnskap i Microsoft Dynamics 365 Supply Chain Management, som vanlig.</span><span class="sxs-lookup"><span data-stu-id="d7a6a-114">Even after you've turned on the cost accounting service, you can still do  inventory accounting in Microsoft Dynamics 365 Supply Chain Management, as usual.</span></span>

<span data-ttu-id="d7a6a-115">Kostregnskapstjenesten er et tillegg.</span><span class="sxs-lookup"><span data-stu-id="d7a6a-115">The cost accounting service is an add-in.</span></span> <span data-ttu-id="d7a6a-116">Hvis du vil gjøre funksjonene tilgjengelige, må du installere det fra Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="d7a6a-116">To makes its features available, you must install it from Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="d7a6a-117">Derfor kan du velge å evaluere den i et testmiljø før du aktiverer den for produksjonsmiljøer.</span><span class="sxs-lookup"><span data-stu-id="d7a6a-117">Therefore, you can choose to evaluate it in a test environment before you turn it on for production environments.</span></span>

<span data-ttu-id="d7a6a-118">Tjenesten for kostnadsregnskap støtter for øyeblikket ikke alle funksjonene for kostnadsstyring som er innebygd i Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="d7a6a-118">The cost accounting service doesn't currently support all the cost management features that are built into Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="d7a6a-119">Det er derfor viktig at du vurderer om funksjonssettet som for øyeblikket er tilgjengelig, oppfyller kravene dine.</span><span class="sxs-lookup"><span data-stu-id="d7a6a-119">Therefore, it's important that you evaluate whether the set of features that is currently available will meet your requirements.</span></span>

## <a name="licensing"></a><span data-ttu-id="d7a6a-120">Lisensiering</span><span class="sxs-lookup"><span data-stu-id="d7a6a-120">Licensing</span></span>

<span data-ttu-id="d7a6a-121">Kostregnskap-tjenesten lisensieres sammen med standardfunksjonene for lagerregnskap som er tilgjengelig for Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="d7a6a-121">The cost accounting service is licensed together with the standard features of inventory accounting that are available for Supply Chain Management.</span></span> <span data-ttu-id="d7a6a-122">Du trenger ikke kjøpe en tilleggslisens for å bruke tjenesten for kostnadsregnskap.</span><span class="sxs-lookup"><span data-stu-id="d7a6a-122">You don't have to purchase an additional license to use the cost accounting service.</span></span>

## <a name="install-the-add-in"></a><span data-ttu-id="d7a6a-123">Installer tillegget</span><span class="sxs-lookup"><span data-stu-id="d7a6a-123">Install the add-in</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d7a6a-124">Hvis du vil bruke tjenesten for kostnadsregnskap, må du ha et LCS-aktivert miljø med høy tilgjengelighet (ikke et OneBox-miljø), og du må kjøre Dynamics 365 Supply Chain Management versjon 10.0.11 eller senere.</span><span class="sxs-lookup"><span data-stu-id="d7a6a-124">To use the cost accounting service, you must have an LCS-enabled high-availability environment (not a OneBox environment), and you must be running Dynamics 365 Supply Chain Management version 10.0.11 or later.</span></span>

<span data-ttu-id="d7a6a-125">Hvis du vil bruke kostregnskap-tjenesten, kan du installere tillegget Supply Chain Management, som beskrevet i fremgangsmåten nedenfor.</span><span class="sxs-lookup"><span data-stu-id="d7a6a-125">To use the cost accounting service, install the cost accounting service add-in for Supply Chain Management as described in the following procedure.</span></span>

1. <span data-ttu-id="d7a6a-126">Logg på LCS.</span><span class="sxs-lookup"><span data-stu-id="d7a6a-126">Sign in to LCS.</span></span>

1. <span data-ttu-id="d7a6a-127">Gå til **Administrasjon av forhåndsvisningsfunksjoner**.</span><span class="sxs-lookup"><span data-stu-id="d7a6a-127">Go to **Preview feature management**.</span></span>

1. <span data-ttu-id="d7a6a-128">Velg plusstegnet (**+**).</span><span class="sxs-lookup"><span data-stu-id="d7a6a-128">Select the plus sign (**+**).</span></span>

1. <span data-ttu-id="d7a6a-129">I **Kode** -feltet angir du betanøkkelen for tillegget for kostregnskap-tjenesten.</span><span class="sxs-lookup"><span data-stu-id="d7a6a-129">In the **Code** field, enter your add-in beta key for the cost accounting service.</span></span> <span data-ttu-id="d7a6a-130">(Du burde ha mottatt nøkkelen via e-post.)</span><span class="sxs-lookup"><span data-stu-id="d7a6a-130">(You should have received your key by email.)</span></span>

1. <span data-ttu-id="d7a6a-131">Velg **Fjern blokkering**.</span><span class="sxs-lookup"><span data-stu-id="d7a6a-131">Select **Unblock**.</span></span>

1. <span data-ttu-id="d7a6a-132">Åpne LCS-miljøet der du vil legge til tjenesten.</span><span class="sxs-lookup"><span data-stu-id="d7a6a-132">Open the LCS environment where you want to add the service.</span></span>

1. <span data-ttu-id="d7a6a-133">Gå til **Detaljerte opplysninger**.</span><span class="sxs-lookup"><span data-stu-id="d7a6a-133">Go to **Full details**.</span></span>

1. <span data-ttu-id="d7a6a-134">Bla ned til **Miljøtillegg**-hurtigfanen.</span><span class="sxs-lookup"><span data-stu-id="d7a6a-134">Scroll down to the **Environment add-ins** FastTab.</span></span>

1. <span data-ttu-id="d7a6a-135">Velg **Installer et nytt tillegg**.</span><span class="sxs-lookup"><span data-stu-id="d7a6a-135">Select **Install a new add-in**.</span></span>

1. <span data-ttu-id="d7a6a-136">Velg **Tjeneste for kostnadsregnskap**.</span><span class="sxs-lookup"><span data-stu-id="d7a6a-136">Select **Cost accounting service**.</span></span>

1. <span data-ttu-id="d7a6a-137">Følg installasjonsveiledningen, og godta vilkårene.</span><span class="sxs-lookup"><span data-stu-id="d7a6a-137">Follow the installation guide, and agree to the terms and conditions.</span></span>

1. <span data-ttu-id="d7a6a-138">Velg **Installer**.</span><span class="sxs-lookup"><span data-stu-id="d7a6a-138">Select **Install**.</span></span>

1. <span data-ttu-id="d7a6a-139">I hurtigfanen **Miljøtillegg** skal du se at tjenesten for kostnadsregnskap blir installert.</span><span class="sxs-lookup"><span data-stu-id="d7a6a-139">On the **Environment add-ins** FastTab, you should see that the cost accounting service is being installed.</span></span> <span data-ttu-id="d7a6a-140">Etter noen minutter skal statusen endres fra **Installerer** til **Installert**.</span><span class="sxs-lookup"><span data-stu-id="d7a6a-140">After a few minutes, the status should change from **Installing** to **Installed**.</span></span> <span data-ttu-id="d7a6a-141">(Det kan hende du må oppdatere siden for å se denne endringen.) På dette tidspunktet er tjenesten for kostnadsregnskap klar til bruk.</span><span class="sxs-lookup"><span data-stu-id="d7a6a-141">(You might have to refresh the page to see this change.) At that point, the cost accounting service is ready for use.</span></span>

## <a name="set-up-the-integration"></a><span data-ttu-id="d7a6a-142">Defininere integreringen</span><span class="sxs-lookup"><span data-stu-id="d7a6a-142">Set up the integration</span></span>

<span data-ttu-id="d7a6a-143">Slik definerer du integreringen mellom kostregnskap-tjenesten og Dynamics 365 Supply Chain Management:</span><span class="sxs-lookup"><span data-stu-id="d7a6a-143">To set up the integration between the cost accounting service and Dynamics 365 Supply Chain Management:</span></span>

1. <span data-ttu-id="d7a6a-144">Gå til **Systemadministrasjon > Funksjonsbehandling**.</span><span class="sxs-lookup"><span data-stu-id="d7a6a-144">Go to **System administration > Feature Management**.</span></span>

1. <span data-ttu-id="d7a6a-145">Velg **Se etter oppdateringer**.</span><span class="sxs-lookup"><span data-stu-id="d7a6a-145">Select **Check for updates**.</span></span>

1. <span data-ttu-id="d7a6a-146">Åpne kategorien **Alle**, og søk etter funksjonen kalt *Tjeneste for kostnadsregnskap*.</span><span class="sxs-lookup"><span data-stu-id="d7a6a-146">Open the **All** tab and search for the feature named *Cost accounting service*.</span></span>

1. <span data-ttu-id="d7a6a-147">Velg **Aktiver nå**.</span><span class="sxs-lookup"><span data-stu-id="d7a6a-147">Select **Enable now**.</span></span>

1. <span data-ttu-id="d7a6a-148">Gå til **Kostnadsstyring > Tjeneste for kostnadsregnskap > Oppsett > Parametere for tjeneste for kostnadsregnskap > Integrasjonsparametere**.</span><span class="sxs-lookup"><span data-stu-id="d7a6a-148">Go to **Cost management > Cost accounting service > Setup > Cost accounting service parameters > Integrations parameters**.</span></span>

1. <span data-ttu-id="d7a6a-149">I feltet **Program-ID** angir du følgende kode:</span><span class="sxs-lookup"><span data-stu-id="d7a6a-149">In the **Application ID** field, enter the following code:</span></span><br> <span data-ttu-id="d7a6a-150">08231eb2-a501-4edb-b3c5-aede5e5e0c3f</span><span class="sxs-lookup"><span data-stu-id="d7a6a-150">08231eb2-a501-4edb-b3c5-aede5e5e0c3f</span></span>

1. <span data-ttu-id="d7a6a-151">I feltet **Datatjenestesluttpunkt** angir du følgende URL-adresse:</span><span class="sxs-lookup"><span data-stu-id="d7a6a-151">In the **Data service endpoint** field, enter the following URL:</span></span><br>https://operationsdataservice.operations365.dynamics.com/

1. <span data-ttu-id="d7a6a-152">I feltet **Sluttpunkt for tjeneste for kostnadsregnskap** angir du følgende URL-adresse:</span><span class="sxs-lookup"><span data-stu-id="d7a6a-152">In the **Cost accounting service endpoint** field, enter the following URL:</span></span><br>https://costaccountingservice.operations365.dynamics.com/

1. <span data-ttu-id="d7a6a-153">Kostregnskap-tjenesten er nå klar for bruk.</span><span class="sxs-lookup"><span data-stu-id="d7a6a-153">The cost accounting service is now ready for use.</span></span>

## <a name="related-resources"></a><span data-ttu-id="d7a6a-154">Relaterte ressurser</span><span class="sxs-lookup"><span data-stu-id="d7a6a-154">Related resources</span></span>

[<span data-ttu-id="d7a6a-155">Startside for tjeneste for kostnadsregnskap</span><span class="sxs-lookup"><span data-stu-id="d7a6a-155">Cost accounting service home page</span></span>](cost-accounting-service-home.md)
