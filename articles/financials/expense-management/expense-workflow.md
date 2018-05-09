---
title: Arbeidsflyt for utgifter
description: "Dette emnet forklarer hvordan du kan bruke arbeidsflytsystemet i Microsoft Dynamics 365 for Finance and Operations, for å sette opp en godkjenningsprosess for utgiftsrapporter i utgiftsstyring."
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
ms.openlocfilehash: 21815fccc91961653189f844718712faf573d2d7
ms.contentlocale: nb-no
ms.lasthandoff: 05/08/2018

---

# <a name="expense-workflow"></a><span data-ttu-id="3a923-103">Arbeidsflyt for utgifter</span><span class="sxs-lookup"><span data-stu-id="3a923-103">Expense workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3a923-104">Du kan bruke arbeidsflytsystemet i Microsoft Dynamics 365 for Finance and Operations, til å sette opp en godkjenningsprosess for utgiftsrapporter i utgiftsstyring.</span><span class="sxs-lookup"><span data-stu-id="3a923-104">You can use the workflow system in Microsoft Dynamics 365 for Finance and Operations, to set up a review process for expense reports in Expense management.</span></span> <span data-ttu-id="3a923-105">Du kan sette opp en arbeidsflyt som bruker følgende kriterier for å fastslå hvem som skal godkjenne utgiftsrapporter.</span><span class="sxs-lookup"><span data-stu-id="3a923-105">You can set up a workflow that uses the following criteria to determine who approves expense reports:</span></span>

- <span data-ttu-id="3a923-106">Ansattes rapporteringshierarki og forhåndsdefinerte godkjenningsgrenser</span><span class="sxs-lookup"><span data-stu-id="3a923-106">The employee reporting hierarchy and predefined approval limits</span></span>
- <span data-ttu-id="3a923-107">Godkjenning på flere nivåer som støtter midlertidig godkjenner og endelig godkjenner</span><span class="sxs-lookup"><span data-stu-id="3a923-107">Multi-level approval that supports interim approvers and a final approver</span></span>
- <span data-ttu-id="3a923-108">Finansielle dimensjoner og prosjektansvar</span><span class="sxs-lookup"><span data-stu-id="3a923-108">Financial dimensions and project responsibility</span></span>
- <span data-ttu-id="3a923-109">Oppgave til bestemte brukere eller brukergrupper</span><span class="sxs-lookup"><span data-stu-id="3a923-109">Assignment to specific users or user groups</span></span>

<span data-ttu-id="3a923-110">Arbeidsflyt for godkjenninger kan opprettes for kostnadsrapporter, reiserekvisisjoner, kontantforskudd og dekning av merverdiavgift (MVA).</span><span class="sxs-lookup"><span data-stu-id="3a923-110">Workflow approvals can be created for expense reports, travel requisitions, cash advances, and value-added tax (VAT) recovery.</span></span>

<span data-ttu-id="3a923-111">**Eksempel**</span><span class="sxs-lookup"><span data-stu-id="3a923-111">**Example**</span></span>

<span data-ttu-id="3a923-112">Følgende prosess er et eksempel på kostnadsstyringsarbeidsflyten for en kostnadsrapport.</span><span class="sxs-lookup"><span data-stu-id="3a923-112">The following process is an example of the expense management workflow for an expense report.</span></span>

1. <span data-ttu-id="3a923-113">En ansatt oppretter og lagrer en utgiftsrapport.</span><span class="sxs-lookup"><span data-stu-id="3a923-113">An employee creates and saves an expense report.</span></span>
2. <span data-ttu-id="3a923-114">Den ansatte sender inn utgiftsrapporten for godkjenning.</span><span class="sxs-lookup"><span data-stu-id="3a923-114">The employee submits the expense report for approval.</span></span> <span data-ttu-id="3a923-115">Godkjenneren er identifisert basert på reglene som ble definert når arbeidsflyten ble opprettet.</span><span class="sxs-lookup"><span data-stu-id="3a923-115">The approver is identified based on the rules that were defined when the workflow was set up.</span></span>
3. <span data-ttu-id="3a923-116">Godkjenner mottar et varsel om at en kostnadsrapport er klar for godkjenning.</span><span class="sxs-lookup"><span data-stu-id="3a923-116">The approver receives a notification that an expense report is ready for approval.</span></span> <span data-ttu-id="3a923-117">Godkjenner vurderer kostnadsrapporten og verifiserer at følgende betingelser er oppfylt:</span><span class="sxs-lookup"><span data-stu-id="3a923-117">The approver reviews the expense report and verifies that the following conditions are met:</span></span>

    - <span data-ttu-id="3a923-118">Utgiftene bryter ikke med noen utgiftspolicyer.</span><span class="sxs-lookup"><span data-stu-id="3a923-118">The expenses don't violate any expense policies.</span></span> <span data-ttu-id="3a923-119">Hvis en utgift bryter med en regel, verifiserer godkjenneren at utgiftsrapporten inneholder en gyldig begrunnelse for virksomheten.</span><span class="sxs-lookup"><span data-stu-id="3a923-119">If an expense violates a policy, the approver verifies that the expense report includes a valid business justification.</span></span>
    - <span data-ttu-id="3a923-120">Elektroniske kvitteringer vedlegges utgiftsrapporten.</span><span class="sxs-lookup"><span data-stu-id="3a923-120">Electronic receipts are attached to the expense report.</span></span>

4. <span data-ttu-id="3a923-121">Godkjenneren godkjenner utgiftsrapporten.</span><span class="sxs-lookup"><span data-stu-id="3a923-121">The approver approves the expense report.</span></span>
5. <span data-ttu-id="3a923-122">Utgiftsrapporten er tilordnet Kredittkoordinatoren for postering.</span><span class="sxs-lookup"><span data-stu-id="3a923-122">The expense report is assigned to the Accounts payable coordinator for posting.</span></span>
6. <span data-ttu-id="3a923-123">Ett av følgende trinn oppstår, avhengig av om automatisk postering er konfigurert:</span><span class="sxs-lookup"><span data-stu-id="3a923-123">One of the following steps occurs, depending on whether automatic posting is configured:</span></span>

    - <span data-ttu-id="3a923-124">Hvis automatisk postering er konfigurert, behandles utgiftsrapporten for betaling, og statusen for utgiftsrapporten oppdateres.</span><span class="sxs-lookup"><span data-stu-id="3a923-124">If automatic posting is configured, the expense report is processed for payment, and the status of the expense report is updated.</span></span>
    - <span data-ttu-id="3a923-125">Hvis automatisk postering ikke er konfigurert, bekrefter Kredittkoordinatoren for postering at alle opprinnelige kvitteringer er sendt inn, og at kvitteringene er justert mot utgiftene på utgiftsrapporten.</span><span class="sxs-lookup"><span data-stu-id="3a923-125">If automatic posting isn't configured, the Accounts payable coordinator verifies that all original receipts have been submitted, and that the receipts are aligned with the expenses on the expense report.</span></span> <span data-ttu-id="3a923-126">Alle skattekoder som er oppgitt på utgiftsrapporten, må også bekreftes som riktige.</span><span class="sxs-lookup"><span data-stu-id="3a923-126">All tax codes that are entered on the expense report must also be verified as correct.</span></span>

<span data-ttu-id="3a923-127">Etter at disse kravene er bekreftet vil utgiftsrapporten legges ut.</span><span class="sxs-lookup"><span data-stu-id="3a923-127">After these requirements are verified, the expense report is posted.</span></span>

<span data-ttu-id="3a923-128">Etter at utgiftsrapporten er lagt ut autoriseres betaling for utgiftsrapporten, og den ansatte blir refundert.</span><span class="sxs-lookup"><span data-stu-id="3a923-128">After the expense report is posted, payment is authorized for the expense report, and the employee is reimbursed.</span></span>

