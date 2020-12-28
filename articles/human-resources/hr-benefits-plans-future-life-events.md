---
title: Konfigurere fremtidige levetidshendelser
description: Du kan planlegge fremtidige levetidshendelser i Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
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
ms.openlocfilehash: 78c65faa4ae0f428184700a912998e9dded026c5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4419849"
---
# <a name="configure-future-life-events"></a><span data-ttu-id="f397b-103">Konfigurere fremtidige levetidshendelser</span><span class="sxs-lookup"><span data-stu-id="f397b-103">Configure future life events</span></span>

<span data-ttu-id="f397b-104">Du kan planlegge fremtidige levetidshendelser i Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="f397b-104">You can schedule future life events in Dynamics 365 Human Resources.</span></span>

1. <span data-ttu-id="f397b-105">I arbeidsområdte **Fordelsbehandling**, under **Oppsett**, velger du **Fremtidige levetidshendelser**.</span><span class="sxs-lookup"><span data-stu-id="f397b-105">In the **Benefits management** workspace, under **Setup**, select **Future life events**.</span></span>

2. <span data-ttu-id="f397b-106">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="f397b-106">Select **New**.</span></span>

3. <span data-ttu-id="f397b-107">Angi verdier for de følgende feltene:</span><span class="sxs-lookup"><span data-stu-id="f397b-107">Specify values for the following fields:</span></span>

   | <span data-ttu-id="f397b-108">Felt</span><span class="sxs-lookup"><span data-stu-id="f397b-108">Field</span></span> | <span data-ttu-id="f397b-109">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="f397b-109">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="f397b-110">Levetidshendelsesdato</span><span class="sxs-lookup"><span data-stu-id="f397b-110">Life event date</span></span> | <span data-ttu-id="f397b-111">Systemet behandler alle hendelser i løpet av registreringsperioden som inntreffer frem til denne datoen.</span><span class="sxs-lookup"><span data-stu-id="f397b-111">The system processes all events during the enrollment period that occur up until this date.</span></span> |
   | <span data-ttu-id="f397b-112">Levetidshendelse logget</span><span class="sxs-lookup"><span data-stu-id="f397b-112">Life event logged</span></span> | <span data-ttu-id="f397b-113">Datoen og klokkeslettet da levetidshendelsen ble logget.</span><span class="sxs-lookup"><span data-stu-id="f397b-113">Date and time when the life event is logged.</span></span> |
   | <span data-ttu-id="f397b-114">Loggtype</span><span class="sxs-lookup"><span data-stu-id="f397b-114">Log type</span></span> | <span data-ttu-id="f397b-115">Viser om handlingen er én av følgende:</span><span class="sxs-lookup"><span data-stu-id="f397b-115">Shows whether the action is one of the following:</span></span></br></br><span data-ttu-id="f397b-116">- **Oppdatering** – en endring i en eksisterende post som sporer levetidshendelser</span><span class="sxs-lookup"><span data-stu-id="f397b-116">- **Update** – a change to an existing record that is tracking life events</span></span></br></br><span data-ttu-id="f397b-117">- **Sett inn** – oppretting av en ny levetidshendelsespost</span><span class="sxs-lookup"><span data-stu-id="f397b-117">- **Insert** – the creation of a new life event record</span></span> |
   | <span data-ttu-id="f397b-118">ID for levetidshendelsestype</span><span class="sxs-lookup"><span data-stu-id="f397b-118">Life event type ID</span></span> | <span data-ttu-id="f397b-119">Den unike ID-en for levetidshendelsestypen.</span><span class="sxs-lookup"><span data-stu-id="f397b-119">The life event type unique identifier.</span></span> |
   | <span data-ttu-id="f397b-120">Levetidshendelsestype</span><span class="sxs-lookup"><span data-stu-id="f397b-120">Life event type</span></span> | <span data-ttu-id="f397b-121">En katalysator for å oppdatere en ansatts fordelsregistrering.</span><span class="sxs-lookup"><span data-stu-id="f397b-121">A catalyst to updating an employee’s benefits enrollment.</span></span> <span data-ttu-id="f397b-122">Hvis du vil ha mer informasjon, kan du se delen om utløsere for levetidshendelser.</span><span class="sxs-lookup"><span data-stu-id="f397b-122">For more details, see the Life event triggers section.</span></span> |
   | <span data-ttu-id="f397b-123">Status</span><span class="sxs-lookup"><span data-stu-id="f397b-123">Status</span></span> | <span data-ttu-id="f397b-124">Om levetidshendelsen er behandlet eller ikke.</span><span class="sxs-lookup"><span data-stu-id="f397b-124">Whether the life event has been processed or not.</span></span> |
   | <span data-ttu-id="f397b-125">Linje</span><span class="sxs-lookup"><span data-stu-id="f397b-125">Line</span></span> | <span data-ttu-id="f397b-126">Linjenummeret til den fremtidige levetidshendelsen.</span><span class="sxs-lookup"><span data-stu-id="f397b-126">The line number of the future life event.</span></span> |

4. <span data-ttu-id="f397b-127">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="f397b-127">Select **Save**.</span></span> 
