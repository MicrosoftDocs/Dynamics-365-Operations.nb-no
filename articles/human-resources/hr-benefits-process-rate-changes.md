---
title: Behandle satsendringer
description: Behandle endringer i fordelssatser i Microsoft Dynamics 365 Human Resources når en ny eller eksisterende fordelsplan har en endring i innstillingene for rettighetsregel.
author: andreabichsel
manager: tfehr
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart, BenefitRate, BenefitEligibilityProcessResultViewer
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c87d98a16431805ad652e28e5ca100a4152ad0c6
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/17/2021
ms.locfileid: "5466236"
---
# <a name="process-rate-changes"></a><span data-ttu-id="02478-103">Behandle satsendringer</span><span class="sxs-lookup"><span data-stu-id="02478-103">Process rate changes</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="02478-104">Behandle endringer i fordelssatser i Microsoft Dynamics 365 Human Resources når en ny eller eksisterende fordelsplan har en endring i innstillingene for rettighetsregel.</span><span class="sxs-lookup"><span data-stu-id="02478-104">Process benefit rate changes in Microsoft Dynamics 365 Human Resources when a new or existing benefit plan has a change in eligibility rule settings.</span></span> <span data-ttu-id="02478-105">Hvis en ny rettighets regel opprettes og tilordnes til planen, vil dette be systemet om å kjøre arbeiderrettigheter på nytt for å kontrollere om arbeidere nå kan være berettiget til planen, basert på nye rettighetsalternativer.</span><span class="sxs-lookup"><span data-stu-id="02478-105">If a new eligibility rule is created and assigned to the plan, this prompts the system to rerun worker eligibility to check if workers may now be eligible for the plan based on new eligibility options.</span></span> 

1. <span data-ttu-id="02478-106">I arbeidsområdet **Fordelsbehandling**, under **Behandling**, velger du **Behandling av oppdatering av satsendring**.</span><span class="sxs-lookup"><span data-stu-id="02478-106">In the **Benefits management** workspace, under **Processing**, select **Rate change update processing**.</span></span>

2. <span data-ttu-id="02478-107">I dialogboksen **Kjør prosess for oppdatering av fordelssats** angir du verdier for følgende felt:</span><span class="sxs-lookup"><span data-stu-id="02478-107">In the **Run benefit rate update process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="02478-108">Felt</span><span class="sxs-lookup"><span data-stu-id="02478-108">Field</span></span> | <span data-ttu-id="02478-109">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="02478-109">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="02478-110">**Registreringsperiode**</span><span class="sxs-lookup"><span data-stu-id="02478-110">**Enrollment period**</span></span> | <span data-ttu-id="02478-111">Registreringsperioden som det skal behandles satsendringer for.</span><span class="sxs-lookup"><span data-stu-id="02478-111">The enrollment period to process rate changes for.</span></span> |

3. <span data-ttu-id="02478-112">Hvis du vil kjøre prosessen i bakgrunnen, velger du **Kjør i bakgrunnen** og utfører følgende oppgaver:</span><span class="sxs-lookup"><span data-stu-id="02478-112">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="02478-113">Angi informasjon for prosessen.</span><span class="sxs-lookup"><span data-stu-id="02478-113">Enter information for the process.</span></span>

   2. <span data-ttu-id="02478-114">Hvis du vil definere en gjentakende jobb, velger du **Gjentakelse**, angir gjentakelsesinformasjonen og velger **OK**.</span><span class="sxs-lookup"><span data-stu-id="02478-114">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="02478-115">Når du skal definere et jobbvarsel, velger du **Varsler**, velger varslene du vil motta, og velger deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="02478-115">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="02478-116">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="02478-116">Select **OK**.</span></span> <span data-ttu-id="02478-117">Prosessen vil kjøre med parameterne du angir.</span><span class="sxs-lookup"><span data-stu-id="02478-117">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="02478-118">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="02478-118">Select **OK**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]