---
title: "Hjemmeside for Økonomimodul og Finansrapportering"
description: "Bruk økonomimodulen til å definere og styre finansposter for den juridiske enheten. Økonomimodulen er et register over debet- og kreditoppføringer. Disse oppføringene klassifiseres ved hjelp av kontoene som vises i en kontoplan."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 65431
ms.assetid: d2c604df-daae-42cd-82d9-c80e3dee4a60
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 78f3d9c27767c089ac686f333cae3cb50c03ee18
ms.contentlocale: nb-no
ms.lasthandoff: 07/18/2017

---

# <a name="general-ledger"></a><span data-ttu-id="8afdb-105">Økonomimodul</span><span class="sxs-lookup"><span data-stu-id="8afdb-105">General ledger</span></span> 

[!include[banner](../includes/banner.md)]


<span data-ttu-id="8afdb-106">Bruk økonomimodulen til å definere og styre finansposter for den juridiske enheten.</span><span class="sxs-lookup"><span data-stu-id="8afdb-106">Use General ledger to define and manage the legal entity’s financial records.</span></span> <span data-ttu-id="8afdb-107">Økonomimodulen er et register over debet- og kreditoppføringer.</span><span class="sxs-lookup"><span data-stu-id="8afdb-107">The general ledger is a register of debit and credit entries.</span></span> <span data-ttu-id="8afdb-108">Disse oppføringene klassifiseres ved hjelp av kontoene som vises i en kontoplan.</span><span class="sxs-lookup"><span data-stu-id="8afdb-108">These entries are classified using the accounts that are listed in a chart of accounts.</span></span> 

<span data-ttu-id="8afdb-109">Du kan fordele, eller distribuere, pengebeløp til én eller flere kontoer eller kombinasjoner og konto og dimensjon basert på fordelingsregler.</span><span class="sxs-lookup"><span data-stu-id="8afdb-109">You can allocate, or distribute, monetary amounts to one or more accounts or account and dimension combinations based on allocation rules.</span></span> <span data-ttu-id="8afdb-110">Det finnes to typer tildelinger: fast og variabel.</span><span class="sxs-lookup"><span data-stu-id="8afdb-110">There are two types of allocations: fixed and variable.</span></span> <span data-ttu-id="8afdb-111">Du kan også utligne transaksjoner mellom finanskontoer og revaluere valutabeløp.</span><span class="sxs-lookup"><span data-stu-id="8afdb-111">You can also settle transactions between ledger accounts and revalue currency amounts.</span></span> <span data-ttu-id="8afdb-112">På slutten av regnskapsåret må du generere avslutningstransaksjoner og klargjøre kontoene for neste regnskapsår.</span><span class="sxs-lookup"><span data-stu-id="8afdb-112">At the end of a fiscal year, you must generate closing transactions and prepare your accounts for the next fiscal year.</span></span> <span data-ttu-id="8afdb-113">Du kan bruke konsolideringsfunksjonaliteten til å kombinere de finansielle resultatene for flere juridiske enheter for datterselskap til resultater for én konsolidert organisasjon.</span><span class="sxs-lookup"><span data-stu-id="8afdb-113">You can use the consolidation functionality to combine the financial results for several subsidiary legal entities into results for a single, consolidated organization.</span></span> <span data-ttu-id="8afdb-114">Datterselskapene kan finnes i den samme Microsoft Dynamics 365 for Finance and Operations-databasen eller i separate databaser.</span><span class="sxs-lookup"><span data-stu-id="8afdb-114">The subsidiaries can be in the same Microsoft Dynamics 365 for Finance and Operations database or in separate databases.</span></span>

# <a name="sales-tax"></a><span data-ttu-id="8afdb-115">Merverdiavgift</span><span class="sxs-lookup"><span data-stu-id="8afdb-115">Sales tax</span></span>
<span data-ttu-id="8afdb-116">Hvert firma samler og betaler avgifter til forskjellige skattemyndigheter.</span><span class="sxs-lookup"><span data-stu-id="8afdb-116">Every company collects and pays taxes to various tax authorities.</span></span> <span data-ttu-id="8afdb-117">Reglene og satsene varierer etter land/område, delstat, region og by.</span><span class="sxs-lookup"><span data-stu-id="8afdb-117">The rules and rates vary by country/region, state, county, and city.</span></span> <span data-ttu-id="8afdb-118">Reglene må i tillegg oppdateres med jevne mellomrom når skattemyndighetene endrer kravene.</span><span class="sxs-lookup"><span data-stu-id="8afdb-118">In addition, the rules must be updated periodically when tax authorities change their requirements.</span></span> <span data-ttu-id="8afdb-119">Mva-koder inneholder grunnleggende informasjon om hvordan du samler og betaler avgifter til myndighetene.</span><span class="sxs-lookup"><span data-stu-id="8afdb-119">Sales tax codes contain the basic information about how much you collect and pay to the authorities.</span></span> <span data-ttu-id="8afdb-120">Når du definerer mva-koder, kan du definere beløpene eller prosentandelene som må samles inn.</span><span class="sxs-lookup"><span data-stu-id="8afdb-120">When you set up sales tax codes, you define the amounts or percentages that must be collected.</span></span> <span data-ttu-id="8afdb-121">Du definerer også de ulike metodene som brukes til å bruke disse beløpene eller prosentandelene på transaksjonsbeløpene.</span><span class="sxs-lookup"><span data-stu-id="8afdb-121">You also define the various methods by which those amounts or percentages are applied to transaction amounts.</span></span> <span data-ttu-id="8afdb-122">Emnene i denne delen gir informasjon om hvordan du definerer mva-koder for metodene og satsene som kreves av skattemyndighetene.</span><span class="sxs-lookup"><span data-stu-id="8afdb-122">The topics in this section provide information about how to set up sales tax codes for the methods and rates that your tax authorities require.</span></span>







