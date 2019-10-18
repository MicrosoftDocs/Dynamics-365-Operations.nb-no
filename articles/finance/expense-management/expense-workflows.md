---
title: Sett opp arbeidsflyter for utgifter
description: Du kan sette opp en arbeidsflytprosess som brukes for å gjennomgå og godkjenne reise- og utleggsbilag.
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 86cadf7277fbb7e08dad4b5dc2a46e1c6ce5a888
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/27/2019
ms.locfileid: "2179214"
---
# <a name="set-up-workflows-for-expense"></a><span data-ttu-id="d3203-103">Sett opp arbeidsflyter for utgifter</span><span class="sxs-lookup"><span data-stu-id="d3203-103">Set up workflows for expense</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d3203-104"> Du kan sette opp en arbeidsflytprosess som brukes for å gjennomgå og godkjenne reise- og utleggsbilag.</span><span class="sxs-lookup"><span data-stu-id="d3203-104">You can set up a workflow process that is used to review and approve travel and expense documents.</span></span> <span data-ttu-id="d3203-105">Dokumentene som arbeidsflyter kan defineres inkluderer kostnadsrapporter, reiserekvisisjoner og forespørsler om kontantforskudd.</span><span class="sxs-lookup"><span data-stu-id="d3203-105">The documents for which workflows can be defined include expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="d3203-106">En arbeidsflyt representerer en forretningsprosess.</span><span class="sxs-lookup"><span data-stu-id="d3203-106">A workflow represents a business process.</span></span> <span data-ttu-id="d3203-107">Den definerer hvordan et dokument går gjennom systemet, og angir hvem som må utføre en oppgave eller godkjenne et dokument.</span><span class="sxs-lookup"><span data-stu-id="d3203-107">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="d3203-108">Det er flere fordeler ved å bruke arbeidsflytsystemet i en organisasjon:</span><span class="sxs-lookup"><span data-stu-id="d3203-108">There are several benefits of using the workflow system in your organization:</span></span>

-   <span data-ttu-id="d3203-109">**Konsekvente prosesser** – Du kan definere godkjenningsprosessen for bestemte dokumenter, for eksempel innkjøpsrekvisisjoner og reiseregningsrapporter.</span><span class="sxs-lookup"><span data-stu-id="d3203-109">**Consistent processes** — You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="d3203-110">Ved hjelp av arbeidsflytsystemet kan du sikre at dokumenter behandles og godkjennes på en konsekvent og effektiv måte.</span><span class="sxs-lookup"><span data-stu-id="d3203-110">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>

-   <span data-ttu-id="d3203-111">Prosessynlighet – Du kan spore status, logg og ytelsesstatistikk for en bestemt arbeidsflytforekomst.</span><span class="sxs-lookup"><span data-stu-id="d3203-111">Process visibility — You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="d3203-112">Dette gjør at du kan finne ut om det må gjøres endringer i arbeidsflyten for å forbedre effektiviteten.</span><span class="sxs-lookup"><span data-stu-id="d3203-112">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>

-   <span data-ttu-id="d3203-113">Sentralisert arbeidsliste – Brukere kan vise en sentralisert arbeidsliste for å vise arbeidsflytoppgavene og -godkjenningene som er tilordnet dem.</span><span class="sxs-lookup"><span data-stu-id="d3203-113">Centralized work list — Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

<span data-ttu-id="d3203-114">**Arbeidsflyttypene som du kan opprette**</span><span class="sxs-lookup"><span data-stu-id="d3203-114">**The types of workflows you can create**</span></span>

<span data-ttu-id="d3203-115">Følgende tabell viser hvilke typer arbeidsflyter du kan opprette i **Utgifter**.</span><span class="sxs-lookup"><span data-stu-id="d3203-115">The following table lists the types of workflows that you can create in **Expense**.</span></span>


|              <span data-ttu-id="d3203-116"><strong>Type</strong></span><span class="sxs-lookup"><span data-stu-id="d3203-116"><strong>Type</strong></span></span>              |                   <span data-ttu-id="d3203-117"><strong>Bruk denne typen til å gjøre følgende:</strong></span><span class="sxs-lookup"><span data-stu-id="d3203-117"><strong>Use this type to</strong></span></span>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|         <span data-ttu-id="d3203-118"><strong>Utgiftsrapport</strong></span><span class="sxs-lookup"><span data-stu-id="d3203-118"><strong>Expense report</strong></span></span>         |            <span data-ttu-id="d3203-119">Opprett arbeidsflyter for utgiftsrapporter.</span><span class="sxs-lookup"><span data-stu-id="d3203-119">Create approval workflows for expense reports.</span></span>             |
|  <span data-ttu-id="d3203-120"><strong>Poster utgiftsrapport automatisk</strong></span><span class="sxs-lookup"><span data-stu-id="d3203-120"><strong>Expense report auto posting</strong></span></span>   |        <span data-ttu-id="d3203-121">Opprett automatiske posteringsflyter for utgiftsrapporter.</span><span class="sxs-lookup"><span data-stu-id="d3203-121">Create automatic posting workflows for expense reports.</span></span>        |
|       <span data-ttu-id="d3203-122"><strong>Utgiftslinjeelement</strong></span><span class="sxs-lookup"><span data-stu-id="d3203-122"><strong>Expense line item</strong></span></span>        |     <span data-ttu-id="d3203-123">Opprett arbeidsflyter for godkjenning av linjeposter på utgiftsrapporter.</span><span class="sxs-lookup"><span data-stu-id="d3203-123">Create approval workflows for line items on expense reports.</span></span>      |
| <span data-ttu-id="d3203-124"><strong>Poster utgiftslinjevare automatisk</strong></span><span class="sxs-lookup"><span data-stu-id="d3203-124"><strong>Expense line item auto posting</strong></span></span> | <span data-ttu-id="d3203-125">Opprett automatiske posteringsflyter for linjeposter på kostnadsrapporter.</span><span class="sxs-lookup"><span data-stu-id="d3203-125">Create automatic posting workflows for line items on expense reports.</span></span> |
|       <span data-ttu-id="d3203-126"><strong>Reiserekvisisjon</strong></span><span class="sxs-lookup"><span data-stu-id="d3203-126"><strong>Travel requisition</strong></span></span>       |          <span data-ttu-id="d3203-127">Opprett arbeidsflyter for godkjenning av reiserekvisisjoner.</span><span class="sxs-lookup"><span data-stu-id="d3203-127">Create approval workflows for travel requisitions.</span></span>           |
|      <span data-ttu-id="d3203-128"><strong>Forskuddsforespørsel</strong></span><span class="sxs-lookup"><span data-stu-id="d3203-128"><strong>Cash advance request</strong></span></span>      |         <span data-ttu-id="d3203-129">Opprett arbeidsflyter for godkjenning av forespørsler om kontantforskudd.</span><span class="sxs-lookup"><span data-stu-id="d3203-129">Create approval workflows for cash advance requests.</span></span>          |
|        <span data-ttu-id="d3203-130"><strong>Mva-fradrag</strong></span><span class="sxs-lookup"><span data-stu-id="d3203-130"><strong>VAT tax recovery</strong></span></span>        | <span data-ttu-id="d3203-131">Opprett arbeidsflyter for godkjenning av tilbakebetaling av merverdiavgift (mva).</span><span class="sxs-lookup"><span data-stu-id="d3203-131">Create approval workflows for the recovery of value-added tax (VAT).</span></span>  |

