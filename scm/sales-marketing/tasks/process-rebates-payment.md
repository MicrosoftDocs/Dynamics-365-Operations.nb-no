--- 
title: Behandle rabatter for betaling
description: "Denne fremgangsmåten beskriver hvordan du konverterer godkjente og behandlede kunderabatter til kreditnotaer."
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 791ec304b9ea7c49fbea506d73c4daffd4478739
ms.contentlocale: nb-no
ms.lasthandoff: 08/29/2017

---
# <a name="process-rebates-for-payment"></a><span data-ttu-id="ff946-103">Behandle rabatter for betaling</span><span class="sxs-lookup"><span data-stu-id="ff946-103">Process rebates for payment</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ff946-104">Denne fremgangsmåten beskriver hvordan du konverterer godkjente og behandlede kunderabatter til kreditnotaer.</span><span class="sxs-lookup"><span data-stu-id="ff946-104">This procedure demonstrates how to convert approved and processed customer rebates to credit notes.</span></span> <span data-ttu-id="ff946-105">Du kan bruke denne veiledningen i USMF-demofirmaet.</span><span class="sxs-lookup"><span data-stu-id="ff946-105">You can use this guide in the USMF demo company.</span></span> <span data-ttu-id="ff946-106">Forutsetningen for denne veiledningen er å ha ett eller flere rabattkrav som har statusen for Merk.</span><span class="sxs-lookup"><span data-stu-id="ff946-106">The precondition for this guide is to have one or more rebate claims which have a status of Mark.</span></span> <span data-ttu-id="ff946-107">Hvis du bruker USMF, bør du kjøre veiledningen Generere og behandle kunderabatter før du starter denne veiledningen.</span><span class="sxs-lookup"><span data-stu-id="ff946-107">If you’re using USMF you should run the "Generate and process customer rebates" guide before you start this guide.</span></span>


## <a name="convert-rebate-claims-to-credit-note"></a><span data-ttu-id="ff946-108">Konvertere rabattkrav til kreditnota</span><span class="sxs-lookup"><span data-stu-id="ff946-108">Convert rebate claims to credit note</span></span>
1. <span data-ttu-id="ff946-109">Gå til Alle kunder.</span><span class="sxs-lookup"><span data-stu-id="ff946-109">Go to All customers.</span></span>
2. <span data-ttu-id="ff946-110">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="ff946-110">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="ff946-111">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="ff946-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="ff946-112">Klikk Innkreving i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="ff946-112">On the Action Pane, click Collect.</span></span>
5. <span data-ttu-id="ff946-113">Klikk Utlign transaksjoner.</span><span class="sxs-lookup"><span data-stu-id="ff946-113">Click Settle transactions.</span></span>
6. <span data-ttu-id="ff946-114">Klikk Funksjoner.</span><span class="sxs-lookup"><span data-stu-id="ff946-114">Click Functions.</span></span>
7. <span data-ttu-id="ff946-115">Klikk Rabattprogram.</span><span class="sxs-lookup"><span data-stu-id="ff946-115">Click Rebate program.</span></span>
    * <span data-ttu-id="ff946-116">Rabatt-siden viser rabattkravene som du har behandlet i arbeidsområdet for kunderabatt, og som har statusen Merk.</span><span class="sxs-lookup"><span data-stu-id="ff946-116">The Rebate page lists the rebate claims that you have processed in the customer rebate workbench and that are in status Mark.</span></span>    
8. <span data-ttu-id="ff946-117">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="ff946-117">Click Edit.</span></span>
    * <span data-ttu-id="ff946-118">Angi merker i feltet Merk for kravene som du vil inkludere i kreditnotaen.</span><span class="sxs-lookup"><span data-stu-id="ff946-118">Set checkmarks in the Mark field for the claims that you want to include into credit note.</span></span>   
9. <span data-ttu-id="ff946-119">Klikk Funksjoner.</span><span class="sxs-lookup"><span data-stu-id="ff946-119">Click Functions.</span></span>
10. <span data-ttu-id="ff946-120">Klikk Opprett kreditnota.</span><span class="sxs-lookup"><span data-stu-id="ff946-120">Click Create credit note.</span></span>
    * <span data-ttu-id="ff946-121">Det vises en melding å informere deg om at en journal er postert (dette er kundeforbruksjournalen, som angitt på Kundeparametere-siden).</span><span class="sxs-lookup"><span data-stu-id="ff946-121">A message appears to inform you that a journal has been posted (This is the Accounts receivable consumption journal, as specified in the Accounts receivable parameters page).</span></span> <span data-ttu-id="ff946-122">Dette gjør at beløpet for reell gjeld (kredit) flyttes til kundesaldoen.</span><span class="sxs-lookup"><span data-stu-id="ff946-122">This causes the real liability (credit) amount to be moved to the customer balance.</span></span> <span data-ttu-id="ff946-123">Dette betyr at kundekontoen er kreditert, og avsetningskontoen for rabatt er debitert.</span><span class="sxs-lookup"><span data-stu-id="ff946-123">This means that the customer’s account has been credited, and the Rebate accrual account has been debited.</span></span>  
11. <span data-ttu-id="ff946-124">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="ff946-124">Close the page.</span></span>
12. <span data-ttu-id="ff946-125">Klikk Avbryt.</span><span class="sxs-lookup"><span data-stu-id="ff946-125">Click Cancel.</span></span>
    * <span data-ttu-id="ff946-126">Dette oppdaterer siden slik at du kan se oppdateringene.</span><span class="sxs-lookup"><span data-stu-id="ff946-126">This refreshes the page so that you can see the updates.</span></span>  
13. <span data-ttu-id="ff946-127">Klikk Innkreving i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="ff946-127">On the Action Pane, click Collect.</span></span>
14. <span data-ttu-id="ff946-128">Klikk Utlign transaksjoner.</span><span class="sxs-lookup"><span data-stu-id="ff946-128">Click Settle transactions.</span></span>
    * <span data-ttu-id="ff946-129">Legg merke til at en transaksjon for negativt beløp, som representerer det totale rabattbeløpet, uten fakturareferanse er lagt til i kundesaldoen.</span><span class="sxs-lookup"><span data-stu-id="ff946-129">Note that a transaction for negative amount, representing the total rebate amount, without invoice reference has been added to the customer balance.</span></span>   
15. <span data-ttu-id="ff946-130">Klikk Avbryt.</span><span class="sxs-lookup"><span data-stu-id="ff946-130">Click Cancel.</span></span>


