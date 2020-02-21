---
title: Deaktiver regler i konsekvenskontroll for detaljhandelstransaksjon
description: Dette emnet beskriver funksjonaliteten for regler for deaktivering av konsekvenskontroll for detaljhandelstransaksjon i Microsoft Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 10/15/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: b11b901fafc3907e9d3cae5cd554cc9a868a414c
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004349"
---
# <a name="disable-rules-in-the-retail-transaction-consistency-checker"></a><span data-ttu-id="c3718-103">Deaktiver regler i konsekvenskontroll for detaljhandelstransaksjon</span><span class="sxs-lookup"><span data-stu-id="c3718-103">Disable rules in the retail transaction consistency checker</span></span> 

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="c3718-104">Forhandlere kan ha forretningsscenarier og -prosesser som er unike for dem.</span><span class="sxs-lookup"><span data-stu-id="c3718-104">Retailers can have business scenarios and processes that are unique to them.</span></span> <span data-ttu-id="c3718-105">Derfor gjelder ikke alle reglene som er inkludert som standard i konsekvenskontrollen for Commerce-transaksjon, for alle forhandlere.</span><span class="sxs-lookup"><span data-stu-id="c3718-105">Therefore, not all the rules that are included by default in the commerce transaction consistency checker are applicable to all retailers.</span></span> <span data-ttu-id="c3718-106">Hvis du vil ha plass til forskjeller, tilbyr Microsoft Dynamics 365 Commerce funksjonalitet som kan brukes til å deaktivere reglene som ikke gjelder.</span><span class="sxs-lookup"><span data-stu-id="c3718-106">To accommodate differences, Microsoft Dynamics 365 Commerce provides functionality that can be used to disable the rules that aren't applicable.</span></span>

<span data-ttu-id="c3718-107">Hvis du vil vise listen over regler som er tilgjengelige i konsekvenskontrollen for transaksjon i miljøet ditt, og i tillegg vise statusen for hver regel, går du til **Detaljhandel og handel \> Hovedkvarteroppsett \> Parameter \> Handelsparametere** og velger kategorien **Transaksjonsvalidering**.</span><span class="sxs-lookup"><span data-stu-id="c3718-107">To view the list of rules that are available in the transaction consistency checker in your environment, and to see the status of each rule, go to **Retail and Commerce \> Headquarters setup \> Parameters \> Commerce parameters**, and select the **Transaction validation** tab.</span></span>

<span data-ttu-id="c3718-108">Som standard er statusen for alle regler satt til **Aktivert**.</span><span class="sxs-lookup"><span data-stu-id="c3718-108">By default, the status of every rule is set to **Enabled**.</span></span> <span data-ttu-id="c3718-109">Derfor brukes alle reglene til å validere transaksjoner før de hentes inn i handelsutdragene.</span><span class="sxs-lookup"><span data-stu-id="c3718-109">Therefore, all the rules are used to validate transactions before they are pulled into the commerce statements.</span></span> <span data-ttu-id="c3718-110">Hvis du vil deaktivere en regel, endrer du statusen til **Deaktivert**.</span><span class="sxs-lookup"><span data-stu-id="c3718-110">To disable a rule, change its status to **Disabled**.</span></span> <span data-ttu-id="c3718-111">Deaktiverte regler tas ikke med når transaksjoner valideres under prosessen for beregning av utdrag.</span><span class="sxs-lookup"><span data-stu-id="c3718-111">Disabled rules aren't considered when transactions are validated during the statement calculation process.</span></span>

<span data-ttu-id="c3718-112">Hvis du vil omgå hele valideringsprosessen, uavhengig av reglene som er aktivert, går du til **Detaljhandel og handel \> Hovedkvarteroppsett \> Parametere \> Handelsparametere**, og deretter setter du verdien for alternativet **Deaktiver konsekvenskontroll for Commerce-transaksjoner** i kategorien **Transaksjonsvalidering** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="c3718-112">To bypass the whole validation process, regardless of the rules that are enabled, go to **Retail and Commerce \> Headquarters setup \> Parameters \> Commerce parameters**, and then, on the **Transaction validation** tab, set the **Disable consistency checker for Commerce transactions** option to **Yes**.</span></span> <span data-ttu-id="c3718-113">Når dette alternativet er satt til **Nei**, kan det ikke settes tilbake til **Ja** fra brukergrensesnittet.</span><span class="sxs-lookup"><span data-stu-id="c3718-113">After this option is set to **No**, it can't be set back to **Yes** from the user interface (UI).</span></span>
