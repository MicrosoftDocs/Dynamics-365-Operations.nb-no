---
title: Opprette og eksportere leverandørbetalinger ved hjelp av ISO20022-betalingsformat
description: Denne prosedyren viser hvordan du oppretter betalingslinjer i leverandørbetalingsjournalen og genererer en leverandørbetalingsfil ved hjelp av eksemplet med ISO2022-kredittoverføring.
author: mrolecki
manager: AnnBe
ms.date: 01/17/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendPaym, SysQueryForm, VendPaymProposalEdit, BankAccountTableLookUp
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b589d64a4446420164175b41f435cf48daac01a9
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1570059"
---
# <a name="create-and-export-vendor-payments-using-iso20022-payment-format"></a><span data-ttu-id="04298-103">Opprette og eksportere leverandørbetalinger ved hjelp av ISO20022-betalingsformat</span><span class="sxs-lookup"><span data-stu-id="04298-103">Create and export vendor payments using ISO20022 payment format</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="04298-104">Dette emnet forklarer hvordan du oppretter betalingslinjer i leverandørbetalingsjournalen og genererer en leverandørbetalingsfil ved hjelp av eksemplet med ISO2022-kredittoverføring.</span><span class="sxs-lookup"><span data-stu-id="04298-104">This topic explains how to create payment lines in the vendor payment journal and generate a vendor payment file using ISO2022 Credit transfer example.</span></span>

<span data-ttu-id="04298-105">Dette er den femte prosedyren av fem, som illustrerer leverandørbetalingsprosessen ved hjelp av konfigurasjoner for elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="04298-105">This is the fifth procedure, out of five, that illustrates the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="04298-106">Bruk DEMF-demodata til å utføre dette eksemplet.</span><span class="sxs-lookup"><span data-stu-id="04298-106">Use the DEMF demo data to complete this example.</span></span>

## <a name="example"></a><span data-ttu-id="04298-107">Eksempel</span><span class="sxs-lookup"><span data-stu-id="04298-107">Example</span></span>

1.  <span data-ttu-id="04298-108">Gå til **Leverandører > Betalinger > Betalingsjournal**.</span><span class="sxs-lookup"><span data-stu-id="04298-108">Go to **Accounts payable > Payments > Payment journal**.</span></span>
2.  <span data-ttu-id="04298-109">Klikk **Ny**.</span><span class="sxs-lookup"><span data-stu-id="04298-109">Click **New**.</span></span>
3.  <span data-ttu-id="04298-110">Angi eller velg en verdi i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="04298-110">In the **Name** field, enter or select a value.</span></span>
4.  <span data-ttu-id="04298-111">Klikk **Linjer > Betalingsforslag > Opprett betalingsforslag**.</span><span class="sxs-lookup"><span data-stu-id="04298-111">Click **Lines > Payment proposal > Create payment proposal**.</span></span>
5.  <span data-ttu-id="04298-112">Utvid delen **Poster som skal inkluderes**.</span><span class="sxs-lookup"><span data-stu-id="04298-112">Expand the **Records to include** section.</span></span>
6.  <span data-ttu-id="04298-113">Klikk **Filter**.</span><span class="sxs-lookup"><span data-stu-id="04298-113">Click **Filter**.</span></span>
7.  <span data-ttu-id="04298-114">I listen velger du raden for **Leverandører-tabellen** og **Leverandørkonto-feltet**.</span><span class="sxs-lookup"><span data-stu-id="04298-114">In the list, select the row for **Vendors table** and **Vendor account field**.</span></span>
8.  <span data-ttu-id="04298-115">Angi eller velg en verdi i **Kriterier**-feltet.</span><span class="sxs-lookup"><span data-stu-id="04298-115">In the **Criteria** field, enter or select a value.</span></span> <span data-ttu-id="04298-116">Du kan bruke hvilke som helst kriterier for å velge leverandørtransaksjoner som skal betales, men i dette eksemplet bruker du DE-001 som en leverandørkonto.</span><span class="sxs-lookup"><span data-stu-id="04298-116">You can apply any criteria for selecting vendor transactions to pay, for this example, use DE-001 as a vendor account.</span></span>
12. <span data-ttu-id="04298-117">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="04298-117">Click **OK**.</span></span>
13. <span data-ttu-id="04298-118">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="04298-118">Click **OK**.</span></span>
14. <span data-ttu-id="04298-119">Klikk **Opprett betalinger**.</span><span class="sxs-lookup"><span data-stu-id="04298-119">Click **Create payments**.</span></span>
15. <span data-ttu-id="04298-120">Generere en ISO20022-betalingsfil.</span><span class="sxs-lookup"><span data-stu-id="04298-120">Generate an ISO20022 payment file.</span></span>
    1.  <span data-ttu-id="04298-121">Klikk **Generer betalinger**.</span><span class="sxs-lookup"><span data-stu-id="04298-121">Click **Generate payments**.</span></span>
    2.  <span data-ttu-id="04298-122">Angi eller velg en verdi i **Betalingsmåte**-feltet.</span><span class="sxs-lookup"><span data-stu-id="04298-122">In the **Method of payment** field, enter or select a value.</span></span>
    3.  <span data-ttu-id="04298-123">Skriv inn en verdi i feltet **Filnavn**.</span><span class="sxs-lookup"><span data-stu-id="04298-123">In the **File name** field, type a value.</span></span> <span data-ttu-id="04298-124">I dette eksemplet blir den genererte filen SEPA-kompatibel på grunn av EUR-betalingen.</span><span class="sxs-lookup"><span data-stu-id="04298-124">For this example, because of the EUR payment, the generated file will be SEPA compliant.</span></span> <span data-ttu-id="04298-125">ISO20022 kredittoverføring i tillegg til andre leverandørbetalingsformater kan også brukes for å generere betalinger i andre valutaer.</span><span class="sxs-lookup"><span data-stu-id="04298-125">ISO20022 credit transfer as well as other vendor payment formats can also be used for generating payments in other currencies.</span></span>
    4.  <span data-ttu-id="04298-126">Angi eller velg en verdi i **Bankkonto**-feltet.</span><span class="sxs-lookup"><span data-stu-id="04298-126">In the **Bank account** field, enter or select a value.</span></span>

