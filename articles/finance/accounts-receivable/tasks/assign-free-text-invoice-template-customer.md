---
title: Tilordne en mal for fritekstfaktura til en kunde
description: Denne oppgaven beskriver hvordan du tilordner en mal for fritekstfaktura til en kunde.
author: ShivamPandey-msft
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustTable, CustRecurrenceInvoice
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0219521867d1cfb1fa4edcdf20dd70eea8a3d0e1
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5819896"
---
# <a name="assign-a-free-text-invoice-template-to-a-customer"></a><span data-ttu-id="80b23-103">Tilordne en mal for fritekstfaktura til en kunde</span><span class="sxs-lookup"><span data-stu-id="80b23-103">Assign a free text invoice template to a customer</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="80b23-104">Denne oppgaven beskriver hvordan du tilordner en mal for fritekstfaktura til en kunde.</span><span class="sxs-lookup"><span data-stu-id="80b23-104">This task demonstrates how to assign a free text invoice template to a customer.</span></span> <span data-ttu-id="80b23-105">Denne oppgaven bruker USMF-demofirmaet og er ment for brukeren som er ansvarlig for administrasjon og behandling av fakturaer for kunder.</span><span class="sxs-lookup"><span data-stu-id="80b23-105">This task uses the USMF demo company and is intended for the user who is responsible for managing and processing A/R invoices.</span></span>

1. <span data-ttu-id="80b23-106">I **navigasjonsruten** går du **Moduler > Kunder > Kunder > Alle kunder**.</span><span class="sxs-lookup"><span data-stu-id="80b23-106">In the **Navigation pane**, go to **Modules > Accounts receivable > Customers > All customers**.</span></span>
2. <span data-ttu-id="80b23-107">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="80b23-107">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="80b23-108">Klikk **Faktura** i **handlingsruten**.</span><span class="sxs-lookup"><span data-stu-id="80b23-108">On the **Action Pane**, click **Invoice**.</span></span>
4. <span data-ttu-id="80b23-109">Klikk **Gjentakende fakturalinjer**.</span><span class="sxs-lookup"><span data-stu-id="80b23-109">Click **Recurring invoices**.</span></span> <span data-ttu-id="80b23-110">Bruk denne siden til å tilordne mallinjer for fritekstfaktura til kunder og angi hvor ofte fakturaer skal sendes til kunden.</span><span class="sxs-lookup"><span data-stu-id="80b23-110">Use this page to assign free text invoice templates to customers and specify how frequently invoices will be sent to the customer.</span></span>  
5. <span data-ttu-id="80b23-111">Klikk **Ny** for å tilordne en ny mal til kunden.</span><span class="sxs-lookup"><span data-stu-id="80b23-111">Click **New** to assign a new template to the customer.</span></span>
6. <span data-ttu-id="80b23-112">I **Mal**-feltet velger du malen for fritekstfaktura du vil tilordne til kunden.</span><span class="sxs-lookup"><span data-stu-id="80b23-112">In the **Template** field, select the free text invoice template you want to assign to the customer.</span></span>
7. <span data-ttu-id="80b23-113">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="80b23-113">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="80b23-114">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="80b23-114">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="80b23-115">I feltet **Startdato for fakturering** angir du datoen for når den første fakturaen skal genereres.</span><span class="sxs-lookup"><span data-stu-id="80b23-115">In the **Billing start date** field, enter the date when the first invoice will be generated.</span></span>
10. <span data-ttu-id="80b23-116">Angi en gjentakende sluttdato i delen **Gjentakende slutt**.</span><span class="sxs-lookup"><span data-stu-id="80b23-116">In the **Recurrence end** section, enter a recurring end date.</span></span>  
    * <span data-ttu-id="80b23-117">Velg ett av følgende: Ingen sluttdato – fakturaer genereres helt til malen blir fjernet fra kundekontoen.</span><span class="sxs-lookup"><span data-stu-id="80b23-117">Select one of the following: No end date – Invoices will be generated indefinitely until the template is removed from the customer account.</span></span>
    * <span data-ttu-id="80b23-118">Sluttdato for fakturering – velg dette alternativet og angi den siste datoen som fakturaen kan genereres på.</span><span class="sxs-lookup"><span data-stu-id="80b23-118">Billing end date – Select this option and enter the last date that the invoice can be generated.</span></span>  
11. <span data-ttu-id="80b23-119">I feltet **Maksimalt akkumulert beløp** angir du det maksimale akkumulerte beløpet for avslutning av fakturagenerering.</span><span class="sxs-lookup"><span data-stu-id="80b23-119">In the **Maximum cumulative amount** field, enter the maximum cumulative amount after which invoice generation will stop.</span></span> <span data-ttu-id="80b23-120">Angi det maksimale akkumulerte beløpet som kan nås ved hjelp av den valgte malen.</span><span class="sxs-lookup"><span data-stu-id="80b23-120">Enter the maximum cumulative amount that can be reached using the selected template.</span></span> <span data-ttu-id="80b23-121">Hvis du for eksempel angir 1 000,00 og genererer månedlige fakturaer for 100,00 hver, stopper genereringen av fakturaer når den tiende fakturaen er generert.</span><span class="sxs-lookup"><span data-stu-id="80b23-121">For example, if you enter 1,000.00 and generate monthly invoices for 100.00 each, invoices will stop generating after the tenth invoice is generated.</span></span>  
12. <span data-ttu-id="80b23-122">I delen **Generer gjentakende fakturaer ved å bruke standardverdiene** velger du kundekontoen eller malen for fritekstfaktura.</span><span class="sxs-lookup"><span data-stu-id="80b23-122">In the **Generate recurring invoices by using the default values from** section, select either free text invoice template or the customer account.</span></span> <span data-ttu-id="80b23-123">Velg om du vil bruke malen for fritekstfaktura eller kundekontoen for å bestemme standardverdiene for språket, posteringsprofilen, merverdiavgiftsgruppen, merverdiavgiftgruppen for vare, listekoden, land/område for levering, valuta, betalingsbetingelser, betalingsmåten, betalingsspesifikasjoner, betalingsplanen, kontantrabatt, finansdimensjoner og girokort når fakturaer opprettes.</span><span class="sxs-lookup"><span data-stu-id="80b23-123">Select whether to use the free text invoice template or the customer account to determine the default values for the language, posting profile, sales tax group, item sales tax group, list code, country/region for delivery, currency, terms of payment, method of payment, payment specification, payment schedule, cash discount, financial dimensions, and giro money transfer slip when invoices are created.</span></span>  
13. <span data-ttu-id="80b23-124">Velg gjentakelsesmønsteret i feltet **Gjentakelsesmønster**.</span><span class="sxs-lookup"><span data-stu-id="80b23-124">In the **Recurrence pattern** field, select the recurrence pattern.</span></span>
    + <span data-ttu-id="80b23-125">Daglig – Velg dette alternativet og angi antall dager i feltet Per.</span><span class="sxs-lookup"><span data-stu-id="80b23-125">Daily – Select this option and enter the number of days in the Per field.</span></span> <span data-ttu-id="80b23-126">Hvis du for eksempel angir 15, genereres en faktura hver 15. dag for denne kunden.</span><span class="sxs-lookup"><span data-stu-id="80b23-126">For example, if you enter 15, an invoice will be generated every 15 days for this customer.</span></span>
    + <span data-ttu-id="80b23-127">Ukentlig – Velg dette alternativet og angi antall uker i feltet Per.</span><span class="sxs-lookup"><span data-stu-id="80b23-127">Weekly - Select this option and enter the number of weeks in the Per field.</span></span> <span data-ttu-id="80b23-128">Hvis du for eksempel angir 2, genereres en faktura annenhver uke for denne kunden.</span><span class="sxs-lookup"><span data-stu-id="80b23-128">For example, if you enter 2, an invoice will be generated every two weeks for this customer.</span></span>
    + <span data-ttu-id="80b23-129">Månedlig – Velg dette alternativet og angi antall måneder i feltet Per.</span><span class="sxs-lookup"><span data-stu-id="80b23-129">Monthly - Select this option and enter the number of months in the Per field.</span></span> <span data-ttu-id="80b23-130">Hvis du for eksempel angir 6, genereres en faktura hver sjette måned for denne kunden.</span><span class="sxs-lookup"><span data-stu-id="80b23-130">For example, if you enter 6, an invoice will be generated every six months for this customer.</span></span>
    + <span data-ttu-id="80b23-131">Årlig – Velg dette alternativet og angi antall år i feltet Per.</span><span class="sxs-lookup"><span data-stu-id="80b23-131">Yearly – Select this option and enter the number of years in the Per field.</span></span> <span data-ttu-id="80b23-132">Hvis du for eksempel angir 2, genereres en faktura annethvert år for denne kunden.</span><span class="sxs-lookup"><span data-stu-id="80b23-132">For example, if you enter 2, an invoice will be generated every two years for this customer.</span></span>  
14. <span data-ttu-id="80b23-133">Angi et tall i feltet **Per**.</span><span class="sxs-lookup"><span data-stu-id="80b23-133">In the **Per** field, enter a number.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]