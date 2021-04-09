---
title: Deaktivere regler i konsekvenskontroll for detaljhandelstransaksjon
description: Dette emnet beskriver funksjonaliteten for deaktivering av regler i konsekvenskontroll for transaksjon i Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 10/15/2019
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: ce2abe7e15773edc3122a1bfdf40f3b830e8790e
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792901"
---
# <a name="disable-rules-in-the-retail-transaction-consistency-checker"></a><span data-ttu-id="41474-103">Deaktivere regler i konsekvenskontroll for detaljhandelstransaksjon</span><span class="sxs-lookup"><span data-stu-id="41474-103">Disable rules in the retail transaction consistency checker</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="41474-104">Forhandlere kan ha forretningsscenarier og -prosesser som er unike for dem.</span><span class="sxs-lookup"><span data-stu-id="41474-104">Retailers can have business scenarios and processes that are unique to them.</span></span> <span data-ttu-id="41474-105">Derfor gjelder ikke alle reglene som er inkludert som standard i konsekvenskontrollen for Commerce-transaksjon, for alle forhandlere.</span><span class="sxs-lookup"><span data-stu-id="41474-105">Therefore, not all the rules that are included by default in the commerce transaction consistency checker are applicable to all retailers.</span></span> <span data-ttu-id="41474-106">Hvis du vil ha plass til forskjeller, tilbyr Microsoft Dynamics 365 Commerce funksjonalitet som kan brukes til å deaktivere reglene som ikke gjelder.</span><span class="sxs-lookup"><span data-stu-id="41474-106">To accommodate differences, Microsoft Dynamics 365 Commerce provides functionality that can be used to disable the rules that aren't applicable.</span></span>

<span data-ttu-id="41474-107">Hvis du vil vise listen over regler som er tilgjengelige i konsekvenskontrollen for transaksjon i miljøet ditt, og i tillegg vise statusen for hver regel, går du til **Retail og Commerce \> Hovedkvarteroppsett \> Parameter \> Commerce-parametere** og velger fanen **Transaksjonsvalidering**.</span><span class="sxs-lookup"><span data-stu-id="41474-107">To view the list of rules that are available in the transaction consistency checker in your environment, and to see the status of each rule, go to **Retail and Commerce \> Headquarters setup \> Parameters \> Commerce parameters**, and select the **Transaction validation** tab.</span></span>

<span data-ttu-id="41474-108">Som standard er statusen for alle regler satt til **Aktivert**.</span><span class="sxs-lookup"><span data-stu-id="41474-108">By default, the status of every rule is set to **Enabled**.</span></span> <span data-ttu-id="41474-109">Derfor brukes alle reglene til å validere transaksjoner før de hentes inn i handelsutdragene.</span><span class="sxs-lookup"><span data-stu-id="41474-109">Therefore, all the rules are used to validate transactions before they are pulled into the commerce statements.</span></span> <span data-ttu-id="41474-110">Hvis du vil deaktivere en regel, endrer du statusen til **Deaktivert**.</span><span class="sxs-lookup"><span data-stu-id="41474-110">To disable a rule, change its status to **Disabled**.</span></span> <span data-ttu-id="41474-111">Deaktiverte regler tas ikke med når transaksjoner valideres under prosessen for beregning av utdrag.</span><span class="sxs-lookup"><span data-stu-id="41474-111">Disabled rules aren't considered when transactions are validated during the statement calculation process.</span></span>

<span data-ttu-id="41474-112">Hvis du vil omgå hele valideringsprosessen, uavhengig av reglene som er aktivert, går du til **Retail og Commerce \> Hovedkvarteroppsett \> Parametere \> Commerce-parametere**, og deretter setter du verdien for alternativet **Deaktiver konsekvenskontroll for Commerce-transaksjoner** i fanen **Transaksjonsvalidering** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="41474-112">To bypass the whole validation process, regardless of the rules that are enabled, go to **Retail and Commerce \> Headquarters setup \> Parameters \> Commerce parameters**, and then, on the **Transaction validation** tab, set the **Disable consistency checker for Commerce transactions** option to **Yes**.</span></span> <span data-ttu-id="41474-113">Når dette alternativet er satt til **Nei**, kan det ikke settes tilbake til **Ja** fra brukergrensesnittet.</span><span class="sxs-lookup"><span data-stu-id="41474-113">After this option is set to **No**, it can't be set back to **Yes** from the user interface (UI).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]