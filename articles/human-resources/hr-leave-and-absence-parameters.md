---
title: Konfigurere permisjons- og fraværsparametere
description: Du kan definere personalparametere for permisjon og fravær i Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
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
ms.openlocfilehash: 2acb8502ebcab122a0a1ff21e9f5e23931026327
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010053"
---
# <a name="configure-leave-and-absence-parameters"></a><span data-ttu-id="9c677-103">Konfigurere permisjons- og fraværsparametere</span><span class="sxs-lookup"><span data-stu-id="9c677-103">Configure leave and absence parameters</span></span>

<span data-ttu-id="9c677-104">Før du definerer permisjons- og fraværsplaner i Dynamics 365 Human Resources, kan det være lurt å kontrollere innstillingene for alle relaterte personaleparametere, inkludert:</span><span class="sxs-lookup"><span data-stu-id="9c677-104">Before you set up leave and absence plans in Dynamics 365 Human Resources, it's a good idea to verify the settings for all related human resources parameters, including:</span></span>

- <span data-ttu-id="9c677-105">Nummerserie for permisjonsforespørsler</span><span class="sxs-lookup"><span data-stu-id="9c677-105">Number sequence for leave requests</span></span>
- <span data-ttu-id="9c677-106">Innstillinger for sykemelding og permisjon (FMLA)</span><span class="sxs-lookup"><span data-stu-id="9c677-106">Family Medical and Leave Act (FMLA) settings</span></span>
- <span data-ttu-id="9c677-107">Innstillinger i Ansattselvbetjening for permisjons- og fraværsforespørsler</span><span class="sxs-lookup"><span data-stu-id="9c677-107">Employee self service settings for leave and absence requests</span></span>
- <span data-ttu-id="9c677-108">Parametere for permisjon og fravær</span><span class="sxs-lookup"><span data-stu-id="9c677-108">Leave and absence parameters</span></span>

## <a name="view-and-change-human-resources-parameters"></a><span data-ttu-id="9c677-109">Vise og endre personaleparametere</span><span class="sxs-lookup"><span data-stu-id="9c677-109">View and change human resources parameters</span></span>

1. <span data-ttu-id="9c677-110">På siden **Permisjon og fravær** velger du **Koblinger**-fanen.</span><span class="sxs-lookup"><span data-stu-id="9c677-110">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="9c677-111">Under **Oppsett** velger du **Personalparametere**.</span><span class="sxs-lookup"><span data-stu-id="9c677-111">Under **Setup**, select **Human resources parameters**.</span></span>

3. <span data-ttu-id="9c677-112">I kategorien **Nummerserier** bekrefter du **Nummerseriekode** for **ID for permisjonsforespørsel** og endrer etter behov.</span><span class="sxs-lookup"><span data-stu-id="9c677-112">On the **Number sequences** tab, verify the **Number sequence code** for **Leave request ID** and change as necessary.</span></span> <span data-ttu-id="9c677-113">Denne innstillingen bestemmer serien som skal brukes til å tilordne ID-er automatisk til permisjonsforespørsler.</span><span class="sxs-lookup"><span data-stu-id="9c677-113">This setting determines the sequence used for automatically assigning IDs to leave requests.</span></span>

4. <span data-ttu-id="9c677-114">I kategorien **FMLA** kontrollerer du FMLA-innstillingene og endrer etter behov.</span><span class="sxs-lookup"><span data-stu-id="9c677-114">On the **FMLA** tab, verify the FMLA settings and change as necessary.</span></span>

5. <span data-ttu-id="9c677-115">I kategorien **Ansattselvbetjening** angir du om ledere kan angi permisjons- og fraværsforespørsler på vegne av de ansatte.</span><span class="sxs-lookup"><span data-stu-id="9c677-115">On the **Employee self service** tab, indicate whether managers can enter leave and absence requests on behalf of their employees.</span></span>

6. <span data-ttu-id="9c677-116">I kategorien **Permisjon og fravær** kontrollerer du innstillingene og endrer etter behov.</span><span class="sxs-lookup"><span data-stu-id="9c677-116">On the **Leave and absence** tab, verify the settings and change as necessary.</span></span>

7. <span data-ttu-id="9c677-117">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="9c677-117">Select **Save**.</span></span>

## <a name="configure-calendar-parameters"></a><span data-ttu-id="9c677-118">Konfigurere kalenderparametere</span><span class="sxs-lookup"><span data-stu-id="9c677-118">Configure calendar parameters</span></span>

<span data-ttu-id="9c677-119">Hvis du har aktivert forhåndsversjonsfunksjonen Permisjons- og fraværskalender, må du konfigurere flere parametere.</span><span class="sxs-lookup"><span data-stu-id="9c677-119">If you have enabled the Leave and absence calendar preview feature, you need to configure additional parameters.</span></span> 

[!include [banner](includes/preview-feature-leave-absence.md)]

> [!NOTE]
> <span data-ttu-id="9c677-120">For forhåndsversjonen av 3. februar 2020 er bare **Ventende permisjonsforespørsler** aktivert.</span><span class="sxs-lookup"><span data-stu-id="9c677-120">For the preview release on February 3, 2020, only **Pending leave requests** are enabled.</span></span>

1. <span data-ttu-id="9c677-121">På siden **Permisjon og fravær** velger du **Koblinger**-fanen.</span><span class="sxs-lookup"><span data-stu-id="9c677-121">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="9c677-122">Under **Oppsett** velger du **Personalparametere**.</span><span class="sxs-lookup"><span data-stu-id="9c677-122">Under **Setup**, select **Human resources parameters**.</span></span>

3. <span data-ttu-id="9c677-123">I kategorien **Kalender** endrer du kalenderinnstillinger etter behov.</span><span class="sxs-lookup"><span data-stu-id="9c677-123">On the **Calendar** tab, change calendar settings as necessary.</span></span>

4. <span data-ttu-id="9c677-124">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="9c677-124">Select **Save**.</span></span>

## <a name="see-also"></a><span data-ttu-id="9c677-125">Se også</span><span class="sxs-lookup"><span data-stu-id="9c677-125">See also</span></span>

- [<span data-ttu-id="9c677-126">Oversikt over permisjon og fravær</span><span class="sxs-lookup"><span data-stu-id="9c677-126">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
