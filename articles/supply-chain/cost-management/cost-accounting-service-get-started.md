---
title: Komme i gang med kostnadsregnskaptjenesten (privat forhåndsversjon)
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
ms.openlocfilehash: a82af9e8ec1806f470103897389d0316d33a4a06
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4434309"
---
# <a name="get-started-with-the-cost-accounting-service-private-preview"></a><span data-ttu-id="86237-103">Komme i gang med kostnadsregnskaptjenesten (privat forhåndsversjon)</span><span class="sxs-lookup"><span data-stu-id="86237-103">Get started with the cost accounting service (private preview)</span></span>

[!INCLUDE [banner](../includes/banner.md)]

> [!IMPORTANT]
> <span data-ttu-id="86237-104">Funksjonaliteten som er nevnt i dette emnet, er tilgjengelige som en del av en privat forhåndsversjon.</span><span class="sxs-lookup"><span data-stu-id="86237-104">The functionality that is described in this topic is available as part of a private preview release.</span></span> <span data-ttu-id="86237-105">Innholdet i dette emnet og funksjonaliteten det beskriver, kan endres.</span><span class="sxs-lookup"><span data-stu-id="86237-105">The content of this topic and the functionality that it describes are subject to change.</span></span> <span data-ttu-id="86237-106">Hvis du vil ha mer informasjon om forhåndsvisning versjoner, kan du se [Vanlige spørsmål om oppdatering av én versjonstjeneste](../../fin-ops-core/fin-ops/get-started/one-version.md).</span><span class="sxs-lookup"><span data-stu-id="86237-106">For more information about preview releases, see [One version service updates FAQ](../../fin-ops-core/fin-ops/get-started/one-version.md).</span></span>

<span data-ttu-id="86237-107">Ved hjelp av tjenesten for kostnadsberegning kan du utføre flere lagerregnskapsforekomster i kostnadsregnskapsfinansene du har definert.</span><span class="sxs-lookup"><span data-stu-id="86237-107">The cost accounting service lets you do multiple inventory accounting in the cost accounting ledgers that you've set up.</span></span> <span data-ttu-id="86237-108">Du knytter hver kostnadsregnskapsfinans til en *konvensjon*.</span><span class="sxs-lookup"><span data-stu-id="86237-108">You associate each cost accounting ledger with a *convention*.</span></span> <span data-ttu-id="86237-109">En konvensjon er en samling av følgende typer regnskapspolicyer:</span><span class="sxs-lookup"><span data-stu-id="86237-109">A convention is a collection of the following types of accounting policies:</span></span>

- <span data-ttu-id="86237-110">Kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="86237-110">Cost object</span></span>
- <span data-ttu-id="86237-111">Målingsgrunnlag for inndata</span><span class="sxs-lookup"><span data-stu-id="86237-111">Input measurement basis</span></span>
- <span data-ttu-id="86237-112">Kostnadsflytforutsetning</span><span class="sxs-lookup"><span data-stu-id="86237-112">Cost flow assumption</span></span>
- <span data-ttu-id="86237-113">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="86237-113">Cost element</span></span>

> [!NOTE]
> <span data-ttu-id="86237-114">Selv etter at du har aktivert tjenesten for kostnadsregnskap, kan du fremdeles utføre lagerregnskap i Microsoft Dynamics 365 Supply Chain Management, som vanlig.</span><span class="sxs-lookup"><span data-stu-id="86237-114">Even after you've turned on the cost accounting service, you can still do  inventory accounting in Microsoft Dynamics 365 Supply Chain Management, as usual.</span></span>

<span data-ttu-id="86237-115">Kostregnskapstjenesten er et tillegg.</span><span class="sxs-lookup"><span data-stu-id="86237-115">The cost accounting service is an add-in.</span></span> <span data-ttu-id="86237-116">Hvis du vil gjøre funksjonene tilgjengelige, må du installere det fra Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="86237-116">To makes its features available, you must install it from Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="86237-117">Derfor kan du velge å evaluere den i et testmiljø før du aktiverer den for produksjonsmiljøer.</span><span class="sxs-lookup"><span data-stu-id="86237-117">Therefore, you can choose to evaluate it in a test environment before you turn it on for production environments.</span></span>

<span data-ttu-id="86237-118">Tjenesten for kostnadsregnskap støtter for øyeblikket ikke alle funksjonene for kostnadsstyring som er innebygd i Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="86237-118">The cost accounting service doesn't currently support all the cost management features that are built into Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="86237-119">Det er derfor viktig at du vurderer om funksjonssettet som for øyeblikket er tilgjengelig, oppfyller kravene dine.</span><span class="sxs-lookup"><span data-stu-id="86237-119">Therefore, it's important that you evaluate whether the set of features that is currently available will meet your requirements.</span></span>

## <a name="how-to-get-the-cost-accounting-service-private-preview"></a><a name="sign-up"></a><span data-ttu-id="86237-120">Få tilgang til kostnadsregnskaptjenesten (privat forhåndsversjon)</span><span class="sxs-lookup"><span data-stu-id="86237-120">How to get the cost accounting service (private preview)</span></span>

> [!IMPORTANT]
> <span data-ttu-id="86237-121">Hvis du vil bruke tjenesten for kostnadsregnskap, må du ha et LCS-aktivert miljø med høy tilgjengelighet (ikke et OneBox-miljø), og du må kjøre Dynamics 365 Supply Chain Management versjon 10.0.11 eller senere.</span><span class="sxs-lookup"><span data-stu-id="86237-121">To use the cost accounting service, you must have an LCS-enabled high-availability environment (not a OneBox environment), and you must be running Dynamics 365 Supply Chain Management version 10.0.11 or later.</span></span>

<span data-ttu-id="86237-122">Hvis du vil registrere deg for den private forhåndsversjonen av kostregnskapstjenesten, kan du sende ID-en din for LCS-miljø via e-post til [Kostnadsregnskaptjeneste (privat forhåndsversjon)](mailto:aevengir@microsoft.com?subject=Cost%20accounting%20service%20%28private%20preview%29).</span><span class="sxs-lookup"><span data-stu-id="86237-122">To sign up for the cost accounting service private preview, please send your LCS environment ID by email to [Cost accounting service (private preview)](mailto:aevengir@microsoft.com?subject=Cost%20accounting%20service%20%28private%20preview%29).</span></span> <span data-ttu-id="86237-123">Når du er godkjent for programmet, sender vi deg en oppfølging via e-post som inneholder en betanøkkel for kostnadsregnskapstjenesten.</span><span class="sxs-lookup"><span data-stu-id="86237-123">On approving you for the program, we will send you a follow up email that contains a cost accounting service beta key.</span></span> <span data-ttu-id="86237-124">Når du mottar betanøkkelen, kan du fortsette ved å [installere tillegget](#install).</span><span class="sxs-lookup"><span data-stu-id="86237-124">On receiving the beta key, you can proceed by [installing the add-in](#install).</span></span>

## <a name="licensing"></a><span data-ttu-id="86237-125">Lisensiering</span><span class="sxs-lookup"><span data-stu-id="86237-125">Licensing</span></span>

<span data-ttu-id="86237-126">Kostregnskap-tjenesten lisensieres sammen med standardfunksjonene for lagerregnskap som er tilgjengelig for Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="86237-126">The cost accounting service is licensed together with the standard features of inventory accounting that are available for Supply Chain Management.</span></span> <span data-ttu-id="86237-127">Du trenger ikke kjøpe en tilleggslisens for å bruke tjenesten for kostnadsregnskap.</span><span class="sxs-lookup"><span data-stu-id="86237-127">You don't have to purchase an additional license to use the cost accounting service.</span></span>

## <a name="install-the-add-in"></a><a name="install"></a><span data-ttu-id="86237-128">Installer tillegget</span><span class="sxs-lookup"><span data-stu-id="86237-128">Install the add-in</span></span>

<span data-ttu-id="86237-129">Hvis du vil bruke kostregnskap-tjenesten, kan du installere tillegget Supply Chain Management, som beskrevet i fremgangsmåten nedenfor.</span><span class="sxs-lookup"><span data-stu-id="86237-129">To use the cost accounting service, install the cost accounting service add-in for Supply Chain Management as described in the following procedure.</span></span>

1. <span data-ttu-id="86237-130">[Registrer deg](#sign-up) for kostnadsregnskaptjenesten (privat forhåndsversjon).</span><span class="sxs-lookup"><span data-stu-id="86237-130">[Sign up](#sign-up) for the cost accounting service (private preview).</span></span>

1. <span data-ttu-id="86237-131">Logg på LCS.</span><span class="sxs-lookup"><span data-stu-id="86237-131">Sign in to LCS.</span></span>

1. <span data-ttu-id="86237-132">Gå til **Administrasjon av forhåndsvisningsfunksjoner**.</span><span class="sxs-lookup"><span data-stu-id="86237-132">Go to **Preview feature management**.</span></span>

1. <span data-ttu-id="86237-133">Velg plusstegnet (**+**).</span><span class="sxs-lookup"><span data-stu-id="86237-133">Select the plus sign (**+**).</span></span>

1. <span data-ttu-id="86237-134">I **Kode** -feltet angir du betanøkkelen for tillegget for kostregnskap-tjenesten.</span><span class="sxs-lookup"><span data-stu-id="86237-134">In the **Code** field, enter your add-in beta key for the cost accounting service.</span></span> <span data-ttu-id="86237-135">(Du burde ha mottatt nøkkelen via e-post.)</span><span class="sxs-lookup"><span data-stu-id="86237-135">(You should have received your key by email.)</span></span>

1. <span data-ttu-id="86237-136">Velg **Fjern blokkering**.</span><span class="sxs-lookup"><span data-stu-id="86237-136">Select **Unblock**.</span></span>

1. <span data-ttu-id="86237-137">Åpne LCS-miljøet der du vil legge til tjenesten.</span><span class="sxs-lookup"><span data-stu-id="86237-137">Open the LCS environment where you want to add the service.</span></span>

1. <span data-ttu-id="86237-138">Gå til **Detaljerte opplysninger**.</span><span class="sxs-lookup"><span data-stu-id="86237-138">Go to **Full details**.</span></span>

1. <span data-ttu-id="86237-139">Bla ned til **Miljøtillegg**-hurtigfanen.</span><span class="sxs-lookup"><span data-stu-id="86237-139">Scroll down to the **Environment add-ins** FastTab.</span></span>

1. <span data-ttu-id="86237-140">Velg **Installer et nytt tillegg**.</span><span class="sxs-lookup"><span data-stu-id="86237-140">Select **Install a new add-in**.</span></span>

1. <span data-ttu-id="86237-141">Velg **Tjeneste for kostnadsregnskap**.</span><span class="sxs-lookup"><span data-stu-id="86237-141">Select **Cost accounting service**.</span></span>

1. <span data-ttu-id="86237-142">Følg installasjonsveiledningen, og godta vilkårene.</span><span class="sxs-lookup"><span data-stu-id="86237-142">Follow the installation guide, and agree to the terms and conditions.</span></span>

1. <span data-ttu-id="86237-143">Velg **Installer**.</span><span class="sxs-lookup"><span data-stu-id="86237-143">Select **Install**.</span></span>

1. <span data-ttu-id="86237-144">I hurtigfanen **Miljøtillegg** skal du se at tjenesten for kostnadsregnskap blir installert.</span><span class="sxs-lookup"><span data-stu-id="86237-144">On the **Environment add-ins** FastTab, you should see that the cost accounting service is being installed.</span></span> <span data-ttu-id="86237-145">Etter noen minutter skal statusen endres fra **Installerer** til **Installert**.</span><span class="sxs-lookup"><span data-stu-id="86237-145">After a few minutes, the status should change from **Installing** to **Installed**.</span></span> <span data-ttu-id="86237-146">(Det kan hende du må oppdatere siden for å se denne endringen.) På dette tidspunktet er tjenesten for kostnadsregnskap klar til bruk.</span><span class="sxs-lookup"><span data-stu-id="86237-146">(You might have to refresh the page to see this change.) At that point, the cost accounting service is ready for use.</span></span>

## <a name="set-up-the-integration"></a><span data-ttu-id="86237-147">Defininere integreringen</span><span class="sxs-lookup"><span data-stu-id="86237-147">Set up the integration</span></span>

<span data-ttu-id="86237-148">Slik definerer du integreringen mellom kostregnskap-tjenesten og Dynamics 365 Supply Chain Management:</span><span class="sxs-lookup"><span data-stu-id="86237-148">To set up the integration between the cost accounting service and Dynamics 365 Supply Chain Management:</span></span>

1. <span data-ttu-id="86237-149">Gå til **Systemadministrasjon > Funksjonsbehandling**.</span><span class="sxs-lookup"><span data-stu-id="86237-149">Go to **System administration > Feature Management**.</span></span>

1. <span data-ttu-id="86237-150">Velg **Se etter oppdateringer**.</span><span class="sxs-lookup"><span data-stu-id="86237-150">Select **Check for updates**.</span></span>

1. <span data-ttu-id="86237-151">Åpne kategorien **Alle**, og søk etter funksjonen kalt *Tjeneste for kostnadsregnskap*.</span><span class="sxs-lookup"><span data-stu-id="86237-151">Open the **All** tab and search for the feature named *Cost accounting service*.</span></span>

1. <span data-ttu-id="86237-152">Velg **Aktiver nå**.</span><span class="sxs-lookup"><span data-stu-id="86237-152">Select **Enable now**.</span></span>

1. <span data-ttu-id="86237-153">Gå til **Kostnadsstyring > Tjeneste for kostnadsregnskap > Oppsett > Parametere for tjeneste for kostnadsregnskap > Integrasjonsparametere**.</span><span class="sxs-lookup"><span data-stu-id="86237-153">Go to **Cost management > Cost accounting service > Setup > Cost accounting service parameters > Integrations parameters**.</span></span>

1. <span data-ttu-id="86237-154">I feltet **Program-ID** angir du følgende kode:</span><span class="sxs-lookup"><span data-stu-id="86237-154">In the **Application ID** field, enter the following code:</span></span><br> <span data-ttu-id="86237-155">08231eb2-a501-4edb-b3c5-aede5e5e0c3f</span><span class="sxs-lookup"><span data-stu-id="86237-155">08231eb2-a501-4edb-b3c5-aede5e5e0c3f</span></span>

1. <span data-ttu-id="86237-156">I feltet **Datatjenesteendepunkt** angir du følgende URL-adresse:</span><span class="sxs-lookup"><span data-stu-id="86237-156">In the **Data service endpoint** field, enter the following URL:</span></span><br>https://operationsdataservice.operations365.dynamics.com/

1. <span data-ttu-id="86237-157">I feltet **Endepunkt for tjeneste for kostnadsregnskap** angir du følgende URL-adresse:</span><span class="sxs-lookup"><span data-stu-id="86237-157">In the **Cost accounting service endpoint** field, enter the following URL:</span></span><br>https://costaccountingservice.operations365.dynamics.com/

1. <span data-ttu-id="86237-158">Kostregnskap-tjenesten er nå klar for bruk.</span><span class="sxs-lookup"><span data-stu-id="86237-158">The cost accounting service is now ready for use.</span></span>

## <a name="related-resources"></a><span data-ttu-id="86237-159">Relaterte ressurser</span><span class="sxs-lookup"><span data-stu-id="86237-159">Related resources</span></span>

[<span data-ttu-id="86237-160">Startside for tjeneste for kostnadsregnskap</span><span class="sxs-lookup"><span data-stu-id="86237-160">Cost accounting service home page</span></span>](cost-accounting-service-home.md)
