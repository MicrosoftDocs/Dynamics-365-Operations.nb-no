---
title: Oppgradere enkeltjournalbilag og valutarevalueringer
description: Dette emnet beskriver hvordan du oppgraderer enkeltbilagsjournaler og valutarevalueringer.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: fb4eca4933716105789d3bbc21dd374395211d1d
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559527"
---
# <a name="upgrade-single-voucher-journals-and-currency-revaluations"></a><span data-ttu-id="87ccf-103">Oppgradere enkeltjournalbilag og valutarevalueringer</span><span class="sxs-lookup"><span data-stu-id="87ccf-103">Upgrade single-voucher journals and currency revaluations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="87ccf-104">Noen organisasjoner angi journaler som inneholder ett enkelt bilag som har mer enn én kunde eller leverandør, og de kjører også prosess for revaluering av utenlandsk valuta for kunder eller leverandører.</span><span class="sxs-lookup"><span data-stu-id="87ccf-104">Some organizations enter journals that contain a single voucher that has more than one customer or vendor, and they also run the Accounts receivable or Accounts payable foreign currency revaluation process.</span></span> <span data-ttu-id="87ccf-105">Dette emnet beskriver fremgangsmåten som disse organisasjonene bør følge når de oppgraderer til Microsoft Dynamics 365 for Operations versjon 1611.</span><span class="sxs-lookup"><span data-stu-id="87ccf-105">This topic describes the steps that these organizations should follow when they upgrade to Microsoft Dynamics 365 for Operations version 1611.</span></span>

<span data-ttu-id="87ccf-106">Bruk fremgangsmåten nedenfor når du oppgraderer til Microsoft Dynamics 365 for Operations versjon 1611.</span><span class="sxs-lookup"><span data-stu-id="87ccf-106">Follow these steps when you upgrade to Microsoft Dynamics 365 for Operations version 1611.</span></span>

1.  <span data-ttu-id="87ccf-107">Kjør prosessene for revaluering av utenlandsk valuta for kunder og leverandører før du oppgraderer til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="87ccf-107">Before you upgrade to Finance and Operations, run the foreign currency revaluation processes for Accounts receivable and Accounts payable.</span></span> <span data-ttu-id="87ccf-108">Sett **Metode**-feltet til **Fakturadato**.</span><span class="sxs-lookup"><span data-stu-id="87ccf-108">Set the **Method** field to **Invoice date**.</span></span> <span data-ttu-id="87ccf-109">Det opprettes en revalueringstransaksjon som tilbakefører den siste revalueringen av utenlandsk valuta.</span><span class="sxs-lookup"><span data-stu-id="87ccf-109">A revaluation transaction is created that reverses the last foreign currency revaluation.</span></span> <span data-ttu-id="87ccf-110">De åpne transaksjonene verdsettes derfor etter sin opprinnelige regnskapsvaluta.</span><span class="sxs-lookup"><span data-stu-id="87ccf-110">Therefore, the open transactions are valued at their original accounting currency.</span></span>
2.  <span data-ttu-id="87ccf-111">Oppgrader til version 1611.</span><span class="sxs-lookup"><span data-stu-id="87ccf-111">Upgrade to version 1611.</span></span>
3.  <span data-ttu-id="87ccf-112">Kjør prosessene for revaluering av utenlandsk valuta for leverandører og kunder på nytt.</span><span class="sxs-lookup"><span data-stu-id="87ccf-112">Run the Accounts receivable and Accounts payable foreign currency revaluation processes again.</span></span> <span data-ttu-id="87ccf-113">Denne gangen setter du **Metode**-feltet til **Standard**.</span><span class="sxs-lookup"><span data-stu-id="87ccf-113">This time, set the **Method** field to **Standard**.</span></span> <span data-ttu-id="87ccf-114">Det opprettes en ny revalueringstransaksjon som er basert på gjeldende valutakurser.</span><span class="sxs-lookup"><span data-stu-id="87ccf-114">A new revaluation transaction is created that is based on the current exchange rates.</span></span> <span data-ttu-id="87ccf-115">Denne transaksjonen registreres urealisert fortjeneste/tap og riktig finanskonto.</span><span class="sxs-lookup"><span data-stu-id="87ccf-115">This transaction records the unrealized gain/loss and the correct summary ledger account.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]