---
title: Opprette månedlige journaloppføringer i en bunke
description: Dette emnet forklarer hvordan du oppretter journaloppføringer i en bunke for å øke effektiviteten når månedlige leieutgifter registreres.
author: moaamer
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 664001dd6e9da449dec65750da53d58bd27438b4
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5816034"
---
# <a name="create-monthly-journal-entries-in-a-batch"></a><span data-ttu-id="db30c-103">Opprette månedlige journaloppføringer i en bunke</span><span class="sxs-lookup"><span data-stu-id="db30c-103">Create monthly journal entries in a batch</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="db30c-104">Dette emnet forklarer hvordan du oppretter journaloppføringer i en bunke for å øke effektiviteten når månedlige leieutgifter registreres.</span><span class="sxs-lookup"><span data-stu-id="db30c-104">This topic explains how to create journal entries in a batch to help increase efficiency when monthly lease expenses are recorded.</span></span> <span data-ttu-id="db30c-105">Satsvis behandling kan brukes til å opprette journaloppføringer fra flere tidsplaner.</span><span class="sxs-lookup"><span data-stu-id="db30c-105">Batch processing can be used to create journal entries from multiple schedules.</span></span> <span data-ttu-id="db30c-106">Disse journaloppføringene kan omfatte leiebetalinger, nedbetaling av gjeld, nedbetaling av bruksrettseiendel og fullbyrdelseskostnader.</span><span class="sxs-lookup"><span data-stu-id="db30c-106">These journal entries can include lease payments, liability amortization, right-of-use (ROU) asset amortization, and executory cost expenses.</span></span> <span data-ttu-id="db30c-107">Du kan også bruke satsvis behandling til å gjøre den opprinnelige føringen av flere leieavtaler samtidig, eller til å opprette overgangsjusteringer for flere leieavtaler samtidig.</span><span class="sxs-lookup"><span data-stu-id="db30c-107">You can also use batch processing to do the initial recognition of multiple leases at the same time, or to create transition adjustments for multiple leases at the same time.</span></span>

<span data-ttu-id="db30c-108">Hvis du vil konfigurere en satsvis jobb eller behandle betalingsfakturaer, avskrivning eller renter for flere leieavtaler, går du til **Aktivaleie \> Periodisk \> Opprettelse av bunkejournal**.</span><span class="sxs-lookup"><span data-stu-id="db30c-108">To set up a batch job, or to process payment invoices, depreciation, or interest for multiple leases, go to **Asset leasing \> Periodic \> Batch journal creation**.</span></span> <span data-ttu-id="db30c-109">I dialogboksen som vises, kan du velge tidsplanen som journaloppføringene skal opprettes fra.</span><span class="sxs-lookup"><span data-stu-id="db30c-109">In the dialog box that appears, you can select the schedule that the journal entries should be created from.</span></span> <span data-ttu-id="db30c-110">Du kan også angi om bunkeprosessen skal kjøres for bestemte enheter, leiegrupper eller leietablåer.</span><span class="sxs-lookup"><span data-stu-id="db30c-110">You can also specify whether the batch process should be run for specific entities, lease groups, or lease books.</span></span>

> [!NOTE]
> <span data-ttu-id="db30c-111">Påfølgende transaksjoner, for eksempel nedbetalingsplaner for gjeld, betalinger, avskrivning og utgifter, posteres bare etter at den opprinnelige føringen for tilsvarende leieavtaler er postert.</span><span class="sxs-lookup"><span data-stu-id="db30c-111">Subsequent transactions, such as liability amortization schedules, payments, depreciation, and expenses, will be posted only after the initial recognition for corresponding leases is posted.</span></span>
>
> <span data-ttu-id="db30c-112">Journaloppføringene opprettes, men de blir ikke postert før du velger **Kjør**-kommandoen.</span><span class="sxs-lookup"><span data-stu-id="db30c-112">The journal entries are created, but they won't be posted until you select the **Run** command.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]