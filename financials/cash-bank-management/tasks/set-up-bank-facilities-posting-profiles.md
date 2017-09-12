--- 
title: Definere bankfasiliteter og posteringsprofiler for garantibrev
description: "Denne oppgaven oppretter en bankfasilitet og posteringsprofil som er nødvendig for å behandle et garantibrev."
author: kweekley
manager: AnnBe
ms.date: 02/10/2016
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
ms.openlocfilehash: c23fe66c58e9ceff74469cc8eab61eb606c57ee1
ms.contentlocale: nb-no
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-bank-facilities-and-posting-profiles-for-letters-of-guarantee"></a><span data-ttu-id="09acb-103">Definere bankfasiliteter og posteringsprofiler for garantibrev</span><span class="sxs-lookup"><span data-stu-id="09acb-103">Set up bank facilities and posting profiles for letters of guarantee</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="09acb-104">Denne oppgaven oppretter en bankfasilitet og posteringsprofil som er nødvendig for å behandle et garantibrev.</span><span class="sxs-lookup"><span data-stu-id="09acb-104">This task creates a Bank facility and posting profile that is needed to process a letter of guarantee.</span></span>



<span data-ttu-id="09acb-105">Denne oppgaven bruker demonstrasjonsfirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="09acb-105">This task uses the USMF demo company.</span></span> 




## <a name="general-ledger-parameter"></a><span data-ttu-id="09acb-106">Parameter for økonomimodul</span><span class="sxs-lookup"><span data-stu-id="09acb-106">General ledger parameter</span></span>
1. <span data-ttu-id="09acb-107">Gå til Kontant- og bankbehandling > Oppsett > Parametere for bankstyring.</span><span class="sxs-lookup"><span data-stu-id="09acb-107">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>
2. <span data-ttu-id="09acb-108">Vis delen Bankdokument.</span><span class="sxs-lookup"><span data-stu-id="09acb-108">Expand the Bank document section.</span></span>
3. <span data-ttu-id="09acb-109">Velg alternativet Aktiver garantibrev.</span><span class="sxs-lookup"><span data-stu-id="09acb-109">Select the Enable letter of guarantee option.</span></span>
4. <span data-ttu-id="09acb-110">Klikk rullegardinknappen i feltet Transaksjonsjournal for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="09acb-110">In the Transaction journal field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="09acb-111">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="09acb-111">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="09acb-112">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="09acb-112">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="09acb-113">Klikk kategorien Nummerserier.</span><span class="sxs-lookup"><span data-stu-id="09acb-113">Click the Number sequences tab.</span></span>
    * <span data-ttu-id="09acb-114">Definere nummerseriekode for garantibrevnummer og transaksjonsreferanser for garantibrev</span><span class="sxs-lookup"><span data-stu-id="09acb-114">Define number sequence code for Letter of guarantee number and Letter of guarantee transaction references</span></span>  
8. <span data-ttu-id="09acb-115">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="09acb-115">Click Save.</span></span>
9. <span data-ttu-id="09acb-116">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="09acb-116">Close the page.</span></span>

## <a name="create-bank-facility"></a><span data-ttu-id="09acb-117">Opprette bankfasilitet</span><span class="sxs-lookup"><span data-stu-id="09acb-117">Create Bank facility</span></span>
1. <span data-ttu-id="09acb-118">Gå til Kontant- og bankbehandling > Oppsett > Bankfasiliteter.</span><span class="sxs-lookup"><span data-stu-id="09acb-118">Go to Cash and bank management > Setup > Bank facilities.</span></span>
2. <span data-ttu-id="09acb-119">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="09acb-119">Click New.</span></span>
3. <span data-ttu-id="09acb-120">I feltet Fasilitetsgruppe angir du navnet på bankfasilitetsgruppen for garantibrevtransaksjonen.</span><span class="sxs-lookup"><span data-stu-id="09acb-120">In the Facility group field, enter the bank facility group name for the letter of guarantee transaction.</span></span>
4. <span data-ttu-id="09acb-121">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="09acb-121">In the Description field, type a value.</span></span>
5. <span data-ttu-id="09acb-122">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="09acb-122">Click Save.</span></span>
6. <span data-ttu-id="09acb-123">Klikk kategorien Fasilitetstyper.</span><span class="sxs-lookup"><span data-stu-id="09acb-123">Click the Facility types tab.</span></span>
7. <span data-ttu-id="09acb-124">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="09acb-124">Click New.</span></span>
8. <span data-ttu-id="09acb-125">I feltet Fasilitetstype skriver du inn navnet på bankfasilitetstypen som er relatert til bankfasilitetsavtalen.</span><span class="sxs-lookup"><span data-stu-id="09acb-125">In the Facility type field, enter the name of the bank facility type that is related to the bank facility agreement.</span></span>
9. <span data-ttu-id="09acb-126">Skriv inn en verdi i Beskrivelse-feltet.</span><span class="sxs-lookup"><span data-stu-id="09acb-126">In the Description field, type a value.</span></span>
10. <span data-ttu-id="09acb-127">Klikk rullegardinknappen i feltet Fasilitetsgruppe for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="09acb-127">In the Facility group field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="09acb-128">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="09acb-128">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="09acb-129">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="09acb-129">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="09acb-130">Velg et alternativ i feltet Fasilitetens art.</span><span class="sxs-lookup"><span data-stu-id="09acb-130">In the Facility nature field, select an option.</span></span>
14. <span data-ttu-id="09acb-131">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="09acb-131">Click Save.</span></span>
15. <span data-ttu-id="09acb-132">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="09acb-132">Close the page.</span></span>

## <a name="bank-posting-profile"></a><span data-ttu-id="09acb-133">Bankposteringsprofil</span><span class="sxs-lookup"><span data-stu-id="09acb-133">Bank posting profile</span></span>
1. <span data-ttu-id="09acb-134">Gå til Kontant- og bankbehandling > Oppsett > Posteringsprofil for bankdokumenter.</span><span class="sxs-lookup"><span data-stu-id="09acb-134">Go to Cash and bank management > Setup > Bank documents posting profile.</span></span>
2. <span data-ttu-id="09acb-135">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="09acb-135">Click New.</span></span>
3. <span data-ttu-id="09acb-136">Klikk rullegardinknappen i feltet Konto/gruppenummer for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="09acb-136">In the Account/Group number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="09acb-137">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="09acb-137">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="09acb-138">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="09acb-138">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="09acb-139">Velg hovedkonto for utligning i Utligningskonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="09acb-139">In the Settle account field, select the main account for settlement.</span></span>
7. <span data-ttu-id="09acb-140">Velg konto for utgiftstransaksjoner i Gebyrkonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="09acb-140">In the Charges account field, select the account for expense transactions.</span></span>
8. <span data-ttu-id="09acb-141">Velg konto for margintransaksjonen i Marginkonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="09acb-141">In the Margin account field, select the account for the margin transaction.</span></span>
9. <span data-ttu-id="09acb-142">I Likvidasjonskonto-feltet velger du likvidasjonskontoen for garantibrevtransaksjonen.</span><span class="sxs-lookup"><span data-stu-id="09acb-142">In the Liquidation account field, select the liquidation account for the letter of guarantee transaction.</span></span> 
10. <span data-ttu-id="09acb-143">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="09acb-143">Click Save.</span></span>
11. <span data-ttu-id="09acb-144">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="09acb-144">Close the page.</span></span>


