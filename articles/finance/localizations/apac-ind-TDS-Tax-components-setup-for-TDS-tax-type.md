---
title: Konfigurere avgiftskomponenter for TDS-avgiftstypen
description: Dette emnet forklarer hvordan du konfigurerer komponenter for kildeskatt for TDS-avgiftstypen (Tax Deducted at Source). Det forklarer også hvordan du definerer terskelgrensen som skal brukes til å beregne TDS for hver TDS-komponent.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 6e0a6a05fcb4afb8c8965e25c3089bc1b3d98431
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023473"
---
# <a name="set-up-tax-components-for-the-tds-tax-type"></a><span data-ttu-id="e5e3d-104">Konfigurere avgiftskomponenter for TDS-avgiftstypen</span><span class="sxs-lookup"><span data-stu-id="e5e3d-104">Set up tax components for the TDS tax type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e5e3d-105">Dette emnet forklarer hvordan du konfigurerer komponenter for kildeskatt for TDS-avgiftstypen (Tax Deducted at Source).</span><span class="sxs-lookup"><span data-stu-id="e5e3d-105">This topic explains how to set up withholding tax components for the Tax Deducted at Source (TDS) tax type.</span></span> <span data-ttu-id="e5e3d-106">TDS-komponentene er TDS, tilleggsavgift, PE-Cess og SHE Cess.</span><span class="sxs-lookup"><span data-stu-id="e5e3d-106">The TDS components are TDS, surcharge, PE-Cess, and SHE Cess.</span></span> <span data-ttu-id="e5e3d-107">Dette emnet forklarer også hvordan du definerer terskelen som skal brukes til å beregne TDS for hver TDS-komponent.</span><span class="sxs-lookup"><span data-stu-id="e5e3d-107">This topic also explains how to define the threshold that is used to calculate TDS for each TDS component.</span></span> <span data-ttu-id="e5e3d-108">Du kan i tillegg definere en unntaksterskel som skal brukes til å beregne TDS for hver TDS-komponent.</span><span class="sxs-lookup"><span data-stu-id="e5e3d-108">Additionally, you can define an exception threshold that is used to calculate TDS for each TDS component.</span></span>

<span data-ttu-id="e5e3d-109">Følg trinnene nedenfor for å konfigurere TDS-komponenter.</span><span class="sxs-lookup"><span data-stu-id="e5e3d-109">Follow these steps to set up TDS components.</span></span>

1. <span data-ttu-id="e5e3d-110">Gå til **Avgift \> Oppsett \> Kildeskatt \> Komponenter for kildeskatt**.</span><span class="sxs-lookup"><span data-stu-id="e5e3d-110">Go to **Tax \> Setup \> Withholding tax \> Withholding tax components**.</span></span>

    <span data-ttu-id="e5e3d-111">[![Siden Komponenter for kildeskatt](./media/apac-ind-TDS-9.png)](./media/apac-ind-TDS-9.png)</span><span class="sxs-lookup"><span data-stu-id="e5e3d-111">[![Withholding tax components page](./media/apac-ind-TDS-9.png)](./media/apac-ind-TDS-9.png)</span></span>

2. <span data-ttu-id="e5e3d-112">Velg **TDS** i **Avgiftstype**-feltet for å definere komponenter for kildeskatt for TDS-avgiftstypen.</span><span class="sxs-lookup"><span data-stu-id="e5e3d-112">In the **Tax type** field, select **TDS** to set up withholding tax components for the TDS tax type.</span></span>
3. <span data-ttu-id="e5e3d-113">I handlingsruten velger du **Ny** for å opprette en linje.</span><span class="sxs-lookup"><span data-stu-id="e5e3d-113">On the Action Pane, select **New** to create a line.</span></span>
4. <span data-ttu-id="e5e3d-114">Angi et navn for TDS-komponenten i feltet **Komponent for kildeskatt**.</span><span class="sxs-lookup"><span data-stu-id="e5e3d-114">In the **Withholding tax component** field, enter a name for the TDS component.</span></span>
5. <span data-ttu-id="e5e3d-115">Velg komponentgruppen for kildeskatt for TDS som TDS-komponenten skal knyttes til, i feltet **Komponentgruppe for kildeskatt**.</span><span class="sxs-lookup"><span data-stu-id="e5e3d-115">In the **Withholding tax component group** field, select the TDS withholding tax component group to attach the TDS component to.</span></span>
6. <span data-ttu-id="e5e3d-116">Skriv inn en beskrivelse av TDS-komponenten i **Beskrivelse**-feltet i hurtigfanen **Generelt**.</span><span class="sxs-lookup"><span data-stu-id="e5e3d-116">On the **General** FastTab, in the **Description** field, enter a description of  the TDS component.</span></span>
7. <span data-ttu-id="e5e3d-117">Velg **Terskel** i handlingsruten for å åpne **Terskel**-siden, slik at du kan definere terskelen som skal brukes til å beregne TDS for TDS-komponenten.</span><span class="sxs-lookup"><span data-stu-id="e5e3d-117">On the Action Pane, select **Threshold** to open **Threshold** page, so that you can define the threshold that is used to calculate TDS for the TDS component.</span></span>
8. <span data-ttu-id="e5e3d-118">Bruk feltene **Fra-dato** og **Til-dato** til å definere perioden som terskelen skal gjelde for.</span><span class="sxs-lookup"><span data-stu-id="e5e3d-118">Use the **From date** and **To date** fields to define the period that the threshold is applicable to.</span></span>
9. <span data-ttu-id="e5e3d-119">Angi terskelbeløpet som skal brukes til å beregne TDS for TDS-komponenten, i **Terskel**-feltet i **Generelt**-fanen.</span><span class="sxs-lookup"><span data-stu-id="e5e3d-119">On the **General** FastTab, in the **Threshold** field, enter the threshold amount that is used to calculate TDS for the TDS component.</span></span> <span data-ttu-id="e5e3d-120">Avgiften trekkes bare fra ved kilden når det kumulative fakturabeløpet krysser terskelen.</span><span class="sxs-lookup"><span data-stu-id="e5e3d-120">The tax will be deducted at the source only when the cumulative invoice amount crosses the threshold.</span></span>

    <span data-ttu-id="e5e3d-121">Hvis terskelbeløpet for eksempel er 10 000, beregnes TDS etter at det kumulative fakturabeløpet overskrider 10 000 (med andre ord når det er 10 001 eller mer).</span><span class="sxs-lookup"><span data-stu-id="e5e3d-121">For example, if the threshold amount is 10,000, TDS is calculated after the cumulative invoice amount exceeds 10,000 (in other words, when it's 10,001 or more).</span></span>

10. <span data-ttu-id="e5e3d-122">Angi unntaksterskelbeløpet som skal brukes til å beregne TDS for TDS-komponenten, i **Unntaksterskel**-feltet.</span><span class="sxs-lookup"><span data-stu-id="e5e3d-122">In the **Exception threshold** field, enter the exception threshold amount that is used to calculate TDS for the TDS component.</span></span> <span data-ttu-id="e5e3d-123">Avgiften på en fakturalinje trekkes bare fra ved kilden når beløpet krysser unntaksterskelen.</span><span class="sxs-lookup"><span data-stu-id="e5e3d-123">The tax on an invoice line will be deducted at the source only when the amount crosses the exception threshold.</span></span>

    <span data-ttu-id="e5e3d-124">Hvis unntaksterskelbeløpet for eksempel er 5 000, beregnes TDS for en bestemt fakturalinje hvis fakturalinjebeløpet overskrider 5 000 (det vil si hvis det er 5 001 eller mer).</span><span class="sxs-lookup"><span data-stu-id="e5e3d-124">For example, if the exception threshold amount is 5,000, TDS is calculated on a specific invoice line if the invoice line amount exceeds 5,000 (in other words, if it's 5,001 or more).</span></span>

    <span data-ttu-id="e5e3d-125">[![Terskel-siden](./media/apac-ind-TDS-10.png)](./media/apac-ind-TDS-10.png)</span><span class="sxs-lookup"><span data-stu-id="e5e3d-125">[![Threshold page](./media/apac-ind-TDS-10.png)](./media/apac-ind-TDS-10.png)</span></span>

    > [!NOTE]
    > <span data-ttu-id="e5e3d-126">Unntaksterskelbeløpet må være mindre enn eller likt terskelbeløpet.</span><span class="sxs-lookup"><span data-stu-id="e5e3d-126">The exception threshold amount must be less than or equal to the threshold amount.</span></span>
    >
    > <span data-ttu-id="e5e3d-127">Avgiften trekkes fra for en transaksjon hvis transaksjonsbeløpet krysser unntaksterskelen, selv om det kumulative fakturabeløpet ikke krysser terskelen som er angitt i **Terskel**-feltet.</span><span class="sxs-lookup"><span data-stu-id="e5e3d-127">The tax is deducted for a transaction if the transaction amount crosses the exception threshold, even if the cumulative invoice amount doesn't cross the threshold that is specified in the **Threshold** field.</span></span>

11. <span data-ttu-id="e5e3d-128">Lukk **Terskel**-siden for å gå tilbake til siden **Komponenter for kildeskatt**.</span><span class="sxs-lookup"><span data-stu-id="e5e3d-128">Close the **Threshold** page to return to the **Withholding tax components** page.</span></span>
12. <span data-ttu-id="e5e3d-129">Velg **Kopier** i handlingsruten for å åpne dialogboksen **Kopier komponenter for kildeskatt**, slik at du kan kopiere TDS-komponentene som er konfigurert for én TDS-komponentgruppe, til en annen TDS-komponentgruppe.</span><span class="sxs-lookup"><span data-stu-id="e5e3d-129">On the Action Pane, select **Copy** to open the **Copy withholding tax components** dialog box, so that you can copy the TDS components that were set up for one TDS component group to another TDS component group.</span></span>
13. <span data-ttu-id="e5e3d-130">I **Fra**-feltet velger du TDS-komponentgruppen du vil kopiere TDS-komponentene fra.</span><span class="sxs-lookup"><span data-stu-id="e5e3d-130">In the **From** field, select the TDS component group to copy the TDS components from.</span></span> <span data-ttu-id="e5e3d-131">I **Til**-feltet velger du komponentgruppen for kildeskatt du vil kopiere TDS-komponentene til.</span><span class="sxs-lookup"><span data-stu-id="e5e3d-131">In the **To** field, select the withholding tax component group to copy the TDS components to.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e5e3d-132">Vanlige TDS-komponenter som er knyttet til begge TDS-komponentgruppene, kopieres ikke.</span><span class="sxs-lookup"><span data-stu-id="e5e3d-132">Common TDS components that are attached to both TDS component groups aren't copied.</span></span>

14. <span data-ttu-id="e5e3d-133">Velg **OK** for å kopiere og opprette TDS-komponenter for den andre TDS-komponentgruppen på siden **Komponenter for kildeskatt**.</span><span class="sxs-lookup"><span data-stu-id="e5e3d-133">Select **OK** to copy and create TDS components for the other TDS component group on the **Withholding tax components** page.</span></span>

    <span data-ttu-id="e5e3d-134">[![Dialogboksen Kopier komponenter for kildeskatt](./media/apac-ind-TDS-11.png)](./media/apac-ind-TDS-11.png)</span><span class="sxs-lookup"><span data-stu-id="e5e3d-134">[![Copy withholding tax components dialog box](./media/apac-ind-TDS-11.png)](./media/apac-ind-TDS-11.png)</span></span>

15. <span data-ttu-id="e5e3d-135">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="e5e3d-135">Close the page.</span></span>
