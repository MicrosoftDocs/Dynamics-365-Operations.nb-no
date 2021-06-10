---
title: Konfigurere fremtidige levetidshendelser
description: Du kan planlegge fremtidige levetidshendelser i Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitFutureLifeEvents, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d52e91e7b050027485b3536f40f6ad80afd90de8
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/18/2021
ms.locfileid: "6056738"
---
# <a name="configure-future-life-events"></a><span data-ttu-id="6af49-103">Konfigurere fremtidige levetidshendelser</span><span class="sxs-lookup"><span data-stu-id="6af49-103">Configure future life events</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="6af49-104">Du kan planlegge fremtidige levetidshendelser i Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="6af49-104">You can schedule future life events in Dynamics 365 Human Resources.</span></span>

1. <span data-ttu-id="6af49-105">I arbeidsområdte **Fordelsbehandling**, under **Oppsett**, velger du **Fremtidige levetidshendelser**.</span><span class="sxs-lookup"><span data-stu-id="6af49-105">In the **Benefits management** workspace, under **Setup**, select **Future life events**.</span></span>

2. <span data-ttu-id="6af49-106">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="6af49-106">Select **New**.</span></span>

3. <span data-ttu-id="6af49-107">Angi verdier for de følgende feltene:</span><span class="sxs-lookup"><span data-stu-id="6af49-107">Specify values for the following fields:</span></span>

   | <span data-ttu-id="6af49-108">Felt</span><span class="sxs-lookup"><span data-stu-id="6af49-108">Field</span></span> | <span data-ttu-id="6af49-109">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="6af49-109">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="6af49-110">Levetidshendelsesdato</span><span class="sxs-lookup"><span data-stu-id="6af49-110">Life event date</span></span> | <span data-ttu-id="6af49-111">Systemet behandler alle hendelser i løpet av registreringsperioden som inntreffer frem til denne datoen.</span><span class="sxs-lookup"><span data-stu-id="6af49-111">The system processes all events during the enrollment period that occur up until this date.</span></span> |
   | <span data-ttu-id="6af49-112">Levetidshendelse logget</span><span class="sxs-lookup"><span data-stu-id="6af49-112">Life event logged</span></span> | <span data-ttu-id="6af49-113">Datoen og klokkeslettet da levetidshendelsen ble logget.</span><span class="sxs-lookup"><span data-stu-id="6af49-113">Date and time when the life event is logged.</span></span> |
   | <span data-ttu-id="6af49-114">Loggtype</span><span class="sxs-lookup"><span data-stu-id="6af49-114">Log type</span></span> | <span data-ttu-id="6af49-115">Viser om handlingen er én av følgende:</span><span class="sxs-lookup"><span data-stu-id="6af49-115">Shows whether the action is one of the following:</span></span></br></br><span data-ttu-id="6af49-116">- **Oppdatering** – en endring i en eksisterende post som sporer levetidshendelser</span><span class="sxs-lookup"><span data-stu-id="6af49-116">- **Update** – a change to an existing record that is tracking life events</span></span></br></br><span data-ttu-id="6af49-117">- **Sett inn** – oppretting av en ny levetidshendelsespost</span><span class="sxs-lookup"><span data-stu-id="6af49-117">- **Insert** – the creation of a new life event record</span></span> |
   | <span data-ttu-id="6af49-118">ID for levetidshendelsestype</span><span class="sxs-lookup"><span data-stu-id="6af49-118">Life event type ID</span></span> | <span data-ttu-id="6af49-119">Den unike ID-en for levetidshendelsestypen.</span><span class="sxs-lookup"><span data-stu-id="6af49-119">The life event type unique identifier.</span></span> |
   | <span data-ttu-id="6af49-120">Levetidshendelsestype</span><span class="sxs-lookup"><span data-stu-id="6af49-120">Life event type</span></span> | <span data-ttu-id="6af49-121">En katalysator for å oppdatere en ansatts fordelsregistrering.</span><span class="sxs-lookup"><span data-stu-id="6af49-121">A catalyst to updating an employee’s benefits enrollment.</span></span> <span data-ttu-id="6af49-122">Hvis du vil ha mer informasjon, kan du se delen om utløsere for levetidshendelser.</span><span class="sxs-lookup"><span data-stu-id="6af49-122">For more details, see the Life event triggers section.</span></span> |
   | <span data-ttu-id="6af49-123">Status</span><span class="sxs-lookup"><span data-stu-id="6af49-123">Status</span></span> | <span data-ttu-id="6af49-124">Om levetidshendelsen er behandlet eller ikke.</span><span class="sxs-lookup"><span data-stu-id="6af49-124">Whether the life event has been processed or not.</span></span> |
   | <span data-ttu-id="6af49-125">Linje</span><span class="sxs-lookup"><span data-stu-id="6af49-125">Line</span></span> | <span data-ttu-id="6af49-126">Linjenummeret til den fremtidige levetidshendelsen.</span><span class="sxs-lookup"><span data-stu-id="6af49-126">The line number of the future life event.</span></span> |

4. <span data-ttu-id="6af49-127">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="6af49-127">Select **Save**.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]