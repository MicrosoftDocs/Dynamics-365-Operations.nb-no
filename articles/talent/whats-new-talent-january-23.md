---
title: Hva er nytt eller endret i Dynamics 365 Talent – Core HR (23. januar 2019)
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Talent – Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 01/23/2019
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
ms.search.validFrom: 2019-01-23
ms.dyn365.ops.version: Talent
ms.openlocfilehash: f1983d5a58fb2e6b1984727e1d7b44803b94cdce
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/24/2019
ms.locfileid: "2023982"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-core-hr-january-23-2019"></a><span data-ttu-id="15301-103">Hva er nytt eller endret i Dynamics 365 Talent: Core HR (23. januar 2019)</span><span class="sxs-lookup"><span data-stu-id="15301-103">What's new or changed in Dynamics 365 Talent: Core HR (January 23, 2019)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="15301-104">**Build 8.1.2121**</span><span class="sxs-lookup"><span data-stu-id="15301-104">**Build 8.1.2121**</span></span>

<span data-ttu-id="15301-105">Dette emnet beskriver funksjoner som enten er nye eller endret i Core HR.</span><span class="sxs-lookup"><span data-stu-id="15301-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="changes"></a><span data-ttu-id="15301-106">Endringer</span><span class="sxs-lookup"><span data-stu-id="15301-106">Changes</span></span>

### <a name="import-of-employee-fixed-compensation-not-working-when-creating-new-fixed-compensation-records"></a><span data-ttu-id="15301-107">Import av fast kompensasjon for ansatte fungerer ikke ved oppretting av nye poster for fast kompensasjon</span><span class="sxs-lookup"><span data-stu-id="15301-107">Import of employee fixed compensation not working when creating new fixed compensation records</span></span>
<span data-ttu-id="15301-108">En endring er gjort i enheten for fast ansattkompensasjon for å hente kompensasjonsnivået ved import.</span><span class="sxs-lookup"><span data-stu-id="15301-108">A change has been made to the employee fixed compensation entity to retrieve the compensation level upon import.</span></span> <span data-ttu-id="15301-109">Før denne versjonen ble det vist en melding som indikerer at nivået er nødvendig.</span><span class="sxs-lookup"><span data-stu-id="15301-109">Prior to this release, a message was displayed indicating that the level was required.</span></span>

### <a name="remove-the-minimum-balance-field-from-the-time-off-request-dialog-box"></a><span data-ttu-id="15301-110">Fjernet feltet for minimumssaldo fra dialogboksen for fraværsforespørsel</span><span class="sxs-lookup"><span data-stu-id="15301-110">Remove the minimum balance field from the time off request dialog box</span></span>
<span data-ttu-id="15301-111">Feltet for **Minimumssaldo** er fjernet fra dialogboksen for **fraværsforespørsel**.</span><span class="sxs-lookup"><span data-stu-id="15301-111">The **Minimum balance** field has been removed from the **Time off request** dialog box.</span></span> <span data-ttu-id="15301-112">Denne endringen påvirker alle områder der fravær kan forespørres.</span><span class="sxs-lookup"><span data-stu-id="15301-112">This change affects all areas where time off can be requested.</span></span>

### <a name="data-upgrade-for-compensation-levels-not-updating-in-all-scenarios"></a><span data-ttu-id="15301-113">Dataoppgradering for kompensasjonsnivåer som ikke oppdateres i alle scenarioer</span><span class="sxs-lookup"><span data-stu-id="15301-113">Data upgrade for compensation levels not updating in all scenarios</span></span>
<span data-ttu-id="15301-114">En endring er gjort for å oppdatere kompensasjonsnivået i planer om fast kompensasjon.</span><span class="sxs-lookup"><span data-stu-id="15301-114">A change has been made to update the compensation level on fixed compensation plans.</span></span> <span data-ttu-id="15301-115">Denne endringen vil fylle ut kompensasjonsnivået i faste planer for jobben som er tilordnet den ansatte.</span><span class="sxs-lookup"><span data-stu-id="15301-115">This change will populate the compensation level on fixed plans for the job assigned to the employee.</span></span>

### <a name="payroll-information-in-the-manage-changes-page-is-only-available-when-logged-in-as-system-administrator"></a><span data-ttu-id="15301-116">Lønnsinformasjon på siden Behandle endringer er bare tilgjengelig når du er logget på som systemansvarlig</span><span class="sxs-lookup"><span data-stu-id="15301-116">Payroll information in the Manage changes page is only available when logged in as System Administrator</span></span>
<span data-ttu-id="15301-117">Denne endringen gir ansatte med lønnsadministratorrollen tilgang til lønnsinformasjon på siden **Tidslinje for endringer > Administrer endringer** for stillingen.</span><span class="sxs-lookup"><span data-stu-id="15301-117">This change allows employees with the Payroll Administrator role access to the payroll information on the **Changes timeline > Manage changes** page for the position.</span></span>

### <a name="job-fields-default-to-positions"></a><span data-ttu-id="15301-118">Jobbfelt går som standard til stillinger</span><span class="sxs-lookup"><span data-stu-id="15301-118">Job fields default to positions</span></span>
<span data-ttu-id="15301-119">Når jobben endres for en stilling, vil jobbfeltene som standard settes til stillingen.</span><span class="sxs-lookup"><span data-stu-id="15301-119">When changing the job on a position, job fields will default to the position.</span></span> <span data-ttu-id="15301-120">En varselsmelding vises og gir et alternativ for å godta standardverdiene eller beholde de eksisterende verdiene for disse feltene.</span><span class="sxs-lookup"><span data-stu-id="15301-120">An alert message will appear giving an option to accept the default values or keep the existing values for those fields.</span></span>

### <a name="probation-period-and-calendar-are-not-displayed-for-future-hired-employees"></a><span data-ttu-id="15301-121">Prøveperiode og kalender vises ikke for fremtidige ansatte.</span><span class="sxs-lookup"><span data-stu-id="15301-121">Probation period and calendar are not displayed for future hired employees.</span></span>
<span data-ttu-id="15301-122">Med denne endringen er det lagt til **Prøveperiode** og **Kalender** på siden **Behandle endringer** for å tillate dataregistrering for fremtidige og tidligere ansatte.</span><span class="sxs-lookup"><span data-stu-id="15301-122">With this change, **Probation period** and **Calendar** fields have been added to the **Manage changes** page to allow for data entry for future and past employees.</span></span>

### <a name="platform-update-23-for-finance-and-operations"></a><span data-ttu-id="15301-123">Platform update 23 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="15301-123">Platform update 23 for Finance and Operations</span></span>
<span data-ttu-id="15301-124">Mindre feilrettinger er inkludert som en del av plattformoppdatering 23 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="15301-124">Minor bug fixes have been included as part of Platform update 23 for Finance and Operations.</span></span> <span data-ttu-id="15301-125">Hvis du vil ha mer informasjon, se [Hva er nytt eller endret i Dynamics 365 Finance and Operations plattformoppdatering 23 (januar 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-23).</span><span class="sxs-lookup"><span data-stu-id="15301-125">For more information, see [What's new or changed in Dynamics 365 Finance and Operations platform update 23 (January 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-23).</span></span> 
