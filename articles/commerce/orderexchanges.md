---
title: Konfigurere og behandle en utveksling i en returordre
description: Dette emnet forklarer hvordan du konfigurerer en utveksling ved en retur i Dynamics 365 Commerce.
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
ms.openlocfilehash: a6d7688e78a375bc262b1156c5439c0fff7cd1f0
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004441"
---
# <a name="configure-and-process-an-exchange-on-a-return-order"></a><span data-ttu-id="97bb4-103">Konfigurere og behandle en utveksling i en returordre</span><span class="sxs-lookup"><span data-stu-id="97bb4-103">Configure and process an exchange on a return order</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="97bb4-104">I tidligere versjoner av Dynamics 365 Commerce ble returer mot kundeordrer behandlet ved hjelp av returordredokumentet i Headquarters.</span><span class="sxs-lookup"><span data-stu-id="97bb4-104">In previous versions of Dynamics 365 Commerce, returns against customer orders were processed by using the return order document in Headquarters.</span></span> <span data-ttu-id="97bb4-105">Returordredokumentet kan imidlertid brukes til å behandle bare produkter som returneres.</span><span class="sxs-lookup"><span data-stu-id="97bb4-105">However, the return order document can be used to process only products that are being returned.</span></span> <span data-ttu-id="97bb4-106">De returnerte produktene angis med et negativt antall på returordrelinjene.</span><span class="sxs-lookup"><span data-stu-id="97bb4-106">The returned products are indicated by a negative quantity on the return order lines.</span></span> <span data-ttu-id="97bb4-107">Derimot angis salg med et positivt antall.</span><span class="sxs-lookup"><span data-stu-id="97bb4-107">By contrast, sales are indicated by a positive quantity.</span></span> <span data-ttu-id="97bb4-108">Returordredokumentet støtter imidlertid ikke positive antall.</span><span class="sxs-lookup"><span data-stu-id="97bb4-108">However, the return order document doesn't support positive quantities.</span></span> <span data-ttu-id="97bb4-109">På grunn av denne begrensningen støttet ikke tidligere versjoner av appen scenarier der produktutvekslinger ble utført ved hjelp av returordredokumentet.</span><span class="sxs-lookup"><span data-stu-id="97bb4-109">Because of this limitation, previous versions of the app didn't support scenarios where product exchanges are done by using the return order document.</span></span>

<span data-ttu-id="97bb4-110">Funksjonaliteten er imidlertid lagt til for å støtte scenarier der utvekslinger blir utført på returordrer.</span><span class="sxs-lookup"><span data-stu-id="97bb4-110">However, functionality has been added to support scenarios where exchanges are done on return orders.</span></span> <span data-ttu-id="97bb4-111">Commerce bruker nå salgsordredokumentet i stedet for returordredokumentet til å behandle disse transaksjonstypene.</span><span class="sxs-lookup"><span data-stu-id="97bb4-111">Commerce now uses the sales order document instead of the return order document to process these types of transactions.</span></span>

## <a name="configure-commerce-to-support-exchanges-on-return-orders"></a><span data-ttu-id="97bb4-112">Konfigurere Commerce til å støtte utvekslinger på returordrer</span><span class="sxs-lookup"><span data-stu-id="97bb4-112">Configure Commerce to support exchanges on return orders</span></span>

<span data-ttu-id="97bb4-113">Følg denne fremgangsmåten for å konfigurere systemet til å støtte utvekslinger på returordrer.</span><span class="sxs-lookup"><span data-stu-id="97bb4-113">Follow these steps to configure the system to support exchanges on return orders.</span></span>

1. <span data-ttu-id="97bb4-114">Gå til **Detaljhandel og handel \> Hovedkvarteroppsett \> Parametere \> Handelsparametere**.</span><span class="sxs-lookup"><span data-stu-id="97bb4-114">Go to **Retail and Commerce \> Headquarters setup \> Parameters \> Commerce parameters**.</span></span> <span data-ttu-id="97bb4-115">Sett alternativet **Behandle returordrer som salgsordrer** til **Ja** i hurtigkategorien **Kundeordrer**.</span><span class="sxs-lookup"><span data-stu-id="97bb4-115">On the **Customer orders** FastTab, set the **Process return orders as sales orders** option to **Yes**.</span></span>
2. <span data-ttu-id="97bb4-116">Kjør jobben **Distribusjonsplan for global konfigurasjon** (**1110**).</span><span class="sxs-lookup"><span data-stu-id="97bb4-116">Run the **Global configuration distribution schedule** job (**1110**).</span></span>

## <a name="make-an-exchange"></a><span data-ttu-id="97bb4-117">Gjøre en utveksling</span><span class="sxs-lookup"><span data-stu-id="97bb4-117">Make an exchange</span></span>

<span data-ttu-id="97bb4-118">Etter at systemet er konfigurert som beskrevet i den forrige delen, vil salgsstedsbrukeren fortsatt velge en salgsordre eller salgsfaktura for å behandle en retur, som i tidligere versjoner av appen.</span><span class="sxs-lookup"><span data-stu-id="97bb4-118">After the system is configured as described in the previous section, the point of sale (POS) user will still select a sales order or sales invoice to process a return, as in previous versions of the app.</span></span> <span data-ttu-id="97bb4-119">Men etter at returvarene er lagt til handlekurven, kan brukeren legge til nye salgslinjer i handlekurven.</span><span class="sxs-lookup"><span data-stu-id="97bb4-119">However, after the return items are added to the cart, the user will be able to add new sales lines to the cart.</span></span>

<span data-ttu-id="97bb4-120">For disse nye salgslinjene må brukeren definere alle attributtene som kreves for å behandle en kundeordrelinje.</span><span class="sxs-lookup"><span data-stu-id="97bb4-120">For these new sales lines, the user must define all the attributes that are required in order to process a customer order line.</span></span> <span data-ttu-id="97bb4-121">Disse attributtene inkluderer leveringsmåten og oppfyllelseslokasjonen.</span><span class="sxs-lookup"><span data-stu-id="97bb4-121">These attributes include the delivery method and fulfillment location.</span></span> <span data-ttu-id="97bb4-122">Betalingen som forfaller for transaksjonen, blir en nettosum av returordrelinjene og salgsordrelinjene.</span><span class="sxs-lookup"><span data-stu-id="97bb4-122">The payment that is due for the transaction will be a net of the return order lines and sales order lines.</span></span> <span data-ttu-id="97bb4-123">Når betalingen er betalt for transaksjonen, blir returordren postert som et salgsordredokument i Headquarters, og systemet vil fakturere de returnerte linjene umiddelbart.</span><span class="sxs-lookup"><span data-stu-id="97bb4-123">When payment is tendered for the transaction, the return order will be posted as a sales order document in Headquarters, and the system will immediately invoice the return lines.</span></span>

<span data-ttu-id="97bb4-124">For å gi deg bedre oversikt over de ulike beløpene for handlekurven, er tre nye beløpsfelt lagt til i handlekurven.</span><span class="sxs-lookup"><span data-stu-id="97bb4-124">To provide better visibility into the various amounts for the cart, three new amount fields have been added to the cart.</span></span> <span data-ttu-id="97bb4-125">Du kan bruke skjermutformingen slik at disse nye feltene blir tilgjengelige i brukergrensesnittet for salgsstedet.</span><span class="sxs-lookup"><span data-stu-id="97bb4-125">You can use the screen designer to make these new fields available in the POS user interface (UI).</span></span>

- <span data-ttu-id="97bb4-126">**Brukt innbetaling** – Innbetalingsbeløpet som brukes for en transaksjon når brukeren utfører en kundeordrehenting.</span><span class="sxs-lookup"><span data-stu-id="97bb4-126">**Deposit applied** – The deposit amount that is applied on a transaction when the user does a customer order pickup.</span></span> <span data-ttu-id="97bb4-127">Hvis det ikke finnes overstyring av innbetaling, og en innbetaling på 10 prosent er konfigurert, vil beløpet i dette feltet være 90 prosent av totalbeløpet for kundeordren.</span><span class="sxs-lookup"><span data-stu-id="97bb4-127">If there is no deposit override, and a 10-percent deposit is configured, the amount in this field is 90 percent of the total amount of the customer order.</span></span>
- <span data-ttu-id="97bb4-128">**Utfør beløp** – Det totale beløpet for linjer der leveringsmåten ble satt til **Utfør** når kundeordren ble opprettet eller redigert, eller under en kundeordreutveksling.</span><span class="sxs-lookup"><span data-stu-id="97bb4-128">**Carry out amount** – The total amount for lines where the delivery mode was set to **Carry out** when the customer order was created or edited, or during a customer order exchange.</span></span> <span data-ttu-id="97bb4-129">Beløpet i dette feltet inneholder avgifter og tillegg.</span><span class="sxs-lookup"><span data-stu-id="97bb4-129">The amount in this field includes taxes and charges.</span></span>
- <span data-ttu-id="97bb4-130">**Returbeløp** – Det totale beløpet for linjer som har negative antall under kundeordreutvekslingen.</span><span class="sxs-lookup"><span data-stu-id="97bb4-130">**Return amount** – The total amount for lines that have negative quantities during the customer order exchange.</span></span> <span data-ttu-id="97bb4-131">Beløpet i dette feltet inneholder avgifter og tillegg.</span><span class="sxs-lookup"><span data-stu-id="97bb4-131">The amount in this field includes taxes and charges.</span></span>