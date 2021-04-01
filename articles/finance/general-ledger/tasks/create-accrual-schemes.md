---
title: Opprette avsetningsplaner
description: Dette emnet forklarer hvordan du oppretter en avsetningsplan.
author: aprilolson
manager: AnnBe
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerAccrualTable
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5c021f71735e63c270e8f1998d77d4e4abcc5506
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5236704"
---
# <a name="create-accrual-schemes"></a><span data-ttu-id="92c65-103">Opprette avsetningsplaner</span><span class="sxs-lookup"><span data-stu-id="92c65-103">Create accrual schemes</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="92c65-104">Dette emnet forklarer hvordan du oppretter en avsetningsplan.</span><span class="sxs-lookup"><span data-stu-id="92c65-104">This topic explains how to create an accrual scheme.</span></span> <span data-ttu-id="92c65-105">Denne oppgaven bruker demonstrasjonsfirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="92c65-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="92c65-106">Gå til **Navigasjonsrute > Moduler > Økonomimodul > Journaloppsett > Avsetningsplaner**.</span><span class="sxs-lookup"><span data-stu-id="92c65-106">Go to **Navigation pane > Modules > General ledger > Journal setup > Accrual schemes**.</span></span>
2. <span data-ttu-id="92c65-107">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="92c65-107">Select **New**.</span></span>
3. <span data-ttu-id="92c65-108">Skriv inn en verdi i feltet **Avsetningsidentifikasjon**.</span><span class="sxs-lookup"><span data-stu-id="92c65-108">In the **Accrual identification** field, type a value.</span></span>
4. <span data-ttu-id="92c65-109">Skriv inn en verdi i feltet **Beskrivelse av avsetningsplan**.</span><span class="sxs-lookup"><span data-stu-id="92c65-109">In the **Description of accrual scheme** field, type a value.</span></span>
5. <span data-ttu-id="92c65-110">Angi de ønskede verdiene i feltet **Debet**.</span><span class="sxs-lookup"><span data-stu-id="92c65-110">In the **Debit** field, specify the desired values.</span></span> <span data-ttu-id="92c65-111">Hovedkontoen definert vil erstatte debet hovedkontoen i journalbilagslinjen, og den brukes også for tilbakeføring av henvisning basert på finansavsetningstransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="92c65-111">The main account defined will replace the debit main account on the journal voucher line and it will also be used for the reversal of the deferral based on the ledger accrual transactions.</span></span>  
6. <span data-ttu-id="92c65-112">Angi de ønskede verdiene i feltet **Kredit**.</span><span class="sxs-lookup"><span data-stu-id="92c65-112">In the **Credit** field, specify the desired values.</span></span> <span data-ttu-id="92c65-113">Hovedkontoen definert vil erstatte kredit hovedkontoen i journalbilagslinjen, og den brukes også for tilbakeføring av henvisning basert på finansavsetningstransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="92c65-113">The main account defined will replace the credit main account on the journal voucher line and it will also be used for the reversal of the deferral based on the ledger accrual transactions.</span></span>  
7. <span data-ttu-id="92c65-114">I **Bilag**-feltet velger du hvordan bilaget bestemmes når transaksjonene posteres.</span><span class="sxs-lookup"><span data-stu-id="92c65-114">In the **Voucher** field, select how you want the voucher determined when the transactions are posted.</span></span>
8. <span data-ttu-id="92c65-115">Skriv inn en verdi for å beskrive transaksjonene som posteres i **Beskrivelse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="92c65-115">In the **Description** field, type a value to describe the transactions that will be posted.</span></span>
9. <span data-ttu-id="92c65-116">Velg hvor ofte transaksjoner skal skje i **Periodefrekvens**-feltet.</span><span class="sxs-lookup"><span data-stu-id="92c65-116">In the **Period frequency** field, select how often the transactions should occur.</span></span>
10. <span data-ttu-id="92c65-117">Angi et nummer i feltet **Antall forekomster etter periode**.</span><span class="sxs-lookup"><span data-stu-id="92c65-117">In the **Number of occurrences by period** field, enter a number.</span></span>
11. <span data-ttu-id="92c65-118">Velg når transaksjonene skal posteres, for eksempel **per måned**, i feltet **Poster transaksjoner**.</span><span class="sxs-lookup"><span data-stu-id="92c65-118">In the **Post transactions** field, select when the transactions should be posted, such as **Monthly**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]