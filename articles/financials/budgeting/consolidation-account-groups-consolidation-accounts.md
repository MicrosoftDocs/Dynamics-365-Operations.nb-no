---
title: Konsolideringskontogrupper og flere konsolideringskontoer
description: Dette emnet gir informasjon om konsolideringskontogrupper og flere konsolideringskontoer, og forklarer hvordan de brukes i Microsoft Dynamics 365 for Finance and Operations.
author: aprilolson
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerConsolidateAccountGroup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 265544
ms.assetid: 71c31df7-b655-46a8-8844-4f92a8bd71b0
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: f1c463ee54512b07f5e45c4df995aefed6110cb0
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "366403"
---
# <a name="consolidation-account-groups-and-additional-consolidation-accounts"></a><span data-ttu-id="40693-103">Konsolideringskontogrupper og flere konsolideringskontoer</span><span class="sxs-lookup"><span data-stu-id="40693-103">Consolidation account groups and additional consolidation accounts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="40693-104">Dette emnet gir informasjon om konsolideringskontogrupper og flere konsolideringskontoer, og forklarer hvordan de brukes i Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="40693-104">This topic provides information about consolidation account groups and additional consolidation accounts, and explains how they are used in Microsoft Dynamics 365 for Finance and Operations.</span></span>

<a name="consolidation-account-groups"></a><span data-ttu-id="40693-105">Konsolideringskontogrupper</span><span class="sxs-lookup"><span data-stu-id="40693-105">Consolidation account groups</span></span>
----------------------------

<span data-ttu-id="40693-106">Med konsolideringskontogrupper kan du opprette grupper med kontoer som du vil bruke til å konsolidere dataene.</span><span class="sxs-lookup"><span data-stu-id="40693-106">Consolidation account groups let you create groups of the accounts that you want to use to consolidate data.</span></span> <span data-ttu-id="40693-107">Som oftest representerer en konsolideringskontogruppe en lovpålagt kontoplan eller tilordner kontoer til en gruppe som er definert av selskapets hovedkontor.</span><span class="sxs-lookup"><span data-stu-id="40693-107">Most often, a consolidation account group represents a government-mandated chart of accounts or maps accounts to a group that is defined by the company's headquarters.</span></span> <span data-ttu-id="40693-108">Du kan finne konsolideringskontogrupper i **Oppsett**-området i **Konsolideringer**-modulen.</span><span class="sxs-lookup"><span data-stu-id="40693-108">You can find consolidation account groups in the **Setup** area of the **Consolidations** module.</span></span> <span data-ttu-id="40693-109">Når du legger til en ny gruppe, angir du en unik ID for kontogruppen og et navn.</span><span class="sxs-lookup"><span data-stu-id="40693-109">When you add a new group, you enter a unique identifier for the account group and a name.</span></span>

## <a name="additional-consolidation-accounts"></a><span data-ttu-id="40693-110">Flere konsolideringskontoer</span><span class="sxs-lookup"><span data-stu-id="40693-110">Additional consolidation accounts</span></span>
<span data-ttu-id="40693-111">Med flere konsolideringskontoer kan du tilordne en konto fra en eksisterende kontoplan til en konsolideringskontogruppe.</span><span class="sxs-lookup"><span data-stu-id="40693-111">Additional consolidation accounts let you assign an account from an existing chart of accounts to a consolidation account group.</span></span> <span data-ttu-id="40693-112">Deretter kan du angi en verdi og et navn for konsolideringskontoen.</span><span class="sxs-lookup"><span data-stu-id="40693-112">You can then specify a consolidation account value and name.</span></span> 

<span data-ttu-id="40693-113">Du kan finne flere konsolideringskontoer i **Oppsett**-området i **Konsolideringer**-modulen.</span><span class="sxs-lookup"><span data-stu-id="40693-113">You can find additional consolidation accounts in the **Setup** area of the **Consolidations** module.</span></span> <span data-ttu-id="40693-114">Når du oppretter en ny konsolideringskonto, må du angi følgende informasjon:</span><span class="sxs-lookup"><span data-stu-id="40693-114">When you create a new consolidation account, you must specify the following information:</span></span>

-   <span data-ttu-id="40693-115">**Hovedkonto** – Dette feltet er et oppslagsfelt som viser alle hovedkontoer som er basert på kontoplanen som du valgte på siden.</span><span class="sxs-lookup"><span data-stu-id="40693-115">**Main account** – This field is a lookup that shows all the main accounts that are based on the chart of accounts that you selected on the page.</span></span> <span data-ttu-id="40693-116">Når du velger en konto, angis navnet automatisk i feltet **Navn på hovedkonto**.</span><span class="sxs-lookup"><span data-stu-id="40693-116">When you select an account, the name is automatically entered in the **Main account name** field.</span></span>
-   <span data-ttu-id="40693-117">**Konsernkontogruppe** – Bruk dette feltet til å angi gruppen du vil tilordne kontoen til.</span><span class="sxs-lookup"><span data-stu-id="40693-117">**Consolidation account group** – Use this field to specify the group to assign the account to.</span></span> <span data-ttu-id="40693-118">Hvis du konsoliderer på to forskjellige måter, må du legge til samme konto i alle fire konsolideringskontogrupper.</span><span class="sxs-lookup"><span data-stu-id="40693-118">If you consolidate in two different ways, you must add the same account to all four consolidation account groups.</span></span>
-   <span data-ttu-id="40693-119">**Konsolideringskonto** – Angi verdien for konsolideringskontoen.</span><span class="sxs-lookup"><span data-stu-id="40693-119">**Consolidation account** – Enter the value of the consolidation account.</span></span> <span data-ttu-id="40693-120">Denne verdien må ikke være en konto fra en kontoplan.</span><span class="sxs-lookup"><span data-stu-id="40693-120">This value doesn't have to be an account from a chart of accounts.</span></span> <span data-ttu-id="40693-121">Det kan være en hvilken som helst verdi du trenger.</span><span class="sxs-lookup"><span data-stu-id="40693-121">It can be any value that you require.</span></span>
-   <span data-ttu-id="40693-122">**Navn på konsolideringskonto** – Angi navnet på kontoen slik du vil at det skal vises i forespørsler og rapporter.</span><span class="sxs-lookup"><span data-stu-id="40693-122">**Consolidation account name** – Enter the name of account as you want it to appear on inquiries and reports.</span></span>
-   <span data-ttu-id="40693-123">**SAT-nivå** – Dette feltet brukes til å rapportere kontoutdrag til meksikanske skattemyndigheter.</span><span class="sxs-lookup"><span data-stu-id="40693-123">**SAT level** – This field is used to report account statements to the Mexican tax authorities.</span></span> 

<span data-ttu-id="40693-124">Når du er ferdig med å opprette konsolideringskontogruppene og ekstra konsolideringskontoer, kan du velge gruppen i den elektroniske konsolideringsprosessen.</span><span class="sxs-lookup"><span data-stu-id="40693-124">When you've finished creating your consolidation account groups and additional consolidation accounts, you can select the group in the Consolidate online process.</span></span>


<span data-ttu-id="40693-125">Hvis du vil ha mer informasjon, kan du se [Opprette konsolideringsgrupper og flere konsolideringskontoer](../general-ledger/tasks/create-consolidation-groups.md)</span><span class="sxs-lookup"><span data-stu-id="40693-125">For more information, see [Create consolidation groups and additional consolidation accounts](../general-ledger/tasks/create-consolidation-groups.md).</span></span> 



