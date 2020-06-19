---
title: Fjerne en forekomst
description: Denne artikkelen leder deg gjennom prosessen med å fjerne en testkjøring eller et produksjonsmiljø for Microsoft Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 17f299f81d1326dfb06c11a6125acc54b8ef2a6e
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/04/2020
ms.locfileid: "3431205"
---
# <a name="remove-an-instance"></a><span data-ttu-id="9b110-103">Fjerne en forekomst</span><span class="sxs-lookup"><span data-stu-id="9b110-103">Remove an instance</span></span>

<span data-ttu-id="9b110-104">Denne artikkelen leder deg gjennom prosessen med å fjerne en testkjøring eller et produksjonsmiljø for Microsoft Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="9b110-104">This article walks you through the process of removing a test drive or production environment for Microsoft Dynamics 365 Human Resources.</span></span>

## <a name="remove-a-test-drive-environment"></a><span data-ttu-id="9b110-105">Fjerne et testversjonsmiljø</span><span class="sxs-lookup"><span data-stu-id="9b110-105">Remove a test drive environment</span></span>

<span data-ttu-id="9b110-106">Testversjoner av Human Resources er klargjort med en policy for utløpsdato på 60 dagers.</span><span class="sxs-lookup"><span data-stu-id="9b110-106">Human Resources test drives are provisioned with a 60-day expiration policy.</span></span> <span data-ttu-id="9b110-107">Eiere av testversjonsmiljøer har imidlertid mulighet til å avslutte prøveversjonen tidlig ved å fullføre trinnene nedenfor.</span><span class="sxs-lookup"><span data-stu-id="9b110-107">However, owners of test drive environments have the option to end their trial early by completing the following steps.</span></span> 

1. <span data-ttu-id="9b110-108">Gå til [Power Apps-administrasjonssenteret](https://admin.businessplatform.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="9b110-108">Navigate to the [Power Apps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="9b110-109">Velg **Miljøer**.</span><span class="sxs-lookup"><span data-stu-id="9b110-109">Select **Environments**.</span></span>
3. <span data-ttu-id="9b110-110">Velg testversjonsmiljøet, som har et navngivingsmønster som ser slik ut: TestDrive - alias@domain</span><span class="sxs-lookup"><span data-stu-id="9b110-110">Select the test drive environment, which has a naming pattern similar to this: TestDrive - alias@domain</span></span>
4. <span data-ttu-id="9b110-111">Velg **Slett**, og bekreft beslutningen.</span><span class="sxs-lookup"><span data-stu-id="9b110-111">Select **Delete** and confirm the decision.</span></span> 

<span data-ttu-id="9b110-112">Det eksisterende testversjonsmiljøet fjernes.</span><span class="sxs-lookup"><span data-stu-id="9b110-112">The existing test drive environment will be removed.</span></span> <span data-ttu-id="9b110-113">Når det fjernes, kan du registrere deg for et nytt testversjonsmiljø.</span><span class="sxs-lookup"><span data-stu-id="9b110-113">When it is removed, you can sign up for a new test drive environment.</span></span> 

## <a name="remove-a-production-environment"></a><span data-ttu-id="9b110-114">Fjerne et produksjonsmiljø</span><span class="sxs-lookup"><span data-stu-id="9b110-114">Remove a production environment</span></span>

<span data-ttu-id="9b110-115">Denne artikkelen antar at du har kjøpt Human Resources gjennom en Cloud Solution Provider (CSP)- eller en enterprise architecture (EA)-avtale.</span><span class="sxs-lookup"><span data-stu-id="9b110-115">This article assumes that you've purchased Human Resources through a Cloud Solution Provider (CSP) or an enterprise architecture (EA) agreement.</span></span> 

<span data-ttu-id="9b110-116">Siden et enkelt Human Resources-miljø er inkludert i et enkelt Power Apps-miljø, finnes det to alternativer du bør vurdere.</span><span class="sxs-lookup"><span data-stu-id="9b110-116">Since a single Human Resources environment is contained within a single Power Apps environment, there are two options to consider.</span></span> <span data-ttu-id="9b110-117">Første alternativ er å fjerne hele Power Apps-miljøet. Det andre alternativet er å fjerne bare Human Resources.</span><span class="sxs-lookup"><span data-stu-id="9b110-117">The first option involves removing the entire Power Apps environment; the second option involves removing only Human Resources.</span></span> <span data-ttu-id="9b110-118">Det første alternativet bør velges når du har opprettet et Power Apps-miljø uttrykkelig for klargjøring av Human Resources, og du akkurat har begynt implementering, eller du ikke har noen etablerte integreringer.</span><span class="sxs-lookup"><span data-stu-id="9b110-118">The first option is preferred when you have created a Power Apps environment expressly for the purpose of provisioning Human Resources, and you've just begun implementation, or you don’t have any established integrations.</span></span> <span data-ttu-id="9b110-119">Det andre alternativet er riktig når du har et etablert Power Apps-miljø fylt ut med rike data som brukes i Power Apps og Power Automate.</span><span class="sxs-lookup"><span data-stu-id="9b110-119">The second option is appropriate when you have an established Power Apps environment populated with rich data that's leveraged in Power Apps and Power Automate.</span></span>

> [!Important]
> <span data-ttu-id="9b110-120">Før du fjerner Power Apps-miljøet, kontrollerer du at det ikke brukes for rike data-integreringer utenfor området for Human Resources.</span><span class="sxs-lookup"><span data-stu-id="9b110-120">Before removing the Power Apps environment, ensure it is not being used for rich data integrations outside the scope of Human Resources.</span></span> <span data-ttu-id="9b110-121">Merk også at standard Power Apps-miljøer ikke kan fjernes.</span><span class="sxs-lookup"><span data-stu-id="9b110-121">Also note that the default Power Apps environments cannot be removed.</span></span> 

<span data-ttu-id="9b110-122">Slik fjerner du hele Power Apps-miljøet, inkludert Human Resources og tilknyttede apper og flyter:</span><span class="sxs-lookup"><span data-stu-id="9b110-122">To remove the entire Power Apps environment, including Human Resources and the associated apps and flows:</span></span>

1. <span data-ttu-id="9b110-123">Gå til [Power Apps-administrasjonssenteret](https://admin.businessplatform.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="9b110-123">Navigate to the [Power Apps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="9b110-124">Velg **Miljøer**.</span><span class="sxs-lookup"><span data-stu-id="9b110-124">Select **Environments**.</span></span>
3. <span data-ttu-id="9b110-125">Velg miljøet som skal fjernes.</span><span class="sxs-lookup"><span data-stu-id="9b110-125">Select the environment to be removed.</span></span>
4. <span data-ttu-id="9b110-126">Velg **Slett**, og bekreft beslutningen.</span><span class="sxs-lookup"><span data-stu-id="9b110-126">Select **Delete** and confirm the decision.</span></span> 
5. <span data-ttu-id="9b110-127">Vent til slettingen er fullført.</span><span class="sxs-lookup"><span data-stu-id="9b110-127">Wait until the deletion is complete.</span></span>
6. <span data-ttu-id="9b110-128">Logg på [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS) ved hjelp av kontoen du brukte til å abonnere på Human Resources.</span><span class="sxs-lookup"><span data-stu-id="9b110-128">Sign in to [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS) using the account that you used to subscribe to Human Resources.</span></span> 
7. <span data-ttu-id="9b110-129">Velg Human Resources-prosjektet som inneholder miljøet.</span><span class="sxs-lookup"><span data-stu-id="9b110-129">Select the Human Resources Project that contains the environment.</span></span> 
8. <span data-ttu-id="9b110-130">I LCS prosjektet velger du flisen **Human Resources-appbehandling**.</span><span class="sxs-lookup"><span data-stu-id="9b110-130">In your LCS project, select the **Human Resources App Management** tile.</span></span> 
9. <span data-ttu-id="9b110-131">Velg forekomsten som skal fjernes.</span><span class="sxs-lookup"><span data-stu-id="9b110-131">Select the instance to remove.</span></span> 
10. <span data-ttu-id="9b110-132">Velg **Fjern forekomst**, og bekrefte beslutningen.</span><span class="sxs-lookup"><span data-stu-id="9b110-132">Select **Remove instance** and confirm your decision.</span></span>  

<span data-ttu-id="9b110-133">Hvis du vil fjerne et Human Resources-miljø fra et eksisterende Power Apps-miljø, kan du fullføre trinnene nedenfor.</span><span class="sxs-lookup"><span data-stu-id="9b110-133">To remove a Human Resources environment from an existing Power Apps environment, complete the following steps.</span></span> <span data-ttu-id="9b110-134">Legg merke til at behovet for å involvere støtte og kontakt Human Resources DevOps-teamet er midlertidig til denne funksjonen er aktivert direkte i LCS.</span><span class="sxs-lookup"><span data-stu-id="9b110-134">Note that the need to involve support and contact the Human Resources DevOps team is temporary until this feature is enabled directly in LCS.</span></span>

1. <span data-ttu-id="9b110-135">Kontakt kundestøtte for å starte en forespørsel om fjerning.</span><span class="sxs-lookup"><span data-stu-id="9b110-135">Contact Support to initiate a removal request.</span></span>
2. <span data-ttu-id="9b110-136">Kundestøtteteamet vil opprette en forespørsel om fjerning med Human Resources DevOps-teamet.</span><span class="sxs-lookup"><span data-stu-id="9b110-136">The Support team will initiate a removal request with the Human Resources DevOps team.</span></span> 
3. <span data-ttu-id="9b110-137">Fortsett etter at du får beskjed om at miljøet er fjernet.</span><span class="sxs-lookup"><span data-stu-id="9b110-137">Continue after you receive word that the environment has been removed.</span></span>
4.  <span data-ttu-id="9b110-138">Logg på LCS ved hjelp av kontoen du brukte til å abonnere på Human Resources.</span><span class="sxs-lookup"><span data-stu-id="9b110-138">Sign in to LCS using the account that you used to subscribe to Human Resources.</span></span> 
5. <span data-ttu-id="9b110-139">Velg Human Resources-prosjektet som inneholder miljøet.</span><span class="sxs-lookup"><span data-stu-id="9b110-139">Select the Human Resources project that contains the environment.</span></span> 
6. <span data-ttu-id="9b110-140">I LCS prosjektet velger du flisen **Human Resources-appbehandling**.</span><span class="sxs-lookup"><span data-stu-id="9b110-140">In your LCS project, select the **Human Resources App Management** tile.</span></span> 
7. <span data-ttu-id="9b110-141">Velg forekomsten du vil fjerne, som skal være merket med distribusjonsstatusen **Mislykket**.</span><span class="sxs-lookup"><span data-stu-id="9b110-141">Select the instance you would like to remove, which should be marked with a Deployment status of **Failed**.</span></span>
8. <span data-ttu-id="9b110-142">Velg **Fjern forekomst**, og bekrefte beslutningen.</span><span class="sxs-lookup"><span data-stu-id="9b110-142">Select **Remove instance** and confirm your decision.</span></span> 
