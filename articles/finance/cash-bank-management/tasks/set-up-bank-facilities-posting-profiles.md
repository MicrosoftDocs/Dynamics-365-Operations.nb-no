---
title: Definere bankfasiliteter og posteringsprofiler for garantibrev
description: Denne oppgaven oppretter en bankfasilitet og posteringsprofil som er nødvendig for å behandle et garantibrev.
author: kweekley
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BankParameters, DefaultDashboard, BankDocumentSetup, BankDocumentPosting
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1147650944ba40d1c8054444c09db9c5ee97bde3
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834626"
---
# <a name="set-up-bank-facilities-and-posting-profiles-for-letters-of-guarantee"></a><span data-ttu-id="ce8e1-103">Definere bankfasiliteter og posteringsprofiler for garantibrev</span><span class="sxs-lookup"><span data-stu-id="ce8e1-103">Set up bank facilities and posting profiles for letters of guarantee</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ce8e1-104">Denne oppgaven oppretter en bankfasilitet og posteringsprofil som er nødvendig for å behandle et garantibrev.</span><span class="sxs-lookup"><span data-stu-id="ce8e1-104">This task creates a Bank facility and posting profile that is needed to process a letter of guarantee.</span></span>



<span data-ttu-id="ce8e1-105">Denne oppgaven bruker demonstrasjonsfirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="ce8e1-105">This task uses the USMF demo company.</span></span> 




## <a name="general-ledger-parameter"></a><span data-ttu-id="ce8e1-106">Parameter for økonomimodul</span><span class="sxs-lookup"><span data-stu-id="ce8e1-106">General ledger parameter</span></span>
1. <span data-ttu-id="ce8e1-107">Gå til Kontant- og bankbehandling > Oppsett > Parametere for bankstyring.</span><span class="sxs-lookup"><span data-stu-id="ce8e1-107">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>
2. <span data-ttu-id="ce8e1-108">Vis delen Bankdokument.</span><span class="sxs-lookup"><span data-stu-id="ce8e1-108">Expand the Bank document section.</span></span>
3. <span data-ttu-id="ce8e1-109">Velg alternativet Aktiver garantibrev.</span><span class="sxs-lookup"><span data-stu-id="ce8e1-109">Select the Enable letter of guarantee option.</span></span>
4. <span data-ttu-id="ce8e1-110">Klikk rullegardinknappen i feltet Transaksjonsjournal for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="ce8e1-110">In the Transaction journal field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="ce8e1-111">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="ce8e1-111">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="ce8e1-112">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="ce8e1-112">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="ce8e1-113">Klikk kategorien Nummerserier.</span><span class="sxs-lookup"><span data-stu-id="ce8e1-113">Click the Number sequences tab.</span></span>
    * <span data-ttu-id="ce8e1-114">Definere nummerseriekode for garantibrevnummer og transaksjonsreferanser for garantibrev</span><span class="sxs-lookup"><span data-stu-id="ce8e1-114">Define number sequence code for Letter of guarantee number and Letter of guarantee transaction references</span></span>  
8. <span data-ttu-id="ce8e1-115">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="ce8e1-115">Click Save.</span></span>
9. <span data-ttu-id="ce8e1-116">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="ce8e1-116">Close the page.</span></span>

## <a name="create-bank-facility"></a><span data-ttu-id="ce8e1-117">Opprette bankfasilitet</span><span class="sxs-lookup"><span data-stu-id="ce8e1-117">Create Bank facility</span></span>
1. <span data-ttu-id="ce8e1-118">Gå til Kontant- og bankbehandling > Oppsett > Bankfasiliteter.</span><span class="sxs-lookup"><span data-stu-id="ce8e1-118">Go to Cash and bank management > Setup > Bank facilities.</span></span>
2. <span data-ttu-id="ce8e1-119">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="ce8e1-119">Click New.</span></span>
3. <span data-ttu-id="ce8e1-120">I feltet Fasilitetsgruppe angir du navnet på bankfasilitetsgruppen for garantibrevtransaksjonen.</span><span class="sxs-lookup"><span data-stu-id="ce8e1-120">In the Facility group field, enter the bank facility group name for the letter of guarantee transaction.</span></span>
4. <span data-ttu-id="ce8e1-121">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="ce8e1-121">In the Description field, type a value.</span></span>
5. <span data-ttu-id="ce8e1-122">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="ce8e1-122">Click Save.</span></span>
6. <span data-ttu-id="ce8e1-123">Klikk kategorien Fasilitetstyper.</span><span class="sxs-lookup"><span data-stu-id="ce8e1-123">Click the Facility types tab.</span></span>
7. <span data-ttu-id="ce8e1-124">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="ce8e1-124">Click New.</span></span>
8. <span data-ttu-id="ce8e1-125">I feltet Fasilitetstype skriver du inn navnet på bankfasilitetstypen som er relatert til bankfasilitetsavtalen.</span><span class="sxs-lookup"><span data-stu-id="ce8e1-125">In the Facility type field, enter the name of the bank facility type that is related to the bank facility agreement.</span></span>
9. <span data-ttu-id="ce8e1-126">Skriv inn en verdi i Beskrivelse-feltet.</span><span class="sxs-lookup"><span data-stu-id="ce8e1-126">In the Description field, type a value.</span></span>
10. <span data-ttu-id="ce8e1-127">Klikk rullegardinknappen i feltet Fasilitetsgruppe for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="ce8e1-127">In the Facility group field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="ce8e1-128">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="ce8e1-128">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="ce8e1-129">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="ce8e1-129">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="ce8e1-130">Velg et alternativ i feltet Fasilitetens art.</span><span class="sxs-lookup"><span data-stu-id="ce8e1-130">In the Facility nature field, select an option.</span></span>
14. <span data-ttu-id="ce8e1-131">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="ce8e1-131">Click Save.</span></span>
15. <span data-ttu-id="ce8e1-132">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="ce8e1-132">Close the page.</span></span>

## <a name="bank-posting-profile"></a><span data-ttu-id="ce8e1-133">Bankposteringsprofil</span><span class="sxs-lookup"><span data-stu-id="ce8e1-133">Bank posting profile</span></span>
1. <span data-ttu-id="ce8e1-134">Gå til Kontant- og bankbehandling > Oppsett > Posteringsprofil for bankdokumenter.</span><span class="sxs-lookup"><span data-stu-id="ce8e1-134">Go to Cash and bank management > Setup > Bank documents posting profile.</span></span>
2. <span data-ttu-id="ce8e1-135">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="ce8e1-135">Click New.</span></span>
3. <span data-ttu-id="ce8e1-136">Klikk rullegardinknappen i feltet Konto/gruppenummer for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="ce8e1-136">In the Account/Group number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="ce8e1-137">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="ce8e1-137">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="ce8e1-138">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="ce8e1-138">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="ce8e1-139">Velg hovedkonto for utligning i Utligningskonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="ce8e1-139">In the Settle account field, select the main account for settlement.</span></span>
7. <span data-ttu-id="ce8e1-140">Velg konto for utgiftstransaksjoner i Gebyrkonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="ce8e1-140">In the Charges account field, select the account for expense transactions.</span></span>
8. <span data-ttu-id="ce8e1-141">Velg konto for margintransaksjonen i Marginkonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="ce8e1-141">In the Margin account field, select the account for the margin transaction.</span></span>
9. <span data-ttu-id="ce8e1-142">I Likvidasjonskonto-feltet velger du likvidasjonskontoen for garantibrevtransaksjonen.</span><span class="sxs-lookup"><span data-stu-id="ce8e1-142">In the Liquidation account field, select the liquidation account for the letter of guarantee transaction.</span></span> 
10. <span data-ttu-id="ce8e1-143">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="ce8e1-143">Click Save.</span></span>
11. <span data-ttu-id="ce8e1-144">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="ce8e1-144">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]