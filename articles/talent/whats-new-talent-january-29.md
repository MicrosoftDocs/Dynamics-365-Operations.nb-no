---
title: Hva er nytt eller endret i Dynamics 365 for Talent (31. januar 2019)
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 for Talent.
author: Darinkramer
manager: AnnBe
ms.date: 01/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-01-29
ms.dyn365.ops.version: Talent
ms.openlocfilehash: ab43bab53afd979d64099425f0582f6c1bb5a8b0
ms.sourcegitcommit: 383a344deb5abf48584ea2ee7774b8dbbbec49b3
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/08/2019
ms.locfileid: "377856"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-january-31-2019"></a><span data-ttu-id="dc935-103">Hva er nytt eller endret i Dynamics 365 for Talent (31. januar 2019)</span><span class="sxs-lookup"><span data-stu-id="dc935-103">What's new or changed in Dynamics 365 for Talent (January 31, 2019)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="dc935-104">Dette emnet beskriver funksjoner som enten er nye eller endret i Dynamics 365 for Talent.</span><span class="sxs-lookup"><span data-stu-id="dc935-104">This topic describes features that are either new or changed in Dynamics 365 for Talent</span></span>

<span data-ttu-id="dc935-105">**Build 8.1.2128**</span><span class="sxs-lookup"><span data-stu-id="dc935-105">**Build 8.1.2128**</span></span>

## <a name="core-hr-changes"></a><span data-ttu-id="dc935-106">Core HR-endringer</span><span class="sxs-lookup"><span data-stu-id="dc935-106">Core HR Changes</span></span>

### <a name="time-off-taken-on-leave-people-card-doesnt-consider-leave-plan-dates"></a><span data-ttu-id="dc935-107">Fridager tatt på fraværskort vurderer ikke fraværsplandatoer</span><span class="sxs-lookup"><span data-stu-id="dc935-107">Time off taken on leave people card doesn't consider leave plan dates</span></span>
<span data-ttu-id="dc935-108">For de som har fraværsplaner som ikke kjøres i henhold til et kalenderår, viser **Tatt**-kortet nå fravær som er tatt i det plandefinerte fraværsåret.</span><span class="sxs-lookup"><span data-stu-id="dc935-108">For those that have leave plans that don’t run on a calendar year, the **Taken** card now displays time off that’s been taken in the plan-defined leave year.</span></span> <span data-ttu-id="dc935-109">For eksempel hvis organisasjonens fraværsår er 1. juni til og med 30. mai og en ansatt har tatt 3 dager fri i desember, viser **Tatt**-kortet 3 dager for 15. januar.</span><span class="sxs-lookup"><span data-stu-id="dc935-109">For example, if an organization’s leave year is June 1 through May 30 and an employee has taken 3 days off in December, the **Taken** card on January 15, will display 3 days.</span></span> 

### <a name="accrual-amounts-not-matching-tier-date-basis"></a><span data-ttu-id="dc935-110">Avsetningsbeløp samsvarer ikke med datogrunnlag for nivå</span><span class="sxs-lookup"><span data-stu-id="dc935-110">Accrual amounts not matching tier date basis</span></span>
<span data-ttu-id="dc935-111">Nye alternativer er lagt til for permisjon og fravær (**Personale**-parametere) for å gjøre det mulig for kunder å fastsette når ansattes dato for måneder med jobberfaring er gyldig.</span><span class="sxs-lookup"><span data-stu-id="dc935-111">New options have been added to leave and absence (**Human resources** parameters) to enable customers to determine when employees’ months of service date are effective.</span></span> <span data-ttu-id="dc935-112">I noen organisasjoner er datoen på slutten av måneden, men det kan være starten av neste måned for andre.</span><span class="sxs-lookup"><span data-stu-id="dc935-112">For some organizations, the date is the end of the month, but for others it may be the start of the next month.</span></span> <span data-ttu-id="dc935-113">En organisasjon kan for eksempel belønne ansatte med fri 31. desember, mens en annen gir fri 1. januar.</span><span class="sxs-lookup"><span data-stu-id="dc935-113">For example, one organization may award time off on December 31, while another may award time off on January 1.</span></span> <span data-ttu-id="dc935-114">Med dette alternativet kan du velge når belønningen skal skje.</span><span class="sxs-lookup"><span data-stu-id="dc935-114">This option will allow you to choose when the award should occur.</span></span> 

### <a name="worker-hire-actions-are-stuck-in-workflow-complete-state"></a><span data-ttu-id="dc935-115">Arbeideransettelseshandlinger står fast i "Arbeidsflyt fullført"-tilstand</span><span class="sxs-lookup"><span data-stu-id="dc935-115">Worker hire actions are stuck in "Workflow complete" state</span></span>
<span data-ttu-id="dc935-116">Endringer er gjort for å løse et problem der et lite antall arbeidsprosesser ble fullført med en "Arbeidsflyt fullført"-status.</span><span class="sxs-lookup"><span data-stu-id="dc935-116">Changes have been made to correct an issue where a small number of workflows finished with a "Workflow complete" status.</span></span> <span data-ttu-id="dc935-117">Nye arbeidsflyter skal nå flyttes til en "Fullført"-tilstand når arbeidsflyten er fullført.</span><span class="sxs-lookup"><span data-stu-id="dc935-117">New workflows should now move to a "Completed" state when the workflow finishes.</span></span> <span data-ttu-id="dc935-118">Arbeidsflyter med en Arbeidsflyt fullført-status blir overført til en feilstatus for å tillate oppdatering eller fjerning hvis nødvendig.</span><span class="sxs-lookup"><span data-stu-id="dc935-118">Any workflows in a workflow completed status will be transitioned to an error status to allow for updating or removal if required.</span></span> 
