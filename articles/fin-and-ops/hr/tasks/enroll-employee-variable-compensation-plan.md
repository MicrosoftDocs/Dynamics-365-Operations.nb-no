--- 
title: Registrere en ansatt i en fast kompensasjonsplan
description: "Kompensasjons- og fordelslederen kan registrere ansatte i variable kompensasjonsplaner for å beregne kontant- og ikke-kontantbonuser for ansatte."
author: kherr75
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: HRMCompVarEnrollEmpl
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: f294d0c802e3f4997baedb15450b85dc25c36732
ms.contentlocale: nb-no
ms.lasthandoff: 09/11/2018

---
# <a name="enroll-an-employee-in-a-variable-compensation-plan"></a><span data-ttu-id="21e15-103">Registrere en ansatt i en fast kompensasjonsplan</span><span class="sxs-lookup"><span data-stu-id="21e15-103">Enroll an employee in a variable compensation plan</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="21e15-104">Kompensasjons- og fordelslederen kan registrere ansatte i variable kompensasjonsplaner for å beregne kontant- og ikke-kontantbonuser for ansatte.</span><span class="sxs-lookup"><span data-stu-id="21e15-104">The Compensation and Benefits manager can enrol employees in variable compensation plans to calculate cash and non-cash awards for employees.</span></span> <span data-ttu-id="21e15-105">Denne fremgangsmåten forutsetter at en variabel kompensasjonsplan er opprettet med Aktiver registrering-feltet satt til Ja, og at det er opprettet rettighetsregler for den variable kompensasjonsplanen.</span><span class="sxs-lookup"><span data-stu-id="21e15-105">This procedure assumes that a variable compensation plan has been created with the Enable enrolment field set to Yes, and that eligibility rules have been created for that variable compensation plan.</span></span> <span data-ttu-id="21e15-106">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="21e15-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="21e15-107">Hvis du vil starte fremgangsmåten, kan du gå til Personale > Arbeidere > Ansatte > Kompensasjon > Registrering av variabel plan</span><span class="sxs-lookup"><span data-stu-id="21e15-107">To begin this procedure, go to Human resources > Workers > Employees > Compensation > Variable plan enrolment</span></span>

1. <span data-ttu-id="21e15-108">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="21e15-108">Click New.</span></span>
2. <span data-ttu-id="21e15-109">Klikk rullegardinknappen i Plan-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="21e15-109">In the Plan field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="21e15-110">Plan-oppslaget filtreres for bare å vise de variable kompensasjonsplanene som den ansatte er kvalifisert for basert på rettighetsreglene.</span><span class="sxs-lookup"><span data-stu-id="21e15-110">The plan lookup will be filtered to only show the variable compensation plans that the employee is eligible for based on the eligibility rules.</span></span>  
3. <span data-ttu-id="21e15-111">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="21e15-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="21e15-112">Aktiver/deaktiver utvidelsen av delen Generelt.</span><span class="sxs-lookup"><span data-stu-id="21e15-112">Toggle the expansion of the General section.</span></span>
5. <span data-ttu-id="21e15-113">Angi en dato i feltet Gyldighetsdato.</span><span class="sxs-lookup"><span data-stu-id="21e15-113">In the Effective date field, enter a date.</span></span>
6. <span data-ttu-id="21e15-114">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="21e15-114">Click Save.</span></span>
7. <span data-ttu-id="21e15-115">Aktiver/deaktiver utvidelsen av delen Overstyringer.</span><span class="sxs-lookup"><span data-stu-id="21e15-115">Toggle the expansion of the Overrides section.</span></span>
    * <span data-ttu-id="21e15-116">Du kan også angi en ansettelsesregeldato til å overstyre ansettelsesdatoen for en ansatt når ansettelsesregelen angitt for den valgte variable planen, er Prosent.</span><span class="sxs-lookup"><span data-stu-id="21e15-116">Optionally, a hire rule date can be set to override the hire date for an employee when the hire rule specified for the selected variable plan is Percent.</span></span>  
    * <span data-ttu-id="21e15-117">Hvis den variable planen er en prosent av grunnplanen, kan belønningsprosenten overstyres for den ansatte.</span><span class="sxs-lookup"><span data-stu-id="21e15-117">If the variable plan is a percent of basis plan, the award percentage can be overridden for the employee.</span></span> <span data-ttu-id="21e15-118">Hvis den variable kompensasjonsplanen er et nummer for enhetsplan, kan antall enheter overstyres for den ansatte.</span><span class="sxs-lookup"><span data-stu-id="21e15-118">If the variable compensation plan is a number of units plan, the number of units can be overridden for the employee.</span></span>  
    * <span data-ttu-id="21e15-119">Hvis den ansatte skal gis et flatt beløp for sin bonus, kan beløpet angis her.</span><span class="sxs-lookup"><span data-stu-id="21e15-119">If the employee should be given a flat amount for their award, the amount can be set here.</span></span>  
8. <span data-ttu-id="21e15-120">Aktiver/deaktiver utvidelsen av delen Organisasjonsmessige overstyringer.</span><span class="sxs-lookup"><span data-stu-id="21e15-120">Toggle the expansion of the Organizational overrides section.</span></span>
    * <span data-ttu-id="21e15-121">Hvis den ansattes ytelse bør ta i betraktning ytelsen til ulike avdelinger eller en annen avdeling enn den som er tilordnet på den ansattes stilling, kan avdelingen overstyres.</span><span class="sxs-lookup"><span data-stu-id="21e15-121">If the employee's performance should take into consideration, the performance of different departments, or a department other than the one assigned on the employee's position, the department can be overridden.</span></span> <span data-ttu-id="21e15-122">Prosent-kolonnen skal være 100 totalt.</span><span class="sxs-lookup"><span data-stu-id="21e15-122">The Percent column should total 100.</span></span>  


