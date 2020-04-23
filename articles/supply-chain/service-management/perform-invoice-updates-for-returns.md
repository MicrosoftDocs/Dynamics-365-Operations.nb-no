---
title: Utføre fakturaoppdateringer for returer
description: Denne funksjonaliteten i støtter forretningsprosessene i organisasjoner som velger å fakturere returordrer og salgsordrer samtidig og utført av samme person.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ec803aaa2f750c43a1865c9536730b275e6ef1d4
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/02/2020
ms.locfileid: "3202151"
---
# <a name="perform-invoice-updates-for-returns"></a><span data-ttu-id="1663a-103">Utføre fakturaoppdateringer for returer</span><span class="sxs-lookup"><span data-stu-id="1663a-103">Perform invoice updates for returns</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="1663a-104">En returordre er en type salgsordre som er merket som en returordre.</span><span class="sxs-lookup"><span data-stu-id="1663a-104">A return order is a type of sales order that is marked as a returned order.</span></span> <span data-ttu-id="1663a-105">Derfor brukes listesiden **Alle salgsordrer** til å generere fakturaer for returordrer i stedet for skjemaet **Returordrer**.</span><span class="sxs-lookup"><span data-stu-id="1663a-105">Therefore, the **All sales orders** list page is used to generate invoices for return orders instead of the **Return orders** form.</span></span> <span data-ttu-id="1663a-106">Denne funksjonaliteten i støtter forretningsprosessene i organisasjoner som velger å fakturere returordrer og salgsordrer samtidig og utført av samme person.</span><span class="sxs-lookup"><span data-stu-id="1663a-106">This functionality supports the business processes of organizations that choose to have return orders and sales orders invoiced at the same time and by the same person.</span></span>

<span data-ttu-id="1663a-107">Fordi fakturaen for en returnert vare er for et negativt beløp, kalles en kreditnota.</span><span class="sxs-lookup"><span data-stu-id="1663a-107">Because the invoice for a returned item is for a negative amount, it is called a credit note.</span></span>

<span data-ttu-id="1663a-108">Når du setter opp fakturaoppdateringen for satsvis behandling, må salgsordren av typen **Returordre** ha returlinjestatusen **Mottatt**, som viser at ordrens følgeseddel er oppdatert.</span><span class="sxs-lookup"><span data-stu-id="1663a-108">When you set up the invoice update for batch processing, the sales order of type **Returned order** must have a return line status of **Received**, which indicates that the order's packing slip has been updated.</span></span>

## <a name="post-an-invoice-for-a-return-order"></a><span data-ttu-id="1663a-109">Postere en faktura for en returordre</span><span class="sxs-lookup"><span data-stu-id="1663a-109">Post an invoice for a return order</span></span>

1.  <span data-ttu-id="1663a-110">Klikk **Kunder** \> **Felles** \> **Salgsordrer** \> **Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="1663a-110">Click **Accounts receivable** \> **Common** \> **Sales orders** \> **All sales orders**.</span></span>

2.  <span data-ttu-id="1663a-111">Velg en salgsordre som **Returordre** vises for i **Ordretype**-feltet.</span><span class="sxs-lookup"><span data-stu-id="1663a-111">Select a sales order for which **Returned order** is displayed in the **Order type** field.</span></span>

3.  <span data-ttu-id="1663a-112">I handlingsruten, på **Faktura**-fanen i **Generer**-gruppen klikker du **Faktura**.</span><span class="sxs-lookup"><span data-stu-id="1663a-112">On the Action Pane, on the **Invoice** tab, in the **Generate** group, click **Invoice**.</span></span>

4.  <span data-ttu-id="1663a-113">På **Parametere**-fanen merker du av for **Postering**.</span><span class="sxs-lookup"><span data-stu-id="1663a-113">On the **Parameters** tab, select the **Posting** check box.</span></span>

5.  <span data-ttu-id="1663a-114">Gå gjennom informasjonen i skjemaet, og gjør eventuelle nødvendige endringer.</span><span class="sxs-lookup"><span data-stu-id="1663a-114">Review information in the form and make any changes that are needed.</span></span>

6.  <span data-ttu-id="1663a-115">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="1663a-115">Click **OK**.</span></span> <span data-ttu-id="1663a-116">Kreditnotaen er postert.</span><span class="sxs-lookup"><span data-stu-id="1663a-116">The credit note is posted.</span></span>

## <a name="see-also"></a><span data-ttu-id="1663a-117">Se også</span><span class="sxs-lookup"><span data-stu-id="1663a-117">See also</span></span>

[<span data-ttu-id="1663a-118">Følgesedddeloppdateringer for returer</span><span class="sxs-lookup"><span data-stu-id="1663a-118">Packing slip updates for returns</span></span>](packing-slip-updates-returns.md)

  


