---
title: Konserninterne utgifter
description: En arbeidstaker som er ansatt av en juridisk enhet i en organisasjon kan utføre arbeid for en annen juridisk enhet i samme organisasjon. I denne situasjonen kan du bruke den konserninterne kostnadsfunksjonen til å tildele arbeidstakers utgifter til den juridiske enheten som arbeidet ble utført for.
author: ShylaThompson
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0967f23e4e1f8e0431c55d4d54554e7e90e2451c
ms.sourcegitcommit: 07e425707eb20730f10246a27799f4deeef93f97
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/21/2020
ms.locfileid: "3390890"
---
# <a name="intercompany-expenses"></a><span data-ttu-id="170d1-104">Konserninterne utgifter</span><span class="sxs-lookup"><span data-stu-id="170d1-104">Intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="170d1-105">En arbeidstaker som er ansatt av en juridisk enhet i en organisasjon kan utføre arbeid for en annen juridisk enhet i samme organisasjon.</span><span class="sxs-lookup"><span data-stu-id="170d1-105">A worker who is employed by one legal entity in an organization might perform work for another legal entity in the same organization.</span></span> <span data-ttu-id="170d1-106">I denne situasjonen kan du bruke den konserninterne kostnadsfunksjonen til å tildele arbeidstakers utgifter til den juridiske enheten som arbeidet ble utført for.</span><span class="sxs-lookup"><span data-stu-id="170d1-106">In this situation, you can use the intercompany expense feature to assign the worker’s expenses to the legal entity for which the work was performed.</span></span> <span data-ttu-id="170d1-107">Den juridiske enheten som benytter arbeidstakeren kalles den utlånende juridiske enheten.</span><span class="sxs-lookup"><span data-stu-id="170d1-107">The legal entity that employs the worker is called the loaning legal entity.</span></span> <span data-ttu-id="170d1-108">Den juridiske enheten som påføres utgifter for arbeidstakeren, kalles den lånende juridiske enheten.</span><span class="sxs-lookup"><span data-stu-id="170d1-108">The legal entity for which the worker incurs expenses is called the borrowing legal entity.</span></span> 

<span data-ttu-id="170d1-109">Før en arbeidstaker kan opprette og sende utgifter for arbeid som utføres for en annen juridisk enhet, i den utlånende juridiske enheten, gå til siden for **Administrer kostnadsparametere** og velg alternativet **Tillatt konserninterne kostnadslinjer**.</span><span class="sxs-lookup"><span data-stu-id="170d1-109">Before a worker can create and submit expenses for work that is performed for a different legal entity, in the loaning legal entity, on the **Expense management parameters** page, select the **Allow intercompany expense lines** option.</span></span> 

## <a name="tax-posting-for-intercompany-expenses"></a><span data-ttu-id="170d1-110">Avgiftspostering for konserninterne utgifter</span><span class="sxs-lookup"><span data-stu-id="170d1-110">Tax posting for intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="170d1-111">Hvis du vil bruke mva-grupper som er tilknyttet den juridiske enheten som låner ut (kilde), i stedet for den juridiske enheten som låner (mål) i reiseregningsrapporten, må du konfigurere denne i dette mva-oppsettet for økonomimodulen.</span><span class="sxs-lookup"><span data-stu-id="170d1-111">If you want to use tax groups that are associated with the loaning (source) legal entity instead of the borrowing (destination) legal entity in your expense report, you will need to configure this in the General ledger sales tax set up.</span></span> <span data-ttu-id="170d1-112">Når parameteren for økonomimodulen, **Juridisk enhet for konsernintern mva-postering** er satt til **Kilde** og **Bruk avgiftsregler for merverdiavgift** er satt til **Nei**, brukes mva-kombinasjonen for den juridiske enheten som låner ut.</span><span class="sxs-lookup"><span data-stu-id="170d1-112">When the General ledger parameter, **Legal entity for intercompany tax posting** is set to **Source** and **Apply sales tax taxation rules** is set to **No**, the tax combination for the loaning legal entity will be used.</span></span> <span data-ttu-id="170d1-113">Når den samme parameteren er satt til **Mål**, brukes mva-kombinasjonen for den juridiske enheten som låner.</span><span class="sxs-lookup"><span data-stu-id="170d1-113">When the same parameter is set to **Destination**, the tax combination for borrowing legal entity will be used.</span></span> <span data-ttu-id="170d1-114">Når det gjelder juridiske enheter i USA når parameteren er satt til **Kilde**, må også feltet **Innkommende merverdiavgift** også være konfigurert på siden **Finansposteringsgrupper**.</span><span class="sxs-lookup"><span data-stu-id="170d1-114">For legal entities in the United States, when the parameter is set to **Source**, the **Sales tax receivable** field must also be configured on the new **Ledger posting groups** page.</span></span> <span data-ttu-id="170d1-115">Regnskapsmotoren bruker informasjonen fra dette feltet for mva-relatert regnskapspost.</span><span class="sxs-lookup"><span data-stu-id="170d1-115">The accounting engine will use the information from this field for tax related accounting entry.</span></span>   
<span data-ttu-id="170d1-116">Virkemåten er konsekvent for utgiftslinjer som er postert med eller uten et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="170d1-116">The behavior is consistent for expense lines posted with or without a project.</span></span>  
