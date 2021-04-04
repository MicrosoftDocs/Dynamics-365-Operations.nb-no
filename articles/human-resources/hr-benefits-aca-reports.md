---
title: Generere rapporter om lov om Affordable Care
description: I ACA-rapporteringen genereres skjema 1095-B og 1095-C til støtte for **Employer Mandate**-delen av Affordable Care Act.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: f46a8efefd8e41c08bf4de49cfec856dc0a86da1
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/17/2021
ms.locfileid: "5468041"
---
# <a name="generate-aca-reports"></a><span data-ttu-id="93ec3-103">Generere ACA-rapporter</span><span class="sxs-lookup"><span data-stu-id="93ec3-103">Generate ACA reports</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="93ec3-104">I ACA-rapporteringen genereres skjema 1095-B og 1095-C til støtte for **Employer Mandate**-delen av Affordable Care Act.</span><span class="sxs-lookup"><span data-stu-id="93ec3-104">Affordable Care Act (ACA) reporting generates forms 1095-B and 1095-C in support of the **Employer Mandate** portion of the Affordable Care Act.</span></span>

> [!NOTE]
> <span data-ttu-id="93ec3-105">ACA-rapportering er bare aktivert for juridiske enheter i USA.</span><span class="sxs-lookup"><span data-stu-id="93ec3-105">ACA reporting is only enabled for legal entities in the United States.</span></span>

## <a name="getting-started"></a><span data-ttu-id="93ec3-106">Komme i gang</span><span class="sxs-lookup"><span data-stu-id="93ec3-106">Getting started</span></span>

<span data-ttu-id="93ec3-107">Hvis du vil spore informasjon for 1095-B- og 1095-C-skjemaer, må du først opprette én eller flere Affordable Care-dekningsgrupper.</span><span class="sxs-lookup"><span data-stu-id="93ec3-107">To track information for forms 1095-B and 1095-C, you must first create one or more Affordable care coverage groups.</span></span> <span data-ttu-id="93ec3-108">Affordable Care-dekningsgrupper indikerer følgende:</span><span class="sxs-lookup"><span data-stu-id="93ec3-108">Affordable Care coverage groups indicate:</span></span>

- <span data-ttu-id="93ec3-109">Tilbud om dekning for en ansatt</span><span class="sxs-lookup"><span data-stu-id="93ec3-109">The offer of coverage for an employee</span></span>
- <span data-ttu-id="93ec3-110">Den ansattes del av den månedlige bonusen med lavest kostnad, hvis kostnaden er over den føderale fattigdomsgrensen</span><span class="sxs-lookup"><span data-stu-id="93ec3-110">The employee’s share of the lowest cost monthly premium, if the cost is above the federal poverty line</span></span>
- <span data-ttu-id="93ec3-111">Safe Harbor som brukes av arbeidsgiveren, dersom det er aktuelt</span><span class="sxs-lookup"><span data-stu-id="93ec3-111">Safe Harbor used by the employer, if applicable</span></span>

<span data-ttu-id="93ec3-112">Ved å bruke Affordable Care-grupper kan du behandle informasjonen for disse feltene uten å måtte endre hver ansattpost der betingelsene er de samme.</span><span class="sxs-lookup"><span data-stu-id="93ec3-112">Affordable Care coverage groups allow you to manage the information for these fields without changing every employee record where the conditions are the same.</span></span> <span data-ttu-id="93ec3-113">Du kan enkelt tilordne Affordable Care-dekningsgrupper til én eller flere ansatte ved hjelp av **Massetilordning**-funksjonen på siden.</span><span class="sxs-lookup"><span data-stu-id="93ec3-113">You can easily assign Affordable Care coverage groups to one or more employees by using the **Mass assign** option on the page.</span></span>

## <a name="maintaining-multiple-versions-of-a-coverage-group"></a><span data-ttu-id="93ec3-114">Vedlikeholde flere versjoner av en dekningsgruppe</span><span class="sxs-lookup"><span data-stu-id="93ec3-114">Maintaining multiple versions of a coverage group</span></span>

<span data-ttu-id="93ec3-115">Du kan vedlikeholde flere versjoner av en hvilken som helst dekningsgruppe.</span><span class="sxs-lookup"><span data-stu-id="93ec3-115">You can maintain multiple versions of any coverage group.</span></span> <span data-ttu-id="93ec3-116">Ved hjelp av denne funksjonaliteten kan du foreta endringer uten å måtte opprette en ny gruppe og tilordne ansatte på nytt.</span><span class="sxs-lookup"><span data-stu-id="93ec3-116">This functionality allows you to make changes without having to create a new group and reassign employees to it.</span></span> 

<span data-ttu-id="93ec3-117">Når du har opprettet ACA-dekningsgrupper, kan du massetildele gruppene til ansatte ved hjelp av alternativet **Massetilordning**.</span><span class="sxs-lookup"><span data-stu-id="93ec3-117">After you’ve created ACA coverage groups, you can mass assign the groups to employees with the **Mass assignment** option.</span></span> <span data-ttu-id="93ec3-118">Du kan også enkeltvis angi om du vil spore og rapportere ACA-informasjon, og tilordne en ansatt til en Affordable Care-dekningsgruppe.</span><span class="sxs-lookup"><span data-stu-id="93ec3-118">You can also individually indicate whether to track and report ACA information, and assign an employee to an Affordable Care coverage group.</span></span>

<span data-ttu-id="93ec3-119">Du trenger ikke å spore noe ACA-dekningsinformasjon, for eksempel for deltidsansatte.</span><span class="sxs-lookup"><span data-stu-id="93ec3-119">You don't need to track some ACA coverage information, such as for part-time employees.</span></span> <span data-ttu-id="93ec3-120">I dette tilfellet angir du **Rapportdekning**-feltet til **Nei**.</span><span class="sxs-lookup"><span data-stu-id="93ec3-120">In this case, set the **Report coverage** field to **No**.</span></span> <span data-ttu-id="93ec3-121">Selv om du må tilordne hver ansatt med sporbar ACA-informasjon til en Affordable Care-dekningsgruppe, kan du fremdeles endre følgende alternativer for måneder med forskjellige verdier:</span><span class="sxs-lookup"><span data-stu-id="93ec3-121">Although you must assign each employee with trackable ACA information to an Affordable Care coverage group, you can still change the following options for months with different values:</span></span>

- <span data-ttu-id="93ec3-122">**Tilbud om dekning**</span><span class="sxs-lookup"><span data-stu-id="93ec3-122">**Offer of coverage**</span></span>
- <span data-ttu-id="93ec3-123">**Ansattdel av kostnad**</span><span class="sxs-lookup"><span data-stu-id="93ec3-123">**Employee share of cost**</span></span>
- <span data-ttu-id="93ec3-124">**Safe harbor**</span><span class="sxs-lookup"><span data-stu-id="93ec3-124">**Safe Harbor**</span></span>

<span data-ttu-id="93ec3-125">Hvis du vil angi unntak for Affordable Care-dekningsgruppenes verdier, velger du på koblingen for **Affordable Care-dekning** på siden **Arbeiderdetaljer** under delen **Mer informasjon** i kategorien **Ansettelse**.</span><span class="sxs-lookup"><span data-stu-id="93ec3-125">To enter exceptions for Affordable Care coverage group values, select the **Affordable Care Coverage** link on the **Worker detail** page under the **Additional information** section on the **Employment tab**.</span></span>

## <a name="reporting-health-care-coverage"></a><span data-ttu-id="93ec3-126">Rapportere helsedekning</span><span class="sxs-lookup"><span data-stu-id="93ec3-126">Reporting health care coverage</span></span>

<span data-ttu-id="93ec3-127">I tillegg til å spore helseforsikringsdekning som tilbys heltidsansatte, må tilleggsinformasjon rapporteres på 1095-C hvis arbeidsgiveren arbeidsgiversponset selvforsikret helsedekning som den ansatte dekkes under (uavhengig av om de jobber fulltid eller deltid).</span><span class="sxs-lookup"><span data-stu-id="93ec3-127">In addition to tracking health insurance coverage offered to full-time employees, if the employer offers employer-sponsored self-insured health coverage for which the employee is enrolled (regardless of whether their employment status is full-time or part-time), additional information needs to be reported on the 1095-C.</span></span> <span data-ttu-id="93ec3-128">Hver ansatt (inkludert avhengige) som er dekket av arbeidsgiver-sponsede fordelsplaner, må tas med i rapporten for månedene de var dekket.</span><span class="sxs-lookup"><span data-stu-id="93ec3-128">Each employee (including dependents) covered by the employer-sponsored benefit plans needs to be included on the report for the months they were covered.</span></span> 

<span data-ttu-id="93ec3-129">Du kan angi om hver fordelsplan må rapporteres eller ikke, ved å merke av for **ACA-rapporterbar**.</span><span class="sxs-lookup"><span data-stu-id="93ec3-129">You can indicate whether or not each benefit plan must be reported by selecting the **ACA reportable** check box.</span></span>

<span data-ttu-id="93ec3-130">Dessuten, hvis ansatte har valgt å dekke noen av sine avhengige under en fordel, kan du angi datoene den avhengige ble dekket, for hver ansatt, på siden **Vedlikehold fordeler**.</span><span class="sxs-lookup"><span data-stu-id="93ec3-130">In addition, if employees have chosen to have any of their dependents covered under a benefit, you can indicate the dates the dependent was covered for each employee on the **Maintain benefits** page.</span></span> <span data-ttu-id="93ec3-131">Du angir at den avhengige dekkes inn under fordelen ved å velge **Rediger**-knappen i handlingsruten på hurtigfanen **Avhengige**.</span><span class="sxs-lookup"><span data-stu-id="93ec3-131">To indicate that the dependent is covered under the benefit, select the **Edit** button in the action pane of the **Dependents** fast tab.</span></span>

<span data-ttu-id="93ec3-132">På siden **Behandling for dekningsdato for avhengig** kan du angi datoene da den avhengige ble dekket av fordelen.</span><span class="sxs-lookup"><span data-stu-id="93ec3-132">On the **Dependent coverage date manager** page, you can indicate the dates the dependent was covered by the benefit.</span></span> <span data-ttu-id="93ec3-133">Når det angis datoer på denne siden, merkes det automatisk av for **Dekket** på **Vedlikehold fordeler**-siden.</span><span class="sxs-lookup"><span data-stu-id="93ec3-133">Entering dates on this page will automatically select the **Covered** checkbox on the **Maintain benefits** page.</span></span>

## <a name="generate-1095-b-and-1095-c-forms"></a><span data-ttu-id="93ec3-134">Generere 1095-B- og 1095-C-skjemaer</span><span class="sxs-lookup"><span data-stu-id="93ec3-134">Generate 1095-B and 1095-C forms</span></span>

<span data-ttu-id="93ec3-135">Du kan også generere 1095-B- og 1095-C-skjemaer fra produktet, og levere dem til alle ansatte.</span><span class="sxs-lookup"><span data-stu-id="93ec3-135">You can also generate 1095-B and 1095-C forms from within the product, and distribute them to each of your employees.</span></span> <span data-ttu-id="93ec3-136">Systemet kan også generere 1095-C-skjemaer elektronisk og overføringsfilene 1094-C IRS.</span><span class="sxs-lookup"><span data-stu-id="93ec3-136">The system can also electronically generate 1095-C forms and the 1094-C IRS transmittal files.</span></span>  

<span data-ttu-id="93ec3-137">Når du genererer skjemaet 1095-C, skriver du inn i det aktuelle skatteåret og angir om personnumre skal maskeres.</span><span class="sxs-lookup"><span data-stu-id="93ec3-137">When generating the 1095-C form, enter the appropriate tax year and indicate if social security numbers should be masked.</span></span> <span data-ttu-id="93ec3-138">Hvis du skriver ut 1095-C-skjemaer for mer enn 500 ansatte, får du mer enn én PDF-fil.</span><span class="sxs-lookup"><span data-stu-id="93ec3-138">If you're printing 1095-C forms for more than 500 employees, you'll receive more than one PDF file.</span></span> <span data-ttu-id="93ec3-139">Det anbefales at du øker **Maksimal filstørrelse** i **Parametere for dokumentstyring**-vinduet til 150 MB.</span><span class="sxs-lookup"><span data-stu-id="93ec3-139">It’s recommended that you increase the **Maximum file size** in the **Document management parameters** window to 150 MB.</span></span>

## <a name="viewing-information"></a><span data-ttu-id="93ec3-140">Vise informasjon</span><span class="sxs-lookup"><span data-stu-id="93ec3-140">Viewing information</span></span>

<span data-ttu-id="93ec3-141">Du kan bruke siden **Affordable Care-dekning for arbeidere** hvis du vil se hvilke ansatte som er tilordnet til hver dekningsgruppe, hvilke ansatte som ikke trenger å være med i en rapport, og hvilke ansatte som ikke er tilordnet.</span><span class="sxs-lookup"><span data-stu-id="93ec3-141">You can use the **Worker Affordable Care coverage** page to see which employees have been assigned to each coverage group, which employees don’t need to be included on a report, and which employees are unassigned.</span></span>

<span data-ttu-id="93ec3-142">Hvis noen av standardverdiene fra Affordable Care-dekningsgruppen har blitt overstyrt, vises en stjerne ved siden av verdien som ble endret.</span><span class="sxs-lookup"><span data-stu-id="93ec3-142">If any of the default values from the Affordable Care coverage group have been overridden, an asterisk will appear next to the value that was changed.</span></span> <span data-ttu-id="93ec3-143">Hvis verdiene for alle tolv månedene er de samme, og ikke har blitt overstyrt, skrives verdien ut i **Alle 12 måneder**-kolonnen.</span><span class="sxs-lookup"><span data-stu-id="93ec3-143">If the values for all 12 months are the same and haven’t been overridden, the value will print in the **All 12 months** column.</span></span>

<span data-ttu-id="93ec3-144">Du kan også bruke forespørselsvinduet til å forstå hvilke ansatte som er flagget som ikke ACA-rapporteringsbare.</span><span class="sxs-lookup"><span data-stu-id="93ec3-144">You can also use the inquiry window to understand which employees have been flagged as not ACA reportable.</span></span> <span data-ttu-id="93ec3-145">Du trenger ikke å spore om dekningen ble tilbudt dem, og du trenger ikke å utstede en 1095-C til dem på slutten av året.</span><span class="sxs-lookup"><span data-stu-id="93ec3-145">You don’t need to track whether coverage was offered to them and won't need to issue a 1095-C to them at the end of the year.</span></span> <span data-ttu-id="93ec3-146">Velg **Ikke ACA-rapporterbar** i **Filtrer etter**-feltet for å generere en liste over alle ansatte som ikke vil motta 1095-C.</span><span class="sxs-lookup"><span data-stu-id="93ec3-146">Select **Not ACA reportable** in the **Filter by** field to generate a list of all employees who won't receive a 1095-C.</span></span>

<span data-ttu-id="93ec3-147">I tillegg kan du vise alle ansatte som ikke er tilordnet (**ACA-rapportens dekningsfelt** er tomt), eller som er knyttet til en Affordable Care-dekningsgruppe som er utløpt for året som er valgt i **År**-feltet.</span><span class="sxs-lookup"><span data-stu-id="93ec3-147">In addition, you can view any employees who are unassigned (the **ACA Report coverage** field is empty) or who have been assigned to an Affordable Care coverage group that is expired for the year selected in the **Year** field.</span></span>

<span data-ttu-id="93ec3-148">Du kan eksportere lister over ansatte som ble generert ved hjelp av noen av alternativene for filtrering til Excel.</span><span class="sxs-lookup"><span data-stu-id="93ec3-148">You can export lists of employees that were generated using any of the filtering options to Excel.</span></span>

<span data-ttu-id="93ec3-149">Hvis du må rapportere dekkede personer fordi du gir selvforsikret dekning, kan du vise avhengige som dekkes av fordelsplaner, som er merket som **ACA-rapporterbar**.</span><span class="sxs-lookup"><span data-stu-id="93ec3-149">If you need to report covered individuals because you provide self-insured coverage, you can view any dependents covered under benefit plans marked as **ACA reportable**.</span></span> <span data-ttu-id="93ec3-150">Velg **Vis avhengig dekning** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="93ec3-150">Select **View Dependent coverage** on the action pane.</span></span>

> [!NOTE]
> <span data-ttu-id="93ec3-151">Bare fordelsplaner som er merket som **ACA-rapporterbare**, vises i forespørselsvinduet.</span><span class="sxs-lookup"><span data-stu-id="93ec3-151">Only benefit plans marked as **ACA reportable** display in the inquiry window.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]