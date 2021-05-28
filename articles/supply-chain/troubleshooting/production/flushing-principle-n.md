---
title: Trekkprinsippinnstillinger på stykklistelinjer overholdes ikke
description: Trekkprinsippinnstillinger på stykklistelinjer overholdes ikke.
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: PurchTable,ProdParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 84a84728016119a2a02f59f6903171afbceb48e7
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026781"
---
# <a name="flushing-principle-settings-on-bom-lines-arent-respected"></a><span data-ttu-id="6c49b-103">Trekkprinsippinnstillinger på stykklistelinjer overholdes ikke</span><span class="sxs-lookup"><span data-stu-id="6c49b-103">Flushing principle settings on BOM lines aren't respected</span></span>

<span data-ttu-id="6c49b-104">KB-nummer: 4612725</span><span class="sxs-lookup"><span data-stu-id="6c49b-104">KB number: 4612725</span></span>

## <a name="symptoms"></a><span data-ttu-id="6c49b-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="6c49b-105">Symptoms</span></span>

<span data-ttu-id="6c49b-106">Dette problemet oppstår når feltet **Automatisk stykklisteforbruk** i kategorien **Automatisk oppdatering** på siden **Parametere for produksjonskontroll** er angitt til *Trekkprinsipp*.</span><span class="sxs-lookup"><span data-stu-id="6c49b-106">This issue occurs when the **Automatic BOM consumption** field on the **Automatic update** tab of the **Production control parameters** page is set to *Flushing principle*.</span></span> <span data-ttu-id="6c49b-107">Denne innstillingen angir at alle stykklistelinjer automatisk skal forbrukes når en bestilling mottas.</span><span class="sxs-lookup"><span data-stu-id="6c49b-107">This setting indicates that all bill of materials (BOM) lines should automatically be consumed when a purchase order is received.</span></span> <span data-ttu-id="6c49b-108">Hvis **Trekkprinsipp**-feltet på stykklistelinjer er uttrykkelig angitt til *Manuell*, kan du forvente at stykklistelinjene ikke forbrukes automatisk.</span><span class="sxs-lookup"><span data-stu-id="6c49b-108">If the **Flushing principle** field on BOM lines is explicitly set to *Manual*, you might expect that the BOM lines won't automatically be consumed.</span></span> <span data-ttu-id="6c49b-109">Når dette problemet oppstår, blir imidlertid stykklistelinjer der **Trekkprinsipp**-feltet er satt til *Manuell*, automatisk forbrukt.</span><span class="sxs-lookup"><span data-stu-id="6c49b-109">However, when this issue occurs, BOM lines where the **Flushing principle** field is set to *Manual* are automatically consumed anyway.</span></span>

## <a name="resolution"></a><span data-ttu-id="6c49b-110">Oppløsning</span><span class="sxs-lookup"><span data-stu-id="6c49b-110">Resolution</span></span>

<span data-ttu-id="6c49b-111">Hvis du har dette problemet, kan det hende at produksjonskontrollparameterne er satt opp til å overstyre **Trekkprinsipp**-innstillinger på stykklistelinjer.</span><span class="sxs-lookup"><span data-stu-id="6c49b-111">If you're experiencing this issue, your production control parameters might be set up to override the **Flushing principle** setting on BOM lines.</span></span> <span data-ttu-id="6c49b-112">Kontroller verdien i feltet **Automatisk stykklisteforbruk** på siden **Produksjonskontrollparametere** i kategorien **Automatisk oppdatering**.</span><span class="sxs-lookup"><span data-stu-id="6c49b-112">On the **Production control parameters** page, on the **Automatic update** tab, check the value of the **Automatic BOM consumption** field.</span></span> <span data-ttu-id="6c49b-113">Hvis den er satt til *Alltid*, vil systemet ignorere innstillingen for **Trekkprinsipp** på alle stykklistelinjer, og linjene tømmes alltid.</span><span class="sxs-lookup"><span data-stu-id="6c49b-113">If it's set to *Always*, the system will disregard the **Flushing principle** setting on all BOM lines and will always flush the lines.</span></span> <span data-ttu-id="6c49b-114">Hvis du vil at systemet skal overholde **Trekkprinsipp**-innstillingen på stykklistelinjer, endrer du verdien i feltet **Automatisk stykklisteforbruk** til *Trekkprinsipp*.</span><span class="sxs-lookup"><span data-stu-id="6c49b-114">To make the system respect the **Flushing principle** setting on BOM lines, change the value of the **Automatic BOM consumption** field to *Flushing principle*.</span></span>
