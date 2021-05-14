---
title: Kvalitetsstyringstester
description: Dette emnet beskriver hvordan du oppretter tester som kan brukes for kvalitetsordrer i Microsoft Dynamics 365 Supply Chain Management.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: b88011f486b6582db4727b85d021868899c6abe1
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956773"
---
# <a name="quality-management-tests"></a><span data-ttu-id="56663-103">Kvalitetsstyringstester</span><span class="sxs-lookup"><span data-stu-id="56663-103">Quality management tests</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="56663-104">Dette emnet beskriver hvordan du oppretter tester som kan brukes for kvalitetsordrer i Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="56663-104">This topic describes how to create tests that can be used for quality orders in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="56663-105">Du bruker **Tester**-siden til å definere og vise de individuelle testene som fastslår om produktene oppfyller kvalitetsspesifikasjoner.</span><span class="sxs-lookup"><span data-stu-id="56663-105">You use the **Tests** page to define and view the individual tests that determine whether your products meet quality specifications.</span></span> <span data-ttu-id="56663-106">Du kan tilordne én eller flere individuelle tester til en testgruppe.</span><span class="sxs-lookup"><span data-stu-id="56663-106">You can assign one or more individual tests to a test group.</span></span> <span data-ttu-id="56663-107">I dette tilfellet må også angi testspesifikk informasjon, for eksempel de akseptable målingsverdiene.</span><span class="sxs-lookup"><span data-stu-id="56663-107">In this case, you also specify test-specific information, such as the acceptable measurement values.</span></span> <span data-ttu-id="56663-108">Målingsverdier brukes for kvantitative tester.</span><span class="sxs-lookup"><span data-stu-id="56663-108">Measurement values are used for quantitative tests.</span></span> <span data-ttu-id="56663-109">For kvalitative tester brukes testvariabler.</span><span class="sxs-lookup"><span data-stu-id="56663-109">For qualitative tests, test variables are used.</span></span>

- <span data-ttu-id="56663-110">For kvantitative tester er **Type**-feltet satt til *Heltall* eller *Brøk*.</span><span class="sxs-lookup"><span data-stu-id="56663-110">For quantitative tests, the **Type** field is set to *Integer* or *Fraction*.</span></span> <span data-ttu-id="56663-111">En måleenhet er også angitt.</span><span class="sxs-lookup"><span data-stu-id="56663-111">A unit of measure is also specified.</span></span> <span data-ttu-id="56663-112">Kvalitetsspesifikasjoner og testresultater uttrykkes som tall.</span><span class="sxs-lookup"><span data-stu-id="56663-112">Quality specifications and test results are expressed as numbers.</span></span>
- <span data-ttu-id="56663-113">For kvalitative tester er **Type**-feltet satt til *Alternativ*.</span><span class="sxs-lookup"><span data-stu-id="56663-113">For qualitative tests, the **Type** field is set to *Option*.</span></span> <span data-ttu-id="56663-114">Kvalitative tester krever mer informasjon om testvariabelen som måles, og de tilhørende opplistede alternativene.</span><span class="sxs-lookup"><span data-stu-id="56663-114">Qualitative tests require additional information about the test variable that is being measured and its enumerated options.</span></span> <span data-ttu-id="56663-115">Kvalitetsspesifikasjoner og testresultater uttrykkes i henhold til et resultat.</span><span class="sxs-lookup"><span data-stu-id="56663-115">Quality specifications and test results are expressed according to an outcome.</span></span>

<span data-ttu-id="56663-116">Du kan også tilordne et testinstrument til en test.</span><span class="sxs-lookup"><span data-stu-id="56663-116">You can optionally assign a test instrument to a test.</span></span> <span data-ttu-id="56663-117">Testinstrumenter kreves imidlertid ikke for å opprette og bruke tester med kvalitetsordrer.</span><span class="sxs-lookup"><span data-stu-id="56663-117">However, test instruments aren't required to create and use tests with quality orders.</span></span> <span data-ttu-id="56663-118">Hvis du vil ha mer informasjon, kan du se [Testinstrumenter for kvalitetsstyring](quality-test-instruments.md).</span><span class="sxs-lookup"><span data-stu-id="56663-118">For more information, see [Quality management test instruments](quality-test-instruments.md).</span></span>

<span data-ttu-id="56663-119">Du kan også velge å angi en enhet for en test for å angi måleenheten som testresultatene registreres i.</span><span class="sxs-lookup"><span data-stu-id="56663-119">You can also optionally specify a unit for a test, to indicate the unit of measure that test results are recorded in.</span></span> <span data-ttu-id="56663-120">En test for temperatur kan for eksempel inneholde en enhet på enten grader Fahrenheit eller grader Celsius.</span><span class="sxs-lookup"><span data-stu-id="56663-120">For example, a test for temperature might include a unit of either degrees Fahrenheit or degrees Celsius.</span></span>

## <a name="example-of-a-test"></a><span data-ttu-id="56663-121">Eksempel på en test</span><span class="sxs-lookup"><span data-stu-id="56663-121">Example of a test</span></span>

<span data-ttu-id="56663-122">Et produksjonsfirma utfører to tester på innkjøpt materiale: en kvantitativ test for materialkvalitet og en kvalitativ test for emballasjeskade.</span><span class="sxs-lookup"><span data-stu-id="56663-122">A manufacturing company performs two tests on purchased material: a quantitative test for material quality and a qualitative test for packaging damage.</span></span> <span data-ttu-id="56663-123">Firmaet angir tilleggsinformasjon om den kvalitative testen for å definere testvariabelen (for eksempel skadet emballasje) og resultatene.</span><span class="sxs-lookup"><span data-stu-id="56663-123">The company specifies additional information about the qualitative test to define the test variable (for example, damaged packaging) and its outcomes.</span></span> <span data-ttu-id="56663-124">Firmaet bruker **Testgrupper**-siden til å tilordne de to testene til en testgruppe og angi testspesifikk informasjon.</span><span class="sxs-lookup"><span data-stu-id="56663-124">The company uses the **Test groups** page to assign the two tests to a test group and to specify the test-specific information.</span></span> <span data-ttu-id="56663-125">Testgruppen tilordnes til en kvalitetsordre, slik at firmaet kan rapportere testresultater for de to testene.</span><span class="sxs-lookup"><span data-stu-id="56663-125">The test group is assigned to a quality order so that the company can report test results for the two tests.</span></span>

## <a name="create-a-test"></a><span data-ttu-id="56663-126">Opprette en test</span><span class="sxs-lookup"><span data-stu-id="56663-126">Create a test</span></span>

<span data-ttu-id="56663-127">Følg trinnene nedenfor for å opprette en test.</span><span class="sxs-lookup"><span data-stu-id="56663-127">Follow these steps to create a test.</span></span>

1. <span data-ttu-id="56663-128">Gå til **Lagerstyring \> Oppsett \> Kvalitetskontroll \> Tester**.</span><span class="sxs-lookup"><span data-stu-id="56663-128">Go to **Inventory management \> Setup \> Quality control \> Tests**.</span></span>
1. <span data-ttu-id="56663-129">I handlingsruten velger du **Ny** for å legge til en rad i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="56663-129">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="56663-130">Angi deretter følgende felter for den nye raden:</span><span class="sxs-lookup"><span data-stu-id="56663-130">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="56663-131">**Test** – Angi en unik ID eller et unikt navn for testen.</span><span class="sxs-lookup"><span data-stu-id="56663-131">**Test** – Enter a unique ID or name for the test.</span></span>
    - <span data-ttu-id="56663-132">**Beskrivelse** – Angi en detaljert beskrivelse av testen.</span><span class="sxs-lookup"><span data-stu-id="56663-132">**Description** – Enter a detailed description of the test.</span></span>
    - <span data-ttu-id="56663-133">**Type** – Velg typen resultater som testen produserer.</span><span class="sxs-lookup"><span data-stu-id="56663-133">**Type** – Select the type of results that the test produces.</span></span> <span data-ttu-id="56663-134">Velg *Brøk* eller *Heltall* for kvantitative tester.</span><span class="sxs-lookup"><span data-stu-id="56663-134">For quantitative tests, select *Fraction* or *Integer*.</span></span> <span data-ttu-id="56663-135">Velg *Alternativ* for kvalitative tester.</span><span class="sxs-lookup"><span data-stu-id="56663-135">For qualitative tests, select *Option*.</span></span>
    - <span data-ttu-id="56663-136">**Testinstrument** – Velg et [testinstrument](quality-test-instruments.md) som skal brukes for testen.</span><span class="sxs-lookup"><span data-stu-id="56663-136">**Test instrument** – Select a [test instrument](quality-test-instruments.md) that should be used for the test.</span></span>
    - <span data-ttu-id="56663-137">**Enhet** – Hvis du valgte *Brøk* eller *Heltall* i **Type**-feltet (det vil si hvis testen er en kvantitativ test), velger du måleenheten som testresultatene skal registreres i.</span><span class="sxs-lookup"><span data-stu-id="56663-137">**Unit** – If you selected *Fraction* or *Integer* in the **Type** field (that is, if the test is a quantitative test), select the unit of measure that test results should be recorded in.</span></span>

1. <span data-ttu-id="56663-138">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="56663-138">Close the page.</span></span>

> [!NOTE]
> <span data-ttu-id="56663-139">Etter at du har lagret en test, kan du ikke lenger redigere **Type**-feltet i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="56663-139">After you save a test, you can no longer edit the **Type** field in the grid.</span></span> <span data-ttu-id="56663-140">Hvis du må endre typen testresultat som skal registreres for en test, velger du **Endre type kvalitetstest** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="56663-140">If you must change the type of test results that will be recorded for a test, select **Change quality test type** on the Action Pane.</span></span> <span data-ttu-id="56663-141">I dialogboksen **Endre type kvalitetstest** setter du **Ny type**-feltet til ønsket type, og velger deretter **OK** for å lukke dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="56663-141">In the **Change quality test type** dialog box, set the **New type** field to the desired type, and then select **OK** to close the dialog box.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="56663-142">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="56663-142">Additional resources</span></span>

- [<span data-ttu-id="56663-143">Testinstrumenter for kvalitetsstyring</span><span class="sxs-lookup"><span data-stu-id="56663-143">Quality management test instruments</span></span>](quality-test-instruments.md)
- [<span data-ttu-id="56663-144">Testgrupper for kvalitetsstyring</span><span class="sxs-lookup"><span data-stu-id="56663-144">Quality management test groups</span></span>](quality-test-groups.md)
- [<span data-ttu-id="56663-145">Testvariabler for kvalitetsstyring</span><span class="sxs-lookup"><span data-stu-id="56663-145">Quality management test variables</span></span>](quality-test-variables.md)
- [<span data-ttu-id="56663-146">Kvalitetstilknytninger</span><span class="sxs-lookup"><span data-stu-id="56663-146">Quality associations</span></span>](quality-associations.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
