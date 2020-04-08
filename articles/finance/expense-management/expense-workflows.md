---
title: Konfigurere arbeidsflyter for reiseregning og utlegg
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
ms.openlocfilehash: cdd4d69cb86da12e4a265f89c021c238d00cad08
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/21/2020
ms.locfileid: "3154000"
---
# <a name="set-up-workflows-for-expense-management"></a><span data-ttu-id="fd04c-103">Konfigurere arbeidsflyter for reiseregning og utlegg</span><span class="sxs-lookup"><span data-stu-id="fd04c-103">Set up workflows for Expense management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fd04c-104">Du kan sette opp en arbeidsflytprosess som brukes for å gjennomgå og godkjenne reise- og utleggsbilag.</span><span class="sxs-lookup"><span data-stu-id="fd04c-104">You can set up a workflow process that is used to review and approve travel and expense documents.</span></span> <span data-ttu-id="fd04c-105">Dokumentene som arbeidsflyter kan defineres inkluderer kostnadsrapporter, reiserekvisisjoner og forespørsler om kontantforskudd.</span><span class="sxs-lookup"><span data-stu-id="fd04c-105">The documents for which workflows can be defined include expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="fd04c-106">En arbeidsflyt representerer en forretningsprosess.</span><span class="sxs-lookup"><span data-stu-id="fd04c-106">A workflow represents a business process.</span></span> <span data-ttu-id="fd04c-107">Den definerer hvordan et dokument går gjennom systemet, og angir hvem som må utføre en oppgave eller godkjenne et dokument.</span><span class="sxs-lookup"><span data-stu-id="fd04c-107">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="fd04c-108">Det er flere fordeler ved å bruke arbeidsflytsystemet i en organisasjon:</span><span class="sxs-lookup"><span data-stu-id="fd04c-108">There are several benefits of using the workflow system in your organization:</span></span>

-   <span data-ttu-id="fd04c-109">**Konsekvente prosesser** – Du kan definere godkjenningsprosessen for bestemte dokumenter, for eksempel innkjøpsrekvisisjoner og reiseregningsrapporter.</span><span class="sxs-lookup"><span data-stu-id="fd04c-109">**Consistent processes** — You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="fd04c-110">Ved hjelp av arbeidsflytsystemet kan du sikre at dokumenter behandles og godkjennes på en konsekvent og effektiv måte.</span><span class="sxs-lookup"><span data-stu-id="fd04c-110">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>

-   <span data-ttu-id="fd04c-111">Prosessynlighet – Du kan spore status, logg og ytelsesstatistikk for en bestemt arbeidsflytforekomst.</span><span class="sxs-lookup"><span data-stu-id="fd04c-111">Process visibility — You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="fd04c-112">Dette gjør at du kan finne ut om det må gjøres endringer i arbeidsflyten for å forbedre effektiviteten.</span><span class="sxs-lookup"><span data-stu-id="fd04c-112">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>

-   <span data-ttu-id="fd04c-113">Sentralisert arbeidsliste – Brukere kan vise en sentralisert arbeidsliste for å vise arbeidsflytoppgavene og -godkjenningene som er tilordnet dem.</span><span class="sxs-lookup"><span data-stu-id="fd04c-113">Centralized work list — Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

<span data-ttu-id="fd04c-114">**Arbeidsflyttypene som du kan opprette**</span><span class="sxs-lookup"><span data-stu-id="fd04c-114">**The types of workflows you can create**</span></span>

<span data-ttu-id="fd04c-115">Følgende tabell viser hvilke typer arbeidsflyter du kan opprette i **Utgifter**.</span><span class="sxs-lookup"><span data-stu-id="fd04c-115">The following table lists the types of workflows that you can create in **Expense**.</span></span>


|              <span data-ttu-id="fd04c-116"><strong>Type</strong></span><span class="sxs-lookup"><span data-stu-id="fd04c-116"><strong>Type</strong></span></span>              |                   <span data-ttu-id="fd04c-117"><strong>Bruk denne typen til å gjøre følgende:</strong></span><span class="sxs-lookup"><span data-stu-id="fd04c-117"><strong>Use this type to</strong></span></span>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|         <span data-ttu-id="fd04c-118"><strong>Utgiftsrapport</strong></span><span class="sxs-lookup"><span data-stu-id="fd04c-118"><strong>Expense report</strong></span></span>         |            <span data-ttu-id="fd04c-119">Opprett arbeidsflyter for utgiftsrapporter.</span><span class="sxs-lookup"><span data-stu-id="fd04c-119">Create approval workflows for expense reports.</span></span>             |
|  <span data-ttu-id="fd04c-120"><strong>Poster utgiftsrapport automatisk</strong></span><span class="sxs-lookup"><span data-stu-id="fd04c-120"><strong>Expense report auto posting</strong></span></span>   |        <span data-ttu-id="fd04c-121">Opprett automatiske posteringsflyter for utgiftsrapporter.</span><span class="sxs-lookup"><span data-stu-id="fd04c-121">Create automatic posting workflows for expense reports.</span></span>        |
|       <span data-ttu-id="fd04c-122"><strong>Utgiftslinjeelement</strong></span><span class="sxs-lookup"><span data-stu-id="fd04c-122"><strong>Expense line item</strong></span></span>        |     <span data-ttu-id="fd04c-123">Opprett arbeidsflyter for godkjenning av linjeposter på utgiftsrapporter.</span><span class="sxs-lookup"><span data-stu-id="fd04c-123">Create approval workflows for line items on expense reports.</span></span>      |
| <span data-ttu-id="fd04c-124"><strong>Poster utgiftslinjevare automatisk</strong></span><span class="sxs-lookup"><span data-stu-id="fd04c-124"><strong>Expense line item auto posting</strong></span></span> | <span data-ttu-id="fd04c-125">Opprett automatiske posteringsflyter for linjeposter på kostnadsrapporter.</span><span class="sxs-lookup"><span data-stu-id="fd04c-125">Create automatic posting workflows for line items on expense reports.</span></span> |
|       <span data-ttu-id="fd04c-126"><strong>Reiserekvisisjon</strong></span><span class="sxs-lookup"><span data-stu-id="fd04c-126"><strong>Travel requisition</strong></span></span>       |          <span data-ttu-id="fd04c-127">Opprett arbeidsflyter for godkjenning av reiserekvisisjoner.</span><span class="sxs-lookup"><span data-stu-id="fd04c-127">Create approval workflows for travel requisitions.</span></span>           |
|      <span data-ttu-id="fd04c-128"><strong>Forskuddsforespørsel</strong></span><span class="sxs-lookup"><span data-stu-id="fd04c-128"><strong>Cash advance request</strong></span></span>      |         <span data-ttu-id="fd04c-129">Opprett arbeidsflyter for godkjenning av forespørsler om kontantforskudd.</span><span class="sxs-lookup"><span data-stu-id="fd04c-129">Create approval workflows for cash advance requests.</span></span>          |
|        <span data-ttu-id="fd04c-130"><strong>Mva-fradrag</strong></span><span class="sxs-lookup"><span data-stu-id="fd04c-130"><strong>VAT tax recovery</strong></span></span>        | <span data-ttu-id="fd04c-131">Opprett arbeidsflyter for godkjenning av tilbakebetaling av merverdiavgift (mva).</span><span class="sxs-lookup"><span data-stu-id="fd04c-131">Create approval workflows for the recovery of value-added tax (VAT).</span></span>  |

