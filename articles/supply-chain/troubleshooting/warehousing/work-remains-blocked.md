---
title: Arbeid gjenstår å blokkere
description: Arbeid gjenstår å blokkere
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTableListPage_WHSWorkUnblocking
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f85364d1ecfadc36b26c3395ab4402d3cb3b1603
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924136"
---
# <a name="work-remains-blocked"></a><span data-ttu-id="24958-103">Arbeid gjenstår å blokkere</span><span class="sxs-lookup"><span data-stu-id="24958-103">Work remains blocked</span></span>

<span data-ttu-id="24958-104">Feilkode: WHSWorkBlockingExecutingWaveReason_ErrorMessage</span><span class="sxs-lookup"><span data-stu-id="24958-104">Error code: WHSWorkBlockingExecutingWaveReason_ErrorMessage</span></span>

## <a name="symptoms"></a><span data-ttu-id="24958-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="24958-105">Symptoms</span></span>

<span data-ttu-id="24958-106">Systemet viser følgende feilmelding:</span><span class="sxs-lookup"><span data-stu-id="24958-106">The system shows the following error message:</span></span>

> <span data-ttu-id="24958-107">Arbeidet %1 er fortsatt blokkert fordi den relaterte bølgen %2 har statusen %3.</span><span class="sxs-lookup"><span data-stu-id="24958-107">Work %1 remains blocked because the related wave %2 has status %3.</span></span>

## <a name="cause"></a><span data-ttu-id="24958-108">Årsak</span><span class="sxs-lookup"><span data-stu-id="24958-108">Cause</span></span>

<span data-ttu-id="24958-109">Arbeidet behandles i øyeblikket i en bølge, og blokkeringen kan ikke oppheves, som angitt ved en av følgende betingelser:</span><span class="sxs-lookup"><span data-stu-id="24958-109">The work is currently being processed on a wave and can't be unblocked, as indicated by one of the following conditions:</span></span>

- <span data-ttu-id="24958-110">I kategorien **Blokkeringsårsaker** er feltet **Arbeidsblokkeringsårsak** for en eller flere linjer satt til *Behandler bølge*.</span><span class="sxs-lookup"><span data-stu-id="24958-110">On the **Blocking reasons** tab, the **Work blocking reason** field for one or more lines is set to *Processing wave*.</span></span>
- <span data-ttu-id="24958-111">Når du velger **Bølge** i gruppen **Beslektet informasjon** i kategorien **Beslektet informasjon** i handlingsruten, er feltet **Bølgestatus** satt til *Behandling*.</span><span class="sxs-lookup"><span data-stu-id="24958-111">When you select **Wave** in the **Related information** group on the **Related information** tab of the Action Pane, the **Wave status** field is set to *Processing*.</span></span>

## <a name="resolution"></a><span data-ttu-id="24958-112">Oppløsning</span><span class="sxs-lookup"><span data-stu-id="24958-112">Resolution</span></span>

<span data-ttu-id="24958-113">Velg **Bølge** i gruppen **Beslektet informasjon** i fanen **Beslektet informasjon** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="24958-113">On the Action Pane, on the **Related information** tab, in the **Related information** group, select **Wave**.</span></span> <span data-ttu-id="24958-114">På **Bølger**-siden i handlingsruten i kategorien **Bølge** i **Bølge**-gruppen velger du **Rydd opp bølgedata**.</span><span class="sxs-lookup"><span data-stu-id="24958-114">Then, on the **Waves** page, on the Action Pane, on the **Wave** tab, in the **Wave** group, select **Cleanup wave data**.</span></span>

## <a name="workaround"></a><span data-ttu-id="24958-115">Løsning</span><span class="sxs-lookup"><span data-stu-id="24958-115">Workaround</span></span>

<span data-ttu-id="24958-116">Hvis de forrige trinnene ikke løste problemet, kan du avbryte arbeidet ved å følge disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="24958-116">If the previous steps didn't fix the issue, you can cancel the work by following these steps.</span></span>

1. <span data-ttu-id="24958-117">Gå til **Lagerstyring \> Periodiske oppgaver \> Rydd opp \> Avbryt arbeid**.</span><span class="sxs-lookup"><span data-stu-id="24958-117">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="24958-118">I **Arbeids-ID**-feltet angir du IDen for arbeidet du vil avbryte, og som for øyeblikket har **Arbeidstatus**-verdien *Åpen*, *Pågår*, *Avbrutt*, *Kombinert* eller *Lukket*.</span><span class="sxs-lookup"><span data-stu-id="24958-118">In the **Work ID** field, specify the ID of the work that you want to cancel, and that currently has a **Work status** value of *Open*, *In progress*, *Canceled*, *Combined*, or *Closed*.</span></span>
1. <span data-ttu-id="24958-119">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="24958-119">Select **OK**.</span></span>
1. <span data-ttu-id="24958-120">Velg **Ja** for å bekrefte at du vil avbryte arbeidet.</span><span class="sxs-lookup"><span data-stu-id="24958-120">Select **Yes** to confirm that you want to cancel the work.</span></span>

<span data-ttu-id="24958-121">For mer informasjon, se [Avbryte lagerarbeid for unntaksbehandling](../../warehousing/cancel-warehouse-work.md).</span><span class="sxs-lookup"><span data-stu-id="24958-121">For more information, see [Cancel warehouse work for exception handling](../../warehousing/cancel-warehouse-work.md).</span></span>
