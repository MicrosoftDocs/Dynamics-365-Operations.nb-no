---
title: Kvalitetsstyringstester
description: Dette emnet beskriver hvordan du oppretter tester som kan brukes for kvalitetsordrer i Microsoft Dynamics 365 Supply Chain Management.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 95f759d051a520b577cb1cf3d595ce64e0dc4668
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021690"
---
# <a name="quality-management-tests"></a><span data-ttu-id="5beae-103">Kvalitetsstyringstester</span><span class="sxs-lookup"><span data-stu-id="5beae-103">Quality management tests</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5beae-104">Dette emnet beskriver hvordan du oppretter tester som kan brukes for kvalitetsordrer i Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="5beae-104">This topic describes how to create tests that can be used for quality orders in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="5beae-105">Du bruker **Tester**-siden til å definere og vise de individuelle testene som fastslår om produktene oppfyller kvalitetsspesifikasjoner.</span><span class="sxs-lookup"><span data-stu-id="5beae-105">You use the **Tests** page to define and view the individual tests that determine whether your products meet quality specifications.</span></span> <span data-ttu-id="5beae-106">Du kan tilordne én eller flere individuelle tester til en testgruppe.</span><span class="sxs-lookup"><span data-stu-id="5beae-106">You can assign one or more individual tests to a test group.</span></span> <span data-ttu-id="5beae-107">I dette tilfellet må også angi testspesifikk informasjon, for eksempel de akseptable målingsverdiene.</span><span class="sxs-lookup"><span data-stu-id="5beae-107">In this case, you also specify test-specific information, such as the acceptable measurement values.</span></span> <span data-ttu-id="5beae-108">Målingsverdier brukes for kvantitative tester.</span><span class="sxs-lookup"><span data-stu-id="5beae-108">Measurement values are used for quantitative tests.</span></span> <span data-ttu-id="5beae-109">For kvalitative tester brukes testvariabler.</span><span class="sxs-lookup"><span data-stu-id="5beae-109">For qualitative tests, test variables are used.</span></span>

- <span data-ttu-id="5beae-110">For kvantitative tester er **Type**-feltet satt til *Heltall* eller *Brøk*.</span><span class="sxs-lookup"><span data-stu-id="5beae-110">For quantitative tests, the **Type** field is set to *Integer* or *Fraction*.</span></span> <span data-ttu-id="5beae-111">En måleenhet er også angitt.</span><span class="sxs-lookup"><span data-stu-id="5beae-111">A unit of measure is also specified.</span></span> <span data-ttu-id="5beae-112">Kvalitetsspesifikasjoner og testresultater uttrykkes som tall.</span><span class="sxs-lookup"><span data-stu-id="5beae-112">Quality specifications and test results are expressed as numbers.</span></span>
- <span data-ttu-id="5beae-113">For kvalitative tester er **Type**-feltet satt til *Alternativ*.</span><span class="sxs-lookup"><span data-stu-id="5beae-113">For qualitative tests, the **Type** field is set to *Option*.</span></span> <span data-ttu-id="5beae-114">Kvalitative tester krever mer informasjon om testvariabelen som måles, og de tilhørende opplistede alternativene.</span><span class="sxs-lookup"><span data-stu-id="5beae-114">Qualitative tests require additional information about the test variable that is being measured and its enumerated options.</span></span> <span data-ttu-id="5beae-115">Kvalitetsspesifikasjoner og testresultater uttrykkes i henhold til et resultat.</span><span class="sxs-lookup"><span data-stu-id="5beae-115">Quality specifications and test results are expressed according to an outcome.</span></span>

<span data-ttu-id="5beae-116">Du kan også tilordne et testinstrument til en test.</span><span class="sxs-lookup"><span data-stu-id="5beae-116">You can optionally assign a test instrument to a test.</span></span> <span data-ttu-id="5beae-117">Testinstrumenter kreves imidlertid ikke for å opprette og bruke tester med kvalitetsordrer.</span><span class="sxs-lookup"><span data-stu-id="5beae-117">However, test instruments aren't required to create and use tests with quality orders.</span></span> <span data-ttu-id="5beae-118">Hvis du vil ha mer informasjon, kan du se [Testinstrumenter for kvalitetsstyring](quality-test-instruments.md).</span><span class="sxs-lookup"><span data-stu-id="5beae-118">For more information, see [Quality management test instruments](quality-test-instruments.md).</span></span>

<span data-ttu-id="5beae-119">Du kan også velge å angi en enhet for en test for å angi måleenheten som testresultatene registreres i.</span><span class="sxs-lookup"><span data-stu-id="5beae-119">You can also optionally specify a unit for a test, to indicate the unit of measure that test results are recorded in.</span></span> <span data-ttu-id="5beae-120">En test for temperatur kan for eksempel inneholde en enhet på enten grader Fahrenheit eller grader Celsius.</span><span class="sxs-lookup"><span data-stu-id="5beae-120">For example, a test for temperature might include a unit of either degrees Fahrenheit or degrees Celsius.</span></span>

## <a name="example-of-a-test"></a><span data-ttu-id="5beae-121">Eksempel på en test</span><span class="sxs-lookup"><span data-stu-id="5beae-121">Example of a test</span></span>

<span data-ttu-id="5beae-122">Et produksjonsfirma utfører to tester på innkjøpt materiale: en kvantitativ test for materialkvalitet og en kvalitativ test for emballasjeskade.</span><span class="sxs-lookup"><span data-stu-id="5beae-122">A manufacturing company performs two tests on purchased material: a quantitative test for material quality and a qualitative test for packaging damage.</span></span> <span data-ttu-id="5beae-123">Firmaet angir tilleggsinformasjon om den kvalitative testen for å definere testvariabelen (for eksempel skadet emballasje) og resultatene.</span><span class="sxs-lookup"><span data-stu-id="5beae-123">The company specifies additional information about the qualitative test to define the test variable (for example, damaged packaging) and its outcomes.</span></span> <span data-ttu-id="5beae-124">Firmaet bruker **Testgrupper**-siden til å tilordne de to testene til en testgruppe og angi testspesifikk informasjon.</span><span class="sxs-lookup"><span data-stu-id="5beae-124">The company uses the **Test groups** page to assign the two tests to a test group and to specify the test-specific information.</span></span> <span data-ttu-id="5beae-125">Testgruppen tilordnes til en kvalitetsordre, slik at firmaet kan rapportere testresultater for de to testene.</span><span class="sxs-lookup"><span data-stu-id="5beae-125">The test group is assigned to a quality order so that the company can report test results for the two tests.</span></span>

## <a name="create-a-test"></a><span data-ttu-id="5beae-126">Opprette en test</span><span class="sxs-lookup"><span data-stu-id="5beae-126">Create a test</span></span>

<span data-ttu-id="5beae-127">Følg trinnene nedenfor for å opprette en test.</span><span class="sxs-lookup"><span data-stu-id="5beae-127">Follow these steps to create a test.</span></span>

1. <span data-ttu-id="5beae-128">Gå til **Lagerstyring \> Oppsett \> Kvalitetskontroll \> Tester**.</span><span class="sxs-lookup"><span data-stu-id="5beae-128">Go to **Inventory management \> Setup \> Quality control \> Tests**.</span></span>
1. <span data-ttu-id="5beae-129">I handlingsruten velger du **Ny** for å legge til en rad i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="5beae-129">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="5beae-130">Angi deretter følgende felter for den nye raden:</span><span class="sxs-lookup"><span data-stu-id="5beae-130">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="5beae-131">**Test** – Angi en unik ID eller et unikt navn for testen.</span><span class="sxs-lookup"><span data-stu-id="5beae-131">**Test** – Enter a unique ID or name for the test.</span></span>
    - <span data-ttu-id="5beae-132">**Beskrivelse** – Angi en detaljert beskrivelse av testen.</span><span class="sxs-lookup"><span data-stu-id="5beae-132">**Description** – Enter a detailed description of the test.</span></span>
    - <span data-ttu-id="5beae-133">**Type** – Velg typen resultater som testen produserer.</span><span class="sxs-lookup"><span data-stu-id="5beae-133">**Type** – Select the type of results that the test produces.</span></span> <span data-ttu-id="5beae-134">Velg *Brøk* eller *Heltall* for kvantitative tester.</span><span class="sxs-lookup"><span data-stu-id="5beae-134">For quantitative tests, select *Fraction* or *Integer*.</span></span> <span data-ttu-id="5beae-135">Velg *Alternativ* for kvalitative tester.</span><span class="sxs-lookup"><span data-stu-id="5beae-135">For qualitative tests, select *Option*.</span></span>
    - <span data-ttu-id="5beae-136">**Testinstrument** – Velg et [testinstrument](quality-test-instruments.md) som skal brukes for testen.</span><span class="sxs-lookup"><span data-stu-id="5beae-136">**Test instrument** – Select a [test instrument](quality-test-instruments.md) that should be used for the test.</span></span>
    - <span data-ttu-id="5beae-137">**Enhet** – Hvis du valgte *Brøk* eller *Heltall* i **Type**-feltet (det vil si hvis testen er en kvantitativ test), velger du måleenheten som testresultatene skal registreres i.</span><span class="sxs-lookup"><span data-stu-id="5beae-137">**Unit** – If you selected *Fraction* or *Integer* in the **Type** field (that is, if the test is a quantitative test), select the unit of measure that test results should be recorded in.</span></span>

1. <span data-ttu-id="5beae-138">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="5beae-138">Close the page.</span></span>

> [!NOTE]
> <span data-ttu-id="5beae-139">Etter at du har lagret en test, kan du ikke lenger redigere **Type**-feltet i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="5beae-139">After you save a test, you can no longer edit the **Type** field in the grid.</span></span> <span data-ttu-id="5beae-140">Hvis du må endre typen testresultat som skal registreres for en test, velger du **Endre type kvalitetstest** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="5beae-140">If you must change the type of test results that will be recorded for a test, select **Change quality test type** on the Action Pane.</span></span> <span data-ttu-id="5beae-141">I dialogboksen **Endre type kvalitetstest** setter du **Ny type**-feltet til ønsket type, og velger deretter **OK** for å lukke dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="5beae-141">In the **Change quality test type** dialog box, set the **New type** field to the desired type, and then select **OK** to close the dialog box.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5beae-142">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="5beae-142">Additional resources</span></span>

- [<span data-ttu-id="5beae-143">Testinstrumenter for kvalitetsstyring</span><span class="sxs-lookup"><span data-stu-id="5beae-143">Quality management test instruments</span></span>](quality-test-instruments.md)
- [<span data-ttu-id="5beae-144">Testgrupper for kvalitetsstyring</span><span class="sxs-lookup"><span data-stu-id="5beae-144">Quality management test groups</span></span>](quality-test-groups.md)
- [<span data-ttu-id="5beae-145">Testvariabler for kvalitetsstyring</span><span class="sxs-lookup"><span data-stu-id="5beae-145">Quality management test variables</span></span>](quality-test-variables.md)
- [<span data-ttu-id="5beae-146">Kvalitetstilknytninger</span><span class="sxs-lookup"><span data-stu-id="5beae-146">Quality associations</span></span>](quality-associations.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
