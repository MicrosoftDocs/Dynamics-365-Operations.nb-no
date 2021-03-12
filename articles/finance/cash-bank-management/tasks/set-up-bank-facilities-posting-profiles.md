---
title: Definere bankfasiliteter og posteringsprofiler for garantibrev
description: Denne oppgaven oppretter en bankfasilitet og posteringsprofil som er nødvendig for å behandle et garantibrev.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankParameters, DefaultDashboard, BankDocumentSetup, BankDocumentPosting
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b6da3b9358192997de1d0231e5c9c8eaba92a23b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976273"
---
# <a name="set-up-bank-facilities-and-posting-profiles-for-letters-of-guarantee"></a><span data-ttu-id="7d138-103">Definere bankfasiliteter og posteringsprofiler for garantibrev</span><span class="sxs-lookup"><span data-stu-id="7d138-103">Set up bank facilities and posting profiles for letters of guarantee</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7d138-104">Denne oppgaven oppretter en bankfasilitet og posteringsprofil som er nødvendig for å behandle et garantibrev.</span><span class="sxs-lookup"><span data-stu-id="7d138-104">This task creates a Bank facility and posting profile that is needed to process a letter of guarantee.</span></span>



<span data-ttu-id="7d138-105">Denne oppgaven bruker demonstrasjonsfirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="7d138-105">This task uses the USMF demo company.</span></span> 




## <a name="general-ledger-parameter"></a><span data-ttu-id="7d138-106">Parameter for økonomimodul</span><span class="sxs-lookup"><span data-stu-id="7d138-106">General ledger parameter</span></span>
1. <span data-ttu-id="7d138-107">Gå til Kontant- og bankbehandling > Oppsett > Parametere for bankstyring.</span><span class="sxs-lookup"><span data-stu-id="7d138-107">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>
2. <span data-ttu-id="7d138-108">Vis delen Bankdokument.</span><span class="sxs-lookup"><span data-stu-id="7d138-108">Expand the Bank document section.</span></span>
3. <span data-ttu-id="7d138-109">Velg alternativet Aktiver garantibrev.</span><span class="sxs-lookup"><span data-stu-id="7d138-109">Select the Enable letter of guarantee option.</span></span>
4. <span data-ttu-id="7d138-110">Klikk rullegardinknappen i feltet Transaksjonsjournal for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="7d138-110">In the Transaction journal field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="7d138-111">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="7d138-111">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="7d138-112">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="7d138-112">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="7d138-113">Klikk kategorien Nummerserier.</span><span class="sxs-lookup"><span data-stu-id="7d138-113">Click the Number sequences tab.</span></span>
    * <span data-ttu-id="7d138-114">Definere nummerseriekode for garantibrevnummer og transaksjonsreferanser for garantibrev</span><span class="sxs-lookup"><span data-stu-id="7d138-114">Define number sequence code for Letter of guarantee number and Letter of guarantee transaction references</span></span>  
8. <span data-ttu-id="7d138-115">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="7d138-115">Click Save.</span></span>
9. <span data-ttu-id="7d138-116">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="7d138-116">Close the page.</span></span>

## <a name="create-bank-facility"></a><span data-ttu-id="7d138-117">Opprette bankfasilitet</span><span class="sxs-lookup"><span data-stu-id="7d138-117">Create Bank facility</span></span>
1. <span data-ttu-id="7d138-118">Gå til Kontant- og bankbehandling > Oppsett > Bankfasiliteter.</span><span class="sxs-lookup"><span data-stu-id="7d138-118">Go to Cash and bank management > Setup > Bank facilities.</span></span>
2. <span data-ttu-id="7d138-119">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="7d138-119">Click New.</span></span>
3. <span data-ttu-id="7d138-120">I feltet Fasilitetsgruppe angir du navnet på bankfasilitetsgruppen for garantibrevtransaksjonen.</span><span class="sxs-lookup"><span data-stu-id="7d138-120">In the Facility group field, enter the bank facility group name for the letter of guarantee transaction.</span></span>
4. <span data-ttu-id="7d138-121">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="7d138-121">In the Description field, type a value.</span></span>
5. <span data-ttu-id="7d138-122">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="7d138-122">Click Save.</span></span>
6. <span data-ttu-id="7d138-123">Klikk kategorien Fasilitetstyper.</span><span class="sxs-lookup"><span data-stu-id="7d138-123">Click the Facility types tab.</span></span>
7. <span data-ttu-id="7d138-124">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="7d138-124">Click New.</span></span>
8. <span data-ttu-id="7d138-125">I feltet Fasilitetstype skriver du inn navnet på bankfasilitetstypen som er relatert til bankfasilitetsavtalen.</span><span class="sxs-lookup"><span data-stu-id="7d138-125">In the Facility type field, enter the name of the bank facility type that is related to the bank facility agreement.</span></span>
9. <span data-ttu-id="7d138-126">Skriv inn en verdi i Beskrivelse-feltet.</span><span class="sxs-lookup"><span data-stu-id="7d138-126">In the Description field, type a value.</span></span>
10. <span data-ttu-id="7d138-127">Klikk rullegardinknappen i feltet Fasilitetsgruppe for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="7d138-127">In the Facility group field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="7d138-128">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="7d138-128">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="7d138-129">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="7d138-129">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="7d138-130">Velg et alternativ i feltet Fasilitetens art.</span><span class="sxs-lookup"><span data-stu-id="7d138-130">In the Facility nature field, select an option.</span></span>
14. <span data-ttu-id="7d138-131">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="7d138-131">Click Save.</span></span>
15. <span data-ttu-id="7d138-132">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="7d138-132">Close the page.</span></span>

## <a name="bank-posting-profile"></a><span data-ttu-id="7d138-133">Bankposteringsprofil</span><span class="sxs-lookup"><span data-stu-id="7d138-133">Bank posting profile</span></span>
1. <span data-ttu-id="7d138-134">Gå til Kontant- og bankbehandling > Oppsett > Posteringsprofil for bankdokumenter.</span><span class="sxs-lookup"><span data-stu-id="7d138-134">Go to Cash and bank management > Setup > Bank documents posting profile.</span></span>
2. <span data-ttu-id="7d138-135">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="7d138-135">Click New.</span></span>
3. <span data-ttu-id="7d138-136">Klikk rullegardinknappen i feltet Konto/gruppenummer for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="7d138-136">In the Account/Group number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="7d138-137">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="7d138-137">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="7d138-138">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="7d138-138">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="7d138-139">Velg hovedkonto for utligning i Utligningskonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="7d138-139">In the Settle account field, select the main account for settlement.</span></span>
7. <span data-ttu-id="7d138-140">Velg konto for utgiftstransaksjoner i Gebyrkonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="7d138-140">In the Charges account field, select the account for expense transactions.</span></span>
8. <span data-ttu-id="7d138-141">Velg konto for margintransaksjonen i Marginkonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="7d138-141">In the Margin account field, select the account for the margin transaction.</span></span>
9. <span data-ttu-id="7d138-142">I Likvidasjonskonto-feltet velger du likvidasjonskontoen for garantibrevtransaksjonen.</span><span class="sxs-lookup"><span data-stu-id="7d138-142">In the Liquidation account field, select the liquidation account for the letter of guarantee transaction.</span></span> 
10. <span data-ttu-id="7d138-143">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="7d138-143">Click Save.</span></span>
11. <span data-ttu-id="7d138-144">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="7d138-144">Close the page.</span></span>

