---
title: Konfigurere permisjons- og fraværsparametere
description: Du kan definere personalparametere for permisjon og fravær i Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: eb992cbfbed33f88e125d3a8b721f8815414599a
ms.sourcegitcommit: 79f8aa2c0b166a423db9b8503da53e96e3fc43dc
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2020
ms.locfileid: "3197987"
---
# <a name="configure-leave-and-absence-parameters"></a><span data-ttu-id="5056d-103">Konfigurere permisjons- og fraværsparametere</span><span class="sxs-lookup"><span data-stu-id="5056d-103">Configure leave and absence parameters</span></span>

<span data-ttu-id="5056d-104">Før du definerer permisjons- og fraværsplaner i Dynamics 365 Human Resources, kan det være lurt å kontrollere innstillingene for alle relaterte personaleparametere, inkludert:</span><span class="sxs-lookup"><span data-stu-id="5056d-104">Before you set up leave and absence plans in Dynamics 365 Human Resources, it's a good idea to verify the settings for all related human resources parameters, including:</span></span>

- <span data-ttu-id="5056d-105">Nummerserie for permisjonsforespørsler</span><span class="sxs-lookup"><span data-stu-id="5056d-105">Number sequence for leave requests</span></span>
- <span data-ttu-id="5056d-106">Innstillinger for sykemelding og permisjon (FMLA)</span><span class="sxs-lookup"><span data-stu-id="5056d-106">Family Medical and Leave Act (FMLA) settings</span></span>
- <span data-ttu-id="5056d-107">Innstillinger i Ansattselvbetjening for permisjons- og fraværsforespørsler</span><span class="sxs-lookup"><span data-stu-id="5056d-107">Employee self service settings for leave and absence requests</span></span>
- <span data-ttu-id="5056d-108">Parametere for permisjon og fravær</span><span class="sxs-lookup"><span data-stu-id="5056d-108">Leave and absence parameters</span></span>

## <a name="view-and-change-human-resources-parameters"></a><span data-ttu-id="5056d-109">Vise og endre personaleparametere</span><span class="sxs-lookup"><span data-stu-id="5056d-109">View and change human resources parameters</span></span>

1. <span data-ttu-id="5056d-110">På siden **Permisjon og fravær** velger du **Koblinger**-fanen.</span><span class="sxs-lookup"><span data-stu-id="5056d-110">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="5056d-111">Under **Oppsett** velger du **Personalparametere**.</span><span class="sxs-lookup"><span data-stu-id="5056d-111">Under **Setup**, select **Human resources parameters**.</span></span>

3. <span data-ttu-id="5056d-112">I kategorien **Nummerserier** bekrefter du **Nummerseriekode** for **ID for permisjonsforespørsel** og endrer etter behov.</span><span class="sxs-lookup"><span data-stu-id="5056d-112">On the **Number sequences** tab, verify the **Number sequence code** for **Leave request ID** and change as necessary.</span></span> <span data-ttu-id="5056d-113">Denne innstillingen bestemmer serien som skal brukes til å tilordne ID-er automatisk til permisjonsforespørsler.</span><span class="sxs-lookup"><span data-stu-id="5056d-113">This setting determines the sequence used for automatically assigning IDs to leave requests.</span></span>

4. <span data-ttu-id="5056d-114">I kategorien **FMLA** kontrollerer du FMLA-innstillingene og endrer etter behov.</span><span class="sxs-lookup"><span data-stu-id="5056d-114">On the **FMLA** tab, verify the FMLA settings and change as necessary.</span></span>

5. <span data-ttu-id="5056d-115">I kategorien **Ansattselvbetjening** angir du om ledere kan angi permisjons- og fraværsforespørsler på vegne av de ansatte.</span><span class="sxs-lookup"><span data-stu-id="5056d-115">On the **Employee self service** tab, indicate whether managers can enter leave and absence requests on behalf of their employees.</span></span>

6. <span data-ttu-id="5056d-116">I kategorien **Permisjon og fravær** kontrollerer du innstillingene og endrer etter behov.</span><span class="sxs-lookup"><span data-stu-id="5056d-116">On the **Leave and absence** tab, verify the settings and change as necessary.</span></span>

7. <span data-ttu-id="5056d-117">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="5056d-117">Select **Save**.</span></span>

## <a name="view-and-change-leave-and-absence-parameters"></a><span data-ttu-id="5056d-118">Vise og endre permisjons- og fraværsparametere</span><span class="sxs-lookup"><span data-stu-id="5056d-118">View and change leave and absence parameters</span></span>

1. <span data-ttu-id="5056d-119">På siden **Permisjon og fravær** velger du **Koblinger**-fanen.</span><span class="sxs-lookup"><span data-stu-id="5056d-119">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="5056d-120">Under **Oppsett**velger du **Permisjons- og fraværsparametere**.</span><span class="sxs-lookup"><span data-stu-id="5056d-120">Under **Setup**, select **Leave and absence parameters**.</span></span>

3. <span data-ttu-id="5056d-121">Angi følgende parametere i kategorien **Generelt**:</span><span class="sxs-lookup"><span data-stu-id="5056d-121">On the **General** tab, set the following parameters:</span></span>
 
    - <span data-ttu-id="5056d-122">Angi **Enhet for permisjon og fravær** til enten timer eller dager.</span><span class="sxs-lookup"><span data-stu-id="5056d-122">Set **Unit for leave and absence** to either hours or days.</span></span> <span data-ttu-id="5056d-123">Hvis dager, kan du velge **Aktiver halvdagsdefinisjon** for å la de ansatte velge enten den første eller andre halvparten av dagen i fritidsforespørsler.</span><span class="sxs-lookup"><span data-stu-id="5056d-123">If days, you can select **Enable half day definition** to allow employees to choose either first or second half of day in their time-off requests.</span></span> 

    - <span data-ttu-id="5056d-124">Velg **Gyldighetsdato for måneder med jobberfaring** for å angi når avsetningsratene trer i kraft for permisjonsplaner som bruker måneder med jobberfaring.</span><span class="sxs-lookup"><span data-stu-id="5056d-124">Select **Months of service effective date** to set when the accrual rates take effect for leave plans using months of service.</span></span>

    - <span data-ttu-id="5056d-125">Velg **Saldoberegning** for å vise saldoer per dag eller per avsetningsperiode.</span><span class="sxs-lookup"><span data-stu-id="5056d-125">Select **Balance calculation** to display balances display as of today or as of the accrual period.</span></span> <span data-ttu-id="5056d-126">Hvis du velger **Saldo per i dag**, viser saldoen summen av alle avsetningene, justeringene og forespørslene per i dag.</span><span class="sxs-lookup"><span data-stu-id="5056d-126">If you select **Balance as of today**, the balance displays the total of all accruals, adjustments, and requests as of today.</span></span> <span data-ttu-id="5056d-127">Hvis du velger **Saldo per avsetningsperiode**, viser saldoen summen av alle avsetningene, justeringene og forespørslene fra avsetningsperioden som er definert av frekvensen i permisjonsplanen.</span><span class="sxs-lookup"><span data-stu-id="5056d-127">If you select **Balance as of accrual period**, the balance displays the total of all accruals, adjustments, and requests as of the accrual period defined by the frequency in the leave plan.</span></span> 

## <a name="configure-calendar-parameters"></a><span data-ttu-id="5056d-128">Konfigurere kalenderparametere</span><span class="sxs-lookup"><span data-stu-id="5056d-128">Configure calendar parameters</span></span>

1. <span data-ttu-id="5056d-129">På siden **Permisjon og fravær** velger du **Koblinger**-fanen.</span><span class="sxs-lookup"><span data-stu-id="5056d-129">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="5056d-130">Under **Oppsett**velger du **Permisjons- og fraværsparametere**.</span><span class="sxs-lookup"><span data-stu-id="5056d-130">Under **Setup**, select **Leave and absence parameters**.</span></span>

3. <span data-ttu-id="5056d-131">I kategorien **Kalender** endrer du kalenderinnstillinger etter behov.</span><span class="sxs-lookup"><span data-stu-id="5056d-131">On the **Calendar** tab, change calendar settings as necessary.</span></span>

4. <span data-ttu-id="5056d-132">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="5056d-132">Select **Save**.</span></span>

## <a name="see-also"></a><span data-ttu-id="5056d-133">Se også</span><span class="sxs-lookup"><span data-stu-id="5056d-133">See also</span></span>

- [<span data-ttu-id="5056d-134">Oversikt over permisjon og fravær</span><span class="sxs-lookup"><span data-stu-id="5056d-134">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
