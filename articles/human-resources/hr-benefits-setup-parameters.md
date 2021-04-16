---
title: Angi parametere for Fordelsbehandling og Ansattselvbetjening for alle firmaer
description: Konfigurer parametere Fordelsbehandling og Ansattselvbetjening i Microsoft Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 10f5310ba4feba4a196d02c406ff3217637e447e
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5791491"
---
# <a name="set-benefits-management-and-employee-self-service-parameters-for-all-companies"></a><span data-ttu-id="04f71-103">Angi parametere for Fordelsbehandling og Ansattselvbetjening for alle firmaer</span><span class="sxs-lookup"><span data-stu-id="04f71-103">Set Benefits management and Employee self-service parameters for all companies</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="04f71-104">Før du kan definere fordelsplaner i Microsoft Dynamics 365 Human Resources, må du konfigurere parametere for Fordelsadministrasjon.</span><span class="sxs-lookup"><span data-stu-id="04f71-104">Before you can set up benefit plans in Microsoft Dynamics 365 Human Resources, you must configure Benefits management parameters.</span></span> <span data-ttu-id="04f71-105">Disse parameterne angir standardverdier, årsakskoder og andre alternativer.</span><span class="sxs-lookup"><span data-stu-id="04f71-105">These parameters set default values, reason codes, and other options.</span></span> 

## <a name="configure-general-parameters"></a><span data-ttu-id="04f71-106">Konfigurere generelle parametere</span><span class="sxs-lookup"><span data-stu-id="04f71-106">Configure general parameters</span></span>

1. <span data-ttu-id="04f71-107">I arbeidsområdet **Fordelsbehandling**, under **Oppsett**, velger du **Delte parametere for personaladministrasjon**.</span><span class="sxs-lookup"><span data-stu-id="04f71-107">In the **Benefits management** workspace, under **Setup**, select **Human Resources Shared Parameters**.</span></span>

2. <span data-ttu-id="04f71-108">I kategorien **Fordelsbehandling** angir du verdier for følgende felt:</span><span class="sxs-lookup"><span data-stu-id="04f71-108">In the **Benefits management** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="04f71-109">Felt</span><span class="sxs-lookup"><span data-stu-id="04f71-109">Field</span></span> | <span data-ttu-id="04f71-110">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="04f71-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="04f71-111">**Land/område**</span><span class="sxs-lookup"><span data-stu-id="04f71-111">**Country/region**</span></span> | <span data-ttu-id="04f71-112">Feltet **Land/område** bestemmer visningsrekkefølgen for postnumre/delstater.</span><span class="sxs-lookup"><span data-stu-id="04f71-112">The **Country/region** field determines the display order of ZIP codes/states.</span></span> <span data-ttu-id="04f71-113">Det valgte landet vises først i rullegardinlisten.</span><span class="sxs-lookup"><span data-stu-id="04f71-113">The selected country displays first in the dropdown list.</span></span> |
   | <span data-ttu-id="04f71-114">**Årsakskode for registrering**</span><span class="sxs-lookup"><span data-stu-id="04f71-114">**Enrollment reason code**</span></span> | <span data-ttu-id="04f71-115">Velg en standard årsakskode som skal brukes når det opprettes ansattplaner under åpen registreringsbehandling.</span><span class="sxs-lookup"><span data-stu-id="04f71-115">Select a default reason code to use when employee plans are created during open enrollment processing.</span></span> |
   | <span data-ttu-id="04f71-116">**Årsakskode for avbrudd**</span><span class="sxs-lookup"><span data-stu-id="04f71-116">**Cancellation reason code**</span></span> | <span data-ttu-id="04f71-117">Årsakskoden som skal brukes når en ansattfordelsplan avbrytes.</span><span class="sxs-lookup"><span data-stu-id="04f71-117">The reason code to use when an employee benefit plan is canceled.</span></span> <span data-ttu-id="04f71-118">Den vises i en dialogboks under annulleringsprosessen.</span><span class="sxs-lookup"><span data-stu-id="04f71-118">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="04f71-119">Brukerne kan endre **årsakskoden for annullering** om nødvendig.</span><span class="sxs-lookup"><span data-stu-id="04f71-119">Users can change it the **Cancellation reason code** if necessary.</span></span> |
   | <span data-ttu-id="04f71-120">**Årsakskode for gjenåpning**</span><span class="sxs-lookup"><span data-stu-id="04f71-120">**Reopen reason code**</span></span> | <span data-ttu-id="04f71-121">Årsakskoden som skal brukes når en ansattfordelsplan åpnes på nytt.</span><span class="sxs-lookup"><span data-stu-id="04f71-121">The reason code to use when an employee benefit plan is reopened.</span></span> <span data-ttu-id="04f71-122">Den vises i en dialogboks under annulleringsprosessen.</span><span class="sxs-lookup"><span data-stu-id="04f71-122">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="04f71-123">Brukerne kan endre **årsakskoden for ny åpning** om nødvendig.</span><span class="sxs-lookup"><span data-stu-id="04f71-123">Users can change the **Reopen reason code** if necessary.</span></span> | 
   | <span data-ttu-id="04f71-124">**Årsakskode for levetidshendelse**</span><span class="sxs-lookup"><span data-stu-id="04f71-124">**Life event reason code**</span></span> | <span data-ttu-id="04f71-125">Årsakskoden som skal brukes når en livshendelse inntreffer.</span><span class="sxs-lookup"><span data-stu-id="04f71-125">The reason code to use when a life event occurs.</span></span> |
   | <span data-ttu-id="04f71-126">**Årsakskode for satsendring**</span><span class="sxs-lookup"><span data-stu-id="04f71-126">**Rate change reason code**</span></span> | <span data-ttu-id="04f71-127">Årsakskoden som skal brukes ved avbryting og nyåpning av en fordelsplan for ansatte i løpet av oppdateringsprosessen for frekvensendring.</span><span class="sxs-lookup"><span data-stu-id="04f71-127">The reason code to use when canceling and reopening an employee benefit plan during the rate change update process.</span></span> <span data-ttu-id="04f71-128">Det viser hvilke poster som ble endret av oppdateringsprosessen for frekvensendring.</span><span class="sxs-lookup"><span data-stu-id="04f71-128">It indicates which records were changed by the rate change update process.</span></span> |
   | <span data-ttu-id="04f71-129">**Årlig fordelslønn**</span><span class="sxs-lookup"><span data-stu-id="04f71-129">**Benefits annual salary**</span></span> | <span data-ttu-id="04f71-130">Gir deg muligheten til å angi et **årlig lønnsbeløp for fordeler** for en ansatt.</span><span class="sxs-lookup"><span data-stu-id="04f71-130">Enables you to set a **Benefits annual salary** amount for an employee.</span></span> <span data-ttu-id="04f71-131">Human Resources bruker **årlig lønnsbeløp for fordeler** når de fastsetter dekningsbeløp i stedet for det årlige beløpet for fast kompensasjonen.</span><span class="sxs-lookup"><span data-stu-id="04f71-131">Human Resources will use the **Benefits annual salary** amount when determining coverage amounts, instead of the fixed compensation annual amount.</span></span> |
   | <span data-ttu-id="04f71-132">**Ny ansettelse kvalifisert**</span><span class="sxs-lookup"><span data-stu-id="04f71-132">**New hire eligible**</span></span> | <span data-ttu-id="04f71-133">Angir om nyansatte skal være berettiget.</span><span class="sxs-lookup"><span data-stu-id="04f71-133">Specifies whether new hires are eligible.</span></span> |
   | <span data-ttu-id="04f71-134">**Periode for registrering av ny ansettelse**</span><span class="sxs-lookup"><span data-stu-id="04f71-134">**New hire enrollment period**</span></span> | <span data-ttu-id="04f71-135">Tidsperioden når ny ansettelsesregistrering tillates.</span><span class="sxs-lookup"><span data-stu-id="04f71-135">The period of time the new hire enrollment is allowed.</span></span></br></br><span data-ttu-id="04f71-136">**Obs!** Denne innstillingen overstyrer registreringsperioden for ny ansettelse som du angir i regelen for planrettigheter.</span><span class="sxs-lookup"><span data-stu-id="04f71-136">**Note**: This setting overrides any new hire enrollment period you set on the plan eligibility rule.</span></span> |
   | <span data-ttu-id="04f71-137">**Standard lønnsfrekvens**</span><span class="sxs-lookup"><span data-stu-id="04f71-137">**Default pay frequency**</span></span> | <span data-ttu-id="04f71-138">Standard betalingsfrekvensen som skal brukes når nye arbeidere legges til.</span><span class="sxs-lookup"><span data-stu-id="04f71-138">The default pay frequency to use when new workers are added.</span></span> |
   | <span data-ttu-id="04f71-139">**Levetidshendelser aktivert**</span><span class="sxs-lookup"><span data-stu-id="04f71-139">**Life events enabled**</span></span> | <span data-ttu-id="04f71-140">Aktiverer livshendelser.</span><span class="sxs-lookup"><span data-stu-id="04f71-140">Enables life events.</span></span> |
   | <span data-ttu-id="04f71-141">**Skjul eldre fordelsskjemaer**</span><span class="sxs-lookup"><span data-stu-id="04f71-141">**Hide legacy benefit forms**</span></span> | <span data-ttu-id="04f71-142">Lar deg skjule eldre fordelsskjemaer.</span><span class="sxs-lookup"><span data-stu-id="04f71-142">Allows you to hide legacy benefit forms.</span></span> |
   | <span data-ttu-id="04f71-143">**Fordelsbekreftelse**</span><span class="sxs-lookup"><span data-stu-id="04f71-143">**Benefit verification**</span></span> | <span data-ttu-id="04f71-144">Bekreftelsesteksten som skal brukes i forbindelse med utsjekking av selvbetjeningsfordeler.</span><span class="sxs-lookup"><span data-stu-id="04f71-144">The verification text to use during self-service benefits checkout.</span></span> |
   | <span data-ttu-id="04f71-145">**Velg utpekte personer automatisk**</span><span class="sxs-lookup"><span data-stu-id="04f71-145">**Auto select designees**</span></span> | <span data-ttu-id="04f71-146">Angir om avhengige og mottakere skal velges automatisk basert, på rettighetene for planalternativer.</span><span class="sxs-lookup"><span data-stu-id="04f71-146">Specifies whether to automatically select dependents and beneficiaries, based on their eligibility for plan options.</span></span> |

3. <span data-ttu-id="04f71-147">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="04f71-147">Select **Save**.</span></span>

## <a name="configure-employee-self-service-parameters"></a><span data-ttu-id="04f71-148">Konfigurere parametere for ansattselvbetjening</span><span class="sxs-lookup"><span data-stu-id="04f71-148">Configure Employee self-service parameters</span></span>

1. <span data-ttu-id="04f71-149">I arbeidsområdet **Fordelsbehandling**, under **Oppsett**, velger du **Parametere for Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="04f71-149">In the **Benefits management** workspace, under **Setup**, select **Human Resources Parameters**.</span></span>

2. <span data-ttu-id="04f71-150">I kategorien **Fordelsbehandling** angir du verdier for følgende felt:</span><span class="sxs-lookup"><span data-stu-id="04f71-150">In the **Benefits management** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="04f71-151">Felt</span><span class="sxs-lookup"><span data-stu-id="04f71-151">Field</span></span> | <span data-ttu-id="04f71-152">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="04f71-152">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="04f71-153">**Fordelsbekreftelse**</span><span class="sxs-lookup"><span data-stu-id="04f71-153">**Benefit verification**</span></span> | <span data-ttu-id="04f71-154">Bekreftelsesteksten som skal brukes i forbindelse med utsjekking av selvbetjeningsfordeler.</span><span class="sxs-lookup"><span data-stu-id="04f71-154">The verification text to use during self-service benefits checkout.</span></span> |
   | <span data-ttu-id="04f71-155">**Velg utpekte personer automatisk**</span><span class="sxs-lookup"><span data-stu-id="04f71-155">**Auto select designees**</span></span> | <span data-ttu-id="04f71-156">Angir om avhengige og mottakere skal velges automatisk basert, på rettighetene for planalternativer.</span><span class="sxs-lookup"><span data-stu-id="04f71-156">Specifies whether to automatically select dependents and beneficiaries based on their eligibility for plan options.</span></span> |

3. <span data-ttu-id="04f71-157">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="04f71-157">Select **Save**.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]