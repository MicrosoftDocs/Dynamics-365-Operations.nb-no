---
title: Hva er nytt eller endret i Dynamics 365 Talent – Core HR (16. oktober 2018)
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Talent – Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 10/22/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-10-22
ms.dyn365.ops.version: Talent
ms.openlocfilehash: d5f2aea5fcc81d0b4c1d8a392a3e56c888440a94
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897402"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-october-16-2018"></a><span data-ttu-id="20bb5-103">Hva er nytt eller endret i Dynamics 365 Talent – Core HR (16. oktober 2018)</span><span class="sxs-lookup"><span data-stu-id="20bb5-103">What's new or changed in Dynamics 365 Talent - Core HR (October 16, 2018)</span></span>

<span data-ttu-id="20bb5-104">**Build 8.1.1067**</span><span class="sxs-lookup"><span data-stu-id="20bb5-104">**Build 8.1.1067**</span></span>

<span data-ttu-id="20bb5-105">Dette emnet beskriver funksjoner som enten er nye eller endret i Core HR.</span><span class="sxs-lookup"><span data-stu-id="20bb5-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="allow-managers-to-update-time-off-requests"></a><span data-ttu-id="20bb5-106">Tillate ledere å oppdatere fraværsforespørsler</span><span class="sxs-lookup"><span data-stu-id="20bb5-106">Allow managers to update time off requests</span></span>

<span data-ttu-id="20bb5-107">Fraværsforespørsler fra ansatte må oppdateres etter at de godkjennes gjennom arbeidsflyten.</span><span class="sxs-lookup"><span data-stu-id="20bb5-107">Employee time off requests may need to be updated after they are approved through the workflow.</span></span> <span data-ttu-id="20bb5-108">I mange tilfeller gjør lederen disse oppdateringene på vegne av den ansatte.</span><span class="sxs-lookup"><span data-stu-id="20bb5-108">In many cases, the manager makes these updates on the employee’s behalf.</span></span> <span data-ttu-id="20bb5-109">Denne nye funksjonen gjør det mulig for ledere å oppdatere fravær eller avbryte fraværsforespørsler på vegne av de ansatte.</span><span class="sxs-lookup"><span data-stu-id="20bb5-109">This new feature provides the ability for managers to update time off or cancel time off requests on behalf of their employees.</span></span> <span data-ttu-id="20bb5-110">Denne funksjonen styres av parameteren **Arbeid på vegne av** som kan angis på siden **Personalparametere**.</span><span class="sxs-lookup"><span data-stu-id="20bb5-110">This capability is controlled by the **Work on behalf** parameter that can be set on the **Human Resource Parameters** page.</span></span> 
 
## <a name="allow-hr-to-update-time-off-requests"></a><span data-ttu-id="20bb5-111">Tillate HR å oppdatere fraværsforespørsler</span><span class="sxs-lookup"><span data-stu-id="20bb5-111">Allow HR to update time off requests</span></span>

<span data-ttu-id="20bb5-112">På samme måte som funksjonen ovenfor, må fraværsforespørsler fra ansatte kanskje oppdateres av HR etter at de tidligere er godkjent via arbeidsflyten.</span><span class="sxs-lookup"><span data-stu-id="20bb5-112">Similar to the feature above, employee time off requests may need to be updated by HR after they have been previously approved through the workflow.</span></span> <span data-ttu-id="20bb5-113">Denne funksjonen gjør det mulig for HR å oppdatere fraværsforespørsler.</span><span class="sxs-lookup"><span data-stu-id="20bb5-113">This feature provides the ability for HR users to update time off requests.</span></span> <span data-ttu-id="20bb5-114">Funksjonaliteten aktiveres i **Mennesker**-arbeidsområdet og på siden **Arbeider** ved hjelp av et nytt alternativ som kalles **Vis fridager**.</span><span class="sxs-lookup"><span data-stu-id="20bb5-114">The capability is enabled in the **People** workspace and on the **Worker** page, using a new option called **View time off**.</span></span> <span data-ttu-id="20bb5-115">På disse sidene kan HR-brukere vise forespørsler og oppdatere fraværestransaksjoner, på lignende måte som ledere kan utføre disse handlingene.</span><span class="sxs-lookup"><span data-stu-id="20bb5-115">On those pages, HR users can view requests and update time off transactions, similar to how managers can perform these actions.</span></span>

<span data-ttu-id="20bb5-116">Sikkerhetsplikten som styrer tilgang til denne funksjonaliteten er:</span><span class="sxs-lookup"><span data-stu-id="20bb5-116">The security duty that controls access to this functionality is:</span></span>
- <span data-ttu-id="20bb5-117">Plikt: Opprettholde arbeiderspesifikke permisjons- og fraværsprosesser.</span><span class="sxs-lookup"><span data-stu-id="20bb5-117">Duty: Maintain worker-specific leave and absence processes.</span></span>
- <span data-ttu-id="20bb5-118">Rettighet: Opprettholde forespørsler om permisjon og fravær for alle arbeidere.</span><span class="sxs-lookup"><span data-stu-id="20bb5-118">Privilege: Maintain leave and absence requests for all workers.</span></span>

## <a name="other-changes"></a><span data-ttu-id="20bb5-119">Andre endringer</span><span class="sxs-lookup"><span data-stu-id="20bb5-119">Other changes</span></span>
<span data-ttu-id="20bb5-120">Følgende oppdateringer er gjort i denne versjonen:</span><span class="sxs-lookup"><span data-stu-id="20bb5-120">The following updates have been made in this release:</span></span>
- <span data-ttu-id="20bb5-121">Endringer i arbeideransettelseshandlinger, slik at de ikke lenger "sitter fast" i **Arbeidsflyt fullført**-tilstanden.</span><span class="sxs-lookup"><span data-stu-id="20bb5-121">Changes to worker hire actions so that they are no longer "stuck" in **Workflow complete** state.</span></span>
- <span data-ttu-id="20bb5-122">Ansettelsesposten kan nå opprettes uten en startdato for ansettelse.</span><span class="sxs-lookup"><span data-stu-id="20bb5-122">Employment record can now be created without an employment start date.</span></span>
- <span data-ttu-id="20bb5-123">Dynamics 365 Talent-registreringsdatoen for et kurs i Ansattselvbetjening bruker nå tidssoneforskyvningen på datoen.</span><span class="sxs-lookup"><span data-stu-id="20bb5-123">The Dynamics 365 Talent registration date for a course shown in Employee self-service now applies the time zone offset to the date.</span></span>
- <span data-ttu-id="20bb5-124">Excel-filer kan importeres flere ganger uten feil ved hjelp av **Ansattenhet**.</span><span class="sxs-lookup"><span data-stu-id="20bb5-124">Excel files can be imported multiple times without any errors using **Employee Entity**.</span></span>

## <a name="known-issue"></a><span data-ttu-id="20bb5-125">Kjent problem</span><span class="sxs-lookup"><span data-stu-id="20bb5-125">Known issue</span></span>

- <span data-ttu-id="20bb5-126">**Problem**: Når du legger til en ny tilknytning til en arbeider, nedtones **Ny** og **Rediger**-knappene.</span><span class="sxs-lookup"><span data-stu-id="20bb5-126">**Issue**: When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out.</span></span> 
- <span data-ttu-id="20bb5-127">**Løsning:** Før du åpner vedleggssiden må du kontrollere at faktaboksene på **Arbeider**-siden er lukket.</span><span class="sxs-lookup"><span data-stu-id="20bb5-127">**Workaround:** Before opening the attachment page, make sure that the FactBoxes on the **Worker** page are closed.</span></span> <span data-ttu-id="20bb5-128">Hvis faktaboksene er lukket når **Arbeider**-siden lastes, blir vedleggsknappene aktivert.</span><span class="sxs-lookup"><span data-stu-id="20bb5-128">If the FactBoxes are closed when the **Worker** page is loaded, the attachments buttons will be enabled.</span></span> <span data-ttu-id="20bb5-129">(Dette problemet vil bli løst i neste plattformoppdatering.)</span><span class="sxs-lookup"><span data-stu-id="20bb5-129">(This issue will be fixed in the next platform update.)</span></span>
