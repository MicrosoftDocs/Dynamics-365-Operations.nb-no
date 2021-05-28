---
title: Feil feltverdi i TaxTrans
description: Dette emnet gir informasjon om feilsøking av feil feltverdier i TaxTrans.
author: bijian
ms.date: 04/27/2021
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
ms.openlocfilehash: 488ff54f1dd99208db940024a2fe8b2d25861f44
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020169"
---
# <a name="incorrect-field-value-in-taxtrans"></a><span data-ttu-id="ec945-103">Feil feltverdi i TaxTrans</span><span class="sxs-lookup"><span data-stu-id="ec945-103">Incorrect field value in TaxTrans</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ec945-104">Hvis en feltverdi i **TaxTrans** er feil, bruker du informasjonen i dette emnet til å forsøke å løse problemet.</span><span class="sxs-lookup"><span data-stu-id="ec945-104">If a field value in **TaxTrans** is incorrect, use the information in this topic to try to resolve the issue.</span></span>

## <a name="overview-of-values"></a><span data-ttu-id="ec945-105">Oversikt over verdier</span><span class="sxs-lookup"><span data-stu-id="ec945-105">Overview of values</span></span>
<span data-ttu-id="ec945-106">Listen nedenfor viser hvordan **TaxTrans**, **TaxUncommitted** og **TmpTaxWorkTrans** er lignende datasett, men fungerer annerledes.</span><span class="sxs-lookup"><span data-stu-id="ec945-106">The following list shows how **TaxTrans**, **TaxUncommitted**, and **TmpTaxWorkTrans** are similar data sets, but in work differently.</span></span>

  - <span data-ttu-id="ec945-107">**TaxTrans** er det siste posterte mva-transaksjonsresultatet som fastholdes i databasen.</span><span class="sxs-lookup"><span data-stu-id="ec945-107">**TaxTrans** is the final posted tax transaction result persisted in the database.</span></span>
  - <span data-ttu-id="ec945-108">**TaxUncommitted** er resultatet av midlertidig beregnet avgift som fastholdes i databasen (om nødvendig), som senere vil bli brukt til postering.</span><span class="sxs-lookup"><span data-stu-id="ec945-108">**TaxUncommitted** is the intermediate calculated tax result persisted in the database (if applicable), which will be used later in posting.</span></span>
  - <span data-ttu-id="ec945-109">**TmpTaxWorkTrans** er resultatet av midlertidig beregnet avgift i minnetabellen (tabelltype = InMemory).</span><span class="sxs-lookup"><span data-stu-id="ec945-109">**TmpTaxWorkTrans** is the temporary calculated tax result in the in-memory table (Table Type = InMemory).</span></span>

<span data-ttu-id="ec945-110">Hvis du finner rotårsaken til en feil **TaxTrans**-kolonne, har du også funnet rotårsaken til en feil **TaxUncommitted**- eller **TmpTaxWorkTrans**-kolonne.</span><span class="sxs-lookup"><span data-stu-id="ec945-110">If you find the root cause of an incorrect **TaxTrans** column, you've also found the root cause of an incorrect **TaxUncommitted** or **TmpTaxWorkTrans** column.</span></span> <span data-ttu-id="ec945-111">Det er fordi de tre kolonnene kopieres fra hverandre.</span><span class="sxs-lookup"><span data-stu-id="ec945-111">This is because the three columns are copied from each other.</span></span>

<span data-ttu-id="ec945-112">Vanligvis genereres **TmpTaxWorkTrans** under avgiftsberegning, og hvis det er aktuelt, genereres **TaxUncommitted**.</span><span class="sxs-lookup"><span data-stu-id="ec945-112">Typically, during tax calculation, **TmpTaxWorkTrans** is generated, and then, if applicable, **TaxUncommitted** is generated.</span></span> <span data-ttu-id="ec945-113">Under avgiftspostering genereres **TaxTrans**.</span><span class="sxs-lookup"><span data-stu-id="ec945-113">During tax posting, **TaxTrans** is generated.</span></span>


## <a name="add-breakpoints"></a><span data-ttu-id="ec945-114">Legge til stoppunkt</span><span class="sxs-lookup"><span data-stu-id="ec945-114">Add breakpoints</span></span>
<span data-ttu-id="ec945-115">Fullfør fremgangsmåten nedenfor for legge til stoppunkt:</span><span class="sxs-lookup"><span data-stu-id="ec945-115">To add breakpoints, complete the following steps:</span></span> 

1. <span data-ttu-id="ec945-116">Legg til utvidelser og stoppunkt i *insert()* og *update()* i tilleggene som vist nedenfor.</span><span class="sxs-lookup"><span data-stu-id="ec945-116">Add extensions and breakpoints in *insert()* and *update()* in the extensions as shown below.</span></span>

     - <span data-ttu-id="ec945-117">**TaxTrans**</span><span class="sxs-lookup"><span data-stu-id="ec945-117">**TaxTrans**</span></span>

        ```x++
        [ExtensionOf(tableStr(TaxTrans))]
        public final class TaxTrans_Extension
        {
            public void insert()
            {
                next insert();
            }
        
            public void update()
            {
                next update();
            }
        
        }
        ```

     - <span data-ttu-id="ec945-118">**TaxUncommitted**</span><span class="sxs-lookup"><span data-stu-id="ec945-118">**TaxUncommitted**</span></span>

        ```x++
        [ExtensionOf(tableStr(TaxUncommitted))]
        public final class TaxUncommitted_Extension
        {
            public void insert()
            {
                next insert();
            }
        
            public void update()
            {
                next update();
            }
        
        }
        ```

     - <span data-ttu-id="ec945-119">**TmpTaxWorkTrans**</span><span class="sxs-lookup"><span data-stu-id="ec945-119">**TmpTaxWorkTrans**</span></span>

        ```x++
        [ExtensionOf(tableStr(TmpTaxWorkTrans))]
        public final class TmpTaxWorkTrans_Extension
        {
            public void insert(boolean _ignoreCalculatedSalesTax)
            {
                next insert(_ignoreCalculatedSalesTax);
            }
        
            public void update(boolean _ignoreCalculatedSalesTax)
            {
                next update(_ignoreCalculatedSalesTax);
            }
        
        }
        
        ```

2. <span data-ttu-id="ec945-120">Du kan også legge til stoppunkt direkte når **TaxUncommitted** ikke er inkludert.</span><span class="sxs-lookup"><span data-stu-id="ec945-120">Alternatively, you can add breakpoints directly when **TaxUncommitted** is not included.</span></span>

     - <span data-ttu-id="ec945-121">*TaxTrans.insert()*, *TaxTrans.update()*</span><span class="sxs-lookup"><span data-stu-id="ec945-121">*TaxTrans.insert()*, *TaxTrans.update()*</span></span>
     - <span data-ttu-id="ec945-122">*TmpTaxWorkTrans.insert()*, *TmpTaxWorkTrans.update()*</span><span class="sxs-lookup"><span data-stu-id="ec945-122">*TmpTaxWorkTrans.insert()*, *TmpTaxWorkTrans.update()*</span></span>

## <a name="reproduce-and-debug"></a><span data-ttu-id="ec945-123">Reprodusere og feilsøke</span><span class="sxs-lookup"><span data-stu-id="ec945-123">Reproduce and debug</span></span>

<span data-ttu-id="ec945-124">Når stoppunktene er angitt, vises alle endringer i data ved feilsøking.</span><span class="sxs-lookup"><span data-stu-id="ec945-124">After the breakpoints are set, every data persistency change is visible during debugging.</span></span> <span data-ttu-id="ec945-125">Hvis du vil finne rotårsaken til feil kolonne i **TaxTrans**, **TaxUncommitted** eller **TmpTaxWorkTrans**, kan du se gjennom og legge merke til følgende elementer:</span><span class="sxs-lookup"><span data-stu-id="ec945-125">To find the root cause of an incorrect column of **TaxTrans**, **TaxUncommitted**, or **TmpTaxWorkTrans**, review and note the following items:</span></span>

- <span data-ttu-id="ec945-126">Det siste stoppunktet der kolonnen er riktig.</span><span class="sxs-lookup"><span data-stu-id="ec945-126">The last breakpoint where the column is correct.</span></span>
- <span data-ttu-id="ec945-127">Det første stoppunktet der kolonnen er uriktig.</span><span class="sxs-lookup"><span data-stu-id="ec945-127">The first breakpoint where the column is incorrect.</span></span>
- <span data-ttu-id="ec945-128">Hva som skjer mellom disse to punktene.</span><span class="sxs-lookup"><span data-stu-id="ec945-128">What happens in between those two points.</span></span>

## <a name="determine-whether-customization-exists"></a><span data-ttu-id="ec945-129">Fastslå om det finnes tilpasning</span><span class="sxs-lookup"><span data-stu-id="ec945-129">Determine whether customization exists</span></span>
<span data-ttu-id="ec945-130">Hvis du har fullført trinnene i de forrige delene, men ikke kunne løse problemet, må du avgjøre om det finnes tilpasning.</span><span class="sxs-lookup"><span data-stu-id="ec945-130">If you've completed the steps in the previous sections but have not been able to resolve the issue, determine whether customization exists.</span></span> <span data-ttu-id="ec945-131">Hvis det ikke finnes noen tilpasning, kan du kontakte Microsoft Kundestøtte for hjelp.</span><span class="sxs-lookup"><span data-stu-id="ec945-131">If no customization exists, contact Microsoft Support for assistance.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

