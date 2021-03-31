---
title: Oversikt over å løse avvik under kontroll for fakturatotaler
description: Du kan bruke kontroll av fakturatotaler som hjelp for å garantere at totale fakturabeløp ikke avviker fra forventede beløp med mer enn et godkjent avvik.
author: abruer
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTotalPriceTolerance
audience: Application User
ms.reviewer: roschlom
ms.custom: 63413
ms.assetid: 9ac42457-95b2-4191-ad06-c7e323704466
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0635f388dba16a1e4374f0915fbab5b88c3b76ab
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5227456"
---
# <a name="resolve-discrepancies-during-invoice-totals-matching-overview"></a><span data-ttu-id="d68b0-103">Oversikt over å løse avvik under kontroll for fakturatotaler</span><span class="sxs-lookup"><span data-stu-id="d68b0-103">Resolve discrepancies during invoice totals matching overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d68b0-104">Én type fakturakontrollvalidering er kontroll av fakturatotaler.</span><span class="sxs-lookup"><span data-stu-id="d68b0-104">One type of invoice matching validation is invoice totals matching.</span></span> <span data-ttu-id="d68b0-105">For å angi at systemet skal utføre kontroll av fakturatotaler går du til siden **Leverandørparametere**, kategorien **Fakturavalidering** og setter alternativet **Samsvar fakturatotaler** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="d68b0-105">To specify that the system should perform invoice totals matching, on the **Accounts payable parameters** page, on the **Invoice validation** tab, set the **Match invoice totals** option **Yes**.</span></span> 

<span data-ttu-id="d68b0-106">Du kan bruke kontroll av fakturatotaler som hjelp for å garantere at totale fakturabeløp ikke avviker fra forventede beløp med mer enn et godkjent avvik.</span><span class="sxs-lookup"><span data-stu-id="d68b0-106">You can use invoice totals matching to help guarantee that total invoice amounts don't deviate from expected amounts by more than an acceptable variance.</span></span> <span data-ttu-id="d68b0-107">Seks totaler sammenlignes på siden **Samsvarende detaljer for fakturatotaler**.</span><span class="sxs-lookup"><span data-stu-id="d68b0-107">Six totals are compared on the **Invoice totals matching details** page.</span></span> <span data-ttu-id="d68b0-108">Hvis noen av totalene avviker fra den forventede tilsvarende bestillingstotalen, flagges et samsvarsavvik.</span><span class="sxs-lookup"><span data-stu-id="d68b0-108">If any one of the totals deviates from the expected corresponding purchase order total, a matching discrepancy is flagged.</span></span> 

<span data-ttu-id="d68b0-109">For å se gjennom fakturaen med totalsamsvarsavvik går du til arbeidsområdet **Leverandørfakturaregistrering** og klikker flisen **Ventende fakturaer**.</span><span class="sxs-lookup"><span data-stu-id="d68b0-109">To review the invoice that has the totals matching discrepancies, in the **Vendor invoice entry** workspace, click the **Pending invoices** tile.</span></span> <span data-ttu-id="d68b0-110">Gå deretter til handlingsruten, velg kategorien **Gjennomgang**, og klikk **Samsvarende detaljer**.</span><span class="sxs-lookup"><span data-stu-id="d68b0-110">Then, on the Action Pane, on the **Review** tab, click **Matching details**.</span></span> <span data-ttu-id="d68b0-111">Hvis samsvarsavvik er oppdaget, vises advarselsikoner ved siden av fakturabeløpet.</span><span class="sxs-lookup"><span data-stu-id="d68b0-111">If matching discrepancies have been detected, warning icons appear next to the invoice amount.</span></span> <span data-ttu-id="d68b0-112">Du kan vise mer detaljert informasjon om totalene ved å vise samsvarende detaljer for fakturatotaler.</span><span class="sxs-lookup"><span data-stu-id="d68b0-112">You can view more detail about the totals by viewing the invoice totals matching details.</span></span> 

<span data-ttu-id="d68b0-113">Når du identifiserer et avvik, kan du det hende du må kontakte leverandøren hvis mener at informasjon i fakturaen er feil.</span><span class="sxs-lookup"><span data-stu-id="d68b0-113">After you identify a discrepancy, you might have to contact the vendor if you think that the information on the invoice is incorrect.</span></span> <span data-ttu-id="d68b0-114">Avhengig av den resulterende avtalen med leverandøren kan du deretter gjøre ett av følgende:</span><span class="sxs-lookup"><span data-stu-id="d68b0-114">Depending on the resulting agreement with the vendor, you can then take one of these actions:</span></span>

-   <span data-ttu-id="d68b0-115">Godta prisavviket og postere fakturaen som har samsvarende avvik.</span><span class="sxs-lookup"><span data-stu-id="d68b0-115">Accept the price difference, and post the invoice that has matching discrepancies.</span></span> <span data-ttu-id="d68b0-116">Systemet kan være konfigurert til å kreve godkjenning før det kan postere hvis det finnes samsvarende avvik.</span><span class="sxs-lookup"><span data-stu-id="d68b0-116">Your system might be set up to require approval before it can post if there are matching discrepancies.</span></span> <span data-ttu-id="d68b0-117">I så fall må du godkjenne det samsvarende avviket og du kan eventuelt skrive inn en merknad om godkjenning.</span><span class="sxs-lookup"><span data-stu-id="d68b0-117">In this case, you must approve the matching discrepancy and can optionally enter an approval comment.</span></span> <span data-ttu-id="d68b0-118">Du kan deretter velge å postere fakturaen.</span><span class="sxs-lookup"><span data-stu-id="d68b0-118">You can then select to post the invoice.</span></span>
-   <span data-ttu-id="d68b0-119">Korriger fakturabeløpet til det forventede beløpet og poster fakturaen.</span><span class="sxs-lookup"><span data-stu-id="d68b0-119">Revise the invoice amount to the expected amount, and post the invoice.</span></span>
-   <span data-ttu-id="d68b0-120">Be om at leverandøren krediterer hele beløpet og gir deg en ny, korrigert faktura.</span><span class="sxs-lookup"><span data-stu-id="d68b0-120">Request a full credit and a new, corrected invoice from the vendor.</span></span>

<span data-ttu-id="d68b0-121">Hvis du vil ha mer informasjon, se [Undersøke/løse unntak](tasks/research-resolve-exceptions.md).</span><span class="sxs-lookup"><span data-stu-id="d68b0-121">For more information, see [Research/Resolve exceptions](tasks/research-resolve-exceptions.md).</span></span>




[!INCLUDE[footer-include](../../includes/footer-banner.md)]