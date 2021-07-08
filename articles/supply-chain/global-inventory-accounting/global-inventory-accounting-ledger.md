---
title: Global lagerregnskap-finansmodul
description: Dette emnet beskriver finansmoduler for Globale lagerregnskap, som er definert av en kombinasjon av en valuta, en kalender, en konvensjon og en tilknytning til en juridisk enhet.
author: AndersGirke
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: ea3434675aa3b7f2304be93ef9b489747994fa9d
ms.sourcegitcommit: eceae470f4ae58000ec33fea34db34b7a7a1af43
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/18/2021
ms.locfileid: "6273202"
---
# <a name="global-inventory-accounting-ledger"></a><span data-ttu-id="400ab-103">Global lagerregnskap-finansmodul</span><span class="sxs-lookup"><span data-stu-id="400ab-103">Global Inventory Accounting ledger</span></span>

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

<span data-ttu-id="400ab-104">Globalt lagerregnskap har et eget sett med finansmoduler.</span><span class="sxs-lookup"><span data-stu-id="400ab-104">Global Inventory Accounting has its own set of ledgers.</span></span> <span data-ttu-id="400ab-105">Hver gang en lagerrelatert transaksjon behandles for en relevant juridisk enhet, kan systemet ta hensyn til transaksjonen i et hvilket som helst antall Globalt lagerregnskap-finansmoduler, etter behov.</span><span class="sxs-lookup"><span data-stu-id="400ab-105">Each time an inventory-related transaction is processed for a relevant legal entity, the system can account for that transaction in any number of Global Inventory Accounting ledgers, as required.</span></span>

<span data-ttu-id="400ab-106">En finansmodul er et register av debet- og kreditoppføringer.</span><span class="sxs-lookup"><span data-stu-id="400ab-106">A ledger is a register of debit and credit measures.</span></span> <span data-ttu-id="400ab-107">Disse oppføringene klassifiseres ved hjelp av kostnadselementer og underregnskapskontoer.</span><span class="sxs-lookup"><span data-stu-id="400ab-107">These measures are classified by using cost elements and subledger accounts.</span></span> <span data-ttu-id="400ab-108">En finansmodul for Globalt lagerregnskap er definert av en kombinasjon av en valuta, en kalender, en konvensjon og en tilknytning til en juridisk enhet.</span><span class="sxs-lookup"><span data-stu-id="400ab-108">A Global Inventory Accounting ledger is defined by its combination of a currency, a calendar, a convention, and an association with a legal entity.</span></span>

<span data-ttu-id="400ab-109">Hvis du vil konfigurere finansmoduler for Globalt lagerregnskap, kan du gå til **Globalt lagerregnskap \> Oppsett \> Globalt lagerregnskap-finanskontoer**.</span><span class="sxs-lookup"><span data-stu-id="400ab-109">To set up your Global Inventory Accounting ledgers, go to **Global inventory accounting \> Setup \> Global inventory accounting ledgers**.</span></span> <span data-ttu-id="400ab-110">For hver finansmodul angir du feltene nedenfor:</span><span class="sxs-lookup"><span data-stu-id="400ab-110">For each ledger, set the following fields:</span></span>

- <span data-ttu-id="400ab-111">**Navn** – Angi navnet på finansmodulen.</span><span class="sxs-lookup"><span data-stu-id="400ab-111">**Name** – Enter the name of the ledger.</span></span>
- <span data-ttu-id="400ab-112">**Beskrivelse** – Angi en beskrivelse av finansmodulen.</span><span class="sxs-lookup"><span data-stu-id="400ab-112">**Description** – Enter a description of the ledger.</span></span>
- <span data-ttu-id="400ab-113">**Regnskapskalender** – Angi regnskapskalenderen for finansmodulen.</span><span class="sxs-lookup"><span data-stu-id="400ab-113">**Fiscal calendar** – Specify the fiscal calendar for the ledger.</span></span>
- <span data-ttu-id="400ab-114">**Valuta og valutakurstype** – Bruk feltene i denne hurtigfanen til å velge regnskapsvalutaen som finansmodulen bruker, og valutakurstypen.</span><span class="sxs-lookup"><span data-stu-id="400ab-114">**Currency and exchange rate type** – Use the fields on this FastTab to select the accounting currency that the ledger uses, and the exchange rate type.</span></span> <span data-ttu-id="400ab-115">Valutaen du velger, kan være forskjellig fra valutaen som den juridiske enheten bruker.</span><span class="sxs-lookup"><span data-stu-id="400ab-115">The currency that you select can differ from the currency that the legal entity uses.</span></span> <span data-ttu-id="400ab-116">I Globalt lagerregnskap kan brukere definere så mange finansmoduler for kostnader som de trenger.</span><span class="sxs-lookup"><span data-stu-id="400ab-116">In Global Inventory Accounting, users can define as many costing ledgers as they require.</span></span> <span data-ttu-id="400ab-117">Globalt lagerregnskap støtter lagerregnskap i flere valutaer og i flere vurderinger.</span><span class="sxs-lookup"><span data-stu-id="400ab-117">Global Inventory Accounting supports inventory accounting in multiple currencies and in multiple valuations.</span></span> <span data-ttu-id="400ab-118">Angi følgende felt:</span><span class="sxs-lookup"><span data-stu-id="400ab-118">Set the following fields:</span></span>

    - <span data-ttu-id="400ab-119">**Valuta** – Velg kostnadsvalutaen som lagerrelaterte verdier vedlikeholdes i.</span><span class="sxs-lookup"><span data-stu-id="400ab-119">**Currency** – Select the costing currency that inventory-related values are maintained in.</span></span> <span data-ttu-id="400ab-120">Disse verdiene omfatter lagerverdi, solgte varers kost, lager i transitt og alle typer avvik.</span><span class="sxs-lookup"><span data-stu-id="400ab-120">These values include the inventory value, cost of goods sold, inventory in transit, and all kinds of variance.</span></span>
    - <span data-ttu-id="400ab-121">**Valutakurstype** – Velg valutakursen som systemet skal bruke til å konvertere transaksjonsbeløpet i transaksjonsvalutaen og standardkostnaden for varene til kostnadsvalutaen.</span><span class="sxs-lookup"><span data-stu-id="400ab-121">**Exchange rate type** – Select the exchange rate that the system should use to convert the transaction amount in the transaction currency and the standard cost of the items into the costing currency.</span></span>

- <span data-ttu-id="400ab-122">**Konvensjonsnavn** – Angi en konvensjon.</span><span class="sxs-lookup"><span data-stu-id="400ab-122">**Convention name** – Specify a convention.</span></span> <span data-ttu-id="400ab-123">En konvensjon er en samling policyer som fastsetter hvordan kostnader blir regnskapsføres i denne finansmodulen.</span><span class="sxs-lookup"><span data-stu-id="400ab-123">A convention is a collection of policies that establish how costs will be accounted in this ledger.</span></span>
- <span data-ttu-id="400ab-124">**Juridisk enhet** – Finansmodulen vil ta hensyn til dokumentene som er postert til den valgte juridiske enheten.</span><span class="sxs-lookup"><span data-stu-id="400ab-124">**Legal entity** – The ledger will account the documents that are posted to the selected legal entity.</span></span>
- <span data-ttu-id="400ab-125">**Optimering** – Velg om lagertransaksjoner som ble opprettet før finansmodulen ble opprettet, skal behandles i henhold til valutaen og konvensjonen i finansmodulen.</span><span class="sxs-lookup"><span data-stu-id="400ab-125">**Priming** – Select whether inventory transactions that were created before the ledger was created should be processed according to the currency and convention in the ledger.</span></span> <span data-ttu-id="400ab-126">Velg én av følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="400ab-126">Select one of the following values:</span></span>

    - <span data-ttu-id="400ab-127">**Aktivert** – Finansmodulen skal behandle transaksjoner som ble opprettet før finansmodulen ble opprettet.</span><span class="sxs-lookup"><span data-stu-id="400ab-127">**Activated** – The ledger should process transactions that were created before the ledger was created.</span></span>
    - <span data-ttu-id="400ab-128">**Deaktivert** – Finansmodulen skal bare behandle transaksjoner som ble opprettet etter finansmodulen ble opprettet.</span><span class="sxs-lookup"><span data-stu-id="400ab-128">**Deactivated** – The ledger should process only transactions that are created after the ledger was created.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="400ab-129">Du kan **ikke** gå tilbake og angi dette feltet etter at du har lagt inn nye dokumenter.</span><span class="sxs-lookup"><span data-stu-id="400ab-129">You will **not** be able to come back and set this field after you enter new documents.</span></span>

- <span data-ttu-id="400ab-130">**Status** – Systemet setter automatisk statusen for nyopprettede finanmodulen til *Klargjør*.</span><span class="sxs-lookup"><span data-stu-id="400ab-130">**Status** – The system automatically sets the status of newly created ledgers to *Prepare*.</span></span>
