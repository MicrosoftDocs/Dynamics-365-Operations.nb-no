---
title: Konfigurere og behandle en utveksling i en returordre
description: Dette emnet forklarer hvordan du konfigurerer en utveksling ved en retur i Microsoft Dynamics 365 for Retail.
author: josaw1
manager: AnnBe
ms.date: 11/12/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 45b628376a483d3d639e5c018dd93570ed8ce7af
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "302683"
---
# <a name="configure-and-process-an-exchange-on-a-return-order"></a><span data-ttu-id="d165b-103">Konfigurere og behandle en utveksling i en returordre</span><span class="sxs-lookup"><span data-stu-id="d165b-103">Configure and process an exchange on a return order</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d165b-104">I tidligere versjoner av Microsoft Dynamics 365 for Retail ble returer mot kundeordrer behandlet ved hjelp av returordredokumentet i Retail Headquarters.</span><span class="sxs-lookup"><span data-stu-id="d165b-104">In previous versions of Microsoft Dynamics 365 for Retail, returns against customer orders were processed by using the return order document in Retail headquarters.</span></span> <span data-ttu-id="d165b-105">Returordredokumentet kan imidlertid brukes til å behandle bare produkter som returneres.</span><span class="sxs-lookup"><span data-stu-id="d165b-105">However, the return order document can be used to process only products that are being returned.</span></span> <span data-ttu-id="d165b-106">De returnerte produktene angis med et negativt antall på returordrelinjene.</span><span class="sxs-lookup"><span data-stu-id="d165b-106">The returned products are indicated by a negative quantity on the return order lines.</span></span> <span data-ttu-id="d165b-107">Derimot angis salg med et positivt antall.</span><span class="sxs-lookup"><span data-stu-id="d165b-107">By contrast, sales are indicated by a positive quantity.</span></span> <span data-ttu-id="d165b-108">Returordredokumentet støtter imidlertid ikke positive antall.</span><span class="sxs-lookup"><span data-stu-id="d165b-108">However, the return order document doesn't support positive quantities.</span></span> <span data-ttu-id="d165b-109">På grunn av denne begrensningen støttet ikke tidligere versjoner av Retail scenarier der produktutvekslinger ble utført ved hjelp av returordredokumentet.</span><span class="sxs-lookup"><span data-stu-id="d165b-109">Because of this limitation, previous versions of Retail didn't support scenarios where product exchanges are done by using the return order document.</span></span>

<span data-ttu-id="d165b-110">Funksjonaliteten er imidlertid lagt til for å støtte scenarier der utvekslinger blir utført på returordrer.</span><span class="sxs-lookup"><span data-stu-id="d165b-110">However, functionality has been added to support scenarios where exchanges are done on return orders.</span></span> <span data-ttu-id="d165b-111">Retail bruker nå salgsordredokumentet i stedet for returordredokumentet til å behandle disse transaksjonstypene.</span><span class="sxs-lookup"><span data-stu-id="d165b-111">Retail now uses the sales order document instead of the return order document to process these types of transactions.</span></span>

## <a name="configure-retail-to-support-exchanges-on-return-orders"></a><span data-ttu-id="d165b-112">Konfigurere Retail til å støtte utvekslinger på returordrer</span><span class="sxs-lookup"><span data-stu-id="d165b-112">Configure Retail to support exchanges on return orders</span></span>

<span data-ttu-id="d165b-113">Følg denne fremgangsmåten for å konfigurere systemet til å støtte utvekslinger på returordrer.</span><span class="sxs-lookup"><span data-stu-id="d165b-113">Follow these steps to configure the system to support exchanges on return orders.</span></span>

1. <span data-ttu-id="d165b-114">Gå til **Retail \> Hovedkvarteroppsett \> Parametere \> Detaljhandelsparametere**.</span><span class="sxs-lookup"><span data-stu-id="d165b-114">Go to **Retail \> Headquarters setup \> Parameters \> Retail parameters**.</span></span> <span data-ttu-id="d165b-115">Sett alternativet **Behandle returordrer som salgsordrer** til **Ja** i hurtigkategorien **Kundeordrer**.</span><span class="sxs-lookup"><span data-stu-id="d165b-115">On the **Customer orders** FastTab, set the **Process return orders as sales orders** option to **Yes**.</span></span>
2. <span data-ttu-id="d165b-116">Kjør jobben **Distribusjonsplan for global konfigurasjon** (**1110**).</span><span class="sxs-lookup"><span data-stu-id="d165b-116">Run the **Global configuration distribution schedule** job (**1110**).</span></span>

## <a name="make-an-exchange"></a><span data-ttu-id="d165b-117">Gjøre en utveksling</span><span class="sxs-lookup"><span data-stu-id="d165b-117">Make an exchange</span></span>

<span data-ttu-id="d165b-118">Etter at systemet er konfigurert som beskrevet i den forrige delen, vil salgsstedsbrukeren fortsatt velge en salgsordre eller salgsfaktura for å behandle en retur, som i tidligere versjoner av Retail.</span><span class="sxs-lookup"><span data-stu-id="d165b-118">After the system is configured as described in the previous section, the point of sale (POS) user will still select a sales order or sales invoice to process a return, as in previous versions of Retail.</span></span> <span data-ttu-id="d165b-119">Men etter at returvarene er lagt til handlekurven, kan brukeren legge til nye salgslinjer i handlekurven.</span><span class="sxs-lookup"><span data-stu-id="d165b-119">However, after the return items are added to the cart, the user will be able to add new sales lines to the cart.</span></span>

<span data-ttu-id="d165b-120">For disse nye salgslinjene må brukeren definere alle attributtene som kreves for å behandle en kundeordrelinje.</span><span class="sxs-lookup"><span data-stu-id="d165b-120">For these new sales lines, the user must define all the attributes that are required in order to process a customer order line.</span></span> <span data-ttu-id="d165b-121">Disse attributtene inkluderer leveringsmåten og oppfyllelseslokasjonen.</span><span class="sxs-lookup"><span data-stu-id="d165b-121">These attributes include the delivery method and fulfillment location.</span></span> <span data-ttu-id="d165b-122">Betalingen som forfaller for transaksjonen, blir en nettosum av returordrelinjene og salgsordrelinjene.</span><span class="sxs-lookup"><span data-stu-id="d165b-122">The payment that is due for the transaction will be a net of the return order lines and sales order lines.</span></span> <span data-ttu-id="d165b-123">Når betalingen er betalt for transaksjonen, blir returordren postert som et salgsordredokument i Retail Headquarters, og systemet vil fakturere de returnerte linjene umiddelbart.</span><span class="sxs-lookup"><span data-stu-id="d165b-123">When payment is tendered for the transaction, the return order will be posted as a sales order document in Retail headquarters, and the system will immediately invoice the return lines.</span></span>

<span data-ttu-id="d165b-124">For å gi deg bedre oversikt over de ulike beløpene for handlekurven, er tre nye beløpsfelt lagt til i handlekurven.</span><span class="sxs-lookup"><span data-stu-id="d165b-124">To provide better visibility into the various amounts for the cart, three new amount fields have been added to the cart.</span></span> <span data-ttu-id="d165b-125">Du kan bruke skjermutformingen slik at disse nye feltene blir tilgjengelige i brukergrensesnittet for salgsstedet.</span><span class="sxs-lookup"><span data-stu-id="d165b-125">You can use the screen designer to make these new fields available in the POS user interface (UI).</span></span>

- <span data-ttu-id="d165b-126">**Brukt innbetaling** – Innbetalingsbeløpet som brukes for en transaksjon når brukeren utfører en kundeordrehenting.</span><span class="sxs-lookup"><span data-stu-id="d165b-126">**Deposit applied** – The deposit amount that is applied on a transaction when the user does a customer order pickup.</span></span> <span data-ttu-id="d165b-127">Hvis det ikke finnes overstyring av innbetaling, og en innbetaling på 10 prosent er konfigurert, vil beløpet i dette feltet være 90 prosent av totalbeløpet for kundeordren.</span><span class="sxs-lookup"><span data-stu-id="d165b-127">If there is no deposit override, and a 10-percent deposit is configured, the amount in this field is 90 percent of the total amount of the customer order.</span></span>
- <span data-ttu-id="d165b-128">**Utfør beløp** – Det totale beløpet for linjer der leveringsmåten ble satt til **Utfør** når kundeordren ble opprettet eller redigert, eller under en kundeordreutveksling.</span><span class="sxs-lookup"><span data-stu-id="d165b-128">**Carry out amount** – The total amount for lines where the delivery mode was set to **Carry out** when the customer order was created or edited, or during a customer order exchange.</span></span> <span data-ttu-id="d165b-129">Beløpet i dette feltet inneholder avgifter og tillegg.</span><span class="sxs-lookup"><span data-stu-id="d165b-129">The amount in this field includes taxes and charges.</span></span>
- <span data-ttu-id="d165b-130">**Returbeløp** – Det totale beløpet for linjer som har negative antall under kundeordreutvekslingen.</span><span class="sxs-lookup"><span data-stu-id="d165b-130">**Return amount** – The total amount for lines that have negative quantities during the customer order exchange.</span></span> <span data-ttu-id="d165b-131">Beløpet i dette feltet inneholder avgifter og tillegg.</span><span class="sxs-lookup"><span data-stu-id="d165b-131">The amount in this field includes taxes and charges.</span></span>
