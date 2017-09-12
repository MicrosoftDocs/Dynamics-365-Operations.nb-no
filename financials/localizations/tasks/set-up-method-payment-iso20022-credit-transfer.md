--- 
title: "Definere en betalingsmåte for ISO20022-kredittoverføring"
description: "Denne fremgangsmåten viser hvordan du setter opp leverandørbetalingsmåten for ISO20022-kredittoverføring eller andre betalingsmåter ved hjelp av elektronisk rapportering for å generere en fil."
author: mrolecki
manager: AnnBe
ms.date: 10/24/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: bed51f8749dfa0264ad39f51f9ceb295ac46fe93
ms.contentlocale: nb-no
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-method-of-payment-for-iso20022-credit-transfer"></a><span data-ttu-id="145e9-103">Definere en betalingsmåte for ISO20022-kredittoverføring</span><span class="sxs-lookup"><span data-stu-id="145e9-103">Set up method of payment for ISO20022 credit transfer</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="145e9-104">Denne fremgangsmåten viser hvordan du setter opp leverandørbetalingsmåten for ISO20022-kredittoverføring eller andre betalingsmåter ved hjelp av elektronisk rapportering for å generere en fil.</span><span class="sxs-lookup"><span data-stu-id="145e9-104">This procedure shows how to set up the vendor method of payment for ISO20022 credit transfer or any other payment type using electronic reporting to generate a file.</span></span> 

<span data-ttu-id="145e9-105">Før du fullfører denne oppgaven, må du definere eksportformatkonfigurasjoner og konfigurere betalingskontoer.</span><span class="sxs-lookup"><span data-stu-id="145e9-105">Before you complete this task, you must export format configurations and set up payment accounts.</span></span>

<span data-ttu-id="145e9-106">Denne oppgaven ble opprettet med demonstrasjonsdatafirmaet DEMF.</span><span class="sxs-lookup"><span data-stu-id="145e9-106">This task was created using the DEMF demo data company.</span></span>

<span data-ttu-id="145e9-107">Dette er den tredje prosedyren av fem, som illustrerer leverandørbetalingsprosessen ved hjelp av konfigurasjoner for elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="145e9-107">This is the third procedure, out of five, that illustrates the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="145e9-108">Denne fremgangsmåten gjelder for en funksjon som ble lagt til i Dynamics 365 for Operations, versjon 1611.</span><span class="sxs-lookup"><span data-stu-id="145e9-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="145e9-109">Gå til Leverandører > Betalingsoppsett > Betalingsmåter.</span><span class="sxs-lookup"><span data-stu-id="145e9-109">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
2. <span data-ttu-id="145e9-110">Bruk hurtigfilteret for å søke etter poster.</span><span class="sxs-lookup"><span data-stu-id="145e9-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="145e9-111">Du kan for eksempel filtrere på Betalingsmåte-feltet med verdien SEPA CT.</span><span class="sxs-lookup"><span data-stu-id="145e9-111">For example, filter on the Method of payment field with a value of 'SEPA CT'.</span></span>
3. <span data-ttu-id="145e9-112">Klikk Rediger</span><span class="sxs-lookup"><span data-stu-id="145e9-112">Click Edit.</span></span>
4. <span data-ttu-id="145e9-113">Velg Total i Periode-feltet.</span><span class="sxs-lookup"><span data-stu-id="145e9-113">In the Period field, select 'Total'.</span></span>
5. <span data-ttu-id="145e9-114">Velg Elektronisk betaling i Betalingstype-feltet.</span><span class="sxs-lookup"><span data-stu-id="145e9-114">In the Payment type field, select 'Electronic payment'.</span></span>
6. <span data-ttu-id="145e9-115">Vis delen Filformater.</span><span class="sxs-lookup"><span data-stu-id="145e9-115">Expand the File formats section.</span></span>
7. <span data-ttu-id="145e9-116">Velg Ja i feltet Generell elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="145e9-116">Select Yes in the Generic electronic reporting field.</span></span>
8. <span data-ttu-id="145e9-117">Angi eller velg en verdi i feltet Eksportformatkonfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="145e9-117">In the Export format configuration field, enter or select a value.</span></span>
    * <span data-ttu-id="145e9-118">I listen velger du verdien ISO20022 kredittoverføring (DE).</span><span class="sxs-lookup"><span data-stu-id="145e9-118">In the list, select the value ISO20022 Credit transfer (DE).</span></span> <span data-ttu-id="145e9-119">Hvis listen er tom, er ikke konfigurasjonen for eksportformater for leverandørbetaling importert og aktiv.</span><span class="sxs-lookup"><span data-stu-id="145e9-119">If the list is empty, the vendor payment export format configuration is not imported and active.</span></span>  
9. <span data-ttu-id="145e9-120">Velg Bank i feltet Kontotype.</span><span class="sxs-lookup"><span data-stu-id="145e9-120">In the Account type field, select 'Bank'.</span></span>
10. <span data-ttu-id="145e9-121">Angi verdiene DEMF OPER i feltet Betalingskonto.</span><span class="sxs-lookup"><span data-stu-id="145e9-121">In the Payment account field, specify the values 'DEMF OPER'.</span></span>
11. <span data-ttu-id="145e9-122">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="145e9-122">Click Save.</span></span>


