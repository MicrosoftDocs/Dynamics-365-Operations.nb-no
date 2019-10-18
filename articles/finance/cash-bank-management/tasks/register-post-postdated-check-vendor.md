---
title: Registrere og postere en etterdatert sjekk for en leverandør
description: Du kan registrere detaljene for en etterdatert sjekk før du utsteder sjekken til en leverandør ved hjelp av journalbilaget.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fe29e106055177dbd12c39ee3fc9de609059f73b
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/27/2019
ms.locfileid: "2179234"
---
# <a name="register-and-post-a-postdated-check-for-a-vendor"></a><span data-ttu-id="92ba1-103">Registrere og postere en etterdatert sjekk for en leverandør</span><span class="sxs-lookup"><span data-stu-id="92ba1-103">Register and post a postdated check for a vendor</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="92ba1-104">Du kan registrere detaljene for en etterdatert sjekk før du utsteder sjekken til en leverandør ved hjelp av journalbilaget.</span><span class="sxs-lookup"><span data-stu-id="92ba1-104">You can register the details of a postdated check before you issue the check to a vendor by using the journal voucher.</span></span> <span data-ttu-id="92ba1-105">Du kan også postere den etterdaterte sjekken og generere finanstransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="92ba1-105">You can also post the postdated check and generate financial transactions.</span></span> <span data-ttu-id="92ba1-106">Fullfør følgende oppgave før du registrerer og posterer en etterdatert sjekk fra en leverandør:</span><span class="sxs-lookup"><span data-stu-id="92ba1-106">Before you register and post a postdated check from a vendor, complete the following task:</span></span> 

<span data-ttu-id="92ba1-107">Definer etterdaterte sjekker på siden Kontant- og bankbehandling.</span><span class="sxs-lookup"><span data-stu-id="92ba1-107">Set up postdated checks in the Cash and bank management page.</span></span> 



<span data-ttu-id="92ba1-108">Rollen til denne oppgaveveiledningen er kasserer.</span><span class="sxs-lookup"><span data-stu-id="92ba1-108">The role of this task guides is Treasurer.</span></span> <span data-ttu-id="92ba1-109">Denne oppgaven bruker demonstrasjonsfirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="92ba1-109">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="92ba1-110">Gå til Leverandører > Betalinger > Betalingsjournal</span><span class="sxs-lookup"><span data-stu-id="92ba1-110">Go to Acounts payable > Payments > Payment journal</span></span>
2. <span data-ttu-id="92ba1-111">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="92ba1-111">Click New.</span></span>
3. <span data-ttu-id="92ba1-112">Skriv inn VendPay i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="92ba1-112">In the Name field, type 'VendPay'.</span></span>
4. <span data-ttu-id="92ba1-113">Klikk Linjer.</span><span class="sxs-lookup"><span data-stu-id="92ba1-113">Click Lines.</span></span>
5. <span data-ttu-id="92ba1-114">Angi de ønskede verdiene i Konto-feltet.</span><span class="sxs-lookup"><span data-stu-id="92ba1-114">In the Account field, specify the desired values.</span></span>
6. <span data-ttu-id="92ba1-115">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="92ba1-115">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="92ba1-116">Angi et tall i Debet-feltet.</span><span class="sxs-lookup"><span data-stu-id="92ba1-116">In the Debit field, enter a number.</span></span>
8. <span data-ttu-id="92ba1-117">Klikk rullegardinknappen i Betalingsmåte-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="92ba1-117">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="92ba1-118">Velge betalingsmåten for den etterdaterte sjekken</span><span class="sxs-lookup"><span data-stu-id="92ba1-118">Select the method of payment for the postdated check</span></span>  
9. <span data-ttu-id="92ba1-119">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="92ba1-119">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="92ba1-120">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="92ba1-120">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="92ba1-121">Velg kategorien Etterdaterte sjekker.</span><span class="sxs-lookup"><span data-stu-id="92ba1-121">Click the Postdated checks tab.</span></span>
12. <span data-ttu-id="92ba1-122">Skriv inn en verdi i feltet Sjekknummer.</span><span class="sxs-lookup"><span data-stu-id="92ba1-122">In the Check number field, type a value.</span></span>
    * <span data-ttu-id="92ba1-123">Angi eller endre det etterdaterte sjekknummeret.</span><span class="sxs-lookup"><span data-stu-id="92ba1-123">Enter or modify the number of the postdated check.</span></span>  
13. <span data-ttu-id="92ba1-124">Angi en verdi i feltet Navn på utstedende bank.</span><span class="sxs-lookup"><span data-stu-id="92ba1-124">In the Issuing bank name field, type a value.</span></span>
    * <span data-ttu-id="92ba1-125">Angi bankdetaljene for den utstedende banken.</span><span class="sxs-lookup"><span data-stu-id="92ba1-125">enter the bank details for the issuing bank.</span></span>  
14. <span data-ttu-id="92ba1-126">Klikk kategorien Liste.</span><span class="sxs-lookup"><span data-stu-id="92ba1-126">Click the List tab.</span></span>
15. <span data-ttu-id="92ba1-127">Klikk Poster.</span><span class="sxs-lookup"><span data-stu-id="92ba1-127">Click Post.</span></span>
16. <span data-ttu-id="92ba1-128">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="92ba1-128">Close the page.</span></span>
17. <span data-ttu-id="92ba1-129">Velg kategorien Etterdaterte sjekker.</span><span class="sxs-lookup"><span data-stu-id="92ba1-129">Click the Postdated checks tab.</span></span>

