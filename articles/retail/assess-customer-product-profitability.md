---
title: Vurdere kunde- og produktlønnsomhet
description: Denne artikkelen forklarer hvordan du kan bruke analyse i minnet og i sanntid til å få tilgang til, utforske og få oversikt over kunder og produkt fortjeneste fra data i Dynamics 365 Retail.
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
ms.openlocfilehash: 5a9bebf948bd4602556f70a5a79690621a03261e
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/24/2019
ms.locfileid: "2023596"
---
# <a name="assess-customer-and-product-profitability"></a><span data-ttu-id="a6e2b-103">Vurdere kunde- og produktlønnsomhet</span><span class="sxs-lookup"><span data-stu-id="a6e2b-103">Assess customer and product profitability</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a6e2b-104">Denne artikkelen forklarer hvordan du kan bruke analyse i minnet og i sanntid til å få tilgang til, utforske og få oversikt over kunder og produkt fortjeneste fra data i Dynamics 365 Retail.</span><span class="sxs-lookup"><span data-stu-id="a6e2b-104">This article explains how you can use the in-memory and real-time analytics to access, explore, and gain insight about customers and product profitability from your Dynamics 365 Retail data.</span></span>

<span data-ttu-id="a6e2b-105">Som en del av Retail kan brukere lese om lønnsomhet til de viktigste kundene (10 til 100) på tvers av forskjellige nivåer av organisasjonshierarkiet, basert på ett av følgende kriterier:</span><span class="sxs-lookup"><span data-stu-id="a6e2b-105">As part of Retail, users can study profitability for the top customers (10 to 100) across different levels of the organization hierarchy, based on one of the following criteria:</span></span>

- <span data-ttu-id="a6e2b-106">Salgsbeløp</span><span class="sxs-lookup"><span data-stu-id="a6e2b-106">Sales amount</span></span>
- <span data-ttu-id="a6e2b-107">Antall</span><span class="sxs-lookup"><span data-stu-id="a6e2b-107">Quantity</span></span>
- <span data-ttu-id="a6e2b-108">Bruttofortjenestemargin</span><span class="sxs-lookup"><span data-stu-id="a6e2b-108">Gross profit margin</span></span>
- <span data-ttu-id="a6e2b-109">Marginprosent</span><span class="sxs-lookup"><span data-stu-id="a6e2b-109">Margin percentage</span></span>

<span data-ttu-id="a6e2b-110">For denne vurderingen kan du bruke den medfølgende rapporten **Toppkunder**, som du kan åpne fra følgende plasseringer:</span><span class="sxs-lookup"><span data-stu-id="a6e2b-110">For this assessment, you can use the out-of-box **Top customers** report, which you can open from any of the following locations:</span></span>

- <span data-ttu-id="a6e2b-111">Arbeidsområdet **Administrasjon av detaljhandelsbutikk** &gt; **Detaljhandel** &gt; **Kanaler** &gt; **Administrasjon av detaljhandelsbutikk** &gt; **Rapporter** &gt; **Rapport for beste kunder**</span><span class="sxs-lookup"><span data-stu-id="a6e2b-111">**Retail store management** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store management** &gt; **Reports** &gt; **Top customers report**</span></span>
- <span data-ttu-id="a6e2b-112">Delen **Forespørsler og rapporter** &gt; **Detaljhandel** &gt; **Forespørsler og rapporter** &gt; **Salgsrapporter** &gt; **Rapport for beste kunder**</span><span class="sxs-lookup"><span data-stu-id="a6e2b-112">**Inquiries and reports** section &gt; **Retail** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Top customers report**</span></span>

<span data-ttu-id="a6e2b-113">På samme måte kan brukere lese om lønnsomhet til de viktigste produktene (10 til 100) på tvers av forskjellige nivåer av organisasjonshierarkiet, basert på ett av følgende kriterier:</span><span class="sxs-lookup"><span data-stu-id="a6e2b-113">Likewise, users can study profitability for the top products (10 to 100) across different levels of the organization hierarchy, based on one of the following criteria:</span></span>

- <span data-ttu-id="a6e2b-114">Salgsbeløp</span><span class="sxs-lookup"><span data-stu-id="a6e2b-114">Sales amount</span></span>
- <span data-ttu-id="a6e2b-115">Antall</span><span class="sxs-lookup"><span data-stu-id="a6e2b-115">Quantity</span></span>
- <span data-ttu-id="a6e2b-116">Bruttofortjenestemargin</span><span class="sxs-lookup"><span data-stu-id="a6e2b-116">Gross profit margin</span></span>
- <span data-ttu-id="a6e2b-117">Marginprosent</span><span class="sxs-lookup"><span data-stu-id="a6e2b-117">Margin percentage</span></span>

<span data-ttu-id="a6e2b-118">For denne vurderingen kan du bruke den medfølgende rapporten **Topprodukter**, som du kan åpne fra følgende plasseringer:</span><span class="sxs-lookup"><span data-stu-id="a6e2b-118">For this assessment, you can use the out-of-box **Top products** report, which you can open from any of the following locations:</span></span>

- <span data-ttu-id="a6e2b-119">Arbeidsområdet **Administrasjon av detaljhandelsbutikk** &gt; **Detaljhandel** &gt; **Kanaler** &gt; **Administrasjon av detaljhandelsbutikk** &gt; **Rapporter** &gt; **Rapport om topprodukter**</span><span class="sxs-lookup"><span data-stu-id="a6e2b-119">**Retail store management** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store management** &gt; **Reports** &gt; **Top products report**</span></span>
- <span data-ttu-id="a6e2b-120">Arbeidsområdet **Kategori- og produktstyring** &gt; **Detaljhandel** &gt; **Produkter og kategorier** &gt; **Administrasjon av detaljhandelsbutikk** &gt; **Rapporter** &gt; **Rapport om topprodukter**</span><span class="sxs-lookup"><span data-stu-id="a6e2b-120">**Category and product management** workspace &gt; **Retail** &gt; **Products and categories** &gt; **Retail store management** &gt; **Reports** &gt; **Top products report**</span></span>
- <span data-ttu-id="a6e2b-121">Delen **Forespørsler og rapporter** &gt; **Detaljhandel** &gt; **Forespørsler og rapporter** &gt; **Salgsrapporter** &gt; **Rapport om topprodukter**</span><span class="sxs-lookup"><span data-stu-id="a6e2b-121">**Inquiries and reports** section &gt; **Retail** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Top products report**</span></span>
