---
title: Initialisere data for utgangsverdi i nye Commerce-miljøer
description: Denne artikkelen beskriver dataene som opprettes som en del av initialiseringsprosessen for Dynamics 365 Commerce.
author: josaw1
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.custom: 49621
ms.assetid: 4dc762eb-190e-4485-8f55-b0cafc81bc37
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 9f534410b21fd97554f4e038bb14eebd5f887130
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792589"
---
# <a name="initialize-seed-data-in-new-commerce-environments"></a><span data-ttu-id="a093d-103">Initialisere data for utgangsverdi i nye Commerce-miljøer</span><span class="sxs-lookup"><span data-stu-id="a093d-103">Initialize seed data in new Commerce environments</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a093d-104">Denne artikkelen beskriver dataene som opprettes som en del av initialiseringsprosessen for Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="a093d-104">This article describes the data that's created as part of the initialization process for Dynamics 365 Commerce.</span></span>

<span data-ttu-id="a093d-105">Etter at handelsløsningen er distribuert via Microsoft Dynamics Lifecycle Services (LCS) må du initialisere handelskonfigurasjonen for å opprette grunnleggende konfigurasjonsdata.</span><span class="sxs-lookup"><span data-stu-id="a093d-105">After the Commerce solution has been deployed through Microsoft Dynamics Lifecycle Services (LCS), you must initialize the Commerce configuration to create the basic configuration data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a093d-106">Før du initialiserer handelskonfigurasjonen, må du kontrollere at du har angitt et språk og postadresse for hver juridiske enhet der du vil definere butikker.</span><span class="sxs-lookup"><span data-stu-id="a093d-106">Before you initialize the commerce configuration, make sure that you've specified a language and a postal address for each legal entity where you will set up stores.</span></span> <span data-ttu-id="a093d-107">Dette trinnet må fullføres for hver juridiske enhet som du bruker for handel.</span><span class="sxs-lookup"><span data-stu-id="a093d-107">This step must be completed for each legal entity that you use for commerce.</span></span>

<span data-ttu-id="a093d-108">Bruk følgende fremgangsmåte for å initialisere konfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="a093d-108">To initialize the configuration, follow these steps.</span></span>

1. <span data-ttu-id="a093d-109">Start Handel-klienten.</span><span class="sxs-lookup"><span data-stu-id="a093d-109">Start the Commerce client.</span></span>
2. <span data-ttu-id="a093d-110">Klikk på **Detaljhandel og handel** &gt; **Hovedkvarteroppsett** &gt; **Parametere** &gt; **Handelsparametere**.</span><span class="sxs-lookup"><span data-stu-id="a093d-110">Click **Retail and Commerce** &gt; **Headquarters setup** &gt; **Parameters** &gt; **Commerce parameters**.</span></span>
3. <span data-ttu-id="a093d-111">Klikk **Initialiser**.</span><span class="sxs-lookup"><span data-stu-id="a093d-111">Click **Initialize**.</span></span>

<span data-ttu-id="a093d-112">Initialisering oppretter følgende standardkonfigurasjonsdata:</span><span class="sxs-lookup"><span data-stu-id="a093d-112">Initialization creates the following default configuration data:</span></span>

- <span data-ttu-id="a093d-113">Jobber og deljobber i Handel-planlegger</span><span class="sxs-lookup"><span data-stu-id="a093d-113">Commerce scheduler jobs and subjobs</span></span>
- <span data-ttu-id="a093d-114">Handelskanalskjema</span><span class="sxs-lookup"><span data-stu-id="a093d-114">Commerce channel schema</span></span>
- <span data-ttu-id="a093d-115">Handelsdistribusjonstidsplaner</span><span class="sxs-lookup"><span data-stu-id="a093d-115">Commerce distribution schedules</span></span>
- <span data-ttu-id="a093d-116">Standard skjermoppsett, som inkluderer knappegrupper, bilder og temaer</span><span class="sxs-lookup"><span data-stu-id="a093d-116">Default screen layouts, which include button grids, images, and themes</span></span>
- <span data-ttu-id="a093d-117">Informasjon om tidssone</span><span class="sxs-lookup"><span data-stu-id="a093d-117">Time zone information</span></span>
- <span data-ttu-id="a093d-118">Salgsstedsoperasjoner</span><span class="sxs-lookup"><span data-stu-id="a093d-118">Point-of-sale (POS) operations</span></span>
- <span data-ttu-id="a093d-119">Salgsstedstillatelser</span><span class="sxs-lookup"><span data-stu-id="a093d-119">POS permissions</span></span>
- <span data-ttu-id="a093d-120">Kanalrapporter</span><span class="sxs-lookup"><span data-stu-id="a093d-120">Channel reports</span></span>
- <span data-ttu-id="a093d-121">Attributtmetadata</span><span class="sxs-lookup"><span data-stu-id="a093d-121">Attribute metadata</span></span>
- <span data-ttu-id="a093d-122">Maler for validering av enhet</span><span class="sxs-lookup"><span data-stu-id="a093d-122">Entity validation templates</span></span>
- <span data-ttu-id="a093d-123">Satsvis jobb for å tømme økthistorikk for Commerce Data Exchange</span><span class="sxs-lookup"><span data-stu-id="a093d-123">Batch job to purge Commerce Data Exchange session history</span></span>

<span data-ttu-id="a093d-124">I tillegg aktiveres logging som er knyttet til betalingskortbransjen (PCI) for Handel-databasen.</span><span class="sxs-lookup"><span data-stu-id="a093d-124">Additionally, logging that is related to the payment card industry (PCI) is enabled for the Commerce database.</span></span>

> [!NOTE]
> <span data-ttu-id="a093d-125">Det finnes et alternativ for å konfigurere Handel-planlegger separat.</span><span class="sxs-lookup"><span data-stu-id="a093d-125">There is an option to separately configure the Commerce scheduler.</span></span> <span data-ttu-id="a093d-126">Dette alternativet lar deg tilbakestille Handel-planleggerkonfigurasjonen til standardinnstillingene.</span><span class="sxs-lookup"><span data-stu-id="a093d-126">This option lets you reset the Commerce scheduler configuration to its default settings.</span></span>

<span data-ttu-id="a093d-127">Når initialiseringen er fullført, må du konfigurere tilleggsdata for handel.</span><span class="sxs-lookup"><span data-stu-id="a093d-127">After initialization is completed, you must configure additional commerce data.</span></span> <span data-ttu-id="a093d-128">Her er noen eksempler:</span><span class="sxs-lookup"><span data-stu-id="a093d-128">Here are some examples:</span></span>

- <span data-ttu-id="a093d-129">Handelsparametere</span><span class="sxs-lookup"><span data-stu-id="a093d-129">Commerce parameters</span></span>
- <span data-ttu-id="a093d-130">Parametre for planlegging av handel</span><span class="sxs-lookup"><span data-stu-id="a093d-130">Commerce scheduler parameters</span></span>
- <span data-ttu-id="a093d-131">Handelskanaler</span><span class="sxs-lookup"><span data-stu-id="a093d-131">Commerce channels</span></span>
- <span data-ttu-id="a093d-132">Kasser og enheter</span><span class="sxs-lookup"><span data-stu-id="a093d-132">Registers and devices</span></span>
- <span data-ttu-id="a093d-133">Assortement</span><span class="sxs-lookup"><span data-stu-id="a093d-133">Assortments</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]