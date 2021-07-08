---
title: Valgt formelnummer er ikke godkjent for en partiordre
description: Når du prøver å autorisere en planlagt bestilling, får du en feilmelding som angir at det valgte formelnummeret ikke er godkjent for en partiordre.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 4f993c92ca0a2f8f79e4b0e0eda43904529163f8
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294142"
---
# <a name="selected-formula-number-isnt-approved-for-a-batch-order"></a><span data-ttu-id="2611d-103">Valgt formelnummer er ikke godkjent for en partiordre</span><span class="sxs-lookup"><span data-stu-id="2611d-103">Selected formula number isn't approved for a batch order</span></span>

<span data-ttu-id="2611d-104">Feilkode: PRO2614</span><span class="sxs-lookup"><span data-stu-id="2611d-104">Error code: PRO2614</span></span>

## <a name="symptoms"></a><span data-ttu-id="2611d-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="2611d-105">Symptoms</span></span>

<span data-ttu-id="2611d-106">Når du prøver å autorisere en planlagt ordre, mottar du følgende feilmelding:</span><span class="sxs-lookup"><span data-stu-id="2611d-106">When you try to firm a planned order, you receive the following error message:</span></span>

> <span data-ttu-id="2611d-107">Det valgte formelnummeret er ikke godkjent for en partiordre.</span><span class="sxs-lookup"><span data-stu-id="2611d-107">The selected formula number is not approved for a batch order.</span></span>

## <a name="cause"></a><span data-ttu-id="2611d-108">Årsak</span><span class="sxs-lookup"><span data-stu-id="2611d-108">Cause</span></span>

<span data-ttu-id="2611d-109">Systemet validerer autoriseringsoperasjonen for å sikre at en godkjent formel er tilgjengelig for den aktive varen.</span><span class="sxs-lookup"><span data-stu-id="2611d-109">The system validates the firming operation to make sure that an approved formula is available for the active item.</span></span> <span data-ttu-id="2611d-110">Du må sannsynligvis godkjenne formelen.</span><span class="sxs-lookup"><span data-stu-id="2611d-110">You must probably approve the formula.</span></span>

## <a name="resolution"></a><span data-ttu-id="2611d-111">Løsning</span><span class="sxs-lookup"><span data-stu-id="2611d-111">Resolution</span></span>

<span data-ttu-id="2611d-112">For å godkjenne en formel, følg denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="2611d-112">To approve a formula, follow these steps.</span></span>

1. <span data-ttu-id="2611d-113">Gå til **Behandling av produktinformasjon \> Stykklister og formler \> Formler**.</span><span class="sxs-lookup"><span data-stu-id="2611d-113">Go to **Product information management \> Bills of materials and formulas \> Formulas**.</span></span>
1. <span data-ttu-id="2611d-114">Velg relevant formel.</span><span class="sxs-lookup"><span data-stu-id="2611d-114">Select the relevant formula.</span></span>
1. <span data-ttu-id="2611d-115">I handlingsruten, i kategorien **Formel**, i **Oppretthold**-gruppen, velger du **Godkjenn formel**.</span><span class="sxs-lookup"><span data-stu-id="2611d-115">On the Action Pane, on the **Formula** tab, in the **Maintain** group, select **Approve formula**.</span></span>
1. <span data-ttu-id="2611d-116">Velg dialogboksen **Godkjenn stykkliste eller formel**, og velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="2611d-116">In the **Approve BOM or formula** dialog box, select an approver, and then select **OK**.</span></span>
