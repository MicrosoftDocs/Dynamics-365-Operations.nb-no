---
title: Funksjonen for deling av faktura
description: Dette emnet beskriver oppsettet og funksjonen for deling av fakturaer etter leveringsadresse og TAN-nummer (Tax Account Number).
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
ms.openlocfilehash: 7dddbb9f69a9735c2a03d2b23928f5cb92d4e0fd
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023483"
---
# <a name="split-invoice-functionality"></a><span data-ttu-id="141b8-103">Funksjonen for deling av faktura</span><span class="sxs-lookup"><span data-stu-id="141b8-103">Split invoice functionality</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="141b8-104">Dette emnet beskriver oppsettet og funksjonen for deling av fakturaer etter leveringsadresse og TAN-nummer (Tax Account Number).</span><span class="sxs-lookup"><span data-stu-id="141b8-104">This topic describes the setup and functionality for splitting invoices by delivery address and tax account number (TAN).</span></span>

<span data-ttu-id="141b8-105">Merk av for **Produktkvittering** eller **Faktura** i **Generelt**-fanen på siden **Leverandørparametere** for å postere og dele en produktkvittering eller faktura som har ulike leveringsadresser eller TAN-numre på siden **Bestilling**.</span><span class="sxs-lookup"><span data-stu-id="141b8-105">On the **Accounts payable parameters** page, on the **General** tab, select the **Product receipt** or **Invoice** checkbox to post and split a product receipt or invoice that has different delivery addresses and TANs on the **Purchase order** page.</span></span> <span data-ttu-id="141b8-106">Den posterte fakturaen blir deretter delt etter leveringsadresse og TAN-nummer.</span><span class="sxs-lookup"><span data-stu-id="141b8-106">The posted invoice will then be split by delivery address and TAN.</span></span>

<span data-ttu-id="141b8-107">Sett alternativet **Bekreftelse**, **Plukkliste**, **Følgeseddel** eller **Faktura** til **Ja** i raden **Leveringsinformasjon** i hurtigfanen **Del basert på** i fanen **Samleoppdatering** for å postere og dele en bekreftelse, plukkliste, følgeseddel eller faktura der ulike leveringsadresser og TAN-numre er definert for ulike fakturalinjer på siden **Salgsordre**.</span><span class="sxs-lookup"><span data-stu-id="141b8-107">On the **Summary update** tab, on the **Split based on** FastTab, in the **Delivery information** row, set the **Confirmation**, **Picking list**, **Packing slip**, or **Invoice** option to **Yes** to post and split a confirmation, picking list, packing slip, or invoice where different delivery addresses and TANs are defined for different invoice lines on the **Sales order** page.</span></span> <span data-ttu-id="141b8-108">Fakturaen blir først delt etter leveringsadresse og deretter etter TAN-nummer.</span><span class="sxs-lookup"><span data-stu-id="141b8-108">The invoice will be split first by delivery address and then by TAN.</span></span>

> [!IMPORTANT]
> - <span data-ttu-id="141b8-109">Hvis ingen alternativer for **Leveringsinformasjon** er satt til **Ja**, blir fakturaen postert som én faktura.</span><span class="sxs-lookup"><span data-stu-id="141b8-109">If no options for **Delivery information** are set to **Yes**, the invoice will be posted as a single invoice.</span></span> <span data-ttu-id="141b8-110">Fakturaen blir ikke delt.</span><span class="sxs-lookup"><span data-stu-id="141b8-110">No invoice splitting will occur.</span></span>
> - <span data-ttu-id="141b8-111">Hvis du vil dele og postere en følgeseddel der fakturalinjene har ulike leveringsadresser og TAN-numre, må du sette alternativet **Følgeseddel** for **Leveringsinformasjon** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="141b8-111">To split and post a packing slip where the invoice lines have different delivery addresses and TANs, you must set the **Packing slip** option for **Delivery information** to **Yes**.</span></span>
> - <span data-ttu-id="141b8-112">Hvis du vil dele og postere en faktura der fakturalinjene har ulike leveringsadresser og TAN-numre, må du sette alternativet **Faktura** for **Leveringsinformasjon** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="141b8-112">To split and post an invoice where the invoice lines have different delivery addresses and TANs, you must set the **Invoice** option for **Delivery information** to **Yes**.</span></span>
> - <span data-ttu-id="141b8-113">Hvis du vil postere en faktura der fakturalinjene har ulike leveringsadresser, men samme TAN-nummer, setter du alternativet **Faktura** for **Leveringsinformasjon** til **Nei**.</span><span class="sxs-lookup"><span data-stu-id="141b8-113">To post an invoice where the invoice lines have different delivery addresses but the same TAN, set the **Invoice** option for **Delivery information** to **No**.</span></span> <span data-ttu-id="141b8-114">Fakturaen blir delt etter leveringsadresse.</span><span class="sxs-lookup"><span data-stu-id="141b8-114">The invoice will be split by delivery address.</span></span>

## <a name="example"></a><span data-ttu-id="141b8-115">Eksempel</span><span class="sxs-lookup"><span data-stu-id="141b8-115">Example</span></span>

<span data-ttu-id="141b8-116">I dette eksemplet er alternativet **Faktura** for **Leveringsinformasjon** satt til **Ja** i fanen **Samleoppdatering** på siden **Leverandørparametere**.</span><span class="sxs-lookup"><span data-stu-id="141b8-116">In this example, the **Invoice** option for **Delivery information** is set to **Yes** on the **Summary update** tab of the **Accounts payable parameters** page.</span></span> <span data-ttu-id="141b8-117">Det posteres en innkjøpsfaktura som har følgende oppsett for leveringsadresser og TAN-numre på linjene:</span><span class="sxs-lookup"><span data-stu-id="141b8-117">A purchase invoice is posted that has the following setup for delivery addresses and TANs on the lines:</span></span>

- <span data-ttu-id="141b8-118">**Varelinje 1:** Leveringsadresse 1, TAN-ABCD12345A</span><span class="sxs-lookup"><span data-stu-id="141b8-118">**Item line 1:** Delivery address 1, TAN-ABCD12345A</span></span>
- <span data-ttu-id="141b8-119">**Varelinje 2:** Leveringsadresse 1, TAN-ABCD12345A</span><span class="sxs-lookup"><span data-stu-id="141b8-119">**Item line 2:** Delivery address 1, TAN-ABCD12345A</span></span>
- <span data-ttu-id="141b8-120">**Varelinje 3:** Leveringsadresse 2, TAN-ABCE12345B</span><span class="sxs-lookup"><span data-stu-id="141b8-120">**Item line 3:** Delivery address 2, TAN-ABCE12345B</span></span>
- <span data-ttu-id="141b8-121">**Varelinje 4:** Leveringsadresse 3, TAN-ABCD12345A</span><span class="sxs-lookup"><span data-stu-id="141b8-121">**Item line 4:** Delivery address 3, TAN-ABCD12345A</span></span>

<span data-ttu-id="141b8-122">Den opprinnelige fakturaen blir i dette tilfellet delt i to fakturaer og postert på følgende måte:</span><span class="sxs-lookup"><span data-stu-id="141b8-122">In this case, the original invoice is split into two invoices and posted in the following way:</span></span>

- <span data-ttu-id="141b8-123">Faktura 1 posteres for varelinje 1 og varelinje 2 fordi begge linjene har samme leveringsadresse og TAN-nummer.</span><span class="sxs-lookup"><span data-stu-id="141b8-123">Invoice 1 is posted for item line 1 and item line 2, because both lines have the same delivery address and TAN.</span></span>
- <span data-ttu-id="141b8-124">Faktura 2 posteres for varelinje 3.</span><span class="sxs-lookup"><span data-stu-id="141b8-124">Invoice 2 is posted for item line 3.</span></span>
- <span data-ttu-id="141b8-125">Faktura 3 posteres for varelinje 4.</span><span class="sxs-lookup"><span data-stu-id="141b8-125">Invoice 3 is posted for item line 4.</span></span>
