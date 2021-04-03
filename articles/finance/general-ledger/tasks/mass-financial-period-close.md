---
title: Lukke masseregnskapsperiode
description: Dette emnet viser hvordan du setter en periode på vent eller permanent lukker en periode for mer enn en juridisk enhet om gangen.
author: aprilolson
manager: AnnBe
ms.date: 08/16/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerCalendar, LedgerPeriodModuleAccessControlUpdate, SysLookupPicklist, LedgerFiscalCalendarPeriodStatus
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4db0f68a22f9129041c7a7c081f397c34c2b07eb
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5254445"
---
# <a name="mass-financial-period-close"></a><span data-ttu-id="f1f5b-103">Lukke masseregnskapsperiode</span><span class="sxs-lookup"><span data-stu-id="f1f5b-103">Mass financial period close</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f1f5b-104">Dette emnet viser hvordan du setter en periode på vent eller permanent lukker en periode for mer enn en juridisk enhet om gangen.</span><span class="sxs-lookup"><span data-stu-id="f1f5b-104">This topic shows how to place a period on hold or permanently close a period or more than one legal entity at a time.</span></span> <span data-ttu-id="f1f5b-105">I tillegg viser oppgaven hvordan du begrenser brukergruppepostering til spesifikke moduler.</span><span class="sxs-lookup"><span data-stu-id="f1f5b-105">In addition, the task will show how to restrict user group posting to specific modules.</span></span>

1. <span data-ttu-id="f1f5b-106">Gå til **Moduler > Økonomimodul > Lukket periode > Finanskalendere** i navigasjonsruten.</span><span class="sxs-lookup"><span data-stu-id="f1f5b-106">In the navigation pane, go to **Modules > General ledger > Period close > Ledger calendars**.</span></span> <span data-ttu-id="f1f5b-107">Vær oppmerksom på at listen over juridiske enheter som vises, er avhengig av regnskapskalenderen som er valgt på siden.</span><span class="sxs-lookup"><span data-stu-id="f1f5b-107">Note that the list of legal entities displayed is dependent on the fiscal calendar selected on the page.</span></span> <span data-ttu-id="f1f5b-108">Bare juridiske enheter som bruker den valgte regnskapskalenderen, vises.</span><span class="sxs-lookup"><span data-stu-id="f1f5b-108">Only legal entities using the selected fiscal calendar will display.</span></span>
2. <span data-ttu-id="f1f5b-109">Velg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="f1f5b-109">Select **Edit**.</span></span>
3. <span data-ttu-id="f1f5b-110">Velg perioden du vil endre statusen for.</span><span class="sxs-lookup"><span data-stu-id="f1f5b-110">Select the period for which you want to modify the status.</span></span>
4. <span data-ttu-id="f1f5b-111">Velg de juridiske enhetene du vil oppdatere statusen for.</span><span class="sxs-lookup"><span data-stu-id="f1f5b-111">Select the legal entities for which you want to update the status.</span></span> <span data-ttu-id="f1f5b-112">Du kan raskt velge alle juridiske enheter ved merke av øverst til venstre i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="f1f5b-112">You can quickly select all legal entities by selecting the check mark on the upper left side of the grid.</span></span>  
5. <span data-ttu-id="f1f5b-113">Velg **Oppdater modultilgang** for å definere posteringstilgangen til en valgt modul.</span><span class="sxs-lookup"><span data-stu-id="f1f5b-113">Select **Update module access** to define the posting access to a selected module.</span></span> <span data-ttu-id="f1f5b-114">Modulstatusen kan også oppdateres en etter en ved å redigere postene i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="f1f5b-114">The module status can also be updated one-by-one by editing the records in the grid.</span></span> <span data-ttu-id="f1f5b-115">Knappen er nyttig når du vil oppdatere flere poster for juridisk enhet raskt.</span><span class="sxs-lookup"><span data-stu-id="f1f5b-115">The button is useful when you want to quickly update multiple legal entity records.</span></span>  
6. <span data-ttu-id="f1f5b-116">I feltet **Programmodul** velger du modulen som du vil oppdatere statusen for.</span><span class="sxs-lookup"><span data-stu-id="f1f5b-116">In the **Application** module, select the module that you want to update the status.</span></span> <span data-ttu-id="f1f5b-117">Klikk **Velg**.</span><span class="sxs-lookup"><span data-stu-id="f1f5b-117">Click **Select**.</span></span>
7. <span data-ttu-id="f1f5b-118">I **tilgangsnivået** velger du **Alle**, **Ingen** eller en bestemt brukergruppe.</span><span class="sxs-lookup"><span data-stu-id="f1f5b-118">In the **Access** level, select **All**, **None**, or a specific user group.</span></span> <span data-ttu-id="f1f5b-119">Klikk **Velg**.</span><span class="sxs-lookup"><span data-stu-id="f1f5b-119">Click **Select**.</span></span> <span data-ttu-id="f1f5b-120">Alle angir at alle brukere med redigeringstilgang til modulen kan postere hvis perioden er åpen.</span><span class="sxs-lookup"><span data-stu-id="f1f5b-120">All indicates all users with edit access to the module can post if the period is open.</span></span> <span data-ttu-id="f1f5b-121">Ingen angir at brukere ikke kan postere til modulen hvis perioden er åpen.</span><span class="sxs-lookup"><span data-stu-id="f1f5b-121">None indicates that users cannot post to the module if the period is open.</span></span> <span data-ttu-id="f1f5b-122">En bestemt brukergruppe angir bare brukere i gruppen kan postere til modulen hvis perioden er åpen.</span><span class="sxs-lookup"><span data-stu-id="f1f5b-122">A specific user group indicates only users in the group are able to post to the module if the period is open.</span></span>  
8. <span data-ttu-id="f1f5b-123">Velg **Oppdater**.</span><span class="sxs-lookup"><span data-stu-id="f1f5b-123">Select **Update**.</span></span>
9. <span data-ttu-id="f1f5b-124">Velg en annen periode å oppdatere statusen for.</span><span class="sxs-lookup"><span data-stu-id="f1f5b-124">Select another period to update the status.</span></span>
10. <span data-ttu-id="f1f5b-125">Velg de juridiske enhetene du vil oppdatere periodestatusen for.</span><span class="sxs-lookup"><span data-stu-id="f1f5b-125">Select the legal entites for which you want to update the period status.</span></span>
11. <span data-ttu-id="f1f5b-126">Velg **Oppdater periodestatus** og sett statusen til **På vent**, **Åpen** eller **Lukket permanent**.</span><span class="sxs-lookup"><span data-stu-id="f1f5b-126">Select **Update period status** and set the status of **On hold**, **Open**, or **Permanently closed**.</span></span> <span data-ttu-id="f1f5b-127">**Åpen** angir perioden det kan posteres til, gitt at brukeren har tilgang.</span><span class="sxs-lookup"><span data-stu-id="f1f5b-127">**Open** indicates the period can be posted to, provided the user has access.</span></span> <span data-ttu-id="f1f5b-128">**På vent** betyr at perioden ikke kan posteres til, men perioden kan åpnes på nytt.</span><span class="sxs-lookup"><span data-stu-id="f1f5b-128">**On hold** means the period cannot be posted to, but the period can be reopened.</span></span> <span data-ttu-id="f1f5b-129">**Lukket permanent** betyr at perioden er lukket og aldri kan åpnes.</span><span class="sxs-lookup"><span data-stu-id="f1f5b-129">**Permanently closed** means the period is closed and can never be opened.</span></span> <span data-ttu-id="f1f5b-130">Justeringer kan ikke posteres.</span><span class="sxs-lookup"><span data-stu-id="f1f5b-130">Adjustments cannot be posted.</span></span> <span data-ttu-id="f1f5b-131">Vi anbefaler ikke å sette en periode til **Lukket permanent** før alle justeringer og revisjoner er fullført.</span><span class="sxs-lookup"><span data-stu-id="f1f5b-131">We do not recommend setting a period to **Permanently closed** until all adjustments and audits are complete.</span></span>  
12. <span data-ttu-id="f1f5b-132">Velg **Oppdater**.</span><span class="sxs-lookup"><span data-stu-id="f1f5b-132">Select **Update**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]