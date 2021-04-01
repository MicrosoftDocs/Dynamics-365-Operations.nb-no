---
title: Postere med avledede tablåer
description: Denne artikkelen beskriver hvordan du bruker avledede tablåer.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBookTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: roschlom
ms.custom: 3421
ms.assetid: f5187c21-eec5-4148-b178-b8a5feff7f23
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 628110e62d30a717b243530367196aeaf930e3e3
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5256745"
---
# <a name="post-with-derived-books"></a><span data-ttu-id="39800-103">Postere med avledede tablåer</span><span class="sxs-lookup"><span data-stu-id="39800-103">Post with derived books</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="39800-104">Denne artikkelen beskriver hvordan du bruker avledede tablåer.</span><span class="sxs-lookup"><span data-stu-id="39800-104">This article describes how to use derived books.</span></span>

<span data-ttu-id="39800-105">Når du posterer transaksjoner for et tablå som inneholder avledede tablåer, posteres de avledede tablåtransaksjoner automatisk i journaler, bestillinger eller fritekstfakturaer.</span><span class="sxs-lookup"><span data-stu-id="39800-105">When you post transactions for a book that contains derived books, the derived book transactions are posted automatically in journals, purchase orders, or free text invoices.</span></span> <span data-ttu-id="39800-106">Hvis du forbereder de primære tablåtransaksjonene i anleggsmiddeljournalen, kan du imidlertid vise og endre beløpene i de avledede transaksjonene før du posterer dem.</span><span class="sxs-lookup"><span data-stu-id="39800-106">However, if you prepare the primary book transactions in the Fixed assets journal, you can view and modify the amounts of the derived transactions before you post them.</span></span>
-   <span data-ttu-id="39800-107">Enkelt kontoer, for eksempel mva-kontoer og kunde- eller leverandørkontoer, oppdateres bare én gang ved hjelp av posteringer av det primære tablået.</span><span class="sxs-lookup"><span data-stu-id="39800-107">Certain accounts, such as sales tax and customer or vendor accounts, are updated only once by postings of the primary book.</span></span> <span data-ttu-id="39800-108">De avledede tablåtransaksjonene posteres til kontoene som er definert for det avledede tablået på siden Posteringsprofiler for anleggsmidler.</span><span class="sxs-lookup"><span data-stu-id="39800-108">The derived book transactions are posted to the accounts that have been defined for the derived book in the Fixed asset posting profiles page.</span></span>
-   <span data-ttu-id="39800-109">Anskaffelse brukes ofte som transaksjonstypen for de avledede tablåene.</span><span class="sxs-lookup"><span data-stu-id="39800-109">Acquisition is often used as the transaction type for the derived books.</span></span> <span data-ttu-id="39800-110">Du bruker dette når tablået og det avledede tablået skal brukes på anleggsmiddelet fra tidspunktet anleggsmiddelet ble anskaffet.</span><span class="sxs-lookup"><span data-stu-id="39800-110">You use this when the book and the derived book should be applied to the fixed asset from the time of the acquisition of the fixed asset.</span></span>
-   <span data-ttu-id="39800-111">Andre verdier for transaksjonstypen kan også brukes.</span><span class="sxs-lookup"><span data-stu-id="39800-111">Other values for the transaction type can also apply.</span></span> <span data-ttu-id="39800-112">Hvis for eksempel det primære tablået og de avledede tablåene har samme intervaller når det gjelder salg eller avhending, er alle anleggsmiddeltransaksjonstyper tilgjengelige for oppsett av et avledet tablå.</span><span class="sxs-lookup"><span data-stu-id="39800-112">For example, if the primary book and the derived books have the same intervals regarding sale or disposal, all fixed asset transaction types are available for the setup of a derived book.</span></span>

> [!WARNING]
> <span data-ttu-id="39800-113">En avskrivning som er postert i det avledede avskrivningstablået, vil ha samme beløp som det som ble postert for det primære tablået.</span><span class="sxs-lookup"><span data-stu-id="39800-113">Depreciation posted in the derived book will be the same amount as was posted for the primary book.</span></span> <span data-ttu-id="39800-114">Hvis avskrivningsmetodene er forskjellige i tablåene, bør du ikke generere avskrivningstransaksjoner ved hjelp av den avledede prosessen.</span><span class="sxs-lookup"><span data-stu-id="39800-114">If the depreciation methods are different between the books, you should not generate depreciation transactions using the derived process.</span></span> |

## <a name="example"></a><span data-ttu-id="39800-115">Eksempel</span><span class="sxs-lookup"><span data-stu-id="39800-115">Example</span></span> 
<span data-ttu-id="39800-116">Informasjonen nedenfor beskriver hvordan du kan angi avskrivningsmetoder med funksjonaliteten til det avledede tablået.</span><span class="sxs-lookup"><span data-stu-id="39800-116">The following information describes how to set up acquisition transactions with the derived book functionality.</span></span>

1.  <span data-ttu-id="39800-117">Opprett tablåene på Tablåer-siden.</span><span class="sxs-lookup"><span data-stu-id="39800-117">Create the books on the Books page.</span></span>
    -   <span data-ttu-id="39800-118">Tablået for regnskap: VM 1, gjeldende posteringslag</span><span class="sxs-lookup"><span data-stu-id="39800-118">The book for accounting: VM 1, Current posting layer</span></span>
    -   <span data-ttu-id="39800-119">Tablået for skatte- og avgiftsformål: VM 2, avgiftsposteringslag</span><span class="sxs-lookup"><span data-stu-id="39800-119">The book for tax purposes: VM 2, Tax posting layer</span></span>

2.  <span data-ttu-id="39800-120">På VM 1 klikker du kategorien Avledede tablåer. Velg VM 2 i boksen Felt og Oppkjøp i feltet Transaksjonstype.</span><span class="sxs-lookup"><span data-stu-id="39800-120">On VM 1, click the Derived books tab. Select VM 2 in the Book field, and Acquisition in the Transaction type field.</span></span>

<span data-ttu-id="39800-121">Tablåene kan deretter knyttes til bestemte anleggsmidler.</span><span class="sxs-lookup"><span data-stu-id="39800-121">The books then can be attached to specific fixed assets.</span></span> 

<span data-ttu-id="39800-122">Når en anskaffelse posteres for et anleggsmiddel med tablået VM 1, posteres anleggsmiddelet ikke bare på VM 1, men også på det avledede tablået VM 2.</span><span class="sxs-lookup"><span data-stu-id="39800-122">When an acquisition is posted for a fixed asset with book VM 1, the acquisition is posted not only on VM 1, but also on the derived book VM 2.</span></span> <span data-ttu-id="39800-123">Statusen for begge anleggsmiddeltablåer oppdateres til Åpen.</span><span class="sxs-lookup"><span data-stu-id="39800-123">The status of both fixed asset books is updated to Open.</span></span>

> [!NOTE]                                                                                                         
> <span data-ttu-id="39800-124">Hvis du ikke bruker avledede tablåer, må du postere anskaffelsen av anleggsmiddelet både for tablå VM 1 og tablå VM 2.</span><span class="sxs-lookup"><span data-stu-id="39800-124">If you do not use derived books, you must post the acquisition of the fixed asset both for book VM 1 and book VM 2.</span></span>

<span data-ttu-id="39800-125">Hvis du vil ha mer informasjon, kan du se [Avledede tablåer](derived-books.md)</span><span class="sxs-lookup"><span data-stu-id="39800-125">For more information, see [Derived books](derived-books.md)</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]