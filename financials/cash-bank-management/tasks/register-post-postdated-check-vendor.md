--- 
title: "Registrere og postere en etterdatert sjekk for en leverandør"
description: "Du kan registrere detaljene for en etterdatert sjekk før du utsteder sjekken til en leverandør ved hjelp av journalbilaget."
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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 8689421d3281f93af9298f777f92c5c3b2c1c86c
ms.contentlocale: nb-no
ms.lasthandoff: 08/29/2017

---
# <a name="register-and-post-a-postdated-check-for-a-vendor"></a><span data-ttu-id="39c22-103">Registrere og postere en etterdatert sjekk for en leverandør</span><span class="sxs-lookup"><span data-stu-id="39c22-103">Register and post a postdated check for a vendor</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="39c22-104">Du kan registrere detaljene for en etterdatert sjekk før du utsteder sjekken til en leverandør ved hjelp av journalbilaget.</span><span class="sxs-lookup"><span data-stu-id="39c22-104">You can register the details of a postdated check before you issue the check to a vendor by using the journal voucher.</span></span> <span data-ttu-id="39c22-105">Du kan også postere den etterdaterte sjekken og generere finanstransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="39c22-105">You can also post the postdated check and generate financial transactions.</span></span> <span data-ttu-id="39c22-106">Fullfør følgende oppgave før du registrerer og posterer en etterdatert sjekk fra en leverandør:</span><span class="sxs-lookup"><span data-stu-id="39c22-106">Before you register and post a postdated check from a vendor, complete the following task:</span></span> 

<span data-ttu-id="39c22-107">Definer etterdaterte sjekker på siden Kontant- og bankbehandling.</span><span class="sxs-lookup"><span data-stu-id="39c22-107">Set up postdated checks in the Cash and bank management page.</span></span> 



<span data-ttu-id="39c22-108">Rollen til denne oppgaveveiledningen er kasserer.</span><span class="sxs-lookup"><span data-stu-id="39c22-108">The role of this task guides is Treasurer.</span></span> <span data-ttu-id="39c22-109">Denne oppgaven bruker demonstrasjonsfirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="39c22-109">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="39c22-110">Gå til Leverandører > Betalinger > Betalingsjournal</span><span class="sxs-lookup"><span data-stu-id="39c22-110">Go to Acounts payable > Payments > Payment journal</span></span>
2. <span data-ttu-id="39c22-111">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="39c22-111">Click New.</span></span>
3. <span data-ttu-id="39c22-112">Skriv inn VendPay i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="39c22-112">In the Name field, type 'VendPay'.</span></span>
4. <span data-ttu-id="39c22-113">Klikk Linjer.</span><span class="sxs-lookup"><span data-stu-id="39c22-113">Click Lines.</span></span>
5. <span data-ttu-id="39c22-114">Angi de ønskede verdiene i Konto-feltet.</span><span class="sxs-lookup"><span data-stu-id="39c22-114">In the Account field, specify the desired values.</span></span>
6. <span data-ttu-id="39c22-115">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="39c22-115">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="39c22-116">Angi et tall i Debet-feltet.</span><span class="sxs-lookup"><span data-stu-id="39c22-116">In the Debit field, enter a number.</span></span>
8. <span data-ttu-id="39c22-117">Klikk rullegardinknappen i Betalingsmåte-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="39c22-117">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="39c22-118">Velge betalingsmåten for den etterdaterte sjekken</span><span class="sxs-lookup"><span data-stu-id="39c22-118">Select the method of payment for the postdated check</span></span>  
9. <span data-ttu-id="39c22-119">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="39c22-119">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="39c22-120">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="39c22-120">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="39c22-121">Velg kategorien Etterdaterte sjekker.</span><span class="sxs-lookup"><span data-stu-id="39c22-121">Click the Postdated checks tab.</span></span>
12. <span data-ttu-id="39c22-122">Skriv inn en verdi i feltet Sjekknummer.</span><span class="sxs-lookup"><span data-stu-id="39c22-122">In the Check number field, type a value.</span></span>
    * <span data-ttu-id="39c22-123">Angi eller endre det etterdaterte sjekknummeret.</span><span class="sxs-lookup"><span data-stu-id="39c22-123">Enter or modify the number of the postdated check.</span></span>  
13. <span data-ttu-id="39c22-124">Angi en verdi i feltet Navn på utstedende bank.</span><span class="sxs-lookup"><span data-stu-id="39c22-124">In the Issuing bank name field, type a value.</span></span>
    * <span data-ttu-id="39c22-125">Angi bankdetaljene for den utstedende banken.</span><span class="sxs-lookup"><span data-stu-id="39c22-125">enter the bank details for the issuing bank.</span></span>  
14. <span data-ttu-id="39c22-126">Klikk kategorien Liste.</span><span class="sxs-lookup"><span data-stu-id="39c22-126">Click the List tab.</span></span>
15. <span data-ttu-id="39c22-127">Klikk Poster.</span><span class="sxs-lookup"><span data-stu-id="39c22-127">Click Post.</span></span>
16. <span data-ttu-id="39c22-128">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="39c22-128">Close the page.</span></span>
17. <span data-ttu-id="39c22-129">Velg kategorien Etterdaterte sjekker.</span><span class="sxs-lookup"><span data-stu-id="39c22-129">Click the Postdated checks tab.</span></span>


