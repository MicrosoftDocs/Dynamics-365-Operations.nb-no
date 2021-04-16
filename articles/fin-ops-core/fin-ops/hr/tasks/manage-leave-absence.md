---
title: Administrere permisjon
description: Dette hjelper med opprettelsen av permisjonsposter for ansatt.
author: andreabichsel
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: HcmWorker, HcmEmploymentLeave
audience: Application User
ms.reviewer: anbichse
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5bb65e7cd77450751718aaa0b6179ba7386de8ab
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751868"
---
# <a name="manage-leave-of-absence"></a><span data-ttu-id="a5c78-103">Administrere permisjon</span><span class="sxs-lookup"><span data-stu-id="a5c78-103">Manage leave of absence</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a5c78-104">Dette hjelper med opprettelsen av permisjonsposter for ansatt.</span><span class="sxs-lookup"><span data-stu-id="a5c78-104">This procedure walks through the creation of employee leave records.</span></span> <span data-ttu-id="a5c78-105">Du kan spore permisjonstid for årsaker som omfatter medisinske aktiviteter, utdanningsaktiviteter eller foreldreaktiviteter.</span><span class="sxs-lookup"><span data-stu-id="a5c78-105">You can track leave time for reasons that include medical, educational, or parental activities.</span></span> <span data-ttu-id="a5c78-106">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="a5c78-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="a5c78-107">Gå til Personale > Arbeidere > Ansatte.</span><span class="sxs-lookup"><span data-stu-id="a5c78-107">Go to Human resources > Workers > Employees.</span></span>
2. <span data-ttu-id="a5c78-108">Velg en ansatt i listen.</span><span class="sxs-lookup"><span data-stu-id="a5c78-108">In the list, select an employee.</span></span>
3. <span data-ttu-id="a5c78-109">Vis detaljert informasjon for den valgte ansatte ved å velge den ansattes navn.</span><span class="sxs-lookup"><span data-stu-id="a5c78-109">Display detailed information for the selected employee by selecting the employee's name.</span></span>
4. <span data-ttu-id="a5c78-110">Klikk på fanen Ansettelse.</span><span class="sxs-lookup"><span data-stu-id="a5c78-110">Click the Employment tab.</span></span>
5. <span data-ttu-id="a5c78-111">Klikk på Ferie.</span><span class="sxs-lookup"><span data-stu-id="a5c78-111">Click Leave.</span></span>
6. <span data-ttu-id="a5c78-112">Klikk på Ny.</span><span class="sxs-lookup"><span data-stu-id="a5c78-112">Click New.</span></span>
7. <span data-ttu-id="a5c78-113">Klikk på rullegardinknappen i Permisonstype-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="a5c78-113">In the Leave type field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="a5c78-114">Du kan knytte en permisjonstype til en inntektskode i Permisjonstype-skjemaet.</span><span class="sxs-lookup"><span data-stu-id="a5c78-114">You can associate a leave type to an earning code in the Leave types form.</span></span> <span data-ttu-id="a5c78-115">Hvis en permisjonstype er knyttet til en inntektskode, genereres en inntektslinje med den tilknyttede inntektskoden i permisjonsperioden som du angir.</span><span class="sxs-lookup"><span data-stu-id="a5c78-115">If a leave type is associated with an earning code, an earning line will be generated with the associated earning code during the leave period that you enter.</span></span>  
8. <span data-ttu-id="a5c78-116">Velg en permisjonstype fra listen.</span><span class="sxs-lookup"><span data-stu-id="a5c78-116">In the list, select a leave type.</span></span> 
    * <span data-ttu-id="a5c78-117">For eksempel: adopsjon</span><span class="sxs-lookup"><span data-stu-id="a5c78-117">For example: Adoption</span></span>  
9. <span data-ttu-id="a5c78-118">Angi datoen som permisjonen skal starte på.</span><span class="sxs-lookup"><span data-stu-id="a5c78-118">Enter the date that the leave will start.</span></span> <span data-ttu-id="a5c78-119">Eksempel: '2015-10-26'</span><span class="sxs-lookup"><span data-stu-id="a5c78-119">Example: '2015-10-26'</span></span>
    * <span data-ttu-id="a5c78-120">For eksempel: 2015-10-26</span><span class="sxs-lookup"><span data-stu-id="a5c78-120">For example:  2015-10-26</span></span>  
10. <span data-ttu-id="a5c78-121">Angi datoen som permisjonen skal starte på.</span><span class="sxs-lookup"><span data-stu-id="a5c78-121">Enter the date that the leave will start.</span></span> 
    * <span data-ttu-id="a5c78-122">For eksempel: 2015-11-20</span><span class="sxs-lookup"><span data-stu-id="a5c78-122">For example:  2015-11-20</span></span>  
11. <span data-ttu-id="a5c78-123">Angi en beskrivelse i merknadsfeltet.</span><span class="sxs-lookup"><span data-stu-id="a5c78-123">In the note field, enter a description.</span></span>
    * <span data-ttu-id="a5c78-124">For eksempel: permisjon ved adopsjon</span><span class="sxs-lookup"><span data-stu-id="a5c78-124">For example: Leave for adoption</span></span>  
12. <span data-ttu-id="a5c78-125">Klikk på Lagre.</span><span class="sxs-lookup"><span data-stu-id="a5c78-125">Click Save.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]