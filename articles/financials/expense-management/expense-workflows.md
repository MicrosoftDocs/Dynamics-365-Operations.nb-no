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
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 1944053a2f52648f4e70d40a2b515c69d462ee26
ms.contentlocale: nb-no
ms.lasthandoff: 05/08/2018

---

# <a name="set-up-workflows-for-expense"></a><span data-ttu-id="a6c0f-103">Sett opp arbeidsflyter for utgifter</span><span class="sxs-lookup"><span data-stu-id="a6c0f-103">Set up workflows for expense</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a6c0f-104"> Du kan sette opp en arbeidsflytprosess som brukes for å gjennomgå og godkjenne reise- og utleggsbilag.</span><span class="sxs-lookup"><span data-stu-id="a6c0f-104">You can set up a workflow process that is used to review and approve travel and expense documents.</span></span> <span data-ttu-id="a6c0f-105">Dokumentene som arbeidsflyter kan defineres inkluderer kostnadsrapporter, reiserekvisisjoner og forespørsler om kontantforskudd.</span><span class="sxs-lookup"><span data-stu-id="a6c0f-105">The documents for which workflows can be defined include expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="a6c0f-106">En arbeidsflyt representerer en forretningsprosess.</span><span class="sxs-lookup"><span data-stu-id="a6c0f-106">A workflow represents a business process.</span></span> <span data-ttu-id="a6c0f-107">Den definerer hvordan et dokument går gjennom systemet, og angir hvem som må utføre en oppgave eller godkjenne et dokument.</span><span class="sxs-lookup"><span data-stu-id="a6c0f-107">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="a6c0f-108">Det er flere fordeler ved å bruke arbeidsflytsystemet i en organisasjon:</span><span class="sxs-lookup"><span data-stu-id="a6c0f-108">There are several benefits of using the workflow system in your organization:</span></span>

-   <span data-ttu-id="a6c0f-109">**Konsekvente prosesser** – Du kan definere godkjenningsprosessen for bestemte dokumenter, for eksempel innkjøpsrekvisisjoner og reiseregningsrapporter.</span><span class="sxs-lookup"><span data-stu-id="a6c0f-109">**Consistent processes** — You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="a6c0f-110">Ved hjelp av arbeidsflytsystemet kan du sikre at dokumenter behandles og godkjennes på en konsekvent og effektiv måte.</span><span class="sxs-lookup"><span data-stu-id="a6c0f-110">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>

-   <span data-ttu-id="a6c0f-111">Prosessynlighet – Du kan spore status, logg og ytelsesstatistikk for en bestemt arbeidsflytforekomst.</span><span class="sxs-lookup"><span data-stu-id="a6c0f-111">Process visibility — You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="a6c0f-112">Dette gjør at du kan finne ut om det må gjøres endringer i arbeidsflyten for å forbedre effektiviteten.</span><span class="sxs-lookup"><span data-stu-id="a6c0f-112">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>

-   <span data-ttu-id="a6c0f-113">Sentralisert arbeidsliste – Brukere kan vise en sentralisert arbeidsliste for å vise arbeidsflytoppgavene og -godkjenningene som er tilordnet dem.</span><span class="sxs-lookup"><span data-stu-id="a6c0f-113">Centralized work list — Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

<span data-ttu-id="a6c0f-114">**Arbeidsflyttypene som du kan opprette**</span><span class="sxs-lookup"><span data-stu-id="a6c0f-114">**The types of workflows you can create**</span></span>

<span data-ttu-id="a6c0f-115">Følgende tabell viser hvilke typer arbeidsflyter du kan opprette i **Utgifter**.</span><span class="sxs-lookup"><span data-stu-id="a6c0f-115">The following table lists the types of workflows that you can create in **Expense**.</span></span>


|              <span data-ttu-id="a6c0f-116"><strong>Type</strong></span><span class="sxs-lookup"><span data-stu-id="a6c0f-116"><strong>Type</strong></span></span>              |                   <span data-ttu-id="a6c0f-117"><strong>Bruk denne typen til å gjøre følgende:</strong></span><span class="sxs-lookup"><span data-stu-id="a6c0f-117"><strong>Use this type to</strong></span></span>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|         <span data-ttu-id="a6c0f-118"><strong>Utgiftsrapport</strong></span><span class="sxs-lookup"><span data-stu-id="a6c0f-118"><strong>Expense report</strong></span></span>         |            <span data-ttu-id="a6c0f-119">Opprett arbeidsflyter for utgiftsrapporter.</span><span class="sxs-lookup"><span data-stu-id="a6c0f-119">Create approval workflows for expense reports.</span></span>             |
|  <span data-ttu-id="a6c0f-120"><strong>Poster utgiftsrapport automatisk</strong></span><span class="sxs-lookup"><span data-stu-id="a6c0f-120"><strong>Expense report auto posting</strong></span></span>   |        <span data-ttu-id="a6c0f-121">Opprett automatiske posteringsflyter for utgiftsrapporter.</span><span class="sxs-lookup"><span data-stu-id="a6c0f-121">Create automatic posting workflows for expense reports.</span></span>        |
|       <span data-ttu-id="a6c0f-122"><strong>Utgiftslinjeelement</strong></span><span class="sxs-lookup"><span data-stu-id="a6c0f-122"><strong>Expense line item</strong></span></span>        |     <span data-ttu-id="a6c0f-123">Opprett arbeidsflyter for godkjenning av linjeposter på utgiftsrapporter.</span><span class="sxs-lookup"><span data-stu-id="a6c0f-123">Create approval workflows for line items on expense reports.</span></span>      |
| <span data-ttu-id="a6c0f-124"><strong>Poster utgiftslinjevare automatisk</strong></span><span class="sxs-lookup"><span data-stu-id="a6c0f-124"><strong>Expense line item auto posting</strong></span></span> | <span data-ttu-id="a6c0f-125">Opprett automatiske posteringsflyter for linjeposter på kostnadsrapporter.</span><span class="sxs-lookup"><span data-stu-id="a6c0f-125">Create automatic posting workflows for line items on expense reports.</span></span> |
|       <span data-ttu-id="a6c0f-126"><strong>Reiserekvisisjon</strong></span><span class="sxs-lookup"><span data-stu-id="a6c0f-126"><strong>Travel requisition</strong></span></span>       |          <span data-ttu-id="a6c0f-127">Opprett arbeidsflyter for godkjenning av reiserekvisisjoner.</span><span class="sxs-lookup"><span data-stu-id="a6c0f-127">Create approval workflows for travel requisitions.</span></span>           |
|      <span data-ttu-id="a6c0f-128"><strong>Forskuddsforespørsel</strong></span><span class="sxs-lookup"><span data-stu-id="a6c0f-128"><strong>Cash advance request</strong></span></span>      |         <span data-ttu-id="a6c0f-129">Opprett arbeidsflyter for godkjenning av forespørsler om kontantforskudd.</span><span class="sxs-lookup"><span data-stu-id="a6c0f-129">Create approval workflows for cash advance requests.</span></span>          |
|        <span data-ttu-id="a6c0f-130"><strong>Mva-fradrag</strong></span><span class="sxs-lookup"><span data-stu-id="a6c0f-130"><strong>VAT tax recovery</strong></span></span>        | <span data-ttu-id="a6c0f-131">Opprett arbeidsflyter for godkjenning av tilbakebetaling av merverdiavgift (mva).</span><span class="sxs-lookup"><span data-stu-id="a6c0f-131">Create approval workflows for the recovery of value-added tax (VAT).</span></span>  |


