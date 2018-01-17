---
title: Sett opp arbeidsflyter for utgifter
description: "Du kan sette opp en arbeidsflytprosess som brukes for å gjennomgå og godkjenne reise- og utleggsbilag."
author: saraschi2
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: ef60fbab0f75ff70206d954e3d098a3866c467b6
ms.contentlocale: nb-no
ms.lasthandoff: 01/17/2018

---

# <a name="set-up-workflows-for-expense"></a><span data-ttu-id="dd316-103">Sett opp arbeidsflyter for utgifter</span><span class="sxs-lookup"><span data-stu-id="dd316-103">Set up workflows for expense</span></span>

[!include[banner](../includes/banner.md)]<span data-ttu-id="dd316-104"> Du kan sette opp en arbeidsflytprosess som brukes for å gjennomgå og godkjenne reise- og utleggsbilag.</span><span class="sxs-lookup"><span data-stu-id="dd316-104"> You can set up a workflow process that is used to review and approve travel and expense documents.</span></span> <span data-ttu-id="dd316-105">Dokumentene som arbeidsflyter kan defineres inkluderer kostnadsrapporter, reiserekvisisjoner og forespørsler om kontantforskudd.</span><span class="sxs-lookup"><span data-stu-id="dd316-105">The documents for which workflows can be defined include expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="dd316-106">En arbeidsflyt representerer en forretningsprosess.</span><span class="sxs-lookup"><span data-stu-id="dd316-106">A workflow represents a business process.</span></span> <span data-ttu-id="dd316-107">Den definerer hvordan et dokument går gjennom systemet, og angir hvem som må utføre en oppgave eller godkjenne et dokument.</span><span class="sxs-lookup"><span data-stu-id="dd316-107">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="dd316-108">Det er flere fordeler ved å bruke arbeidsflytsystemet i en organisasjon:</span><span class="sxs-lookup"><span data-stu-id="dd316-108">There are several benefits of using the workflow system in your organization:</span></span>

-   <span data-ttu-id="dd316-109">**Konsekvente prosesser** – Du kan definere godkjenningsprosessen for bestemte dokumenter, for eksempel innkjøpsrekvisisjoner og reiseregningsrapporter.</span><span class="sxs-lookup"><span data-stu-id="dd316-109">**Consistent processes** — You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="dd316-110">Ved hjelp av arbeidsflytsystemet kan du sikre at dokumenter behandles og godkjennes på en konsekvent og effektiv måte.</span><span class="sxs-lookup"><span data-stu-id="dd316-110">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>

-   <span data-ttu-id="dd316-111">Prosessynlighet – Du kan spore status, logg og ytelsesstatistikk for en bestemt arbeidsflytforekomst.</span><span class="sxs-lookup"><span data-stu-id="dd316-111">Process visibility — You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="dd316-112">Dette gjør at du kan finne ut om det må gjøres endringer i arbeidsflyten for å forbedre effektiviteten.</span><span class="sxs-lookup"><span data-stu-id="dd316-112">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>

-   <span data-ttu-id="dd316-113">Sentralisert arbeidsliste – Brukere kan vise en sentralisert arbeidsliste for å vise arbeidsflytoppgavene og -godkjenningene som er tilordnet dem.</span><span class="sxs-lookup"><span data-stu-id="dd316-113">Centralized work list — Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

<span data-ttu-id="dd316-114">**Arbeidsflyttypene som du kan opprette**</span><span class="sxs-lookup"><span data-stu-id="dd316-114">**The types of workflows you can create**</span></span>

<span data-ttu-id="dd316-115">Følgende tabell viser hvilke typer arbeidsflyter du kan opprette i **Utgifter**.</span><span class="sxs-lookup"><span data-stu-id="dd316-115">The following table lists the types of workflows that you can create in **Expense**.</span></span>

| <span data-ttu-id="dd316-116">**Type**</span><span class="sxs-lookup"><span data-stu-id="dd316-116">**Type**</span></span>                           | <span data-ttu-id="dd316-117">**Bruk denne typen til å gjøre følgende:**</span><span class="sxs-lookup"><span data-stu-id="dd316-117">**Use this type to**</span></span>                                                 |     
|------------------------------------|----------------------------------------------------------------------|
| <span data-ttu-id="dd316-118">**Utgiftsrapport**</span><span class="sxs-lookup"><span data-stu-id="dd316-118">**Expense report**</span></span>                 | <span data-ttu-id="dd316-119">Opprett arbeidsflyter for utgiftsrapporter.</span><span class="sxs-lookup"><span data-stu-id="dd316-119">Create approval workflows for expense reports.</span></span>                       |      
| <span data-ttu-id="dd316-120">**Poster utgiftsrapport automatisk**</span><span class="sxs-lookup"><span data-stu-id="dd316-120">**Expense report auto posting**</span></span>    | <span data-ttu-id="dd316-121">Opprett automatiske posteringsflyter for utgiftsrapporter.</span><span class="sxs-lookup"><span data-stu-id="dd316-121">Create automatic posting workflows for expense reports.</span></span>              |     
| <span data-ttu-id="dd316-122">**Utgiftslinjeelement**</span><span class="sxs-lookup"><span data-stu-id="dd316-122">**Expense line item**</span></span>              | <span data-ttu-id="dd316-123">Opprett arbeidsflyter for godkjenning av linjeposter på utgiftsrapporter.</span><span class="sxs-lookup"><span data-stu-id="dd316-123">Create approval workflows for line items on expense reports.</span></span>         |     
| <span data-ttu-id="dd316-124">**Poster utgiftslinjevare automatisk**</span><span class="sxs-lookup"><span data-stu-id="dd316-124">**Expense line item auto posting**</span></span> | <span data-ttu-id="dd316-125">Opprett automatiske posteringsflyter for linjeposter på kostnadsrapporter.</span><span class="sxs-lookup"><span data-stu-id="dd316-125">Create automatic posting workflows for line items on expense reports.</span></span>|
| <span data-ttu-id="dd316-126">**Reiserekvisisjon**</span><span class="sxs-lookup"><span data-stu-id="dd316-126">**Travel requisition**</span></span>             | <span data-ttu-id="dd316-127">Opprett arbeidsflyter for godkjenning av reiserekvisisjoner.</span><span class="sxs-lookup"><span data-stu-id="dd316-127">Create approval workflows for travel requisitions.</span></span>                   |    
| <span data-ttu-id="dd316-128">**Forskuddsforespørsel**</span><span class="sxs-lookup"><span data-stu-id="dd316-128">**Cash advance request**</span></span>           | <span data-ttu-id="dd316-129">Opprett arbeidsflyter for godkjenning av forespørsler om kontantforskudd.</span><span class="sxs-lookup"><span data-stu-id="dd316-129">Create approval workflows for cash advance requests.</span></span>                 |     
| <span data-ttu-id="dd316-130">**Mva-fradrag**</span><span class="sxs-lookup"><span data-stu-id="dd316-130">**VAT tax recovery**</span></span>               | <span data-ttu-id="dd316-131">Opprett arbeidsflyter for godkjenning av tilbakebetaling av merverdiavgift (mva).</span><span class="sxs-lookup"><span data-stu-id="dd316-131">Create approval workflows for the recovery of value-added tax (VAT).</span></span> |       

