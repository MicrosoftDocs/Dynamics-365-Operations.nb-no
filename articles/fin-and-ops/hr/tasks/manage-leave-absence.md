---
title: Administrere permisjon
description: Dette hjelper med opprettelsen av permisjonsposter for ansatt.
author: ShielaSogge
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmWorker, HcmEmploymentLeave
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7687d31fbf73a02b1b924d092e77ac28b573e694
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "337975"
---
# <a name="manage-leave-of-absence"></a><span data-ttu-id="b30f2-103">Administrere permisjon</span><span class="sxs-lookup"><span data-stu-id="b30f2-103">Manage leave of absence</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b30f2-104">Dette hjelper med opprettelsen av permisjonsposter for ansatt.</span><span class="sxs-lookup"><span data-stu-id="b30f2-104">This procedure walks through the creation of employee leave records.</span></span> <span data-ttu-id="b30f2-105">Du kan spore permisjonstid for årsaker som omfatter medisinske aktiviteter, utdanningsaktiviteter eller foreldreaktiviteter.</span><span class="sxs-lookup"><span data-stu-id="b30f2-105">You can track leave time for reasons that include medical, educational, or parental activities.</span></span> <span data-ttu-id="b30f2-106">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="b30f2-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="b30f2-107">Gå til Personale > Arbeidere > Ansatte.</span><span class="sxs-lookup"><span data-stu-id="b30f2-107">Go to Human resources > Workers > Employees.</span></span>
2. <span data-ttu-id="b30f2-108">Velg en ansatt i listen.</span><span class="sxs-lookup"><span data-stu-id="b30f2-108">In the list, select an employee.</span></span>
3. <span data-ttu-id="b30f2-109">Vis detaljert informasjon for den valgte ansatte ved å velge den ansattes navn.</span><span class="sxs-lookup"><span data-stu-id="b30f2-109">Display detailed information for the selected employee by selecting the employee's name.</span></span>
4. <span data-ttu-id="b30f2-110">Klikk kategorien Ansettelse.</span><span class="sxs-lookup"><span data-stu-id="b30f2-110">Click the Employment tab.</span></span>
5. <span data-ttu-id="b30f2-111">Klikk Ferie.</span><span class="sxs-lookup"><span data-stu-id="b30f2-111">Click Leave.</span></span>
6. <span data-ttu-id="b30f2-112">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="b30f2-112">Click New.</span></span>
7. <span data-ttu-id="b30f2-113">Klikk rullegardinknappen i Permisonstype-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="b30f2-113">In the Leave type field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="b30f2-114">Du kan knytte en permisjonstype til en inntektskode i Permisjonstype-skjemaet.</span><span class="sxs-lookup"><span data-stu-id="b30f2-114">You can associate a leave type to an earning code in the Leave types form.</span></span> <span data-ttu-id="b30f2-115">Hvis en permisjonstype er knyttet til en inntektskode, genereres en inntektslinje med den tilknyttede inntektskoden i permisjonsperioden som du angir.</span><span class="sxs-lookup"><span data-stu-id="b30f2-115">If a leave type is associated with an earning code, an earning line will be generated with the associated earning code during the leave period that you enter.</span></span>  
8. <span data-ttu-id="b30f2-116">Velg en permisjonstype fra listen.</span><span class="sxs-lookup"><span data-stu-id="b30f2-116">In the list, select a leave type.</span></span> 
    * <span data-ttu-id="b30f2-117">For eksempel: adopsjon</span><span class="sxs-lookup"><span data-stu-id="b30f2-117">For example: Adoption</span></span>  
9. <span data-ttu-id="b30f2-118">Angi datoen som permisjonen skal starte på.</span><span class="sxs-lookup"><span data-stu-id="b30f2-118">Enter the date that the leave will start.</span></span> <span data-ttu-id="b30f2-119">Eksempel: '2015-10-26'</span><span class="sxs-lookup"><span data-stu-id="b30f2-119">Example: '2015-10-26'</span></span>
    * <span data-ttu-id="b30f2-120">For eksempel: 2015-10-26</span><span class="sxs-lookup"><span data-stu-id="b30f2-120">For example:  2015-10-26</span></span>  
10. <span data-ttu-id="b30f2-121">Angi datoen som permisjonen skal starte på.</span><span class="sxs-lookup"><span data-stu-id="b30f2-121">Enter the date that the leave will start.</span></span> 
    * <span data-ttu-id="b30f2-122">For eksempel: 2015-11-20</span><span class="sxs-lookup"><span data-stu-id="b30f2-122">For example:  2015-11-20</span></span>  
11. <span data-ttu-id="b30f2-123">Angi en beskrivelse i merknadsfeltet.</span><span class="sxs-lookup"><span data-stu-id="b30f2-123">In the note field, enter a description.</span></span>
    * <span data-ttu-id="b30f2-124">For eksempel: permisjon ved adopsjon</span><span class="sxs-lookup"><span data-stu-id="b30f2-124">For example: Leave for adoption</span></span>  
12. <span data-ttu-id="b30f2-125">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="b30f2-125">Click Save.</span></span>

