---
title: Initialisere utgangsverdidata i nye miljøer for detaljhandel
description: Denne artikkelen beskriver dataene som opprettes som en del av initialiseringsprosessen for Dynamics 365 Commerce.
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
ms.openlocfilehash: e2833c32d557ec3d2dc80808222d1d47860ce6ea
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023588"
---
# <a name="initialize-seed-data-in-new-retail-environments"></a><span data-ttu-id="bccec-103">Initialisere data for utgangsverdi i nye Retail-miljøer</span><span class="sxs-lookup"><span data-stu-id="bccec-103">Initialize seed data in new Retail environments</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="bccec-104">Denne artikkelen beskriver dataene som opprettes som en del av initialiseringsprosessen for Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="bccec-104">This article describes the data that's created as part of the initialization process for Dynamics 365 Commerce.</span></span>

<span data-ttu-id="bccec-105">Etter at handelsløsningen er distribuert via Microsoft Dynamics Lifecycle Services (LCS) må du initialisere handelskonfigurasjonen for å opprette grunnleggende konfigurasjonsdata.</span><span class="sxs-lookup"><span data-stu-id="bccec-105">After the Commerce solution has been deployed through Microsoft Dynamics Lifecycle Services (LCS), you must initialize the Commerce configuration to create the basic configuration data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bccec-106">Før du initialiserer handelskonfigurasjonen, må du kontrollere at du har angitt et språk og postadresse for hver juridiske enhet der du vil definere butikker.</span><span class="sxs-lookup"><span data-stu-id="bccec-106">Before you initialize the commerce configuration, make sure that you've specified a language and a postal address for each legal entity where you will set up stores.</span></span> <span data-ttu-id="bccec-107">Dette trinnet må fullføres for hver juridiske enhet som du bruker for handel.</span><span class="sxs-lookup"><span data-stu-id="bccec-107">This step must be completed for each legal entity that you use for commerce.</span></span>

<span data-ttu-id="bccec-108">Bruk følgende fremgangsmåte for å initialisere konfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="bccec-108">To initialize the configuration, follow these steps.</span></span>

1. <span data-ttu-id="bccec-109">Start Handel-klienten.</span><span class="sxs-lookup"><span data-stu-id="bccec-109">Start the Commerce client.</span></span>
2. <span data-ttu-id="bccec-110">Klikk på **Detaljhandel og handel** &gt; **Hovedkvarteroppsett** &gt; **Parametere** &gt; **Handelsparametere**.</span><span class="sxs-lookup"><span data-stu-id="bccec-110">Click **Retail and Commerce** &gt; **Headquarters setup** &gt; **Parameters** &gt; **Commerce parameters**.</span></span>
3. <span data-ttu-id="bccec-111">Klikk **Initialiser**.</span><span class="sxs-lookup"><span data-stu-id="bccec-111">Click **Initialize**.</span></span>

<span data-ttu-id="bccec-112">Initialisering oppretter følgende standardkonfigurasjonsdata:</span><span class="sxs-lookup"><span data-stu-id="bccec-112">Initialization creates the following default configuration data:</span></span>

- <span data-ttu-id="bccec-113">Jobber og deljobber i Handel-planlegger</span><span class="sxs-lookup"><span data-stu-id="bccec-113">Commerce scheduler jobs and subjobs</span></span>
- <span data-ttu-id="bccec-114">Handelskanalskjema</span><span class="sxs-lookup"><span data-stu-id="bccec-114">Commerce channel schema</span></span>
- <span data-ttu-id="bccec-115">Handelsdistribusjonstidsplaner</span><span class="sxs-lookup"><span data-stu-id="bccec-115">Commerce distribution schedules</span></span>
- <span data-ttu-id="bccec-116">Standard skjermoppsett, som inkluderer knappegrupper, bilder og temaer</span><span class="sxs-lookup"><span data-stu-id="bccec-116">Default screen layouts, which include button grids, images, and themes</span></span>
- <span data-ttu-id="bccec-117">Informasjon om tidssone</span><span class="sxs-lookup"><span data-stu-id="bccec-117">Time zone information</span></span>
- <span data-ttu-id="bccec-118">Salgsstedsoperasjoner</span><span class="sxs-lookup"><span data-stu-id="bccec-118">Point-of-sale (POS) operations</span></span>
- <span data-ttu-id="bccec-119">Salgsstedstillatelser</span><span class="sxs-lookup"><span data-stu-id="bccec-119">POS permissions</span></span>
- <span data-ttu-id="bccec-120">Kanalrapporter</span><span class="sxs-lookup"><span data-stu-id="bccec-120">Channel reports</span></span>
- <span data-ttu-id="bccec-121">Attributtmetadata</span><span class="sxs-lookup"><span data-stu-id="bccec-121">Attribute metadata</span></span>
- <span data-ttu-id="bccec-122">Maler for validering av enhet</span><span class="sxs-lookup"><span data-stu-id="bccec-122">Entity validation templates</span></span>
- <span data-ttu-id="bccec-123">Satsvis jobb for å tømme økthistorikk for Commerce Data Exchange</span><span class="sxs-lookup"><span data-stu-id="bccec-123">Batch job to purge Commerce Data Exchange session history</span></span>

<span data-ttu-id="bccec-124">I tillegg aktiveres logging som er knyttet til betalingskortbransjen (PCI) for Handel-databasen.</span><span class="sxs-lookup"><span data-stu-id="bccec-124">Additionally, logging that is related to the payment card industry (PCI) is enabled for the Commerce database.</span></span>

> [!NOTE]
> <span data-ttu-id="bccec-125">Det finnes et alternativ for å konfigurere Handel-planlegger separat.</span><span class="sxs-lookup"><span data-stu-id="bccec-125">There is an option to separately configure the Commerce scheduler.</span></span> <span data-ttu-id="bccec-126">Dette alternativet lar deg tilbakestille Handel-planleggerkonfigurasjonen til standardinnstillingene.</span><span class="sxs-lookup"><span data-stu-id="bccec-126">This option lets you reset the Commerce scheduler configuration to its default settings.</span></span>

<span data-ttu-id="bccec-127">Når initialiseringen er fullført, må du konfigurere tilleggsdata for handel.</span><span class="sxs-lookup"><span data-stu-id="bccec-127">After initialization is completed, you must configure additional commerce data.</span></span> <span data-ttu-id="bccec-128">Her er noen eksempler:</span><span class="sxs-lookup"><span data-stu-id="bccec-128">Here are some examples:</span></span>

- <span data-ttu-id="bccec-129">Handelsparametere</span><span class="sxs-lookup"><span data-stu-id="bccec-129">Commerce parameters</span></span>
- <span data-ttu-id="bccec-130">Parametre for planlegging av handel</span><span class="sxs-lookup"><span data-stu-id="bccec-130">Commerce scheduler parameters</span></span>
- <span data-ttu-id="bccec-131">Handelskanaler</span><span class="sxs-lookup"><span data-stu-id="bccec-131">Commerce channels</span></span>
- <span data-ttu-id="bccec-132">Kasser og enheter</span><span class="sxs-lookup"><span data-stu-id="bccec-132">Registers and devices</span></span>
- <span data-ttu-id="bccec-133">Assortement</span><span class="sxs-lookup"><span data-stu-id="bccec-133">Assortments</span></span>
