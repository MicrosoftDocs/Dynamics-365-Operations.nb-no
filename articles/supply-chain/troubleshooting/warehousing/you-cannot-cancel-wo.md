---
title: Du kan ikke avbryte arbeid som er på en bruker
description: Du kan ikke avbryte arbeid som er på en bruker
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
ms.openlocfilehash: e5f6912cfb1d5be8e46b7989856af99f8a611c11
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924407"
---
# <a name="you-cant-cancel-work-that-is-on-a-user"></a><span data-ttu-id="ff8dc-103">Du kan ikke avbryte arbeid som er på en bruker</span><span class="sxs-lookup"><span data-stu-id="ff8dc-103">You can't cancel work that is on a user</span></span>

<span data-ttu-id="ff8dc-104">Feilkode: WAX708</span><span class="sxs-lookup"><span data-stu-id="ff8dc-104">Error code: WAX708</span></span>

## <a name="symptoms"></a><span data-ttu-id="ff8dc-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="ff8dc-105">Symptoms</span></span>

<span data-ttu-id="ff8dc-106">Systemet viser følgende feilmelding:</span><span class="sxs-lookup"><span data-stu-id="ff8dc-106">The system shows the following error message:</span></span>

> <span data-ttu-id="ff8dc-107">Du kan ikke avbryte arbeid som er på en bruker.</span><span class="sxs-lookup"><span data-stu-id="ff8dc-107">You cannot cancel work that is on a user.</span></span>

## <a name="cause"></a><span data-ttu-id="ff8dc-108">Årsak</span><span class="sxs-lookup"><span data-stu-id="ff8dc-108">Cause</span></span>

<span data-ttu-id="ff8dc-109">Arbeidet er låst av en bruker og kan ikke avbrytes.</span><span class="sxs-lookup"><span data-stu-id="ff8dc-109">The work is locked by a user and can't be canceled.</span></span> <span data-ttu-id="ff8dc-110">Hvis du vil bekrefte dette, åpner du arbeids-IDen og åpner deretter kategorien **Generelt**. Hvis arbeidet er låst, settes **Arbeidsstatus**-feltet til *Pågår*, og feltet **Sperret av** blir satt til en bruker-ID.</span><span class="sxs-lookup"><span data-stu-id="ff8dc-110">To confirm this, open the work ID and then open the **General** tab. If the work is locked, the **Work status** field will be set to *In progress*, and the **Locked by** field will be set to a user ID.</span></span>

## <a name="resolution"></a><span data-ttu-id="ff8dc-111">Oppløsning</span><span class="sxs-lookup"><span data-stu-id="ff8dc-111">Resolution</span></span>

<span data-ttu-id="ff8dc-112">Følg denne fremgangsmåten for å avbryte arbeidet.</span><span class="sxs-lookup"><span data-stu-id="ff8dc-112">To cancel the work, follow these steps.</span></span>

1. <span data-ttu-id="ff8dc-113">Gå til **Lagerstyring \> Periodiske oppgaver \> Rydd opp \> Avbryt arbeid**.</span><span class="sxs-lookup"><span data-stu-id="ff8dc-113">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="ff8dc-114">Angi IDen for arbeidet du vil avbryte, i **Arbeids-ID**-feltet.</span><span class="sxs-lookup"><span data-stu-id="ff8dc-114">In the **Work ID** field, specify the ID of the work that you want to cancel.</span></span>
1. <span data-ttu-id="ff8dc-115">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="ff8dc-115">Select **OK**.</span></span>
1. <span data-ttu-id="ff8dc-116">Velg **Ja** for å bekrefte at du vil avbryte arbeidet.</span><span class="sxs-lookup"><span data-stu-id="ff8dc-116">Select **Yes** to confirm that you want to cancel the work.</span></span>

<span data-ttu-id="ff8dc-117">For mer informasjon, se [Avbryte lagerarbeid for unntaksbehandling](../../warehousing/cancel-warehouse-work.md).</span><span class="sxs-lookup"><span data-stu-id="ff8dc-117">For more information, see [Cancel warehouse work for exception handling](../../warehousing/cancel-warehouse-work.md).</span></span>
