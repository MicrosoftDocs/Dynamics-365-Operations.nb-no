---
title: Konfigurerer TDS-finanskontoer
description: Dette emnet forklarer hvordan du konfigurerer finanskontoer for TDS-funksjonen (Tax Deducted at Source).
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
ms.openlocfilehash: 93d4cb54488ec0eeee40ca56f3e46f30012f54f5
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023477"
---
# <a name="set-up-tds-ledger-accounts"></a><span data-ttu-id="573ff-103">Konfigurerer TDS-finanskontoer</span><span class="sxs-lookup"><span data-stu-id="573ff-103">Set up TDS ledger accounts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="573ff-104">Dette emnet forklarer hvordan du konfigurerer finanskontoer for TDS-funksjonen (Tax Deducted at Source).</span><span class="sxs-lookup"><span data-stu-id="573ff-104">This topic explains how to set up ledger accounts for the Tax Deducted at Source (TDS) feature.</span></span> <span data-ttu-id="573ff-105">Du bruker **Kontoplan**-siden til å konfigurere finanskontoer for TDS.</span><span class="sxs-lookup"><span data-stu-id="573ff-105">You use the **Chart of accounts** page to set up ledger accounts for TDS.</span></span>

1. <span data-ttu-id="573ff-106">Gå til **Økonomimodul \> Kontoplan \> Kontoer \> Hovedkontoer**.</span><span class="sxs-lookup"><span data-stu-id="573ff-106">Go to **General ledger \> Chart of accounts \> Accounts \> Main accounts**.</span></span>
2. <span data-ttu-id="573ff-107">Trykk på **ALT+N** i **Oversikt**-fanen for å opprette en TDS-finanskonto, og angi de nødvendige detaljene.</span><span class="sxs-lookup"><span data-stu-id="573ff-107">On the **Overview** tab, select **Alt+N** to create a TDS ledger account, and enter the required details.</span></span>
3. <span data-ttu-id="573ff-108">Velg **Kildeskatt** i **Posteringstype**-feltet i **Oppsett**-fanen.</span><span class="sxs-lookup"><span data-stu-id="573ff-108">On the **Setup** tab, in the **Posting type** field, select **Withholding tax**.</span></span>     

    > [!NOTE]
    > <span data-ttu-id="573ff-109">Finanskontoer som har posteringstypen **Kildeskatt**, kan bare defineres som kundereskontroer som brukes til å postere TDS-tilgodebeløpet for en TDS-avgiftskode.</span><span class="sxs-lookup"><span data-stu-id="573ff-109">Ledger accounts that have a posting type of **Withholding tax** can be defined only as receivable accounts that are used to post the TDS receivable amount for a TDS tax code.</span></span>

4. <span data-ttu-id="573ff-110">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="573ff-110">Close the page.</span></span>
