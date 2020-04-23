---
title: Angi parametere i Fordelsbehandling
description: Konfigurer parametere for Fordelsadministrasjon i Microsoft Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9d6d463df08b9ae68047f09316f19e98740a8441
ms.sourcegitcommit: a9461650d11d6845e1942865ebf7e35f75f61ad3
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/06/2020
ms.locfileid: "3229769"
---
# <a name="set-benefits-management-parameters"></a><span data-ttu-id="ac45b-103">Angi parametere for fordelsbehandling</span><span class="sxs-lookup"><span data-stu-id="ac45b-103">Set Benefits management parameters</span></span>

<span data-ttu-id="ac45b-104">Før du kan definere permisjonsplaner i Microsoft Dynamics 365 Human Resources, må du konfigurere parametere for Fordelsadministrasjon.</span><span class="sxs-lookup"><span data-stu-id="ac45b-104">Before you can set up leave plans in Microsoft Dynamics 365 Human Resources, you must configure Benefits management parameters.</span></span> <span data-ttu-id="ac45b-105">Disse parameterne angir standardverdier, årsakskoder og andre alternativer.</span><span class="sxs-lookup"><span data-stu-id="ac45b-105">These parameters set default values, reason codes, and other options.</span></span>

## <a name="configure-general-parameters"></a><span data-ttu-id="ac45b-106">Konfigurere generelle parametere</span><span class="sxs-lookup"><span data-stu-id="ac45b-106">Configure general parameters</span></span>

1. <span data-ttu-id="ac45b-107">I arbeidsområdet **Fordelsbehandling**, under **Oppsett**, velger du **Parametere**.</span><span class="sxs-lookup"><span data-stu-id="ac45b-107">In the **Benefits management** workspace, under **Setup**, select **Parameters**.</span></span>

2. <span data-ttu-id="ac45b-108">I kategorien **Generelt** angir du verdier for følgende felt:</span><span class="sxs-lookup"><span data-stu-id="ac45b-108">In the **General** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="ac45b-109">Felt</span><span class="sxs-lookup"><span data-stu-id="ac45b-109">Field</span></span> | <span data-ttu-id="ac45b-110">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="ac45b-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="ac45b-111">**Land/område**</span><span class="sxs-lookup"><span data-stu-id="ac45b-111">**Country/region**</span></span> | <span data-ttu-id="ac45b-112">Feltet **Land/område** bestemmer visningsrekkefølgen for postnumre/delstater.</span><span class="sxs-lookup"><span data-stu-id="ac45b-112">The **Country/region** field determines the display order of ZIP codes/states.</span></span> <span data-ttu-id="ac45b-113">Det valgte landet vises først i rullegardinlisten.</span><span class="sxs-lookup"><span data-stu-id="ac45b-113">The selected country displays first in the dropdown list.</span></span> |
   | <span data-ttu-id="ac45b-114">**Årsakskode for registrering**</span><span class="sxs-lookup"><span data-stu-id="ac45b-114">**Enrollment reason code**</span></span> | <span data-ttu-id="ac45b-115">Velg en standard årsakskode som skal brukes når det opprettes ansattplaner under åpen registreringsbehandling.</span><span class="sxs-lookup"><span data-stu-id="ac45b-115">Select a default reason code to use when employee plans are created during open enrollment processing.</span></span> |
   | <span data-ttu-id="ac45b-116">**Årsakskode for avbrudd**</span><span class="sxs-lookup"><span data-stu-id="ac45b-116">**Cancellation reason code**</span></span> | <span data-ttu-id="ac45b-117">Årsakskoden som skal brukes når en ansattfordelsplan avbrytes.</span><span class="sxs-lookup"><span data-stu-id="ac45b-117">The reason code to use when an employee benefit plan is canceled.</span></span> <span data-ttu-id="ac45b-118">Den vises i en dialogboks under annulleringsprosessen.</span><span class="sxs-lookup"><span data-stu-id="ac45b-118">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="ac45b-119">Brukerne kan endre **årsakskoden for annullering** om nødvendig.</span><span class="sxs-lookup"><span data-stu-id="ac45b-119">Users can change it the **Cancellation reason code** if necessary.</span></span> |
   | <span data-ttu-id="ac45b-120">**Årsakskode for gjenåpning**</span><span class="sxs-lookup"><span data-stu-id="ac45b-120">**Reopen reason code**</span></span> | <span data-ttu-id="ac45b-121">Årsakskoden som skal brukes når en ansattfordelsplan åpnes på nytt.</span><span class="sxs-lookup"><span data-stu-id="ac45b-121">The reason code to use when an employee benefit plan is reopened.</span></span> <span data-ttu-id="ac45b-122">Den vises i en dialogboks under annulleringsprosessen.</span><span class="sxs-lookup"><span data-stu-id="ac45b-122">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="ac45b-123">Brukerne kan endre **årsakskoden for ny åpning** om nødvendig.</span><span class="sxs-lookup"><span data-stu-id="ac45b-123">Users can change the **Reopen reason code** if necessary.</span></span> | 
   | <span data-ttu-id="ac45b-124">**Årsakskode for levetidshendelse**</span><span class="sxs-lookup"><span data-stu-id="ac45b-124">**Life event reason code**</span></span> | <span data-ttu-id="ac45b-125">Årsakskoden som skal brukes når en livshendelse inntreffer.</span><span class="sxs-lookup"><span data-stu-id="ac45b-125">The reason code to use when a life event occurs.</span></span> |
   | <span data-ttu-id="ac45b-126">**Årsakskode for satsendring**</span><span class="sxs-lookup"><span data-stu-id="ac45b-126">**Rate change reason code**</span></span> | <span data-ttu-id="ac45b-127">Årsakskoden som skal brukes ved avbryting og nyåpning av en fordelsplan for ansatte i løpet av oppdateringsprosessen for frekvensendring.</span><span class="sxs-lookup"><span data-stu-id="ac45b-127">The reason code to use when canceling and reopening an employee benefit plan during the rate change update process.</span></span> <span data-ttu-id="ac45b-128">Det viser hvilke poster som ble endret av oppdateringsprosessen for frekvensendring.</span><span class="sxs-lookup"><span data-stu-id="ac45b-128">It indicates which records were changed by the rate change update process.</span></span> |
   | <span data-ttu-id="ac45b-129">**Ny ansettelse kvalifisert**</span><span class="sxs-lookup"><span data-stu-id="ac45b-129">**New hire eligible**</span></span> | <span data-ttu-id="ac45b-130">Angir om nyansatte skal være berettiget.</span><span class="sxs-lookup"><span data-stu-id="ac45b-130">Specifies whether new hires are eligible.</span></span> |
   | <span data-ttu-id="ac45b-131">**Periode for registrering av ny ansettelse**</span><span class="sxs-lookup"><span data-stu-id="ac45b-131">**New hire enrollment period**</span></span> | <span data-ttu-id="ac45b-132">Tidsperioden når ny ansettelsesregistrering tillates.</span><span class="sxs-lookup"><span data-stu-id="ac45b-132">The period of time the new hire enrollment is allowed.</span></span></br></br><span data-ttu-id="ac45b-133">**Obs!** Denne innstillingen overstyrer registreringsperioden for ny ansettelse som du angir i regelen for planrettigheter.</span><span class="sxs-lookup"><span data-stu-id="ac45b-133">**Note**: This setting overrides any new hire enrollment period you set on the plan eligibility rule.</span></span> | 
   | <span data-ttu-id="ac45b-134">**Levetidshendelser aktivert**</span><span class="sxs-lookup"><span data-stu-id="ac45b-134">**Life events enabled**</span></span> | <span data-ttu-id="ac45b-135">Aktiverer livshendelser.</span><span class="sxs-lookup"><span data-stu-id="ac45b-135">Enables life events.</span></span> |
   | <span data-ttu-id="ac45b-136">**Skjul eldre fordelsskjemaer**</span><span class="sxs-lookup"><span data-stu-id="ac45b-136">**Hide legacy benefit forms**</span></span> | <span data-ttu-id="ac45b-137">Lar deg skjule eldre fordelsskjemaer.</span><span class="sxs-lookup"><span data-stu-id="ac45b-137">Allows you to hide legacy benefit forms.</span></span> |

3. <span data-ttu-id="ac45b-138">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="ac45b-138">Select **Save**.</span></span>

## <a name="configure-employee-self-service-parameters"></a><span data-ttu-id="ac45b-139">Konfigurere parametere for ansattselvbetjening</span><span class="sxs-lookup"><span data-stu-id="ac45b-139">Configure Employee self service parameters</span></span>

1. <span data-ttu-id="ac45b-140">I arbeidsområdet **Fordelsbehandling**, under **Oppsett**, velger du **Parametere**.</span><span class="sxs-lookup"><span data-stu-id="ac45b-140">In the **Benefits management** workspace, under **Setup**, select **Parameters**.</span></span>

2. <span data-ttu-id="ac45b-141">I kategorien **Ansattselvbetjening** angir du verdier for følgende felt:</span><span class="sxs-lookup"><span data-stu-id="ac45b-141">In the **Employee self service** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="ac45b-142">Felt</span><span class="sxs-lookup"><span data-stu-id="ac45b-142">Field</span></span> | <span data-ttu-id="ac45b-143">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="ac45b-143">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="ac45b-144">**Fordelsbekreftelse**</span><span class="sxs-lookup"><span data-stu-id="ac45b-144">**Benefit verification**</span></span> | <span data-ttu-id="ac45b-145">Bekreftelsesteksten som skal brukes i forbindelse med utsjekking av selvbetjeningsfordeler.</span><span class="sxs-lookup"><span data-stu-id="ac45b-145">The verification text to use during self-service benefits checkout.</span></span> |
   | <span data-ttu-id="ac45b-146">**Velg utpekte personer automatisk**</span><span class="sxs-lookup"><span data-stu-id="ac45b-146">**Auto select designees**</span></span> | <span data-ttu-id="ac45b-147">Angir om avhengige og mottakere skal velges automatisk basert, på rettighetene for planalternativer.</span><span class="sxs-lookup"><span data-stu-id="ac45b-147">Specifies whether to automatically select dependents and beneficiaries based on their eligibility for plan options.</span></span> |

3. <span data-ttu-id="ac45b-148">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="ac45b-148">Select **Save**.</span></span>
