---
title: Arbeid kan ikke avbrytes på grunn av statusen
description: Arbeid kan ikke avbrytes på grunn av statusen
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
ms.openlocfilehash: 60b4da44ca5e6790302e0797640317cef8493db7
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924261"
---
# <a name="work-cant-be-canceled-because-of-its-status"></a><span data-ttu-id="862a0-103">Arbeid kan ikke avbrytes på grunn av statusen</span><span class="sxs-lookup"><span data-stu-id="862a0-103">Work can't be canceled because of its status</span></span>

<span data-ttu-id="862a0-104">Feilkode: WAX2190</span><span class="sxs-lookup"><span data-stu-id="862a0-104">Error code: WAX2190</span></span>

## <a name="symptoms"></a><span data-ttu-id="862a0-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="862a0-105">Symptoms</span></span>

<span data-ttu-id="862a0-106">Systemet viser følgende feilmelding:</span><span class="sxs-lookup"><span data-stu-id="862a0-106">The system shows the following error message:</span></span>

> <span data-ttu-id="862a0-107">Du kan ikke avbryte arbeidet %1 fordi det har statusen %2.</span><span class="sxs-lookup"><span data-stu-id="862a0-107">You cannot cancel work %1 because it has a status of %2.</span></span>

## <a name="cause"></a><span data-ttu-id="862a0-108">Årsak</span><span class="sxs-lookup"><span data-stu-id="862a0-108">Cause</span></span>

<span data-ttu-id="862a0-109">Arbeidet kan ikke avbrytes med gjeldende status.</span><span class="sxs-lookup"><span data-stu-id="862a0-109">The work can't be canceled in its current state.</span></span>

<span data-ttu-id="862a0-110">Arbeidshodet eller arbeidslinjene har ikke den forventede **Arbeidsstatus**-verdien.</span><span class="sxs-lookup"><span data-stu-id="862a0-110">The work header or work lines don't have the expected **Work status** value.</span></span> <span data-ttu-id="862a0-111">Feltet **Arbeidsstatus** på arbeidshodehodet er ikke satt til *Åpen* eller *Pågår*.</span><span class="sxs-lookup"><span data-stu-id="862a0-111">The **Work status** field on the work header isn't set to *Open* or *In progress*.</span></span>

## <a name="resolution"></a><span data-ttu-id="862a0-112">Oppløsning</span><span class="sxs-lookup"><span data-stu-id="862a0-112">Resolution</span></span>

<span data-ttu-id="862a0-113">Følg denne fremgangsmåten for å avbryte arbeidet.</span><span class="sxs-lookup"><span data-stu-id="862a0-113">To cancel the work, follow these steps.</span></span>

1. <span data-ttu-id="862a0-114">Gå til **Lagerstyring \> Periodiske oppgaver \> Rydd opp \> Avbryt arbeid**.</span><span class="sxs-lookup"><span data-stu-id="862a0-114">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="862a0-115">Angi IDen for arbeidet du vil avbryte, i **Arbeids-ID**-feltet.</span><span class="sxs-lookup"><span data-stu-id="862a0-115">In the **Work ID** field, specify the ID of the work that you want to cancel.</span></span>
1. <span data-ttu-id="862a0-116">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="862a0-116">Select **OK**.</span></span>
1. <span data-ttu-id="862a0-117">Velg **Ja** for å bekrefte at du vil avbryte arbeidet.</span><span class="sxs-lookup"><span data-stu-id="862a0-117">Select **Yes** to confirm that you want to cancel the work.</span></span>

<span data-ttu-id="862a0-118">For mer informasjon, se [Avbryte lagerarbeid for unntaksbehandling](../../warehousing/cancel-warehouse-work.md).</span><span class="sxs-lookup"><span data-stu-id="862a0-118">For more information, see [Cancel warehouse work for exception handling](../../warehousing/cancel-warehouse-work.md).</span></span>
