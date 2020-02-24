---
title: Angi parametere i Fordelsbehandling
description: Konfigurer parametere for Fordelsadministrasjon i Microsoft Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
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
ms.openlocfilehash: ab9b1fc78ce42479d9265b80337adf899cec3866
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010079"
---
# <a name="set-benefits-management-parameters"></a><span data-ttu-id="87ff4-103">Angi parametere i Fordelsbehandling</span><span class="sxs-lookup"><span data-stu-id="87ff4-103">Set Benefits management parameters</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="87ff4-104">Før du kan definere permisjonsplaner i Microsoft Dynamics 365 Human Resources, må du konfigurere parametere for Fordelsadministrasjon.</span><span class="sxs-lookup"><span data-stu-id="87ff4-104">Before you can set up leave plans in Microsoft Dynamics 365 Human Resources, you need to configure Benefits management parameters.</span></span> <span data-ttu-id="87ff4-105">Disse parameterne angir standardverdier, årsakskoder og andre alternativer.</span><span class="sxs-lookup"><span data-stu-id="87ff4-105">These parameters set default values, reason codes, and other options.</span></span>

## <a name="configure-general-parameters"></a><span data-ttu-id="87ff4-106">Konfigurere generelle parametere</span><span class="sxs-lookup"><span data-stu-id="87ff4-106">Configure general parameters</span></span>

1. <span data-ttu-id="87ff4-107">I arbeidsområdet **Fordelsbehandling**, under **Oppsett**, velger du **Parametere**.</span><span class="sxs-lookup"><span data-stu-id="87ff4-107">In the **Benefits management** workspace, under **Setup**, select **Parameters**.</span></span>

2. <span data-ttu-id="87ff4-108">I kategorien **Generelt** angir du verdier for følgende felt:</span><span class="sxs-lookup"><span data-stu-id="87ff4-108">In the **General** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="87ff4-109">Felt</span><span class="sxs-lookup"><span data-stu-id="87ff4-109">Field</span></span> | <span data-ttu-id="87ff4-110">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="87ff4-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="87ff4-111">**Land/område**</span><span class="sxs-lookup"><span data-stu-id="87ff4-111">**Country/region**</span></span> | <span data-ttu-id="87ff4-112">Feltet **Land/område** bestemmer visningsrekkefølgen for postnumre/delstater.</span><span class="sxs-lookup"><span data-stu-id="87ff4-112">The **Country/region** field determines the display order of ZIP codes/states.</span></span> <span data-ttu-id="87ff4-113">Det valgte landet vises først i rullegardinlisten.</span><span class="sxs-lookup"><span data-stu-id="87ff4-113">The selected country displays first in the dropdown list.</span></span> |
   | <span data-ttu-id="87ff4-114">**Årsakskode for registrering**</span><span class="sxs-lookup"><span data-stu-id="87ff4-114">**Enrollment reason code**</span></span> | <span data-ttu-id="87ff4-115">Velg en standard årsakskode som skal brukes når det opprettes ansattplaner under åpen registreringsbehandling.</span><span class="sxs-lookup"><span data-stu-id="87ff4-115">Select a default reason code to use when employee plans are created during open enrollment processing.</span></span> |
   | <span data-ttu-id="87ff4-116">**Årsakskode for avbrudd**</span><span class="sxs-lookup"><span data-stu-id="87ff4-116">**Cancellation reason code**</span></span> | <span data-ttu-id="87ff4-117">Årsakskoden som skal brukes når en ansattfordelsplan avbrytes.</span><span class="sxs-lookup"><span data-stu-id="87ff4-117">The reason code to use when an employee benefit plan is canceled.</span></span> <span data-ttu-id="87ff4-118">Den vises i en dialogboks under annulleringsprosessen.</span><span class="sxs-lookup"><span data-stu-id="87ff4-118">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="87ff4-119">Brukerne kan endre **årsakskoden for annullering** om nødvendig.</span><span class="sxs-lookup"><span data-stu-id="87ff4-119">Users can change it the **Cancellation reason code** if necessary.</span></span> |
   | <span data-ttu-id="87ff4-120">**Årsakskode for gjenåpning**</span><span class="sxs-lookup"><span data-stu-id="87ff4-120">**Reopen reason code**</span></span> | <span data-ttu-id="87ff4-121">Årsakskoden som skal brukes når en ansattfordelsplan åpnes på nytt.</span><span class="sxs-lookup"><span data-stu-id="87ff4-121">The reason code to use when an employee benefit plan is reopened.</span></span> <span data-ttu-id="87ff4-122">Den vises i en dialogboks under annulleringsprosessen.</span><span class="sxs-lookup"><span data-stu-id="87ff4-122">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="87ff4-123">Brukerne kan endre **årsakskoden for ny åpning** om nødvendig.</span><span class="sxs-lookup"><span data-stu-id="87ff4-123">Users can change the **Reopen reason code** if necessary.</span></span> | 
   | <span data-ttu-id="87ff4-124">**Årsakskode for levetidshendelse**</span><span class="sxs-lookup"><span data-stu-id="87ff4-124">**Life event reason code**</span></span> | <span data-ttu-id="87ff4-125">Årsakskoden som skal brukes når en livshendelse inntreffer.</span><span class="sxs-lookup"><span data-stu-id="87ff4-125">The reason code to use when a life event occurs.</span></span> |
   | <span data-ttu-id="87ff4-126">**Årsakskode for satsendring**</span><span class="sxs-lookup"><span data-stu-id="87ff4-126">**Rate change reason code**</span></span> | <span data-ttu-id="87ff4-127">Årsakskoden som skal brukes ved avbryting og nyåpning av en fordelsplan for ansatte i løpet av oppdateringsprosessen for frekvensendring.</span><span class="sxs-lookup"><span data-stu-id="87ff4-127">The reason code to use when canceling and reopening an employee benefit plan during the rate change update process.</span></span> <span data-ttu-id="87ff4-128">Det viser hvilke poster som ble endret av oppdateringsprosessen for frekvensendring.</span><span class="sxs-lookup"><span data-stu-id="87ff4-128">It indicates which records were changed by the rate change update process.</span></span> |
   | <span data-ttu-id="87ff4-129">**Ny ansettelse kvalifisert**</span><span class="sxs-lookup"><span data-stu-id="87ff4-129">**New hire eligible**</span></span> | <span data-ttu-id="87ff4-130">Angir om nyansatte skal være berettiget.</span><span class="sxs-lookup"><span data-stu-id="87ff4-130">Specifies whether new hires are eligible.</span></span> |
   | <span data-ttu-id="87ff4-131">**Periode for registrering av ny ansettelse**</span><span class="sxs-lookup"><span data-stu-id="87ff4-131">**New hire enrollment period**</span></span> | <span data-ttu-id="87ff4-132">Tidsperioden når ny ansettelsesregistrering tillates.</span><span class="sxs-lookup"><span data-stu-id="87ff4-132">The period of time the new hire enrollment is allowed.</span></span></br></br><span data-ttu-id="87ff4-133">**Obs!** Denne innstillingen overstyrer registreringsperioden for ny ansettelse som du angir i regelen for planrettigheter.</span><span class="sxs-lookup"><span data-stu-id="87ff4-133">**Note**: This setting overrides any new hire enrollment period you set on the plan eligibility rule.</span></span> | 
   | <span data-ttu-id="87ff4-134">**Årlig lønnsøkning**</span><span class="sxs-lookup"><span data-stu-id="87ff4-134">**Annual salary enhancement**</span></span> | <span data-ttu-id="87ff4-135">Angir om beløpet for **Årlig fordel lønn** skal beregnes automatisk i **Fordelsdetaljer for ansatt**.</span><span class="sxs-lookup"><span data-stu-id="87ff4-135">Specifies whether to automatically calculate the **Annual benefit salary** amount in **Employment Benefit Details**.</span></span> <span data-ttu-id="87ff4-136">Dette er basert på **Fast kompensasjonssats**, **Gjennomsnittlig timer** og **Betalingsfrekvens**.</span><span class="sxs-lookup"><span data-stu-id="87ff4-136">It's based on the employee’s **Fixed compensation pay rate**, **Average hours**, and **Payment frequency**.</span></span></br></br><span data-ttu-id="87ff4-137">**Gjennomsnittlig timer** x **Fast betalingssats** x **Betalingsfrekvens** (antall betalingsperioder) = **Årlig fordel lønn**</span><span class="sxs-lookup"><span data-stu-id="87ff4-137">**Average hours** x **Fixed pay rate** x **Payment frequency** (# of pay periods) = **Annual benefit salary**</span></span> </br></br><span data-ttu-id="87ff4-138">Hvis noen av verdiene i feltene **Gjennomsnittlig timer**, **Fast kompensasjonssats** eller **Betalingsfrekvens** endres, beregner systemet automatisk beløpet for **Årlig fordel lønn** på nytt for den ansatte basert på de endrede verdiene.</span><span class="sxs-lookup"><span data-stu-id="87ff4-138">If any of the values in the **Average hours**, **Fixed compensation pay rate**, or **Payment frequency** fields change, the system automatically recalculates the employee’s **Annual benefit salary** amount based on the changed values.</span></span> <span data-ttu-id="87ff4-139">Systemet oppretter en **Gyldig dato**-post for å identifisere nøyaktig dato og klokkeslett for når endringen ble utført.</span><span class="sxs-lookup"><span data-stu-id="87ff4-139">The system creates a **Date effective** record to identify the exact date and time the change occurred.</span></span> <span data-ttu-id="87ff4-140">Du kan manuelt redigere beløpet for **Årlig fordel lønn** hvis det er nødvendig.</span><span class="sxs-lookup"><span data-stu-id="87ff4-140">You can manually edit the **Annual benefit salary** amount if necessary.</span></span> |
   | <span data-ttu-id="87ff4-141">**Levetidshendelser aktivert**</span><span class="sxs-lookup"><span data-stu-id="87ff4-141">**Life events enabled**</span></span> | <span data-ttu-id="87ff4-142">Aktiverer livshendelser.</span><span class="sxs-lookup"><span data-stu-id="87ff4-142">Enables life events.</span></span> |
   | <span data-ttu-id="87ff4-143">**Skjul eldre fordelsskjemaer**</span><span class="sxs-lookup"><span data-stu-id="87ff4-143">**Hide legacy benefit forms**</span></span> | <span data-ttu-id="87ff4-144">Lar deg skjule eldre fordelsskjemaer.</span><span class="sxs-lookup"><span data-stu-id="87ff4-144">Allows you to hide legacy benefit forms.</span></span> |

3. <span data-ttu-id="87ff4-145">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="87ff4-145">Select **Save**.</span></span>

## <a name="configure-employee-self-service-parameters"></a><span data-ttu-id="87ff4-146">Konfigurere parametere for ansattselvbetjening</span><span class="sxs-lookup"><span data-stu-id="87ff4-146">Configure Employee self service parameters</span></span>

1. <span data-ttu-id="87ff4-147">I arbeidsområdet **Fordelsbehandling**, under **Oppsett**, velger du **Parametere**.</span><span class="sxs-lookup"><span data-stu-id="87ff4-147">In the **Benefits management** workspace, under **Setup**, select **Parameters**.</span></span>

2. <span data-ttu-id="87ff4-148">I kategorien **Ansattselvbetjening** angir du verdier for følgende felt:</span><span class="sxs-lookup"><span data-stu-id="87ff4-148">In the **Employee self service** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="87ff4-149">Felt</span><span class="sxs-lookup"><span data-stu-id="87ff4-149">Field</span></span> | <span data-ttu-id="87ff4-150">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="87ff4-150">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="87ff4-151">**Fordelsbekreftelse**</span><span class="sxs-lookup"><span data-stu-id="87ff4-151">**Benefit verification**</span></span> | <span data-ttu-id="87ff4-152">Bekreftelsesteksten som skal brukes i forbindelse med utsjekking av selvbetjeningsfordeler.</span><span class="sxs-lookup"><span data-stu-id="87ff4-152">The verification text to use during self-service benefits checkout.</span></span> |
   | <span data-ttu-id="87ff4-153">**Velg utpekte personer automatisk**</span><span class="sxs-lookup"><span data-stu-id="87ff4-153">**Auto select designees**</span></span> | <span data-ttu-id="87ff4-154">Angir om avhengige og mottakere skal velges automatisk basert, på rettighetene for planalternativer.</span><span class="sxs-lookup"><span data-stu-id="87ff4-154">Specifies whether to automatically select dependents and beneficiaries based on their eligibility for plan options.</span></span> |

3. <span data-ttu-id="87ff4-155">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="87ff4-155">Select **Save**.</span></span>
