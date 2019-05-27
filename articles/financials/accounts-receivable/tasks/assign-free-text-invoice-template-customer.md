---
title: Tilordne mal for fritekstfaktura til en kunde
description: Denne oppgaven beskriver hvordan du tilordner en mal for fritekstfaktura til en kunde.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, CustRecurrenceInvoice
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 317b3bd4c1f395987ef3dbbd268c40be5c688320
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1568986"
---
# <a name="assign-free-text-invoice-template-to-a-customer"></a><span data-ttu-id="d053a-103">Tilordne mal for fritekstfaktura til en kunde</span><span class="sxs-lookup"><span data-stu-id="d053a-103">Assign free text invoice template to a customer</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d053a-104">Denne oppgaven beskriver hvordan du tilordner en mal for fritekstfaktura til en kunde.</span><span class="sxs-lookup"><span data-stu-id="d053a-104">This task demonstrates how to assign a free text invoice template to a customer.</span></span> <span data-ttu-id="d053a-105">Denne oppgaven bruker USMF-demofirmaet og er ment for brukeren som er ansvarlig for administrasjon og behandling av fakturaer for kunder.</span><span class="sxs-lookup"><span data-stu-id="d053a-105">This task uses the USMF demo company and is intended for the user who is responsible for managing and processing A/R invoices.</span></span>

1. <span data-ttu-id="d053a-106">Gå til Kunder > Kunder > Alle kunder.</span><span class="sxs-lookup"><span data-stu-id="d053a-106">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="d053a-107">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="d053a-107">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="d053a-108">Klikk Faktura i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="d053a-108">On the Action Pane, click Invoice.</span></span>
4. <span data-ttu-id="d053a-109">Klikk Gjentakende fakturalinjer.</span><span class="sxs-lookup"><span data-stu-id="d053a-109">Click Recurring invoices.</span></span>
    * <span data-ttu-id="d053a-110">Bruk denne siden til å tilordne mallinjer for fritekstfaktura til kunder og angi hvor ofte fakturaer skal sendes til kunden.</span><span class="sxs-lookup"><span data-stu-id="d053a-110">Use this page to assign free text invoice templates to customers and specify how frequently invoices will be sent to the customer.</span></span>  
5. <span data-ttu-id="d053a-111">Klikk Ny for å tilordne en ny mal til kunden.</span><span class="sxs-lookup"><span data-stu-id="d053a-111">Click New to assign a new template to the customer.</span></span>
6. <span data-ttu-id="d053a-112">Velg malen for fritekstfaktura du vil tilordne til kunden.</span><span class="sxs-lookup"><span data-stu-id="d053a-112">Select the free text invoice template you want to assign to the customer.</span></span>
7. <span data-ttu-id="d053a-113">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="d053a-113">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="d053a-114">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="d053a-114">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="d053a-115">Angi datoen som den første fakturaen skal genereres på.</span><span class="sxs-lookup"><span data-stu-id="d053a-115">Enter the date when the first invoice will be generated.</span></span>
    * <span data-ttu-id="d053a-116">Angi en gjentakende sluttdato.</span><span class="sxs-lookup"><span data-stu-id="d053a-116">Enter a recurring end date.</span></span>  
    * <span data-ttu-id="d053a-117">Velg ett av følgende: Ingen sluttdato – fakturaer genereres helt til malen blir fjernet fra kundekontoen.</span><span class="sxs-lookup"><span data-stu-id="d053a-117">Select one of the following: No end date – Invoices will be generated indefinitely until the template is removed from the customer account.</span></span>  <span data-ttu-id="d053a-118">Sluttdato for fakturering – velg dette alternativet og angi den siste datoen som fakturaen kan genereres på.</span><span class="sxs-lookup"><span data-stu-id="d053a-118">Billing end date – Select this option and enter the last date that the invoice can be generated.</span></span>  
    * <span data-ttu-id="d053a-119">Maksimalt akkumulert beløp før fakturagenerering stopper.</span><span class="sxs-lookup"><span data-stu-id="d053a-119">Maximum cumulative amount after which invoice generation will stop.</span></span>  
    * <span data-ttu-id="d053a-120">Angi det maksimale akkumulerte beløpet som kan nås ved hjelp av den valgte malen.</span><span class="sxs-lookup"><span data-stu-id="d053a-120">Enter the maximum cumulative amount that can be reached using the selected template.</span></span> <span data-ttu-id="d053a-121">Hvis du for eksempel angir 1 000,00 og genererer månedlige fakturaer for 100,00 hver, stopper genereringen av fakturaer når den tiende fakturaen er generert.</span><span class="sxs-lookup"><span data-stu-id="d053a-121">For example, if you enter 1,000.00 and generate monthly invoices for 100.00 each, invoices will stop generating after the tenth invoice is generated.</span></span>  
    * <span data-ttu-id="d053a-122">Generer gjentakende fakturaer ved å bruke standardverdiene fra kundekontoen eller malen for fritekstfaktura.</span><span class="sxs-lookup"><span data-stu-id="d053a-122">Generate recurring invoices by using the default values from either free text invoice template or the customer account.</span></span>  
    * <span data-ttu-id="d053a-123">Velg om du vil bruke malen for fritekstfaktura eller kundekontoen for å bestemme standardverdiene for språket, posteringsprofilen, merverdiavgiftsgruppen, merverdiavgiftgruppen for vare, listekoden, land/område for levering, valuta, betalingsbetingelser, betalingsmåten, betalingsspesifikasjoner, betalingsplanen, kontantrabatt, finansdimensjoner og girokort når fakturaer opprettes.</span><span class="sxs-lookup"><span data-stu-id="d053a-123">Select whether to use the free text invoice template or the customer account to determine the default values for the language, posting profile, sales tax group, item sales tax group, list code, country/region for delivery, currency, terms of payment, method of payment, payment specification, payment schedule, cash discount, financial dimensions, and giro money transfer slip when invoices are created.</span></span>  
10. <span data-ttu-id="d053a-124">Velg mønsteret for regelmessighet.</span><span class="sxs-lookup"><span data-stu-id="d053a-124">Select the recurrence pattern.</span></span>
    * <span data-ttu-id="d053a-125">Daglig – Velg dette alternativet og angi antall dager i feltet Per.</span><span class="sxs-lookup"><span data-stu-id="d053a-125">Daily – Select this option and enter the number of days in the Per field.</span></span> <span data-ttu-id="d053a-126">Hvis du for eksempel angir 15, genereres en faktura hver 15. dag for denne kunden.</span><span class="sxs-lookup"><span data-stu-id="d053a-126">For example, if you enter 15, an invoice will be generated every 15 days for this customer.</span></span>  <span data-ttu-id="d053a-127">Ukentlig – Velg dette alternativet og angi antall uker i feltet Per.</span><span class="sxs-lookup"><span data-stu-id="d053a-127">Weekly - Select this option and enter the number of weeks in the Per field.</span></span> <span data-ttu-id="d053a-128">Hvis du for eksempel angir 2, genereres en faktura annenhver uke for denne kunden.</span><span class="sxs-lookup"><span data-stu-id="d053a-128">For example, if you enter 2, an invoice will be generated every two weeks for this customer.</span></span>  <span data-ttu-id="d053a-129">Månedlig – Velg dette alternativet og angi antall måneder i feltet Per.</span><span class="sxs-lookup"><span data-stu-id="d053a-129">Monthly - Select this option and enter the number of months in the Per field.</span></span> <span data-ttu-id="d053a-130">Hvis du for eksempel angir 6, genereres en faktura hver sjette måned for denne kunden.</span><span class="sxs-lookup"><span data-stu-id="d053a-130">For example, if you enter 6, an invoice will be generated every six months for this customer.</span></span>  <span data-ttu-id="d053a-131">Årlig – Velg dette alternativet og angi antall år i feltet Per.</span><span class="sxs-lookup"><span data-stu-id="d053a-131">Yearly – Select this option and enter the number of years in the Per field.</span></span> <span data-ttu-id="d053a-132">Hvis du for eksempel angir 2, genereres en faktura annethvert år for denne kunden.</span><span class="sxs-lookup"><span data-stu-id="d053a-132">For example, if you enter 2, an invoice will be generated every two years for this customer.</span></span>  
11. <span data-ttu-id="d053a-133">Angi et tall i feltet Per.</span><span class="sxs-lookup"><span data-stu-id="d053a-133">In the Per field, enter a number.</span></span>

