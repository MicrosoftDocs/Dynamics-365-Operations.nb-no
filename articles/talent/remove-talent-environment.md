---
title: "Fjerne Talent-miljøer"
description: "Dette emnet leder deg gjennom prosessen med å fjerne en testversjon eller et produksjonsmiljø for Microsoft Dynamics 365 for Talent."
author: rschloma
manager: AnnBe
ms.date: 11/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Talent
ms.custom: 17271
ms.assetid: ba1ad49d-8232-400e-b11f-525423506a3f
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2017-11-20
ms.dyn365.ops.version: Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 965826f5fddc2f53f33157434929eb265979376e
ms.openlocfilehash: e0422a5b7ac227ad03ccafb4e34e614dc770a363
ms.contentlocale: nb-no
ms.lasthandoff: 09/17/2018

---
# <a name="remove-talent-environments"></a><span data-ttu-id="19ebf-103">Fjerne Talent-miljøer</span><span class="sxs-lookup"><span data-stu-id="19ebf-103">Remove Talent environments</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="19ebf-104">Dette emnet leder deg gjennom prosessen med å fjerne en testversjon eller et produksjonsmiljø for Microsoft Dynamics 365 for Talent.</span><span class="sxs-lookup"><span data-stu-id="19ebf-104">This topic walks you through the process of removing a test drive or production environment for Microsoft Dynamics 365 for Talent.</span></span>

## <a name="removing-a-test-drive-environment"></a><span data-ttu-id="19ebf-105">Fjerne et testversjonsmiljø</span><span class="sxs-lookup"><span data-stu-id="19ebf-105">Removing a test drive environment</span></span>

<span data-ttu-id="19ebf-106">Testversjoner av Talent er klargjort med en policy for utløpsdato på 60 dagers.</span><span class="sxs-lookup"><span data-stu-id="19ebf-106">Talent test drives are provisioned with a 60-day expiration policy.</span></span> <span data-ttu-id="19ebf-107">Eiere av testversjonsmiljøer har imidlertid mulighet til å avslutte prøveversjonen tidlig ved å fullføre trinnene nedenfor.</span><span class="sxs-lookup"><span data-stu-id="19ebf-107">However, owners of test drive environments have the option to end their trial early by completing the following steps.</span></span> 

1. <span data-ttu-id="19ebf-108">Gå til [PowerApps-administrasjonssenteret](https://admin.businessplatform.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="19ebf-108">Navigate to the [PowerApps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="19ebf-109">Velg **Miljøer**.</span><span class="sxs-lookup"><span data-stu-id="19ebf-109">Select **Environments**.</span></span>
3. <span data-ttu-id="19ebf-110">Velg testversjonsmiljøet, som har et navngivingsmønster som ser slik ut: TestDrive - alias@domain</span><span class="sxs-lookup"><span data-stu-id="19ebf-110">Select the test drive environment, which has a naming pattern similar to this: TestDrive - alias@domain</span></span>
4. <span data-ttu-id="19ebf-111">Velg **Slett**, og bekreft beslutningen.</span><span class="sxs-lookup"><span data-stu-id="19ebf-111">Select **Delete** and confirm the decision.</span></span> 

<span data-ttu-id="19ebf-112">Det eksisterende testversjonsmiljøet fjernes.</span><span class="sxs-lookup"><span data-stu-id="19ebf-112">The existing test drive environment will be removed.</span></span> <span data-ttu-id="19ebf-113">Når det fjernes, kan du registrere deg for et nytt testversjonsmiljø.</span><span class="sxs-lookup"><span data-stu-id="19ebf-113">When it is removed, you can sign up for a new test drive environment.</span></span> 

## <a name="removing-a-production-environment"></a><span data-ttu-id="19ebf-114">Fjerne et produksjonsmiljø</span><span class="sxs-lookup"><span data-stu-id="19ebf-114">Removing a production environment</span></span>

<span data-ttu-id="19ebf-115">Dette emnet antar at du har kjøpt Talent gjennom en Cloud Solution Provider (CSP)- or enterprise architecture (EA)-avtale.</span><span class="sxs-lookup"><span data-stu-id="19ebf-115">This topic assumes that you've purchased Talent through a Cloud Solution Provider (CSP) or an enterprise architecture (EA) agreement.</span></span> 

<span data-ttu-id="19ebf-116">Siden et enkelt Talent-miljø er inkludert i et enkelt PowerApps-miljø, finnes det to alternativer du bør vurdere.</span><span class="sxs-lookup"><span data-stu-id="19ebf-116">Since a single Talent environment is “contained” within a single PowerApps environment, there are two options to consider.</span></span> <span data-ttu-id="19ebf-117">Første alternativ er å fjerne hele PowerApps-miljøet. Det andre alternativet er å fjerne bare Talent.</span><span class="sxs-lookup"><span data-stu-id="19ebf-117">The first option involves removing the entire PowerApps environment; the second option involves removing only Talent.</span></span> <span data-ttu-id="19ebf-118">Det første alternativet bør velges når du har opprettet et PowerApps-miljø uttrykkelig for klargjøring av Talent, og du akkurat har begynt implementering, eller du ikke har noen etablerte integreringer.</span><span class="sxs-lookup"><span data-stu-id="19ebf-118">The first option is preferred when you have created a PowerApps environment expressly for the purpose of provisioning Talent, and you've just begun implementation, or you don’t have any established integrations.</span></span> <span data-ttu-id="19ebf-119">Det andre alternativet er riktig når du har et etablert PowerApps-miljø fylt ut med rike data som brukes i PowerApps og flyter.</span><span class="sxs-lookup"><span data-stu-id="19ebf-119">The second option is appropriate when you have an established PowerApps environment populated with rich data that's leveraged in PowerApps and Flows.</span></span>

> [!Important]
> <span data-ttu-id="19ebf-120">Før du fjerner PowerApps-miljøet, kontrollerer du at det ikke brukes for rike data-integreringer utenfor området for Talent.</span><span class="sxs-lookup"><span data-stu-id="19ebf-120">Before removing the PowerApps environment, ensure it is not being used for rich data integrations outside the scope of Talent.</span></span> <span data-ttu-id="19ebf-121">Merk også at standard PowerApps-miljøer ikke kan fjernes.</span><span class="sxs-lookup"><span data-stu-id="19ebf-121">Also note that the default PowerApps environments cannot be removed.</span></span> 

<span data-ttu-id="19ebf-122">Slik fjerner du hele PowerApps-miljøet, inkludert Talent og tilknyttede apper og flyter:</span><span class="sxs-lookup"><span data-stu-id="19ebf-122">To remove the entire PowerApps environment, including Talent and the associated Apps and Flows:</span></span>

1. <span data-ttu-id="19ebf-123">Gå til [PowerApps-administrasjonssenteret](https://admin.businessplatform.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="19ebf-123">Navigate to the [PowerApps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="19ebf-124">Velg **Miljøer**.</span><span class="sxs-lookup"><span data-stu-id="19ebf-124">Select **Environments**.</span></span>
3. <span data-ttu-id="19ebf-125">Velg miljøet som skal fjernes.</span><span class="sxs-lookup"><span data-stu-id="19ebf-125">Select the environment to be removed.</span></span>
4. <span data-ttu-id="19ebf-126">Velg **Slett**, og bekreft beslutningen.</span><span class="sxs-lookup"><span data-stu-id="19ebf-126">Select **Delete** and confirm the decision.</span></span> 
5. <span data-ttu-id="19ebf-127">Vent til slettingen er fullført.</span><span class="sxs-lookup"><span data-stu-id="19ebf-127">Wait until the deletion is complete.</span></span>
6. <span data-ttu-id="19ebf-128">Logg på [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS) ved hjelp av kontoen du brukte til å abonnere på Talent.</span><span class="sxs-lookup"><span data-stu-id="19ebf-128">Sign in to [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS) using the account that you used to subscribe to Talent.</span></span> 
7. <span data-ttu-id="19ebf-129">Velg Talent-prosjektet som inneholder miljøet.</span><span class="sxs-lookup"><span data-stu-id="19ebf-129">Select the Talent Project that contains the environment.</span></span> 
8. <span data-ttu-id="19ebf-130">I LCS prosjektet velger du flisen **Talent-appbehandling**.</span><span class="sxs-lookup"><span data-stu-id="19ebf-130">In your LCS project, select the **Talent App Management** tile.</span></span> 
9. <span data-ttu-id="19ebf-131">Velg forekomsten som skal fjernes.</span><span class="sxs-lookup"><span data-stu-id="19ebf-131">Select the instance to remove.</span></span> 
10. <span data-ttu-id="19ebf-132">Velg **Fjern forekomst**, og bekrefte beslutningen.</span><span class="sxs-lookup"><span data-stu-id="19ebf-132">Select **Remove instance** and confirm your decision.</span></span>  

<span data-ttu-id="19ebf-133">Hvis du vil fjerne et Talent-miljø fra et eksisterende PowerApps-miljø, kan du fullføre trinnene nedenfor.</span><span class="sxs-lookup"><span data-stu-id="19ebf-133">To remove a Talent environment from an existing PowerApps environment, complete the following steps.</span></span> <span data-ttu-id="19ebf-134">Legg merke til at behovet for å involvere støtte og kontakt Talent DevOps-teamet er midlertidig til denne funksjonen er aktivert direkte i LCS.</span><span class="sxs-lookup"><span data-stu-id="19ebf-134">Note that the need to involve support and contact the Talent DevOps team is temporary until this feature is enabled directly in LCS.</span></span>

1. <span data-ttu-id="19ebf-135">Kontakt kundestøtte for å starte en forespørsel om fjerning.</span><span class="sxs-lookup"><span data-stu-id="19ebf-135">Contact Support to initiate a removal request.</span></span>
2. <span data-ttu-id="19ebf-136">Kundestøtteteamet vil opprette en forespørsel om fjerning med Talent DevOps-teamet.</span><span class="sxs-lookup"><span data-stu-id="19ebf-136">The Support team will initiate a removal request with the Talent DevOps team.</span></span> 
3. <span data-ttu-id="19ebf-137">Fortsett etter at du får beskjed om at miljøet er fjernet.</span><span class="sxs-lookup"><span data-stu-id="19ebf-137">Continue after you receive word that the environment has been removed.</span></span>
4.  <span data-ttu-id="19ebf-138">Logg på LCS ved hjelp av kontoen du brukte til å abonnere på Talent.</span><span class="sxs-lookup"><span data-stu-id="19ebf-138">Sign in to LCS using the account that you used to subscribe to Talent.</span></span> 
5. <span data-ttu-id="19ebf-139">Velg Talent-prosjektet som inneholder miljøet.</span><span class="sxs-lookup"><span data-stu-id="19ebf-139">Select the Talent project that contains the environment.</span></span> 
6. <span data-ttu-id="19ebf-140">I LCS prosjektet velger du flisen **Talent-appbehandling**.</span><span class="sxs-lookup"><span data-stu-id="19ebf-140">In your LCS project, select the **Talent App Management** tile.</span></span> 
7. <span data-ttu-id="19ebf-141">Velg forekomsten du vil fjerne, som skal være merket med distribusjonsstatusen **Mislykket**.</span><span class="sxs-lookup"><span data-stu-id="19ebf-141">Select the instance you would like to remove, which should be marked with a Deployment status of **Failed**.</span></span>
8. <span data-ttu-id="19ebf-142">Velg **Fjern forekomst**, og bekrefte beslutningen.</span><span class="sxs-lookup"><span data-stu-id="19ebf-142">Select **Remove instance** and confirm your decision.</span></span> 


