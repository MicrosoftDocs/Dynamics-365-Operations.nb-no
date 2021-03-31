---
title: Beregne og justere merverdiavgift på en leverandørfaktura
description: Dette emnet forklarer hvordan du justerer merverdiavgiften på en leverandørfaktura i Dynamics 365 Finance.
author: twheeloc
manager: AnnBe
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendInvoice, VendTableLookup, TaxTmpWorkTrans
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f4d01fe7587e01c04af28be934a235d955455216
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5204743"
---
# <a name="calculate-and-adjust-sales-tax-on-a-vendor-invoice"></a><span data-ttu-id="561d7-103">Beregne og justere merverdiavgift på en leverandørfaktura</span><span class="sxs-lookup"><span data-stu-id="561d7-103">Calculate and adjust sales tax on a vendor invoice</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="561d7-104">Dette emnet forklarer hvordan du justerer merverdiavgiften på en leverandørfaktura.</span><span class="sxs-lookup"><span data-stu-id="561d7-104">This topic explains how to adjust sales tax on a vendor invoice.</span></span> <span data-ttu-id="561d7-105">Hvis det opprinnelige kildedokumentet viser forskjellige mva-beløp som er beregnet, kan du justere disse beløpene før postering.</span><span class="sxs-lookup"><span data-stu-id="561d7-105">If the original source document displays different tax amounts as calculated, you can adjust those amounts before posting.</span></span> <span data-ttu-id="561d7-106">Denne oppgaven bruker demonstrasjonsfirmaet DEMF.</span><span class="sxs-lookup"><span data-stu-id="561d7-106">This task uses the DEMF demo company.</span></span>

1. <span data-ttu-id="561d7-107">Gå til **Moduler > Leverandører > Fakturaer > Fakturajournal** i navigasjonsruten.</span><span class="sxs-lookup"><span data-stu-id="561d7-107">In the navigation pane, go to **Modules > Accounts payable > Invoices > Invoice journal**.</span></span>
2. <span data-ttu-id="561d7-108">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="561d7-108">Select **New**.</span></span>
3. <span data-ttu-id="561d7-109">I **Navn**-feltet i den nye raden velger du et alternativ fra rullegardinmenyen.</span><span class="sxs-lookup"><span data-stu-id="561d7-109">In the **Name** field of the new row, select an option in the drop-down menu.</span></span>
4. <span data-ttu-id="561d7-110">Velg **Linjer** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="561d7-110">In the Action Pane, select **Lines**.</span></span>
5. <span data-ttu-id="561d7-111">Angi de ønskede verdiene i **Konto**-feltet.</span><span class="sxs-lookup"><span data-stu-id="561d7-111">In the **Account** field, specify the desired values.</span></span>
6. <span data-ttu-id="561d7-112">Skriv inn en verdi i **Faktura**-feltet.</span><span class="sxs-lookup"><span data-stu-id="561d7-112">In the **Invoice** field, type a value.</span></span>
7. <span data-ttu-id="561d7-113">Angi et tall i **Kredit**-feltet.</span><span class="sxs-lookup"><span data-stu-id="561d7-113">In the **Credit** field, enter a number.</span></span>
8. <span data-ttu-id="561d7-114">Angi ønskede verdier i **Motkonto**-feltet.</span><span class="sxs-lookup"><span data-stu-id="561d7-114">In the **Offset account** field, specify the desired values.</span></span>
9. <span data-ttu-id="561d7-115">Velg **Merverdiavgift**.</span><span class="sxs-lookup"><span data-stu-id="561d7-115">Select **Sales tax**.</span></span>
10. <span data-ttu-id="561d7-116">Angi et tall i feltet **Totalt faktisk mva-beløp**.</span><span class="sxs-lookup"><span data-stu-id="561d7-116">In the **Total actual sales tax amount** field, enter a number.</span></span>
11. <span data-ttu-id="561d7-117">Mva-beløp kan justeres per mva-kode i kategorien **Justering**.</span><span class="sxs-lookup"><span data-stu-id="561d7-117">On the **Adjustment** tab, the sales tax amounts can be adjusted per sales tax code.</span></span>
12. <span data-ttu-id="561d7-118">Velg **Tilbakestill faktiske fra beregnede beløp**.</span><span class="sxs-lookup"><span data-stu-id="561d7-118">Select **Reset actual from calculated amounts**.</span></span>
13. <span data-ttu-id="561d7-119">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="561d7-119">Select **OK**.</span></span>
14. <span data-ttu-id="561d7-120">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="561d7-120">Select **Save**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]