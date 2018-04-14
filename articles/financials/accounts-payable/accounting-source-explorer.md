---
title: Regnskapskildeutforsker
description: "Denne artikkelen inneholder informasjon om regnskapskildeutforsker, som du kan bruke for detaljert analyse av kildeinformasjonen bak regnskapsoppføringer i økonomimodulen."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AccountingSourceExplorer
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 15391
ms.assetid: 57b95899-7298-43c0-8034-45b5d993cbf2
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: d5d9f7ff6b4d3ea764717240f9736a81c1aee6c1
ms.contentlocale: nb-no
ms.lasthandoff: 04/13/2018

---

# <a name="accounting-source-explorer"></a><span data-ttu-id="caa5d-103">Regnskapskildeutforsker</span><span class="sxs-lookup"><span data-stu-id="caa5d-103">Accounting source explorer</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="caa5d-104">Denne artikkelen inneholder informasjon om regnskapskildeutforsker, som du kan bruke for detaljert analyse av kildeinformasjonen bak regnskapsoppføringer i økonomimodulen.</span><span class="sxs-lookup"><span data-stu-id="caa5d-104">This article provides information about Accounting source explorer, which you can use for detailed analysis of the source information behind general ledger accounting entries.</span></span>

<span data-ttu-id="caa5d-105">Regnskapskildeutforsker er en ny side som viser kildeinformasjon.</span><span class="sxs-lookup"><span data-stu-id="caa5d-105">Accounting source explorer is a new page that shows source information.</span></span> <span data-ttu-id="caa5d-106">Du kan bruke Regnskapskildeutforsker enten som et frittstående verktøy eller til å analysere detaljene bak regnskapsoppføringer i økonomimodulen.</span><span class="sxs-lookup"><span data-stu-id="caa5d-106">You can use Accounting source explorer either as a stand-alone tool or to analyze the details behind general ledger accounting entries.</span></span> <span data-ttu-id="caa5d-107">Du kan for eksempel bruke Regnskapskildeutforsker til å få den mest detaljerte kildeinformasjonen for en saldo i Råbalanse eller for en bilagstransaksjon.</span><span class="sxs-lookup"><span data-stu-id="caa5d-107">For example, you can use Accounting source explorer to get the most detailed source information for a balance in Trail balance or for a voucher transaction.</span></span> <span data-ttu-id="caa5d-108">Du kan deretter bruke funksjonen Eksporter til Microsoft Excel for å dele opp informasjonen ytterligere i Microsoft Excel (for eksempel i en pivottabell eller pivottabellrapport).</span><span class="sxs-lookup"><span data-stu-id="caa5d-108">You can then use the Export to MS Excel feature to further slice and dice the information in Microsoft Excel (for example, in a PivotTable or on a PivotTable report).</span></span>

<span data-ttu-id="caa5d-109">Regnskapskildeutforsker viser alltid det samme totalbeløpet per finanskonto som Økonomimodul viser (for eksempel i Råbalanse).</span><span class="sxs-lookup"><span data-stu-id="caa5d-109">Accounting source explorer always shows the same total amount per ledger account as General ledger shows (for example, in Trial balance).</span></span> <span data-ttu-id="caa5d-110">På samme måte som i Råbalanse kan du vise segmenter i separate kolonner.</span><span class="sxs-lookup"><span data-stu-id="caa5d-110">As in Trial balance, you can display segments in separate columns.</span></span> <span data-ttu-id="caa5d-111">Bare velg det riktige finansdimensjonssettet.</span><span class="sxs-lookup"><span data-stu-id="caa5d-111">Just select the appropriate financial dimension set.</span></span> 

<span data-ttu-id="caa5d-112">Du kan bruke parametere til å definere et datointervall for analysen.</span><span class="sxs-lookup"><span data-stu-id="caa5d-112">You can use parameters to define a date interval for the analysis.</span></span> <span data-ttu-id="caa5d-113">Denne funksjonen ligner også funksjonaliteten i Råbalanse.</span><span class="sxs-lookup"><span data-stu-id="caa5d-113">This functionality also resembles the functionality in Trial balance.</span></span>

<span data-ttu-id="caa5d-114">Regnskapskildeutforsker viser tilleggsinformasjon basert på regnskapsdistribusjoner og, hvis det er aktuelt, prosjektregnskapsdistribusjoner for alle dokumenter som bruker kildedokumentrammeverket.</span><span class="sxs-lookup"><span data-stu-id="caa5d-114">For all documents that use the source document framework, Accounting source explorer shows additional information, based on accounting distributions and, if applicable, project accounting distributions.</span></span> <span data-ttu-id="caa5d-115">Denne informasjonen omfatter pengebeløpstype, prosjekt, aktivitet, kategori og linjeegenskap.</span><span class="sxs-lookup"><span data-stu-id="caa5d-115">This information includes the monetary amount type, project, activity, category, and line property.</span></span> <span data-ttu-id="caa5d-116">Her er noen eksempler på analysen du kan foreta:</span><span class="sxs-lookup"><span data-stu-id="caa5d-116">Here are some examples of the analysis that you can do:</span></span>

-   <span data-ttu-id="caa5d-117">Avvik mellom bestillinger og leverandørfakturaer, fordi hvert enkelt avvik representeres av en pengebeløpstype, for eksempel gebyravvik</span><span class="sxs-lookup"><span data-stu-id="caa5d-117">Variances between purchase orders and vendor invoices, because each variance is represented by a monetary amount type, such as charge variance</span></span>
-   <span data-ttu-id="caa5d-118">Fakturerbare kontra ikke-fakturerbare timer og utgifter per prosjekt, forretningsenhet og hovedkonto</span><span class="sxs-lookup"><span data-stu-id="caa5d-118">Billable versus non-billable hours and expenses per project, business unit, and main account</span></span>

<span data-ttu-id="caa5d-119">Når det gjelder kildedokumenter som bruker konseptet referanse-ID-er for kildedokument, viser Regnskapskildeutforsker ytterligere detaljer, for eksempel kunde, leverandør, arbeider, produkt, antall, enhetstekst og beskrivelser.</span><span class="sxs-lookup"><span data-stu-id="caa5d-119">For source documents that use the source document reference identities concept, Accounting source explorer shows even more details, such as the customer, vendor, worker, product, quantity, unit text, and descriptions.</span></span> <span data-ttu-id="caa5d-120">Her er noen eksempler på analysen du kan foreta:</span><span class="sxs-lookup"><span data-stu-id="caa5d-120">Here are some examples of the analysis that you can do:</span></span>

-   <span data-ttu-id="caa5d-121">Hotellutgifter per forretningsenhet og hotellmerke for en regnskapsperiode, basert på reiseregninger</span><span class="sxs-lookup"><span data-stu-id="caa5d-121">Hotel expenses per business unit and hotel brand for a fiscal period, based on expense reports</span></span>
-   <span data-ttu-id="caa5d-122">Rabatter per leverandør, produkt, avdeling</span><span class="sxs-lookup"><span data-stu-id="caa5d-122">Discounts per vendor, product, department</span></span>

<span data-ttu-id="caa5d-123">Når det gjelder disse dokumentene, kan du også navigere til det faktiske kildedokumentet fra Regnskapskildeutforsker.</span><span class="sxs-lookup"><span data-stu-id="caa5d-123">For these documents, you can also navigate to the actual source document from Accounting source explorer.</span></span>




