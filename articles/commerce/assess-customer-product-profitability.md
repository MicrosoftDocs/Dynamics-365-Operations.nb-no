---
title: Vurdere kunde- og produktlønnsomhet
description: Denne artikkelen forklarer hvordan du kan bruke analyse i minnet og i sanntid til å få tilgang til, utforske og få oversikt over kunder og produkt fortjeneste fra data i Dynamics 365 Commerce.
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
ms.openlocfilehash: 3218a29995791ce0d9a42d5b6d898d6e548f0f1d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4414621"
---
# <a name="assess-customer-and-product-profitability"></a><span data-ttu-id="b947f-103">Vurdere kunde- og produktlønnsomhet</span><span class="sxs-lookup"><span data-stu-id="b947f-103">Assess customer and product profitability</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b947f-104">Denne artikkelen forklarer hvordan du kan bruke analyse i minnet og i sanntid til å få tilgang til, utforske og få oversikt over kunder og produkt fortjeneste fra data i Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b947f-104">This article explains how you can use the in-memory and real-time analytics to access, explore, and gain insight about customers and product profitability from your Dynamics 365 Commerce data.</span></span>

<span data-ttu-id="b947f-105">Som en del av Commerce kan brukere lese om lønnsomhet til de viktigste kundene (10 til 100) på tvers av forskjellige nivåer av organisasjonshierarkiet, basert på ett av følgende kriterier:</span><span class="sxs-lookup"><span data-stu-id="b947f-105">As part of Commerce, users can study profitability for the top customers (10 to 100) across different levels of the organization hierarchy, based on one of the following criteria:</span></span>

- <span data-ttu-id="b947f-106">Salgsbeløp</span><span class="sxs-lookup"><span data-stu-id="b947f-106">Sales amount</span></span>
- <span data-ttu-id="b947f-107">Antall</span><span class="sxs-lookup"><span data-stu-id="b947f-107">Quantity</span></span>
- <span data-ttu-id="b947f-108">Bruttofortjenestemargin</span><span class="sxs-lookup"><span data-stu-id="b947f-108">Gross profit margin</span></span>
- <span data-ttu-id="b947f-109">Marginprosent</span><span class="sxs-lookup"><span data-stu-id="b947f-109">Margin percentage</span></span>

<span data-ttu-id="b947f-110">For denne vurderingen kan du bruke den medfølgende rapporten **Toppkunder**, som du kan åpne fra følgende plasseringer:</span><span class="sxs-lookup"><span data-stu-id="b947f-110">For this assessment, you can use the out-of-box **Top customers** report, which you can open from any of the following locations:</span></span>

- <span data-ttu-id="b947f-111">Arbeidsområdet **Butikkadministrasjon** &gt; **Retail og Commerce** &gt; **Kanaler** &gt; **Butikkadministrasjon** &gt; **Rapporter** &gt; **Rapport for beste kunder**</span><span class="sxs-lookup"><span data-stu-id="b947f-111">**Store management** workspace &gt; **Retail and Commerce** &gt; **Channels** &gt; **Store management** &gt; **Reports** &gt; **Top customers report**</span></span>
- <span data-ttu-id="b947f-112">Delen **Forespørsler og rapporter** &gt; **Retail og Commerce** &gt; **Forespørsler og rapporter** &gt; **Salgsrapporter** &gt; **Rapport for beste kunder**</span><span class="sxs-lookup"><span data-stu-id="b947f-112">**Inquiries and reports** section &gt; **Retail and Commerce** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Top customers report**</span></span>

<span data-ttu-id="b947f-113">På samme måte kan brukere lese om lønnsomhet til de viktigste produktene (10 til 100) på tvers av forskjellige nivåer av organisasjonshierarkiet, basert på ett av følgende kriterier:</span><span class="sxs-lookup"><span data-stu-id="b947f-113">Likewise, users can study profitability for the top products (10 to 100) across different levels of the organization hierarchy, based on one of the following criteria:</span></span>

- <span data-ttu-id="b947f-114">Salgsbeløp</span><span class="sxs-lookup"><span data-stu-id="b947f-114">Sales amount</span></span>
- <span data-ttu-id="b947f-115">Antall</span><span class="sxs-lookup"><span data-stu-id="b947f-115">Quantity</span></span>
- <span data-ttu-id="b947f-116">Bruttofortjenestemargin</span><span class="sxs-lookup"><span data-stu-id="b947f-116">Gross profit margin</span></span>
- <span data-ttu-id="b947f-117">Marginprosent</span><span class="sxs-lookup"><span data-stu-id="b947f-117">Margin percentage</span></span>

<span data-ttu-id="b947f-118">For denne vurderingen kan du bruke den medfølgende rapporten **Topprodukter**, som du kan åpne fra følgende plasseringer:</span><span class="sxs-lookup"><span data-stu-id="b947f-118">For this assessment, you can use the out-of-box **Top products** report, which you can open from any of the following locations:</span></span>

- <span data-ttu-id="b947f-119">Arbeidsområdet **Butikkadministrasjon** &gt; **Retail og Commerce** &gt; **Kanaler** &gt; **Butikkadministrasjon** &gt; **Rapporter** &gt; **Rapport om topprodukter**</span><span class="sxs-lookup"><span data-stu-id="b947f-119">**Store management** workspace &gt; **Retail and Commerce** &gt; **Channels** &gt; **Store management** &gt; **Reports** &gt; **Top products report**</span></span>
- <span data-ttu-id="b947f-120">Arbeidsområdet **Kategori- og produktstyring** &gt; **Retail og Commerce** &gt; **Produkter og kategorier** &gt; **Butikkadministrasjon** &gt; **Rapporter** &gt; **Rapport om topprodukter**</span><span class="sxs-lookup"><span data-stu-id="b947f-120">**Category and product management** workspace &gt; **Retail and Commerce** &gt; **Products and categories** &gt; **Store management** &gt; **Reports** &gt; **Top products report**</span></span>
- <span data-ttu-id="b947f-121">Delen **Forespørsler og rapporter** &gt; **Retail og Commerce** &gt; **Forespørsler og rapporter** &gt; **Salgsrapporter** &gt; **Rapport om topprodukter**</span><span class="sxs-lookup"><span data-stu-id="b947f-121">**Inquiries and reports** section &gt; **Retail and Commerce** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Top products report**</span></span>
