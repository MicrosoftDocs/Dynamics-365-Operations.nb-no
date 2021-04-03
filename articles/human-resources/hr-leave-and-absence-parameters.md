---
title: Konfigurere permisjons- og fraværsparametere
description: Du kan definere personalparametere for permisjon og fravær i Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 11/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: db96073f0a16f1c710fbfebb2d08a1d693eab1e1
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/17/2021
ms.locfileid: "5463388"
---
# <a name="configure-leave-and-absence-parameters"></a><span data-ttu-id="e0b57-103">Konfigurere permisjons- og fraværsparametere</span><span class="sxs-lookup"><span data-stu-id="e0b57-103">Configure leave and absence parameters</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="e0b57-104">Før du definerer permisjons- og fraværsplaner i Dynamics 365 Human Resources, kan det være lurt å kontrollere innstillingene for alle relaterte personaleparametere, inkludert:</span><span class="sxs-lookup"><span data-stu-id="e0b57-104">Before you set up leave and absence plans in Dynamics 365 Human Resources, it's a good idea to verify the settings for all related human resources parameters, including:</span></span>

- <span data-ttu-id="e0b57-105">Nummerserie for permisjonsforespørsler</span><span class="sxs-lookup"><span data-stu-id="e0b57-105">Number sequence for leave requests</span></span>
- <span data-ttu-id="e0b57-106">Innstillinger for sykemelding og permisjon (FMLA)</span><span class="sxs-lookup"><span data-stu-id="e0b57-106">Family Medical and Leave Act (FMLA) settings</span></span>
- <span data-ttu-id="e0b57-107">Innstillinger i Ansattselvbetjening for permisjons- og fraværsforespørsler</span><span class="sxs-lookup"><span data-stu-id="e0b57-107">Employee self service settings for leave and absence requests</span></span>
- <span data-ttu-id="e0b57-108">Parametere for permisjon og fravær</span><span class="sxs-lookup"><span data-stu-id="e0b57-108">Leave and absence parameters</span></span>

## <a name="view-and-change-human-resources-parameters"></a><span data-ttu-id="e0b57-109">Vise og endre personaleparametere</span><span class="sxs-lookup"><span data-stu-id="e0b57-109">View and change human resources parameters</span></span>

1. <span data-ttu-id="e0b57-110">På siden **Permisjon og fravær** velger du **Koblinger**-fanen.</span><span class="sxs-lookup"><span data-stu-id="e0b57-110">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="e0b57-111">Under **Oppsett** velger du **Personalparametere**.</span><span class="sxs-lookup"><span data-stu-id="e0b57-111">Under **Setup**, select **Human resources parameters**.</span></span>

3. <span data-ttu-id="e0b57-112">I kategorien **Nummerserier** bekrefter du **Nummerseriekode** for **ID for permisjonsforespørsel** og endrer etter behov.</span><span class="sxs-lookup"><span data-stu-id="e0b57-112">On the **Number sequences** tab, verify the **Number sequence code** for **Leave request ID** and change as necessary.</span></span> <span data-ttu-id="e0b57-113">Denne innstillingen bestemmer serien som skal brukes til å tilordne ID-er automatisk til permisjonsforespørsler.</span><span class="sxs-lookup"><span data-stu-id="e0b57-113">This setting determines the sequence used for automatically assigning IDs to leave requests.</span></span>

4. <span data-ttu-id="e0b57-114">I kategorien **FMLA** kontrollerer du FMLA-innstillingene og endrer etter behov.</span><span class="sxs-lookup"><span data-stu-id="e0b57-114">On the **FMLA** tab, verify the FMLA settings and change as necessary.</span></span>

5. <span data-ttu-id="e0b57-115">I kategorien **Ansattselvbetjening** angir du om ledere kan angi permisjons- og fraværsforespørsler på vegne av de ansatte.</span><span class="sxs-lookup"><span data-stu-id="e0b57-115">On the **Employee self service** tab, indicate whether managers can enter leave and absence requests on behalf of their employees.</span></span>

7. <span data-ttu-id="e0b57-116">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="e0b57-116">Select **Save**.</span></span>

>[!IMPORTANT]
><span data-ttu-id="e0b57-117">Visning av permisjon og fravær på tvers av firmaer er for øyeblikket i forhåndsversjon.</span><span class="sxs-lookup"><span data-stu-id="e0b57-117">Viewing leave and absence across companies is currently in preview.</span></span> <span data-ttu-id="e0b57-118">Du må aktivere den i **sandkassemiljøet** for å vise alternativet for permisjon og fravær.</span><span class="sxs-lookup"><span data-stu-id="e0b57-118">You'll need to enable it in your **Sandbox** environment to display the option for leave and absence.</span></span> <span data-ttu-id="e0b57-119">Hvis du vil ha mer informasjon om aktivering av evalueringsfunksjonalitet, kan du se [Behandle funksjoner](hr-admin-manage-features.md).</span><span class="sxs-lookup"><span data-stu-id="e0b57-119">For more information about enabling preview features, see [Manage features](hr-admin-manage-features.md).</span></span>

## <a name="view-and-change-human-resources-shared-parameters"></a><span data-ttu-id="e0b57-120">Vise og endre delte parametere for Human Resources</span><span class="sxs-lookup"><span data-stu-id="e0b57-120">View and change Human resources shared parameters</span></span>

1. <span data-ttu-id="e0b57-121">På siden **Personaladministrasjon** velger du **Koblinger**-fanen.</span><span class="sxs-lookup"><span data-stu-id="e0b57-121">On the **Personnel management** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="e0b57-122">Under **Oppsett** velger du **delte parametere for Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="e0b57-122">Under **Setup**, select **Human resources shared parameters**.</span></span>

3. <span data-ttu-id="e0b57-123">I fanen **Avansert tilgang** velger du **Ja** for å **aktivere permisjonsvisning på tvers av firmaer** for å tillate at permisjon vises på tvers av firmaet.</span><span class="sxs-lookup"><span data-stu-id="e0b57-123">On the **Advance access** tab, select **Yes** for **Enable cross company leave view** to allow leave to be viewed across company.</span></span>

4. <span data-ttu-id="e0b57-124">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="e0b57-124">Select **Save**.</span></span>

## <a name="view-and-change-leave-and-absence-parameters"></a><span data-ttu-id="e0b57-125">Vise og endre permisjons- og fraværsparametere</span><span class="sxs-lookup"><span data-stu-id="e0b57-125">View and change leave and absence parameters</span></span>

1. <span data-ttu-id="e0b57-126">På siden **Permisjon og fravær** velger du **Koblinger**-fanen.</span><span class="sxs-lookup"><span data-stu-id="e0b57-126">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="e0b57-127">Under **Oppsett** velger du **Permisjons- og fraværsparametere**.</span><span class="sxs-lookup"><span data-stu-id="e0b57-127">Under **Setup**, select **Leave and absence parameters**.</span></span>

3. <span data-ttu-id="e0b57-128">Angi følgende parametere i kategorien **Generelt**:</span><span class="sxs-lookup"><span data-stu-id="e0b57-128">On the **General** tab, set the following parameters:</span></span>
 
    - <span data-ttu-id="e0b57-129">Angi **Enhet for permisjon og fravær** til enten timer eller dager.</span><span class="sxs-lookup"><span data-stu-id="e0b57-129">Set **Unit for leave and absence** to either hours or days.</span></span> <span data-ttu-id="e0b57-130">Hvis dager, kan du velge **Aktiver halvdagsdefinisjon** for å la de ansatte velge enten den første eller andre halvparten av dagen i fritidsforespørsler.</span><span class="sxs-lookup"><span data-stu-id="e0b57-130">If days, you can select **Enable half day definition** to allow employees to choose either first or second half of day in their time-off requests.</span></span> 

    - <span data-ttu-id="e0b57-131">Velg **Gyldighetsdato for måneder med jobberfaring** for å angi når avsetningsratene trer i kraft for permisjonsplaner som bruker måneder med jobberfaring.</span><span class="sxs-lookup"><span data-stu-id="e0b57-131">Select **Months of service effective date** to set when the accrual rates take effect for leave plans using months of service.</span></span>

    - <span data-ttu-id="e0b57-132">Velg **Saldoberegning** for å vise saldoer per dag eller per avsetningsperiode.</span><span class="sxs-lookup"><span data-stu-id="e0b57-132">Select **Balance calculation** to display balances as of today or as of the accrual period.</span></span> <span data-ttu-id="e0b57-133">Hvis du velger **Saldo per i dag**, viser saldoen summen av alle avsetningene, justeringene og forespørslene per i dag.</span><span class="sxs-lookup"><span data-stu-id="e0b57-133">If you select **Balance as of today**, the balance displays the total of all accruals, adjustments, and requests as of today.</span></span> <span data-ttu-id="e0b57-134">Hvis du velger **Saldo per avsetningsperiode**, viser saldoen summen av alle avsetningene, justeringene og forespørslene fra avsetningsperioden som er definert av frekvensen i permisjonsplanen.</span><span class="sxs-lookup"><span data-stu-id="e0b57-134">If you select **Balance as of accrual period**, the balance displays the total of all accruals, adjustments, and requests as of the accrual period defined by the frequency in the leave plan.</span></span> 

    - <span data-ttu-id="e0b57-135">Angi starttidspunktet for den satsvise jobben for utløpet av overføring.</span><span class="sxs-lookup"><span data-stu-id="e0b57-135">Set the start time for the carry forward expiration batch job.</span></span>  
    
    - <span data-ttu-id="e0b57-136">Velg **Ja** for **Tillat ansatte å kjøpe permisjon** og **Tillat ansatte å selge permisjon**.</span><span class="sxs-lookup"><span data-stu-id="e0b57-136">Select **Yes** for **Allow employees to buy leave** and **Allow employees to sell leave**.</span></span> <span data-ttu-id="e0b57-137">Hvis du velger **Ja** for disse alternativene, kan du opprette policyer for kjøp og salg av permisjoner og gjøre det mulig for ansatte å sende inn og selge permisjonsforespørsler.</span><span class="sxs-lookup"><span data-stu-id="e0b57-137">If you select **Yes** for these options, you can create buy and sell leave policies and enable employees to submit buy and sell leave requests.</span></span>

## <a name="configure-calendar-parameters"></a><span data-ttu-id="e0b57-138">Konfigurere kalenderparametere</span><span class="sxs-lookup"><span data-stu-id="e0b57-138">Configure calendar parameters</span></span>

1. <span data-ttu-id="e0b57-139">På siden **Permisjon og fravær** velger du **Koblinger**-fanen.</span><span class="sxs-lookup"><span data-stu-id="e0b57-139">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="e0b57-140">Under **Oppsett** velger du **Permisjons- og fraværsparametere**.</span><span class="sxs-lookup"><span data-stu-id="e0b57-140">Under **Setup**, select **Leave and absence parameters**.</span></span>

3. <span data-ttu-id="e0b57-141">I kategorien **Kalender** endrer du kalenderinnstillinger etter behov.</span><span class="sxs-lookup"><span data-stu-id="e0b57-141">On the **Calendar** tab, change calendar settings as necessary.</span></span>

4. <span data-ttu-id="e0b57-142">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="e0b57-142">Select **Save**.</span></span>

## <a name="see-also"></a><span data-ttu-id="e0b57-143">Se også</span><span class="sxs-lookup"><span data-stu-id="e0b57-143">See also</span></span>

- [<span data-ttu-id="e0b57-144">Oversikt over permisjon og fravær</span><span class="sxs-lookup"><span data-stu-id="e0b57-144">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]