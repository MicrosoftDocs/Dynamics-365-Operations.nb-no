---
title: Siste lukkede arbeidslinje må være av typen Plasser
description: Siste lukkede arbeidslinje må være av typen Plasser
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkCancel, WHSWorkTableListPage_WHSWorkCancel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: a5b78154b51252b3ac96ba28c254e823caf87019
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924381"
---
# <a name="the-last-closed-work-line-must-be-a-put"></a><span data-ttu-id="dcfb9-103">Siste lukkede arbeidslinje må være av typen Plasser</span><span class="sxs-lookup"><span data-stu-id="dcfb9-103">The last closed work line must be a put</span></span>

<span data-ttu-id="dcfb9-104">Feilkode: WAX1285</span><span class="sxs-lookup"><span data-stu-id="dcfb9-104">Error code: WAX1285</span></span>

## <a name="symptoms"></a><span data-ttu-id="dcfb9-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="dcfb9-105">Symptoms</span></span>

<span data-ttu-id="dcfb9-106">Systemet viser følgende feilmelding:</span><span class="sxs-lookup"><span data-stu-id="dcfb9-106">The system shows the following error message:</span></span>

> <span data-ttu-id="dcfb9-107">Siste lukkede arbeidslinje må være av typen Plasser.</span><span class="sxs-lookup"><span data-stu-id="dcfb9-107">The last closed work line must be a put.</span></span>

## <a name="cause"></a><span data-ttu-id="dcfb9-108">Årsak</span><span class="sxs-lookup"><span data-stu-id="dcfb9-108">Cause</span></span>

<span data-ttu-id="dcfb9-109">Arbeidet kan ikke avbrytes med gjeldende status.</span><span class="sxs-lookup"><span data-stu-id="dcfb9-109">The work can't be canceled in its current state.</span></span>

<span data-ttu-id="dcfb9-110">På den siste arbeidslinjen er **Arbeidsstatus**-feltet satt til *Lukket*, men **Arbeidstype**-feltet er satt til *Plasser*.</span><span class="sxs-lookup"><span data-stu-id="dcfb9-110">On the last work line, the **Work status** field is set to *Closed*, but the **Work type** field isn't set to *Put*.</span></span>

## <a name="resolution"></a><span data-ttu-id="dcfb9-111">Oppløsning</span><span class="sxs-lookup"><span data-stu-id="dcfb9-111">Resolution</span></span>

<span data-ttu-id="dcfb9-112">Følg denne fremgangsmåten for å avbryte arbeidet.</span><span class="sxs-lookup"><span data-stu-id="dcfb9-112">To cancel the work, follow these steps.</span></span>

1. <span data-ttu-id="dcfb9-113">Gå til **Lagerstyring \> Periodiske oppgaver \> Rydd opp \> Avbryt arbeid**.</span><span class="sxs-lookup"><span data-stu-id="dcfb9-113">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="dcfb9-114">Angi IDen for arbeidet du vil avbryte, i **Arbeids-ID**-feltet.</span><span class="sxs-lookup"><span data-stu-id="dcfb9-114">In the **Work ID** field, specify the ID of the work that you want to cancel.</span></span>
1. <span data-ttu-id="dcfb9-115">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="dcfb9-115">Select **OK**.</span></span>
1. <span data-ttu-id="dcfb9-116">Velg **Ja** for å bekrefte at du vil avbryte arbeidet.</span><span class="sxs-lookup"><span data-stu-id="dcfb9-116">Select **Yes** to confirm that you want to cancel the work.</span></span>

<span data-ttu-id="dcfb9-117">For mer informasjon, se [Avbryte lagerarbeid for unntaksbehandling](../../warehousing/cancel-warehouse-work.md).</span><span class="sxs-lookup"><span data-stu-id="dcfb9-117">For more information, see [Cancel warehouse work for exception handling](../../warehousing/cancel-warehouse-work.md).</span></span>
