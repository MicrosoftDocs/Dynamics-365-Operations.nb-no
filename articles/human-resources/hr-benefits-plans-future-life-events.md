---
title: Konfigurere fremtidige levetidshendelser
description: Du kan planlegge fremtidige levetidshendelser i Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitFutureLifeEvents, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d390bf2e9b25c50e913967ea51fcfadd4a1120b8
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/17/2021
ms.locfileid: "5464356"
---
# <a name="configure-future-life-events"></a><span data-ttu-id="21998-103">Konfigurere fremtidige levetidshendelser</span><span class="sxs-lookup"><span data-stu-id="21998-103">Configure future life events</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="21998-104">Du kan planlegge fremtidige levetidshendelser i Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="21998-104">You can schedule future life events in Dynamics 365 Human Resources.</span></span>

1. <span data-ttu-id="21998-105">I arbeidsområdte **Fordelsbehandling**, under **Oppsett**, velger du **Fremtidige levetidshendelser**.</span><span class="sxs-lookup"><span data-stu-id="21998-105">In the **Benefits management** workspace, under **Setup**, select **Future life events**.</span></span>

2. <span data-ttu-id="21998-106">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="21998-106">Select **New**.</span></span>

3. <span data-ttu-id="21998-107">Angi verdier for de følgende feltene:</span><span class="sxs-lookup"><span data-stu-id="21998-107">Specify values for the following fields:</span></span>

   | <span data-ttu-id="21998-108">Felt</span><span class="sxs-lookup"><span data-stu-id="21998-108">Field</span></span> | <span data-ttu-id="21998-109">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="21998-109">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="21998-110">Levetidshendelsesdato</span><span class="sxs-lookup"><span data-stu-id="21998-110">Life event date</span></span> | <span data-ttu-id="21998-111">Systemet behandler alle hendelser i løpet av registreringsperioden som inntreffer frem til denne datoen.</span><span class="sxs-lookup"><span data-stu-id="21998-111">The system processes all events during the enrollment period that occur up until this date.</span></span> |
   | <span data-ttu-id="21998-112">Levetidshendelse logget</span><span class="sxs-lookup"><span data-stu-id="21998-112">Life event logged</span></span> | <span data-ttu-id="21998-113">Datoen og klokkeslettet da levetidshendelsen ble logget.</span><span class="sxs-lookup"><span data-stu-id="21998-113">Date and time when the life event is logged.</span></span> |
   | <span data-ttu-id="21998-114">Loggtype</span><span class="sxs-lookup"><span data-stu-id="21998-114">Log type</span></span> | <span data-ttu-id="21998-115">Viser om handlingen er én av følgende:</span><span class="sxs-lookup"><span data-stu-id="21998-115">Shows whether the action is one of the following:</span></span></br></br><span data-ttu-id="21998-116">- **Oppdatering** – en endring i en eksisterende post som sporer levetidshendelser</span><span class="sxs-lookup"><span data-stu-id="21998-116">- **Update** – a change to an existing record that is tracking life events</span></span></br></br><span data-ttu-id="21998-117">- **Sett inn** – oppretting av en ny levetidshendelsespost</span><span class="sxs-lookup"><span data-stu-id="21998-117">- **Insert** – the creation of a new life event record</span></span> |
   | <span data-ttu-id="21998-118">ID for levetidshendelsestype</span><span class="sxs-lookup"><span data-stu-id="21998-118">Life event type ID</span></span> | <span data-ttu-id="21998-119">Den unike ID-en for levetidshendelsestypen.</span><span class="sxs-lookup"><span data-stu-id="21998-119">The life event type unique identifier.</span></span> |
   | <span data-ttu-id="21998-120">Levetidshendelsestype</span><span class="sxs-lookup"><span data-stu-id="21998-120">Life event type</span></span> | <span data-ttu-id="21998-121">En katalysator for å oppdatere en ansatts fordelsregistrering.</span><span class="sxs-lookup"><span data-stu-id="21998-121">A catalyst to updating an employee’s benefits enrollment.</span></span> <span data-ttu-id="21998-122">Hvis du vil ha mer informasjon, kan du se delen om utløsere for levetidshendelser.</span><span class="sxs-lookup"><span data-stu-id="21998-122">For more details, see the Life event triggers section.</span></span> |
   | <span data-ttu-id="21998-123">Status</span><span class="sxs-lookup"><span data-stu-id="21998-123">Status</span></span> | <span data-ttu-id="21998-124">Om levetidshendelsen er behandlet eller ikke.</span><span class="sxs-lookup"><span data-stu-id="21998-124">Whether the life event has been processed or not.</span></span> |
   | <span data-ttu-id="21998-125">Linje</span><span class="sxs-lookup"><span data-stu-id="21998-125">Line</span></span> | <span data-ttu-id="21998-126">Linjenummeret til den fremtidige levetidshendelsen.</span><span class="sxs-lookup"><span data-stu-id="21998-126">The line number of the future life event.</span></span> |

4. <span data-ttu-id="21998-127">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="21998-127">Select **Save**.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]