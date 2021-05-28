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
ms.openlocfilehash: ee342de6d069131e230120c5d65aef58da8e632a
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020393"
---
# <a name="rebate-management-deal-workflows"></a><span data-ttu-id="0ea71-103">Arbeidsflyter for rabattbehandlingsavtale</span><span class="sxs-lookup"><span data-stu-id="0ea71-103">Rebate management deal workflows</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0ea71-104">Når du skal godkjenne rabattavtaler, bruker Rabattbehandling den samme arbeidsflytplattformen som andre Finance and Operations-apper.</span><span class="sxs-lookup"><span data-stu-id="0ea71-104">To approve rebate deals, Rebate management uses the same workflow platform as other Finance and Operations apps.</span></span> <span data-ttu-id="0ea71-105">To jobbprosesser er tilknyttet hver arbeidsflyt:</span><span class="sxs-lookup"><span data-stu-id="0ea71-105">Two job processes are associated with every workflow:</span></span>

- <span data-ttu-id="0ea71-106">Ett av elementene i arbeidsflyten aktiverer avtalen, slik at bruker- eller arbeidsflytprosessen kan godkjenne transaksjonene.</span><span class="sxs-lookup"><span data-stu-id="0ea71-106">One element of the workflow activates the deal so that the user or workflow process can approve the transactions.</span></span>
- <span data-ttu-id="0ea71-107">Ett av elementene i arbeidsflyten godkjenner avtalen.</span><span class="sxs-lookup"><span data-stu-id="0ea71-107">One element of the workflow approves the deal.</span></span>

<span data-ttu-id="0ea71-108">Før du kan bruke en rabattavtale, må den være aktiv i **Rabattbehandling**-modulen.</span><span class="sxs-lookup"><span data-stu-id="0ea71-108">Before you can use a rebate deal, it must be active in the **Rebate management** module.</span></span> <span data-ttu-id="0ea71-109">Hvis du vil aktivere en avtale, må du først opprette og konfigurere en *arbeidsflyt for rabattbehandlingsavtale*.</span><span class="sxs-lookup"><span data-stu-id="0ea71-109">To activate a deal, you must first create and configure a *Rebate management deal workflow*.</span></span>

<span data-ttu-id="0ea71-110">Når en arbeidsflyt er aktivert for Rabattbehandling, kan brukere ikke godkjenne avtaler manuelt.</span><span class="sxs-lookup"><span data-stu-id="0ea71-110">After a workflow is activated for Rebate management, users can't manually approve deals.</span></span> <span data-ttu-id="0ea71-111">Arbeidsflyten må alltid brukes.</span><span class="sxs-lookup"><span data-stu-id="0ea71-111">The workflow must be always used.</span></span>

## <a name="create-and-manage-rebate-management-deal-workflows"></a><span data-ttu-id="0ea71-112">Opprett og administrer arbeidsflyter for rabattbehandlingsavtale</span><span class="sxs-lookup"><span data-stu-id="0ea71-112">Create and manage Rebate management deal workflows</span></span>

<span data-ttu-id="0ea71-113">For å arbeide med arbeidsflyter for rabattbehandlingsavtale må du gå til **Rabattbehandling \> Oppsett \> Arbeidsflyter for rabattbehandling**.</span><span class="sxs-lookup"><span data-stu-id="0ea71-113">To work with your Rebate management deal workflows, go to **Rebate management \> Setup \> Rebate management workflows**.</span></span> <span data-ttu-id="0ea71-114">Der kan du vise, opprette og oppdatere arbeidsflyter etter behov.</span><span class="sxs-lookup"><span data-stu-id="0ea71-114">There, you can view, create, and update workflows as required.</span></span> <span data-ttu-id="0ea71-115">Bare én arbeidsflyt av denne typen kan være aktiv om gangen.</span><span class="sxs-lookup"><span data-stu-id="0ea71-115">Only one workflow of this type can be active at a time.</span></span> <span data-ttu-id="0ea71-116">Hvis du vil ha mer informasjon om arbeidsflyter, hvordan du arbeider med siden **Arbeidsflyter for rabattbehandling** og hvordan du oppretter arbeidsflyter, kan du se [Oversikt over arbeidsflytsystem](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md) og de relaterte emnene.</span><span class="sxs-lookup"><span data-stu-id="0ea71-116">For more information about workflows, how to work with the **Rebate management workflows** page, and how to create workflows, see [Workflow system overview](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md) and its related topics.</span></span>

## <a name="use-a-workflow-to-activate-a-deal"></a><span data-ttu-id="0ea71-117">Bruk en arbeidsflyt til å aktivere en avtale</span><span class="sxs-lookup"><span data-stu-id="0ea71-117">Use a workflow to activate a deal</span></span>

<span data-ttu-id="0ea71-118">Hvis du vil aktivere en avtale via en arbeidsflyt, åpner du avtalen (for eksempel på siden **Alle rabattbehandlingsavtaler**).</span><span class="sxs-lookup"><span data-stu-id="0ea71-118">To activate a deal through a workflow, open the deal (for example, on the **All rebate management deals** page).</span></span> <span data-ttu-id="0ea71-119">Velg deretter **Arbeidsflyt \> Send inn** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="0ea71-119">Then, on the Action Pane, select **Workflow \> Submit**.</span></span> <span data-ttu-id="0ea71-120">Etter at den nye avtalen er behandlet og godkjent via arbeidsflyten, vil den være aktiv og klar til bruk.</span><span class="sxs-lookup"><span data-stu-id="0ea71-120">After the new deal has been processed and approved through the workflow, it will be active and ready to use.</span></span>

<span data-ttu-id="0ea71-121">Når en avtale er aktivert, kan du ikke endre oppsettet.</span><span class="sxs-lookup"><span data-stu-id="0ea71-121">After a deal has been activated, you can't change its setup.</span></span> <span data-ttu-id="0ea71-122">Hvis du må endre en aktiv avtale, må du deaktivere den og deretter opprette en ny avtale.</span><span class="sxs-lookup"><span data-stu-id="0ea71-122">If you must change an active deal, inactivate it, and then create a new deal.</span></span> <span data-ttu-id="0ea71-123">Hvis den nye avtalen kommer til å ligne på den gamle avtalen, kan du opprette den ved å kopiere den gamle avtalen.</span><span class="sxs-lookup"><span data-stu-id="0ea71-123">If the new deal will resemble the old deal, you can create it by copying the old deal.</span></span>
