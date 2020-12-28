---
title: Hva er nytt eller endret i Dynamics 365 Talent (14. februar 2019)?
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 02/14/2019
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
ms.search.validFrom: 2019-02-14
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 32f3bab38233833498ed566fa1558a023b3bc0dd
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4462124"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-february-14-2019"></a><span data-ttu-id="8ce87-103">Hva er nytt eller endret i Dynamics 365 Talent (14. februar 2019)?</span><span class="sxs-lookup"><span data-stu-id="8ce87-103">What's new or changed in Dynamics 365 Talent (February 14, 2019)</span></span>

<span data-ttu-id="8ce87-104">Dette emnet beskriver funksjoner som enten er nye eller endret i Talent.</span><span class="sxs-lookup"><span data-stu-id="8ce87-104">This topic describes features that are either new or changed in Talent.</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="8ce87-105">Endringer i Attract</span><span class="sxs-lookup"><span data-stu-id="8ce87-105">Changes in Attract</span></span>
<span data-ttu-id="8ce87-106">Det er mindre feilrettinger inkludert i denne utgivelsen.</span><span class="sxs-lookup"><span data-stu-id="8ce87-106">There are minor bug fixes included with this release.</span></span>

## <a name="changes-in-onboarding"></a><span data-ttu-id="8ce87-107">Endringer i jobbintroduksjon</span><span class="sxs-lookup"><span data-stu-id="8ce87-107">Changes in Onboarding</span></span>
<span data-ttu-id="8ce87-108">Det er mindre feilrettinger inkludert i denne utgivelsen.</span><span class="sxs-lookup"><span data-stu-id="8ce87-108">There are minor bug fixes included with this release.</span></span>
 
## <a name="changes-in-core-hr"></a><span data-ttu-id="8ce87-109">Endringer i Core HR</span><span class="sxs-lookup"><span data-stu-id="8ce87-109">Changes in Core HR</span></span> 
<span data-ttu-id="8ce87-110">**Build 8.1.2146**</span><span class="sxs-lookup"><span data-stu-id="8ce87-110">**Build 8.1.2146**</span></span>

### <a name="employee-fixed-compensation-entity-doesnt-export-all-records"></a><span data-ttu-id="8ce87-111">Enheten Fast kompensasjon for ansatt eksporterer ikke alle poster</span><span class="sxs-lookup"><span data-stu-id="8ce87-111">Employee fixed compensation entity doesn't export all records</span></span>
<span data-ttu-id="8ce87-112">Med denne endringen vil enheten **Fast kompensasjon for ansatt** nå eksportere alle poster.</span><span class="sxs-lookup"><span data-stu-id="8ce87-112">With this change, the **Employee fixed compensation** entity will now export all records.</span></span> <span data-ttu-id="8ce87-113">Enheten kan brukes til å opprette og oppdatere eksisterende poster for fast kompensasjon for ansatte.</span><span class="sxs-lookup"><span data-stu-id="8ce87-113">The entity can be used to create and update existing fixed compensation records for employees.</span></span> 

### <a name="employment-end-date-doesnt-honor-employee-preferred-time-zone-settings"></a><span data-ttu-id="8ce87-114">Sluttdato for ansettelse overholder ikke innstillinger for foretrukket tidssone for ansatte</span><span class="sxs-lookup"><span data-stu-id="8ce87-114">Employment end date doesn't honor employee preferred time zone settings</span></span>
<span data-ttu-id="8ce87-115">Sluttdatoer for ansettelse tar nå hensyn til brukervalgt tidssone når ansettelse i et firma opprettes eller avsluttes.</span><span class="sxs-lookup"><span data-stu-id="8ce87-115">Employment end dates are now honoring the user-preferred time zone when creating or ending employment with a company.</span></span>
 
### <a name="uk-addresses-display-in-analytics-as-eastern-switzerland-addresses"></a><span data-ttu-id="8ce87-116">Adresser i Storbritannia vises som adresser i det østlige Sveits i Analyse</span><span class="sxs-lookup"><span data-stu-id="8ce87-116">UK addresses display in Analytics as Eastern Switzerland addresses</span></span>
<span data-ttu-id="8ce87-117">En endring er gjort i denne versjonen for å rette opp feilplasserte adresser i rapporten **Personaladministrasjon** "Antall ansatte etter sted".</span><span class="sxs-lookup"><span data-stu-id="8ce87-117">In this release, a change has been made to correct misalignment in addresses in the **Personnel Management** "Headcount by location" report.</span></span>
 
### <a name="termination-code-is-not-populated-on-the-worker-position-assignment-record-when-ending-the-position"></a><span data-ttu-id="8ce87-118">Opphørskode fylles ikke ut på tilordningsposten for arbeiderstilling ved avslutning av stillingen</span><span class="sxs-lookup"><span data-stu-id="8ce87-118">Termination code is not populated on the worker position assignment record when ending the position</span></span>
<span data-ttu-id="8ce87-119">En endring er gjort for å angi "Avslutningsårsak"-koden som standard ved avslutning av ansattes stillingstilordning.</span><span class="sxs-lookup"><span data-stu-id="8ce87-119">A change has been made to default the "Termination reason" code when ending the employees position assignment.</span></span>

### <a name="new-entity-created-for-job-compensation-levels"></a><span data-ttu-id="8ce87-120">Ny enhet opprettet for jobbkompensasjonsnivåer</span><span class="sxs-lookup"><span data-stu-id="8ce87-120">New entity created for job compensation levels</span></span>
<span data-ttu-id="8ce87-121">En ny enhet for rammeverk for databehandling (DMF) er opprettet.</span><span class="sxs-lookup"><span data-stu-id="8ce87-121">A new data management framework (DMF) entity was created.</span></span> <span data-ttu-id="8ce87-122">Enheten muliggjør oppretting og oppdatering til kompensasjonsnivåer, markedsverdier og undersøkelsesinformasjon for hver jobb som er definert i systemet.</span><span class="sxs-lookup"><span data-stu-id="8ce87-122">The entity provides for creation and updates to compensation levels, market values, and survey information for each job defined in the system.</span></span>
