---
title: Bilag genereres ikke
description: Dette emnet gir feilsøkingsinformasjon som kan være til hjelp når et bilag ikke genereres som det skal.
author: qire
manager: beya
ms.date: 04/13/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: eafc9110ec58be5083569188d59b67a62e86c85d
ms.sourcegitcommit: 57668404d61359b33e0c0280f2f7c4eb829b1ed2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/27/2021
ms.locfileid: "5947688"
---
# <a name="voucher-isnt-generated"></a><span data-ttu-id="51604-103">Bilag genereres ikke</span><span class="sxs-lookup"><span data-stu-id="51604-103">Voucher isn't generated</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="51604-104">Hvis et bilag skal genereres, men **bilagstransaksjonssiden** ikke viser noen bilag, følger du trinnene i de følgende delene etter behov for å feilsøke dette problemet.</span><span class="sxs-lookup"><span data-stu-id="51604-104">If a voucher should be generated, but the **Voucher transactions** page doesn't show any vouchers, follow the steps in the following sections as required to troubleshoot this issue.</span></span>

<span data-ttu-id="51604-105">[![Bilagstransaksjonsside som ikke har noen bilag](./media/voucher-not-generated-Picture1.png)](./media/voucher-not-generated-Picture1.png)</span><span class="sxs-lookup"><span data-stu-id="51604-105">[![Voucher transactions page that has no vouchers](./media/voucher-not-generated-Picture1.png)](./media/voucher-not-generated-Picture1.png)</span></span>

## <a name="check-the-tax-applicability"></a><span data-ttu-id="51604-106">Kontrollere mva-relevansen</span><span class="sxs-lookup"><span data-stu-id="51604-106">Check the tax applicability</span></span>

1. <span data-ttu-id="51604-107">Gå til **Avgift** \> **Periodiske oppgaver** \> **Underfinansjournaloppføringer som ennå ikke er overført**.</span><span class="sxs-lookup"><span data-stu-id="51604-107">Go to **Tax** \> **Periodic tasks** \> **Subledger journal entries not yet transferred**.</span></span>
2. <span data-ttu-id="51604-108">Hvis det finnes en journalpost, velger du den, og deretter velger du **Overfør nå**.</span><span class="sxs-lookup"><span data-stu-id="51604-108">If there is a journal record, select it, and then select **Transfer now**.</span></span>

    <span data-ttu-id="51604-109">[![Overfør nå-knappen på siden Underfinansjournaloppføringer som ennå ikke er overført](./media/voucher-not-generated-Picture2.png)](./media/voucher-not-generated-Picture2.png)</span><span class="sxs-lookup"><span data-stu-id="51604-109">[![Transfer now button on the Subledger journal entries not yet transferred page](./media/voucher-not-generated-Picture2.png)](./media/voucher-not-generated-Picture2.png)</span></span>

3. <span data-ttu-id="51604-110">Åpne **bilagstransaksjonssiden** på nytt for å se om bilaget ble generert.</span><span class="sxs-lookup"><span data-stu-id="51604-110">Open the **Voucher transactions** page again to see whether the voucher was generated.</span></span>

## <a name="determine-whether-customization-exists"></a><span data-ttu-id="51604-111">Fastslå om det finnes tilpasning</span><span class="sxs-lookup"><span data-stu-id="51604-111">Determine whether customization exists</span></span>

<span data-ttu-id="51604-112">Hvis du har fullført trinnene i den forrige delen, men ikke har funnet problemet, må du avgjøre om det finnes tilpasning.</span><span class="sxs-lookup"><span data-stu-id="51604-112">If you've completed the steps in the previous section but have found no issue, determine whether customization exists.</span></span> <span data-ttu-id="51604-113">Hvis det ikke finnes noen tilpasning, oppretter du en Microsoft-tjenesteforespørsel for mer støtte.</span><span class="sxs-lookup"><span data-stu-id="51604-113">If no customization exists, create a Microsoft service request for further support.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]