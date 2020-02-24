---
title: Konfigurere fremtidige levetidshendelser
description: Du kan planlegge fremtidige levetidshendelser i Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitFutureLifeEvents
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 655070e52e3d1f43ca6904ce3218582868f193fe
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010085"
---
# <a name="configure-future-life-events"></a><span data-ttu-id="59ca2-103">Konfigurere fremtidige levetidshendelser</span><span class="sxs-lookup"><span data-stu-id="59ca2-103">Configure future life events</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="59ca2-104">Du kan planlegge fremtidige levetidshendelser i Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="59ca2-104">You can schedule future life events in Dynamics 365 Human Resources.</span></span>

1. <span data-ttu-id="59ca2-105">I arbeidsområdte **Fordelsbehandling**, under **Oppsett**, velger du **Fremtidige levetidshendelser**.</span><span class="sxs-lookup"><span data-stu-id="59ca2-105">In the **Benefits management** workspace, under **Setup**, select **Future life events**.</span></span>

2. <span data-ttu-id="59ca2-106">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="59ca2-106">Select **New**.</span></span>

3. <span data-ttu-id="59ca2-107">Angi verdier for de følgende feltene:</span><span class="sxs-lookup"><span data-stu-id="59ca2-107">Specify values for the following fields:</span></span>

   | <span data-ttu-id="59ca2-108">Felt</span><span class="sxs-lookup"><span data-stu-id="59ca2-108">Field</span></span> | <span data-ttu-id="59ca2-109">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="59ca2-109">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="59ca2-110">Levetidshendelsesdato</span><span class="sxs-lookup"><span data-stu-id="59ca2-110">Life event date</span></span> | <span data-ttu-id="59ca2-111">Systemet behandler alle hendelser i løpet av registreringsperioden som inntreffer frem til denne datoen.</span><span class="sxs-lookup"><span data-stu-id="59ca2-111">The system processes all events during the enrollment period that occur up until this date.</span></span> |
   | <span data-ttu-id="59ca2-112">Levetidshendelse logget</span><span class="sxs-lookup"><span data-stu-id="59ca2-112">Life event logged</span></span> | <span data-ttu-id="59ca2-113">Datoen og klokkeslettet da levetidshendelsen ble logget.</span><span class="sxs-lookup"><span data-stu-id="59ca2-113">Date and time when the life event is logged.</span></span> |
   | <span data-ttu-id="59ca2-114">Loggtype</span><span class="sxs-lookup"><span data-stu-id="59ca2-114">Log type</span></span> | <span data-ttu-id="59ca2-115">Viser om handlingen er én av følgende:</span><span class="sxs-lookup"><span data-stu-id="59ca2-115">Shows whether the action is one of the following:</span></span></br></br><span data-ttu-id="59ca2-116">- **Oppdatering** – en endring i en eksisterende post som sporer levetidshendelser</span><span class="sxs-lookup"><span data-stu-id="59ca2-116">- **Update** – a change to an existing record that is tracking life events</span></span></br></br><span data-ttu-id="59ca2-117">- **Sett inn** – oppretting av en ny levetidshendelsespost</span><span class="sxs-lookup"><span data-stu-id="59ca2-117">- **Insert** – the creation of a new life event record</span></span> |
   | <span data-ttu-id="59ca2-118">ID for levetidshendelsestype</span><span class="sxs-lookup"><span data-stu-id="59ca2-118">Life event type ID</span></span> | <span data-ttu-id="59ca2-119">Den unike ID-en for levetidshendelsestypen.</span><span class="sxs-lookup"><span data-stu-id="59ca2-119">The life event type unique identifier.</span></span> |
   | <span data-ttu-id="59ca2-120">Levetidshendelsestype</span><span class="sxs-lookup"><span data-stu-id="59ca2-120">Life event type</span></span> | <span data-ttu-id="59ca2-121">En katalysator for å oppdatere en ansatts fordelsregistrering.</span><span class="sxs-lookup"><span data-stu-id="59ca2-121">A catalyst to updating an employee’s benefits enrollment.</span></span> <span data-ttu-id="59ca2-122">Hvis du vil ha mer informasjon, kan du se delen om utløsere for levetidshendelser.</span><span class="sxs-lookup"><span data-stu-id="59ca2-122">For more details, see the Life event triggers section.</span></span> |
   | <span data-ttu-id="59ca2-123">Status</span><span class="sxs-lookup"><span data-stu-id="59ca2-123">Status</span></span> | <span data-ttu-id="59ca2-124">Om levetidshendelsen er behandlet eller ikke.</span><span class="sxs-lookup"><span data-stu-id="59ca2-124">Whether the life event has been processed or not.</span></span> |
   | <span data-ttu-id="59ca2-125">Linje</span><span class="sxs-lookup"><span data-stu-id="59ca2-125">Line</span></span> | <span data-ttu-id="59ca2-126">Linjenummeret til den fremtidige levetidshendelsen.</span><span class="sxs-lookup"><span data-stu-id="59ca2-126">The line number of the future life event.</span></span> |

4. <span data-ttu-id="59ca2-127">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="59ca2-127">Select **Save**.</span></span> 
