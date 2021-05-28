---
title: Registrere TDS-konsesjonssertifikatnumre
description: Dette emnet forklarer hvordan du registrerer TDS-konsesjonssertifikatnumre (Tax Deducted at Source) som utstedes til leverandører.
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
ms.openlocfilehash: f543adc8bab5ca224bdb672d6b3c282c2d8531d8
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023466"
---
# <a name="record-tds-concession-certificate-numbers"></a><span data-ttu-id="1b381-103">Registrere TDS-konsesjonssertifikatnumre</span><span class="sxs-lookup"><span data-stu-id="1b381-103">Record TDS concession certificate numbers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1b381-104">Dette emnet forklarer hvordan du registrerer TDS-konsesjonssertifikatnumre (Tax Deducted at Source) som utstedes til leverandører.</span><span class="sxs-lookup"><span data-stu-id="1b381-104">This topic explains how to record the Tax Deducted at Source (TDS) concession certificate numbers that are issued to vendors.</span></span>

1. <span data-ttu-id="1b381-105">Gå til **Avgift \> Indirekte avgifter \> Kildeskatt \> Kildeskattkonsesjoner**.</span><span class="sxs-lookup"><span data-stu-id="1b381-105">Go to **Tax \> Indirect taxes \> Withholding tax \> Withholding tax concessions**.</span></span>
2. <span data-ttu-id="1b381-106">Velg **TDS** i **Avgiftstype**-feltet for å registrere konsesjonssertifikater for TDS-avgiftstypen.</span><span class="sxs-lookup"><span data-stu-id="1b381-106">In the **Tax type** field, select **TDS** to record concession certificates for the TDS tax type.</span></span>
3. <span data-ttu-id="1b381-107">Trykk på **ALT+N** i **Oversikt**-fanen for å opprette en linje.</span><span class="sxs-lookup"><span data-stu-id="1b381-107">On the **Overview** tab, select **Alt+N** to create a line.</span></span>

    <span data-ttu-id="1b381-108">[![Topptekst for den nye linjen](./media/apac-ind-TDS-34.png)](./media/apac-ind-TDS-34.png)</span><span class="sxs-lookup"><span data-stu-id="1b381-108">[![Header of the new line](./media/apac-ind-TDS-34.png)](./media/apac-ind-TDS-34.png)</span></span>

4. <span data-ttu-id="1b381-109">I feltet **Kildeskattkode** velger du TDS-avgiftskoden som konsesjonssertifikatene for leverandør er utstedt for.</span><span class="sxs-lookup"><span data-stu-id="1b381-109">In the **Withholding tax code** field, select the TDS tax code that the vendor concession certificates are issued for.</span></span> <span data-ttu-id="1b381-110">Feltet **Navn på kildeskattkode** viser navnet på TDS-avgiftskoden.</span><span class="sxs-lookup"><span data-stu-id="1b381-110">The **Withholding tax code name** field shows the name of the TDS tax code.</span></span>
5. <span data-ttu-id="1b381-111">Definer gyldighetsperioden for konsesjonssertifikatet som bruker TDS-avgiftskoden til å beregne TDS for leverandøren på en konsesjonsmessig basis, i feltene **Fra-dato** og **Til-dato**.</span><span class="sxs-lookup"><span data-stu-id="1b381-111">In the **From date** and **To date** fields, define the period of validity for the concession certificate that uses the TDS tax code to calculate TDS for the vendor on a concessional basis.</span></span>
6. <span data-ttu-id="1b381-112">Skriv inn eventuelle kommentarer i **Kommentarer**-feltet.</span><span class="sxs-lookup"><span data-stu-id="1b381-112">In the **Remarks** field, enter any remarks.</span></span>
7. <span data-ttu-id="1b381-113">I **Paragraf**-feltet angir du den rettslige paragrafkoden som TDS-konsesjonssertifikatet brukes under.</span><span class="sxs-lookup"><span data-stu-id="1b381-113">In the **Section** field, enter the legal section code that the TDS concession certificate is availed under.</span></span>

    <span data-ttu-id="1b381-114">Hvis paragrafkoden er 197, vises verdien «A» i både kolonnen «Reason for non-deduction/lower deduction» i Form 26Q og kolonnen «Reason for non-deduction/lower deduction/grossing up (if any)» i Form 27Q.</span><span class="sxs-lookup"><span data-stu-id="1b381-114">If the section code is 197, the value "A" appears in both the "Reason for non-deduction/lower deduction" column in Form 26Q and the "Reason for non-deduction/lower deduction/grossing up (if any)" column in Form 27Q.</span></span> <span data-ttu-id="1b381-115">Hvis paragrafkoden er 197A, vises verdien «B» begge disse stedene.</span><span class="sxs-lookup"><span data-stu-id="1b381-115">If the section code is 197A, the value "B" appears in both those places.</span></span>

8. <span data-ttu-id="1b381-116">Velg hurtigfanen **Sertifikat** for å registrere TDS-konsesjonssertifikatnumre for leverandører.</span><span class="sxs-lookup"><span data-stu-id="1b381-116">Select the **Certificate** FastTab to record TDS concession certificate numbers for vendors.</span></span>
9. <span data-ttu-id="1b381-117">I **Leverandørkonto**-feltet velger du leverandørkontoen som TDS-konsesjonssertifikatet er utstedt for.</span><span class="sxs-lookup"><span data-stu-id="1b381-117">In the **Vendor account** field, select the vendor account that the TDS concession certificate is issued for.</span></span>
10. <span data-ttu-id="1b381-118">Definer gyldighetsperioden for TDS-konsesjonssertifikatet i feltene **Fra-dato** og **Til-dato**.</span><span class="sxs-lookup"><span data-stu-id="1b381-118">In the **From date** and **To date** fields, define the period of validity for the TDS concession certificate.</span></span>

    <span data-ttu-id="1b381-119">Beregningen av TDS på konsesjonsmessig basis er basert på perioden når sertifikatet opprettes for leverandøren.</span><span class="sxs-lookup"><span data-stu-id="1b381-119">The calculation of TDS on a concessional basis is based on the period when the certificate is created for the vendor.</span></span>

11. <span data-ttu-id="1b381-120">Angi TDS-konsesjonssertifikatnummeret i **Sertifikat**-feltet.</span><span class="sxs-lookup"><span data-stu-id="1b381-120">In the **Certificate** field, enter the TDS concession certificate number.</span></span>

    <span data-ttu-id="1b381-121">[![Hurtigfanen Sertifikat](./media/apac-ind-TDS-33.png)](./media/apac-ind-TDS-33.png)</span><span class="sxs-lookup"><span data-stu-id="1b381-121">[![Certificate FastTab](./media/apac-ind-TDS-33.png)](./media/apac-ind-TDS-33.png)</span></span>

12. <span data-ttu-id="1b381-122">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="1b381-122">Close the page.</span></span>
