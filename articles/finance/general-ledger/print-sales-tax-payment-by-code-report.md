---
title: Skriv ut Mva-betaling etter kode-rapporten
description: Dette emnet inneholder informasjon om innstillingene og handlingene som kreves for å skrive ut mva-betaling etter kode-rapporten i regnskaps- eller avgiftskodevalutaen.
author: anasyash
ms.date: 05/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: anasyash
ms.search.validFrom: 2020-04-08
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: eb3ee4a12d2d29c2769f1ae22e11dc05608b47c1
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815458"
---
# <a name="print-the-sales-tax-payment-by-code-report"></a><span data-ttu-id="ecf98-103">Skriv ut Mva-betaling etter kode-rapporten</span><span class="sxs-lookup"><span data-stu-id="ecf98-103">Print the Sales tax payment by code report</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ecf98-104">For å skrive ut **Mva-betaling etter kode**-rapporten går du til **Avgift** \> **Forespørsler og rapporter** \> **Merverdiavgiftsrapporter** \> **Mva-betaling etter kode**.</span><span class="sxs-lookup"><span data-stu-id="ecf98-104">To print the **Sales tax payment by code** report, go to **Tax** \> **Inquiries and reports** \> **Sales tax reports** \> **Sales tax payment by code**.</span></span> <span data-ttu-id="ecf98-105">Som standard genereres rapportbeløp i regnskapsvalutaen til den juridiske enheten for alle rapporteringskoder som er definert på siden **Mva-rapporteringskoder**.</span><span class="sxs-lookup"><span data-stu-id="ecf98-105">By default, report amounts are generated in the accounting currency of the legal entity for all reporting codes that are set up on the **Sales tax reporting codes** page.</span></span>

<span data-ttu-id="ecf98-106">Du kan også generere denne rapporten slik at den viser betalingsbeløp for merverdiavgift i valutaene til mva-kodene for alle rapporteringskoder som er tilordnet mva-koder på siden **Mva-koder**.</span><span class="sxs-lookup"><span data-stu-id="ecf98-106">You can also generate this report so that it shows the sales tax payment amounts in the currencies of sales tax codes for all reporting codes that are assigned to sales tax codes on the **Sales tax codes** page.</span></span>

## <a name="turn-on-the-feature"></a><span data-ttu-id="ecf98-107">Aktivere funksjonen</span><span class="sxs-lookup"><span data-stu-id="ecf98-107">Turn on the feature</span></span>

<span data-ttu-id="ecf98-108">I arbeidsområdet **Funksjonsbehandling** aktiverer du følgende funksjon: **Generate Mva-betaling etter kode-rapporten i valutaen for mva-koden**.</span><span class="sxs-lookup"><span data-stu-id="ecf98-108">In the **Feature management** workspace, turn on the following feature: **Generate the Sales tax payment by code report in the sales tax code currency**.</span></span>

## <a name="run-the-report"></a><span data-ttu-id="ecf98-109">Kjøre rapporten</span><span class="sxs-lookup"><span data-stu-id="ecf98-109">Run the report</span></span>

1. <span data-ttu-id="ecf98-110">Gå til **Avgift** \> **Forespørsler og rapporter** \> **Merverdiavgiftsrapporter** \> **Mva-betaling etter rapporteringskode**.</span><span class="sxs-lookup"><span data-stu-id="ecf98-110">Go to **Tax** \> **Inquiries and reports** \> **Sales tax reports** \> **Sales tax payment by code**.</span></span>
2. <span data-ttu-id="ecf98-111">I feltet **Rapportvaluta** velger du en av følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="ecf98-111">In the **Report currency** field, select one of the following values:</span></span>

    - <span data-ttu-id="ecf98-112">**Regnskapsvaluta** – Skriv ut rapportbeløpene i regnskapsvalutaen.</span><span class="sxs-lookup"><span data-stu-id="ecf98-112">**Accounting currency** – Print the report amounts in the accounting currency.</span></span>
    - <span data-ttu-id="ecf98-113">**Valuta for mva-kode** – Skriv ut rapportbeløpene i valutaene for mva-kodene.</span><span class="sxs-lookup"><span data-stu-id="ecf98-113">**Sales tax code currency** – Print the report amounts in the currencies of sales tax codes.</span></span>

    ![Dialogboksen Mva-betaling etter kode](media/Sales-tax-payment-by-code.png)

<span data-ttu-id="ecf98-115">Illustrasjonen nedenfor viser et eksempel på rapporten som genereres.</span><span class="sxs-lookup"><span data-stu-id="ecf98-115">The following illustration shows an example of the report that is generated.</span></span> <span data-ttu-id="ecf98-116">Rapporten viser at rapporteringskoden **101** har **EUR**-valutaen hvis feltet **Mva-valuta** er satt til **EUR** for mva-koden som rapporteringskoden er tilordnet til.</span><span class="sxs-lookup"><span data-stu-id="ecf98-116">The report shows that reporting code **101** has the **EUR** currency if the **Sales tax currency** field is set to **EUR** for the sales tax code that the reporting code is assigned to.</span></span>

![Eksempel på Mva-betaling etter kode-rapporten](media/Sales-tax-payment-by-code-2.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]