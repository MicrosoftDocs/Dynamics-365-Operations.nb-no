---
title: Postere journaloppføringer for overgangsjustering i aktivaleie
description: Dette emnet beskriver funksjonaliteten som lar deg overføre en leieavtaleportefølje til de nye regnskapsstandardene for leieavtaler, Accounting Standards Codification-emne 842 (ASC 842) og International Financial Reporting Standard 16 (IFRS 16).
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 7ed62f52753a6697a7547ada0317041669cf3506
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5207211"
---
# <a name="post-transition-adjustment-journal-entries-in-asset-leasing"></a><span data-ttu-id="c0154-103">Postere journaloppføringer for overgangsjustering i aktivaleie</span><span class="sxs-lookup"><span data-stu-id="c0154-103">Post transition adjustment journal entries in Asset leasing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c0154-104">Dette emnet beskriver funksjonaliteten som lar deg overføre en leieavtaleportefølje til de nye regnskapsstandardene for leieavtaler: Accounting Standards Codification-emne 842 (ASC 842), som er standard i Generally Accepted Accounting Principles i USA (US GAAP), og International Financial Reporting Standard 16 (IFRS 16).</span><span class="sxs-lookup"><span data-stu-id="c0154-104">This topic describes the functionality that lets you transition a lease portfolio to the new lease accounting standards: Accounting Standards Codification Topic 842 (ASC 842), which is the standard in Generally Accepted Accounting Principles in the US (US GAAP), and International Financial Reporting Standard 16 (IFRS 16).</span></span>

<span data-ttu-id="c0154-105">Hvis du vil ha informasjon om hvordan du definerer et tablå for overgangen til de nye standardene, kan du se [Definere leietablåer](set-up-lease-books.md).</span><span class="sxs-lookup"><span data-stu-id="c0154-105">For information about how to set up a book for the transition to the new standards, see [Set up lease books](set-up-lease-books.md).</span></span>

<span data-ttu-id="c0154-106">Når du oppretter en journaloppføring for overgangsjustering, genereres det en journaloppføring.</span><span class="sxs-lookup"><span data-stu-id="c0154-106">When you create a transition adjustment journal entry, a journal entry is generated.</span></span> <span data-ttu-id="c0154-107">Denne oppføringen gjenspeiler balansevirkningen for registrering av leieavtalen i henhold til de nye standardene på denne datoen.</span><span class="sxs-lookup"><span data-stu-id="c0154-107">This entry reflects the balance sheet impact of recording the lease under the new standards on that date.</span></span> <span data-ttu-id="c0154-108">Den relevante aktivakontoen debiteres for det indirekte beløpet på denne datoen, og gjeldskontoen krediteres.</span><span class="sxs-lookup"><span data-stu-id="c0154-108">The appropriate asset account is debited for the carrying amount on that date, and the liability account is credited.</span></span> <span data-ttu-id="c0154-109">Differansen blir enten debitert eller kreditert til opptjente midler.</span><span class="sxs-lookup"><span data-stu-id="c0154-109">The difference is either debited or credited to retained earnings.</span></span>

<span data-ttu-id="c0154-110">Hvis du vil postere en overgangsjustering i samsvar med de nye regnskapsstandardene, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="c0154-110">To post a transition adjustment in compliance with the new accounting standards, follow these steps.</span></span>

1. <span data-ttu-id="c0154-111">På siden **Leiesammendrag** velger du leieavtalen, og deretter velger du **Tablåer**.</span><span class="sxs-lookup"><span data-stu-id="c0154-111">On the **Lease summary** page, select the lease, and then select **Books**.</span></span>
2. <span data-ttu-id="c0154-112">I tablået velger du **Betalingsplan**.</span><span class="sxs-lookup"><span data-stu-id="c0154-112">In the book, select **Payment schedule**.</span></span>
3. <span data-ttu-id="c0154-113">I dialogboksen **Betalingsplan** velger du **Bekreft**.</span><span class="sxs-lookup"><span data-stu-id="c0154-113">In the **Payment schedule** dialog box, select **Confirm**.</span></span> <span data-ttu-id="c0154-114">Lukk deretter dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="c0154-114">Then close the dialog box.</span></span>
4. <span data-ttu-id="c0154-115">Velg **Overgangsjustering**.</span><span class="sxs-lookup"><span data-stu-id="c0154-115">Select **Transition adjustment**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c0154-116">En overgangsjustering kan bare opprettes for leietablåer som er tilordnet til et tablå der feltet for **overgangstablå** er tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="c0154-116">A transition adjustment can be created only for lease books that are assigned to a book where the **Transition book** field is available.</span></span> <span data-ttu-id="c0154-117">Hvis verdien i feltet for **leieavtalestart** er senere enn overgangsdatoen, vil ikke verdien i feltet for **Overgangsjustering** oppdateres.</span><span class="sxs-lookup"><span data-stu-id="c0154-117">If the value in the **Lease commencement** field is later than the transition date, the value in the **Transition adjustment** field won't be updated.</span></span>

5. <span data-ttu-id="c0154-118">Du viser journaloppføringen ved å velge **Journaler for leie av anleggsmidler**.</span><span class="sxs-lookup"><span data-stu-id="c0154-118">To view the journal entry, select **Asset leasing journals**.</span></span>
6. <span data-ttu-id="c0154-119">Velg den nye journalen, og velg deretter **Poster**.</span><span class="sxs-lookup"><span data-stu-id="c0154-119">Select the new journal, and then select **Post**.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]