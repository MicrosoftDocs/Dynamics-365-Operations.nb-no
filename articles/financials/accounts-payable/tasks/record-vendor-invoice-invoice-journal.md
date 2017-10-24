--- 
title: "Registrere en leverandørfaktura i fakturajournalen"
description: "Denne oppgaveveiledningen viser hvordan du kan registrere leverandørfakturaer som ikke er knyttet til bestillinger."
author: abruer
manager: AnnBe
ms.date: 11/15/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 42f93e6d8fcf62babc3e3244bc1fe76d1efd9d13
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="record-a-vendor-invoice-in-the-invoice-journal"></a><span data-ttu-id="f8f7f-103">Registrere en leverandørfaktura i fakturajournalen</span><span class="sxs-lookup"><span data-stu-id="f8f7f-103">Record a vendor invoice in the invoice journal</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f8f7f-104">Denne oppgaveveiledningen viser hvordan du kan registrere leverandørfakturaer som ikke er knyttet til bestillinger.</span><span class="sxs-lookup"><span data-stu-id="f8f7f-104">This task guide will show how to record vendor invoices that are not associated with purchase orders.</span></span> <span data-ttu-id="f8f7f-105">Eksempler på denne typen faktura er utgifter for forsyninger eller tjenester.</span><span class="sxs-lookup"><span data-stu-id="f8f7f-105">Examples of this type of invoice include expenses for supplies or services.</span></span>  <span data-ttu-id="f8f7f-106">Denne registreringen bruker demonstrasjonsfirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="f8f7f-106">This recording uses the USMF demo company.</span></span>

1. <span data-ttu-id="f8f7f-107">Gå til Leverandører > Arbeidsområder > Leverandørfakturaregistrering.</span><span class="sxs-lookup"><span data-stu-id="f8f7f-107">Go to Accounts payable > Workspaces > Vendor invoice entry.</span></span>
2. <span data-ttu-id="f8f7f-108">Klikk Ny fakturajournal.</span><span class="sxs-lookup"><span data-stu-id="f8f7f-108">Click New invoice journal.</span></span>
3. <span data-ttu-id="f8f7f-109">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="f8f7f-109">Click New.</span></span>
4. <span data-ttu-id="f8f7f-110">I Navn-feltet angir du journalnavnet eller klikker rullegardinknappen for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="f8f7f-110">In the Name field, enter the journal name or click the drop down button to open the lookup.</span></span>
5. <span data-ttu-id="f8f7f-111">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="f8f7f-111">In the Description field, type a value.</span></span>
6. <span data-ttu-id="f8f7f-112">Klikk Linjer.</span><span class="sxs-lookup"><span data-stu-id="f8f7f-112">Click Lines.</span></span>
    * <span data-ttu-id="f8f7f-113">Angi posteringsdatoen som oppdaterer Økonomimodul, i Dato-feltet.</span><span class="sxs-lookup"><span data-stu-id="f8f7f-113">In the Date field, enter the posting date that will update General Ledger.</span></span>  
7. <span data-ttu-id="f8f7f-114">Angi leverandørkontoen i Konto-feltet.</span><span class="sxs-lookup"><span data-stu-id="f8f7f-114">In the Account field, specify the Vendor account.</span></span>
8. <span data-ttu-id="f8f7f-115">I Faktura-feltet angir du fakturanummeret.</span><span class="sxs-lookup"><span data-stu-id="f8f7f-115">In the Invoice field, enter the invoice number.</span></span>
9. <span data-ttu-id="f8f7f-116">Skriv inn en verdi i Beskrivelse-feltet.</span><span class="sxs-lookup"><span data-stu-id="f8f7f-116">In the Description field, type a value.</span></span>
10. <span data-ttu-id="f8f7f-117">Angi et tall i Kredit-feltet.</span><span class="sxs-lookup"><span data-stu-id="f8f7f-117">In the Credit field, enter a number.</span></span>
11. <span data-ttu-id="f8f7f-118">I Motkonto-feltet angir du kontonummeret eller klikker rullegardinknappen for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="f8f7f-118">In the Offset account field, enter the account number or click the drop down button to open the lookup</span></span>
    * <span data-ttu-id="f8f7f-119">Mva-gruppen hentes fra leverandørkontoen.</span><span class="sxs-lookup"><span data-stu-id="f8f7f-119">The Sales tax group will default from the vendor account.</span></span>  
    * <span data-ttu-id="f8f7f-120">Mva-gruppen for vare hentes fra hovedkontoen angitt i Motkonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="f8f7f-120">The Item sales tax group will default from the main account specified in the Offset account field.</span></span>  
    * <span data-ttu-id="f8f7f-121">Forfallsdatoen beregnes basert på betalingsbetingelsene.</span><span class="sxs-lookup"><span data-stu-id="f8f7f-121">The Due date will be calculated based on the Terms of payment.</span></span>  
    * <span data-ttu-id="f8f7f-122">Kontantrabatten hentes fra leverandørkontoen.</span><span class="sxs-lookup"><span data-stu-id="f8f7f-122">The Cash discount will default from the Vendor account.</span></span>  
12. <span data-ttu-id="f8f7f-123">Klikk Poster.</span><span class="sxs-lookup"><span data-stu-id="f8f7f-123">Click Post.</span></span>
13. <span data-ttu-id="f8f7f-124">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="f8f7f-124">Close the page.</span></span>


