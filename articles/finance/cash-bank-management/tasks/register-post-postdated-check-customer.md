---
title: Registrere og postere en etterdatert sjekk for en kunde
description: Du kan registrere informasjon i en etterdatert sjekk fra en kunde.
author: kweekley
manager: AnnBe
ms.date: 10/26/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6f27675a2aa2160619bf78eea33bba2ce0b7bd81
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/27/2019
ms.locfileid: "2188102"
---
# <a name="register-and-post-a-postdated-check-for-a-customer"></a><span data-ttu-id="30b85-103">Registrere og postere en etterdatert sjekk for en kunde</span><span class="sxs-lookup"><span data-stu-id="30b85-103">Register and post a postdated check for a customer</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="30b85-104">Du kan registrere informasjon i en etterdatert sjekk fra en kunde.</span><span class="sxs-lookup"><span data-stu-id="30b85-104">You can register details of a postdated check received from a customer.</span></span> <span data-ttu-id="30b85-105">Du kan også postere den etterdaterte sjekken og generere finanstransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="30b85-105">You can also post the postdated check and generate financial transactions.</span></span>   <span data-ttu-id="30b85-106">Fullfør følgende oppgaver før du registrerer og posterer en etterdatert sjekk fra en kunde: • Definer etterdaterte sjekker på siden Kontant- og bankbehandling • Definer en betalingsmåte for etterdaterte sjekker. Rollen for denne prosedyren er Kasserer.</span><span class="sxs-lookup"><span data-stu-id="30b85-106">Complete the following tasks before you register and post a postdated check received from a customer:   • Set up postdated check in the Cash and bank management page • Set up a method of payment for postdated checks   The role for this procedure is Treasurer.</span></span> <span data-ttu-id="30b85-107">Denne fremgangsmåten bruker demonstrasjonsfirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="30b85-107">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="30b85-108">Gå til Kunder > Betalinger > Betalingsjournal.</span><span class="sxs-lookup"><span data-stu-id="30b85-108">Go to Accounts receivable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="30b85-109">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="30b85-109">Click New.</span></span>
3. <span data-ttu-id="30b85-110">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="30b85-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="30b85-111">Klikk Linjer.</span><span class="sxs-lookup"><span data-stu-id="30b85-111">Click Lines.</span></span>
5. <span data-ttu-id="30b85-112">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="30b85-112">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="30b85-113">Angi de ønskede verdiene i Konto-feltet.</span><span class="sxs-lookup"><span data-stu-id="30b85-113">In the Account field, specify the desired values.</span></span>
7. <span data-ttu-id="30b85-114">Angi et tall i Kredit-feltet.</span><span class="sxs-lookup"><span data-stu-id="30b85-114">In the Credit field, enter a number.</span></span>
    * <span data-ttu-id="30b85-115">Angi beløpet i den etterdaterte sjekken.</span><span class="sxs-lookup"><span data-stu-id="30b85-115">Enter the amount specified in the postdated check.</span></span>  
8. <span data-ttu-id="30b85-116">Klikk kategorien Betaling.</span><span class="sxs-lookup"><span data-stu-id="30b85-116">Click the Payment tab.</span></span>
9. <span data-ttu-id="30b85-117">Skriv inn en verdi i Betalingsmåte-feltet.</span><span class="sxs-lookup"><span data-stu-id="30b85-117">In the Method of payment field, type a value.</span></span>
    * <span data-ttu-id="30b85-118">Velge betalingsmåten for den etterdaterte sjekken.</span><span class="sxs-lookup"><span data-stu-id="30b85-118">Select the method of payment for the postdated check.</span></span>  
10. <span data-ttu-id="30b85-119">Velg kategorien Etterdaterte sjekker.</span><span class="sxs-lookup"><span data-stu-id="30b85-119">Click the Postdated checks tab.</span></span>
11. <span data-ttu-id="30b85-120">Angi en dato i feltet Forfallsdato.</span><span class="sxs-lookup"><span data-stu-id="30b85-120">In the Maturity date field, enter a date.</span></span>
    * <span data-ttu-id="30b85-121">Angi datoen når den etterdaterte sjekken forfaller til betaling.</span><span class="sxs-lookup"><span data-stu-id="30b85-121">Enter the date when the postdated check is due for payment.</span></span>  
12. <span data-ttu-id="30b85-122">Angi en verdi i feltet Avdeling av utstedende bank.</span><span class="sxs-lookup"><span data-stu-id="30b85-122">In the Issuing bank branch field, type a value.</span></span>
    * <span data-ttu-id="30b85-123">Angi bankdetaljene for den etterdaterte sjekken.</span><span class="sxs-lookup"><span data-stu-id="30b85-123">Enter the bank details of the postdated check.</span></span>  
13. <span data-ttu-id="30b85-124">Skriv inn en verdi i feltet for sjekknummer.</span><span class="sxs-lookup"><span data-stu-id="30b85-124">In the check number field, type a value.</span></span>
14. <span data-ttu-id="30b85-125">Angi en verdi i feltet Navn på utstedende bank.</span><span class="sxs-lookup"><span data-stu-id="30b85-125">In the Issuing bank name field, type a value.</span></span>
    * <span data-ttu-id="30b85-126">Angi bankdetaljene for den etterdaterte sjekken.</span><span class="sxs-lookup"><span data-stu-id="30b85-126">Enter the bank details of the postdated check.</span></span>  
15. <span data-ttu-id="30b85-127">Klikk Poster.</span><span class="sxs-lookup"><span data-stu-id="30b85-127">Click Post.</span></span>
16. <span data-ttu-id="30b85-128">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="30b85-128">Close the page.</span></span>

