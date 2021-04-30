---
title: Leiekonvensjoner for aktiva
description: Dette emnet beskriver konvensjoner for leide aktiva.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLease
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2021-1-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 67c4d2b7162cf6bda2eedfecef43ff0b216e6e6c
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881814"
---
# <a name="asset-leasing-conventions"></a><span data-ttu-id="a4bfa-103">Leiekonvensjoner for aktiva</span><span class="sxs-lookup"><span data-stu-id="a4bfa-103">Asset leasing conventions</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="a4bfa-104">Dette emnet beskriver konvensjoner for leide aktiva.</span><span class="sxs-lookup"><span data-stu-id="a4bfa-104">This topic describes conventions for leased assets.</span></span> <span data-ttu-id="a4bfa-105">Leiekonvensjoner brukes til å bestemme startdatoen for et leietablå.</span><span class="sxs-lookup"><span data-stu-id="a4bfa-105">Leasing conventions are used to determine the commencement date of a lease book.</span></span> <span data-ttu-id="a4bfa-106">Hvis leiekonvensjonen er satt til **Ingen**, er startdatoen den samme som startdatoen for leien (det vil si verdien for **Startdato for leie**).</span><span class="sxs-lookup"><span data-stu-id="a4bfa-106">If the leasing convention is set to **None**, the commencement date is the same as the start date for the lease (that is, the value of the **Lease start date** field).</span></span> <span data-ttu-id="a4bfa-107">Hvis leiekonvensjonen er satt til **Hele måneden**, er startdatoen den første dagen i måneden som startdatoen for leieavtalen faller på.</span><span class="sxs-lookup"><span data-stu-id="a4bfa-107">If the leasing convention is set to **Full month**, the commencement date is the first day of the month that the lease's start date falls in.</span></span>

<span data-ttu-id="a4bfa-108">Startdatoen fastsetter startdatoen for perioden for planene for nedbetaling av gjeld og avskrivning av aktiva.</span><span class="sxs-lookup"><span data-stu-id="a4bfa-108">The commencement date determines the start date of the period for the liability amortization and asset depreciation schedules.</span></span> <span data-ttu-id="a4bfa-109">Rente- og avskrivningsutgifter posteres på sluttdatoen for perioden i de gjeldende planene.</span><span class="sxs-lookup"><span data-stu-id="a4bfa-109">Interest expenses and depreciation expenses are posted on the period end date of the corresponding schedules.</span></span> <span data-ttu-id="a4bfa-110">Den første journaloppføringen for opprinnelig føring og justering posteres på startdatoen.</span><span class="sxs-lookup"><span data-stu-id="a4bfa-110">The initial recognition and adjustment journal entry are posted on the commencement date.</span></span>

> [!NOTE]
> <span data-ttu-id="a4bfa-111">Funksjonen for leiekonvensjoner må aktiveres ved hjelp av Funksjonsbehandling.</span><span class="sxs-lookup"><span data-stu-id="a4bfa-111">The feature for leasing conventions must be turned on through Feature Management.</span></span> <span data-ttu-id="a4bfa-112">I arbeidsområdet for **Funksjonsbehandling** finner og velger du funksjonen for **Leiekonvensjon for aktivaleie**, og deretter velger du **Aktiver nå**.</span><span class="sxs-lookup"><span data-stu-id="a4bfa-112">In the **Feature management** workspace, find and select the feature that is named **Leasing convention for asset leasing** feature, and then select **Enable now**.</span></span>

<span data-ttu-id="a4bfa-113">Leiekonvensjoner tilordnes til oppsettet for et leieaktivatablå.</span><span class="sxs-lookup"><span data-stu-id="a4bfa-113">Leasing conventions are assigned to the setup for a lease asset book.</span></span>

<span data-ttu-id="a4bfa-114">Følg denne fremgangsmåten for å vise eller tilordne leiekonvensjonen.</span><span class="sxs-lookup"><span data-stu-id="a4bfa-114">To view or assign the leasing convention, follow these steps.</span></span>

1. <span data-ttu-id="a4bfa-115">Gå til **Aktivaleie \> Oppsett \> Leietablåer**.</span><span class="sxs-lookup"><span data-stu-id="a4bfa-115">Go to **Asset leasing \> Setup \> Lease books**.</span></span>
2. <span data-ttu-id="a4bfa-116">I feltet **Leiekonvensjon** velger du en av følgende verdier.</span><span class="sxs-lookup"><span data-stu-id="a4bfa-116">In the **Leasing convention** field, select one of the following values.</span></span>

    | <span data-ttu-id="a4bfa-117">Leiekonvensjon</span><span class="sxs-lookup"><span data-stu-id="a4bfa-117">Leasing convention</span></span> | <span data-ttu-id="a4bfa-118">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="a4bfa-118">Description</span></span> |
    |--------------------|-------------|
    | <span data-ttu-id="a4bfa-119">None</span><span class="sxs-lookup"><span data-stu-id="a4bfa-119">None</span></span>               | <span data-ttu-id="a4bfa-120">Planene for nedbetaling av gjeld og avskrivning av aktiva starter på startdatoen for leieavtalen, fordi startdatoen er lik startdatoen for leieavtalen.</span><span class="sxs-lookup"><span data-stu-id="a4bfa-120">The liability amortization and asset depreciation schedules start on the lease's start date, because the commencement date equals the lease's start date.</span></span> <span data-ttu-id="a4bfa-121">Sluttdatoen er én måned senere.</span><span class="sxs-lookup"><span data-stu-id="a4bfa-121">The end date is one month later.</span></span> <span data-ttu-id="a4bfa-122">Denne leiekonvensjonen gir ingen garanti for at renten posteres på den siste dagen i hver måned.</span><span class="sxs-lookup"><span data-stu-id="a4bfa-122">This leasing convention doesn't guarantee that the interest will be posted on the last day of each month.</span></span> |
    | <span data-ttu-id="a4bfa-123">Hele måneden</span><span class="sxs-lookup"><span data-stu-id="a4bfa-123">Full month</span></span>         | <span data-ttu-id="a4bfa-124">For leieavtaler med startdato når som helst i løpet av måneden, begynner planene for nedbetaling av gjeld og avskrivning av aktiva å avsette utgifter på den første dagen i denne måneden.</span><span class="sxs-lookup"><span data-stu-id="a4bfa-124">For leases that have a start date that occurs at any time during the month, the liability amortization and asset depreciation schedules start to accrue expenses on the first day of that month.</span></span> <span data-ttu-id="a4bfa-125">Denne leiekonvensjonen sikrer at det avsettes rente på den siste dagen i hver måned for hele måneden.</span><span class="sxs-lookup"><span data-stu-id="a4bfa-125">This leasing convention ensures that interest is accrued on the last day of each month for the whole month.</span></span> |

3. <span data-ttu-id="a4bfa-126">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="a4bfa-126">Select **Save**.</span></span>

<span data-ttu-id="a4bfa-127">Når det opprettes en leieavtale, angis startdatoen for hvert tablå automatisk basert på startdatoen som er angitt for leieavtalen og leiekonvensjonen som er angitt for tablået.</span><span class="sxs-lookup"><span data-stu-id="a4bfa-127">When a lease is created, the commencement date of each book is automatically entered based on the start date that is entered for the lease and the leasing convention that is specified for the book.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
