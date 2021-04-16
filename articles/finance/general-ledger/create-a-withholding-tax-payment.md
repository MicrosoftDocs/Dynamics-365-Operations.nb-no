---
title: Opprette en kildeskattbetaling
description: Jobbprosedyren kildeskattbetaling utligner kildeskattsaldoer fra leverandører på kildeskattkontoer og på mva-kontoene og forskyver dem til kildeskattoppgjørskontoen for en gitt periode. Dette emnet viser en oversikt over trinnene for å definere en kildeskattbetaling.
author: roschlom
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2020-01-12
ms.dyn365.ops.version: AX 10.0.16
ms.openlocfilehash: 72d80fbb3b2448f4b89fa7d7fa580387e1a3621c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5832952"
---
# <a name="create-a-withholding-tax-payment"></a><span data-ttu-id="02aae-104">Opprette en kildeskattbetaling</span><span class="sxs-lookup"><span data-stu-id="02aae-104">Create a withholding tax payment</span></span>

<span data-ttu-id="02aae-105">Jobbprosedyren kildeskattbetaling utligner kildeskattsaldoer fra leverandører på kildeskattkontoer og på mva-kontoene og forskyver dem til kildeskattoppgjørskontoen for en gitt periode.</span><span class="sxs-lookup"><span data-stu-id="02aae-105">The Withholding tax payment job procedure settles withholding tax balances from Accounts payable on withholding tax accounts, and offsets them to the withholding tax settlement account for a given period.</span></span> <span data-ttu-id="02aae-106">Dette emnet viser en oversikt over trinnene for å definere en kildeskattbetaling.</span><span class="sxs-lookup"><span data-stu-id="02aae-106">This topic lists the steps for setting up a withholding tax payment.</span></span>

> [!NOTE] 
> <span data-ttu-id="02aae-107">Kildeskattmotkonto (fra kunder) tas ikke med i betraktningen når en kildeskattbetaling beregnes.</span><span class="sxs-lookup"><span data-stu-id="02aae-107">Withholding tax offset (from accounts receivable) is not taken into account when a withholding tax payment is calculated.</span></span>

1. <span data-ttu-id="02aae-108">Gå til **Navigasjonsrute > Moduler > Avgift > Deklareringer > Kildeskatt > Kildeskattbetaling**.</span><span class="sxs-lookup"><span data-stu-id="02aae-108">Go to **Navigation pane > Modules > Tax > Declarations > Withholding tax > Withholding tax payment**.</span></span>
2. <span data-ttu-id="02aae-109">Klikk på rullegardinknappen i **Utligningsperiode**-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="02aae-109">In the **Settlement period** field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="02aae-110">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="02aae-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="02aae-111">Angi en dato i **Fra dato**-feltet.</span><span class="sxs-lookup"><span data-stu-id="02aae-111">In the **From date** field, enter a date.</span></span>
5. <span data-ttu-id="02aae-112">Angi en dato i feltet **Transaksjonsdato**.</span><span class="sxs-lookup"><span data-stu-id="02aae-112">In the **Transaction date** field, enter a date.</span></span>
6. <span data-ttu-id="02aae-113">Velg **Oppdater** for å postere kildeskattbetalingsbilag til kildeskattoppgjørskontoen.</span><span class="sxs-lookup"><span data-stu-id="02aae-113">Select **Update** to post withholding tax payment voucher to the withholding tax settlement account.</span></span>
7. <span data-ttu-id="02aae-114">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="02aae-114">Click **OK**.</span></span>

![Parametere for kildeskattbetaling](media/withholding-tax-payment.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]