---
title: Definere indeksrenter
description: Dette emnet forklarer hvordan du konfigurerer indeksrenter. Indeksrenter kreves hvis organisasjonen knytter leierbetalingsbeløp med et sett med indeksrenter.
author: moaamer
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 6424248e8d01d04720ad65e80aaa543b42abccc6
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5823029"
---
# <a name="set-up-index-rates"></a><span data-ttu-id="5d619-104">Definere indeksrenter</span><span class="sxs-lookup"><span data-stu-id="5d619-104">Set up index rates</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5d619-105">Hvis leiebetalinger er avhengige av en indeks, kan indeksrentetypene legges til og vedlikeholdes i systemet.</span><span class="sxs-lookup"><span data-stu-id="5d619-105">If lease payments depend on an index, the index rate types can be added and maintained in the system.</span></span> <span data-ttu-id="5d619-106">Når du skal revaluere leiebetalinger fra siden **Indeksrentetype**, bruker revalueringsprosessen for indeksrente den nyligste indeksrenten fra datoen for revalueringen.</span><span class="sxs-lookup"><span data-stu-id="5d619-106">To revalue the lease payments from the **Index rate type** page, the index rate revaluation process uses the most recent index rate from the date of revaluation.</span></span>

<span data-ttu-id="5d619-107">Følg denne fremgangsmåten for å legge til indeksrentetyper og indeksrenter.</span><span class="sxs-lookup"><span data-stu-id="5d619-107">To add index rate types and index rates, follow these steps.</span></span>

1. <span data-ttu-id="5d619-108">Gå til **Aktivaleie \> Oppsett \> Indeksrentetype**.</span><span class="sxs-lookup"><span data-stu-id="5d619-108">Go to **Asset leasing \> Setup \> Index rate type**.</span></span>
2. <span data-ttu-id="5d619-109">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="5d619-109">Select **New**.</span></span>
3. <span data-ttu-id="5d619-110">I de aktuelle feltene angir du rentetypen og navnet på indeksrenten.</span><span class="sxs-lookup"><span data-stu-id="5d619-110">In the appropriate fields, enter the rate type and the name of the index rate.</span></span>
4. <span data-ttu-id="5d619-111">Hvis du vil legge til en ny verdi for en indeksrenteverdi, velger du indeksrentetypen, og deretter velger du **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="5d619-111">To add a new index rate value, select the index rate type, and then select **Add**.</span></span>
5. <span data-ttu-id="5d619-112">Velg den gjeldende startdatoen for renten, og velg renteverdien.</span><span class="sxs-lookup"><span data-stu-id="5d619-112">Select the effective start date of the rate, and select the rate value.</span></span>

<span data-ttu-id="5d619-113">Du må velge enten **verdidifferanse for indeksrente** eller **indeksrenteverdi** som indeksrentemetode.</span><span class="sxs-lookup"><span data-stu-id="5d619-113">You must select either **Index rate value difference** or **Index rate value** as the index rate method.</span></span>

- <span data-ttu-id="5d619-114">Velg metoden for **verdidifferanse for indeksrente** for å beregne en ny leiebetaling basert på forskjellen mellom indeksrenten på startdatoen og den seneste indeksrenten.</span><span class="sxs-lookup"><span data-stu-id="5d619-114">Select the **Index rate value difference** method to calculate a new lease payment, based on the difference between the index rate on the start date and the most recent index rate.</span></span> <span data-ttu-id="5d619-115">Indeksrenten er definert i feltet for **indeksrente (%)**.</span><span class="sxs-lookup"><span data-stu-id="5d619-115">The index rate is defined in the **Index rate (%)** field.</span></span>
- <span data-ttu-id="5d619-116">Velg metoden for **indeksrenteverdi** for å beregne leiebetalingen ved å bruke prosenten som er angitt i feltet for **indeksrente (%)**.</span><span class="sxs-lookup"><span data-stu-id="5d619-116">Select the **Index rate value** method to calculate the lease payment by using the percentage that is specified in the **Index rate (%)** field.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]