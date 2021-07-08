---
title: Arbeidsflyter for rabattbehandlingsavtale
description: Dette emnet beskriver hvordan du konfigurerer en arbeidsflyt for rabattbehandlingsavtale for å godkjenne og aktivere avtaler.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 8436842b4f07ba000649075198bdef43ad508f8f
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/17/2021
ms.locfileid: "6270963"
---
# <a name="rebate-management-deal-workflows"></a><span data-ttu-id="87d74-103">Arbeidsflyter for rabattbehandlingsavtale</span><span class="sxs-lookup"><span data-stu-id="87d74-103">Rebate management deal workflows</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="87d74-104">Når du skal godkjenne rabattavtaler, bruker Rabattbehandling den samme arbeidsflytplattformen som andre Finance and Operations-apper.</span><span class="sxs-lookup"><span data-stu-id="87d74-104">To approve rebate deals, Rebate management uses the same workflow platform as other Finance and Operations apps.</span></span> <span data-ttu-id="87d74-105">To jobbprosesser er tilknyttet hver arbeidsflyt:</span><span class="sxs-lookup"><span data-stu-id="87d74-105">Two job processes are associated with every workflow:</span></span>

- <span data-ttu-id="87d74-106">Ett av elementene i arbeidsflyten godkjenner avtalen.</span><span class="sxs-lookup"><span data-stu-id="87d74-106">One element of the workflow approves the deal.</span></span>
- <span data-ttu-id="87d74-107">Ett av elementene i arbeidsflyten aktiverer avtalen, slik at bruker- eller arbeidsflytprosessen kan godkjenne transaksjonene.</span><span class="sxs-lookup"><span data-stu-id="87d74-107">One element of the workflow activates the deal so that the user or workflow process can approve the transactions.</span></span>

<span data-ttu-id="87d74-108">Før du kan bruke en rabattavtale, må den være aktiv i **Rabattbehandling**-modulen.</span><span class="sxs-lookup"><span data-stu-id="87d74-108">Before you can use a rebate deal, it must be active in the **Rebate management** module.</span></span> <span data-ttu-id="87d74-109">Hvis du vil aktivere en avtale, må du først opprette og konfigurere en *arbeidsflyt for rabattbehandlingsavtale*.</span><span class="sxs-lookup"><span data-stu-id="87d74-109">To activate a deal, you must first create and configure a *Rebate management deal workflow*.</span></span>

<span data-ttu-id="87d74-110">Brukere kan ikke godkjenne avtaler manuelt.</span><span class="sxs-lookup"><span data-stu-id="87d74-110">Users can't manually approve deals.</span></span> <span data-ttu-id="87d74-111">Arbeidsflyten må alltid brukes.</span><span class="sxs-lookup"><span data-stu-id="87d74-111">The workflow must always be used.</span></span>

## <a name="create-and-manage-rebate-management-deal-workflows"></a><span data-ttu-id="87d74-112">Opprett og administrer arbeidsflyter for rabattbehandlingsavtale</span><span class="sxs-lookup"><span data-stu-id="87d74-112">Create and manage Rebate management deal workflows</span></span>

<span data-ttu-id="87d74-113">For å arbeide med arbeidsflyter for rabattbehandlingsavtale må du gå til **Rabattbehandling \> Oppsett \> Arbeidsflyter for rabattbehandling**.</span><span class="sxs-lookup"><span data-stu-id="87d74-113">To work with your Rebate management deal workflows, go to **Rebate management \> Setup \> Rebate management workflows**.</span></span> <span data-ttu-id="87d74-114">Der kan du vise, opprette og oppdatere arbeidsflyter etter behov.</span><span class="sxs-lookup"><span data-stu-id="87d74-114">There, you can view, create, and update workflows as required.</span></span> <span data-ttu-id="87d74-115">Bare én arbeidsflyt av denne typen kan være aktiv om gangen.</span><span class="sxs-lookup"><span data-stu-id="87d74-115">Only one workflow of this type can be active at a time.</span></span> <span data-ttu-id="87d74-116">Hvis du vil ha mer informasjon om arbeidsflyter, hvordan du arbeider med siden **Arbeidsflyter for rabattbehandling** og hvordan du oppretter arbeidsflyter, kan du se [Oversikt over arbeidsflytsystem](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md) og de relaterte emnene.</span><span class="sxs-lookup"><span data-stu-id="87d74-116">For more information about workflows, how to work with the **Rebate management workflows** page, and how to create workflows, see [Workflow system overview](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md) and its related topics.</span></span>

## <a name="use-a-workflow-to-activate-a-deal"></a><span data-ttu-id="87d74-117">Bruk en arbeidsflyt til å aktivere en avtale</span><span class="sxs-lookup"><span data-stu-id="87d74-117">Use a workflow to activate a deal</span></span>

<span data-ttu-id="87d74-118">Hvis du vil aktivere en avtale via en arbeidsflyt, åpner du avtalen (for eksempel på siden **Alle rabattbehandlingsavtaler**).</span><span class="sxs-lookup"><span data-stu-id="87d74-118">To activate a deal through a workflow, open the deal (for example, on the **All rebate management deals** page).</span></span> <span data-ttu-id="87d74-119">Velg deretter **Arbeidsflyt \> Send inn** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="87d74-119">Then, on the Action Pane, select **Workflow \> Submit**.</span></span> <span data-ttu-id="87d74-120">Etter at den nye avtalen er behandlet og godkjent via arbeidsflyten, vil den være aktiv og klar til bruk.</span><span class="sxs-lookup"><span data-stu-id="87d74-120">After the new deal has been processed and approved through the workflow, it will be active and ready to use.</span></span>

<span data-ttu-id="87d74-121">Når en avtale er aktivert, kan du ikke endre mesteparten av oppsettet.</span><span class="sxs-lookup"><span data-stu-id="87d74-121">After a deal has been activated, you can't change most of its setup.</span></span> <span data-ttu-id="87d74-122">Hvis du må endre en aktiv avtale, må du først deaktivere den og deretter opprette en ny avtale.</span><span class="sxs-lookup"><span data-stu-id="87d74-122">If you must change an active deal, first inactivate it, and then create a new deal.</span></span> <span data-ttu-id="87d74-123">Hvis den nye avtalen kommer til å ligne på den gamle avtalen, kan du opprette den ved å kopiere den gamle avtalen.</span><span class="sxs-lookup"><span data-stu-id="87d74-123">If the new deal will resemble the old deal, you can create it by copying the old deal.</span></span>

<span data-ttu-id="87d74-124">Du kan endre følgende innstillinger for en avtale etter at den er aktivert:</span><span class="sxs-lookup"><span data-stu-id="87d74-124">You can change the following settings for a deal after it has been activated:</span></span>

- <span data-ttu-id="87d74-125">Avstem etter</span><span class="sxs-lookup"><span data-stu-id="87d74-125">Reconcile by</span></span>
- <span data-ttu-id="87d74-126">Akkumulert garanti</span><span class="sxs-lookup"><span data-stu-id="87d74-126">Cumulative guarantee</span></span>
- <span data-ttu-id="87d74-127">Posteringsprofil</span><span class="sxs-lookup"><span data-stu-id="87d74-127">Posting profile</span></span>
- <span data-ttu-id="87d74-128">Posteringsprofil for garanti</span><span class="sxs-lookup"><span data-stu-id="87d74-128">Posting profile for guarantee</span></span>
- <span data-ttu-id="87d74-129">Dokumentmerknader</span><span class="sxs-lookup"><span data-stu-id="87d74-129">Document notes</span></span>
- <span data-ttu-id="87d74-130">Valuta.</span><span class="sxs-lookup"><span data-stu-id="87d74-130">Currency</span></span>
- <span data-ttu-id="87d74-131">Fra dato</span><span class="sxs-lookup"><span data-stu-id="87d74-131">From date</span></span>
- <span data-ttu-id="87d74-132">Til dags dato</span><span class="sxs-lookup"><span data-stu-id="87d74-132">To date</span></span>

<span data-ttu-id="87d74-133">I tillegg kan rabattlinjer fjernes.</span><span class="sxs-lookup"><span data-stu-id="87d74-133">In addition, rebate lines can be removed.</span></span>
