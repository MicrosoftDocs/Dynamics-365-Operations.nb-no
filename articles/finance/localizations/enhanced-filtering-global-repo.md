---
title: Forbedret RCS-filtrering i RCS/det globale repositoriet
description: Dette emnet beskriver forbedrede filtreringsfunksjoner for det det globale repositoriet RCS som er forbedret for å inkludere tilleggsfiltrene.
author: JaneA07
manager: AnnBe
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 1913b661c46af5e34da1a2939cb2a5d5b4e46411
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4446271"
---
# <a name="rcs-enhanced-filtering-options-for-finding-configurations-in-the-rcsglobal-repository"></a><span data-ttu-id="9f039-103">Forbedrede RCS-filtreringsalternativer for å finne konfigurasjoner i RCS/det globale repositoriet</span><span class="sxs-lookup"><span data-stu-id="9f039-103">RCS enhanced filtering options for finding configurations in the RCS/Global repository</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9f039-104">Dette emnet beskriver forbedrede filtreringsfunksjoner for det det globale repositoriet (RCS) som er forbedret for å inkludere muligheten til å filtrere med følgende kriterier:</span><span class="sxs-lookup"><span data-stu-id="9f039-104">This topic describes enhanced filtering capabilities for Regulatory Configuration Services (RCS) Global repository, which have been improved to include the ability to filter with the following criteria:</span></span> 
- <span data-ttu-id="9f039-105">**Land/område**– basert på ISO-landskoder</span><span class="sxs-lookup"><span data-stu-id="9f039-105">**Country/region** - Based on ISO country codes</span></span>  
- <span data-ttu-id="9f039-106">**Kode**-typer for:</span><span class="sxs-lookup"><span data-stu-id="9f039-106">**Tags** types for:</span></span>
  - <span data-ttu-id="9f039-107">Funksjonelt område</span><span class="sxs-lookup"><span data-stu-id="9f039-107">Functional area</span></span>
  - <span data-ttu-id="9f039-108">Funksjonsområde</span><span class="sxs-lookup"><span data-stu-id="9f039-108">Feature area</span></span>
  - <span data-ttu-id="9f039-109">Bransje</span><span class="sxs-lookup"><span data-stu-id="9f039-109">Industry</span></span> 
  - <span data-ttu-id="9f039-110">Forretningsdokument</span><span class="sxs-lookup"><span data-stu-id="9f039-110">Business document</span></span> 

<span data-ttu-id="9f039-111">Du kan bruke filtre, enten individuelt eller i grupper, for å gjøre det lettere å finne bestemte eller relaterte konfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="9f039-111">To make it easier to discover specific or related configurations you can apply filters, either individually or as a group.</span></span> <span data-ttu-id="9f039-112">Hvis du for eksempel vil finne en enkelt type konfigurerbare forretningsdokumenter som er relatert til leverandørfakturaer, kan du bruke et **Forretningsdokumenttype**-filter for å søke etter denne dokumenttypen.</span><span class="sxs-lookup"><span data-stu-id="9f039-112">For example, to find a single type of 'configurable business documents that are related to vendor invoices, you could apply a **Business document type** filter to search for that type of document.</span></span> 

<span data-ttu-id="9f039-113">[![Filterdel for det globale repositoriet](media/rcs-enhanced-filter-section.JPG)](./media/rcs-enhanced-filter-section.JPG)</span><span class="sxs-lookup"><span data-stu-id="9f039-113">[![Filter section for Global repository](media/rcs-enhanced-filter-section.JPG)](./media/rcs-enhanced-filter-section.JPG)</span></span> 

<span data-ttu-id="9f039-114">Du kan finjustere søket ytterligere ved å velge dokumenttype, for eksempel "leverandørfaktura", og klikke **Bruk filter**.</span><span class="sxs-lookup"><span data-stu-id="9f039-114">You can further refine the search by selecting document type, for example 'vendor invoice' and clicking **Apply filter**.</span></span> <span data-ttu-id="9f039-115">Følgende eksempel viser resultatene ved filtrering på **Forretningsdokumenttype** med dokumenttypen lagt til.</span><span class="sxs-lookup"><span data-stu-id="9f039-115">The following example shows the results when filtering on **Business document type** with the document type added.</span></span> 

<span data-ttu-id="9f039-116">[![Brukte filter og import for forretningsdokumenttype](media/rcs-enhanced-filtering-applied.JPG)](./media/rcs-enhanced-filtering-applied.JPG)</span><span class="sxs-lookup"><span data-stu-id="9f039-116">[![Applied filter and Import for business document type](media/rcs-enhanced-filtering-applied.JPG)](./media/rcs-enhanced-filtering-applied.JPG)</span></span> 

<span data-ttu-id="9f039-117">Filtrerte resultater kan importeres til en brukers RCS-repositorium eller et Dynamics 365 Finance-miljø, enten individuelt eller som et sett.</span><span class="sxs-lookup"><span data-stu-id="9f039-117">Filtered results can be imported into a users RCS repository or a Dynamics 365 Finance environment, either individually or as a set.</span></span> <span data-ttu-id="9f039-118">Dette gjør du ved å velge konfigurasjonsgruppen og klikke **Importer**.</span><span class="sxs-lookup"><span data-stu-id="9f039-118">To do this, select the group of configurations, and click **Import**.</span></span>
