---
title: Initialisere utgangsverdidata i nye miljøer for detaljhandel
description: Denne artikkelen beskriver dataene som opprettes som en del av initialiseringsprosessen for Microsoft Dynamics 365 for Retail.
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailParameters
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
ms.openlocfilehash: 52f0c52748958f0bebb6c40df01cfac10c0ed427
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1556904"
---
# <a name="initialize-seed-data-in-new-retail-environments"></a><span data-ttu-id="65a61-103">Initialisere data for utgangsverdi i nye Retail-miljøer</span><span class="sxs-lookup"><span data-stu-id="65a61-103">Initialize seed data in new Retail environments</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="65a61-104">Denne artikkelen beskriver dataene som opprettes som en del av initialiseringsprosessen for Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="65a61-104">This article describes the data that's created as part of the initialization process for Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="65a61-105">Etter at detaljhandelsløsningen er distribuert via Microsoft Dynamics Lifecycle Services (LCS) må du initialisere detaljhandelskonfigurasjonen for å opprette grunnleggende konfigurasjonsdata.</span><span class="sxs-lookup"><span data-stu-id="65a61-105">After the Retail solution has been deployed through Microsoft Dynamics Lifecycle Services (LCS), you must initialize the retail configuration to create the basic configuration data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="65a61-106">Før du initialiserer detaljhandelskonfigurasjonen, må du kontrollere at du har angitt et språk og postadresse for hver juridiske enhet der du vil definere detaljhandelsbutikker.</span><span class="sxs-lookup"><span data-stu-id="65a61-106">Before you initialize the retail configuration, make sure that you've specified a language and a postal address for each legal entity where you will set up retail stores.</span></span> <span data-ttu-id="65a61-107">Dette trinnet må fullføres for hver juridiske enhet som du bruker for detaljhandel.</span><span class="sxs-lookup"><span data-stu-id="65a61-107">This step must be completed for each legal entity that you use for retail.</span></span>

<span data-ttu-id="65a61-108">Bruk følgende fremgangsmåte for å initialisere detaljhandelskonfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="65a61-108">To initialize the retail configuration, follow these steps.</span></span>

1. <span data-ttu-id="65a61-109">Start Dynamics 365 for Retail-klienten.</span><span class="sxs-lookup"><span data-stu-id="65a61-109">Start the Dynamics 365 for Retail client.</span></span>
2. <span data-ttu-id="65a61-110">Klikk **Detaljhandel** &gt; **Hovedkvarteroppsett** &gt; **Parametere** &gt; **Detaljhandelsparametere**.</span><span class="sxs-lookup"><span data-stu-id="65a61-110">Click **Retail** &gt; **Headquarters setup** &gt; **Parameters** &gt; **Retail parameters**.</span></span>
3. <span data-ttu-id="65a61-111">Klikk **Initialiser**.</span><span class="sxs-lookup"><span data-stu-id="65a61-111">Click **Initialize**.</span></span>

<span data-ttu-id="65a61-112">Initialisering oppretter følgende standardkonfigurasjonsdata:</span><span class="sxs-lookup"><span data-stu-id="65a61-112">Initialization creates the following default configuration data:</span></span>

- <span data-ttu-id="65a61-113">Detaljhandel Planlegger jobber og deljobber</span><span class="sxs-lookup"><span data-stu-id="65a61-113">Retail scheduler jobs and subjobs</span></span>
- <span data-ttu-id="65a61-114">Handelskanalskjema</span><span class="sxs-lookup"><span data-stu-id="65a61-114">Retail channel schema</span></span>
- <span data-ttu-id="65a61-115">Distribusjonstidsplaner for detaljhandel</span><span class="sxs-lookup"><span data-stu-id="65a61-115">Retail distribution schedules</span></span>
- <span data-ttu-id="65a61-116">Standard skjermoppsett, som inkluderer knappegrupper, bilder og temaer</span><span class="sxs-lookup"><span data-stu-id="65a61-116">Default screen layouts, which include button grids, images, and themes</span></span>
- <span data-ttu-id="65a61-117">Informasjon om tidssone</span><span class="sxs-lookup"><span data-stu-id="65a61-117">Time zone information</span></span>
- <span data-ttu-id="65a61-118">Salgsstedsoperasjoner</span><span class="sxs-lookup"><span data-stu-id="65a61-118">Point-of-sale (POS) operations</span></span>
- <span data-ttu-id="65a61-119">Salgsstedstillatelser</span><span class="sxs-lookup"><span data-stu-id="65a61-119">POS permissions</span></span>
- <span data-ttu-id="65a61-120">Kanalrapporter</span><span class="sxs-lookup"><span data-stu-id="65a61-120">Channel reports</span></span>
- <span data-ttu-id="65a61-121">Attributtmetadata</span><span class="sxs-lookup"><span data-stu-id="65a61-121">Attribute metadata</span></span>
- <span data-ttu-id="65a61-122">Maler for validering av enhet</span><span class="sxs-lookup"><span data-stu-id="65a61-122">Entity validation templates</span></span>
- <span data-ttu-id="65a61-123">Satsvis jobb for å tømme økthistorikk for Commerce Data Exchange</span><span class="sxs-lookup"><span data-stu-id="65a61-123">Batch job to purge Commerce Data Exchange session history</span></span>

<span data-ttu-id="65a61-124">I tillegg aktiveres logging som er knyttet til betalingskortbransjen (PCI) for Dynamics 365 for Retail-databasen.</span><span class="sxs-lookup"><span data-stu-id="65a61-124">Additionally, logging that is related to the payment card industry (PCI) is enabled for the Dynamics 365 for Retail database.</span></span>

> [!NOTE]
> <span data-ttu-id="65a61-125">Det finnes et alternativ for å konfigurere Detaljhandel Planlegger separat.</span><span class="sxs-lookup"><span data-stu-id="65a61-125">There is an option to separately configure the Retail scheduler.</span></span> <span data-ttu-id="65a61-126">Dette alternativet lar deg tilbakestille Detaljhandel Planlegger-konfigurasjonen til standardinnstillingene.</span><span class="sxs-lookup"><span data-stu-id="65a61-126">This option lets you reset the Retail scheduler configuration to its default settings.</span></span>

<span data-ttu-id="65a61-127">Når initialiseringen er fullført, må du konfigurere tilleggsdata for detaljhandel.</span><span class="sxs-lookup"><span data-stu-id="65a61-127">After initialization is completed, you must configure additional retail data.</span></span> <span data-ttu-id="65a61-128">Her er noen eksempler:</span><span class="sxs-lookup"><span data-stu-id="65a61-128">Here are some examples:</span></span>

- <span data-ttu-id="65a61-129">Detaljhandelsparametere</span><span class="sxs-lookup"><span data-stu-id="65a61-129">Retail parameters</span></span>
- <span data-ttu-id="65a61-130">Parametre for Detaljhandel Planlegger</span><span class="sxs-lookup"><span data-stu-id="65a61-130">Retail scheduler parameters</span></span>
- <span data-ttu-id="65a61-131">Detaljhandelskanaler</span><span class="sxs-lookup"><span data-stu-id="65a61-131">Retail channels</span></span>
- <span data-ttu-id="65a61-132">Kasser og enheter</span><span class="sxs-lookup"><span data-stu-id="65a61-132">Registers and devices</span></span>
- <span data-ttu-id="65a61-133">Assortement</span><span class="sxs-lookup"><span data-stu-id="65a61-133">Assortments</span></span>
