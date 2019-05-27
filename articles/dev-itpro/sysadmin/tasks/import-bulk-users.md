---
title: Masseimportere brukere
description: Denne fremgangsmåten kan brukes av systemansvarlige til å importere et stort antall brukere fra Azure Active Directory.
author: maertenm
manager: AnnBe
ms.date: 07/07/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 339cc1d3bcdc1dc93b796c385d2165f45f8f7ecf
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1548100"
---
# <a name="import-users-in-bulk"></a><span data-ttu-id="c0f0e-103">Masseimportere brukere</span><span class="sxs-lookup"><span data-stu-id="c0f0e-103">Import users in bulk</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c0f0e-104">Denne fremgangsmåten kan brukes av systemansvarlige til å importere et stort antall brukere fra Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c0f0e-104">This procedure can be used by system administrators to import a large number of users from Azure Active Directory.</span></span>


## <a name="run-as-a-batch-job"></a><span data-ttu-id="c0f0e-105">Kjør som satsvis jobb</span><span class="sxs-lookup"><span data-stu-id="c0f0e-105">Run as a batch job</span></span>
1. <span data-ttu-id="c0f0e-106">Gå til Systemadministrasjon > Brukere > Brukere.</span><span class="sxs-lookup"><span data-stu-id="c0f0e-106">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="c0f0e-107">Klikk Satsvis import.</span><span class="sxs-lookup"><span data-stu-id="c0f0e-107">Click Batch import.</span></span>
3. <span data-ttu-id="c0f0e-108">Utvid Kjør i bakgrunnen.</span><span class="sxs-lookup"><span data-stu-id="c0f0e-108">Expand the Run in the background section.</span></span>
4. <span data-ttu-id="c0f0e-109">Velg Ja i feltet Satsvis behandling.</span><span class="sxs-lookup"><span data-stu-id="c0f0e-109">Select Yes in the Batch processing field.</span></span>
5. <span data-ttu-id="c0f0e-110">Skriv inn en verdi i Oppgavebeskrivelse-feltet.</span><span class="sxs-lookup"><span data-stu-id="c0f0e-110">In the Task description field, type a value.</span></span>
6. <span data-ttu-id="c0f0e-111">Angi eller velg en verdi i Parti-feltet.</span><span class="sxs-lookup"><span data-stu-id="c0f0e-111">In the Batch group field, enter or select a value.</span></span>
    * <span data-ttu-id="c0f0e-112">Dette er et valgfritt trinn.</span><span class="sxs-lookup"><span data-stu-id="c0f0e-112">This is an optional step.</span></span>  
7. <span data-ttu-id="c0f0e-113">Velg Ja i feltet Privat.</span><span class="sxs-lookup"><span data-stu-id="c0f0e-113">Select Yes in the Private field.</span></span>
    * <span data-ttu-id="c0f0e-114">Dette er et valgfritt trinn.</span><span class="sxs-lookup"><span data-stu-id="c0f0e-114">This is an optional step.</span></span>  
8. <span data-ttu-id="c0f0e-115">Velg Ja i feltet Kritisk jobb.</span><span class="sxs-lookup"><span data-stu-id="c0f0e-115">Select Yes in the Critical Job field.</span></span>
    * <span data-ttu-id="c0f0e-116">Dette er et valgfritt trinn.</span><span class="sxs-lookup"><span data-stu-id="c0f0e-116">This is an optional step.</span></span>  
9. <span data-ttu-id="c0f0e-117">Velg et alternativ i Overvåkingskategori-feltet.</span><span class="sxs-lookup"><span data-stu-id="c0f0e-117">In the Monitoring category field, select an option.</span></span>
10. <span data-ttu-id="c0f0e-118">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="c0f0e-118">Click OK.</span></span>

## <a name="run-in-a-sandbox-environment"></a><span data-ttu-id="c0f0e-119">Kjøre i et sandkassemiljø</span><span class="sxs-lookup"><span data-stu-id="c0f0e-119">Run in a sandbox environment</span></span>
1. <span data-ttu-id="c0f0e-120">Klikk Satsvis import.</span><span class="sxs-lookup"><span data-stu-id="c0f0e-120">Click Batch import.</span></span>
2. <span data-ttu-id="c0f0e-121">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="c0f0e-121">Click OK.</span></span>

