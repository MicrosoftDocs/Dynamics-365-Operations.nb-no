---
title: " Betalingskonfigurasjoner for detaljhandelsutdrag"
description: Denne prosedyren beskriver konfigurasjoner for betalingsmetoder for handel, som påvirker hvordan utdrag opprettes og posteres.
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailStoreTable, RetailStoreTenderTypeTable
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8723f786c2eaf5f045007de32ce5cbe57563eaf9
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5205703"
---
# <a name="payment-configurations-for-retail-statements"></a><span data-ttu-id="e65a1-103"> Betalingskonfigurasjoner for detaljhandelsutdrag</span><span class="sxs-lookup"><span data-stu-id="e65a1-103">Payment configurations for Retail statements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e65a1-104">Denne prosedyren beskriver konfigurasjoner for betalingsmetoder for handel, som påvirker hvordan utdrag opprettes og posteres.</span><span class="sxs-lookup"><span data-stu-id="e65a1-104">This procedure demonstrates configurations for Commerce store payment methods, which affect how statements get created and posted.</span></span>

<span data-ttu-id="e65a1-105">Denne registreringen bruker demonstrasjonsfirmaet USRT.</span><span class="sxs-lookup"><span data-stu-id="e65a1-105">This recording uses the USRT demo company.</span></span>

1. <span data-ttu-id="e65a1-106">Gå til Retail og Commerce > Kanaler > Butikker > Alle butikker.</span><span class="sxs-lookup"><span data-stu-id="e65a1-106">Go to Retail and Commerce > Channels > Stores > All stores.</span></span>
2. <span data-ttu-id="e65a1-107">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="e65a1-107">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="e65a1-108">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="e65a1-108">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="e65a1-109">Klikk Oppsett i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="e65a1-109">On the Action Pane, click Set up.</span></span>
5. <span data-ttu-id="e65a1-110">Klikk Betalingsmåter.</span><span class="sxs-lookup"><span data-stu-id="e65a1-110">Click Payment methods.</span></span>
6. <span data-ttu-id="e65a1-111">Vis eller skjul delen Postering.</span><span class="sxs-lookup"><span data-stu-id="e65a1-111">Expand or collapse the Posting section.</span></span>
7. <span data-ttu-id="e65a1-112">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="e65a1-112">Click Edit.</span></span>
    * <span data-ttu-id="e65a1-113">Velg om beløpene som er mottatt for denne betalingsmåten, skal posteres til en finanskonto eller bankkonto.</span><span class="sxs-lookup"><span data-stu-id="e65a1-113">Select whether the amounts received for this payment method should be posted to a ledger account or bank account.</span></span>  
    * <span data-ttu-id="e65a1-114">Velg kontoen som beløp som er mottatt for denne betalingsmåten, skal posteres til.</span><span class="sxs-lookup"><span data-stu-id="e65a1-114">Select the account that amounts received for this payment method should be posted to.</span></span>  
    * <span data-ttu-id="e65a1-115">Velg en konto for postering av mulige forskjeller mellom det totale transaksjonsbeløpet som er mottatt, og beløpet som er telt opp for denne betalingsmåten.</span><span class="sxs-lookup"><span data-stu-id="e65a1-115">Select an account to post possible differences between the total transaction amount received and the amount counted for this payment method.</span></span>  
    * <span data-ttu-id="e65a1-116">I dette feltet kan du angi et beløp for å kontrollere når differansebeløpet skal posteres til en annen differansekonto.</span><span class="sxs-lookup"><span data-stu-id="e65a1-116">In this field you can enter an amount to control when the difference amount should be posted to another difference account.</span></span> <span data-ttu-id="e65a1-117">Du kan bruke dette til å spore store forskjeller.</span><span class="sxs-lookup"><span data-stu-id="e65a1-117">You can use this to track big differences.</span></span>  
    * <span data-ttu-id="e65a1-118">Velg en konto for postering av mulige forskjeller mellom det totale transaksjonsbeløpet som er mottatt, og beløpet som er telt opp, når det overskrider verdien som er definert i feltet Største differansebeløp.</span><span class="sxs-lookup"><span data-stu-id="e65a1-118">Select an account to post possible differences between the total transaction amount received and the amount counted, when it exceeds the value that is defined in the "Maximum difference amount" field.</span></span>  
    * <span data-ttu-id="e65a1-119">Velg Ja for å postere bankdeponeringsbeløp til en separat konto.</span><span class="sxs-lookup"><span data-stu-id="e65a1-119">Select "Yes" to post bank drop amounts to a separate account.</span></span>  
    * <span data-ttu-id="e65a1-120">I dette feltet kan du velge om bankdeponeringsbeløp skal posteres til en finanskonto eller en bankkonto.</span><span class="sxs-lookup"><span data-stu-id="e65a1-120">In this field you can select whether bank drop amounts should be posted to a ledger account or a bank account.</span></span>  
    * <span data-ttu-id="e65a1-121">Velg kontoen bankdeponeringsbeløp skal posteres på.</span><span class="sxs-lookup"><span data-stu-id="e65a1-121">Select the account to post bank drop amounts into.</span></span>  
    * <span data-ttu-id="e65a1-122">Velg banktransaksjonstypen som skal brukes ved postering av bankdeponeringsbeløp til bankkontoen.</span><span class="sxs-lookup"><span data-stu-id="e65a1-122">Select the bank transaction type to use when posting bank drop amounts to the bank account.</span></span>  
    * <span data-ttu-id="e65a1-123">Velg Ja for å postere safedeponeringsbeløp på en separat konto.</span><span class="sxs-lookup"><span data-stu-id="e65a1-123">Select "Yes" to post safe drop amounts to a separate account.</span></span>  
    * <span data-ttu-id="e65a1-124">Velg om safedeponeringsbeløp skal posteres til finanskontoen eller bankkontoen.</span><span class="sxs-lookup"><span data-stu-id="e65a1-124">Select whether safe drop amounts should be posted to the ledger account or the bank account.</span></span>  
    * <span data-ttu-id="e65a1-125">Velg kontoen safedeponeringsbeløp skal posteres på.</span><span class="sxs-lookup"><span data-stu-id="e65a1-125">Select the account to post safe drop amounts into.</span></span>  
8. <span data-ttu-id="e65a1-126">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="e65a1-126">Click Save.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]