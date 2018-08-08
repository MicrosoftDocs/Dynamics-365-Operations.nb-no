--- 
title: Opprette en fasilitetsavtale for garantibrevet
description: "Denne oppgaven oppretter en bankfasilitetsavtale for å behandle et garantibrev."
author: ShylaThompson
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 04ee7b1483f3b8a7cda7fce5439586f0a2979e51
ms.contentlocale: nb-no
ms.lasthandoff: 08/07/2018

---
# <a name="create-a-bank-facility-agreement-for-the-letter-of-guarantee"></a><span data-ttu-id="d78ab-103">Opprette en fasilitetsavtale for garantibrevet</span><span class="sxs-lookup"><span data-stu-id="d78ab-103">Create a bank facility agreement for the letter of guarantee</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d78ab-104">Denne oppgaven oppretter en bankfasilitetsavtale for å behandle et garantibrev.</span><span class="sxs-lookup"><span data-stu-id="d78ab-104">This task creates a bank facility agreement to process a letter of guarantee.</span></span> <span data-ttu-id="d78ab-105">Denne oppgaven bruker demonstrasjonsfirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="d78ab-105">This task uses the USMF demo company.</span></span> 


## <a name="create-bank-facility-agreement"></a><span data-ttu-id="d78ab-106">Opprette en bankfasilitetsavtale</span><span class="sxs-lookup"><span data-stu-id="d78ab-106">Create Bank facility agreement</span></span>
1. <span data-ttu-id="d78ab-107">Gå til Kontant- og bankbehandling > Garantibrev > Bankfasilitetsavtaler.</span><span class="sxs-lookup"><span data-stu-id="d78ab-107">Go to Cash and bank management > Letters of guarantee > Bank facility agreements.</span></span>
2. <span data-ttu-id="d78ab-108">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="d78ab-108">Click New.</span></span>
3. <span data-ttu-id="d78ab-109">Angi bankavtalenummeret for transaksjonen i feltet Avtalenummer.</span><span class="sxs-lookup"><span data-stu-id="d78ab-109">In the Agreement number field, enter the bank agreement number for the transaction.</span></span>
4. <span data-ttu-id="d78ab-110">I feltet Bankkonto velger du bankkontonummeret som garantibrevet er åpent for.</span><span class="sxs-lookup"><span data-stu-id="d78ab-110">In the Bank account field, select the bank account number for which the letter of guarantee is open.</span></span> 
5. <span data-ttu-id="d78ab-111">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="d78ab-111">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="d78ab-112">Angi dato og klokkeslett i Startdato-feltet.</span><span class="sxs-lookup"><span data-stu-id="d78ab-112">In the Start date field, enter a date and time.</span></span>
7. <span data-ttu-id="d78ab-113">Angi dato og klokkeslett i Sluttdato-feltet.</span><span class="sxs-lookup"><span data-stu-id="d78ab-113">In the End date field, enter a date and time.</span></span>
8. <span data-ttu-id="d78ab-114">Aktiver/deaktiver utvidelsen av delen Generelt.</span><span class="sxs-lookup"><span data-stu-id="d78ab-114">Toggle the expansion of the General section.</span></span>
9. <span data-ttu-id="d78ab-115">Klikk Legg til linje.</span><span class="sxs-lookup"><span data-stu-id="d78ab-115">Click Add line.</span></span>
10. <span data-ttu-id="d78ab-116">Klikk rullegardinknappen i feltet Fasilitetstype for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="d78ab-116">In the Facility type field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="d78ab-117">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="d78ab-117">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="d78ab-118">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="d78ab-118">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="d78ab-119">I Grense-feltet angir du beløpet som er forhandlet med banken.</span><span class="sxs-lookup"><span data-stu-id="d78ab-119">In the Limit field, enter the amount negotiated with the bank.</span></span>
14. <span data-ttu-id="d78ab-120">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="d78ab-120">Click Save.</span></span>
15. <span data-ttu-id="d78ab-121">Aktiver/deaktiver utvidelsen av delen Garantibrev.</span><span class="sxs-lookup"><span data-stu-id="d78ab-121">Toggle the expansion of the Letter of guarantee section.</span></span>
16. <span data-ttu-id="d78ab-122">Velg et alternativ i Beregningsmåte-feltet.</span><span class="sxs-lookup"><span data-stu-id="d78ab-122">In the Calculation method field, select an option.</span></span>
    * <span data-ttu-id="d78ab-123">Angi detaljer om beregningmetode og prosent for Kontantmargin, Utstedelsesprovisjon, Forlengelsesprovisjon, Øk verdiprovisjon, eller Reduser verdiprovisjon, etter behov.</span><span class="sxs-lookup"><span data-stu-id="d78ab-123">Enter the calculation method and percentage details for the Cash margin, Issuance commission, Extension commission, Increase value commission, or Decrease value commission, as appropriate.</span></span>   
17. <span data-ttu-id="d78ab-124">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="d78ab-124">Click Save.</span></span>

## <a name="extend-bank-facility-agreement"></a><span data-ttu-id="d78ab-125">Forlenge bankfasilitetsavtale</span><span class="sxs-lookup"><span data-stu-id="d78ab-125">Extend bank facility agreement</span></span>
1. <span data-ttu-id="d78ab-126">Klikk Utvid for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="d78ab-126">Click Extend to open the drop dialog.</span></span>
2. <span data-ttu-id="d78ab-127">Angi en verdi i feltet Nytt avtalenummer.</span><span class="sxs-lookup"><span data-stu-id="d78ab-127">In the New agreement number field, type a value.</span></span>
3. <span data-ttu-id="d78ab-128">Angi dato og klokkeslett i Sluttdato-feltet.</span><span class="sxs-lookup"><span data-stu-id="d78ab-128">In the End date field, enter a date and time.</span></span>
4. <span data-ttu-id="d78ab-129">Klikk Utvid.</span><span class="sxs-lookup"><span data-stu-id="d78ab-129">Click Extend.</span></span>
5. <span data-ttu-id="d78ab-130">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="d78ab-130">Click Save.</span></span>
6. <span data-ttu-id="d78ab-131">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="d78ab-131">Close the page.</span></span>


