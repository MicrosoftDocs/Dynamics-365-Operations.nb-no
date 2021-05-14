---
title: Administrere måleenheter
description: Dette emnet beskriver hvordan du definerer en målenhet, angir oversettelser for enheten og beskrivelsen og definerer omregningsreglene for relaterte enheter.
author: sorenva
ms.date: 04/09/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, UnitOfMeasure, UnitOfMeasureReportingTranslation, UnitOfMeasureTranslation, UnitOfMeasureConversion, UnitOfMeasureConversionEditOrCreate, UnitOfMeasureLookup, UnitOfMeasureCalculator, UnitOfMeasureWizard, UnitOfMeasureLookupTest
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d36839cd8e3398225d3421bf0f268068599ca49f
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921347"
---
# <a name="manage-units-of-measure"></a><span data-ttu-id="17854-103">Administrere måleenheter</span><span class="sxs-lookup"><span data-stu-id="17854-103">Manage units of measure</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="17854-104">Dette emnet beskriver hvordan du definerer en målenhet, angir oversettelser for enheten og beskrivelsen og definerer omregningsreglene for relaterte enheter.</span><span class="sxs-lookup"><span data-stu-id="17854-104">This topic describes how to define a unit of measure, provide translations for the unit and its description, and define conversion rules for related units.</span></span>

## <a name="open-the-units-page"></a><span data-ttu-id="17854-105">Åpne Enheter-siden</span><span class="sxs-lookup"><span data-stu-id="17854-105">Open the Units page</span></span>

<span data-ttu-id="17854-106">Hvis du vil opprette og arbeide med måleenhetene som er tilgjengelige i systemet, kan du gå til **Organisasjonsstyring \> Oppsett \> Enheter \> Enheter**.</span><span class="sxs-lookup"><span data-stu-id="17854-106">To create and work with the units of measure that are available in your system, go to **Organization administration \> Setup \> Units \> Units**.</span></span>

<span data-ttu-id="17854-107">Resten av delene i dette emnet beskriver hva du kan gjøre på **Enheter**-siden.</span><span class="sxs-lookup"><span data-stu-id="17854-107">The remaining sections of this topic describe what you can do on the **Units** page.</span></span>

## <a name="create-standard-units-and-conversions"></a><span data-ttu-id="17854-108">Opprette standardenheter og konverteringer</span><span class="sxs-lookup"><span data-stu-id="17854-108">Create standard units and conversions</span></span>

<span data-ttu-id="17854-109">Hvis systemet ikke allerede inneholder de mest vanlige måleenhetene for det metriske systemet og/eller det amerikanske målesystemet (USCS), kan installasjonsveiviseren hjelpe deg med å komme raskt i gang med grunnleggende enhetsdefinisjoner og konverteringer.</span><span class="sxs-lookup"><span data-stu-id="17854-109">If your system doesn't already include the most commonly used units of measure for the metric system and/or the US customary system (USCS), the unit setup wizard can help you quickly get started with basic unit definitions and conversions.</span></span> <span data-ttu-id="17854-110">Hvis du vil fullføre veiviseren, velger du **veiviseren for enhetsopprettelse** i handlingsruten, og deretter følger du instruksjonene på skjermen.</span><span class="sxs-lookup"><span data-stu-id="17854-110">To complete the wizard, select **Unit creation wizard** on the Action Pane, and then follow the on-screen instructions.</span></span>

## <a name="create-or-edit-a-unit-of-measure"></a><span data-ttu-id="17854-111">Opprette eller redigere en måleenhet</span><span class="sxs-lookup"><span data-stu-id="17854-111">Create or edit a unit of measure</span></span>

<span data-ttu-id="17854-112">Følg denne fremgangsmåten for å opprette eller redigere en måleenhet.</span><span class="sxs-lookup"><span data-stu-id="17854-112">To create or edit a unit of measure, follow these steps.</span></span>

1. <span data-ttu-id="17854-113">Følg ett av disse trinnene:</span><span class="sxs-lookup"><span data-stu-id="17854-113">Follow one of these steps:</span></span>

    - <span data-ttu-id="17854-114">Hvis du vil redigere en eksisterende enhet, velger du den i listeruten.</span><span class="sxs-lookup"><span data-stu-id="17854-114">To edit an existing unit, select it in the list pane.</span></span>
    - <span data-ttu-id="17854-115">For å opprette en ny enhet velger du **Ny** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="17854-115">To create a new unit, select **New** on the Action Pane.</span></span>

1. <span data-ttu-id="17854-116">I toppteksten for den nye posten angir du følgende felt:</span><span class="sxs-lookup"><span data-stu-id="17854-116">On the header of the record, set the following fields:</span></span>

    - <span data-ttu-id="17854-117">**Enhet** – Angi IDen eller symbolet som skal brukes for å referere til enheten på systemspråket.</span><span class="sxs-lookup"><span data-stu-id="17854-117">**Unit** – Enter the ID or symbol to use to refer to the unit in the system language.</span></span> <span data-ttu-id="17854-118">IDen eller symbolet er vanligvis en felles forkortelse for enheten, for eksempel *hv* for hver eller *cm* for centimeter.</span><span class="sxs-lookup"><span data-stu-id="17854-118">This ID or symbol is usually a common abbreviation for the unit, such as *ea* for each or *cm* for centimeter.</span></span>
    - <span data-ttu-id="17854-119">**Beskrivelse** – Angi et beskrivende navn for måleenheten på systemspråket.</span><span class="sxs-lookup"><span data-stu-id="17854-119">**Description** – Enter a descriptive name for the unit in the system language.</span></span> <span data-ttu-id="17854-120">Dette navnet er vanligvis hele navnet på enheten, for eksempel *Hver* eller *Centimeter*.</span><span class="sxs-lookup"><span data-stu-id="17854-120">This name is usually the full name of the unit, such as *Each* or *Centimeter*.</span></span>

1. <span data-ttu-id="17854-121">Angi følgende felt i hurtigfanen **Generelt**:</span><span class="sxs-lookup"><span data-stu-id="17854-121">On the **General** FastTab, set the following fields:</span></span><!-- KFM: confirm this:    - **Fixed unit assignment** and **Fixed unit** – These fields have an effect only if you're using the Microsoft Retail Essentials product. If the current unit can be mapped to one of the fixed units that are used by Retail Essentials, set the **Fixed unit assignment** option to *Yes*. Then select the fixed unit in the **Fixed unit** field. -->

    - <span data-ttu-id="17854-122">**Enhetsklasse** – Velg egenskapen som enheten måler (for eksempel lengde, område, masse eller antall).</span><span class="sxs-lookup"><span data-stu-id="17854-122">**Unit class** – Select the property that the unit measures (such as length, area, mass, or quantity).</span></span>
    - <span data-ttu-id="17854-123">**Enhetssystem** – Velg målingssystemet som enheten tilhører (*Metriske enheter* eller *Amerikanske måleenheter*).</span><span class="sxs-lookup"><span data-stu-id="17854-123">**System of units** – Select the measurement system that the unit belongs to (*Metric units* or *United States customary units*).</span></span>
    - <span data-ttu-id="17854-124">**Basisenhet** – Sett dette alternativet til *Ja* for å bruke gjeldende enhet som basisenhet for enhetsklassen.</span><span class="sxs-lookup"><span data-stu-id="17854-124">**Base unit** – Set this option to *Yes* to use the current unit as the base unit for its unit class.</span></span> <span data-ttu-id="17854-125">I dette tilfellet må du bare angi omregningsfaktoren mellom basisenheten og hver tilleggsenhet i enhetsklassen.</span><span class="sxs-lookup"><span data-stu-id="17854-125">In this case, you only have to specify the conversion factor between the base unit and each additional unit in the unit class.</span></span> <span data-ttu-id="17854-126">Systemet kan deretter konvertere mellom alle enheter i denne enhetsklassen.</span><span class="sxs-lookup"><span data-stu-id="17854-126">The system can then convert between all units in that unit class.</span></span> <span data-ttu-id="17854-127">Det er derfor enklere å konfigurere konverteringer.</span><span class="sxs-lookup"><span data-stu-id="17854-127">Therefore, it's easier to set up conversions.</span></span>

        <span data-ttu-id="17854-128">Hvis for eksempel gallon er basisenheten for *Volum*-enhetsklassen, trenger du bare å angi omregningsfaktorer fra quart til gallon og fra pint til gallon.</span><span class="sxs-lookup"><span data-stu-id="17854-128">For example, if gallon is the base unit for the *Volume* unit class, you only have to set up conversion factors from quart to gallon and from pint to gallon.</span></span> <span data-ttu-id="17854-129">Systemet kan deretter også konvertere fra quart til pint.</span><span class="sxs-lookup"><span data-stu-id="17854-129">The system can then also convert from quart to pint.</span></span>

        <span data-ttu-id="17854-130">Du kan bare ha én basisenhet per enhetsklasse.</span><span class="sxs-lookup"><span data-stu-id="17854-130">You can have only one base unit per unit class.</span></span>

    - <span data-ttu-id="17854-131">**Systemenhet** – Sett dette alternativet til *Ja* for å bruke gjeldende enhet som antatt enhet for alle uspesifiserte målinger i enhetsklassen.</span><span class="sxs-lookup"><span data-stu-id="17854-131">**System unit** – Set this option to *Yes* to use the current unit as the assumed unit for all unspecified measurements in its unit class.</span></span> <span data-ttu-id="17854-132">Hvis for eksempel et felt som brukes til å angi et antall, ikke tillater at det angis en enhet (hvis brukeren ikke velger en enhet), bruker systemet enheten som er angitt som systemenhet for *Antall*-enhetsklassen.</span><span class="sxs-lookup"><span data-stu-id="17854-132">For example, if a field that is used to enter a quantity doesn't allow a unit to be specified (of if the user doesn't select a unit), the system uses the unit that is set as the system unit for the *Quantity* unit class.</span></span> <span data-ttu-id="17854-133">Du kan bare ha én systemenhet per enhetsklasse.</span><span class="sxs-lookup"><span data-stu-id="17854-133">You can have only one system unit per unit class.</span></span>
    - <span data-ttu-id="17854-134">**Desimalpresisjon** – Angi antall desimaler som verdier som er angitt for den gjeldende enheten eller konverteres til den, skal avrundes til.</span><span class="sxs-lookup"><span data-stu-id="17854-134">**Decimal precision** – Specify the number of decimal places that values that are specified for the current unit or converted to it should be rounded to.</span></span>

1. <span data-ttu-id="17854-135">Velg **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="17854-135">On the Action Pane, select **Save**.</span></span>

## <a name="define-unit-translations"></a><span data-ttu-id="17854-136">Definer enhetsoversettelser</span><span class="sxs-lookup"><span data-stu-id="17854-136">Define unit translations</span></span>

<span data-ttu-id="17854-137">Følg denne fremgangsmåten for å definere oversettelser for IDen eller symbolet og beskrivelsen av en måleenhet.</span><span class="sxs-lookup"><span data-stu-id="17854-137">To define translations for the ID or symbol and the description for a unit of measure, follow these steps.</span></span>

1. <span data-ttu-id="17854-138">Opprett eller velg enheten du vil opprette oversettelser for.</span><span class="sxs-lookup"><span data-stu-id="17854-138">Create or select the unit to create translations for.</span></span>
1. <span data-ttu-id="17854-139">I handlingsruten velger du **Enhetstekster**.</span><span class="sxs-lookup"><span data-stu-id="17854-139">On the Action Pane, select **Unit texts**.</span></span>

    <span data-ttu-id="17854-140">Siden **Enhetstekster** vises.</span><span class="sxs-lookup"><span data-stu-id="17854-140">The **Unit texts** page appears.</span></span> <span data-ttu-id="17854-141">Du bruker denne siden til å definere oversettelser for IDen eller symbolet for den valgte enheten.</span><span class="sxs-lookup"><span data-stu-id="17854-141">You use this page to define translations for the ID or symbol for the selected unit.</span></span> <span data-ttu-id="17854-142">Disse oversettelsene kan deretter brukes på eksterne dokumenter på kundespesifikke eller leverandørspesifikke språk.</span><span class="sxs-lookup"><span data-stu-id="17854-142">Those translations can then be used on external documents in customer-specific or vendor-specific languages.</span></span>

1. <span data-ttu-id="17854-143">Velg **Ny** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="17854-143">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="17854-144">I **Språk**-feltet velger du språket som enhets-IDen eller symbolet skal oversettes til.</span><span class="sxs-lookup"><span data-stu-id="17854-144">In the **Language** field, select the language to translate the unit ID or symbol to.</span></span>
1. <span data-ttu-id="17854-145">I **Tekst**-feltet angir du oversettelsen av enhets-IDen eller symbolet på det valgte språket.</span><span class="sxs-lookup"><span data-stu-id="17854-145">In the **Text** field, enter the translation of the unit ID or symbol in the selected language.</span></span>
1. <span data-ttu-id="17854-146">Velg **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="17854-146">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="17854-147">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="17854-147">Close the page.</span></span>
1. <span data-ttu-id="17854-148">Gå til **Handlingsrute**, velg **Oversatte enhetsbeskrivelser**.</span><span class="sxs-lookup"><span data-stu-id="17854-148">On the **Action Pane**, select **Translated unit descriptions**.</span></span>

    <span data-ttu-id="17854-149">Siden **Oversatte enhetsbeskrivelser** vises.</span><span class="sxs-lookup"><span data-stu-id="17854-149">The **Translated unit descriptions** page appears.</span></span> <span data-ttu-id="17854-150">Du bruker denne siden til å definere språkspesifikke beskrivelser for den valgte enheten.</span><span class="sxs-lookup"><span data-stu-id="17854-150">You use this page to define language-specific descriptions for the selected unit.</span></span>

1. <span data-ttu-id="17854-151">Velg **Ny** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="17854-151">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="17854-152">I **Språk**-feltet velger du språket som enhetsbeskrivelsen skal oversettes til.</span><span class="sxs-lookup"><span data-stu-id="17854-152">In the **Language** field, select the language to translate the unit description to.</span></span>
1. <span data-ttu-id="17854-153">I **Beskrivelse**-feltet angir du oversettelsen av enhetsbeskrivelsen på det valgte språket.</span><span class="sxs-lookup"><span data-stu-id="17854-153">In the **Description** field, enter the translation of the unit description in the selected language.</span></span>
1. <span data-ttu-id="17854-154">Velg **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="17854-154">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="17854-155">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="17854-155">Close the page.</span></span>

## <a name="define-unit-conversion-rules"></a><span data-ttu-id="17854-156">Definer enhetsomregningsregler</span><span class="sxs-lookup"><span data-stu-id="17854-156">Define unit conversion rules</span></span>

<span data-ttu-id="17854-157">Følg denne fremgangsmåten for å definere regler for omregninger mellom måleenheter.</span><span class="sxs-lookup"><span data-stu-id="17854-157">To define rules for conversions between units of measure, follow these steps.</span></span>

1. <span data-ttu-id="17854-158">Opprett eller velg enheten du vil definere omregningsregler for.</span><span class="sxs-lookup"><span data-stu-id="17854-158">Create or select the unit to define conversion rules for.</span></span>
1. <span data-ttu-id="17854-159">I handlingsruten velger du **Enhetskonverteringer**.</span><span class="sxs-lookup"><span data-stu-id="17854-159">On the Action Pane, select **Unit conversions**.</span></span>

    <span data-ttu-id="17854-160">Siden **Enhetskonverteringer** vises.</span><span class="sxs-lookup"><span data-stu-id="17854-160">The **Unit conversions** page appears.</span></span> <span data-ttu-id="17854-161">Du kan bruke denne siden til å definere regler for å konvertere måleenheten til og fra andre enheter i den valgte enhetsklassen.</span><span class="sxs-lookup"><span data-stu-id="17854-161">You use this page to define rules for converting the selected unit to and from other units in the unit class.</span></span>

1. <span data-ttu-id="17854-162">Velg én av følgende kategorier, avhengig av hvilken type konvertering du vil definere:</span><span class="sxs-lookup"><span data-stu-id="17854-162">Select one of the following tabs, depending on the type of conversion that you want to set up:</span></span>

    - <span data-ttu-id="17854-163">**Standardkonverteringer** – Definer standard konverteringsregler for alle produkter.</span><span class="sxs-lookup"><span data-stu-id="17854-163">**Standard conversions** – Set up standard conversion rules for all products.</span></span>
    - <span data-ttu-id="17854-164">**Klasseinterne konverteringer** – Definer produktspesifikke omregningsregler for enheter i samme enhetsklasse.</span><span class="sxs-lookup"><span data-stu-id="17854-164">**Intra-class conversions** – Set up product-specific conversion rules for units in the same unit class.</span></span>
    - <span data-ttu-id="17854-165">**Mellomklassekonverteringer** – Definer produktspesifikke omregningsregler for enheter på tvers av enhetsklasser.</span><span class="sxs-lookup"><span data-stu-id="17854-165">**Inter-class conversions** – Set up product-specific conversion rules for units across unit classes.</span></span>

1. <span data-ttu-id="17854-166">Følg ett av disse trinnene:</span><span class="sxs-lookup"><span data-stu-id="17854-166">Follow one of these steps:</span></span>

    - <span data-ttu-id="17854-167">For å opprette en ny konvertering velger du **Ny** på verktøylinjen.</span><span class="sxs-lookup"><span data-stu-id="17854-167">To create a new conversion, select **New** on the toolbar.</span></span>
    - <span data-ttu-id="17854-168">Hvis du vil redigere en eksisterende konvertering, velger du konverteringen i rutenettet og velger deretter **Rediger** på verktøylinjen.</span><span class="sxs-lookup"><span data-stu-id="17854-168">To edit an existing conversion, select the conversion in the grid, and then select **Edit** on the toolbar.</span></span>

1. <span data-ttu-id="17854-169">I rullegardinboksen som vises, angir du følgende felt:</span><span class="sxs-lookup"><span data-stu-id="17854-169">In the drop-down dialog box that appears, set the following fields:</span></span>

    - <span data-ttu-id="17854-170">**Produkt** – Velg det spesifikke produktet som omregningen gjelder.</span><span class="sxs-lookup"><span data-stu-id="17854-170">**Product** – Select the specific product that the conversion applies to.</span></span> <span data-ttu-id="17854-171">Dette feltet er bare tilgjengelig for klasseinterne konverteringer og mellomklassekonverteringer.</span><span class="sxs-lookup"><span data-stu-id="17854-171">This field is available only for intra-class and inter-class conversions.</span></span>
    - <span data-ttu-id="17854-172">**Formeloppsett** – La dette feltet være satt til *Enkel* for å angi en enkel konvertering som har én enkelt faktor.</span><span class="sxs-lookup"><span data-stu-id="17854-172">**Formula layout** – Leave this field set to *Simple* to specify a simple conversion that has a single factor.</span></span> <span data-ttu-id="17854-173">Sett den til *Avansert* for å definere en mer kompleks ligning.</span><span class="sxs-lookup"><span data-stu-id="17854-173">Set it to *Advanced* to set up a more complex equation.</span></span> <span data-ttu-id="17854-174">Formatet for avanserte ligninger varierer, avhengig av enhetsklassen.</span><span class="sxs-lookup"><span data-stu-id="17854-174">The format for advanced equations varies, depending on the unit class.</span></span>
    - <span data-ttu-id="17854-175">**Fra enhet** – Dette feltet viser den valgte enheten.</span><span class="sxs-lookup"><span data-stu-id="17854-175">**From unit** – This field shows the selected unit.</span></span> <span data-ttu-id="17854-176">Vanligvis bør du ikke endre verdien.</span><span class="sxs-lookup"><span data-stu-id="17854-176">Usually, you should not change the value.</span></span> <span data-ttu-id="17854-177">(Hvis du endrer verdien, må du åpne siden **Enhetsomregninger** for den valgte enheten for å vise den nye omregningen etter at du har lagret den.)</span><span class="sxs-lookup"><span data-stu-id="17854-177">(If you do change the value, you must open the **Unit conversions** page for the selected unit to view your new conversion after you save it.)</span></span>
    - <span data-ttu-id="17854-178">**Til enhet** – Velg enheten du vil konvertere til.</span><span class="sxs-lookup"><span data-stu-id="17854-178">**To unit** – Select the unit to convert to.</span></span>
    - <span data-ttu-id="17854-179">**Avrunding** – Velg hvordan brøker skal avrundes basert på **Desimalpresisjon**-verdien til den valgte enheten (*Til nærmeste*, *Opp* eller *Ned*).</span><span class="sxs-lookup"><span data-stu-id="17854-179">**Rounding** – Select how fractions should be rounded, based on the **Decimal precision** value of the selected unit (*To nearest*, *Up*, or *Down*).</span></span>
    - <span data-ttu-id="17854-180">**Konverteringsformel** – Bruk de gjenværende feltene øverst i rullegardinlisten til å angi formelen for omregning mellom de to enhetene.</span><span class="sxs-lookup"><span data-stu-id="17854-180">**Conversion formula** – Use the remaining fields at the top of the drop-down dialog box to specify the formula for converting between the two units.</span></span> <span data-ttu-id="17854-181">De tilgjengelige feltene varierer avhengig av enhetsklassen og formeloppsettet du har valgt.</span><span class="sxs-lookup"><span data-stu-id="17854-181">The available fields vary, depending on the unit class and formula layout that you've selected.</span></span>

1. <span data-ttu-id="17854-182">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="17854-182">Select **OK**.</span></span>
1. <span data-ttu-id="17854-183">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="17854-183">Close the page.</span></span>

> [!TIP]
> <span data-ttu-id="17854-184">Du kan også definere enhetsomregninger per produktvariant.</span><span class="sxs-lookup"><span data-stu-id="17854-184">You can also set up unit conversions per product variant.</span></span> <span data-ttu-id="17854-185">Hvis du vil ha mer informasjon, kan du se [Konvertering av måleenhet per produktvariant](../uom-conversion-per-product-variant.md).</span><span class="sxs-lookup"><span data-stu-id="17854-185">For more information, see [Unit of measure conversion per product variant](../uom-conversion-per-product-variant.md).</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
