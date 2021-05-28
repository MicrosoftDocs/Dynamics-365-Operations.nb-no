---
title: TaxTrans-post blir ikke generert
description: Dette emnet gir feilsøkingsinformasjon som kan være til hjelp når en TaxTrans-post ikke genereres.
author: qire
ms.date: 04/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 74987506699834d86703702106e5abf87bfa45da
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018787"
---
# <a name="taxtrans-record-isnt-generated"></a><span data-ttu-id="6f46e-103">TaxTrans-post blir ikke generert</span><span class="sxs-lookup"><span data-stu-id="6f46e-103">TaxTrans record isn't generated</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6f46e-104">Hvis du velger **Postert merverdiavgift** for en transaksjon, men **Postert merverdiavgift** -siden enten viser ingen mva-linjer eller mangler en mva-linje, kan det hende at **TaxTrans**-posten ikke er generert.</span><span class="sxs-lookup"><span data-stu-id="6f46e-104">If you select **Posted sales tax** for a transaction, but the **Posted sales tax** page either shows no tax lines or is missing a tax line, the **TaxTrans** record might not have been generated.</span></span>

<span data-ttu-id="6f46e-105">[![Postert merverdiavgift-side som ikke har noen linjeelementer](./media/taxtrans-is-not-generated-Picture1.png)](./media/taxtrans-is-not-generated-Picture1.png)</span><span class="sxs-lookup"><span data-stu-id="6f46e-105">[![Posted sales tax page that has no line items](./media/taxtrans-is-not-generated-Picture1.png)](./media/taxtrans-is-not-generated-Picture1.png)</span></span>

<span data-ttu-id="6f46e-106">Hvis du vil feilsøke dette problemet, følger du trinnene i de følgende delene etter behov.</span><span class="sxs-lookup"><span data-stu-id="6f46e-106">To troubleshoot this issue, follow the steps in the following sections as required.</span></span>

## <a name="check-the-sales-tax-before-you-post-the-transaction"></a><span data-ttu-id="6f46e-107">Kontroller merverdiavgiften før du posterer transaksjonen</span><span class="sxs-lookup"><span data-stu-id="6f46e-107">Check the sales tax before you post the transaction</span></span>

1. <span data-ttu-id="6f46e-108">Før du posterer transaksjonen, velger du **Merverdiavgift** på siden **Postering av faktura** for å kontrollere beregningen.</span><span class="sxs-lookup"><span data-stu-id="6f46e-108">Before you post the transaction, on the **Posting invoice** page, select **Sales tax** to check the calculation.</span></span>

    <span data-ttu-id="6f46e-109">[![Mva-knappen på Postering av faktura-siden](./media/taxtrans-is-not-generated-Picture2.png)](./media/taxtrans-is-not-generated-Picture2.png)</span><span class="sxs-lookup"><span data-stu-id="6f46e-109">[![Sales tax button on the Posting invoice page](./media/taxtrans-is-not-generated-Picture2.png)](./media/taxtrans-is-not-generated-Picture2.png)</span></span>

2. <span data-ttu-id="6f46e-110">Gå gjennom resultatet av beregningen på siden **Midlertidige mva-transaksjoner**.</span><span class="sxs-lookup"><span data-stu-id="6f46e-110">On the **Temporary sales tax transactions** page, review the result of the calculation.</span></span> <span data-ttu-id="6f46e-111">Hvis det ikke beregnes avgift, kan du se [Avgift beregnes ikke eller avgiftsbeløpet er null](sales-tax-troubleshooting-tax-not-calculated-amount-zero.md).</span><span class="sxs-lookup"><span data-stu-id="6f46e-111">If no tax is calculated, see [Tax isn't calculated or the tax amount is zero](sales-tax-troubleshooting-tax-not-calculated-amount-zero.md).</span></span>

## <a name="find-the-taxtrans-record-in-all-posted-sales-tax"></a><span data-ttu-id="6f46e-112">Finn TaxTrans-posten i all postert merverdiavgift</span><span class="sxs-lookup"><span data-stu-id="6f46e-112">Find the TaxTrans record in all posted sales tax</span></span>

1. <span data-ttu-id="6f46e-113">Gå til **Avgift** \> **Forespørsler og rapporter** \> **Merverdiavgiftforespørsler** > **Postert merverdiavgift**.</span><span class="sxs-lookup"><span data-stu-id="6f46e-113">Go to **Tax** \> **Inquiries and reports** \> **Sales tax inquiries** > **Posted sales tax**.</span></span>
2. <span data-ttu-id="6f46e-114">Velg filtersymbolet i **Bilag**-kolonneoverskriften for å finne **TaxTrans**-posten.</span><span class="sxs-lookup"><span data-stu-id="6f46e-114">In the **Voucher** column heading, select the filter symbol to find the **TaxTrans** record.</span></span>
3. <span data-ttu-id="6f46e-115">Hvis du finner mva-postene du leter etter, kan du kontrollere datoen.</span><span class="sxs-lookup"><span data-stu-id="6f46e-115">If you find the sales tax records that you're looking for, check the date.</span></span> <span data-ttu-id="6f46e-116">Hvis datoen er forskjellig fra datoen på journalhodet, oppretter du en Forespørsel om Microsoft-tjeneste for mer støtte.</span><span class="sxs-lookup"><span data-stu-id="6f46e-116">If the date differs from the date of the journal header, create a Microsoft service request for additional support.</span></span>

    <span data-ttu-id="6f46e-117">[![Siden Postert merverdiavgift](./media/taxtrans-is-not-generated-Picture4.png)](./media/taxtrans-is-not-generated-Picture4.png)</span><span class="sxs-lookup"><span data-stu-id="6f46e-117">[![Posted sales tax page](./media/taxtrans-is-not-generated-Picture4.png)](./media/taxtrans-is-not-generated-Picture4.png)</span></span>

## <a name="debug-to-check-details"></a><span data-ttu-id="6f46e-118">Feilsøke for å kontrollere detaljer</span><span class="sxs-lookup"><span data-stu-id="6f46e-118">Debug to check details</span></span>

1. <span data-ttu-id="6f46e-119">Hvis du vil ha mer informasjon om hvordan du feilsøker og finner ut om **TmpTaxWorkTrans** og **TaxUncommitted** er riktig generert, kan du se [Feltverdi i TaxTrans er feil](sales-tax-troubleshooting-field-value-taxtrans-incorrect.md).</span><span class="sxs-lookup"><span data-stu-id="6f46e-119">For information about how to debug and determine whether **TmpTaxWorkTrans** and **TaxUncommitted** are correctly generated, see [Field value in TaxTrans is incorrect](sales-tax-troubleshooting-field-value-taxtrans-incorrect.md).</span></span>
2. <span data-ttu-id="6f46e-120">Hvis **TaxTmpWorkTrans** eller **TaxUncommitted** genereres på riktig måte, legger du til et stoppunkt på **TaxPost::SaveAndPost()** og **Tax::SaveAndPost** for å feilsøke årsaken til at **TaxTrans** ikke er satt inn.</span><span class="sxs-lookup"><span data-stu-id="6f46e-120">If **TaxTmpWorkTrans** or **TaxUncommitted** is correctly generated, add a breakpoint at **TaxPost::SaveAndPost()** and **Tax::SaveAndPost** to debug the reason why **TaxTrans** isn't inserted.</span></span>

    <span data-ttu-id="6f46e-121">[![Stoppunkt som er lagt til i kode](./media/taxtrans-is-not-generated-Picture5.png)](./media/taxtrans-is-not-generated-Picture5.png)</span><span class="sxs-lookup"><span data-stu-id="6f46e-121">[![Breakpoints added in code](./media/taxtrans-is-not-generated-Picture5.png)](./media/taxtrans-is-not-generated-Picture5.png)</span></span>

    <span data-ttu-id="6f46e-122">[![Resultater av nye stoppunkter](./media/taxtrans-is-not-generated-Picture6.png)](./media/taxtrans-is-not-generated-Picture6.png)</span><span class="sxs-lookup"><span data-stu-id="6f46e-122">[![Results of added breakpoints](./media/taxtrans-is-not-generated-Picture6.png)](./media/taxtrans-is-not-generated-Picture6.png)</span></span>

## <a name="determine-whether-customization-exists"></a><span data-ttu-id="6f46e-123">Fastslå om det finnes tilpasning</span><span class="sxs-lookup"><span data-stu-id="6f46e-123">Determine whether customization exists</span></span>

<span data-ttu-id="6f46e-124">Hvis du har fullført trinnene i de forrige delene, men ikke har funnet problemet, må du avgjøre om det finnes tilpasning.</span><span class="sxs-lookup"><span data-stu-id="6f46e-124">If you've completed the steps in the previous sections but have found no issue, determine whether customization exists.</span></span> <span data-ttu-id="6f46e-125">Hvis det ikke finnes noen tilpasning, oppretter du en Microsoft-tjenesteforespørsel for mer støtte.</span><span class="sxs-lookup"><span data-stu-id="6f46e-125">If no customization exists, create a Microsoft service request for further support.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
