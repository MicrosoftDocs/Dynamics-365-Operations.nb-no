---
title: Opprette en kildeskattbetaling
description: Jobbprosedyren kildeskattbetaling utligner kildeskattsaldoer fra leverandører på kildeskattkontoer og på mva-kontoene og forskyver dem til kildeskattoppgjørskontoen for en gitt periode. Dette emnet viser en oversikt over trinnene for å definere en kildeskattbetaling.
author: roschlom
manager: AnnBe
ms.date: 01/12/2021
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
ms.search.validFrom: 2020-01-12
ms.dyn365.ops.version: AX 10.0.16
ms.openlocfilehash: e522711340b663bd849825b3d4dd2b7e78e4737c
ms.sourcegitcommit: 630a0b3f800f36ced49b79156dd52132904fef75
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/25/2021
ms.locfileid: "5060777"
---
# <a name="create-a-withholding-tax-payment"></a><span data-ttu-id="bcf1c-104">Opprette en kildeskattbetaling</span><span class="sxs-lookup"><span data-stu-id="bcf1c-104">Create a withholding tax payment</span></span>

<span data-ttu-id="bcf1c-105">Jobbprosedyren kildeskattbetaling utligner kildeskattsaldoer fra leverandører på kildeskattkontoer og på mva-kontoene og forskyver dem til kildeskattoppgjørskontoen for en gitt periode.</span><span class="sxs-lookup"><span data-stu-id="bcf1c-105">The Withholding tax payment job procedure settles withholding tax balances from Accounts payable on withholding tax accounts, and offsets them to the withholding tax settlement account for a given period.</span></span> <span data-ttu-id="bcf1c-106">Dette emnet viser en oversikt over trinnene for å definere en kildeskattbetaling.</span><span class="sxs-lookup"><span data-stu-id="bcf1c-106">This topic lists the steps for setting up a withholding tax payment.</span></span>

> [!NOTE] 
> <span data-ttu-id="bcf1c-107">Kildeskattmotkonto (fra kunder) tas ikke med i betraktningen når en kildeskattbetaling beregnes.</span><span class="sxs-lookup"><span data-stu-id="bcf1c-107">Withholding tax offset (from accounts receivable) is not taken into account when a withholding tax payment is calculated.</span></span>

1. <span data-ttu-id="bcf1c-108">Gå til **Navigasjonsrute > Moduler > Avgift > Deklareringer > Kildeskatt > Kildeskattbetaling**.</span><span class="sxs-lookup"><span data-stu-id="bcf1c-108">Go to **Navigation pane > Modules > Tax > Declarations > Withholding tax > Withholding tax payment**.</span></span>
2. <span data-ttu-id="bcf1c-109">Klikk på rullegardinknappen i **Utligningsperiode**-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="bcf1c-109">In the **Settlement period** field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="bcf1c-110">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="bcf1c-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="bcf1c-111">Angi en dato i **Fra dato**-feltet.</span><span class="sxs-lookup"><span data-stu-id="bcf1c-111">In the **From date** field, enter a date.</span></span>
5. <span data-ttu-id="bcf1c-112">Angi en dato i feltet **Transaksjonsdato**.</span><span class="sxs-lookup"><span data-stu-id="bcf1c-112">In the **Transaction date** field, enter a date.</span></span>
6. <span data-ttu-id="bcf1c-113">Velg **Oppdater** for å postere kildeskattbetalingsbilag til kildeskattoppgjørskontoen.</span><span class="sxs-lookup"><span data-stu-id="bcf1c-113">Select **Update** to post withholding tax payment voucher to the withholding tax settlement account.</span></span>
7. <span data-ttu-id="bcf1c-114">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="bcf1c-114">Click **OK**.</span></span>

![Parametere for kildeskattbetaling](media/withholding-tax-payment.png)
