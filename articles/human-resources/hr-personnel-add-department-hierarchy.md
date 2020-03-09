---
title: Opprette avdelinger og inkludere dem i avdelingshierarkiet
description: En avdeling er en driftsenhet som representerer en kategori eller et funksjonsområde i en organisasjon. En avdeling er ansvarlig for et bestemt område i organisasjonen, for eksempel salg, regnskap eller Personale. Du kan bruke avdelinger til å rapportere om funksjonsområder. Avdelinger kan ha ansvar for fortjeneste og tap.
author: andreabichsel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HierarchyDesigner, OMOperatingUnit
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.custom: 63213
ms.assetid: 5dbc62fc-0184-4c0e-9856-e735fc68799e
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 99ecdb936071c2c71dbfae1277d20aa6dc9ef0ca
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010108"
---
# <a name="create-departments-and-include-them-in-the-department-hierarchy"></a><span data-ttu-id="8d732-106">Opprette avdelinger og inkludere dem i avdelingshierarkiet</span><span class="sxs-lookup"><span data-stu-id="8d732-106">Create departments and include them in the department hierarchy</span></span>

<span data-ttu-id="8d732-107">En avdeling er en driftsenhet som representerer en kategori eller et funksjonsområde i en organisasjon.</span><span class="sxs-lookup"><span data-stu-id="8d732-107">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="8d732-108">En avdeling er ansvarlig for et bestemt område i organisasjonen, for eksempel salg, regnskap eller Personale.</span><span class="sxs-lookup"><span data-stu-id="8d732-108">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="8d732-109">Du kan bruke avdelinger til å rapportere om funksjonsområder.</span><span class="sxs-lookup"><span data-stu-id="8d732-109">You can use departments to report on functional areas.</span></span> <span data-ttu-id="8d732-110">Avdelinger kan ha ansvar for fortjeneste og tap.</span><span class="sxs-lookup"><span data-stu-id="8d732-110">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="8d732-111">En avdeling kan inneholde en gruppe med kostsentre.</span><span class="sxs-lookup"><span data-stu-id="8d732-111">A department might include a group of cost centers.</span></span> <span data-ttu-id="8d732-112">Stillinger kan tilordnes til avdelinger.</span><span class="sxs-lookup"><span data-stu-id="8d732-112">Positions can be assigned to departments.</span></span> <span data-ttu-id="8d732-113">Hvis du vil opprette en avdeling, klikker du **Personale** &gt; **Avdelinger** &gt; **Avdeling**.</span><span class="sxs-lookup"><span data-stu-id="8d732-113">To create a department, click **Human Resources** &gt; **Departments** &gt; **Department**.</span></span> <span data-ttu-id="8d732-114">Følgende tabell beskriver feltene som er tilgjengelige.</span><span class="sxs-lookup"><span data-stu-id="8d732-114">The following table describes the fields that are available.</span></span>

| <span data-ttu-id="8d732-115">Felt</span><span class="sxs-lookup"><span data-stu-id="8d732-115">Field</span></span>               | <span data-ttu-id="8d732-116">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="8d732-116">Description</span></span>                                                                                                                                                                                                       |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d732-117">Navn</span><span class="sxs-lookup"><span data-stu-id="8d732-117">Name</span></span>                | <span data-ttu-id="8d732-118">Skriv inn et navn for avdelingen.</span><span class="sxs-lookup"><span data-stu-id="8d732-118">Enter a name for the department.</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="8d732-119">Avdelingsnummer</span><span class="sxs-lookup"><span data-stu-id="8d732-119">Department number</span></span>   | <span data-ttu-id="8d732-120">Det kan hende at en standardverdi genereres automatisk hvis en nummerseriekode er tilordnet til **Organisasjonsnummer**-referansen på siden **Nummerserier**.</span><span class="sxs-lookup"><span data-stu-id="8d732-120">A default value might be generated automatically if a number sequence code is assigned to the **Organization number** reference on the **Number sequences** page.</span></span>                                                 |
| <span data-ttu-id="8d732-121">Søkenavn</span><span class="sxs-lookup"><span data-stu-id="8d732-121">Search name</span></span>         | <span data-ttu-id="8d732-122">Angi et navn eller akronym som kan brukes til å søke etter avdelingen.</span><span class="sxs-lookup"><span data-stu-id="8d732-122">Enter a name or acronym that can be used to search for the department.</span></span>                                                                                                                                            |
| <span data-ttu-id="8d732-123">Notat</span><span class="sxs-lookup"><span data-stu-id="8d732-123">Memo</span></span>                | <span data-ttu-id="8d732-124">Angi eventuell tilleggsinformasjon her.</span><span class="sxs-lookup"><span data-stu-id="8d732-124">Enter any additional information here.</span></span>                                                                                                                                                                            |
| <span data-ttu-id="8d732-125">I hierarki</span><span class="sxs-lookup"><span data-stu-id="8d732-125">In hierarchy</span></span>        | <span data-ttu-id="8d732-126">En merket boks indikerer at avdelingen er inkludert i avdelingshierarkiet.</span><span class="sxs-lookup"><span data-stu-id="8d732-126">A selected check box indicates that the department is included in the department hierarchy.</span></span> <span data-ttu-id="8d732-127">Hvis du vil ha informasjon om hvordan du legger til en avdeling i avdeling-hierarkiet, kan du se informasjonen senere i denne artikkelen.</span><span class="sxs-lookup"><span data-stu-id="8d732-127">For information about how to add a department to the department hierarchy, see the information later in this article.</span></span> |
| <span data-ttu-id="8d732-128">DUNS-nummer</span><span class="sxs-lookup"><span data-stu-id="8d732-128">DUNS number</span></span>         | <span data-ttu-id="8d732-129">DUNS står for Data Universal Number System.</span><span class="sxs-lookup"><span data-stu-id="8d732-129">DUNS stands for Data Universal Number System.</span></span> <span data-ttu-id="8d732-130">Dette er et nisifret nummer som utstedes av Dun & Bradstreet.</span><span class="sxs-lookup"><span data-stu-id="8d732-130">This is a nine-digit number that is issued by Dun & Bradstreet.</span></span>                                                                                                     |
| <span data-ttu-id="8d732-131">Leder</span><span class="sxs-lookup"><span data-stu-id="8d732-131">Manager</span></span>             | <span data-ttu-id="8d732-132">Angi personen som administrerer avdelingen.</span><span class="sxs-lookup"><span data-stu-id="8d732-132">Enter the persona that manages the department.</span></span>                                                                                                                                                                    |
| <span data-ttu-id="8d732-133">Adresser</span><span class="sxs-lookup"><span data-stu-id="8d732-133">Addresses</span></span>           | <span data-ttu-id="8d732-134">Legg til adresseinformasjonen for avdelingen.</span><span class="sxs-lookup"><span data-stu-id="8d732-134">Add the address information for the department.</span></span> <span data-ttu-id="8d732-135">Legg for eksempel til postadressen til bygningen som avdelingen er i.</span><span class="sxs-lookup"><span data-stu-id="8d732-135">For example, add the mailing address for the building that the department is located in.</span></span>                                                                          |
| <span data-ttu-id="8d732-136">Kontaktinformasjon</span><span class="sxs-lookup"><span data-stu-id="8d732-136">Contact information</span></span> | <span data-ttu-id="8d732-137">Legg til kontaktinformasjonen for avdelingen.</span><span class="sxs-lookup"><span data-stu-id="8d732-137">Add contact information for the department.</span></span> <span data-ttu-id="8d732-138">Legg for eksempel til et telefonnummer for brukerstøtten i avdelingen.</span><span class="sxs-lookup"><span data-stu-id="8d732-138">For example, add a telephone number for the service desk in the department.</span></span>                                                                                           |

<span data-ttu-id="8d732-139">Bruk følgende fremgangsmåte for å legge til en avdeling i avdelingshierarkiet.</span><span class="sxs-lookup"><span data-stu-id="8d732-139">To add a department to the department hierarchy, follow these steps.</span></span>

1.  <span data-ttu-id="8d732-140">Klikk **Personale** &gt; **Avdelinger** &gt; **Avdelingshierarki**.</span><span class="sxs-lookup"><span data-stu-id="8d732-140">Click **Human Resources** &gt; **Departments** &gt; **Department hierarchy**.</span></span>
2.  <span data-ttu-id="8d732-141">Klikk **Rediger**, og velg deretter organisasjonen som avdelingen skal være under.</span><span class="sxs-lookup"><span data-stu-id="8d732-141">Click **Edit**, and then select the organization that the department should be under.</span></span>
3.  <span data-ttu-id="8d732-142">Klikk **Sett inn**, og velg **Avdeling** i listen.</span><span class="sxs-lookup"><span data-stu-id="8d732-142">Click **Insert**, and select **Department** in the list.</span></span>
4.  <span data-ttu-id="8d732-143">Velg avdelingen som skal legges til hierarkiet, i listen over avdelinger som vises.</span><span class="sxs-lookup"><span data-stu-id="8d732-143">In the list of departments that appears, select the department to add to the hierarchy.</span></span>
5.  <span data-ttu-id="8d732-144">Lagre endringene.</span><span class="sxs-lookup"><span data-stu-id="8d732-144">Save your changes.</span></span> <span data-ttu-id="8d732-145">Du får en melding om at det har blitt opprettet en kladdeversjon av hierarkiet.</span><span class="sxs-lookup"><span data-stu-id="8d732-145">You receive a message that a draft version of the hierarchy has been created.</span></span>
6.  <span data-ttu-id="8d732-146">Når du er klar, klikker du **Publiser** i hierarkidesigneren.</span><span class="sxs-lookup"><span data-stu-id="8d732-146">When you're ready, click **Publish** in the hierarchy designer.</span></span> <span data-ttu-id="8d732-147">Du kan angi en gyldig dato som angir når hierarkiet skal publiseres.</span><span class="sxs-lookup"><span data-stu-id="8d732-147">You can enter an effective date that indicates when the hierarchy should be published.</span></span> <span data-ttu-id="8d732-148">Hvis du vil legge til en ny avdeling i begynnelsen av neste kalenderår, kan du for eksempel angi gyldighetsdatoen til 1. januar i det nye kalenderåret.</span><span class="sxs-lookup"><span data-stu-id="8d732-148">For example, to add a new department at the beginning of the next calendar year, set the effective date to January 1 of the new calendar year.</span></span> <span data-ttu-id="8d732-149">Hierarkiendringene vil tre i kraft på denne datoen.</span><span class="sxs-lookup"><span data-stu-id="8d732-149">The changes to the hierarchy will take effect on that date.</span></span>

## <a name="steps-for-creating-a-department"></a><span data-ttu-id="8d732-150">Fremgangsmåter for å opprette en avdeling</span><span class="sxs-lookup"><span data-stu-id="8d732-150">Steps for creating a department</span></span>
<span data-ttu-id="8d732-151">Se artikkelen [Definere nye avdelinger](../fin-and-ops/hr/tasks/define-new-departments.md) for trinnvis fremgangsmåte for å opprette en ny avdeling.</span><span class="sxs-lookup"><span data-stu-id="8d732-151">Refer to the [Define new departments](../fin-and-ops/hr/tasks/define-new-departments.md) article for the step-by-step procedure for creating a new department.</span></span> 