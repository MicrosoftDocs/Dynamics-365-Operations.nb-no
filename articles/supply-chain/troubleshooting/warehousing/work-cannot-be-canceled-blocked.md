---
title: Arbeid kan ikke avbrytes fordi det er blokkert
description: Arbeid kan ikke avbrytes fordi det er blokkert
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkCancel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: a7ab4c7263947767164702fb7dd6da7573175253
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924285"
---
# <a name="work-cant-be-canceled-because-its-blocked"></a><span data-ttu-id="0f7a1-103">Arbeid kan ikke avbrytes fordi det er blokkert</span><span class="sxs-lookup"><span data-stu-id="0f7a1-103">Work can't be canceled because it's blocked</span></span>

<span data-ttu-id="0f7a1-104">Feilkode: WHSCancellationOfWorkBlockedByExecutingWave_ErrorMessage</span><span class="sxs-lookup"><span data-stu-id="0f7a1-104">Error code: WHSCancellationOfWorkBlockedByExecutingWave_ErrorMessage</span></span>

## <a name="symptoms"></a><span data-ttu-id="0f7a1-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="0f7a1-105">Symptoms</span></span>

<span data-ttu-id="0f7a1-106">Systemet viser følgende feilmelding:</span><span class="sxs-lookup"><span data-stu-id="0f7a1-106">The system shows the following error message:</span></span>

> <span data-ttu-id="0f7a1-107">Arbeid %1 kan ikke avbrytes fordi det er sperret av årsakstypen %2.</span><span class="sxs-lookup"><span data-stu-id="0f7a1-107">Work %1 cannot be cancelled because it is blocked by reason type %2.</span></span> <span data-ttu-id="0f7a1-108">Blokkeringen av arbeid må oppheves før det kan avbrytes.</span><span class="sxs-lookup"><span data-stu-id="0f7a1-108">The work must be unblocked before it can be cancelled.</span></span>

## <a name="cause"></a><span data-ttu-id="0f7a1-109">Årsak</span><span class="sxs-lookup"><span data-stu-id="0f7a1-109">Cause</span></span>

<span data-ttu-id="0f7a1-110">Arbeidet er blokkert og kan ikke avbrytes.</span><span class="sxs-lookup"><span data-stu-id="0f7a1-110">The work is blocked and can't be canceled.</span></span>

<span data-ttu-id="0f7a1-111">På **Arbeid**-siden i kategorien **Generelt** er alternativet **Blokkert** satt til *Ja*.</span><span class="sxs-lookup"><span data-stu-id="0f7a1-111">On the **Work** page, on the **General** tab, the **Blocked** option is set to *Yes*.</span></span> <span data-ttu-id="0f7a1-112">Denne innstillingen angir at arbeidet er sperret.</span><span class="sxs-lookup"><span data-stu-id="0f7a1-112">This setting indicates that the work is blocked.</span></span> <span data-ttu-id="0f7a1-113">Kategorien **Blokkeringsårsaker** viser hvorfor arbeidet ble blokkert.</span><span class="sxs-lookup"><span data-stu-id="0f7a1-113">The **Blocking reasons** tab shows why the work was blocked.</span></span>

## <a name="resolution"></a><span data-ttu-id="0f7a1-114">Oppløsning</span><span class="sxs-lookup"><span data-stu-id="0f7a1-114">Resolution</span></span>

<span data-ttu-id="0f7a1-115">Hvis du vil fjerne blokkeringen av arbeidet, velger du kategorien **Blokkeringsårsaker**, og deretter følger du ett av disse trinnene:</span><span class="sxs-lookup"><span data-stu-id="0f7a1-115">To unblock the work, select the **Blocking reasons** tab, and then follow one of these steps:</span></span>

- <span data-ttu-id="0f7a1-116">Hvis feltet **Arbeidsblokkeringsårsak** er satt til *Udefinert årsak*: I handlingsruten i kategorien **Arbeid**, i **Arbeid**-gruppen, velger du **Opphev blokkering av arbeid**.</span><span class="sxs-lookup"><span data-stu-id="0f7a1-116">If the **Work blocking reason** field is set to *Undefined reason*: On the Action Pane, on the **Work** tab, in the **Work** group, select **Unblock work**.</span></span>
- <span data-ttu-id="0f7a1-117">Hvis feltet **Arbeidsblokkeringsårsak** er satt til *Behandler bølge*: I handlingsruten i kategorien **Relatert informasjon**, i gruppen **Relatert informasjon**, velger du **Bølge**.</span><span class="sxs-lookup"><span data-stu-id="0f7a1-117">If the **Work blocking reason** field is set to *Processing wave*: On the Action Pane, on the **Related information** tab, in the **Related information** group, select **Wave**.</span></span> <span data-ttu-id="0f7a1-118">På **Bølger**-siden i handlingsruten i kategorien **Bølge** i **Bølge**-gruppen velger du **Rydd opp bølgedata**.</span><span class="sxs-lookup"><span data-stu-id="0f7a1-118">Then, on the **Waves** page, on the Action Pane, on the **Wave** tab, in the **Wave** group, select **Cleanup wave data**.</span></span>

## <a name="workaround"></a><span data-ttu-id="0f7a1-119">Løsning</span><span class="sxs-lookup"><span data-stu-id="0f7a1-119">Workaround</span></span>

<span data-ttu-id="0f7a1-120">Hvis de forrige trinnene ikke løste problemet, kan du avbryte arbeidet ved å følge disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="0f7a1-120">If the previous steps didn't fix the issue, you can cancel the work by following these steps.</span></span>

1. <span data-ttu-id="0f7a1-121">Gå til **Lagerstyring \> Periodiske oppgaver \> Rydd opp \> Avbryt arbeid**.</span><span class="sxs-lookup"><span data-stu-id="0f7a1-121">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="0f7a1-122">I **Arbeids-ID**-feltet angir du IDen for arbeidet du vil avbryte, og som for øyeblikket har **Arbeidstatus**-verdien *Åpen*, *Pågår*, *Avbrutt*, *Kombinert* eller *Lukket*.</span><span class="sxs-lookup"><span data-stu-id="0f7a1-122">In the **Work ID** field, specify the ID of the work that you want to cancel, and that currently has a **Work status** value of *Open*, *In progress*, *Canceled*, *Combined*, or *Closed*.</span></span>
1. <span data-ttu-id="0f7a1-123">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="0f7a1-123">Select **OK**.</span></span>
1. <span data-ttu-id="0f7a1-124">Velg **Ja** for å bekrefte at du vil avbryte arbeidet.</span><span class="sxs-lookup"><span data-stu-id="0f7a1-124">Select **Yes** to confirm that you want to cancel the work.</span></span>

<span data-ttu-id="0f7a1-125">For mer informasjon, se [Avbryte lagerarbeid for unntaksbehandling](../../warehousing/cancel-warehouse-work.md).</span><span class="sxs-lookup"><span data-stu-id="0f7a1-125">For more information, see [Cancel warehouse work for exception handling](../../warehousing/cancel-warehouse-work.md).</span></span>
