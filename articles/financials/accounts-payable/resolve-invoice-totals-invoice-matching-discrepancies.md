---
title: Løse avvik under kontroll for fakturatotaler
description: Du kan bruke kontroll av fakturatotaler som hjelp for å garantere at totale fakturabeløp ikke avviker fra forventede beløp med mer enn et godkjent avvik.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 10/25/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTotalPriceTolerance
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 63413
ms.assetid: 9ac42457-95b2-4191-ad06-c7e323704466
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 67aa0b89eed1f82290659029dfcce92ca3710aea
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "331512"
---
# <a name="resolve-discrepancies-during-invoice-totals-matching"></a><span data-ttu-id="ff231-103">Løse avvik under kontroll for fakturatotaler</span><span class="sxs-lookup"><span data-stu-id="ff231-103">Resolve discrepancies during invoice totals matching</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ff231-104">Én type fakturakontrollvalidering er kontroll av fakturatotaler.</span><span class="sxs-lookup"><span data-stu-id="ff231-104">One type of invoice matching validation is invoice totals matching.</span></span> <span data-ttu-id="ff231-105">For å angi at systemet skal utføre kontroll av fakturatotaler går du til siden **Leverandørparametere**, kategorien **Fakturavalidering** og setter alternativet **Samsvar fakturatotaler** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="ff231-105">To specify that the system should perform invoice totals matching, on the **Accounts payable parameters** page, on the **Invoice validation** tab, set the **Match invoice totals** option **Yes**.</span></span> 

<span data-ttu-id="ff231-106">Du kan bruke kontroll av fakturatotaler som hjelp for å garantere at totale fakturabeløp ikke avviker fra forventede beløp med mer enn et godkjent avvik.</span><span class="sxs-lookup"><span data-stu-id="ff231-106">You can use invoice totals matching to help guarantee that total invoice amounts don't deviate from expected amounts by more than an acceptable variance.</span></span> <span data-ttu-id="ff231-107">Seks totaler sammenlignes på siden **Samsvarende detaljer for fakturatotaler**.</span><span class="sxs-lookup"><span data-stu-id="ff231-107">Six totals are compared on the **Invoice totals matching details** page.</span></span> <span data-ttu-id="ff231-108">Hvis noen av totalene avviker fra den forventede tilsvarende bestillingstotalen, flagges et samsvarsavvik.</span><span class="sxs-lookup"><span data-stu-id="ff231-108">If any one of the totals deviates from the expected corresponding purchase order total, a matching discrepancy is flagged.</span></span> 

<span data-ttu-id="ff231-109">For å se gjennom fakturaen med totalsamsvarsavvik går du til arbeidsområdet **Leverandørfakturaregistrering** og klikker flisen **Ventende fakturaer**.</span><span class="sxs-lookup"><span data-stu-id="ff231-109">To review the invoice that has the totals matching discrepancies, in the **Vendor invoice entry** workspace, click the **Pending invoices** tile.</span></span> <span data-ttu-id="ff231-110">Gå deretter til handlingsruten, velg kategorien **Gjennomgang**, og klikk **Samsvarende detaljer**.</span><span class="sxs-lookup"><span data-stu-id="ff231-110">Then, on the Action Pane, on the **Review** tab, click **Matching details**.</span></span> <span data-ttu-id="ff231-111">Hvis samsvarsavvik er oppdaget, vises advarselsikoner ved siden av fakturabeløpet.</span><span class="sxs-lookup"><span data-stu-id="ff231-111">If matching discrepancies have been detected, warning icons appear next to the invoice amount.</span></span> <span data-ttu-id="ff231-112">Du kan vise mer detaljert informasjon om totalene ved å vise samsvarende detaljer for fakturatotaler.</span><span class="sxs-lookup"><span data-stu-id="ff231-112">You can view more detail about the totals by viewing the invoice totals matching details.</span></span> 

<span data-ttu-id="ff231-113">Når du identifiserer et avvik, kan du det hende du må kontakte leverandøren hvis mener at informasjon i fakturaen er feil.</span><span class="sxs-lookup"><span data-stu-id="ff231-113">After you identify a discrepancy, you might have to contact the vendor if you think that the information on the invoice is incorrect.</span></span> <span data-ttu-id="ff231-114">Avhengig av den resulterende avtalen med leverandøren kan du deretter gjøre ett av følgende:</span><span class="sxs-lookup"><span data-stu-id="ff231-114">Depending on the resulting agreement with the vendor, you can then take one of these actions:</span></span>

-   <span data-ttu-id="ff231-115">Godta prisavviket og postere fakturaen som har samsvarende avvik.</span><span class="sxs-lookup"><span data-stu-id="ff231-115">Accept the price difference, and post the invoice that has matching discrepancies.</span></span> <span data-ttu-id="ff231-116">Systemet kan være konfigurert til å kreve godkjenning før det kan postere hvis det finnes samsvarende avvik.</span><span class="sxs-lookup"><span data-stu-id="ff231-116">Your system might be set up to require approval before it can post if there are matching discrepancies.</span></span> <span data-ttu-id="ff231-117">I så fall må du godkjenne det samsvarende avviket og du kan eventuelt skrive inn en merknad om godkjenning.</span><span class="sxs-lookup"><span data-stu-id="ff231-117">In this case, you must approve the matching discrepancy and can optionally enter an approval comment.</span></span> <span data-ttu-id="ff231-118">Du kan deretter velge å postere fakturaen.</span><span class="sxs-lookup"><span data-stu-id="ff231-118">You can then select to post the invoice.</span></span>
-   <span data-ttu-id="ff231-119">Korriger fakturabeløpet til det forventede beløpet og poster fakturaen.</span><span class="sxs-lookup"><span data-stu-id="ff231-119">Revise the invoice amount to the expected amount, and post the invoice.</span></span>
-   <span data-ttu-id="ff231-120">Be om at leverandøren krediterer hele beløpet og gir deg en ny, korrigert faktura.</span><span class="sxs-lookup"><span data-stu-id="ff231-120">Request a full credit and a new, corrected invoice from the vendor.</span></span>

<span data-ttu-id="ff231-121">Hvis du vil ha mer informasjon, se [Undersøke eller løse unntak](tasks/research-resolve-exceptions.md).</span><span class="sxs-lookup"><span data-stu-id="ff231-121">For more information, see [Research or resolve exceptions](tasks/research-resolve-exceptions.md).</span></span>


