---
title: Lagre oppgaveveiledninger i LCS og spille dem av på nytt
description: Denne artikkelen forklarer hvordan du lagrer oppgaveveiledninger til Microsoft Dynamics Lifecycle Services (LCS) og deretter spiller dem av på nytt.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 7d6102bafc9b55f9eff05bfc4a63c177c6548694
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/17/2021
ms.locfileid: "5463268"
---
# <a name="save-task-guides-to-lcs-and-replay-them"></a><span data-ttu-id="74c09-103">Lagre oppgaveveiledninger i LCS og spille dem av på nytt</span><span class="sxs-lookup"><span data-stu-id="74c09-103">Save task guides to LCS and replay them</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="74c09-104">**Miljødetaljer**</span><span class="sxs-lookup"><span data-stu-id="74c09-104">**Environment details**</span></span> 

<span data-ttu-id="74c09-105">Microsoft Dynamics 365 Human Resources, som ble distribuert via Microsoft Dynamics Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="74c09-105">Microsoft Dynamics 365 Human Resources, which was deployed via Microsoft Dynamics Lifecycle Services (LCS)</span></span>

<span data-ttu-id="74c09-106">**Avgang**</span><span class="sxs-lookup"><span data-stu-id="74c09-106">**Issue**</span></span>

<span data-ttu-id="74c09-107">Kunden ønsker å lagre nye oppgaveopptak til vedkommendes LCS-prosjekt og deretter spille av de lagrede oppgaveveiledningene på nytt.</span><span class="sxs-lookup"><span data-stu-id="74c09-107">The customer wants to save new task recordings to his or her LCS project, and then replay the saved task guides.</span></span>

<span data-ttu-id="74c09-108">**Oppløsning**</span><span class="sxs-lookup"><span data-stu-id="74c09-108">**Resolution**</span></span>

<span data-ttu-id="74c09-109">Følg disse trinnene for å lagre oppgaveopptak til LCS.</span><span class="sxs-lookup"><span data-stu-id="74c09-109">Follow these steps to save a task recording to LCS.</span></span>

1. <span data-ttu-id="74c09-110">Logg på LCS, og velg prosjektet.</span><span class="sxs-lookup"><span data-stu-id="74c09-110">Sign in to LCS, and select the project.</span></span>
2. <span data-ttu-id="74c09-111">Velg **Forretningsprosessmodelerer**-flisen.</span><span class="sxs-lookup"><span data-stu-id="74c09-111">Select the **Business process modeler** tile.</span></span>
3. <span data-ttu-id="74c09-112">Vis denne siden i den "oppdaterte BPM-opplevelsen".</span><span class="sxs-lookup"><span data-stu-id="74c09-112">View the page in the "Updated BPM experience."</span></span>
4. <span data-ttu-id="74c09-113">Velg et bibliotek, og velg deretter **Kopier**.</span><span class="sxs-lookup"><span data-stu-id="74c09-113">Select a library, and then select **Copy**.</span></span>
5. <span data-ttu-id="74c09-114">Angi et navn for Forretningsprosessmodelerer-modellen (BPM).</span><span class="sxs-lookup"><span data-stu-id="74c09-114">Enter a name for the Business process modeler (BPM) model.</span></span>
6. <span data-ttu-id="74c09-115">Logg på Human Resources fra LCS.</span><span class="sxs-lookup"><span data-stu-id="74c09-115">Sign in to Human Resources from LCS.</span></span>
7. <span data-ttu-id="74c09-116">I **Søk**-feltet angir du **Hjelp**.</span><span class="sxs-lookup"><span data-stu-id="74c09-116">In the **Search** field, enter **help**.</span></span> <span data-ttu-id="74c09-117">Lifecycle Services-hjelpen åpnes.</span><span class="sxs-lookup"><span data-stu-id="74c09-117">Lifecycle Services Help is opened.</span></span>
8. <span data-ttu-id="74c09-118">Velg knappen **Oppdater** for konfigurasjon av Lifecycle Services-hjelpen.</span><span class="sxs-lookup"><span data-stu-id="74c09-118">Select the **Refresh** button for Lifecycle Services Help configuration.</span></span>

    <span data-ttu-id="74c09-119">Det nye BPM-biblioteket skal vises, og det skal være aktivt.</span><span class="sxs-lookup"><span data-stu-id="74c09-119">Your new BPM library should appear, and it should be active.</span></span>

9. <span data-ttu-id="74c09-120">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="74c09-120">Close the page.</span></span>
10. <span data-ttu-id="74c09-121">Opprett et oppgaveopptak.</span><span class="sxs-lookup"><span data-stu-id="74c09-121">Create a task recording.</span></span>
11. <span data-ttu-id="74c09-122">Når du er ferdig, velger **Lagre i Lifecycle Services**.</span><span class="sxs-lookup"><span data-stu-id="74c09-122">When you've finished, select **Save to Lifecycle Services**.</span></span>

    ![Lagre i Lifecycle Services](media/task-guides.png)

12. <span data-ttu-id="74c09-124">Velg BPM-biblioteket og noden for å lagre oppgaveopptaket.</span><span class="sxs-lookup"><span data-stu-id="74c09-124">Select the BPM library and node to save the task recording to.</span></span>

<span data-ttu-id="74c09-125">Følg denne fremgangsmåten for å spille av en oppgaveveiledningen på nytt fra LCS.</span><span class="sxs-lookup"><span data-stu-id="74c09-125">Follow these steps to replay a task guide from LCS.</span></span>

1. <span data-ttu-id="74c09-126">Start oppgaveopptakeren.</span><span class="sxs-lookup"><span data-stu-id="74c09-126">Start Task recorder.</span></span>
2. <span data-ttu-id="74c09-127">Velg **Åpne fra LCS**.</span><span class="sxs-lookup"><span data-stu-id="74c09-127">Select **Open from LCS**.</span></span>
3. <span data-ttu-id="74c09-128">Velg biblioteket og BPM-noden som har den lagrede oppgaveveiledningen.</span><span class="sxs-lookup"><span data-stu-id="74c09-128">Select the library and the BPM node that have the saved task guide.</span></span>
4. <span data-ttu-id="74c09-129">Åpne oppgaveveiledningen.</span><span class="sxs-lookup"><span data-stu-id="74c09-129">Open the task guide.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]