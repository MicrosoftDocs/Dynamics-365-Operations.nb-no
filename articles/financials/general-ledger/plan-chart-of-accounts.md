---
title: Planlegge kontoplanen
description: "Denne artikkelen inneholder informasjon som hjelper deg med å planlegge kontoplanen for organisasjonen."
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DimensionConfigureAccountStructure, LedgerChartOfAccounts
audience: Application User
ms.reviewer: robinr
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 14051
ms.assetid: 10edb129-33f0-4cf9-b2a7-4b7ffa09b229
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 848da7ec8f4a7915f3b78945b808b564f4510434
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---

# <a name="plan-your-chart-of-accounts"></a><span data-ttu-id="13159-103">Planlegge kontoplanen</span><span class="sxs-lookup"><span data-stu-id="13159-103">Plan your chart of accounts</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="13159-104">Denne artikkelen inneholder informasjon som hjelper deg med å planlegge kontoplanen for organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="13159-104">This article provides information that will help you plan the chart of accounts for your organization.</span></span>

<span data-ttu-id="13159-105">Hvis du vil spore og vedlikeholde økonomisk informasjon i en organisasjon, kan du definere en kontoplan.</span><span class="sxs-lookup"><span data-stu-id="13159-105">To track and maintain financial information in an organization, you can set up a chart of accounts.</span></span> <span data-ttu-id="13159-106">En kontoplan er en samling kontoer som definerer et økonomisk rammeverk.</span><span class="sxs-lookup"><span data-stu-id="13159-106">A chart of accounts is a collection of accounts that define a financial framework.</span></span> <span data-ttu-id="13159-107">Hvis du vil spore transaksjonene videre i disse kontoene, kan du legge til segmenter, som kalles finansdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="13159-107">To further track the transactions in these accounts, you can add segments, which are known as financial dimensions.</span></span> <span data-ttu-id="13159-108">En utgiftskonto kan for eksempel omfatte finansdimensjoner kalt Avdeling, Kostsenter og Formål.</span><span class="sxs-lookup"><span data-stu-id="13159-108">For example, an expense account might include financial dimensions that are named Department, Cost center, and Purpose.</span></span> <span data-ttu-id="13159-109">Brukerdefinerte regler, som kalles kontostrukturer og avanserte regler, fastsetter hvordan finansdimensjonene er knyttet til hovedkontoene og andre finansdimensjoner, og også hvordan transaksjoner registreres.</span><span class="sxs-lookup"><span data-stu-id="13159-109">User-defined rules, which are known as account structures and advanced rules, determine how financial dimensions are attached to the main accounts and other financial dimensions, and also how transactions are entered.</span></span> 

<span data-ttu-id="13159-110">Kontoplanen er en strukturert liste over den juridiske enhetens finanskontoer.</span><span class="sxs-lookup"><span data-stu-id="13159-110">The chart of accounts is a structured list of a legal entity’s general ledger accounts.</span></span> <span data-ttu-id="13159-111">Listen brukes til å utarbeide økonomiske rapporter til myndigheter og eiere.</span><span class="sxs-lookup"><span data-stu-id="13159-111">The list is used to prepare financial reports for authorities and owners.</span></span> <span data-ttu-id="13159-112">Kontoene grupperes i kontotyper og aggregeres deretter ytterligere i større, overordnede kategorier.</span><span class="sxs-lookup"><span data-stu-id="13159-112">The accounts are grouped into types of accounts and then further aggregated into larger categories.</span></span> <span data-ttu-id="13159-113">På det øverste nivået grupperes kontoene som henholdsvis inntekter og kostnader (driftskontoer) og aktiva og gjeld (balansekontoer).</span><span class="sxs-lookup"><span data-stu-id="13159-113">At the most general level, the accounts are grouped as revenues and costs (operating accounts), and assets and liabilities (balance accounts).</span></span> 

<span data-ttu-id="13159-114">En kontoplan kan deles og brukes av alle juridiske enheter i en organisasjon.</span><span class="sxs-lookup"><span data-stu-id="13159-114">A chart of accounts can be shared and used by any legal entity in an organization.</span></span> <span data-ttu-id="13159-115">Kontoplanen som brukes av en juridisk enhet, er definert på **Finans**-siden.</span><span class="sxs-lookup"><span data-stu-id="13159-115">The chart of accounts that is used by a legal entity is defined on the **Ledger** page.</span></span> 

<span data-ttu-id="13159-116">Her er noen av faktorene du må vurdere når du planlegger strukturen til kontoplanen for organisasjonen:</span><span class="sxs-lookup"><span data-stu-id="13159-116">Here are some of the factors that you must consider when you plan the structure of the chart of accounts for your organization:</span></span>

-   <span data-ttu-id="13159-117">Rapporteringskravene i landet/området der organisasjonen holder til</span><span class="sxs-lookup"><span data-stu-id="13159-117">The reporting requirements of the country/region where your organization is based</span></span>
-   <span data-ttu-id="13159-118">Rapporteringskravene til den juridiske enheten</span><span class="sxs-lookup"><span data-stu-id="13159-118">The reporting requirements of your legal entity</span></span>
-   <span data-ttu-id="13159-119">Graden av detaljer som kreves, både for den eksterne organisasjonen og organisasjonen din</span><span class="sxs-lookup"><span data-stu-id="13159-119">The degree of specification that is required, both for both external organizations and for your organization</span></span>

<span data-ttu-id="13159-120">Definer kontoplanen på **Kontoplan**-siden.</span><span class="sxs-lookup"><span data-stu-id="13159-120">Create the chart of accounts on the **Chart of accounts** page.</span></span> <span data-ttu-id="13159-121">Hovedkontoer kan opprettes fra **Kontoplan**-siden eller **Hovedkontoer**-siden.</span><span class="sxs-lookup"><span data-stu-id="13159-121">Main accounts can be created from the **Chart of accounts** page or the **Main accounts** page.</span></span> <span data-ttu-id="13159-122">Hovedkontoene kan ikke bruke spesialtegn som brukes som skilletegn for kontoplan.</span><span class="sxs-lookup"><span data-stu-id="13159-122">Your main accounts shouldn't use any special characters that are used as chart of accounts delimiters.</span></span> <span data-ttu-id="13159-123">Hvis du har et spesialtegn som er det samme som skilletegnet for kontoplan, kan dette føre til ustabilitet, eller det kan bli nødvendig å alltid bruke oppslag eller undermenyen når du angir kombinasjoner av konto og dimensjon.</span><span class="sxs-lookup"><span data-stu-id="13159-123">If you do have a special character that is the same as your chart of accounts delimiter, you may experience instability, or the need to always use lookups or the flyout when entering account and dimension combinations.</span></span> <span data-ttu-id="13159-124">Hvis du vil ha mer informasjon, kan du se [Opprette en hovedkonto](tasks/create-account-structures.md).</span><span class="sxs-lookup"><span data-stu-id="13159-124">For more information, see [Create a main account](tasks/create-account-structures.md).</span></span>


<span data-ttu-id="13159-125">Det er lurt å koble hovedkontoene til hovedkontokategorier, slik at du kan dra nytte av standard økonomiske rapporter uten å måtte gjøre endringer.</span><span class="sxs-lookup"><span data-stu-id="13159-125">It's a good idea to link the main accounts to main account categories, so that you can take advantage of the default financial reports without having to make any modifications.</span></span> <span data-ttu-id="13159-126">Derfor går det raskere og enklere å utforme og vedlikeholde rapporter.</span><span class="sxs-lookup"><span data-stu-id="13159-126">Therefore, you can more quickly and easily design and maintain reports.</span></span> 

<span data-ttu-id="13159-127">Bruk siden **Konfigurer kontostrukturer** til å opprette kontostrukturer.</span><span class="sxs-lookup"><span data-stu-id="13159-127">Use the **Configure account structures** page to create account structures.</span></span> <span data-ttu-id="13159-128">Kontostrukturer brukes til å definere gyldige kombinasjoner.</span><span class="sxs-lookup"><span data-stu-id="13159-128">Account structures define valid combinations.</span></span> <span data-ttu-id="13159-129">Kombinasjonene, sammen med hovedkontoer, utgjør en kontoplan.</span><span class="sxs-lookup"><span data-stu-id="13159-129">The combinations, together with main accounts, form a chart of accounts.</span></span>  <span data-ttu-id="13159-130">Hvis du vil ha mer informasjon, kan du se [Opprette kontostrukturer](tasks/create-main-account.md).</span><span class="sxs-lookup"><span data-stu-id="13159-130">For more information, see [Create account structures](tasks/create-main-account.md).</span></span>

<span data-ttu-id="13159-131">**Overstyringer for juridisk enhet**</span><span class="sxs-lookup"><span data-stu-id="13159-131">**Legal entity overrides**</span></span> 

<span data-ttu-id="13159-132">Ikke alle hovedkontoer er gyldige for alle juridiske enheter, og noen er kanskje bare relevante i en bestemt tidsperiode.</span><span class="sxs-lookup"><span data-stu-id="13159-132">Not all main accounts are valid for all legal entities and some may only be relevant for a specific time period.</span></span> <span data-ttu-id="13159-133">I denne situasjonen kan delen Overstyringer for juridisk enhet brukes til å identifisere hvilke firmaer hovedkontoen skal suspenderes for, hvem som er eier, og tidsperioden dimensjonen er aktiv.</span><span class="sxs-lookup"><span data-stu-id="13159-133">In this scenario the Legal entity overrides section can be used to identify which companies the main account should be suspended for, who the owner is and the time period the dimension is active.</span></span> <span data-ttu-id="13159-134">Overstyringene på det delte nivået kan ikke være mer begrensende enn overstyringer på nivået for juridisk enhet.</span><span class="sxs-lookup"><span data-stu-id="13159-134">The overrides at the shared level cannot be more restrictive than the overrides at the legal entity level.</span></span>

<span data-ttu-id="13159-135">Hvis du vil ha mer informasjon, se følgende emner: [Finansdimensjoner](financial-dimensions.md)
[Opprette og tilordne avanserte regelstrukturer](tasks/create-assign-advanced-rule-structures.md)</span><span class="sxs-lookup"><span data-stu-id="13159-135">For more information, see the following topics: [Financial dimensions](financial-dimensions.md)
[Create and assign advanced rule structures](tasks/create-assign-advanced-rule-structures.md)</span></span>




