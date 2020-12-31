---
title: Konfigurere arbeidsflyter for godkjenning av leie
description: Emnet beskriver hvordan du definerer en godkjenningsarbeidsflyt som skal kjøres når en ny leieavtale opprettes.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 58c0fd781710b7ab8efeaa7a6874f412279a5924
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/28/2020
ms.locfileid: "4446584"
---
# <a name="set-up-lease-approval-workflows"></a><span data-ttu-id="e3020-103">Konfigurere arbeidsflyter for godkjenning av leie</span><span class="sxs-lookup"><span data-stu-id="e3020-103">Set up lease approval workflows</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e3020-104">Emnet beskriver hvordan du definerer en godkjenningsarbeidsflyt som skal kjøres når en ny leieavtale opprettes.</span><span class="sxs-lookup"><span data-stu-id="e3020-104">The topic explains how to set up an approval workflow that will run when a new lease is created.</span></span> <span data-ttu-id="e3020-105">Hvis du vil ha informasjon om hvordan du bruker arbeidsflyten, kan du se [Bruke arbeidsflyter for godkjenning av leie](use-create-lease-wrkflw.md).</span><span class="sxs-lookup"><span data-stu-id="e3020-105">For information about how to use the workflow, see [Use lease approval workflows](use-create-lease-wrkflw.md).</span></span> 

1. <span data-ttu-id="e3020-106">Gå til **Aktivaleie \> Oppsett \> Leiearbeidsflyt**.</span><span class="sxs-lookup"><span data-stu-id="e3020-106">Go to **Asset leasing \> Setup \> Lease workflow**.</span></span>
2. <span data-ttu-id="e3020-107">Velg **Ny** på siden **Leiearbeidsflyt**.</span><span class="sxs-lookup"><span data-stu-id="e3020-107">On the **Lease workflow** page, select **New**.</span></span>
3. <span data-ttu-id="e3020-108">I dialogboksen som vises, under **Arbeidsflyttype**, velger du koblingen **Leiearbeidsflyt**.</span><span class="sxs-lookup"><span data-stu-id="e3020-108">In the dialog box that appears, under **Workflow type**, select the **Lease workflow** link.</span></span>

    <span data-ttu-id="e3020-109">Programmet åpnes.</span><span class="sxs-lookup"><span data-stu-id="e3020-109">The application is opened.</span></span> <span data-ttu-id="e3020-110">Når den har kjørt, må du logge på Azure Active Directory (Azure AD) for å omadressert til arbeidsflytprogrammet.</span><span class="sxs-lookup"><span data-stu-id="e3020-110">After it runs, sign in to Azure Active Directory (Azure AD) to be redirected to the workflow application.</span></span>

4. <span data-ttu-id="e3020-111">Dra elementet for **Godkjenningsarbeidsflyt for leie** til arbeidsflyten.</span><span class="sxs-lookup"><span data-stu-id="e3020-111">Drag the **Lease workflow approval** element onto the workflow.</span></span>
5. <span data-ttu-id="e3020-112">Koble én node fra **Start** til **Godkjenningsarbeidsflyt for leie**.</span><span class="sxs-lookup"><span data-stu-id="e3020-112">Connect one node from **Start** to **Lease workflow approval**.</span></span> <span data-ttu-id="e3020-113">Deretter kobler du **Godkjenningsarbeidsflyt for leie** til **Slutt**.</span><span class="sxs-lookup"><span data-stu-id="e3020-113">Then connect **Lease workflow approval** to **End**.</span></span>
6. <span data-ttu-id="e3020-114">Dobbeltklikk på **Godkjenningsarbeidsflyt for leie**.</span><span class="sxs-lookup"><span data-stu-id="e3020-114">Double-click **Lease workflow approval**.</span></span>
7. <span data-ttu-id="e3020-115">Velg **Egenskaper** og deretter, under **Grunnleggende innstillinger**, angir du navnet på arbeidsflyten.</span><span class="sxs-lookup"><span data-stu-id="e3020-115">Select **Properties**, and then, under **Basic settings**, enter a name for the workflow.</span></span>

    <span data-ttu-id="e3020-116">På denne siden kan du også angi flere parametere for arbeidsflyten.</span><span class="sxs-lookup"><span data-stu-id="e3020-116">On this page, you can also set more parameters for the workflow.</span></span> <span data-ttu-id="e3020-117">Hvis du har aktivert **Automatiske handlinger**, vil systemet automatisk utføre en bestemt handling.</span><span class="sxs-lookup"><span data-stu-id="e3020-117">If you've turned on **Automatic actions**, the system will automatically take a specific action.</span></span> <span data-ttu-id="e3020-118">Du kan sende varslinger hvis de er angitt i kategorien **Varslinger**. I kategorien **Avanserte innstillinger** kan du angi en endelig godkjenner, angi en tidsgrense og angi bestemte handlinger som må fullføres.</span><span class="sxs-lookup"><span data-stu-id="e3020-118">Notifications can be sent if they are specified on the **Notifications** tab. On the **Advanced settings** tab, you can specify a final approver, set a time limit, and designate specific actions that must be completed.</span></span>

8. <span data-ttu-id="e3020-119">Når du er ferdig med å angi arbeidsflytparametere, velger du **Lukk**.</span><span class="sxs-lookup"><span data-stu-id="e3020-119">When you've finished setting the workflow parameters, select **Close**.</span></span>
9. <span data-ttu-id="e3020-120">Velg **Trinn 1**, og velg deretter **Egenskaper**.</span><span class="sxs-lookup"><span data-stu-id="e3020-120">Select **Step 1**, and then select **Properties**.</span></span>
10. <span data-ttu-id="e3020-121">Under **Grunnleggende innstillinger** skriver du inn et navn på trinnet, oppretter en emnelinje for godkjenningen og angir instruksjoner for godkjenningen.</span><span class="sxs-lookup"><span data-stu-id="e3020-121">Under **Basic settings**, enter a name for the step, create a subject line for the approval, and specify instructions for the approval.</span></span>
11. <span data-ttu-id="e3020-122">På siden **Tilordning** velger du tilordningstypen.</span><span class="sxs-lookup"><span data-stu-id="e3020-122">On the **Assignment** page, select the assignment type.</span></span>
12. <span data-ttu-id="e3020-123">Hvis du vil tilordne bestemte brukere til godkjenningen, velger **Bruker**, velger brukerne som godkjenner leieavtaler, og deretter velger du **Lukk**.</span><span class="sxs-lookup"><span data-stu-id="e3020-123">To assign specific users to the approval, select **User**, select the users who approve leases, and then select **Close**.</span></span>
13. <span data-ttu-id="e3020-124">Velg **Lagre og Lukk** for å opprette arbeidsflyten.</span><span class="sxs-lookup"><span data-stu-id="e3020-124">Select **Save and close** to create the workflow.</span></span> <span data-ttu-id="e3020-125">Deretter velger du **OK** når du blir bedt om det.</span><span class="sxs-lookup"><span data-stu-id="e3020-125">Then, when you're prompted, select **OK**.</span></span>
14. <span data-ttu-id="e3020-126">Velg **Lukk** på siden **Opprett arbeidsflyt**.</span><span class="sxs-lookup"><span data-stu-id="e3020-126">On the **Create workflow** page, select **Close**.</span></span>
14. <span data-ttu-id="e3020-127">Velg den nye arbeidsflyten, og velg deretter **Versjoner**.</span><span class="sxs-lookup"><span data-stu-id="e3020-127">Select the new workflow, and then select **Versions**.</span></span> <span data-ttu-id="e3020-128">Velg deretter **Gjør aktiv** for å sikre at arbeidsflyten er aktiv.</span><span class="sxs-lookup"><span data-stu-id="e3020-128">Then select **Make active** to ensure that the workflow is active.</span></span>
15. <span data-ttu-id="e3020-129">Velg **Lukk**.</span><span class="sxs-lookup"><span data-stu-id="e3020-129">Select **Close**.</span></span> <span data-ttu-id="e3020-130">Den nye aktive versjonen vises.</span><span class="sxs-lookup"><span data-stu-id="e3020-130">The new active version appears.</span></span>
