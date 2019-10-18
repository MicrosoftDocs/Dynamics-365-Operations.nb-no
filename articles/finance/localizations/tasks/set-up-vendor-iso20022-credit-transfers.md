---
title: Definere leverandørers bankkontoer for ISO20022-kreditoverføringer
description: Denne fremgangsmåten beskriver hvordan du definerer leverandøren og den leverandørspesifikke bankkontoinformasjonen som kreves for ISO20022-kredittoverføring eller en annen filgenerering for leverandørbetalinger.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, VendBankAccounts
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ab8c52b9b457505c2cf2bfca46cb938e73c0142e
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174982"
---
# <a name="set-up-vendors-and-vendor-bank-accounts-for-iso20022-credit-transfers"></a><span data-ttu-id="93af5-103">Definere leverandørers bankkontoer for ISO20022-kreditoverføringer</span><span class="sxs-lookup"><span data-stu-id="93af5-103">Set up vendors and vendor bank accounts for ISO20022 credit transfers</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="93af5-104">Denne fremgangsmåten beskriver hvordan du definerer leverandøren og den leverandørspesifikke bankkontoinformasjonen som kreves for ISO20022-kredittoverføring eller en annen filgenerering for leverandørbetalinger.</span><span class="sxs-lookup"><span data-stu-id="93af5-104">This procedure demonstrates how to set up the vendor and vendor specific bank account information required for ISO20022 Credit transfer or any other vendor payment file generation.</span></span> 

<span data-ttu-id="93af5-105">Demonstrasjonsdatafirmaet DEMF brukes til å opprette denne prosedyren.</span><span class="sxs-lookup"><span data-stu-id="93af5-105">The demo data company used to create this procedure is DEMF.</span></span>
<span data-ttu-id="93af5-106">Dette er den fjerde prosedyren av fem, som illustrerer leverandørbetalingsprosessen ved hjelp av konfigurasjoner for elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="93af5-106">This is the fourth procedure, out of five, that illustrates the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="93af5-107">Denne fremgangsmåten gjelder for en funksjon som ble lagt til i Dynamics 365 for Operations versjon 1611.</span><span class="sxs-lookup"><span data-stu-id="93af5-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="set-up-bank-details"></a><span data-ttu-id="93af5-108">Definere bankdetaljer</span><span class="sxs-lookup"><span data-stu-id="93af5-108">Set up bank details</span></span>
1. <span data-ttu-id="93af5-109">Gå til Leverandører > Leverandører > Alle leverandører.</span><span class="sxs-lookup"><span data-stu-id="93af5-109">Go to Accounts payable > Vendors > All vendors.</span></span>
2. <span data-ttu-id="93af5-110">Bruk hurtigfilteret for å søke etter poster.</span><span class="sxs-lookup"><span data-stu-id="93af5-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="93af5-111">Du kan for eksempel filtrere på Leverandørkonto-feltet med verdien DE-001.</span><span class="sxs-lookup"><span data-stu-id="93af5-111">For example, filter on the Vendor account field with a value of 'DE-001'.</span></span>
3. <span data-ttu-id="93af5-112">Klikk DE-001 for å åpne leverandørdetaljer.</span><span class="sxs-lookup"><span data-stu-id="93af5-112">Click DE-001 to open vendor details.</span></span>
4. <span data-ttu-id="93af5-113">Klikk Leverandør i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="93af5-113">On the Action Pane, click Vendor.</span></span>
5. <span data-ttu-id="93af5-114">Klikk Bankkontoer.</span><span class="sxs-lookup"><span data-stu-id="93af5-114">Click Bank accounts.</span></span>
6. <span data-ttu-id="93af5-115">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="93af5-115">Click Edit.</span></span>
    * <span data-ttu-id="93af5-116">Hvis ingen bankkonto er tilgjengelig, må du opprette en ny.</span><span class="sxs-lookup"><span data-stu-id="93af5-116">If there is no bank account available, you need to create a new one.</span></span>  
7. <span data-ttu-id="93af5-117">Skriv inn COBADEFFXXX i SWIFT-kode-feltet.</span><span class="sxs-lookup"><span data-stu-id="93af5-117">In the SWIFT code field, type 'COBADEFFXXX'.</span></span>
8. <span data-ttu-id="93af5-118">Skriv inn 36200400000628808808 i IBAN-feltet.</span><span class="sxs-lookup"><span data-stu-id="93af5-118">In the IBAN field, type 'DE36200400000628808808'.</span></span>
9. <span data-ttu-id="93af5-119">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="93af5-119">Close the page.</span></span>

## <a name="set-up-a-method-of-payment-for-the-vendor"></a><span data-ttu-id="93af5-120">Definere en betalingsmåte for leverandøren</span><span class="sxs-lookup"><span data-stu-id="93af5-120">Set up a method of payment for the vendor</span></span>
1. <span data-ttu-id="93af5-121">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="93af5-121">Click Edit.</span></span>
2. <span data-ttu-id="93af5-122">Vis eller skjul delen Betaling.</span><span class="sxs-lookup"><span data-stu-id="93af5-122">Expand or collapse the Payment section.</span></span>
3. <span data-ttu-id="93af5-123">Klikk rullegardinknappen i Betalingsmåte-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="93af5-123">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="93af5-124">Klikk koblingen i SEPA CT-raden i listen.</span><span class="sxs-lookup"><span data-stu-id="93af5-124">In the list, click the link in the SEPA CT row.</span></span>
5. <span data-ttu-id="93af5-125">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="93af5-125">Click Save.</span></span>

