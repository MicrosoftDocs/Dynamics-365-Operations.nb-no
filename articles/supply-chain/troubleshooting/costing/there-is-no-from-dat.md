---
title: Det er ingen Fra dato-verdi i kategorien Aktive priser på vareprissiden
description: Det er ingen Fra dato-verdi i kategorien Aktive priser på vareprissiden.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventItemPrice
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 3dd13f6a3e5ce3c894e96f420358d337f2e43dba
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026794"
---
# <a name="there-is-no-from-date-value-on-the-active-prices-tab-of-the-item-price-page"></a><span data-ttu-id="ac645-103">Det er ingen Fra dato-verdi i kategorien Aktive priser på vareprissiden</span><span class="sxs-lookup"><span data-stu-id="ac645-103">There is no From date value on the Active prices tab of the Item price page</span></span>

<span data-ttu-id="ac645-104">KB-nummer: 4613548</span><span class="sxs-lookup"><span data-stu-id="ac645-104">KB number: 4613548</span></span>

## <a name="symptoms"></a><span data-ttu-id="ac645-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="ac645-105">Symptoms</span></span>

<span data-ttu-id="ac645-106">Det er ingen **Fra dato**-verdi i kategorien **Aktive priser** på **Varepris**-siden.</span><span class="sxs-lookup"><span data-stu-id="ac645-106">There is no **From date** value on the **Active prices** tab of the **Item price** page.</span></span>

## <a name="resolution"></a><span data-ttu-id="ac645-107">Oppløsning</span><span class="sxs-lookup"><span data-stu-id="ac645-107">Resolution</span></span>

<span data-ttu-id="ac645-108">**Fra dato**-verdien (gyldig-dato) som er definert på den ventende prisen, blir ikke overført til den aktive prisen.</span><span class="sxs-lookup"><span data-stu-id="ac645-108">The **From date** value (effective date) that is set on the pending price isn't transferred to the active price.</span></span>

<span data-ttu-id="ac645-109">Når en varekostnadspost angis først, har den statusen *Ventende* og en beregnet effektiv dato.</span><span class="sxs-lookup"><span data-stu-id="ac645-109">When an item cost record is first entered, it has a status of *Pending* and an intended effective date.</span></span> <span data-ttu-id="ac645-110">Når du aktiverer varekostnadsposten, oppdateres statusen *Aktiv*, og den effektive datoen oppdateres til aktiveringsdatoen.</span><span class="sxs-lookup"><span data-stu-id="ac645-110">When you activate the item cost record, the status is updated to *Active*, and the effective date is updated to the activation date.</span></span> <span data-ttu-id="ac645-111">Derfor er den aktive prisens aktiveringsdato alltid den faktiske datoen for aktiveringen.</span><span class="sxs-lookup"><span data-stu-id="ac645-111">Therefore, the active price's activation date is always the actual date of the activation.</span></span>

<span data-ttu-id="ac645-112">Hvis du vil ha mer informasjon, kan du se [Oversikt over etterkalkuleringsversjoner](../../cost-management/costing-versions.md).</span><span class="sxs-lookup"><span data-stu-id="ac645-112">For more information, see [Costing versions overview](../../cost-management/costing-versions.md).</span></span>
