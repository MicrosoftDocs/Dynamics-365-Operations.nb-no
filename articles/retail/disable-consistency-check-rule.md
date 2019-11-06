---
title: Deaktiver regler i konsekvenskontroll for detaljhandelstransaksjon
description: Dette emnet beskriver funksjonaliteten for regler for deaktivering av konsekvenskontroll for detaljhandelstransaksjon i Microsoft Dynamics 365 Retail.
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
ms.openlocfilehash: 4bf8df2fb9f8f5c33ceb13eb012fb6879f81ec66
ms.sourcegitcommit: bdbca89bd9b328c282ebfb681f75b8f1ed96e7a8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/14/2019
ms.locfileid: "2586303"
---
# <a name="disable-rules-in-the-retail-transaction-consistency-checker"></a><span data-ttu-id="a1fe7-103">Deaktiver regler i konsekvenskontroll for detaljhandelstransaksjon</span><span class="sxs-lookup"><span data-stu-id="a1fe7-103">Disable rules in the retail transaction consistency checker</span></span> 

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="a1fe7-104">Forhandlere kan ha forretningsscenarier og -prosesser som er unike for dem.</span><span class="sxs-lookup"><span data-stu-id="a1fe7-104">Retailers can have business scenarios and processes that are unique to them.</span></span> <span data-ttu-id="a1fe7-105">Derfor gjelder ikke alle reglene som er inkludert som standard i konsekvenskontrollen for detaljhandelstransaksjon, for alle forhandlere.</span><span class="sxs-lookup"><span data-stu-id="a1fe7-105">Therefore, not all the rules that are included by default in the retail transaction consistency checker are applicable to all retailers.</span></span> <span data-ttu-id="a1fe7-106">Hvis du vil ha plass til forskjeller, tilbyr Microsoft Dynamics 365 Retail funksjonalitet som kan brukes til å deaktivere reglene som ikke gjelder.</span><span class="sxs-lookup"><span data-stu-id="a1fe7-106">To accommodate differences, Microsoft Dynamics 365 Retail provides functionality that can be used to disable the rules that aren't applicable.</span></span>

<span data-ttu-id="a1fe7-107">Hvis du vil vise listen over regler som er tilgjengelige i konsekvenskontrollen for detaljhandelstransaksjon i miljøet ditt, og i tillegg vise statusen for hver regel, går du til **Detaljhandel \> Hovedkvarteroppsett \> Parameter \> Detaljhandelsparametere** og velger kategorien **Transaksjonsvalidering**.</span><span class="sxs-lookup"><span data-stu-id="a1fe7-107">To view the list of rules that are available in the retail transaction consistency checker in your environment, and to see the status of each rule, go to **Retail \> Headquarters setup \> Parameters \> Retail parameters**, and select the **Transaction validation** tab.</span></span>

<span data-ttu-id="a1fe7-108">Som standard er statusen for alle regler satt til **Aktivert**.</span><span class="sxs-lookup"><span data-stu-id="a1fe7-108">By default, the status of every rule is set to **Enabled**.</span></span> <span data-ttu-id="a1fe7-109">Derfor brukes alle reglene til å validere detaljhandelstransaksjoner før de hentes inn i detaljhandelsutdragene.</span><span class="sxs-lookup"><span data-stu-id="a1fe7-109">Therefore, all the rules are used to validate retail transactions before they are pulled into the retail statements.</span></span> <span data-ttu-id="a1fe7-110">Hvis du vil deaktivere en regel, endrer du statusen til **Deaktivert**.</span><span class="sxs-lookup"><span data-stu-id="a1fe7-110">To disable a rule, change its status to **Disabled**.</span></span> <span data-ttu-id="a1fe7-111">Deaktiverte regler tas ikke med når detaljhandelstransaksjoner valideres under prosessen for beregning av utdrag.</span><span class="sxs-lookup"><span data-stu-id="a1fe7-111">Disabled rules aren't considered when retail transactions are validated during the statement calculation process.</span></span>

<span data-ttu-id="a1fe7-112">Hvis du vil omgå hele valideringsprosessen, uavhengig av reglene som er aktivert, går du til **Detaljhandel \> Hovedkvarteroppsett \> Parametere \> Detaljhandelsparametere**, og deretter setter du verdien for alternativet **Deaktiver konsekvenskontroll for detaljhandelstransaksjoner** i kategorien **Transaksjonsvalidering** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="a1fe7-112">To bypass the whole validation process, regardless of the rules that are enabled, go to **Retail \> Headquarters setup \> Parameters \> Retail parameters**, and then, on the **Transaction validation** tab, set the **Disable consistency checker for Retail transactions** option to **Yes**.</span></span> <span data-ttu-id="a1fe7-113">Når dette alternativet er satt til **Nei**, kan det ikke settes tilbake til **Ja** fra brukergrensesnittet.</span><span class="sxs-lookup"><span data-stu-id="a1fe7-113">After this option is set to **No**, it can't be set back to **Yes** from the user interface (UI).</span></span>
