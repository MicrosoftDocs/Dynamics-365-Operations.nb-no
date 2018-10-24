---
title: Hva er nytt eller endret i Dynamics 365 for Talent Core HR (1. oktober 2018)
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 for Talent Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 10/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-10-01
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: c5d4fb53939d88fcb1bd83d70bc361ed9879f298
ms.openlocfilehash: 97820cd25ece48dc0b8045d9ba509d0971ca5aad
ms.contentlocale: nb-no
ms.lasthandoff: 10/16/2018

---

# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-october-1-2018"></a><span data-ttu-id="404b1-103">Hva er nytt eller endret i Dynamics 365 for Talent Core HR (1. oktober 2018)</span><span class="sxs-lookup"><span data-stu-id="404b1-103">What's new or changed in Dynamics 365 for Talent Core HR (October 1, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="404b1-104">**Build 8.1.1035.0**</span><span class="sxs-lookup"><span data-stu-id="404b1-104">**Build 8.1.1035.0**</span></span>

<span data-ttu-id="404b1-105">Dette emnet beskriver funksjoner som enten er nye eller endret i Core HR.</span><span class="sxs-lookup"><span data-stu-id="404b1-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="turn-off-electronic-payment-validation"></a><span data-ttu-id="404b1-106">Slå av validering av elektroniske betalinger</span><span class="sxs-lookup"><span data-stu-id="404b1-106">Turn off electronic payment validation</span></span>

<span data-ttu-id="404b1-107">Validering av elektroniske betalinger skjer hvis du setter opp leverandørbetalinger for direkteinnskudd, enten via arbeidsområdet **Ansattselvbetjening** eller direkte på ansattskjemaet.</span><span class="sxs-lookup"><span data-stu-id="404b1-107">Electronic payment information validation occurs if you set up disbursements for direct deposit either through **Employee self-service** workspace (ESS) or directly on the employee form.</span></span> <span data-ttu-id="404b1-108">Dette alternativet gir deg fleksibilitet til å fjerne denne valideringen hvis du ikke trenger valideringskontrollerer for beløp og gjenværende verdier.</span><span class="sxs-lookup"><span data-stu-id="404b1-108">This option gives you the flexibility to remove that validation if you do not require the validation checks for amounts and remainder values.</span></span> <span data-ttu-id="404b1-109">Denne funksjonen er nyttig hvis du skal integrere med et eksternt lønnssystem som har forskjellige krav.</span><span class="sxs-lookup"><span data-stu-id="404b1-109">This feature is helpful if you're integrating with an external payroll system that has different requirements.</span></span>

## <a name="manager-self-service---add-goals-for-team-members-through-the-team-performance-goals-tile"></a><span data-ttu-id="404b1-110">Lederselvbetjening - Legg til mål for teammedlemmer via flisen Ytelsesmål for team</span><span class="sxs-lookup"><span data-stu-id="404b1-110">Manager self-service - Add goals for team members through the Team performance goals tile</span></span>

<span data-ttu-id="404b1-111">Før denne versjonen kan ledere legge til mål for ansatte individuelt via ytelsesmålene knyttet til hver ansatt.</span><span class="sxs-lookup"><span data-stu-id="404b1-111">Prior to this release, managers can add goals to their employees individually through the performance goals associated to each employee.</span></span> <span data-ttu-id="404b1-112">Med denne oppdateringen kan ledere få tilgang til flisen **Ytelsesmål for team** og opprette nye mål ved å velge en av de direkte rapportene.</span><span class="sxs-lookup"><span data-stu-id="404b1-112">With this update, managers can access the **Team performance goals** tile and create new goals by selecting any of their direct reports.</span></span>

## <a name="manager-self-service---add-reviews-for-team-members-through-the-team-performance-reviews-tile"></a><span data-ttu-id="404b1-113">Lederselvbetjening - Legg til gjennomganger for teammedlemmer via flisen Gjennomganger av teamytelse</span><span class="sxs-lookup"><span data-stu-id="404b1-113">Manager self-service - Add reviews for team members through the Team performance reviews tile</span></span>

<span data-ttu-id="404b1-114">Før denne versjonen kan ledere legge til gjennomganger for ansatte individuelt via gjennomgangene knyttet til hver ansatt.</span><span class="sxs-lookup"><span data-stu-id="404b1-114">Prior to this release, managers can add reviews to their employees individually through the reviews associated to each employee.</span></span> <span data-ttu-id="404b1-115">Med denne oppdateringen kan ledere få tilgang til flisen **Gjennomgang av teamytelse** og opprette nye gjennomganger ved å velge en av de direkte rapportene.</span><span class="sxs-lookup"><span data-stu-id="404b1-115">With this update, managers can access the **Team performance reviews** tile and create new reviews by selecting any of their direct reports.</span></span>

## <a name="configure-proration-options-by-leave-plan"></a><span data-ttu-id="404b1-116">Konfigurere fordelingsalternativer etter permisjonsplan</span><span class="sxs-lookup"><span data-stu-id="404b1-116">Configure proration options by leave plan</span></span>

<span data-ttu-id="404b1-117">Organisasjoner belønner de ansatte med fritid på forskjellige måter, basert på når ansatte starter hos og forlater firmaet.</span><span class="sxs-lookup"><span data-stu-id="404b1-117">Organizations award time off differently based on when employees join and leave the company.</span></span> <span data-ttu-id="404b1-118">I noen organisasjoner får de ansatte fullstendig tildeling på startdatoen mens andre fordeler bonusen.</span><span class="sxs-lookup"><span data-stu-id="404b1-118">For some organizations, employees are awarded their full allocation on their start date while others prorate the award.</span></span> <span data-ttu-id="404b1-119">Du finner nye alternativer i denne versjonen som lar deg velge hvordan belønningene og avsetningene skal fordeles for ansatte som starter hos og forlater en organisasjon.</span><span class="sxs-lookup"><span data-stu-id="404b1-119">New options are provided in this release to choose how to prorate the awards and accruals for joiners and leavers in an organization.</span></span> <span data-ttu-id="404b1-120">Alternativene omfatter: Fordelt, Full avsetning og ingen avsetning.</span><span class="sxs-lookup"><span data-stu-id="404b1-120">Options include: Prorated, Full accrual, and No accrual.</span></span>

## <a name="other-changes"></a><span data-ttu-id="404b1-121">Andre endringer</span><span class="sxs-lookup"><span data-stu-id="404b1-121">Other changes</span></span>

-   <span data-ttu-id="404b1-122">Ansattenhet oppdatert – **Personlig**-flisen kan nå oppdateres ved hjelp av Excel-tillegg / dataadministrasjon.</span><span class="sxs-lookup"><span data-stu-id="404b1-122">Employee entity updated - The **Personal** title can now be updated using the Excel add-in/data management.</span></span>

-   <span data-ttu-id="404b1-123">Sikkerhetsendring for å tillate fjerning av knappene **Slett** og **Deaktiver** i ansattselvbetjening for betalingsinformasjon.</span><span class="sxs-lookup"><span data-stu-id="404b1-123">Security change to allow removal of the **Delete** and **Deactivate** buttons in employee self-service for payment information.</span></span>

## <a name="known-issue"></a><span data-ttu-id="404b1-124">Kjent problem</span><span class="sxs-lookup"><span data-stu-id="404b1-124">Known issue</span></span>

-   <span data-ttu-id="404b1-125">**Problem:** Når du legger til en ny tilknytning til en arbeider, er knappenei **Ny** og **Rediger** nedtonet. **Løsning:** Før du åpner vedleggssiden, må du kontrollere at faktaboksene på **Arbeider**-siden er lukket.</span><span class="sxs-lookup"><span data-stu-id="404b1-125">**Issue:** When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out. **Workaround:** Before opening the attachment page, make sure that the FactBoxes on the **Worker** page are closed.</span></span> <span data-ttu-id="404b1-126">Hvis faktaboksene er lukket når **Arbeider**-siden lastes, blir **Vedlegg**-knappene aktivert.</span><span class="sxs-lookup"><span data-stu-id="404b1-126">If the FactBoxes are closed when the **Worker** page is loaded, the **Attachments** buttons will be enabled.</span></span> <span data-ttu-id="404b1-127">(Dette problemet vil bli løst i neste plattformoppdatering.)</span><span class="sxs-lookup"><span data-stu-id="404b1-127">(This issue will be fixed in the next platform update.)</span></span>

