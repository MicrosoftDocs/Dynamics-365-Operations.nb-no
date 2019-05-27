---
title: Beregne og justere merverdiavgift på en leverandørfaktura
description: Hvis det opprinnelige kildedokumentet viser forskjellige mva-beløp som er beregnet, kan du justere disse beløpene før postering.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendInvoice, VendTableLookup, TaxTmpWorkTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 803c038d907b68a3c72a83a3e035c4e08b8a8661
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1545177"
---
# <a name="calculate-and-adjust-sales-tax-on-a-vendor-invoice"></a><span data-ttu-id="c2aec-103">Beregne og justere merverdiavgift på en leverandørfaktura</span><span class="sxs-lookup"><span data-stu-id="c2aec-103">Calculate and adjust sales tax on a vendor invoice</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c2aec-104">Hvis det opprinnelige kildedokumentet viser forskjellige mva-beløp som er beregnet, kan du justere disse beløpene før postering.</span><span class="sxs-lookup"><span data-stu-id="c2aec-104">If the original source document displays different tax amounts as calculated, you can adjust those amounts before posting.</span></span> <span data-ttu-id="c2aec-105">Denne oppgaven bruker demonstrasjonsfirmaet DEMF.</span><span class="sxs-lookup"><span data-stu-id="c2aec-105">This task uses the DEMF demo company.</span></span>

1. <span data-ttu-id="c2aec-106">Gå til Leverandører > Fakturaer > Fakturajournal.</span><span class="sxs-lookup"><span data-stu-id="c2aec-106">Go to Accounts payable > Invoices > Invoice journal.</span></span>
2. <span data-ttu-id="c2aec-107">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="c2aec-107">Click New.</span></span>
3. <span data-ttu-id="c2aec-108">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="c2aec-108">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="c2aec-109">Klikk rullegardinknappen i Navn-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="c2aec-109">In the Name field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="c2aec-110">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="c2aec-110">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="c2aec-111">Klikk Linjer.</span><span class="sxs-lookup"><span data-stu-id="c2aec-111">Click Lines.</span></span>
7. <span data-ttu-id="c2aec-112">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="c2aec-112">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="c2aec-113">Angi de ønskede verdiene i Konto-feltet.</span><span class="sxs-lookup"><span data-stu-id="c2aec-113">In the Account field, specify the desired values.</span></span>
9. <span data-ttu-id="c2aec-114">Skriv inn en verdi i Faktura-feltet.</span><span class="sxs-lookup"><span data-stu-id="c2aec-114">In the Invoice field, type a value.</span></span>
10. <span data-ttu-id="c2aec-115">Angi et tall i Kredit-feltet.</span><span class="sxs-lookup"><span data-stu-id="c2aec-115">In the Credit field, enter a number.</span></span>
11. <span data-ttu-id="c2aec-116">Angi ønskede verdier i Motkonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="c2aec-116">In the Offset account field, specify the desired values.</span></span>
12. <span data-ttu-id="c2aec-117">Klikk Merverdiavgift.</span><span class="sxs-lookup"><span data-stu-id="c2aec-117">Click Sales tax.</span></span>
13. <span data-ttu-id="c2aec-118">Angi et tall i feltet Totalt faktisk mva-beløp.</span><span class="sxs-lookup"><span data-stu-id="c2aec-118">In the Total actual sales tax amount field, enter a number.</span></span>
14. <span data-ttu-id="c2aec-119">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="c2aec-119">Click OK.</span></span>
15. <span data-ttu-id="c2aec-120">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="c2aec-120">Click Save.</span></span>
16. <span data-ttu-id="c2aec-121">Klikk Merverdiavgift.</span><span class="sxs-lookup"><span data-stu-id="c2aec-121">Click Sales tax.</span></span>
17. <span data-ttu-id="c2aec-122">Mva-beløp kan justeres per mva-kode i kategorien Justering.</span><span class="sxs-lookup"><span data-stu-id="c2aec-122">On the Adjustment tab, the sales tax amounts can be adjusted per sales tax code.</span></span>
18. <span data-ttu-id="c2aec-123">Klikk Tilbakestill faktiske fra beregnede beløp.</span><span class="sxs-lookup"><span data-stu-id="c2aec-123">Click Reset actual from calculated amounts.</span></span>
19. <span data-ttu-id="c2aec-124">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="c2aec-124">Click OK.</span></span>
20. <span data-ttu-id="c2aec-125">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="c2aec-125">Click Save.</span></span>

