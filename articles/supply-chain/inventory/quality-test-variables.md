---
title: Testvariabler for kvalitetsstyring
description: Dette emnet beskriver hvordan du oppretter testvariabler som kan brukes for kvalitative tester på kvalitetsordrer i Microsoft Dynamics 365 Supply Chain Management.
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
ms.openlocfilehash: b5102d09f5762a390d6fd3aadafcb2ed23820982
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021714"
---
# <a name="quality-management-test-variables"></a><span data-ttu-id="19d12-103">Testvariabler for kvalitetsstyring</span><span class="sxs-lookup"><span data-stu-id="19d12-103">Quality management test variables</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="19d12-104">Dette emnet beskriver hvordan du oppretter testvariabler som kan brukes for kvalitative tester på kvalitetsordrer i Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="19d12-104">This topic describes how to create test variables that can be used for qualitative tests on quality orders in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="19d12-105">Du må definere en testvariabel og mulige resultater for hver kvalitative test som defineres på siden **Tester**.</span><span class="sxs-lookup"><span data-stu-id="19d12-105">For every qualitative test that is defined on the **Tests** page, you must define a test variable and its possible outcomes (results).</span></span> <span data-ttu-id="19d12-106">(For kvalitative tester er **Type**-feltet på **Tester**-siden satt til *Alternativ*.)</span><span class="sxs-lookup"><span data-stu-id="19d12-106">(For qualitative tests, the **Type** field on the **Tests** page is set to *Option*.)</span></span>

<span data-ttu-id="19d12-107">Du kan bruke **Testvariabler**-siden til å definere, redigere og vise de mulige resultatene for en testvariabel som er knyttet til en kvalitativ test.</span><span class="sxs-lookup"><span data-stu-id="19d12-107">You use the **Test variables** page to set up, edit, and view the possible outcomes for a test variable that is associated with a qualitative test.</span></span> <span data-ttu-id="19d12-108">For hvert resultat tilordner du resultatstatusen til enten *Bestått* eller *Mislykket* for å angi om testen er bestått eller mislyktes når dette resultatet er valgt som et testresult.</span><span class="sxs-lookup"><span data-stu-id="19d12-108">For each outcome, you assign an outcome status of either *Pass* or *Fail* to indicate whether the test is passed or failed when that outcome is selected as a test result.</span></span> <span data-ttu-id="19d12-109">Bruk siden **Testgrupper** for å tilordne en testvariabel og et standardresultat for den til en enkelt kvalitetstest.</span><span class="sxs-lookup"><span data-stu-id="19d12-109">You use the **Test groups** page to assign a test variable and a default outcome for it to an individual qualitative test.</span></span>

<span data-ttu-id="19d12-110">For hver testvariabel anbefaler vi at du definerer minst to resultater: ett som har resultatstatusen *Bestått*, og ett som har resultatstatusen *Mislykket*.</span><span class="sxs-lookup"><span data-stu-id="19d12-110">For every test variable, we recommend that you define at least two outcomes: one that has an outcome status of *Pass* and one that has an outcome status of *Fail*.</span></span> <span data-ttu-id="19d12-111">Det er ingen grense for totalt antall variabler eller resultater som kan defineres.</span><span class="sxs-lookup"><span data-stu-id="19d12-111">There is no limit on the total number of variables or outcomes that can be defined.</span></span> <span data-ttu-id="19d12-112">I tillegg kan flere tester bruke de samme testvariablene til å registrere resultater.</span><span class="sxs-lookup"><span data-stu-id="19d12-112">Additionally, multiple tests can use the same test variables to record results.</span></span>

## <a name="examples-of-test-variables"></a><span data-ttu-id="19d12-113">Eksempler på testvariabler</span><span class="sxs-lookup"><span data-stu-id="19d12-113">Examples of test variables</span></span>

### <a name="example-1"></a><span data-ttu-id="19d12-114">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="19d12-114">Example 1</span></span>

<span data-ttu-id="19d12-115">Et produksjonsfirma utfører to tester på produserte materialer.</span><span class="sxs-lookup"><span data-stu-id="19d12-115">A manufacturing company performs two tests on manufactured materials.</span></span> <span data-ttu-id="19d12-116">I en test er pH-nivået knyttet til en fargestripe.</span><span class="sxs-lookup"><span data-stu-id="19d12-116">In one test, the pH level is associated with a color strip.</span></span> <span data-ttu-id="19d12-117">Akseptable pH-nivåer er i lysere farger, og uakseptabelt pH-nivåer er i mørkere farger.</span><span class="sxs-lookup"><span data-stu-id="19d12-117">Acceptable pH levels are in lighter colors, and unacceptable pH levels are in darker colors.</span></span> <span data-ttu-id="19d12-118">I en annen test utføres det flere visuelle inspeksjoner, og kvalitetsarbeidere bruker sitt skjønn for å fastslå om varen består eller feiler den visuelle inspeksjonen.</span><span class="sxs-lookup"><span data-stu-id="19d12-118">In another test, multiple visual inspections are performed, and quality workers use their judgement to determine whether the item passes or fails the visual inspection.</span></span>

### <a name="example-2"></a><span data-ttu-id="19d12-119">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="19d12-119">Example 2</span></span>

<span data-ttu-id="19d12-120">En produksjonsfirma som produserer kjeks, bruker en inspeksjonstest til det ferdige produktet.</span><span class="sxs-lookup"><span data-stu-id="19d12-120">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="19d12-121">Denne inspeksjonstesten har flere variabler.</span><span class="sxs-lookup"><span data-stu-id="19d12-121">This inspection test has several variables.</span></span> <span data-ttu-id="19d12-122">Én variabel er smak, og de mulige resultatene for den er god og dårlig.</span><span class="sxs-lookup"><span data-stu-id="19d12-122">One variable is taste, and the possible outcomes for it are good and bad.</span></span> <span data-ttu-id="19d12-123">En annen variabel er farge, og de mulige resultatene for den er for mørk, for lys og riktig.</span><span class="sxs-lookup"><span data-stu-id="19d12-123">A second variable is color, and the possible outcomes for it are too dark, too light, and correct.</span></span>

## <a name="create-a-test-variable"></a><span data-ttu-id="19d12-124">Opprette en testvariabel</span><span class="sxs-lookup"><span data-stu-id="19d12-124">Create a test variable</span></span>

<span data-ttu-id="19d12-125">Hvis du vil opprette en testvariabel, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="19d12-125">Follow these steps to create a test variable.</span></span>

1. <span data-ttu-id="19d12-126">Gå til **Lagerstyring \> Oppsett \> Kvalitetskontroll \> Testvariabler**.</span><span class="sxs-lookup"><span data-stu-id="19d12-126">Go to **Inventory management \> Setup \> Quality control \> Test variables**.</span></span>
1. <span data-ttu-id="19d12-127">I handlingsruten velger du **Ny** for å legge til en rad i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="19d12-127">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="19d12-128">Angi deretter følgende felter for den nye raden:</span><span class="sxs-lookup"><span data-stu-id="19d12-128">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="19d12-129">**Variabel** – Angi en unik ID eller et unikt navn for variabelen.</span><span class="sxs-lookup"><span data-stu-id="19d12-129">**Variable** – Enter a unique ID or name for the variable.</span></span>
    - <span data-ttu-id="19d12-130">**Beskrivelse** – Angi en detaljert beskrivelse av variabelen.</span><span class="sxs-lookup"><span data-stu-id="19d12-130">**Description** – Enter a detailed description of the variable.</span></span>

1. <span data-ttu-id="19d12-131">Mens den nye raden fremdeles er valgt, velger du **Resultater** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="19d12-131">While the new row is still selected, select **Outcomes** on the Action Pane.</span></span>
1. <span data-ttu-id="19d12-132">Velg **Ny** i handlingsruten på siden **Testvariabelresultater** for å legge til en rad i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="19d12-132">On the **Test variable outcomes** page, on the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="19d12-133">Angi deretter følgende felter for den nye raden:</span><span class="sxs-lookup"><span data-stu-id="19d12-133">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="19d12-134">**Resultat** – Angi en unik ID eller et unikt navn for resultatet.</span><span class="sxs-lookup"><span data-stu-id="19d12-134">**Outcome** – Enter a unique ID or name for the outcome.</span></span>
    - <span data-ttu-id="19d12-135">**Beskrivelse** – Angi en detaljert beskrivelse av resultatet.</span><span class="sxs-lookup"><span data-stu-id="19d12-135">**Description** – Enter a detailed description of the outcome.</span></span>
    - <span data-ttu-id="19d12-136">**Resultatstatus** – Velg enten *Bestått* eller *Mislykket* for å angi om testen er bestått eller mislyktes når resultatet er valgt som et testresult.</span><span class="sxs-lookup"><span data-stu-id="19d12-136">**Outcome status** – Select either *Pass* or *Fail* to indicate whether the test is passed or failed when the outcome is selected as a test result.</span></span>

1. <span data-ttu-id="19d12-137">Gjenta det forrige trinnet for hvert tilleggsresultat.</span><span class="sxs-lookup"><span data-stu-id="19d12-137">Repeat the previous step for each additional outcome.</span></span> <span data-ttu-id="19d12-138">Kontroller at minst ett resultat har resultatstatusen *Bestått*, og at minst én har resultatstatusen *Mislykket*.</span><span class="sxs-lookup"><span data-stu-id="19d12-138">Make sure that at least one outcome has an outcome status of *Pass* and at least one has an outcome status of *Fail*.</span></span>
1. <span data-ttu-id="19d12-139">Lukk sidene.</span><span class="sxs-lookup"><span data-stu-id="19d12-139">Close the pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="19d12-140">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="19d12-140">Additional resources</span></span>

- [<span data-ttu-id="19d12-141">Testinstrumenter for kvalitetsstyring</span><span class="sxs-lookup"><span data-stu-id="19d12-141">Quality management test instruments</span></span>](quality-test-instruments.md)
- [<span data-ttu-id="19d12-142">Kvalitetsstyringstester</span><span class="sxs-lookup"><span data-stu-id="19d12-142">Quality management tests</span></span>](quality-tests.md)
- [<span data-ttu-id="19d12-143">Testgrupper for kvalitetsstyring</span><span class="sxs-lookup"><span data-stu-id="19d12-143">Quality management test groups</span></span>](quality-test-groups.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
