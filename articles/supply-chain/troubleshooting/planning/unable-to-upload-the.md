---
title: Du kan ikke oppdatere anslått enhetskostnad når du importerer behovsprognoseposter
description: Når du bruker dataenheter til å importere behovsprognoseposter, oppdateres ikke kostprisen for eksisterende poster slik at den samsvarer med de importerte dataene.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: DataManagementWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: angarmas
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: c8ea8322a6c7bafe2dfcaaee3e9989f753c85e2a
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026783"
---
# <a name="you-cant-update-the-forecasted-unit-cost-when-you-import-demand-forecast-records"></a><span data-ttu-id="67f5c-103">Du kan ikke oppdatere anslått enhetskostnad når du importerer behovsprognoseposter</span><span class="sxs-lookup"><span data-stu-id="67f5c-103">You can't update the forecasted unit cost when you import demand forecast records</span></span>

<span data-ttu-id="67f5c-104">KB-nummer: 4614109</span><span class="sxs-lookup"><span data-stu-id="67f5c-104">KB number: 4614109</span></span>

## <a name="symptoms"></a><span data-ttu-id="67f5c-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="67f5c-105">Symptoms</span></span>

<span data-ttu-id="67f5c-106">Når du bruker dataenheter til å importere behovsprognoseposter, oppdateres ikke verdien for **anslått enhetskostnad** for eksisterende poster slik at den samsvarer med de importerte dataene.</span><span class="sxs-lookup"><span data-stu-id="67f5c-106">When you use data entities to import demand forecast records, the **Forecasted unit cost** value for existing records isn't updated so that it matches the imported data.</span></span>

## <a name="cause"></a><span data-ttu-id="67f5c-107">Årsak</span><span class="sxs-lookup"><span data-stu-id="67f5c-107">Cause</span></span>

<span data-ttu-id="67f5c-108">**Anslått enhetskostnad** er et skrivebeskyttet felt.</span><span class="sxs-lookup"><span data-stu-id="67f5c-108">**Forecasted unit cost** is a read-only field.</span></span> <span data-ttu-id="67f5c-109">Verdien er basert på produktenhetskostnaden og kan ikke angis direkte ved import.</span><span class="sxs-lookup"><span data-stu-id="67f5c-109">The value is based on the product unit cost and can't be set directly through import.</span></span>

## <a name="resolution"></a><span data-ttu-id="67f5c-110">Oppløsning</span><span class="sxs-lookup"><span data-stu-id="67f5c-110">Resolution</span></span>

<span data-ttu-id="67f5c-111">Fordi feltet er skrivebeskyttet, kan du ikke importere verdier for det.</span><span class="sxs-lookup"><span data-stu-id="67f5c-111">Because the field is read only, you can't import values for it.</span></span> <span data-ttu-id="67f5c-112">Verdien blir beregnet i henhold til den eksisterende forretningslogikken.</span><span class="sxs-lookup"><span data-stu-id="67f5c-112">The value will be calculated according to the existing business logic.</span></span>
