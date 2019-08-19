---
title: Oppgradere journaler med ett bilag og valutarevalueringer
description: Noen organisasjoner angi journaler som inneholder ett enkelt bilag som har mer enn én kunde eller leverandør, og de kjører også prosess for revaluering av utenlandsk valuta for kunder eller leverandører. Dette emnet beskriver fremgangsmåten som disse organisasjonene bør følge når de oppgraderer til Microsoft Dynamics 365 for Operations versjon 1611.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: b76354d0b8bb89e09e861e013a0c680c36b6537d
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/02/2019
ms.locfileid: "1851687"
---
# <a name="upgrade-single-voucher-journals-and-currency-revaluations"></a><span data-ttu-id="94833-104">Oppgradere enkeltjournalbilag og valutarevalueringer</span><span class="sxs-lookup"><span data-stu-id="94833-104">Upgrade single-voucher journals and currency revaluations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="94833-105">Noen organisasjoner angi journaler som inneholder ett enkelt bilag som har mer enn én kunde eller leverandør, og de kjører også prosess for revaluering av utenlandsk valuta for kunder eller leverandører.</span><span class="sxs-lookup"><span data-stu-id="94833-105">Some organizations enter journals that contain a single voucher that has more than one customer or vendor, and they also run the Accounts receivable or Accounts payable foreign currency revaluation process.</span></span> <span data-ttu-id="94833-106">Dette emnet beskriver fremgangsmåten som disse organisasjonene bør følge når de oppgraderer til Microsoft Dynamics 365 for Operations versjon 1611.</span><span class="sxs-lookup"><span data-stu-id="94833-106">This topic describes the steps that these organizations should follow when they upgrade to Microsoft Dynamics 365 for Operations version 1611.</span></span>

<span data-ttu-id="94833-107">Bruk fremgangsmåten nedenfor når du oppgraderer til Microsoft Dynamics 365 for Operations versjon 1611.</span><span class="sxs-lookup"><span data-stu-id="94833-107">Follow these steps when you upgrade to Microsoft Dynamics 365 for Operations version 1611.</span></span>

1.  <span data-ttu-id="94833-108">Kjør prosessene for revaluering av utenlandsk valuta for kunder og leverandører før du oppgraderer til Dynamics 365 for Operations.</span><span class="sxs-lookup"><span data-stu-id="94833-108">Before you upgrade to Dynamics 365 for Operations, run the foreign currency revaluation processes for Accounts receivable and Accounts payable.</span></span> <span data-ttu-id="94833-109">Sett **Metode**-feltet til **Fakturadato**.</span><span class="sxs-lookup"><span data-stu-id="94833-109">Set the **Method** field to **Invoice date**.</span></span> <span data-ttu-id="94833-110">Det opprettes en revalueringstransaksjon som tilbakefører den siste revalueringen av utenlandsk valuta.</span><span class="sxs-lookup"><span data-stu-id="94833-110">A revaluation transaction is created that reverses the last foreign currency revaluation.</span></span> <span data-ttu-id="94833-111">De åpne transaksjonene verdsettes derfor etter sin opprinnelige regnskapsvaluta.</span><span class="sxs-lookup"><span data-stu-id="94833-111">Therefore, the open transactions are valued at their original accounting currency.</span></span>
2.  <span data-ttu-id="94833-112">Oppgrader til Dynamics 365 for Operations version 1611.</span><span class="sxs-lookup"><span data-stu-id="94833-112">Upgrade to Dynamics 365 for Operations version 1611.</span></span>
3.  <span data-ttu-id="94833-113">Kjør prosessene for revaluering av utenlandsk valuta for leverandører og kunder på nytt.</span><span class="sxs-lookup"><span data-stu-id="94833-113">Run the Accounts receivable and Accounts payable foreign currency revaluation processes again.</span></span> <span data-ttu-id="94833-114">Denne gangen setter du **Metode**-feltet til **Standard**.</span><span class="sxs-lookup"><span data-stu-id="94833-114">This time, set the **Method** field to **Standard**.</span></span> <span data-ttu-id="94833-115">Det opprettes en ny revalueringstransaksjon som er basert på gjeldende valutakurser.</span><span class="sxs-lookup"><span data-stu-id="94833-115">A new revaluation transaction is created that is based on the current exchange rates.</span></span> <span data-ttu-id="94833-116">Denne transaksjonen registreres urealisert fortjeneste/tap og riktig finanskonto.</span><span class="sxs-lookup"><span data-stu-id="94833-116">This transaction records the unrealized gain/loss and the correct summary ledger account.</span></span>




