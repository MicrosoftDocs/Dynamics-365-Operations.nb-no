---
title: Planlegge kontoplanen
description: Dette emnet inneholder informasjon som hjelper deg med å planlegge kontoplanen for organisasjonen.
author: aprilolson
manager: AnnBe
ms.date: 04/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionConfigureAccountStructure, LedgerChartOfAccounts
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 14051
ms.assetid: 10edb129-33f0-4cf9-b2a7-4b7ffa09b229
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 93d5ef19a4b1cb2885c611c8675ac06fd841ac56
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "337584"
---
# <a name="plan-your-chart-of-accounts"></a><span data-ttu-id="0ad95-103">Planlegge kontoplanen</span><span class="sxs-lookup"><span data-stu-id="0ad95-103">Plan your chart of accounts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0ad95-104">Dette emnet inneholder informasjon som hjelper deg med å planlegge kontoplanen for organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="0ad95-104">This topic provides information that will help you plan the chart of accounts for your organization.</span></span>

<span data-ttu-id="0ad95-105">Hvis du vil spore og vedlikeholde økonomisk informasjon i en organisasjon, kan du definere en kontoplan.</span><span class="sxs-lookup"><span data-stu-id="0ad95-105">To track and maintain financial information in an organization, you can set up a chart of accounts.</span></span> <span data-ttu-id="0ad95-106">En kontoplan er en samling kontoer som definerer et økonomisk rammeverk.</span><span class="sxs-lookup"><span data-stu-id="0ad95-106">A chart of accounts is a collection of accounts that define a financial framework.</span></span> <span data-ttu-id="0ad95-107">For å spore ytterligere transaksjonene i disse kontoene, kan du legge til segmenter.</span><span class="sxs-lookup"><span data-stu-id="0ad95-107">To further track the transactions in these accounts, you can add segments.</span></span> <span data-ttu-id="0ad95-108">Disse segmentene kalles finansdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="0ad95-108">These segments are known as financial dimensions.</span></span> <span data-ttu-id="0ad95-109">En utgiftskonto kan for eksempel omfatte finansdimensjoner kalt Avdeling, Kostsenter og Formål.</span><span class="sxs-lookup"><span data-stu-id="0ad95-109">For example, an expense account might include financial dimensions that are named Department, Cost center, and Purpose.</span></span> <span data-ttu-id="0ad95-110">Brukerdefinerte regler fastsetter hvordan finansdimensjonene er knyttet til hovedkontoene og til andre finansdimensjoner, og også hvordan transaksjoner registreres.</span><span class="sxs-lookup"><span data-stu-id="0ad95-110">User-defined rules determine how financial dimensions are attached to the main accounts and to other financial dimensions, and also how transactions are entered.</span></span> <span data-ttu-id="0ad95-111">Disse brukerdefinerte reglene er kjent som kontostrukturer og avanserte regler.</span><span class="sxs-lookup"><span data-stu-id="0ad95-111">These user-defined rules are known as account structures and advanced rules.</span></span>

<span data-ttu-id="0ad95-112">Kontoplanen er en strukturert liste over den juridiske enhetens finanskontoer.</span><span class="sxs-lookup"><span data-stu-id="0ad95-112">The chart of accounts is a structured list of a legal entity's general ledger accounts.</span></span> <span data-ttu-id="0ad95-113">Listen brukes til å utarbeide økonomiske rapporter til myndigheter og eiere.</span><span class="sxs-lookup"><span data-stu-id="0ad95-113">The list is used to prepare financial reports for authorities and owners.</span></span> <span data-ttu-id="0ad95-114">Kontoene grupperes først i kontotyper og aggregeres deretter ytterligere i større, overordnede kategorier.</span><span class="sxs-lookup"><span data-stu-id="0ad95-114">The accounts are first grouped into types of accounts and then further aggregated into larger categories.</span></span> <span data-ttu-id="0ad95-115">På det øverste nivået grupperes kontoene som henholdsvis inntekter og kostnader (driftskontoer) og aktiva og gjeld (balansekontoer).</span><span class="sxs-lookup"><span data-stu-id="0ad95-115">At the most general level, the accounts are grouped as revenues and costs (operating accounts), and assets and liabilities (balance accounts).</span></span>

<span data-ttu-id="0ad95-116">En kontoplan kan deles og brukes av alle juridiske enheter i en organisasjon.</span><span class="sxs-lookup"><span data-stu-id="0ad95-116">A chart of accounts can be shared and used by any legal entity in an organization.</span></span> <span data-ttu-id="0ad95-117">Kontoplanen som brukes av en juridisk enhet, er definert på **Finans**-siden.</span><span class="sxs-lookup"><span data-stu-id="0ad95-117">The chart of accounts that is used by a legal entity is defined on the **Ledger** page.</span></span>

<span data-ttu-id="0ad95-118">Her er noen av faktorene du må vurdere når du planlegger strukturen til kontoplanen for organisasjonen:</span><span class="sxs-lookup"><span data-stu-id="0ad95-118">Here are some of the factors that you must consider when you plan the structure of the chart of accounts for your organization:</span></span>

- <span data-ttu-id="0ad95-119">Rapporteringskravene i landet eller området der organisasjonen holder til</span><span class="sxs-lookup"><span data-stu-id="0ad95-119">The reporting requirements of the country or region where your organization is based</span></span>
- <span data-ttu-id="0ad95-120">Rapporteringskravene til den juridiske enheten</span><span class="sxs-lookup"><span data-stu-id="0ad95-120">The reporting requirements of your legal entity</span></span>
- <span data-ttu-id="0ad95-121">Graden av detaljer som kreves, både for den eksterne organisasjonen og organisasjonen din</span><span class="sxs-lookup"><span data-stu-id="0ad95-121">The degree of specification that is required, both for both external organizations and for your organization</span></span>

<span data-ttu-id="0ad95-122">Du kan definere kontoplanen på **Kontoplan**-siden.</span><span class="sxs-lookup"><span data-stu-id="0ad95-122">You create the chart of accounts on the **Chart of accounts** page.</span></span> <span data-ttu-id="0ad95-123">Du kan opprette hovedkontoer fra **Kontoplan**-siden eller **Hovedkontoer**-siden.</span><span class="sxs-lookup"><span data-stu-id="0ad95-123">You can create main accounts from the **Chart of accounts** page or the **Main accounts** page.</span></span> <span data-ttu-id="0ad95-124">Hovedkontoene kan ikke bruke spesialtegn som brukes som skilletegn for kontoplan.</span><span class="sxs-lookup"><span data-stu-id="0ad95-124">Your main accounts shouldn't use any special characters that are used as delimiters for chart of accounts.</span></span> <span data-ttu-id="0ad95-125">Ellers kan du oppleve ustabilitet, eller du må kanskje alltid bruke oppslag eller dialogboksen når du angir kombinasjoner av kontoer og dimensjoner.</span><span class="sxs-lookup"><span data-stu-id="0ad95-125">Otherwise, you might experience instability, or you might always have to use lookups or the dialog box when you enter combinations of accounts and dimensions.</span></span> <span data-ttu-id="0ad95-126">Hvis du vil ha mer informasjon, kan du se [Opprette en hovedkonto](tasks/create-main-account.md).</span><span class="sxs-lookup"><span data-stu-id="0ad95-126">For more information, see [Create a main account](tasks/create-main-account.md).</span></span>

> [!NOTE]
> <span data-ttu-id="0ad95-127">I Microsoft Dynamics for Finance and Operations versjon 8.0 (april 2018) kan du endre skilletegn for kontoplan på **Parametere for økonomimodul**-siden.</span><span class="sxs-lookup"><span data-stu-id="0ad95-127">In Microsoft Dynamics for Finance and Operations version 8.0 (April 2018), you can modify the chart of accounts delimiter from the **General ledger parameters** page.</span></span>

<span data-ttu-id="0ad95-128">Det er lurt å koble hovedkontoene til hovedkontokategorier, slik at du kan dra nytte av standard økonomiske rapporter uten å måtte gjøre endringer.</span><span class="sxs-lookup"><span data-stu-id="0ad95-128">It's a good idea to link the main accounts to main account categories, so that you can take advantage of the default financial reports without having to make any modifications.</span></span> <span data-ttu-id="0ad95-129">Derfor går det raskere og enklere å utforme og vedlikeholde rapporter.</span><span class="sxs-lookup"><span data-stu-id="0ad95-129">Therefore, you can more quickly and easily design and maintain reports.</span></span>

<span data-ttu-id="0ad95-130">Du kan opprette kontostrukturer på siden **Konfigurer kontostrukturer**.</span><span class="sxs-lookup"><span data-stu-id="0ad95-130">You create account structures on the **Configure account structures** page.</span></span> <span data-ttu-id="0ad95-131">Kontostrukturer brukes til å definere gyldige kombinasjoner.</span><span class="sxs-lookup"><span data-stu-id="0ad95-131">Account structures define valid combinations.</span></span> <span data-ttu-id="0ad95-132">Disse kombinasjonene, sammen med hovedkontoer, utgjør en kontoplan.</span><span class="sxs-lookup"><span data-stu-id="0ad95-132">These combinations, together with main accounts, form a chart of accounts.</span></span> <span data-ttu-id="0ad95-133">Hvis du vil ha mer informasjon, kan du se [Opprette kontostrukturer](tasks/create-account-structures.md).</span><span class="sxs-lookup"><span data-stu-id="0ad95-133">For more information, see [Create account structures](tasks/create-account-structures.md).</span></span>

<span data-ttu-id="0ad95-134">**Overstyringer for juridisk enhet**</span><span class="sxs-lookup"><span data-stu-id="0ad95-134">**Legal entity overrides**</span></span>

<span data-ttu-id="0ad95-135">Ikke alle hovedkontoer er gyldige for alle juridiske enheter, og noen hovedkontoer er kanskje bare relevante i en bestemt periode.</span><span class="sxs-lookup"><span data-stu-id="0ad95-135">Not all main accounts are valid for all legal entities, and some main account might be relevant only for a specific period.</span></span> <span data-ttu-id="0ad95-136">I dette scenarioet kan du bruke delen **Overstyringer for juridisk enhet** til å identifisere firmaene som hovedkontoen skal suspenderes for, eieren, og perioden dimensjonen er aktiv.</span><span class="sxs-lookup"><span data-stu-id="0ad95-136">In this scenario, you can use the **Legal entity overrides** section to identify the companies that the main account should be suspended for, the owner, and the period when the dimension is active.</span></span> <span data-ttu-id="0ad95-137">Overstyringene på det delte nivået kan ikke være mer begrensende enn overstyringer på nivået for juridisk enhet.</span><span class="sxs-lookup"><span data-stu-id="0ad95-137">The overrides at the shared level can't be more restrictive than the overrides at the legal entity level.</span></span>

<span data-ttu-id="0ad95-138">Hvis du vil ha mer informasjon, se følgende emner:</span><span class="sxs-lookup"><span data-stu-id="0ad95-138">For more information, see the following topics:</span></span>

- [<span data-ttu-id="0ad95-139">Finansdimensjoner</span><span class="sxs-lookup"><span data-stu-id="0ad95-139">Financial dimensions</span></span>](financial-dimensions.md)
- [<span data-ttu-id="0ad95-140">Opprette og tilordne avanserte regelstrukturer</span><span class="sxs-lookup"><span data-stu-id="0ad95-140">Create and assign advanced rule structures</span></span>](tasks/create-assign-advanced-rule-structures.md)
