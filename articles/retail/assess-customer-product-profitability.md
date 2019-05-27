---
title: Vurdere kunde- og produktlønnsomhet
description: Denne artikkelen forklarer hvordan du kan bruke analyse i minnet og i sanntid til å få tilgang til, utforske og få oversikt over kunder og produkt fortjeneste fra data i Microsoft Dynamics 365 for Retail.
author: ashishmsft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: SysOperationsTemplateForm, RetailStoreManagementWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 52902
ms.assetid: 1a77d04b-2985-4bee-9138-c216fe0483de
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 28d4eeaa3fcae33f817690ad496b4b123a5838ce
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1561370"
---
# <a name="assess-customer-and-product-profitability"></a><span data-ttu-id="23a04-103">Vurdere kunde- og produktlønnsomhet</span><span class="sxs-lookup"><span data-stu-id="23a04-103">Assess customer and product profitability</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="23a04-104">Denne artikkelen forklarer hvordan du kan bruke analyse i minnet og i sanntid til å få tilgang til, utforske og få oversikt over kunder og produkt fortjeneste fra data i Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="23a04-104">This article explains how you can use the in-memory and real-time analytics to access, explore, and gain insight about customers and product profitability from your Microsoft Dynamics 365 for Retail data.</span></span>

<span data-ttu-id="23a04-105">Som en del av Dynamics 365 for Retail, kan brukere lese om lønnsomhet til de viktigste kundene (10 til 100) på tvers av forskjellige nivåer av organisasjonshierarkiet, basert på ett av følgende kriterier:</span><span class="sxs-lookup"><span data-stu-id="23a04-105">As part of Dynamics 365 for Retail, users can study profitability for the top customers (10 to 100) across different levels of the organization hierarchy, based on one of the following criteria:</span></span>

- <span data-ttu-id="23a04-106">Salgsbeløp</span><span class="sxs-lookup"><span data-stu-id="23a04-106">Sales amount</span></span>
- <span data-ttu-id="23a04-107">Antall</span><span class="sxs-lookup"><span data-stu-id="23a04-107">Quantity</span></span>
- <span data-ttu-id="23a04-108">Bruttofortjenestemargin</span><span class="sxs-lookup"><span data-stu-id="23a04-108">Gross profit margin</span></span>
- <span data-ttu-id="23a04-109">Marginprosent</span><span class="sxs-lookup"><span data-stu-id="23a04-109">Margin percentage</span></span>

<span data-ttu-id="23a04-110">For denne vurderingen kan du bruke den medfølgende rapporten **Toppkunder**, som du kan åpne fra følgende plasseringer:</span><span class="sxs-lookup"><span data-stu-id="23a04-110">For this assessment, you can use the out-of-box **Top customers** report, which you can open from any of the following locations:</span></span>

- <span data-ttu-id="23a04-111">Arbeidsområdet **Administrasjon av detaljhandelsbutikk** &gt; **Detaljhandel** &gt; **Kanaler** &gt; **Administrasjon av detaljhandelsbutikk** &gt; **Rapporter** &gt; **Rapport for beste kunder**</span><span class="sxs-lookup"><span data-stu-id="23a04-111">**Retail store management** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store management** &gt; **Reports** &gt; **Top customers report**</span></span>
- <span data-ttu-id="23a04-112">Delen **Forespørsler og rapporter** &gt; **Detaljhandel** &gt; **Forespørsler og rapporter** &gt; **Salgsrapporter** &gt; **Rapport for beste kunder**</span><span class="sxs-lookup"><span data-stu-id="23a04-112">**Inquiries and reports** section &gt; **Retail** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Top customers report**</span></span>

<span data-ttu-id="23a04-113">På samme måte kan brukere lese om lønnsomhet til de viktigste produktene (10 til 100) på tvers av forskjellige nivåer av organisasjonshierarkiet, basert på ett av følgende kriterier:</span><span class="sxs-lookup"><span data-stu-id="23a04-113">Likewise, users can study profitability for the top products (10 to 100) across different levels of the organization hierarchy, based on one of the following criteria:</span></span>

- <span data-ttu-id="23a04-114">Salgsbeløp</span><span class="sxs-lookup"><span data-stu-id="23a04-114">Sales amount</span></span>
- <span data-ttu-id="23a04-115">Antall</span><span class="sxs-lookup"><span data-stu-id="23a04-115">Quantity</span></span>
- <span data-ttu-id="23a04-116">Bruttofortjenestemargin</span><span class="sxs-lookup"><span data-stu-id="23a04-116">Gross profit margin</span></span>
- <span data-ttu-id="23a04-117">Marginprosent</span><span class="sxs-lookup"><span data-stu-id="23a04-117">Margin percentage</span></span>

<span data-ttu-id="23a04-118">For denne vurderingen kan du bruke den medfølgende rapporten **Topprodukter**, som du kan åpne fra følgende plasseringer:</span><span class="sxs-lookup"><span data-stu-id="23a04-118">For this assessment, you can use the out-of-box **Top products** report, which you can open from any of the following locations:</span></span>

- <span data-ttu-id="23a04-119">Arbeidsområdet **Administrasjon av detaljhandelsbutikk** &gt; **Detaljhandel** &gt; **Kanaler** &gt; **Administrasjon av detaljhandelsbutikk** &gt; **Rapporter** &gt; **Rapport om topprodukter**</span><span class="sxs-lookup"><span data-stu-id="23a04-119">**Retail store management** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store management** &gt; **Reports** &gt; **Top products report**</span></span>
- <span data-ttu-id="23a04-120">Arbeidsområdet **Kategori- og produktstyring** &gt; **Detaljhandel** &gt; **Produkter og kategorier** &gt; **Administrasjon av detaljhandelsbutikk** &gt; **Rapporter** &gt; **Rapport om topprodukter**</span><span class="sxs-lookup"><span data-stu-id="23a04-120">**Category and product management** workspace &gt; **Retail** &gt; **Products and categories** &gt; **Retail store management** &gt; **Reports** &gt; **Top products report**</span></span>
- <span data-ttu-id="23a04-121">Delen **Forespørsler og rapporter** &gt; **Detaljhandel** &gt; **Forespørsler og rapporter** &gt; **Salgsrapporter** &gt; **Rapport om topprodukter**</span><span class="sxs-lookup"><span data-stu-id="23a04-121">**Inquiries and reports** section &gt; **Retail** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Top products report**</span></span>
