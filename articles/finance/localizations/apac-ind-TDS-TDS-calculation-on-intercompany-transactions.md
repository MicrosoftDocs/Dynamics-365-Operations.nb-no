---
title: TDS-beregning for konserninterne transaksjoner
description: Dette emnet beskriver fremgangsmåten som brukes til å beregne TDS (Tax Deducted at Source) for konserninterne transaksjoner i faser.
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
ms.openlocfilehash: 0e304747cc93bfe0a39beababc3182ca14664b11
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023481"
---
# <a name="tds-calculation-on-intercompany-transactions"></a><span data-ttu-id="b04b3-103">TDS-beregning for konserninterne transaksjoner</span><span class="sxs-lookup"><span data-stu-id="b04b3-103">TDS calculation on intercompany transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b04b3-104">Dette emnet beskriver fremgangsmåten som brukes til å beregne TDS (Tax Deducted at Source) for konserninterne transaksjoner i faser.</span><span class="sxs-lookup"><span data-stu-id="b04b3-104">This topic describes the process that is used to calculate Tax Deducted at Source (TDS) on intercompany transactions in phases.</span></span>

<span data-ttu-id="b04b3-105">Når det opprettes en konsernintern bestilling eller salgsordre, brukes den standard TDS-gruppen som er definert for kunden eller leverandøren, til å beregne TDS-beløpet.</span><span class="sxs-lookup"><span data-stu-id="b04b3-105">When an intercompany purchase order or sales order is created, the default TDS group that is defined for the customer or vendor is used to calculate the TDS amount.</span></span> <span data-ttu-id="b04b3-106">TDS-beløpet posteres på fradragskontoene eller leverandørreskontroene etter at fakturaen er postert.</span><span class="sxs-lookup"><span data-stu-id="b04b3-106">The TDS amount is posted to the recoverable or payable accounts after the invoice is posted.</span></span>

<span data-ttu-id="b04b3-107">En konsernintern salgsordre eller bestilling opprettes automatisk for den opprinnelige bestillingen eller salgsordren.</span><span class="sxs-lookup"><span data-stu-id="b04b3-107">An intercompany sales order or purchase order is automatically created for the original purchase order or sales order.</span></span> <span data-ttu-id="b04b3-108">Standard TDS-gruppe vises i den konserninterne ordren, slik at TDS kan beregnes.</span><span class="sxs-lookup"><span data-stu-id="b04b3-108">The default TDS group is shown on the intercompany order, so that TDS can be calculated.</span></span> <span data-ttu-id="b04b3-109">Du kan endre TDS-gruppen.</span><span class="sxs-lookup"><span data-stu-id="b04b3-109">You can change the TDS group.</span></span> <span data-ttu-id="b04b3-110">Fakturaen kan bare posteres hvis netto fakturabeløp i den konserninterne ordren som opprettes automatisk, er i samsvar med netto fakturabeløp i den opprinnelige ordren.</span><span class="sxs-lookup"><span data-stu-id="b04b3-110">The invoice can be posted only if the net invoice amount on the intercompany order that is automatically created matches the net invoice amount on the original order.</span></span> <span data-ttu-id="b04b3-111">(Nettobeløpet er fakturabeløpet etter at TDS er trukket fra.)</span><span class="sxs-lookup"><span data-stu-id="b04b3-111">(The net amount is the invoice amount after TDS is deducted.)</span></span>

<span data-ttu-id="b04b3-112">La oss si at en salgsfaktura opprettes for 50 000 og TDS-gruppen **10 %** er knyttet til den.</span><span class="sxs-lookup"><span data-stu-id="b04b3-112">For example, a sales invoice is created for 50,000, and the **10%** TDS group is attached to it.</span></span> <span data-ttu-id="b04b3-113">Det posterte fakturabeløpet er 45 000, og det posterte TDS-beløpet for salgsfakturaen er 5 000.</span><span class="sxs-lookup"><span data-stu-id="b04b3-113">The posted invoice amount is 45,000, and the posted TDS amount for the sales invoice is 5,000.</span></span> <span data-ttu-id="b04b3-114">Det opprettes automatisk en bestilling for den konserninterne salgsordren, og TDS-gruppen **10 %** er knyttet til den.</span><span class="sxs-lookup"><span data-stu-id="b04b3-114">A purchase order is automatically created for the intercompany sales order, and the  **10%** TDS group is attached to it.</span></span> <span data-ttu-id="b04b3-115">Hvis du endrer TDS-gruppen til **15 %**, kan du ikke postere fakturaen, fordi netto fakturabeløp i den konserninterne salgsordren som ble opprettet automatisk, ikke samsvarer med netto fakturabeløp for den opprinnelige salgsordren.</span><span class="sxs-lookup"><span data-stu-id="b04b3-115">If you change the TDS group to **15%**, you can't post the invoice, because the net invoice amount of the intercompany sales order that was automatically created doesn't match the net invoice amount of the original sales order.</span></span>

<span data-ttu-id="b04b3-116">En betalingsjournal som opprettes for en konsernintern faktura, posteres automatisk.</span><span class="sxs-lookup"><span data-stu-id="b04b3-116">A payment journal that is created for an intercompany invoice is automatically posted.</span></span> <span data-ttu-id="b04b3-117">Denne betalingsjournalen kan bare posteres hvis netto betalingsbeløp på den er i samsvar med netto betalingsbeløp i den opprinnelige betalingsjournalen.</span><span class="sxs-lookup"><span data-stu-id="b04b3-117">That payment journal can be posted only if the net payment amount on it matches the net payment amount on the original payment journal.</span></span>
