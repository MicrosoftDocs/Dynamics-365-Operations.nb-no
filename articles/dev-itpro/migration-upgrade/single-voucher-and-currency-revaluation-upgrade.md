---
title: Oppgradering av enkelt bilag og revaluering av valuta
description: "Noen organisasjoner angi journaler som inneholder ett enkelt bilag som har mer enn én kunde eller leverandør, og de kjører også prosess for revaluering av utenlandsk valuta for kunder eller leverandører. Dette emnet beskriver fremgangsmåten som disse organisasjonene bør følge når de oppgraderer til Microsoft Dynamics 365 for Operations versjon 1611."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 84b295440db6cad74d919eb7bbdd41651b9825e9
ms.contentlocale: nb-no
ms.lasthandoff: 04/13/2018

---

# <a name="single-voucher-and-currency-revaluation-upgrade"></a><span data-ttu-id="7e59d-104">Oppgradering av enkelt bilag og revaluering av valuta</span><span class="sxs-lookup"><span data-stu-id="7e59d-104">Single voucher and currency revaluation upgrade</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="7e59d-105">Noen organisasjoner angi journaler som inneholder ett enkelt bilag som har mer enn én kunde eller leverandør, og de kjører også prosess for revaluering av utenlandsk valuta for kunder eller leverandører.</span><span class="sxs-lookup"><span data-stu-id="7e59d-105">Some organizations enter journals that contain a single voucher that has more than one customer or vendor, and they also run the Accounts receivable or Accounts payable foreign currency revaluation process.</span></span> <span data-ttu-id="7e59d-106">Dette emnet beskriver fremgangsmåten som disse organisasjonene bør følge når de oppgraderer til Microsoft Dynamics 365 for Operations versjon 1611.</span><span class="sxs-lookup"><span data-stu-id="7e59d-106">This topic describes the steps that these organizations should follow when they upgrade to Microsoft Dynamics 365 for Operations version 1611.</span></span>

<span data-ttu-id="7e59d-107">Bruk fremgangsmåten nedenfor når du oppgraderer til Microsoft Dynamics 365 for Operations versjon 1611.</span><span class="sxs-lookup"><span data-stu-id="7e59d-107">Follow these steps when you upgrade to Microsoft Dynamics 365 for Operations version 1611.</span></span>

1.  <span data-ttu-id="7e59d-108">Kjør prosessene for revaluering av utenlandsk valuta for kunder og leverandører før du oppgraderer til Dynamics 365 for Operations.</span><span class="sxs-lookup"><span data-stu-id="7e59d-108">Before you upgrade to Dynamics 365 for Operations, run the foreign currency revaluation processes for Accounts receivable and Accounts payable.</span></span> <span data-ttu-id="7e59d-109">Sett **Metode**-feltet til **Fakturadato**.</span><span class="sxs-lookup"><span data-stu-id="7e59d-109">Set the **Method** field to **Invoice date**.</span></span> <span data-ttu-id="7e59d-110">Det opprettes en revalueringstransaksjon som tilbakefører den siste revalueringen av utenlandsk valuta.</span><span class="sxs-lookup"><span data-stu-id="7e59d-110">A revaluation transaction is created that reverses the last foreign currency revaluation.</span></span> <span data-ttu-id="7e59d-111">De åpne transaksjonene verdsettes derfor etter sin opprinnelige regnskapsvaluta.</span><span class="sxs-lookup"><span data-stu-id="7e59d-111">Therefore, the open transactions are valued at their original accounting currency.</span></span>
2.  <span data-ttu-id="7e59d-112">Oppgrader til Dynamics 365 for Operations versjon 1611.</span><span class="sxs-lookup"><span data-stu-id="7e59d-112">Upgrade to Dynamics 365 for Operations version 1611.</span></span>
3.  <span data-ttu-id="7e59d-113">Kjør prosessene for revaluering av utenlandsk valuta for leverandører og kunder på nytt.</span><span class="sxs-lookup"><span data-stu-id="7e59d-113">Run the Accounts receivable and Accounts payable foreign currency revaluation processes again.</span></span> <span data-ttu-id="7e59d-114">Denne gangen setter du **Metode**-feltet til **Standard**.</span><span class="sxs-lookup"><span data-stu-id="7e59d-114">This time, set the **Method** field to **Standard**.</span></span> <span data-ttu-id="7e59d-115">Det opprettes en ny revalueringstransaksjon som er basert på gjeldende valutakurser.</span><span class="sxs-lookup"><span data-stu-id="7e59d-115">A new revaluation transaction is created that is based on the current exchange rates.</span></span> <span data-ttu-id="7e59d-116">Denne transaksjonen registreres urealisert fortjeneste/tap og riktig finanskonto.</span><span class="sxs-lookup"><span data-stu-id="7e59d-116">This transaction records the unrealized gain/loss and the correct summary ledger account.</span></span>





