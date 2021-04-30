---
title: Definere leiejournalnavn
description: Dette emnet forklarer hvordan du definerer navn på leierjournaler. Leiejournalnavn angir journalene som oppføringer som kommer fra aktivaleie, posteres til.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeasePostingAccounts
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: c139df124b249ec9dc5d16096e6f45f22d435456
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/13/2021
ms.locfileid: "5880892"
---
# <a name="set-up-lease-journal-names"></a><span data-ttu-id="2150c-104">Definere leiejournalnavn</span><span class="sxs-lookup"><span data-stu-id="2150c-104">Set up lease journal names</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2150c-105">Leiejournalnavn angir journalene som aktivaleietransaksjoner posteres til.</span><span class="sxs-lookup"><span data-stu-id="2150c-105">Lease journal names specify the journals that Asset leasing transactions are posted to.</span></span> <span data-ttu-id="2150c-106">Bare journalnavn som er tilordnet til **Aktivaleie**-journaltyper, vises i feltene **Opprinnelig føring** og **Månedlig journalnavn** på siden **Parametere for aktivaleie**.</span><span class="sxs-lookup"><span data-stu-id="2150c-106">Only journal names that are assigned to the **Asset leasing** journal type appear in the **Initial Recognition** and **Monthly Journal Name** fields on the **Asset leasing parameters** page.</span></span> <span data-ttu-id="2150c-107">Bare journaltypen **registrering av leverandørfaktura** kan tilordnes til feltet for **fakturajournalnavn**.</span><span class="sxs-lookup"><span data-stu-id="2150c-107">Only **vendor invoice recording** journal type can be assigned to the **Invoice journal name** field.</span></span>

<span data-ttu-id="2150c-108">Følg denne fremgangsmåten for å konfigurere navn på leiejournaler:</span><span class="sxs-lookup"><span data-stu-id="2150c-108">To configure lease journal names, follow these steps.</span></span>

1. <span data-ttu-id="2150c-109">Gå til **Aktivaleie \> Oppsett \> Parametere for aktivaleie**.</span><span class="sxs-lookup"><span data-stu-id="2150c-109">Go to **Asset leasing \> Setup \> Asset leasing parameters**.</span></span>
2. <span data-ttu-id="2150c-110">Gå til kategorien **Generelt** i feltet **navn på journal for opprinnelig føring**, og velg en journal.</span><span class="sxs-lookup"><span data-stu-id="2150c-110">On the **General** tab, in the **Initial recognition journal name** field, and select a journal.</span></span> <span data-ttu-id="2150c-111">Alle journaloppføringer for opprinnelig føring posteres til dette journalnavnet.</span><span class="sxs-lookup"><span data-stu-id="2150c-111">All initial recognition journal entries will be posted to this journal name.</span></span>
3. <span data-ttu-id="2150c-112">I feltet for **fakturajournalnavn** velger du en journal.</span><span class="sxs-lookup"><span data-stu-id="2150c-112">In the **Invoice journal name** field, select a journal.</span></span> <span data-ttu-id="2150c-113">Hvis alternativet **Betal til leverandør** er satt til **Ja** for leietablået, vil leie- og utgiftsbetalingsfakturaer posteres til dette journalnavnet.</span><span class="sxs-lookup"><span data-stu-id="2150c-113">If the **Pay to vendor** option is set to **Yes** for the lease book, lease and expense payment invoices will be posted to this journal name.</span></span>
4. <span data-ttu-id="2150c-114">I feltet for **leiejournalnavn** velger du en journal.</span><span class="sxs-lookup"><span data-stu-id="2150c-114">In the **Lease journal name** field, select a journal.</span></span> <span data-ttu-id="2150c-115">Alle poster for avskrivning, rente og kortsiktige omklassifiseringer vil bli postert til dette journalnavnet.</span><span class="sxs-lookup"><span data-stu-id="2150c-115">All depreciation, interest, and short-term reclassification entries will be posted to this journal name.</span></span> <span data-ttu-id="2150c-116">Hvis alternativet **Betal til leverandør** er satt til **Nei** for leietablået, vil leiebetalings- og utgiftsbetalingsoppføringer også posteres til dette journalnavnet.</span><span class="sxs-lookup"><span data-stu-id="2150c-116">If the **Pay to vendor** option is set to **No** for the lease book, lease payments and expense payment entries will also be posted to this journal name.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
