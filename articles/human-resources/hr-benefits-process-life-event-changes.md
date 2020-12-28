---
title: Behandle endringer i levetidshendelser
description: Behandle endringer i levetidshendelser i Microsoft Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart, BenefitLifeEventTypes, BenefitEligibilityProcessResultViewer
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 39d1e94347809a1756fc4f66e5edc345c70eaf39
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4419844"
---
# <a name="process-life-event-changes"></a><span data-ttu-id="43591-103">Behandle endringer i levetidshendelser</span><span class="sxs-lookup"><span data-stu-id="43591-103">Process life event changes</span></span>

<span data-ttu-id="43591-104">Behandle endringer i levetidshendelser i Microsoft Dynamics 365 Human Resources for to endringer i levetidshendelse:</span><span class="sxs-lookup"><span data-stu-id="43591-104">Process life event changes in Microsoft Dynamics 365 Human Resources for two life event changes:</span></span>

- <span data-ttu-id="43591-105">Bursdagsendringer</span><span class="sxs-lookup"><span data-stu-id="43591-105">Birthday changes</span></span>
- <span data-ttu-id="43591-106">Overstyr utløpsendringer for rettighetsregel</span><span class="sxs-lookup"><span data-stu-id="43591-106">Eligibility rule override expiration changes</span></span> 

1. <span data-ttu-id="43591-107">I arbeidsområdet **Fordelsbehandling**, under **Behandling**, velger du **Behandling av endring av levetidshendelse**.</span><span class="sxs-lookup"><span data-stu-id="43591-107">In the **Benefits management** workspace, under **Processing**, select **Life event change processing**.</span></span>

2. <span data-ttu-id="43591-108">I dialogboksen **Kjør prosess for endring av levetidshendelse** angir du verdier for følgende felt:</span><span class="sxs-lookup"><span data-stu-id="43591-108">In the **Run life event change process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="43591-109">Felt</span><span class="sxs-lookup"><span data-stu-id="43591-109">Field</span></span> | <span data-ttu-id="43591-110">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="43591-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="43591-111">Registreringsperiode</span><span class="sxs-lookup"><span data-stu-id="43591-111">Enrollment period</span></span> | <span data-ttu-id="43591-112">Registreringsperioden som det skal behandles endringer i levetidshendelse for.</span><span class="sxs-lookup"><span data-stu-id="43591-112">The enrollment period to process life event changes for.</span></span> |
   | <span data-ttu-id="43591-113">Juridisk enhet</span><span class="sxs-lookup"><span data-stu-id="43591-113">Legal entity</span></span> | <span data-ttu-id="43591-114">Den juridiske enheten som det skal behandles endringer i levetidshendelse for.</span><span class="sxs-lookup"><span data-stu-id="43591-114">The legal entity to process life event changes for.</span></span> |

3. <span data-ttu-id="43591-115">Hvis du vil kjøre prosessen i bakgrunnen, velger du **Kjør i bakgrunnen** og utfører følgende oppgaver:</span><span class="sxs-lookup"><span data-stu-id="43591-115">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="43591-116">Angi informasjon for prosessen.</span><span class="sxs-lookup"><span data-stu-id="43591-116">Enter information for the process.</span></span>

   2. <span data-ttu-id="43591-117">Hvis du vil definere en gjentakende jobb, velger du **Gjentakelse**, angir gjentakelsesinformasjonen og velger **OK**.</span><span class="sxs-lookup"><span data-stu-id="43591-117">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="43591-118">Når du skal definere et jobbvarsel, velger du **Varsler**, velger varslene du vil motta, og velger deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="43591-118">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="43591-119">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="43591-119">Select **OK**.</span></span> <span data-ttu-id="43591-120">Prosessen vil kjøre med parameterne du angir.</span><span class="sxs-lookup"><span data-stu-id="43591-120">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="43591-121">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="43591-121">Select **OK**.</span></span>
