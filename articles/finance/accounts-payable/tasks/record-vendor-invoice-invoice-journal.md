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
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a60a5959046ca9e953bac80aaeb382d07a267643
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5227142"
---
# <a name="record-a-vendor-invoice-in-the-invoice-journal"></a><span data-ttu-id="6ba5f-103">Registrere en leverandørfaktura i fakturajournalen</span><span class="sxs-lookup"><span data-stu-id="6ba5f-103">Record a vendor invoice in the invoice journal</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6ba5f-104">Denne oppgaveveiledningen viser hvordan du kan registrere leverandørfakturaer som ikke er knyttet til bestillinger.</span><span class="sxs-lookup"><span data-stu-id="6ba5f-104">This task guide will show how to record vendor invoices that are not associated with purchase orders.</span></span> <span data-ttu-id="6ba5f-105">Eksempler på denne typen faktura er utgifter for forsyninger eller tjenester.</span><span class="sxs-lookup"><span data-stu-id="6ba5f-105">Examples of this type of invoice include expenses for supplies or services.</span></span>  <span data-ttu-id="6ba5f-106">Denne registreringen bruker demonstrasjonsfirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="6ba5f-106">This recording uses the USMF demo company.</span></span>

1. <span data-ttu-id="6ba5f-107">Gå til **Navigasjonsrute > Moduler > Leverandører > Arbeidsområder > Leverandørfakturaregistrering**.</span><span class="sxs-lookup"><span data-stu-id="6ba5f-107">Go to **Navigation pane > Modules > Accounts payable > Workspaces > Vendor invoice entry**.</span></span>
2. <span data-ttu-id="6ba5f-108">Klikk **Ny fakturajournal** i **handlingsruten**.</span><span class="sxs-lookup"><span data-stu-id="6ba5f-108">On the **Action pane**, click **New invoice journal**.</span></span>
3. <span data-ttu-id="6ba5f-109">Klikk på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="6ba5f-109">Click **New**.</span></span>
4. <span data-ttu-id="6ba5f-110">I **Navn**-feltet angir du journalnavnet eller klikker rullegardinknappen for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="6ba5f-110">In the **Name** field, enter the journal name or click the drop down button to open the lookup.</span></span>
5. <span data-ttu-id="6ba5f-111">Skriv inn en verdi i **Beskrivelse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="6ba5f-111">In the **Description** field, type a value.</span></span>
6. <span data-ttu-id="6ba5f-112">Klikk på **Linjer** i **handlingsruten**.</span><span class="sxs-lookup"><span data-stu-id="6ba5f-112">On the **Action pane**, click **Lines**.</span></span> <span data-ttu-id="6ba5f-113">Angi posteringsdatoen som oppdaterer Økonomimodul, i **Dato**-feltet.</span><span class="sxs-lookup"><span data-stu-id="6ba5f-113">In the **Date** field, enter the posting date that will update General Ledger.</span></span>  
7. <span data-ttu-id="6ba5f-114">Angi **leverandørkontoen** i **Konto**-feltet.</span><span class="sxs-lookup"><span data-stu-id="6ba5f-114">In the **Account** field, specify the **Vendor account**.</span></span>
8. <span data-ttu-id="6ba5f-115">I **Faktura**-feltet angir du fakturanummeret.</span><span class="sxs-lookup"><span data-stu-id="6ba5f-115">In the **Invoice** field, enter the invoice number.</span></span>
9. <span data-ttu-id="6ba5f-116">Skriv inn en verdi i **Beskrivelse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="6ba5f-116">In the **Description** field, type a value.</span></span>
10. <span data-ttu-id="6ba5f-117">Angi et tall i **Kredit**-feltet.</span><span class="sxs-lookup"><span data-stu-id="6ba5f-117">In the **Credit** field, enter a number.</span></span>
11. <span data-ttu-id="6ba5f-118">I **Motkonto**-feltet angir du kontonummeret eller klikker rullegardinknappen for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="6ba5f-118">In the **Offset account** field, enter the account number or click the drop down button to open the lookup</span></span>
    * <span data-ttu-id="6ba5f-119">**Mva-gruppen** hentes fra leverandørkontoen.</span><span class="sxs-lookup"><span data-stu-id="6ba5f-119">The **Sales tax group** will be default from the vendor account.</span></span>  
    * <span data-ttu-id="6ba5f-120">**Mva-gruppen for vare** hentes fra hovedkontoen angitt i **Motkonto**-feltet.</span><span class="sxs-lookup"><span data-stu-id="6ba5f-120">The **Item sales tax group** will be default from the main account specified in the **Offset account** field.</span></span>  
    * <span data-ttu-id="6ba5f-121">**Forfallsdatoen** beregnes basert på betalingsbetingelsene.</span><span class="sxs-lookup"><span data-stu-id="6ba5f-121">The **Due date** will be calculated based on the Terms of payment.</span></span>  
    * <span data-ttu-id="6ba5f-122">**Kontantrabatten** hentes fra leverandørkontoen.</span><span class="sxs-lookup"><span data-stu-id="6ba5f-122">The **Cash discount** will default from the Vendor account.</span></span>
12. <span data-ttu-id="6ba5f-123">Hvis du har aktivert arbeidsflyten for leverandørfakturajournal, klikker du **Arbeidsflyt > Send**.</span><span class="sxs-lookup"><span data-stu-id="6ba5f-123">If you have enabled Vendor invoice journal workflow, click **Workflow > Submit**.</span></span>
    * <span data-ttu-id="6ba5f-124">Når sendingen er godkjent, vil datoen flyttes til den første dagen i neste åpne periode hvis posteringsdatoen for transaksjonen er innenfor en periode som er på vent eller lukket for finanspostering.</span><span class="sxs-lookup"><span data-stu-id="6ba5f-124">When your submission is approved, the date will be advanced to the first day of the next open period, if the transaction posting date falls within a period that is On hold or Closed for ledger posting.</span></span>
12. <span data-ttu-id="6ba5f-125">Klikk **Poster**.</span><span class="sxs-lookup"><span data-stu-id="6ba5f-125">Click **Post**.</span></span>
13. <span data-ttu-id="6ba5f-126">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="6ba5f-126">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]