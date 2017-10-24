---
title: Definere SEPA-avtalegiromandat
description: 
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 59491
ms.assetid: 653a135f-c515-4ae3-9da2-82b5e1f103b5
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 8b50c2d585c7e0bcd8dc15aa70446cd7346ad33c
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---

# <a name="set-up-sepa-direct-debit-mandate"></a><span data-ttu-id="ee381-102">Definere SEPA-avtalegiromandat</span><span class="sxs-lookup"><span data-stu-id="ee381-102">Set up SEPA direct debit mandate</span></span>

[!include[banner](../includes/banner.md)]




<span data-ttu-id="ee381-103">Med en SEPA-avtalegiro (Single Euro Payment Area) kan kreditor kreve inn penger fra kundens bankkonto, forutsatt at kunden har gitt kreditoren et signert mandat.</span><span class="sxs-lookup"><span data-stu-id="ee381-103">A Single Euro Payment Area (SEPA) direct debit lets a creditor collect funds from a customer's bank account, provided that the customer has granted a signed mandate to the creditor.</span></span> <span data-ttu-id="ee381-104">Mandatet som kunden signerer, tillater kreditor å kreve betaling og instruerer kundens bank om å betale purringen.</span><span class="sxs-lookup"><span data-stu-id="ee381-104">The mandate that the customer signs authorizes the creditor to collect a payment and instructs the customer's bank to pay the collection.</span></span> <span data-ttu-id="ee381-105">Dette emnet er organisert slik at det viser prosessen med å definere SEPA-avtalegiromandater.</span><span class="sxs-lookup"><span data-stu-id="ee381-105">This topic is organized to show the process for setting up SEPA direct debit mandates.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="ee381-106">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="ee381-106">Prerequisites</span></span>
<span data-ttu-id="ee381-107">Tabellen nedenfor viser forutsetninger som må være på plass før du starter.</span><span class="sxs-lookup"><span data-stu-id="ee381-107">The following table shows the prerequisites that must be in place before you start.</span></span>

| <span data-ttu-id="ee381-108">Kategori</span><span class="sxs-lookup"><span data-stu-id="ee381-108">Category</span></span>       | <span data-ttu-id="ee381-109">Forutsetning</span><span class="sxs-lookup"><span data-stu-id="ee381-109">Prerequisite</span></span>                                                                                                                                              |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee381-110">Land/område</span><span class="sxs-lookup"><span data-stu-id="ee381-110">Country/region</span></span> | <span data-ttu-id="ee381-111">Primæradressen for den juridiske enheten må være i følgende land: Østerrike, Belgia, Tyskland, Spania, Frankrike, Italia eller Nederland.</span><span class="sxs-lookup"><span data-stu-id="ee381-111">The primary address for the legal entity must be in the following countries/regions: Austria, Belgium, Germany, Spain, France, Italy, or the Netherlands.</span></span> |

1. <span data-ttu-id="ee381-112">Angi en nummerserie for avtalegiromandater. Hver avtalegiromandat må ha et unikt nummer.</span><span class="sxs-lookup"><span data-stu-id="ee381-112">Set up a number sequence for direct debit mandates Each direct debit mandate must have a unique number.</span></span> <span data-ttu-id="ee381-113">Bruk siden **Nummerserier** til å opprette en nummerserie for avtalegiromandater.</span><span class="sxs-lookup"><span data-stu-id="ee381-113">Use the **Number sequences** page to create a number sequence for direct debit mandates.</span></span> <span data-ttu-id="ee381-114">Du bruker denne identifikatoren til å tilordne nummerserien til systemet for avtalegiromandat på siden **Kundeparametere**.</span><span class="sxs-lookup"><span data-stu-id="ee381-114">You will use this identifier to assign the number sequence to the direct debit mandate system on the **Accounts receivable parameters** page.</span></span>

2. <span data-ttu-id="ee381-115">Definere kundeparametre for avtalegiromandater. Bruk siden **Kundeparametere** til å definere parametere for avtalegiromandater.</span><span class="sxs-lookup"><span data-stu-id="ee381-115">Set up Accounts receivable parameters for direct debit mandates Use the **Accounts receivable parameters** page to set up parameters for direct debit mandates.</span></span> <span data-ttu-id="ee381-116">For å definere parametere i kategorien **Avtalegiro** endrer du standardparameterne etter behov.</span><span class="sxs-lookup"><span data-stu-id="ee381-116">To set up the parameters, on the **Direct debit** tab, change the default parameters as you require.</span></span> <span data-ttu-id="ee381-117">I kategorien **Nummerserier** oppdaterer du feltet **ID for avtalegiromandat** med nummerserien som du tidligere definerte.</span><span class="sxs-lookup"><span data-stu-id="ee381-117">Then, on the **Number sequences** tab, update the **Direct debit mandate ID** field with the number sequence that you set up earlier.</span></span>

3. <span data-ttu-id="ee381-118">Definere en betalingsmåte for avtalegiromandater. Du må definere en betalingsmåte for avtalegiromandater.</span><span class="sxs-lookup"><span data-stu-id="ee381-118">Set up a method of payment for direct debit mandates You must set up a method of payment for direct debit mandates.</span></span> <span data-ttu-id="ee381-119">Du bruker denne betalingsmåten til å utføre spørringer for fakturaer du vil generere avtalegirobetaling for.</span><span class="sxs-lookup"><span data-stu-id="ee381-119">You use this method of payment to query for invoices to generate direct debit payments for.</span></span> <span data-ttu-id="ee381-120">Bruk siden **Betalingsmåter** til å definere betalingsmetoder.</span><span class="sxs-lookup"><span data-stu-id="ee381-120">Use the **Methods of payment** page to set up the method of payment.</span></span> <span data-ttu-id="ee381-121">Hvis du vil definere en betalingsmåte for avtalegiromandater, må du følge disse tilleggstrinnene for en betalingsmåte:</span><span class="sxs-lookup"><span data-stu-id="ee381-121">To set up a method of payment for direct debit mandates, you must follow these additional steps for a method of payment:</span></span>

-   <span data-ttu-id="ee381-122">I feltet **Betalingsmiddel** velger du **Elektronisk betaling**.</span><span class="sxs-lookup"><span data-stu-id="ee381-122">In the **Payment type** field, select **Electronic payment**.</span></span>
-   <span data-ttu-id="ee381-123">Valgfritt: Hvis du forventer at hver av kundene har flere mandater, velger du **Faktura** i **Periode**-feltet.</span><span class="sxs-lookup"><span data-stu-id="ee381-123">Optional: If you expect each of your customers to have multiple mandates, in the **Period** field, select **Invoice**.</span></span> <span data-ttu-id="ee381-124">Det blir opprettet en egen betaling for hver faktura, og hver betaling bruker mandatet som er angitt for fakturaen.</span><span class="sxs-lookup"><span data-stu-id="ee381-124">A separate payment will be created for each invoice, and each payment will use the mandate that is specified for the invoice.</span></span>
-   <span data-ttu-id="ee381-125">Velg **Krever mandat**-alternativet for å opprette betalinger ved hjelp av avtalegiromandater.</span><span class="sxs-lookup"><span data-stu-id="ee381-125">Select the **Require mandate** option to create payments by using direct debit mandates.</span></span> <span data-ttu-id="ee381-126">**Krever mandat**-alternativet er bare tilgjengelig hvis du velger **Elektronisk betaling** i feltet **Betalingstype**.</span><span class="sxs-lookup"><span data-stu-id="ee381-126">The **Require mandate** option is available only if you select **Electronic payment** in the **Payment type** field.</span></span>

<span data-ttu-id="ee381-127">Se også</span><span class="sxs-lookup"><span data-stu-id="ee381-127">See Also</span></span>

[<span data-ttu-id="ee381-128">Oversikt over avtalegiro</span><span class="sxs-lookup"><span data-stu-id="ee381-128">Direct debit overview</span></span>](sepa-direct-debit-overview.md) 

[<span data-ttu-id="ee381-129">Opprette et nytt avtalegiromandat for en kunde</span><span class="sxs-lookup"><span data-stu-id="ee381-129">Create a direct debit mandate for a customer</span></span>](tasks/create-direct-debit-mandate-customer.md) 


