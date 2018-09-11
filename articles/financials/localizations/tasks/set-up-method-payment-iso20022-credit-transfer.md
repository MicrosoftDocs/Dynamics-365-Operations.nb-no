--- 
title: "Definere en betalingsmåte for ISO20022-kredittoverføring"
description: "Denne fremgangsmåten viser hvordan du setter opp leverandørbetalingsmåten for ISO20022-kredittoverføring eller andre betalingsmåter ved hjelp av elektronisk rapportering for å generere en fil."
author: mrolecki
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendPaymMode
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 2c8e858f15047652b9d6561bc1a4ff8e09ea02d5
ms.contentlocale: nb-no
ms.lasthandoff: 09/11/2018

---
# <a name="set-up-method-of-payment-for-iso20022-credit-transfer"></a><span data-ttu-id="0d971-103">Definere en betalingsmåte for ISO20022-kredittoverføring</span><span class="sxs-lookup"><span data-stu-id="0d971-103">Set up method of payment for ISO20022 credit transfer</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0d971-104">Denne fremgangsmåten viser hvordan du setter opp leverandørbetalingsmåten for ISO20022-kredittoverføring eller andre betalingsmåter ved hjelp av elektronisk rapportering for å generere en fil.</span><span class="sxs-lookup"><span data-stu-id="0d971-104">This procedure shows how to set up the vendor method of payment for ISO20022 credit transfer or any other payment type using electronic reporting to generate a file.</span></span> 

<span data-ttu-id="0d971-105">Før du fullfører denne oppgaven, må du definere eksportformatkonfigurasjoner og konfigurere betalingskontoer.</span><span class="sxs-lookup"><span data-stu-id="0d971-105">Before you complete this task, you must export format configurations and set up payment accounts.</span></span>

<span data-ttu-id="0d971-106">Denne oppgaven ble opprettet med demonstrasjonsdatafirmaet DEMF.</span><span class="sxs-lookup"><span data-stu-id="0d971-106">This task was created using the DEMF demo data company.</span></span>

<span data-ttu-id="0d971-107">Dette er den tredje prosedyren av fem, som illustrerer leverandørbetalingsprosessen ved hjelp av konfigurasjoner for elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="0d971-107">This is the third procedure, out of five, that illustrates the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="0d971-108">Denne fremgangsmåten gjelder for en funksjon som ble lagt til i Dynamics 365 for Operations, versjon 1611.</span><span class="sxs-lookup"><span data-stu-id="0d971-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="0d971-109">Gå til Leverandører > Betalingsoppsett > Betalingsmåter.</span><span class="sxs-lookup"><span data-stu-id="0d971-109">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
2. <span data-ttu-id="0d971-110">Bruk hurtigfilteret for å søke etter poster.</span><span class="sxs-lookup"><span data-stu-id="0d971-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="0d971-111">Du kan for eksempel filtrere på Betalingsmåte-feltet med verdien SEPA CT.</span><span class="sxs-lookup"><span data-stu-id="0d971-111">For example, filter on the Method of payment field with a value of 'SEPA CT'.</span></span>
3. <span data-ttu-id="0d971-112">Klikk Rediger</span><span class="sxs-lookup"><span data-stu-id="0d971-112">Click Edit.</span></span>
4. <span data-ttu-id="0d971-113">Velg Total i Periode-feltet.</span><span class="sxs-lookup"><span data-stu-id="0d971-113">In the Period field, select 'Total'.</span></span>
5. <span data-ttu-id="0d971-114">Velg Elektronisk betaling i Betalingstype-feltet.</span><span class="sxs-lookup"><span data-stu-id="0d971-114">In the Payment type field, select 'Electronic payment'.</span></span>
6. <span data-ttu-id="0d971-115">Vis delen Filformater.</span><span class="sxs-lookup"><span data-stu-id="0d971-115">Expand the File formats section.</span></span>
7. <span data-ttu-id="0d971-116">Velg Ja i feltet Generell elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="0d971-116">Select Yes in the Generic electronic reporting field.</span></span>
8. <span data-ttu-id="0d971-117">Angi eller velg en verdi i feltet Eksportformatkonfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="0d971-117">In the Export format configuration field, enter or select a value.</span></span>
    * <span data-ttu-id="0d971-118">I listen velger du verdien ISO20022 kredittoverføring (DE).</span><span class="sxs-lookup"><span data-stu-id="0d971-118">In the list, select the value ISO20022 Credit transfer (DE).</span></span> <span data-ttu-id="0d971-119">Hvis listen er tom, er ikke konfigurasjonen for eksportformater for leverandørbetaling importert og aktiv.</span><span class="sxs-lookup"><span data-stu-id="0d971-119">If the list is empty, the vendor payment export format configuration is not imported and active.</span></span>  
9. <span data-ttu-id="0d971-120">Velg Bank i feltet Kontotype.</span><span class="sxs-lookup"><span data-stu-id="0d971-120">In the Account type field, select 'Bank'.</span></span>
10. <span data-ttu-id="0d971-121">Angi verdiene DEMF OPER i feltet Betalingskonto.</span><span class="sxs-lookup"><span data-stu-id="0d971-121">In the Payment account field, specify the values 'DEMF OPER'.</span></span>
11. <span data-ttu-id="0d971-122">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="0d971-122">Click Save.</span></span>


