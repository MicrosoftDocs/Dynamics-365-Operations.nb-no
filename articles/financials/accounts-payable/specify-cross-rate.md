---
title: Angi krysskurs
description: Dette emnet gir informasjon om krysskurs i Microsoft Dynamics 365 for Finance and Operations.
author: abruer
manager: AnnBe
ms.date: 05/16/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f9c2cba3ed655e2b4b1ada75bdbb5f01c300b25a
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/01/2019
ms.locfileid: "1834541"
---
# <a name="specify-the-cross-rate"></a><span data-ttu-id="41b1b-103">Angi krysskurs</span><span class="sxs-lookup"><span data-stu-id="41b1b-103">Specify the cross rate</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="41b1b-104">Dette emnet forklarer formålet med en kryssats, og hvordan du spesifiserer kryssatsen når du utligner en betaling med en faktura.</span><span class="sxs-lookup"><span data-stu-id="41b1b-104">This topic explains the purpose of a cross rate, and how to specify the cross rate when you settle a payment with an invoice.</span></span> <span data-ttu-id="41b1b-105">Bruk en kryssats når alle kriteriene nedenfor gjelder:</span><span class="sxs-lookup"><span data-stu-id="41b1b-105">Use a cross rate when all of the following criteria apply:</span></span> 
-   <span data-ttu-id="41b1b-106">Du utligner en betaling med en faktura.</span><span class="sxs-lookup"><span data-stu-id="41b1b-106">You are settling a payment with an invoice.</span></span> 
-   <span data-ttu-id="41b1b-107">Betalingslinjen og fakturalinjen bruker forskjellige valutaer.</span><span class="sxs-lookup"><span data-stu-id="41b1b-107">The payment line and the invoice line use different currencies.</span></span> 
-   <span data-ttu-id="41b1b-108">Ingen valuta er regnskapsvalutaen.</span><span class="sxs-lookup"><span data-stu-id="41b1b-108">Neither currency is the accounting currency.</span></span> 

<span data-ttu-id="41b1b-109">Krysskursen brukes ikke til å beregne valutaomveksling for betalingstransaksjon til betalingsregnskapsvalutaen.</span><span class="sxs-lookup"><span data-stu-id="41b1b-109">The cross rate is not used to calculate the payment transaction currency translation to the payment accounting currency.</span></span> <span data-ttu-id="41b1b-110">Valutakursene fra valutakurstabellene hentes i stedet for å beregne verdien av valutabeløpet for betalingstransaksjonen og valutabeløpet for betalingsregnskapet.</span><span class="sxs-lookup"><span data-stu-id="41b1b-110">Instead, the exchange rates from the exchange rate tables are retrieved to calculate the value of the payment transaction currency amount and the payment accounting currency amount.</span></span> 

<span data-ttu-id="41b1b-111">Regnskapsvalutaen er for eksempel USD, fakturavalutaen er CAD og betalingsvalutaen er EUR.</span><span class="sxs-lookup"><span data-stu-id="41b1b-111">For example, the accounting currency is USD, the invoice currency is CAD, and the payment currency is EUR.</span></span> <span data-ttu-id="41b1b-112">Med kryssatsen kan du angi en valutakurs for å konvertere direkte mellom CAD og EUR, og ikke måtte konvertere gjennom USD.</span><span class="sxs-lookup"><span data-stu-id="41b1b-112">The cross rate lets you enter an exchange rate to translate directly between CAD and EUR, and not have to translate through USD.</span></span> <span data-ttu-id="41b1b-113">Når du velger en faktura og en hovedbetaling, kan du angi en kryssats for fakturalinjen.</span><span class="sxs-lookup"><span data-stu-id="41b1b-113">When you select an invoice and a primary payment, you can enter a cross rate for the invoice line.</span></span> <span data-ttu-id="41b1b-114">Kryssatsen er valutakursen mellom valutaene for disse transaksjonene på utligningsdatoen.</span><span class="sxs-lookup"><span data-stu-id="41b1b-114">The cross rate is the exchange rate between the currencies for those transactions, as of the settlement date.</span></span>

1.  <span data-ttu-id="41b1b-115">Gå til én av følgende sider:</span><span class="sxs-lookup"><span data-stu-id="41b1b-115">Go to one of the following pages:</span></span>
- <span data-ttu-id="41b1b-116">**Kunder > Felles > Kunder > Alle kunder**</span><span class="sxs-lookup"><span data-stu-id="41b1b-116">**Accounts receivable > Common > Customers > All customers**</span></span> 
- <span data-ttu-id="41b1b-117">**Leverandører > Felles > Leverandører > Alle leverandører**</span><span class="sxs-lookup"><span data-stu-id="41b1b-117">**Accounts payable > Common > Vendors > All vendors**</span></span> 
- <span data-ttu-id="41b1b-118">**Innkjøp og leverandører > Felles > Leverandører > Alle leverandører**</span><span class="sxs-lookup"><span data-stu-id="41b1b-118">**Procurement and sourcing > Common > Vendors > All vendors**</span></span>
2.  <span data-ttu-id="41b1b-119">Velg kunden eller leverandøren som du utligner åpne transaksjoner for.</span><span class="sxs-lookup"><span data-stu-id="41b1b-119">Select the customer or vendor whose open transactions you are settling.</span></span> 
3.  <span data-ttu-id="41b1b-120">For en kunde, på **Alle kunder**-listesiden gå til **Samle inn > Utlign åpne transaksjoner**.</span><span class="sxs-lookup"><span data-stu-id="41b1b-120">For a customer, on the **All customers** list page, go to **Collect > Settle open transactions**.</span></span> <span data-ttu-id="41b1b-121">For en leverandør, på **Alle leverandører**-listesiden gå til **Faktura > Utlign åpne transaksjoner**.</span><span class="sxs-lookup"><span data-stu-id="41b1b-121">For a vendor, on the **All vendors** list page, go to **Invoice > Settle open transactions**.</span></span> 
4.  <span data-ttu-id="41b1b-122">Velg transaksjonen som er hovedbetalingen, og klikk deretter på **Merk betaling**.</span><span class="sxs-lookup"><span data-stu-id="41b1b-122">Select the transaction that is the primary payment, and then click **Mark payment**.</span></span> <span data-ttu-id="41b1b-123">Avmerkingsboksen i **Merk**-kolonnen er valgt, og det vises et informasjonsikon i **Primærbetaling**-kolonnen.</span><span class="sxs-lookup"><span data-stu-id="41b1b-123">The check box in the **Mark** column is selected, and an information icon is shown in the **Primary payment** column.</span></span> 
5.  <span data-ttu-id="41b1b-124">I **Kryssats**-feltet kan du angi valutakursen mellom fakturavalutaen og betalingsvalutaen som gjelder på utligningsdatoen.</span><span class="sxs-lookup"><span data-stu-id="41b1b-124">In the **Cross rate** field, enter the exchange rate between the invoice currency and the payment currency, as of the settlement date.</span></span> 
