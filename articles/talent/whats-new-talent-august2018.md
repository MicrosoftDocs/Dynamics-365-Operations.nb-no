---
title: Hva er nytt eller endret i Dynamics 365 for Talent Core HR (august 2018)
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 for Talent Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 08/27/2018
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
ms.search.validFrom: 2018-08-27
ms.dyn365.ops.version: Talent August 2018 update
ms.openlocfilehash: be76f29dc9d38cdf3c2d56120a830acae69937a4
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/19/2019
ms.locfileid: "857020"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-august-2018"></a><span data-ttu-id="891dc-103">Hva er nytt eller endret i Dynamics 365 for Talent Core HR (august 2018)</span><span class="sxs-lookup"><span data-stu-id="891dc-103">What's new or changed in Dynamics 365 for Talent Core HR (August 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="891dc-104">**Build 8.1.104**</span><span class="sxs-lookup"><span data-stu-id="891dc-104">**Build 8.1.104**</span></span>

<span data-ttu-id="891dc-105">Dette emnet beskriver funksjoner som enten er nye eller endret i Dynamics 365 for Talent Core HR.</span><span class="sxs-lookup"><span data-stu-id="891dc-105">This topic describes features that are either new or changed in Dynamics 365 for Talent Core HR.</span></span>

## <a name="view-expiring-records-in-manager-self-service"></a><span data-ttu-id="891dc-106">Vise utløpende poster i Lederselvbetjening</span><span class="sxs-lookup"><span data-stu-id="891dc-106">View expiring records in Manager self service</span></span>

<span data-ttu-id="891dc-107">Du kan nå vise utløpende poster i Lederselvbetjening.</span><span class="sxs-lookup"><span data-stu-id="891dc-107">You can now view expiring records in Manager self-service.</span></span> <span data-ttu-id="891dc-108">Nye alternativer er at du kan konfigurere hva slags informasjon som skal være tilgjengelige for prosjektledere å vise.</span><span class="sxs-lookup"><span data-stu-id="891dc-108">New options are allow you to configure what information will be available for managers to view.</span></span> <span data-ttu-id="891dc-109">Disse omfatter:</span><span class="sxs-lookup"><span data-stu-id="891dc-109">These include:</span></span>

-   <span data-ttu-id="891dc-110">Attester</span><span class="sxs-lookup"><span data-stu-id="891dc-110">Certificates</span></span>

-   <span data-ttu-id="891dc-111">Identifikasjonsnumre</span><span class="sxs-lookup"><span data-stu-id="891dc-111">Identification numbers</span></span>

-   <span data-ttu-id="891dc-112">Prøveperioder</span><span class="sxs-lookup"><span data-stu-id="891dc-112">Probation periods</span></span>

-   <span data-ttu-id="891dc-113">Screeninger</span><span class="sxs-lookup"><span data-stu-id="891dc-113">Screenings</span></span>

-   <span data-ttu-id="891dc-114">Tester</span><span class="sxs-lookup"><span data-stu-id="891dc-114">Tests</span></span>

<span data-ttu-id="891dc-115">Denne funksjonen gir deg også muligheten til å angi datointervallet for søking etter poster som utløper.</span><span class="sxs-lookup"><span data-stu-id="891dc-115">This feature also gives you the ability to specify the range of days in which to look for expiring records.</span></span>

## <a name="configurable-transfer-actions"></a><span data-ttu-id="891dc-116">Konfigurerbare overføringshandlinger</span><span class="sxs-lookup"><span data-stu-id="891dc-116">Configurable transfer actions</span></span>

<span data-ttu-id="891dc-117">Du kan konfigurere etter rolle hvilke alternativer som er tilgjengelige under registreringen av en forespørsel om overføring.</span><span class="sxs-lookup"><span data-stu-id="891dc-117">You can configure by role the options that will be available during the entry of a transfer request.</span></span> <span data-ttu-id="891dc-118">Denne funksjonen gir større fleksibilitet på tvers av rollene i en organisasjon.</span><span class="sxs-lookup"><span data-stu-id="891dc-118">This feature provides additional flexibility across the roles in an organization.</span></span>

<span data-ttu-id="891dc-119">Ledere som ber om overføringer av ansatte, har for eksempel ikke tilgang til å foreslå eller angi kompensasjonsbeløp eller velge oppgavelistene som skal være knyttet til overføringen.</span><span class="sxs-lookup"><span data-stu-id="891dc-119">For example, managers requesting employee transfers may not have access to suggest or enter compensation amounts or select the task lists that will be associated with the transfer request.</span></span> <span data-ttu-id="891dc-120">I dette tilfellet kan ledere opprette og sende forespørsler for overføring, men er ikke tillatt for å angi kompensasjon eller aktivitetstildelinger i listen.</span><span class="sxs-lookup"><span data-stu-id="891dc-120">In this case, managers can create and submit transfer requests but are not allowed to enter compensation or task list assignments.</span></span> <span data-ttu-id="891dc-121">I denne samme konfigurasjonen kan Personale tilordne de nye verdiene for kompensasjon, i tillegg til å tilordne en ekstra sjekklister fullføres som et resultat av overføringen er fullført.</span><span class="sxs-lookup"><span data-stu-id="891dc-121">In this same configuration, HR will be able to assign the new compensation values as well as assign any additional checklists to be completed as a result of the transfer completing.</span></span>

<span data-ttu-id="891dc-122">De nye konfigurasjonsalternativene settes som standard ikke endre egenskapene før denne oppdateringen.</span><span class="sxs-lookup"><span data-stu-id="891dc-122">By default, the new configuration options are set to not change the capabilities prior to this update.</span></span>

## <a name="leave-and-absence"></a><span data-ttu-id="891dc-123">Permisjon og fravær</span><span class="sxs-lookup"><span data-stu-id="891dc-123">Leave and absence</span></span>

<span data-ttu-id="891dc-124">Det finnes nå flere datofelt i Lønn og fravær.</span><span class="sxs-lookup"><span data-stu-id="891dc-124">There are now additional Date fields available in Leave and Absence.</span></span>

<span data-ttu-id="891dc-125">Med denne funksjonen kan du angi grunnlaget for den påløpte perioden på plannivået der du vil bruke datoer for ansatte.</span><span class="sxs-lookup"><span data-stu-id="891dc-125">With this feature you can set the accrual period basis at the plan level to use specific employee dates.</span></span> <span data-ttu-id="891dc-126">Dette gjør at andre datoer enn startdatoen for planen kan brukes under avsetning av lønn.</span><span class="sxs-lookup"><span data-stu-id="891dc-126">This allows for dates other than the plan start date to be used during the leave accrual process.</span></span> <span data-ttu-id="891dc-127">Alternativene for spesifikke datoer for ansatte omfatter følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="891dc-127">Options for employee specific dates include the following values:</span></span>

-   <span data-ttu-id="891dc-128">Egendefinert (tilgjengelig før denne oppdateringen)</span><span class="sxs-lookup"><span data-stu-id="891dc-128">Custom (available prior to this update)</span></span>

-   <span data-ttu-id="891dc-129">Jubileumsdato</span><span class="sxs-lookup"><span data-stu-id="891dc-129">Anniversary date</span></span>

-   <span data-ttu-id="891dc-130">Opprinnelig ansettelsesdato</span><span class="sxs-lookup"><span data-stu-id="891dc-130">Original hire date</span></span>

-   <span data-ttu-id="891dc-131">Ansiennitetsdato</span><span class="sxs-lookup"><span data-stu-id="891dc-131">Seniority date</span></span>

-   <span data-ttu-id="891dc-132">Arbeiderens justerte startdato</span><span class="sxs-lookup"><span data-stu-id="891dc-132">Worker’s adjusted start date</span></span>

-   <span data-ttu-id="891dc-133">Arbeiderens startdato</span><span class="sxs-lookup"><span data-stu-id="891dc-133">Worker’s start date</span></span>

<span data-ttu-id="891dc-134">Når konfigurert til å bruke en av de bestemte datoene for ansatte, bruker registreringsprosessen den angitte datoen til å beregne avsetningsperiodene.</span><span class="sxs-lookup"><span data-stu-id="891dc-134">When configured to use one of the employee specific dates, the enrollment process will use the specified date to calculate the accrual periods.</span></span> <span data-ttu-id="891dc-135">Grunnlaget for påløpt periode vises også i den ansattes registrering, noe som hjelper deg med å forstå hva som brukes under prosessen med avsetningen.</span><span class="sxs-lookup"><span data-stu-id="891dc-135">The accrual period basis is also displayed on the employee’s plan enrollment to help you understand what’s being used during the accrual process.</span></span>

## <a name="microsoft-word-integration"></a><span data-ttu-id="891dc-136">Microsoft Word-integrering</span><span class="sxs-lookup"><span data-stu-id="891dc-136">Microsoft Word integration</span></span>

<span data-ttu-id="891dc-137">Dokumentmaler er aktivert i hele Core HR.</span><span class="sxs-lookup"><span data-stu-id="891dc-137">Document templates have been enabled throughout Core HR.</span></span> <span data-ttu-id="891dc-138">Med denne funksjonen kan du opprette brev og rapporter basert på Word-maler du oppretter.</span><span class="sxs-lookup"><span data-stu-id="891dc-138">This feature allows you to create letters and reports based on Word templates that you create.</span></span>

<span data-ttu-id="891dc-139">Mer informasjon om denne funksjonen er tilgjengelig i [Opplæring i Office-integrering](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/office-integration/office-integration-tutorial?toc=/dynamics365/unified-operations/talent/toc.json).</span><span class="sxs-lookup"><span data-stu-id="891dc-139">Additional information about this feature is available in the [Office integration tutorial](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/office-integration/office-integration-tutorial?toc=/dynamics365/unified-operations/talent/toc.json).</span></span>


## <a name="other-fixes"></a><span data-ttu-id="891dc-140">Andre reparasjoner</span><span class="sxs-lookup"><span data-stu-id="891dc-140">Other fixes</span></span>

<span data-ttu-id="891dc-141">Denne versjonen inkluderer en rekke feilrettinger, nye enheter, reparasjoner for eksisterende enheter og lokaliserte etikettendringer.</span><span class="sxs-lookup"><span data-stu-id="891dc-141">This release also includes a number of bug fixes, the addition of new entities, fixes to existing entities, and localized label changes.</span></span>
