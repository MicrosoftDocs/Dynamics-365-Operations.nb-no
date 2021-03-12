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
ms.openlocfilehash: 2536e87953267eae13cf3b42c2bd5476fc647c22
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994721"
---
# <a name="calculate-and-adjust-sales-tax-on-a-vendor-invoice"></a><span data-ttu-id="948b6-103">Beregne og justere merverdiavgift på en leverandørfaktura</span><span class="sxs-lookup"><span data-stu-id="948b6-103">Calculate and adjust sales tax on a vendor invoice</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="948b6-104">Dette emnet forklarer hvordan du justerer merverdiavgiften på en leverandørfaktura.</span><span class="sxs-lookup"><span data-stu-id="948b6-104">This topic explains how to adjust sales tax on a vendor invoice.</span></span> <span data-ttu-id="948b6-105">Hvis det opprinnelige kildedokumentet viser forskjellige mva-beløp som er beregnet, kan du justere disse beløpene før postering.</span><span class="sxs-lookup"><span data-stu-id="948b6-105">If the original source document displays different tax amounts as calculated, you can adjust those amounts before posting.</span></span> <span data-ttu-id="948b6-106">Denne oppgaven bruker demonstrasjonsfirmaet DEMF.</span><span class="sxs-lookup"><span data-stu-id="948b6-106">This task uses the DEMF demo company.</span></span>

1. <span data-ttu-id="948b6-107">Gå til **Moduler > Leverandører > Fakturaer > Fakturajournal** i navigasjonsruten.</span><span class="sxs-lookup"><span data-stu-id="948b6-107">In the navigation pane, go to **Modules > Accounts payable > Invoices > Invoice journal**.</span></span>
2. <span data-ttu-id="948b6-108">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="948b6-108">Select **New**.</span></span>
3. <span data-ttu-id="948b6-109">I **Navn**-feltet i den nye raden velger du et alternativ fra rullegardinmenyen.</span><span class="sxs-lookup"><span data-stu-id="948b6-109">In the **Name** field of the new row, select an option in the drop-down menu.</span></span>
4. <span data-ttu-id="948b6-110">Velg **Linjer** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="948b6-110">In the Action Pane, select **Lines**.</span></span>
5. <span data-ttu-id="948b6-111">Angi de ønskede verdiene i **Konto**-feltet.</span><span class="sxs-lookup"><span data-stu-id="948b6-111">In the **Account** field, specify the desired values.</span></span>
6. <span data-ttu-id="948b6-112">Skriv inn en verdi i **Faktura**-feltet.</span><span class="sxs-lookup"><span data-stu-id="948b6-112">In the **Invoice** field, type a value.</span></span>
7. <span data-ttu-id="948b6-113">Angi et tall i **Kredit**-feltet.</span><span class="sxs-lookup"><span data-stu-id="948b6-113">In the **Credit** field, enter a number.</span></span>
8. <span data-ttu-id="948b6-114">Angi ønskede verdier i **Motkonto**-feltet.</span><span class="sxs-lookup"><span data-stu-id="948b6-114">In the **Offset account** field, specify the desired values.</span></span>
9. <span data-ttu-id="948b6-115">Velg **Merverdiavgift**.</span><span class="sxs-lookup"><span data-stu-id="948b6-115">Select **Sales tax**.</span></span>
10. <span data-ttu-id="948b6-116">Angi et tall i feltet **Totalt faktisk mva-beløp**.</span><span class="sxs-lookup"><span data-stu-id="948b6-116">In the **Total actual sales tax amount** field, enter a number.</span></span>
11. <span data-ttu-id="948b6-117">Mva-beløp kan justeres per mva-kode i kategorien **Justering**.</span><span class="sxs-lookup"><span data-stu-id="948b6-117">On the **Adjustment** tab, the sales tax amounts can be adjusted per sales tax code.</span></span>
12. <span data-ttu-id="948b6-118">Velg **Tilbakestill faktiske fra beregnede beløp**.</span><span class="sxs-lookup"><span data-stu-id="948b6-118">Select **Reset actual from calculated amounts**.</span></span>
13. <span data-ttu-id="948b6-119">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="948b6-119">Select **OK**.</span></span>
14. <span data-ttu-id="948b6-120">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="948b6-120">Select **Save**.</span></span>

