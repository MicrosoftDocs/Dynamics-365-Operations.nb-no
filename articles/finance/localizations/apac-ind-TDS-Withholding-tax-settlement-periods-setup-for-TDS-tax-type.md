---
title: Definere utligningsperioder for kildeskatt for TCS-avgiftstypen
description: Dette emnet forklarer hvordan du konfigurerer utligningsperioder for TDS-utligningsperioder (Tax Deducted at Source).
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
ms.openlocfilehash: 9430bc1386f127d02b598d6cad1b53f66e0cf2ba
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023465"
---
# <a name="set-up-withholding-tax-settlement-periods-for-the-tds-tax-type"></a><span data-ttu-id="f0dd9-103">Definere utligningsperioder for kildeskatt for TCS-avgiftstypen</span><span class="sxs-lookup"><span data-stu-id="f0dd9-103">Set up withholding tax settlement periods for the TDS tax type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f0dd9-104">Dette emnet forklarer hvordan du konfigurerer utligningsperioder for TDS-utligningsperioder (Tax Deducted at Source).</span><span class="sxs-lookup"><span data-stu-id="f0dd9-104">This topic explains how to set up settlement periods for Tax Deducted at Source (TDS) settlement periods.</span></span>

1. <span data-ttu-id="f0dd9-105">Gå til **Avgift \> Indirekte avgifter \> Kildeskatt \> Utligningsperioder for kildeskatt**.</span><span class="sxs-lookup"><span data-stu-id="f0dd9-105">Go to **Tax \> Indirect taxes \> Withholding tax \> Withholding tax settlement periods**.</span></span>

    <span data-ttu-id="f0dd9-106">[![Siden Utligningsperioder for kildeskatt](./media/apac-ind-TDS-13.png)](./media/apac-ind-TDS-13.png)</span><span class="sxs-lookup"><span data-stu-id="f0dd9-106">[![Withholding tax settlement periods page](./media/apac-ind-TDS-13.png)](./media/apac-ind-TDS-13.png)</span></span>

2. <span data-ttu-id="f0dd9-107">Velg **TDS** i **Avgiftstype**-feltet for å definere utligningsperioder for kildeskatt for TDS-avgiftstypen.</span><span class="sxs-lookup"><span data-stu-id="f0dd9-107">In the **Tax type** field, select **TDS** to set up withholding tax settlement periods for the TDS tax type.</span></span>
3. <span data-ttu-id="f0dd9-108">Velg **Ny** for å opprette en linje.</span><span class="sxs-lookup"><span data-stu-id="f0dd9-108">Select **New** to create a line.</span></span>
4. <span data-ttu-id="f0dd9-109">I **Utligningsperiode**-feltet angir du et navn for TDS-utligningsperioden.</span><span class="sxs-lookup"><span data-stu-id="f0dd9-109">In the **Settlement period** field, enter a name for the TDS settlement period.</span></span>
5. <span data-ttu-id="f0dd9-110">Angi en beskrivelse i **Beskrivelse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="f0dd9-110">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="f0dd9-111">I feltet for **kildeskattemyndighet** velger du TDS-myndigheten som du definerer TDS-utligningsperioden for.</span><span class="sxs-lookup"><span data-stu-id="f0dd9-111">In the **Withholding tax authority** field, select the TDS authority that you're defining the TDS settlement period for.</span></span>
7. <span data-ttu-id="f0dd9-112">I feltet **Periodeintervall** i hurtigfanen **Generelt** velger du typen periodeintervall for TDS-utligningsperioden.</span><span class="sxs-lookup"><span data-stu-id="f0dd9-112">On the **General** FastTab, in the **Period interval** field, select the type of period interval for the TDS settlement period.</span></span>
8. <span data-ttu-id="f0dd9-113">I feltet **Antall enheter** angir du antall enheter for periodeintervalltypen.</span><span class="sxs-lookup"><span data-stu-id="f0dd9-113">In the **Number of units** field, specify the number of units for the period interval type.</span></span>
9. <span data-ttu-id="f0dd9-114">I hurtigfanen **Perioder** i feltet **Fra dato** velger du startdatoen for TDS-utligningsperioden.</span><span class="sxs-lookup"><span data-stu-id="f0dd9-114">On the **Periods** FastTab, in the **From date** field, select the start date for the TDS settlement period.</span></span> <span data-ttu-id="f0dd9-115">I **Til dato**-feltet velger du sluttdatoen.</span><span class="sxs-lookup"><span data-stu-id="f0dd9-115">In the **To date** field, select the end date.</span></span>
10. <span data-ttu-id="f0dd9-116">Hvis du vil opprette en etterfølgende TDS-utligningsperiode for en eksisterende periode, velger du **Ny periode** basert på periodeintervallet og periodeenhetene.</span><span class="sxs-lookup"><span data-stu-id="f0dd9-116">To create a subsequent TDS settlement period for an existing period, based on the period interval and period units, select **New period**.</span></span>
11. <span data-ttu-id="f0dd9-117">Hvis du vil vise detaljene for den periodiske TDS-utligningen som kjøres for en bestemt utligningsperiode, velger du **Kildeskattbetalinger** for å åpne **Kildeskattbetaling**-siden.</span><span class="sxs-lookup"><span data-stu-id="f0dd9-117">To view the details of the periodic TDS settlement that is run for a specific settlement period, select **Withholding tax payments** to open the **Withholding tax payment** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f0dd9-118">Hvis du vil kjøre den periodiske TDS-utligningsprosessen, går du til **Økonomimodul \> Periodisk \> Kildeskatt \> Kildeskattbetaling**.</span><span class="sxs-lookup"><span data-stu-id="f0dd9-118">To run the periodic TDS settlement process, go to **General ledger \> Periodic \> Withholding tax \> Withholding tax payment**.</span></span>

    <span data-ttu-id="f0dd9-119">[![Siden Kildeskattbetaling](./media/apac-ind-TDS-15.png)](./media/apac-ind-TDS-15.png)</span><span class="sxs-lookup"><span data-stu-id="f0dd9-119">[![Withholding tax payment page](./media/apac-ind-TDS-15.png)](./media/apac-ind-TDS-15.png)</span></span>

12. <span data-ttu-id="f0dd9-120">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="f0dd9-120">Close the page.</span></span>
