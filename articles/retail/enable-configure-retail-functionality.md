---
title: "Initialisere utgangsverdidata i et nytt miljø for detaljhandel"
description: Denne artikkelen beskriver dataene som opprettes som en del av initialiseringsprosessen for Microsoft Dynamics 365 for Retail.
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 49621
ms.assetid: 4dc762eb-190e-4485-8f55-b0cafc81bc37
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 7388324fe8a9abc8fc3d723b7c8df2c73d76a2ae
ms.contentlocale: nb-no
ms.lasthandoff: 11/03/2017

---

# <a name="initialize-seed-data-in-a-new-retail-environment"></a><span data-ttu-id="13423-103">Initialisere utgangsverdidata i et nytt miljø for detaljhandel</span><span class="sxs-lookup"><span data-stu-id="13423-103">Initialize seed data in a new Retail environment</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="13423-104">Denne artikkelen beskriver dataene som opprettes som en del av initialiseringsprosessen for Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="13423-104">This article describes the data that's created as part of the initialization process for Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="13423-105">Etter at detaljhandelsløsningen er distribuert via Microsoft Dynamics Lifecycle Services (LCS) må du initialisere detaljhandelskonfigurasjonen for å opprette grunnleggende konfigurasjonsdata.</span><span class="sxs-lookup"><span data-stu-id="13423-105">After the Retail solution has been deployed through Microsoft Dynamics Lifecycle Services (LCS), you must initialize the retail configuration to create the basic configuration data.</span></span> <span data-ttu-id="13423-106">**Viktig:** Før du initialiserer detaljhandelskonfigurasjonen må du kontrollere at du har angitt et språk og postadresse for hver juridiske enhet der du vil definere detaljhandelsbutikker.</span><span class="sxs-lookup"><span data-stu-id="13423-106">**Important:** Before you initialize the retail configuration, make sure that you've specified a language and a postal address for each legal entity where you will set up retail stores.</span></span> <span data-ttu-id="13423-107">Dette trinnet må fullføres for hver juridiske enhet som du bruker for detaljhandel.</span><span class="sxs-lookup"><span data-stu-id="13423-107">This step must be completed for each legal entity that you use for retail.</span></span> <span data-ttu-id="13423-108">Bruk følgende fremgangsmåte for å initialisere detaljhandelskonfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="13423-108">To initialize the retail configuration, follow these steps.</span></span>

1.  <span data-ttu-id="13423-109">Start Dynamics 365 for Retail-klienten.</span><span class="sxs-lookup"><span data-stu-id="13423-109">Start the Dynamics 365 for Retail client.</span></span>
2.  <span data-ttu-id="13423-110">Klikk **Detaljhandel** &gt; **Hovedkvarteroppsett** &gt; **Parametere** &gt; **Detaljhandelsparametere**.</span><span class="sxs-lookup"><span data-stu-id="13423-110">Click **Retail** &gt; **Headquarters setup** &gt; **Parameters** &gt; **Retail parameters**.</span></span>
3.  <span data-ttu-id="13423-111">Klikk **Initialiser**.</span><span class="sxs-lookup"><span data-stu-id="13423-111">Click **Initialize**.</span></span>

<span data-ttu-id="13423-112">Initialisering oppretter følgende standardkonfigurasjonsdata:</span><span class="sxs-lookup"><span data-stu-id="13423-112">Initialization creates the following default configuration data:</span></span>

-   <span data-ttu-id="13423-113">Detaljhandel Planlegger jobber og deljobber</span><span class="sxs-lookup"><span data-stu-id="13423-113">Retail scheduler jobs and subjobs</span></span>
-   <span data-ttu-id="13423-114">Handelskanalskjema</span><span class="sxs-lookup"><span data-stu-id="13423-114">Retail channel schema</span></span>
-   <span data-ttu-id="13423-115">Distribusjonstidsplaner for detaljhandel</span><span class="sxs-lookup"><span data-stu-id="13423-115">Retail distribution schedules</span></span>
-   <span data-ttu-id="13423-116">Standard skjermoppsett, som inkluderer knappegrupper, bilder og temaer</span><span class="sxs-lookup"><span data-stu-id="13423-116">Default screen layouts, which include button grids, images, and themes</span></span>
-   <span data-ttu-id="13423-117">Informasjon om tidssone</span><span class="sxs-lookup"><span data-stu-id="13423-117">Time zone information</span></span>
-   <span data-ttu-id="13423-118">Salgsstedsoperasjoner</span><span class="sxs-lookup"><span data-stu-id="13423-118">Point-of-sale (POS) operations</span></span>
-   <span data-ttu-id="13423-119">Salgsstedstillatelser</span><span class="sxs-lookup"><span data-stu-id="13423-119">POS permissions</span></span>
-   <span data-ttu-id="13423-120">Kanalrapporter</span><span class="sxs-lookup"><span data-stu-id="13423-120">Channel reports</span></span>
-   <span data-ttu-id="13423-121">Attributtmetadata</span><span class="sxs-lookup"><span data-stu-id="13423-121">Attribute metadata</span></span>
-   <span data-ttu-id="13423-122">Maler for validering av enhet</span><span class="sxs-lookup"><span data-stu-id="13423-122">Entity validation templates</span></span>
-   <span data-ttu-id="13423-123">Satsvis jobb for å tømme økthistorikk for Commerce Data Exchange</span><span class="sxs-lookup"><span data-stu-id="13423-123">Batch job to purge Commerce Data Exchange session history</span></span>

<span data-ttu-id="13423-124">I tillegg aktiveres logging som er knyttet til betalingskortbransjen (PCI) for Dynamics 365 for Retail-databasen.</span><span class="sxs-lookup"><span data-stu-id="13423-124">Additionally, logging that is related to the payment card industry (PCI) is enabled for the Dynamics 365 for Retail database.</span></span> <span data-ttu-id="13423-125">**Obs!** Det finnes et alternativ for å konfigurere Detaljhandel Planlegger separat.</span><span class="sxs-lookup"><span data-stu-id="13423-125">**Note:** There is an option to separately configure the Retail scheduler.</span></span> <span data-ttu-id="13423-126">Dette alternativet lar deg tilbakestille Detaljhandel Planlegger-konfigurasjonen til standardinnstillingene.</span><span class="sxs-lookup"><span data-stu-id="13423-126">This option lets you reset the Retail scheduler configuration to its default settings.</span></span> <span data-ttu-id="13423-127">Når initialiseringen er fullført, må du konfigurere tilleggsdata for detaljhandel.</span><span class="sxs-lookup"><span data-stu-id="13423-127">After initialization is completed, you must configure additional retail data.</span></span> <span data-ttu-id="13423-128">Her er noen eksempler:</span><span class="sxs-lookup"><span data-stu-id="13423-128">Here are some examples:</span></span>

-   <span data-ttu-id="13423-129">Detaljhandelsparametere</span><span class="sxs-lookup"><span data-stu-id="13423-129">Retail parameters</span></span>
-   <span data-ttu-id="13423-130">Parametre for Detaljhandel Planlegger</span><span class="sxs-lookup"><span data-stu-id="13423-130">Retail scheduler parameters</span></span>
-   <span data-ttu-id="13423-131">Detaljhandelskanaler</span><span class="sxs-lookup"><span data-stu-id="13423-131">Retail channels</span></span>
-   <span data-ttu-id="13423-132">Kasser og enheter</span><span class="sxs-lookup"><span data-stu-id="13423-132">Registers and devices</span></span>
-   <span data-ttu-id="13423-133">Assortement</span><span class="sxs-lookup"><span data-stu-id="13423-133">Assortments</span></span>





