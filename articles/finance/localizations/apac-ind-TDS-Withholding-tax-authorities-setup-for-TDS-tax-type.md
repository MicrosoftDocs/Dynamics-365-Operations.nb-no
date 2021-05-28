---
title: Definere kildeskattmyndigheter for TDS-avgiftstypen
description: Dette emnet forklarer hvordan du konfigurerer myndigheter for TDS-funksjonen (Tax Deducted at Source).
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
ms.openlocfilehash: 5375363a9b1383a83e80fc3c4b841780adab4172
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023470"
---
# <a name="set-up-withholding-tax-authorities-for-the-tds-tax-type"></a><span data-ttu-id="ecc81-103">Definere kildeskattmyndigheter for TDS-avgiftstypen</span><span class="sxs-lookup"><span data-stu-id="ecc81-103">Set up withholding tax authorities for the TDS tax type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ecc81-104">Dette emnet forklarer hvordan du konfigurerer myndigheter for TDS-funksjonen (Tax Deducted at Source).</span><span class="sxs-lookup"><span data-stu-id="ecc81-104">This topic explains how to set up Tax Deducted at Source (TDS) authorities.</span></span>

1. <span data-ttu-id="ecc81-105">Gå til **Avgift \> Indirekte avgifter \> Myndigheter for kildeskatt**.</span><span class="sxs-lookup"><span data-stu-id="ecc81-105">Go to **Tax \> Indirect taxes \> Withholding tax authorities**.</span></span>

    <span data-ttu-id="ecc81-106">[![Siden Myndigheter for kildeskatt](./media/apac-ind-TDS-12.png)](./media/apac-ind-TDS-12.png)</span><span class="sxs-lookup"><span data-stu-id="ecc81-106">[![Withholding tax authorities page](./media/apac-ind-TDS-12.png)](./media/apac-ind-TDS-12.png)</span></span>

2. <span data-ttu-id="ecc81-107">Velg **TDS** i **Avgiftstype**-feltet for å definere myndigheter for kildeskatt for TDS-avgiftstypen.</span><span class="sxs-lookup"><span data-stu-id="ecc81-107">In the **Tax type** field, select **TDS** to set up withholding tax authorities for the TDS tax type.</span></span>
3. <span data-ttu-id="ecc81-108">I handlingsruten velger du **Ny** for å opprette en linje.</span><span class="sxs-lookup"><span data-stu-id="ecc81-108">On the Action Pane, select **New** to create a line.</span></span>
4. <span data-ttu-id="ecc81-109">Angi et navn for TDS-myndigheten i feltet **Kildeskattemyndighet**.</span><span class="sxs-lookup"><span data-stu-id="ecc81-109">In the **Withholding tax authority** field, enter a name for the TDS authority.</span></span>
5. <span data-ttu-id="ecc81-110">Angi en beskrivelse i **Beskrivelse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="ecc81-110">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="ecc81-111">I hurtifanene **Generelt** i feltet **Leverandørkonto** velger du leverandørkontoen for TDS-myndigheten.</span><span class="sxs-lookup"><span data-stu-id="ecc81-111">On the **General** FastTab, in the **Vendor account** field, select the vendor account for the TDS authority.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ecc81-112">Du må definere navnet på banken der det blir satt inn penger som skyldes til TDS-myndighetsleverandøren.</span><span class="sxs-lookup"><span data-stu-id="ecc81-112">You must define the name of the bank where funds that are owed to the TDS authority vendor will be deposited.</span></span> <span data-ttu-id="ecc81-113">Bankens navn er definert på siden **Bankkontoer** (**Leverandører \> Alle leverandører \> Leverandør \> Konfigurer \> Bankkontoer**).</span><span class="sxs-lookup"><span data-stu-id="ecc81-113">The bank's name is defined on the **Bank accounts** page (**Accounts payable \> All vendors \> Vendor \> Set up \> Bank accounts**).</span></span>

7. <span data-ttu-id="ecc81-114">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="ecc81-114">Close the page.</span></span>
