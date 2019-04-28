---
title: Hva er nytt eller endret i Dynamics 365 for Talent Core HR (11. januar 2019)?
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 for Talent Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 01/11/2019
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
ms.search.validFrom: 2019-01-11
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e6a89ba455acbed9724da6826ac4d41c6a481490
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/19/2019
ms.locfileid: "856144"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-january-11-2019"></a><span data-ttu-id="94a88-103">Hva er nytt eller endret i Dynamics 365 for Talent Core HR (11. januar 2019)?</span><span class="sxs-lookup"><span data-stu-id="94a88-103">What's new or changed in Dynamics 365 for Talent Core HR (January 11, 2019)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="94a88-104">**Build 8.1.2100**</span><span class="sxs-lookup"><span data-stu-id="94a88-104">**Build 8.1.2100**</span></span>

<span data-ttu-id="94a88-105">Dette emnet beskriver funksjoner som enten er nye eller endret i Core HR.</span><span class="sxs-lookup"><span data-stu-id="94a88-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="changes"></a><span data-ttu-id="94a88-106">Endringer</span><span class="sxs-lookup"><span data-stu-id="94a88-106">Changes</span></span>

### <a name="validate-leave-requests-by-forecasting-available-balance"></a><span data-ttu-id="94a88-107">Validere permisjonsforespørsler ved hjelp av prognoser for tilgjengelig saldo</span><span class="sxs-lookup"><span data-stu-id="94a88-107">Validate leave requests by forecasting available balance</span></span>
<span data-ttu-id="94a88-108">Endringer i denne versjonen tillater ansatte å be om fremtidig permisjon uten å trekke fra den gjeldende saldoen.</span><span class="sxs-lookup"><span data-stu-id="94a88-108">Changes made in this release allow employees to request future leave time without subtracting from their current balance.</span></span> <span data-ttu-id="94a88-109">Standard arbeidsflyter brukes for eventuelle fremtidige forespørsler.</span><span class="sxs-lookup"><span data-stu-id="94a88-109">Standard workflows will be used for any future requests made.</span></span> <span data-ttu-id="94a88-110">Hvis du vil ha mer informasjon, les [Avsette fridager basert på arbeidstimer](leave-accrue-hours-worked.md).</span><span class="sxs-lookup"><span data-stu-id="94a88-110">For more information, read [Accrue time off based on hours worked](leave-accrue-hours-worked.md).</span></span>

### <a name="view-forecasted-leave-balance-in-ess-and-people"></a><span data-ttu-id="94a88-111">Vise anslått permisjonssaldo i ESS og Personer</span><span class="sxs-lookup"><span data-stu-id="94a88-111">View forecasted leave balance in ESS and People</span></span>
<span data-ttu-id="94a88-112">Denne funksjonen aktiverer visning av saldoer for fremtidige permisjonsperioder for Personale, ledere og ansatte.</span><span class="sxs-lookup"><span data-stu-id="94a88-112">This feature enables viewing of balances for future leave periods by HR, managers, and employees.</span></span> <span data-ttu-id="94a88-113">Ansatte kan vise fremtidige saldoer i arbeidsområdet **Ansattbetjening**, og Personale har tilgang til den samme informasjon ved hjelp av **Personer**-arbeidsområdet.</span><span class="sxs-lookup"><span data-stu-id="94a88-113">Employees can view future balances in the **Employee Self-Service** workspace and HR has access to the same information using the **People** workspace.</span></span>

### <a name="notifications-for-changing-leave-balances"></a><span data-ttu-id="94a88-114">Varslinger for å endre lønnssaldoer</span><span class="sxs-lookup"><span data-stu-id="94a88-114">Notifications for changing leave balances</span></span>
<span data-ttu-id="94a88-115">Lønnssaldoer viser den gjeldende saldoen for ansatte.</span><span class="sxs-lookup"><span data-stu-id="94a88-115">Leave balances will display the employees current balance.</span></span> <span data-ttu-id="94a88-116">Fremtidige saldoer er tilgjengelige i arbeidsområdene **Ansattselvbetjening** og **Personer** ved å angi en "per dato" for å beregne forventet saldo.</span><span class="sxs-lookup"><span data-stu-id="94a88-116">Future balances are available on the **Employee Self-Service** and **People** workspaces by entering an “as of date” to calculate the forecasted balance.</span></span>

<span data-ttu-id="94a88-117">Navigasjon er lagt til for å vise prognoseberegnede saldoer på følgende områder:</span><span class="sxs-lookup"><span data-stu-id="94a88-117">Navigation has been added to view forecasted balances in the following areas:</span></span>
  - <span data-ttu-id="94a88-118">**Fridager**-kort i arbeidsområet **Ansattselvbetjening**.</span><span class="sxs-lookup"><span data-stu-id="94a88-118">**Time off** card on the **Employee Self-Service** workspace.</span></span>
  - <span data-ttu-id="94a88-119">**Permisjon og fravær**-kort i arbeidsområdet **Lederselvbetjening** .</span><span class="sxs-lookup"><span data-stu-id="94a88-119">**Leave and absence** card on the **Manager Self-Service** workspace.</span></span>
  - <span data-ttu-id="94a88-120">**Permisjon og fravær**-siden i **Personer**-arbeidsområdet.</span><span class="sxs-lookup"><span data-stu-id="94a88-120">**Leave and absence** page on the **People** workspace.</span></span>

### <a name="allow-decimals-for-variable-compensation-plans-cash-plans"></a><span data-ttu-id="94a88-121">Tillat desimaler for variable kompensasjonsplaner (kontantplaner)</span><span class="sxs-lookup"><span data-stu-id="94a88-121">Allow decimals for Variable compensation plans (Cash plans)</span></span>
<span data-ttu-id="94a88-122">Variable kontantbelønninger og -planer har nå mer fleksibilitet for beløp og overstyringer for verdier med desimalbeløp.</span><span class="sxs-lookup"><span data-stu-id="94a88-122">Variable cash awards and plans now have the additional flexibility for amounts and overrides for values with decimal amounts.</span></span>

### <a name="unable-to-change-the-dates-on-variable-comp-enrollments-after-the-plan-is-saved"></a><span data-ttu-id="94a88-123">Kan ikke endre datoene i Variabel kompensasjonsregistrering når planen er lagret</span><span class="sxs-lookup"><span data-stu-id="94a88-123">Unable to change the dates on Variable comp enrollments after the plan is saved</span></span>
<span data-ttu-id="94a88-124">Denne endringen fører til at sluttdatoen for planen kan oppdateres (utvidet eller utløpt) når planen er lagret.</span><span class="sxs-lookup"><span data-stu-id="94a88-124">This change allows for the plan end date to be updated (extended or expired) after the plan has been saved.</span></span> <span data-ttu-id="94a88-125">Du kan fortsatt aktivere eller deaktivere planer uavhengig av start- og sluttdatoer.</span><span class="sxs-lookup"><span data-stu-id="94a88-125">You can still activate or de-activate plans independent of start and end dates.</span></span>

### <a name="payroll-information-available-when-assigned-the-payroll-admin-security-role"></a><span data-ttu-id="94a88-126">Lønnsinformasjon tilgjengelig når tilordnet Lønnsadministrator-sikkerhetsrollen</span><span class="sxs-lookup"><span data-stu-id="94a88-126">Payroll information available when assigned the Payroll admin security role</span></span>
<span data-ttu-id="94a88-127">Lønnsadministratorrollen er oppdatert for å få tilgang til lønnsinformasjonen under forespørselsprosessen.</span><span class="sxs-lookup"><span data-stu-id="94a88-127">The Payroll Administrator role has been updated to have access to the payroll information during the request process.</span></span>

### <a name="employee-self-service--position-hierarchy-drill-down-from-tile-fails-to-get-parent-node"></a><span data-ttu-id="94a88-128">Ansattselvbetjening | Neddrilling i stillingshierarki fra flis kan ikke hente overordnet node</span><span class="sxs-lookup"><span data-stu-id="94a88-128">Employee self-service | Position hierarchy drill-down from tile fails to get parent node</span></span>
<span data-ttu-id="94a88-129">Endringer er gjort for å fjerne en feil som oppstod ved tillegging av stillingshierarkiet til nye arbeidsområder og navigering i organisasjonsstrukturen.</span><span class="sxs-lookup"><span data-stu-id="94a88-129">Changes have been made to eliminate an error that occurred when adding the position hierarchy to new workspaces and navigating within the organizational structure.</span></span>

### <a name="new-validation-message-when-personnel-number-sequence-is-in-use"></a><span data-ttu-id="94a88-130">Ny valideringsmelding når personellnummerserie er i bruk</span><span class="sxs-lookup"><span data-stu-id="94a88-130">New validation message when personnel number sequence is in use</span></span>
<span data-ttu-id="94a88-131">En endring er gjort for å oppklare hva problemet er når du ansetter en ansatt og det neste personalnummeret er i bruk.</span><span class="sxs-lookup"><span data-stu-id="94a88-131">A change has been made to clarify what the issue is when you hire an employee and the next personnel number is in use.</span></span>

### <a name="employee-self-service-workspace-selected-as-the-initial-startup-page"></a><span data-ttu-id="94a88-132">Ansattselvbetjening-arbeidsområdet valgt som første oppstartsside</span><span class="sxs-lookup"><span data-stu-id="94a88-132">Employee self-service workspace selected as the initial startup page</span></span>
<span data-ttu-id="94a88-133">Når **Ansattselvbetjening**-arbeidsområdet er valgt som første oppstartsside for en bruker, og vedkommende ikke er tilordnet ansattrollen, vil systemet omdirigere til standard instrumentbord.</span><span class="sxs-lookup"><span data-stu-id="94a88-133">When the **Employee self-service** workspace is selected as the initial startup page for a user and that user is not assigned the employee role, the system will redirect to the default dashboard.</span></span>

### <a name="termination-reason-code-updates-position-assignment-record"></a><span data-ttu-id="94a88-134">Avslutningsårsakskode oppdaterer stillingstilordningspost</span><span class="sxs-lookup"><span data-stu-id="94a88-134">Termination reason code updates position assignment record</span></span>
<span data-ttu-id="94a88-135">Avslutningsårsakskoden oppdaterer nå stillingstilordningen når en ansatt slutter og stillingen avsluttes.</span><span class="sxs-lookup"><span data-stu-id="94a88-135">The termination reason code will now update the position assignment when terminating an employee and ending the position.</span></span> 
