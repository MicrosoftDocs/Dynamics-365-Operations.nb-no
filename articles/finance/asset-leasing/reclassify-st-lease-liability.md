---
title: Omklassifisere den kortsiktige delen av en leieforpliktelse
description: Dette emnet forklarer hvordan du oppretter en månedlig journaloppføring for å reklassifisere en del av leieforpliktelsen som kortsiktig.
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
ms.openlocfilehash: 9189033987a3072c7122e1a198768d9de6aa2a52
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5254089"
---
# <a name="reclassify-the-short-term-portion-of-lease-liability"></a><span data-ttu-id="96d63-103">Omklassifisere den kortsiktige delen av leieforpliktelse</span><span class="sxs-lookup"><span data-stu-id="96d63-103">Reclassify the short-term portion of lease liability</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="96d63-104">Dette emnet forklarer hvordan du oppretter en månedlig journaloppføring for å reklassifisere en del av leieforpliktelsen som kortsiktig.</span><span class="sxs-lookup"><span data-stu-id="96d63-104">This topic explains how to create a monthly journal entry to reclassify a portion of the lease liability as short-term.</span></span> <span data-ttu-id="96d63-105">Når planen som er valgt i den satsvise prosessen, er **Omklassifisering av kortsiktig leieforpliktelse**, opprettes det en journaloppføring.</span><span class="sxs-lookup"><span data-stu-id="96d63-105">When the schedule that is selected in the batch process is **Short-term lease liability reclass**, a journal entry is created.</span></span> <span data-ttu-id="96d63-106">Denne oppføringen brukes til å postere den gjeldende delen av leieforpliktelsen på den siste dagen i måneden.</span><span class="sxs-lookup"><span data-stu-id="96d63-106">This entry is used to post the current portion of the lease liability on the last day of the month.</span></span> <span data-ttu-id="96d63-107">Samtidig posteres en tilbakeføringspost per den første dagen i neste måned.</span><span class="sxs-lookup"><span data-stu-id="96d63-107">At the same time, a reversal entry is posted as of the first day of the next month.</span></span>

<span data-ttu-id="96d63-108">Den kortsiktige delen av leieforpliktelsen vises i tidsplanen for nedbetalingsplanen for gjeld.</span><span class="sxs-lookup"><span data-stu-id="96d63-108">The short-term portion of the lease liability is shown on the liability amortization schedule.</span></span> <span data-ttu-id="96d63-109">Når journaloppføringen posteres, blir kolonnen for **journal for omklassifisering av gjeld opprettet** tilgjengelig, og journal-IDen blir også fylt ut på tidsplanen.</span><span class="sxs-lookup"><span data-stu-id="96d63-109">When the journal entry is posted, the **Liability reclass journal created** column becomes available, and the journal ID is also filled in on the schedule.</span></span>

<span data-ttu-id="96d63-110">Følg denne fremgangsmåten for å opprette og postere en journaloppføring for omklassifisering av kortsiktig gjeld.</span><span class="sxs-lookup"><span data-stu-id="96d63-110">To create and post the short-term liability reclassification journal entry, follow these steps.</span></span>

1. <span data-ttu-id="96d63-111">Gå til **Aktivaleie \> Periodisk \> Opprettelse av bunkejournal**.</span><span class="sxs-lookup"><span data-stu-id="96d63-111">Go to **Asset leasing \> Periodic \> Batch journal creation**.</span></span>
2. <span data-ttu-id="96d63-112">I dialogboksen **Opprettelse av bunkejournal**, i feltet for **Velg tidsplan**, velger du **Omklassifisering av kortsiktig leieforpliktelse**.</span><span class="sxs-lookup"><span data-stu-id="96d63-112">In the **Batch journal creation** dialog box, in the **Select schedule** field, select **Short-term lease liability reclass**.</span></span>
3. <span data-ttu-id="96d63-113">I feltet **Leiegruppe** velger du en leiegruppe.</span><span class="sxs-lookup"><span data-stu-id="96d63-113">In the **Lease group** field, select a lease group.</span></span> <span data-ttu-id="96d63-114">Du kan også velge tablå-ID i feltet **Tablå-ID**.</span><span class="sxs-lookup"><span data-stu-id="96d63-114">Alternatively, in the **Book ID** field, select the book ID.</span></span>
4. <span data-ttu-id="96d63-115">Aktiver **Post**-parameteren.</span><span class="sxs-lookup"><span data-stu-id="96d63-115">Turn on the **Post** parameter.</span></span> <span data-ttu-id="96d63-116">Hvis posten skal opprettes, men ikke posteres, lar du denne parameteren være deaktivert.</span><span class="sxs-lookup"><span data-stu-id="96d63-116">Alternatively, if the entry should be created but not posted, leave this parameter turned off.</span></span>
5. <span data-ttu-id="96d63-117">Aktiver **Forhåndsvis for postering**-parameter for å vise posten før den posteres.</span><span class="sxs-lookup"><span data-stu-id="96d63-117">Turn on the **Preview before posting** parameter to view the entry before it's posted.</span></span>
6. <span data-ttu-id="96d63-118">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="96d63-118">Select **OK**.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]