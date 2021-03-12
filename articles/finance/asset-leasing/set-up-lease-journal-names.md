---
title: Definere leiejournalnavn
description: Dette emnet forklarer hvordan du definerer navn på leierjournaler. Leiejournalnavn angir journalene som oppføringer som kommer fra aktivaleie, posteres til.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 89c5fc768aafe9e5de9adcde32e7b4d0a084941b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4990923"
---
# <a name="set-up-lease-journal-names"></a><span data-ttu-id="5aa7e-104">Definere leiejournalnavn</span><span class="sxs-lookup"><span data-stu-id="5aa7e-104">Set up lease journal names</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5aa7e-105">Leiejournalnavn angir journalene som aktivaleietransaksjoner posteres til.</span><span class="sxs-lookup"><span data-stu-id="5aa7e-105">Lease journal names specify the journals that Asset leasing transactions are posted to.</span></span> <span data-ttu-id="5aa7e-106">Bare journalnavn som er tilordnet til **Aktivaleie**-journaltyper, vises i feltene **Opprinnelig føring** og **Månedlig journalnavn** på siden **Parametere for aktivaleie**.</span><span class="sxs-lookup"><span data-stu-id="5aa7e-106">Only journal names that are assigned to the **Asset leasing** journal type appear in the **Initial Recognition** and **Monthly Journal Name** fields on the **Asset leasing parameters** page.</span></span> <span data-ttu-id="5aa7e-107">Bare journaltypen **registrering av leverandørfaktura** kan tilordnes til feltet for **fakturajournalnavn**.</span><span class="sxs-lookup"><span data-stu-id="5aa7e-107">Only **vendor invoice recording** journal type can be assigned to the **Invoice journal name** field.</span></span>

<span data-ttu-id="5aa7e-108">Følg denne fremgangsmåten for å konfigurere navn på leiejournaler:</span><span class="sxs-lookup"><span data-stu-id="5aa7e-108">To configure lease journal names, follow these steps.</span></span>

1. <span data-ttu-id="5aa7e-109">Gå til **Aktivaleie \> Oppsett \> Parametere for aktivaleie**.</span><span class="sxs-lookup"><span data-stu-id="5aa7e-109">Go to **Asset leasing \> Setup \> Asset leasing parameters**.</span></span>
2. <span data-ttu-id="5aa7e-110">Gå til kategorien **Generelt** i feltet **navn på journal for opprinnelig føring**, og velg en journal.</span><span class="sxs-lookup"><span data-stu-id="5aa7e-110">On the **General** tab, in the **Initial recognition journal name** field, and select a journal.</span></span> <span data-ttu-id="5aa7e-111">Alle journaloppføringer for opprinnelig føring posteres til dette journalnavnet.</span><span class="sxs-lookup"><span data-stu-id="5aa7e-111">All initial recognition journal entries will be posted to this journal name.</span></span>
3. <span data-ttu-id="5aa7e-112">I feltet for **fakturajournalnavn** velger du en journal.</span><span class="sxs-lookup"><span data-stu-id="5aa7e-112">In the **Invoice journal name** field, select a journal.</span></span> <span data-ttu-id="5aa7e-113">Hvis alternativet **Betal til leverandør** er satt til **Ja** for leietablået, vil leie- og utgiftsbetalingsfakturaer posteres til dette journalnavnet.</span><span class="sxs-lookup"><span data-stu-id="5aa7e-113">If the **Pay to vendor** option is set to **Yes** for the lease book, lease and expense payment invoices will be posted to this journal name.</span></span>
4. <span data-ttu-id="5aa7e-114">I feltet for **leiejournalnavn** velger du en journal.</span><span class="sxs-lookup"><span data-stu-id="5aa7e-114">In the **Lease journal name** field, select a journal.</span></span> <span data-ttu-id="5aa7e-115">Alle poster for avskrivning, rente og kortsiktige omklassifiseringer vil bli postert til dette journalnavnet.</span><span class="sxs-lookup"><span data-stu-id="5aa7e-115">All depreciation, interest, and short-term reclassification entries will be posted to this journal name.</span></span> <span data-ttu-id="5aa7e-116">Hvis alternativet **Betal til leverandør** er satt til **Nei** for leietablået, vil leiebetalings- og utgiftsbetalingsoppføringer også posteres til dette journalnavnet.</span><span class="sxs-lookup"><span data-stu-id="5aa7e-116">If the **Pay to vendor** option is set to **No** for the lease book, lease payments and expense payment entries will also be posted to this journal name.</span></span>
