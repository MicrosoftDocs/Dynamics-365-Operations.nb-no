--- 
title: "Definere firmaets bankkontoer for ISO20022-kreditoverføringer"
description: Denne prosedyren beskriver hvordan du definerer firmaspesifikk bankkontoinformasjon som kreves for generering av betalingsfilen.
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
ms.openlocfilehash: 1d0eabdfdeb5ed7d0bdb6df87ebdfa0d41e87492
ms.contentlocale: nb-no
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-company-bank-accounts-for-iso20022-credit-transfers"></a><span data-ttu-id="fb997-103">Definere firmaets bankkontoer for ISO20022-kreditoverføringer</span><span class="sxs-lookup"><span data-stu-id="fb997-103">Set up company bank accounts for ISO20022 credit transfers</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fb997-104">Denne prosedyren beskriver hvordan du definerer firmaspesifikk bankkontoinformasjon som kreves for generering av betalingsfilen.</span><span class="sxs-lookup"><span data-stu-id="fb997-104">This procedure shows how to set up company-specific bank account information that is required for payment file generation.</span></span> <span data-ttu-id="fb997-105">Du kan angi informasjon som kreves for å generere ISO 20022-kredittoverføringsformat, men avhengig av formatet kan det være annen informasjon som kreves, for eksempel firma-ID eller sorteringskode.</span><span class="sxs-lookup"><span data-stu-id="fb997-105">You set up information required to generate ISO 20022 credit transfer format but depending on the format there might be other information required, such as the Company ID or the Sort code.</span></span> 

<span data-ttu-id="fb997-106">Demonstrasjonsdatafirmaet DEMF brukes til å opprette denne prosedyren.</span><span class="sxs-lookup"><span data-stu-id="fb997-106">The demo data company used to create this procedure is DEMF.</span></span>

<span data-ttu-id="fb997-107">Dette er den andre prosedyren av fem, som illustrerer leverandørbetalingsprosessen ved hjelp av konfigurasjoner for elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="fb997-107">This is the second procedure, out of five, that illustrates the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="fb997-108">Denne fremgangsmåten gjelder for en funksjon som ble lagt til i Dynamics 365 for Operations, versjon 1611.</span><span class="sxs-lookup"><span data-stu-id="fb997-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="set-up-iban-and-swift-code"></a><span data-ttu-id="fb997-109">Konfigurere IBAN- og SWIFT-kode</span><span class="sxs-lookup"><span data-stu-id="fb997-109">Set up IBAN and SWIFT code</span></span>
1. <span data-ttu-id="fb997-110">Gå til Kontant- og bankbehandling > Bankkontoer.</span><span class="sxs-lookup"><span data-stu-id="fb997-110">Go to Cash and bank management > Bank accounts.</span></span>
2. <span data-ttu-id="fb997-111">Bruk hurtigfilteret til å filtrere på Bankkonto-feltet med en verdi lik DEMF OPER.</span><span class="sxs-lookup"><span data-stu-id="fb997-111">Use the Quick Filter to filter on the Bank account field with a value of 'DEMF OPER'.</span></span>
3. <span data-ttu-id="fb997-112">Klikk DEMF OPER for å åpne bankkontodetaljer.</span><span class="sxs-lookup"><span data-stu-id="fb997-112">Click DEMF OPER to open bank account details.</span></span>
4. <span data-ttu-id="fb997-113">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="fb997-113">Click Edit.</span></span>
5. <span data-ttu-id="fb997-114">Vis delen Tilleggsidentifikasjon.</span><span class="sxs-lookup"><span data-stu-id="fb997-114">Expand the Additional identification section.</span></span>
6. <span data-ttu-id="fb997-115">Skriv inn 89370400440532013000 i IBAN-feltet.</span><span class="sxs-lookup"><span data-stu-id="fb997-115">In the IBAN field, type 'DE89370400440532013000'.</span></span>
7. <span data-ttu-id="fb997-116">Skriv inn DEUTDEFF i SWIFT-kode-feltet.</span><span class="sxs-lookup"><span data-stu-id="fb997-116">In the SWIFT code field, type 'DEUTDEFF'.</span></span>
    * <span data-ttu-id="fb997-117">Vær oppmerksom på at SWIFT\BIC ikke er nødvendig for mange betalingsformater, men det anbefales at det er registrert for en bankkonto.</span><span class="sxs-lookup"><span data-stu-id="fb997-117">Note that SWIFT\BIC is not required for many payment formats, however it is recommended to have it registered for a bank account.</span></span>  
8. <span data-ttu-id="fb997-118">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="fb997-118">Click Save.</span></span>

## <a name="set-up-bank-account-for-the-legal-entity"></a><span data-ttu-id="fb997-119">Konfigurere bankkonto for juridisk enhet</span><span class="sxs-lookup"><span data-stu-id="fb997-119">Set up bank account for the legal entity</span></span>
1. <span data-ttu-id="fb997-120">Gå til Organisasjonsstyring > Organisasjoner > Juridiske enheter.</span><span class="sxs-lookup"><span data-stu-id="fb997-120">Go to Organization administration > Organizations > Legal entities.</span></span>
2. <span data-ttu-id="fb997-121">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="fb997-121">Click Edit.</span></span>
3. <span data-ttu-id="fb997-122">Utvid delen Bankkontoinformasjon.</span><span class="sxs-lookup"><span data-stu-id="fb997-122">Expand the Bank account information section.</span></span>
4. <span data-ttu-id="fb997-123">Angi eller velg en verdi i Bankkonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="fb997-123">In the Bank account field, enter or select a value.</span></span>
5. <span data-ttu-id="fb997-124">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="fb997-124">Click Save.</span></span>


