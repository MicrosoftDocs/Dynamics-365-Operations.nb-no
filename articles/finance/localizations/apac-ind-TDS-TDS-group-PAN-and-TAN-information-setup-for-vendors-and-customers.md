---
title: Konfigurere informasjon om TDS-gruppe, PAN og TAN for leverandører og kunder
description: Dette emnet forklarer hvordan du konfigurerer informasjon om TDS-gruppe (Tax Deducted at Source), permanent kontonummer (PAN) og TAN (Tax Account Number) for leverandører og kunder.
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
ms.openlocfilehash: fd33b1775afefed798f1e9bb7601f4112222c430
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023479"
---
# <a name="tds-group-pan-and-tan-information-setup-for-vendors-and-customers"></a><span data-ttu-id="8aa71-103">Konfigurasjon av informasjon om TDS-gruppe, PAN og TAN for leverandører og kunder</span><span class="sxs-lookup"><span data-stu-id="8aa71-103">TDS group, PAN, and TAN information setup for vendors and customers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8aa71-104">Dette emnet forklarer hvordan du konfigurerer informasjon om TDS-gruppe (Tax Deducted at Source), permanent kontonummer (PAN) og TAN (Tax Account Number) for leverandører og kunder.</span><span class="sxs-lookup"><span data-stu-id="8aa71-104">This topic explains how to set up information about the Tax Deducted at Source (TDS) group, permanent account number (PAN), and tax account number (TAN) for vendors and customers.</span></span>

1. <span data-ttu-id="8aa71-105">Gå til **Leverandører \> Leverandører \> Alle leverandører** eller **Kunder \> Kunder \> Alle kunder**.</span><span class="sxs-lookup"><span data-stu-id="8aa71-105">Go to **Accounts payable \> Vendors \> All vendors** or **Accounts receivable \> Customers \> All customers**.</span></span>

    <span data-ttu-id="8aa71-106">[![Siden Alle leverandører](./media/apac-ind-TDS-55.png)](./media/apac-ind-TDS-55.png)</span><span class="sxs-lookup"><span data-stu-id="8aa71-106">[![All vendors page](./media/apac-ind-TDS-55.png)](./media/apac-ind-TDS-55.png)</span></span>

2. <span data-ttu-id="8aa71-107">Velg **Ny** i handlingsruten for å opprette en leverandør eller kunde, og angi de nødvendige detaljene.</span><span class="sxs-lookup"><span data-stu-id="8aa71-107">On the Action Pane, select **New** to create a vendor or customer, and enter the required details.</span></span> <span data-ttu-id="8aa71-108">Du kan alternativt velge en eksisterende leverandør eller kunde.</span><span class="sxs-lookup"><span data-stu-id="8aa71-108">Alternatively, select an existing vendor or customer.</span></span>
3. <span data-ttu-id="8aa71-109">Sett alternativet **Beregn kildeskatt** til **Ja** i **Kildeskatt**-delen i hurtigfanen **Faktura og levering** for å beregne kildeskatt, TDS eller TCS (Tax Collected at Source) for leverandøren eller kunden.</span><span class="sxs-lookup"><span data-stu-id="8aa71-109">On the **Invoice and delivery** FastTab, in the **Withholding tax** section, set the **Calculate withholding tax** option to **Yes** to calculate withholding tax, TDS, or Tax Collected at Source (TCS) for the vendor or customer.</span></span>
4. <span data-ttu-id="8aa71-110">TDS for en innkjøpsfaktura beregnes basert på standard TDS-gruppe som er definert for leverandøren eller kunden.</span><span class="sxs-lookup"><span data-stu-id="8aa71-110">TDS for a purchase invoice is calculated based on the default TDS group that is defined for the vendor or customer.</span></span> <span data-ttu-id="8aa71-111">Velg standard TDS-gruppe i feltet **TDS-gruppe**.</span><span class="sxs-lookup"><span data-stu-id="8aa71-111">In the **TDS group** field, select the default TDS group.</span></span>

    > [!NOTE]
    > <span data-ttu-id="8aa71-112">Feltene **Kildeskattgruppe** og **TDS-gruppe** blir utilgjengelige når du velger en TDS-gruppe i feltet **TDS-gruppe**.</span><span class="sxs-lookup"><span data-stu-id="8aa71-112">When you select a TDS group in the **TDS group** field, the **Withholding tax group** and **TCS group** fields become unavailable.</span></span>

5. <span data-ttu-id="8aa71-113">Velg statusen for det permanente kontonummeret for leverandøren eller kunden i **Status**-feltet i delen **PAN-informasjon** i hurtigfanen **Avgiftsinformasjon**:</span><span class="sxs-lookup"><span data-stu-id="8aa71-113">On the **Tax information** FastTab, in the **PAN information** section, in the **Status** field, select the status of the permanent account number for the vendor or customer:</span></span>

    - <span data-ttu-id="8aa71-114">**Ikke tilgjengelig** – Leverandøren eller kunden har ikke et PAN-nummer.</span><span class="sxs-lookup"><span data-stu-id="8aa71-114">**Not available** – The vendor or customer doesn't have a PAN.</span></span>
    - <span data-ttu-id="8aa71-115">**Mottatt** – Leverandøren eller kunden har et PAN-nummer.</span><span class="sxs-lookup"><span data-stu-id="8aa71-115">**Received** – The vendor or customer has a PAN.</span></span>
    - <span data-ttu-id="8aa71-116">**Søkt** – Leverandøren eller kunden har søkt om et PAN-nummer.</span><span class="sxs-lookup"><span data-stu-id="8aa71-116">**Applied** – The vendor or customer has applied for a PAN.</span></span>
    - <span data-ttu-id="8aa71-117">**Ugyldig** – Leverandøren eller kunden har et PAN-nummer, men det er ikke gyldig.</span><span class="sxs-lookup"><span data-stu-id="8aa71-117">**Invalid** – The vendor or customer has a PAN, but it isn't valid.</span></span>

6. <span data-ttu-id="8aa71-118">Hvis du valgte **Mottatt** i **Status**-feltet for å angi at leverandøren eller kunden har et PAN-nummer, angir du PAN-nummeret i **Nummer**-feltet.</span><span class="sxs-lookup"><span data-stu-id="8aa71-118">If you selected **Received** in the **Status** field to indicate that the vendor or customer has a PAN, enter the PAN in the **Number** field.</span></span> <span data-ttu-id="8aa71-119">PAN-nummeret må bestå av fem alfabetiske bokstaver, deretter fire numeriske tegn og deretter én alfabetisk bokstav.</span><span class="sxs-lookup"><span data-stu-id="8aa71-119">The PAN must consist of five alphabetic characters, then four numeric characters, and then one alphabetic character.</span></span> <span data-ttu-id="8aa71-120">Her er et eksempel: **ABCDE1260A**.</span><span class="sxs-lookup"><span data-stu-id="8aa71-120">Here is an example: **ABCDE1260A**.</span></span>
7. <span data-ttu-id="8aa71-121">Hvis du valgte **Søkt** i **Status**-feltet for å angi at leverandøren eller kunden har søkt om et PAN-nummer, angir du referansenummeret i feltet **Referansenummer**.</span><span class="sxs-lookup"><span data-stu-id="8aa71-121">If you selected **Applied** in the **Status** field to indicate that the vendor or customer has applied for PAN, enter the reference number in the **Reference number** field.</span></span>
8. <span data-ttu-id="8aa71-122">Velg kategorien for skattebetalertype som leverandøren eller kunden hører til i, i feltet **Skattebetalertype**.</span><span class="sxs-lookup"><span data-stu-id="8aa71-122">In the **Nature of assessee** field, select the nature of assessee category that the vendor or customer belongs to:</span></span>

    - <span data-ttu-id="8aa71-123">Selskap</span><span class="sxs-lookup"><span data-stu-id="8aa71-123">Company</span></span>
    - <span data-ttu-id="8aa71-124">HUF</span><span class="sxs-lookup"><span data-stu-id="8aa71-124">HUF</span></span>
    - <span data-ttu-id="8aa71-125">Firma</span><span class="sxs-lookup"><span data-stu-id="8aa71-125">Firm</span></span>
    - <span data-ttu-id="8aa71-126">Enkeltperson</span><span class="sxs-lookup"><span data-stu-id="8aa71-126">Individual</span></span>
    - <span data-ttu-id="8aa71-127">AOP</span><span class="sxs-lookup"><span data-stu-id="8aa71-127">AOP</span></span>
    - <span data-ttu-id="8aa71-128">BOI</span><span class="sxs-lookup"><span data-stu-id="8aa71-128">BOI</span></span>
    - <span data-ttu-id="8aa71-129">Lokale myndigheter</span><span class="sxs-lookup"><span data-stu-id="8aa71-129">Local authority</span></span>
    - <span data-ttu-id="8aa71-130">Andre</span><span class="sxs-lookup"><span data-stu-id="8aa71-130">Others</span></span>

    <span data-ttu-id="8aa71-131">[![Hurtigfanen Avgiftsinformasjon](./media/apac-ind-TDS-56.png)](./media/apac-ind-TDS-56.png)</span><span class="sxs-lookup"><span data-stu-id="8aa71-131">[![Tax information FastTab](./media/apac-ind-TDS-56.png)](./media/apac-ind-TDS-56.png)</span></span>

9. <span data-ttu-id="8aa71-132">Velg **Registrerings-ID-er** i **Registrering**-gruppen i **Leverandør**-fanen i handlingsruten for å åpne siden **Administrer adresser**.</span><span class="sxs-lookup"><span data-stu-id="8aa71-132">On the Action Pane, on the **Vendor** tab, in the **Registration** group, select **Registration IDs** to open the **Manage addresses** page.</span></span>
10. <span data-ttu-id="8aa71-133">Velg **Legg til** eller **Rediger** i hurtigfanen **Avgiftsinformasjon** på siden **Administrer adresser** for å åpne siden **Administrer avgiftsinformasjon**, der du kan vedlikeholde oppføringen for avgiftsregistrering.</span><span class="sxs-lookup"><span data-stu-id="8aa71-133">On the **Manage addresses** page, on the **Tax information** FastTab, select **Add** or **Edit** to open the **Manage tax information** page, where you can maintain the tax registration entry.</span></span>
11. <span data-ttu-id="8aa71-134">Angi TAN-nummeret i feltet **TAN-nummer (Tax Account Number)** i hurtigfanen **Kildeskatt** på siden **Administrer avgiftsinformasjon**.</span><span class="sxs-lookup"><span data-stu-id="8aa71-134">On the **Manage tax information** page, on the **Withholding tax** FastTab, in the **Tax Account Number (TAN)** field, enter the TAN.</span></span> <span data-ttu-id="8aa71-135">TAN-nummeret må bestå av fire alfabetiske bokstaver, deretter fem numeriske tegn og deretter én alfabetisk bokstav.</span><span class="sxs-lookup"><span data-stu-id="8aa71-135">The TAN must consist of four alphabetic characters, then five numeric characters, and then one alphabetic character.</span></span> <span data-ttu-id="8aa71-136">Her er et eksempel: **AFGH54821T**.</span><span class="sxs-lookup"><span data-stu-id="8aa71-136">Here is an example: **AFGH54821T**.</span></span>
12. <span data-ttu-id="8aa71-137">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="8aa71-137">Close the page.</span></span>
