---
title: Arbeidsområde for leverandørsamarbeidsfakturering
description: Dette emnet forklarer hvordan du kan vise leverandørfakturaer og sende fakturaer fra arbeidsområdet for leverandørsamarbeidsfakturering.
author: abruer
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendInvoiceWorkspace
audience: Application User
ms.reviewer: roschlom
ms.custom: 221534
ms.assetid: c4ed62f3-d351-41d7-a2ad-790576cde4ab
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: ddb9d561e9785ee744c49d7fe03128102e77e9d3
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5248213"
---
# <a name="vendor-collaboration-invoicing-workspace"></a><span data-ttu-id="3756d-103">Arbeidsområde for leverandørsamarbeidsfakturering</span><span class="sxs-lookup"><span data-stu-id="3756d-103">Vendor collaboration invoicing workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3756d-104">Dette emnet forklarer hvordan du kan vise leverandørfakturaer og sende fakturaer fra arbeidsområdet for leverandørsamarbeidsfakturering.</span><span class="sxs-lookup"><span data-stu-id="3756d-104">This topic explains how you can view vendor invoices and submit invoices from the vendor collaboration invoicing workspace.</span></span>

<span data-ttu-id="3756d-105">Arbeidsområdet **Fakturering av leverandørsamarbeid** kan brukes til å vise informasjon om leverandør og sende fakturaer til systemet som bruker funksjonene for arbeidsflyt.</span><span class="sxs-lookup"><span data-stu-id="3756d-105">The **Vendor collaboration invoicing** workspace can be used to view vendor invoice information and to submit invoices to the system using workflow capabilities.</span></span>


<a name="vendor-collaboration-invoicing-workspace"></a><span data-ttu-id="3756d-106">Arbeidsområde for leverandørsamarbeidsfakturering</span><span class="sxs-lookup"><span data-stu-id="3756d-106">Vendor collaboration invoicing workspace</span></span>
----------------------------------------

### <a name="summary-tiles"></a><span data-ttu-id="3756d-107">Sammendrag-fliser</span><span class="sxs-lookup"><span data-stu-id="3756d-107">Summary tiles</span></span>

<span data-ttu-id="3756d-108">Flisene **Sammendrag** gir en oversikt over fakturaer for den valgte leverandøren.</span><span class="sxs-lookup"><span data-stu-id="3756d-108">The **Summary** tiles give an overview of the invoices for the selected vendor.</span></span> <span data-ttu-id="3756d-109">Du kan vise fakturaer etter deres tilstand.</span><span class="sxs-lookup"><span data-stu-id="3756d-109">You can view invoices by their state.</span></span>
-   <span data-ttu-id="3756d-110">Fakturautkast er ikke sendt til arbeidsflyten.</span><span class="sxs-lookup"><span data-stu-id="3756d-110">Draft invoices have not been submitted to workflow.</span></span>
-   <span data-ttu-id="3756d-111">Sendte, ikke-godkjente fakturaer er de fakturaene som leverandøren har sendt, men de ikke er postert i programmet.</span><span class="sxs-lookup"><span data-stu-id="3756d-111">Submitted, not approved invoices are those invoices that the vendor has submitted, but they have not been posted in the application.</span></span>
-   <span data-ttu-id="3756d-112">Godkjente, ikke-betalte fakturaer er de fakturaene som er postert, men som ikke er fullstendig betalte.</span><span class="sxs-lookup"><span data-stu-id="3756d-112">Approved, not paid invoices are those that have been posted, but they have not yet been fully paid.</span></span>
-   <span data-ttu-id="3756d-113">Betalte fakturaer er de som er fullstendig betalte i programmet.</span><span class="sxs-lookup"><span data-stu-id="3756d-113">Paid invoices are those that have been fully paid in the application.</span></span>

<span data-ttu-id="3756d-114">Ved å klikke en flis, vises det en filtrert visning av siden **Fakturaliste**.</span><span class="sxs-lookup"><span data-stu-id="3756d-114">Clicking on a tile will open a filtered view of the **Invoices list** page.</span></span>

### <a name="tabular-lists"></a><span data-ttu-id="3756d-115">Tabellister</span><span class="sxs-lookup"><span data-stu-id="3756d-115">Tabular lists</span></span>

<span data-ttu-id="3756d-116">I delen **Tabellister** er statusen for fakturering delt inn på samme måte som sammendragsflisene: Utkast og Sendt, men ikke godkjente lister.</span><span class="sxs-lookup"><span data-stu-id="3756d-116">In the **Tabular lists** section, the status of the invoicing is broken down in similar ways as the summary tiles: Draft and Submitted, not approved lists.</span></span> <span data-ttu-id="3756d-117">Når du er i kladdemodus, kan en faktura sendes til arbeidsflyten eller slettes.</span><span class="sxs-lookup"><span data-stu-id="3756d-117">While in the Draft state, an invoice can be submitted to workflow or deleted.</span></span> <span data-ttu-id="3756d-118">Den siste tabellisten er et alternativ for å finne fakturaer.</span><span class="sxs-lookup"><span data-stu-id="3756d-118">The last tabular list is an option to find invoices.</span></span> <span data-ttu-id="3756d-119">Du kan filtrere når du søker, slik at søk utføres raskere.</span><span class="sxs-lookup"><span data-stu-id="3756d-119">You can filter as you search, to allow for faster searches.</span></span>

### <a name="all-vendor-invoices-list-page"></a><span data-ttu-id="3756d-120">Side med liste over alle leverandørfakturaer</span><span class="sxs-lookup"><span data-stu-id="3756d-120">All vendor invoices list page</span></span>

<span data-ttu-id="3756d-121">Du kan vise alle posterte og uposterte leverandørfakturaer på listesiden **Leverandørsamarbeidsfakturaer**.</span><span class="sxs-lookup"><span data-stu-id="3756d-121">You can view all posted and unposted vendor invoices on the **Vendor collaboration invoices** list page.</span></span> <span data-ttu-id="3756d-122">Du kan bruke denne listesiden til å vise betalingsstatusen for fakturaene.</span><span class="sxs-lookup"><span data-stu-id="3756d-122">You can use this list page to view the payment status of the invoices.</span></span> <span data-ttu-id="3756d-123">Betalingsstatusene inkluderer Ikke-bokført, Ubetalt, Delvis betalt og Fullt betalt.</span><span class="sxs-lookup"><span data-stu-id="3756d-123">The payment statuses include Unposted, Unpaid, Partially paid, and Fully paid.</span></span>
<span data-ttu-id="3756d-124">Opprette en ny faktura fra en bestilling</span><span class="sxs-lookup"><span data-stu-id="3756d-124">Creating a new invoice from a purchase order</span></span>

<span data-ttu-id="3756d-125">Du kan opprette en ny leverandørfaktura ved å velge handlingen **Ny** i arbeidsområdet **Fakturering av leverandørsamarbeid**.</span><span class="sxs-lookup"><span data-stu-id="3756d-125">You can create a new vendor invoice by selecting the **New** action on the **Vendor collaboration invoicing** workspace.</span></span> <span data-ttu-id="3756d-126">Bestillingsnummeret og fakturanummeret må være oppgitt av leverandøren.</span><span class="sxs-lookup"><span data-stu-id="3756d-126">The purchase order number and invoice number must be provided by the vendor.</span></span> <span data-ttu-id="3756d-127">Som standard vises alle linjene fra leverandørens bestilling på den nye fakturaen.</span><span class="sxs-lookup"><span data-stu-id="3756d-127">By default, all of the lines from the vendor's purchase order will appear on the new invoice.</span></span> <span data-ttu-id="3756d-128">Informasjon om antall og kostnad kan redigeres før du sender leverandørfakturaen til arbeidsflyten.</span><span class="sxs-lookup"><span data-stu-id="3756d-128">The quantity and cost information can be edited prior to submitting the vendor invoice to workflow.</span></span> <span data-ttu-id="3756d-129">Du kan knytte filer, notater, bilder og URL-adresser til en faktura før de sendes.</span><span class="sxs-lookup"><span data-stu-id="3756d-129">You can attach files, notes, images, and URLs to an invoice before submitting it.</span></span>

<span data-ttu-id="3756d-130">Hvis du vil ha mer informasjon, kan du se [Leverandørsamarbeid med eksterne leverandører](../../supply-chain/procurement/vendor-collaboration-work-external-vendors.md)</span><span class="sxs-lookup"><span data-stu-id="3756d-130">For more information, see [Vendor collaboration with external vendors](../../supply-chain/procurement/vendor-collaboration-work-external-vendors.md)</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]