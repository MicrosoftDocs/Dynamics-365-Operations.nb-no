--- 
title: Registrere og postere en etterdatert sjekk for en kunde
description: Du kan registrere informasjon i en etterdatert sjekk fra en kunde.
author: kweekley
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 1610036815349f625a67d5dd67260114d42fff97
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="register-and-post-a-postdated-check-for-a-customer"></a><span data-ttu-id="9f814-103">Registrere og postere en etterdatert sjekk for en kunde</span><span class="sxs-lookup"><span data-stu-id="9f814-103">Register and post a postdated check for a customer</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9f814-104">Du kan registrere informasjon i en etterdatert sjekk fra en kunde.</span><span class="sxs-lookup"><span data-stu-id="9f814-104">You can register details of a postdated cheque received from a customer.</span></span> <span data-ttu-id="9f814-105">Du kan også postere den etterdaterte sjekken og generere finanstransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="9f814-105">You can also post the postdated cheque and generate financial transactions.</span></span>   <span data-ttu-id="9f814-106">Fullfør følgende oppgaver før du registrerer og posterer en etterdatert sjekk fra en kunde: • Definer etterdaterte sjekker på siden Kontant- og bankbehandling • Definer en betalingsmåte for etterdaterte sjekker. Rollen for denne prosedyren er Kasserer.</span><span class="sxs-lookup"><span data-stu-id="9f814-106">Complete the following tasks before you register and post a postdated cheque received from a customer:   • Set up postdated Cheques in the Cash and bank management page • Set up a method of payment for postdated Cheques   The role for this procedure is Treasurer.</span></span> <span data-ttu-id="9f814-107">Denne fremgangsmåten bruker demonstrasjonsfirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="9f814-107">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="9f814-108">Gå til Kunder > Betalinger > Betalingsjournal.</span><span class="sxs-lookup"><span data-stu-id="9f814-108">Go to Accounts receivable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="9f814-109">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="9f814-109">Click New.</span></span>
3. <span data-ttu-id="9f814-110">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="9f814-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="9f814-111">Klikk Linjer.</span><span class="sxs-lookup"><span data-stu-id="9f814-111">Click Lines.</span></span>
5. <span data-ttu-id="9f814-112">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="9f814-112">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="9f814-113">Angi de ønskede verdiene i Konto-feltet.</span><span class="sxs-lookup"><span data-stu-id="9f814-113">In the Account field, specify the desired values.</span></span>
7. <span data-ttu-id="9f814-114">Angi et tall i Kredit-feltet.</span><span class="sxs-lookup"><span data-stu-id="9f814-114">In the Credit field, enter a number.</span></span>
    * <span data-ttu-id="9f814-115">Angi beløpet i den etterdaterte sjekken.</span><span class="sxs-lookup"><span data-stu-id="9f814-115">Enter the amount specified in the postdated cheque.</span></span>  
8. <span data-ttu-id="9f814-116">Klikk kategorien Betaling.</span><span class="sxs-lookup"><span data-stu-id="9f814-116">Click the Payment tab.</span></span>
9. <span data-ttu-id="9f814-117">Skriv inn en verdi i Betalingsmåte-feltet.</span><span class="sxs-lookup"><span data-stu-id="9f814-117">In the Method of payment field, type a value.</span></span>
    * <span data-ttu-id="9f814-118">Velge betalingsmåten for den etterdaterte sjekken</span><span class="sxs-lookup"><span data-stu-id="9f814-118">Select the method of payment for the postdated cheque</span></span>  
10. <span data-ttu-id="9f814-119">Velg kategorien Etterdaterte sjekker.</span><span class="sxs-lookup"><span data-stu-id="9f814-119">Click the Postdated checks tab.</span></span>
11. <span data-ttu-id="9f814-120">Angi en dato i feltet Forfallsdato.</span><span class="sxs-lookup"><span data-stu-id="9f814-120">In the Maturity date field, enter a date.</span></span>
    * <span data-ttu-id="9f814-121">Angi datoen når den etterdaterte sjekken forfaller til betaling.</span><span class="sxs-lookup"><span data-stu-id="9f814-121">Enter the date when the postdated cheque is due for payment.</span></span>  
12. <span data-ttu-id="9f814-122">Angi en verdi i feltet Avdeling av utstedende bank.</span><span class="sxs-lookup"><span data-stu-id="9f814-122">In the Issuing bank branch field, type a value.</span></span>
    * <span data-ttu-id="9f814-123">Angi bankdetaljene for den etterdaterte sjekken.</span><span class="sxs-lookup"><span data-stu-id="9f814-123">Enter the bank details of the postdated cheque.</span></span>  
13. <span data-ttu-id="9f814-124">Skriv inn en verdi i feltet Sjekknummer.</span><span class="sxs-lookup"><span data-stu-id="9f814-124">In the cheque number field, type a value.</span></span>
14. <span data-ttu-id="9f814-125">Angi en verdi i feltet Navn på utstedende bank.</span><span class="sxs-lookup"><span data-stu-id="9f814-125">In the Issuing bank name field, type a value.</span></span>
    * <span data-ttu-id="9f814-126">Angi bankdetaljene for den etterdaterte sjekken.</span><span class="sxs-lookup"><span data-stu-id="9f814-126">Enter the bank details of the postdated check.</span></span>  
15. <span data-ttu-id="9f814-127">Klikk Poster.</span><span class="sxs-lookup"><span data-stu-id="9f814-127">Click Post.</span></span>
16. <span data-ttu-id="9f814-128">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="9f814-128">Close the page.</span></span>


