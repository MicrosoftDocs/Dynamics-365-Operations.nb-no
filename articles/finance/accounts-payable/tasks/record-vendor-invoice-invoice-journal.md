---
title: Registrere en leverandørfaktura i fakturajournalen
description: Denne oppgaveveiledningen viser hvordan du kan registrere leverandørfakturaer som ikke er knyttet til bestillinger.
author: abruer
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendInvoiceWorkspace, LedgerJournalTable, LedgerJournalTransVendInvoice
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5277081d9f7adcc43c30d30208d13c7e39d76118
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140381"
---
# <a name="record-a-vendor-invoice-in-the-invoice-journal"></a><span data-ttu-id="36057-103">Registrere en leverandørfaktura i fakturajournalen</span><span class="sxs-lookup"><span data-stu-id="36057-103">Record a vendor invoice in the invoice journal</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="36057-104">Denne oppgaveveiledningen viser hvordan du kan registrere leverandørfakturaer som ikke er knyttet til bestillinger.</span><span class="sxs-lookup"><span data-stu-id="36057-104">This task guide will show how to record vendor invoices that are not associated with purchase orders.</span></span> <span data-ttu-id="36057-105">Eksempler på denne typen faktura er utgifter for forsyninger eller tjenester.</span><span class="sxs-lookup"><span data-stu-id="36057-105">Examples of this type of invoice include expenses for supplies or services.</span></span>  <span data-ttu-id="36057-106">Denne registreringen bruker demonstrasjonsfirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="36057-106">This recording uses the USMF demo company.</span></span>

1. <span data-ttu-id="36057-107">Gå til **Navigasjonsrute > Moduler > Leverandører > Arbeidsområder > Leverandørfakturaregistrering**.</span><span class="sxs-lookup"><span data-stu-id="36057-107">Go to **Navigation pane > Modules > Accounts payable > Workspaces > Vendor invoice entry**.</span></span>
2. <span data-ttu-id="36057-108">Klikk **Ny fakturajournal** i **handlingsruten**.</span><span class="sxs-lookup"><span data-stu-id="36057-108">On the **Action pane**, click **New invoice journal**.</span></span>
3. <span data-ttu-id="36057-109">Klikk på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="36057-109">Click **New**.</span></span>
4. <span data-ttu-id="36057-110">I **Navn**-feltet angir du journalnavnet eller klikker rullegardinknappen for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="36057-110">In the **Name** field, enter the journal name or click the drop down button to open the lookup.</span></span>
5. <span data-ttu-id="36057-111">Skriv inn en verdi i **Beskrivelse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="36057-111">In the **Description** field, type a value.</span></span>
6. <span data-ttu-id="36057-112">Klikk på **Linjer** i **handlingsruten**.</span><span class="sxs-lookup"><span data-stu-id="36057-112">On the **Action pane**, click **Lines**.</span></span> <span data-ttu-id="36057-113">Angi posteringsdatoen som oppdaterer Økonomimodul, i **Dato**-feltet.</span><span class="sxs-lookup"><span data-stu-id="36057-113">In the **Date** field, enter the posting date that will update General Ledger.</span></span>  
7. <span data-ttu-id="36057-114">Angi **leverandørkontoen** i **Konto**-feltet.</span><span class="sxs-lookup"><span data-stu-id="36057-114">In the **Account** field, specify the **Vendor account**.</span></span>
8. <span data-ttu-id="36057-115">I **Faktura**-feltet angir du fakturanummeret.</span><span class="sxs-lookup"><span data-stu-id="36057-115">In the **Invoice** field, enter the invoice number.</span></span>
9. <span data-ttu-id="36057-116">Skriv inn en verdi i **Beskrivelse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="36057-116">In the **Description** field, type a value.</span></span>
10. <span data-ttu-id="36057-117">Angi et tall i **Kredit**-feltet.</span><span class="sxs-lookup"><span data-stu-id="36057-117">In the **Credit** field, enter a number.</span></span>
11. <span data-ttu-id="36057-118">I **Motkonto**-feltet angir du kontonummeret eller klikker rullegardinknappen for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="36057-118">In the **Offset account** field, enter the account number or click the drop down button to open the lookup</span></span>
    * <span data-ttu-id="36057-119">**Mva-gruppen** hentes fra leverandørkontoen.</span><span class="sxs-lookup"><span data-stu-id="36057-119">The **Sales tax group** will be default from the vendor account.</span></span>  
    * <span data-ttu-id="36057-120">**Mva-gruppen for vare** hentes fra hovedkontoen angitt i **Motkonto**-feltet.</span><span class="sxs-lookup"><span data-stu-id="36057-120">The **Item sales tax group** will be default from the main account specified in the **Offset account** field.</span></span>  
    * <span data-ttu-id="36057-121">**Forfallsdatoen** beregnes basert på betalingsbetingelsene.</span><span class="sxs-lookup"><span data-stu-id="36057-121">The **Due date** will be calculated based on the Terms of payment.</span></span>  
    * <span data-ttu-id="36057-122">**Kontantrabatten** hentes fra leverandørkontoen.</span><span class="sxs-lookup"><span data-stu-id="36057-122">The **Cash discount** will default from the Vendor account.</span></span>  
12. <span data-ttu-id="36057-123">Klikk **Poster**.</span><span class="sxs-lookup"><span data-stu-id="36057-123">Click **Post**.</span></span>
13. <span data-ttu-id="36057-124">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="36057-124">Close the page.</span></span>

