---
title: Behandle rabatter for betaling
description: Denne fremgangsmåten beskriver hvordan du konverterer godkjente og behandlede kunderabatter til kreditnotaer.
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 412e7df299a419642018a62e6e8febd5d59c65e1
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148463"
---
# <a name="process-rebates-for-payment"></a><span data-ttu-id="cc5e8-103">Behandle rabatter for betaling</span><span class="sxs-lookup"><span data-stu-id="cc5e8-103">Process rebates for payment</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="cc5e8-104">Denne fremgangsmåten beskriver hvordan du konverterer godkjente og behandlede kunderabatter til kreditnotaer.</span><span class="sxs-lookup"><span data-stu-id="cc5e8-104">This procedure demonstrates how to convert approved and processed customer rebates to credit notes.</span></span> <span data-ttu-id="cc5e8-105">Du kan bruke denne veiledningen i USMF-demofirmaet.</span><span class="sxs-lookup"><span data-stu-id="cc5e8-105">You can use this guide in the USMF demo company.</span></span> <span data-ttu-id="cc5e8-106">Forutsetningen for denne veiledningen er å ha ett eller flere rabattkrav som har statusen for Merk.</span><span class="sxs-lookup"><span data-stu-id="cc5e8-106">The precondition for this guide is to have one or more rebate claims which have a status of Mark.</span></span> <span data-ttu-id="cc5e8-107">Hvis du bruker USMF, bør du kjøre veiledningen Generere og behandle kunderabatter før du starter denne veiledningen.</span><span class="sxs-lookup"><span data-stu-id="cc5e8-107">If you're using USMF you should run the "Generate and process customer rebates" guide before you start this guide.</span></span>


## <a name="convert-rebate-claims-to-credit-note"></a><span data-ttu-id="cc5e8-108">Konvertere rabattkrav til kreditnota</span><span class="sxs-lookup"><span data-stu-id="cc5e8-108">Convert rebate claims to credit note</span></span>
1. <span data-ttu-id="cc5e8-109">Gå til Alle kunder.</span><span class="sxs-lookup"><span data-stu-id="cc5e8-109">Go to All customers.</span></span>
2. <span data-ttu-id="cc5e8-110">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="cc5e8-110">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="cc5e8-111">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="cc5e8-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="cc5e8-112">Klikk Innkreving i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="cc5e8-112">On the Action Pane, click Collect.</span></span>
5. <span data-ttu-id="cc5e8-113">Klikk Utlign transaksjoner.</span><span class="sxs-lookup"><span data-stu-id="cc5e8-113">Click Settle transactions.</span></span>
6. <span data-ttu-id="cc5e8-114">Klikk Funksjoner.</span><span class="sxs-lookup"><span data-stu-id="cc5e8-114">Click Functions.</span></span>
7. <span data-ttu-id="cc5e8-115">Klikk Rabattprogram.</span><span class="sxs-lookup"><span data-stu-id="cc5e8-115">Click Rebate program.</span></span>
    * <span data-ttu-id="cc5e8-116">Rabatt-siden viser rabattkravene som du har behandlet i arbeidsområdet for kunderabatt, og som har statusen Merk.</span><span class="sxs-lookup"><span data-stu-id="cc5e8-116">The Rebate page lists the rebate claims that you have processed in the customer rebate workbench and that are in status Mark.</span></span>    
8. <span data-ttu-id="cc5e8-117">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="cc5e8-117">Click Edit.</span></span>
    * <span data-ttu-id="cc5e8-118">Angi merker i feltet Merk for kravene som du vil inkludere i kreditnotaen.</span><span class="sxs-lookup"><span data-stu-id="cc5e8-118">Set checkmarks in the Mark field for the claims that you want to include into credit note.</span></span>   
9. <span data-ttu-id="cc5e8-119">Klikk Funksjoner.</span><span class="sxs-lookup"><span data-stu-id="cc5e8-119">Click Functions.</span></span>
10. <span data-ttu-id="cc5e8-120">Klikk Opprett kreditnota.</span><span class="sxs-lookup"><span data-stu-id="cc5e8-120">Click Create credit note.</span></span>
    * <span data-ttu-id="cc5e8-121">Det vises en melding å informere deg om at en journal er postert (dette er kundeforbruksjournalen, som angitt på Kundeparametere-siden).</span><span class="sxs-lookup"><span data-stu-id="cc5e8-121">A message appears to inform you that a journal has been posted (This is the Accounts receivable consumption journal, as specified in the Accounts receivable parameters page).</span></span> <span data-ttu-id="cc5e8-122">Dette gjør at beløpet for reell gjeld (kredit) flyttes til kundesaldoen.</span><span class="sxs-lookup"><span data-stu-id="cc5e8-122">This causes the real liability (credit) amount to be moved to the customer balance.</span></span> <span data-ttu-id="cc5e8-123">Dette betyr at kundekontoen er kreditert, og avsetningskontoen for rabatt er debitert.</span><span class="sxs-lookup"><span data-stu-id="cc5e8-123">This means that the customer's account has been credited, and the Rebate accrual account has been debited.</span></span>  
11. <span data-ttu-id="cc5e8-124">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="cc5e8-124">Close the page.</span></span>
12. <span data-ttu-id="cc5e8-125">Klikk Avbryt.</span><span class="sxs-lookup"><span data-stu-id="cc5e8-125">Click Cancel.</span></span>
    * <span data-ttu-id="cc5e8-126">Dette oppdaterer siden slik at du kan se oppdateringene.</span><span class="sxs-lookup"><span data-stu-id="cc5e8-126">This refreshes the page so that you can see the updates.</span></span>  
13. <span data-ttu-id="cc5e8-127">Klikk Innkreving i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="cc5e8-127">On the Action Pane, click Collect.</span></span>
14. <span data-ttu-id="cc5e8-128">Klikk Utlign transaksjoner.</span><span class="sxs-lookup"><span data-stu-id="cc5e8-128">Click Settle transactions.</span></span>
    * <span data-ttu-id="cc5e8-129">Legg merke til at en transaksjon for negativt beløp, som representerer det totale rabattbeløpet, uten fakturareferanse er lagt til i kundesaldoen.</span><span class="sxs-lookup"><span data-stu-id="cc5e8-129">Note that a transaction for negative amount, representing the total rebate amount, without invoice reference has been added to the customer balance.</span></span>   
15. <span data-ttu-id="cc5e8-130">Klikk Avbryt.</span><span class="sxs-lookup"><span data-stu-id="cc5e8-130">Click Cancel.</span></span>

