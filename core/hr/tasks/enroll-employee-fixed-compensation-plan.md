--- 
title: Registrere en ansatt i en fast kompensasjonsplan
description: "Kompensasjons- og fordelsansvarlig kan knytte ansatte til faste kompensasjonsplaner for å administrere deres grunnlønn."
author: kherr75
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 88630311a4326508fa69a8938fa216f1a45ba089
ms.contentlocale: nb-no
ms.lasthandoff: 08/29/2017

---
# <a name="enroll-an-employee-in-a-fixed-compensation-plan"></a><span data-ttu-id="25a63-103">Registrere en ansatt i en fast kompensasjonsplan</span><span class="sxs-lookup"><span data-stu-id="25a63-103">Enroll an employee in a fixed compensation plan</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="25a63-104">Kompensasjons- og fordelsansvarlig kan knytte ansatte til faste kompensasjonsplaner for å administrere deres grunnlønn.</span><span class="sxs-lookup"><span data-stu-id="25a63-104">The compensation and benefits manager can assign employees to fixed compensation plans to manage their base pay.</span></span> <span data-ttu-id="25a63-105">Denne fremgangsmåten forutsetter at en fast plan er opprettet og er aktiv, og at det er angitt rettighetsregler for planen.</span><span class="sxs-lookup"><span data-stu-id="25a63-105">This procedure assumes that a fixed plan has been created and is active, and that eligibility rules have been set for the plan.</span></span> <span data-ttu-id="25a63-106">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="25a63-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="25a63-107">Hvis du vil starte fremgangsmåten, kan du gå til Personale > Arbeidere > Ansatte > Kompensasjon > Fast plan</span><span class="sxs-lookup"><span data-stu-id="25a63-107">To begin the procedure, go to Human resources > Workers > Employees > Compensation > Fixed plan</span></span>

1. <span data-ttu-id="25a63-108">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="25a63-108">Click New.</span></span>
2. <span data-ttu-id="25a63-109">I Handling-feltet velger du en fast kompensasjonshandling av typen Ansette/ansette på nytt for å beskrive endringen i den ansattes kompensasjon.</span><span class="sxs-lookup"><span data-stu-id="25a63-109">In the Action field, select a Fixed compensation action of type Hire/Rehire to describe the change in the employee's compensation.</span></span>
3. <span data-ttu-id="25a63-110">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="25a63-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="25a63-111">Klikk rullegardinknappen i Stilling-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="25a63-111">In the Position field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="25a63-112">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="25a63-112">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="25a63-113">Nivået som vises er fra kompensasjonsnivået for jobben på stillingen.</span><span class="sxs-lookup"><span data-stu-id="25a63-113">The level that's displayed is from the Compensation Level of the Job on the Position.</span></span> <span data-ttu-id="25a63-114">Nivået må angis for jobben før kompensasjon kan tilordnes til ansatt.</span><span class="sxs-lookup"><span data-stu-id="25a63-114">The level must be set on the Job before compensation can be assigned to the employee.</span></span>  
6. <span data-ttu-id="25a63-115">I Plan-feltet velger du den faste kompensasjonsplanen for den ansatte.</span><span class="sxs-lookup"><span data-stu-id="25a63-115">In the Plan field, select the fixed compensation plan for the employee.</span></span> <span data-ttu-id="25a63-116">Plan-oppslaget er filtrert for bare å vise planene som den ansatte er kvalifisert for basert på rettighetsreglene.</span><span class="sxs-lookup"><span data-stu-id="25a63-116">The Plan lookup is filtered to show only the plans that the employee is eligible for based on the Eligibility rules.</span></span>
7. <span data-ttu-id="25a63-117">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="25a63-117">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="25a63-118">De effektive datoene og utløpsdatoene for kompensasjon hentes fra start- og sluttdatoene for arbeiderens stillingstilordning.</span><span class="sxs-lookup"><span data-stu-id="25a63-118">The Effective and Expiration dates for the compensation default from the start and end dates for the worker's position assignment.</span></span> <span data-ttu-id="25a63-119">Du kan endre disse datoene etter behov.</span><span class="sxs-lookup"><span data-stu-id="25a63-119">You can adjust these dates as needed.</span></span>  
    * <span data-ttu-id="25a63-120">Hvis den faste kompensasjonsplanen er en trinnplan, velger du trinnet som inneholder den riktige lønnssatsen for den ansatte.</span><span class="sxs-lookup"><span data-stu-id="25a63-120">If the Fixed compensation plan is a step plan, select the step containing the correct pay rate for the employee.</span></span> <span data-ttu-id="25a63-121">Hvis den faste kompensasjonsplanen er en klasse- eller segmentplan, angir du lønnssatsen for den ansatte.</span><span class="sxs-lookup"><span data-stu-id="25a63-121">If the fixed compensation plan is a grade or a band plan, enter the pay rate for the employee.</span></span> <span data-ttu-id="25a63-122">Lønnssatsen blir validert mot toleranseinnstillinger for planen, og minimum og maksimum referansepunkt for jobbens kompensasjonsnivå.</span><span class="sxs-lookup"><span data-stu-id="25a63-122">The pay rate will be validated against the tolerance settings for the plan, and the minimum and maximum reference points for the job's compensation level.</span></span>  
8. <span data-ttu-id="25a63-123">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="25a63-123">Click OK.</span></span>


