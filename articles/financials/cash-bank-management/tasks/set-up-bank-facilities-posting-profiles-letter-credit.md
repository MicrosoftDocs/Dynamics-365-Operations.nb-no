--- 
title: Definere bankfasiliteter og posteringsprofiler for remburs
description: "Denne prosedyren hjelper med å opprette en bankfasilitet og posteringsprofil som kreves for å behandle purringer."
author: kweekley
manager: AnnBe
ms.date: 10/27/2017
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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 708a961ccafd149ce3cd6090c4f671bb6aadb77f
ms.contentlocale: nb-no
ms.lasthandoff: 05/08/2018

---
# <a name="set-up-bank-facilities-and-posting-profiles-for-letter-of-credit"></a><span data-ttu-id="0b666-103">Definere bankfasiliteter og posteringsprofiler for remburs</span><span class="sxs-lookup"><span data-stu-id="0b666-103">Set up bank facilities and posting profiles for letter of credit</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0b666-104">Denne prosedyren hjelper med å opprette en bankfasilitet og posteringsprofil som kreves for å behandle purringer.</span><span class="sxs-lookup"><span data-stu-id="0b666-104">This procedure walks through creating a Bank facility and posting profile required to process Letters of credit.</span></span> 

<span data-ttu-id="0b666-105">Denne oppgaven bruker demonstrasjonsfirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="0b666-105">This task uses the demo company 'USMF'.</span></span>






## <a name="general-ledger-parameter"></a><span data-ttu-id="0b666-106">Parameter for økonomimodul</span><span class="sxs-lookup"><span data-stu-id="0b666-106">General ledger parameter</span></span>
1. <span data-ttu-id="0b666-107">Gå til Kontant- og bankbehandling > Oppsett > Parametere for bankstyring.</span><span class="sxs-lookup"><span data-stu-id="0b666-107">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>
2. <span data-ttu-id="0b666-108">Vis delen Bankdokument.</span><span class="sxs-lookup"><span data-stu-id="0b666-108">Expand the Bank document section.</span></span>
3. <span data-ttu-id="0b666-109">Velg alternativet Aktiver rembursimport.</span><span class="sxs-lookup"><span data-stu-id="0b666-109">Select the Enable import letter of credit option.</span></span>
4. <span data-ttu-id="0b666-110">Velg alternativet Aktiver remburseksport.</span><span class="sxs-lookup"><span data-stu-id="0b666-110">Select the Enable export letter of credit option.</span></span>
5. <span data-ttu-id="0b666-111">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="0b666-111">Click Save.</span></span>
6. <span data-ttu-id="0b666-112">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="0b666-112">Close the page.</span></span>

## <a name="create-bank-facility"></a><span data-ttu-id="0b666-113">Opprette bankfasilitet</span><span class="sxs-lookup"><span data-stu-id="0b666-113">Create Bank facility</span></span>
1. <span data-ttu-id="0b666-114">Gå til Kontant- og bankbehandling > Oppsett > Bankfasiliteter.</span><span class="sxs-lookup"><span data-stu-id="0b666-114">Go to Cash and bank management > Setup > Bank facilities.</span></span>
2. <span data-ttu-id="0b666-115">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="0b666-115">Click New.</span></span>
3. <span data-ttu-id="0b666-116">I feltet Fasilitetsgruppe angir du navnet på bankfasilitetsgruppen.</span><span class="sxs-lookup"><span data-stu-id="0b666-116">In the Facility group field, enter the bank facility group name.</span></span>
4. <span data-ttu-id="0b666-117">I feltet Beskrivelse skriver du inn beskrivelsen av bankfasilitetsgruppen.</span><span class="sxs-lookup"><span data-stu-id="0b666-117">In the Description field, enter the bank facility group description.</span></span>
5. <span data-ttu-id="0b666-118">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="0b666-118">Click Save.</span></span>
6. <span data-ttu-id="0b666-119">Klikk kategorien Fasilitetstyper.</span><span class="sxs-lookup"><span data-stu-id="0b666-119">Click the Facility types tab.</span></span>
7. <span data-ttu-id="0b666-120">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="0b666-120">Click New.</span></span>
8. <span data-ttu-id="0b666-121">I Fasilitetstype-feltet angir du en unik kode.</span><span class="sxs-lookup"><span data-stu-id="0b666-121">In the Facility type field, enter a unique code.</span></span>
9. <span data-ttu-id="0b666-122">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="0b666-122">In the Description field, type a value.</span></span>
10. <span data-ttu-id="0b666-123">Klikk rullegardinknappen i feltet Fasilitetsgruppe for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="0b666-123">In the Facility group field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="0b666-124">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="0b666-124">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="0b666-125">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="0b666-125">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="0b666-126">I feltet Fasilitetens art velger du arten for bankfasiliteten.</span><span class="sxs-lookup"><span data-stu-id="0b666-126">In the Facility nature field, select the nature of the bank facility.</span></span>
14. <span data-ttu-id="0b666-127">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="0b666-127">Click Save.</span></span>
15. <span data-ttu-id="0b666-128">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="0b666-128">Close the page.</span></span>

## <a name="bank-posting-profile"></a><span data-ttu-id="0b666-129">Bankposteringsprofil</span><span class="sxs-lookup"><span data-stu-id="0b666-129">Bank posting profile</span></span>
1. <span data-ttu-id="0b666-130">Gå til Kontant- og bankbehandling > Oppsett > Posteringsprofil for bankdokumenter.</span><span class="sxs-lookup"><span data-stu-id="0b666-130">Go to Cash and bank management > Setup > Bank documents posting profile.</span></span>
2. <span data-ttu-id="0b666-131">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="0b666-131">Click New.</span></span>
3. <span data-ttu-id="0b666-132">Klikk rullegardinknappen i feltet Konto/gruppenummer for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="0b666-132">In the Account/Group number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="0b666-133">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="0b666-133">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="0b666-134">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="0b666-134">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="0b666-135">Velg hovedkontoen for utligning.</span><span class="sxs-lookup"><span data-stu-id="0b666-135">Select the main account for settlement.</span></span>
    * <span data-ttu-id="0b666-136">Denne kontoen brukes ved beregning av kontantstrømprognose.</span><span class="sxs-lookup"><span data-stu-id="0b666-136">This account is used when calculating cash flow forecast.</span></span>  
7. <span data-ttu-id="0b666-137">Velg konto for utgiftstransaksjoner i Gebyrkonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="0b666-137">In the Charges account field, select the account for expense transactions.</span></span>
8. <span data-ttu-id="0b666-138">Velg konto for margintransaksjoner i Marginkonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="0b666-138">In the Margin account field, select the account for margin transactions.</span></span>
    * <span data-ttu-id="0b666-139">Denne kontoen blir debitert når åpningsmarginen blir postert, og kreditert når betalingen blir postert.</span><span class="sxs-lookup"><span data-stu-id="0b666-139">This account is debited when the opening margin is posted and credited when the payment is posted.</span></span>  
9. <span data-ttu-id="0b666-140">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="0b666-140">Click Save.</span></span>


