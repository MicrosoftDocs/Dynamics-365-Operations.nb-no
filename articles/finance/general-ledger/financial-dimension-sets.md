---
title: Finansdimensjonssett
description: Dette emnet beskriver finansdimensjonssett og gir noen tips for optimalisering av bruken.
author: yukonpeegs
ms.date: 03/23/2021
ms.topic: article
ems.prod: ''
ms.technology: ''
ms.search.form: DimensionFocus, LedgerTrialBalanceListPage
audience: Application User
ms.reviewer: roschlom
ms.custom: 25871
ms.search.region: Global
ms.author: epegors
ms.search.validFrom: 2021-03-23
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: ba11be028ebeea140df93e2a07dbb463402e3ef0
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021834"
---
# <a name="financial-dimension-sets"></a><span data-ttu-id="0deb6-103">Finansdimensjonssett</span><span class="sxs-lookup"><span data-stu-id="0deb6-103">Financial dimension sets</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0deb6-104">Dette emnet beskriver finansdimensjonssett og gir noen tips for optimalisering av bruken.</span><span class="sxs-lookup"><span data-stu-id="0deb6-104">This topic describes financial dimension sets and provides some tips for optimizing their use.</span></span>

<span data-ttu-id="0deb6-105">Et dimensjonssett er en sortert liste over finansdimensjoner som kan brukes til å oppsummere økonomimoduldata på en brukerdefinert måte.</span><span class="sxs-lookup"><span data-stu-id="0deb6-105">A dimension set is an ordered list of financial dimensions that can be used to summarize General ledger data in a user-defined way.</span></span> <span data-ttu-id="0deb6-106">En primær bruk av dimensjonssett er å definere en råbalanse.</span><span class="sxs-lookup"><span data-stu-id="0deb6-106">A primary use of dimension sets is to define a trial balance.</span></span>

<span data-ttu-id="0deb6-107">Det eneste standard dimensjonssettet er dimensjonssettet som bare inneholder hovedkontoen.</span><span class="sxs-lookup"><span data-stu-id="0deb6-107">The only standard dimension set is the dimension set that contains only the main account.</span></span>

<span data-ttu-id="0deb6-108">Du bruker siden **Finansdimensjonssett** til å opprette og behandle finansdimensjonssett.</span><span class="sxs-lookup"><span data-stu-id="0deb6-108">You use the **Financial dimension sets** page to create and manage financial dimension sets.</span></span>

## <a name="dimension-set-balances"></a><span data-ttu-id="0deb6-109">Dimensjonssettsaldoer</span><span class="sxs-lookup"><span data-stu-id="0deb6-109">Dimension set balances</span></span>

<span data-ttu-id="0deb6-110">Et dimensjonssett kan ha saldoer som er basert på finansdimensjonene.</span><span class="sxs-lookup"><span data-stu-id="0deb6-110">A dimension set can have balances that are based on its financial dimensions.</span></span> <span data-ttu-id="0deb6-111">Saldoene finnes i økonomimodulen og er basert på dimensjonssettdefinisjonen.</span><span class="sxs-lookup"><span data-stu-id="0deb6-111">The balances exist in General ledger and are based on the dimension set definition.</span></span> <span data-ttu-id="0deb6-112">Saldoene oppsummeres fra økonomimoduldataene for å forbedre ytelsen når de hentes (for eksempel når det genereres en råbalanse).</span><span class="sxs-lookup"><span data-stu-id="0deb6-112">The balances are summarized from the General ledger data to help improve performance when they are retrieved (for example, when a trial balance is generated).</span></span>

## <a name="create-balances"></a><span data-ttu-id="0deb6-113">Opprett saldoer</span><span class="sxs-lookup"><span data-stu-id="0deb6-113">Create balances</span></span>

<span data-ttu-id="0deb6-114">Bruk knappen **Opprett saldoer** til å initialisere saldoene for et dimensjonssett som ikke har saldoer for øyeblikket.</span><span class="sxs-lookup"><span data-stu-id="0deb6-114">Use the **Create balances** button to initialize the balances for a dimension set that doesn't currently have balances.</span></span>

> [!NOTE]
> <span data-ttu-id="0deb6-115">Vi anbefaler at du begrenser antall dimensjonssett som har saldoer, fordi saldooppdateringer påvirker alle posteringsaktiviteter i økonomimodulen.</span><span class="sxs-lookup"><span data-stu-id="0deb6-115">We recommend that you limit the number of dimension sets that have balances, because balance updates affect all General ledger posting activities.</span></span>

## <a name="update-balances"></a><span data-ttu-id="0deb6-116">Oppdater saldoer</span><span class="sxs-lookup"><span data-stu-id="0deb6-116">Update balances</span></span>

<span data-ttu-id="0deb6-117">Bruk **Oppdater saldoer**-knappen til å inkludere den siste posteringsaktiviteten for økonomimodulen i saldoene.</span><span class="sxs-lookup"><span data-stu-id="0deb6-117">Use the **Update balances** button to include the latest General ledger posting activity in the balances.</span></span> <span data-ttu-id="0deb6-118">Saldooppdateringer er enkle operasjoner.</span><span class="sxs-lookup"><span data-stu-id="0deb6-118">Balance updates are light operations.</span></span> <span data-ttu-id="0deb6-119">De må bare behandle posteringsaktiviteten for økonomimodulen som har inntruffet siden forrige oppdatering.</span><span class="sxs-lookup"><span data-stu-id="0deb6-119">They must process only the General ledger posting activity that has occurred since the last update.</span></span>

> [!NOTE]
> <span data-ttu-id="0deb6-120">Visning av råbalansen tvinger en oppdatering for å sikre at saldoene som vises, er gjeldende.</span><span class="sxs-lookup"><span data-stu-id="0deb6-120">Display of the trial balance forces an update, to ensure that the balances that are shown are current.</span></span> <span data-ttu-id="0deb6-121">Vurder å bruke en gjentakende satsvis jobb, slik at oppdateringer av de mest brukte dimensjonssettene går raskt.</span><span class="sxs-lookup"><span data-stu-id="0deb6-121">Consider using a recurring batch job so that updates to your most frequently used dimension sets are quick.</span></span> <span data-ttu-id="0deb6-122">På denne måten kan du redusere tiden som råbalansebrukere må vente.</span><span class="sxs-lookup"><span data-stu-id="0deb6-122">In this way, you help minimize the time that trial balance users must wait.</span></span>

## <a name="rebuild-balances"></a><span data-ttu-id="0deb6-123">Bygg saldoer på nytt</span><span class="sxs-lookup"><span data-stu-id="0deb6-123">Rebuild balances</span></span>

<span data-ttu-id="0deb6-124">Bruk knappen **Bygg saldoer på nytt** til å opprette saldoene på nytt fra begynnelsen.</span><span class="sxs-lookup"><span data-stu-id="0deb6-124">Use the **Rebuild balances** button to re-create the balances from scratch.</span></span> <span data-ttu-id="0deb6-125">På denne måten kan du sikre at de samsvarer med dataene i økonomimodulen.</span><span class="sxs-lookup"><span data-stu-id="0deb6-125">In this way, you help ensure that they match the data in General ledger.</span></span> <span data-ttu-id="0deb6-126">En gjenoppbygging av saldoer krever masse behandling, og bør vanligvis ikke være nødvendig.</span><span class="sxs-lookup"><span data-stu-id="0deb6-126">A rebuild of balances requires lots of processing and should not usually be required.</span></span>

> [!NOTE]
> <span data-ttu-id="0deb6-127">Hvis du har et scenario som regelmessig krever en gjenoppbygging av saldoer, anbefaler vi at du kontakter kundestøtte.</span><span class="sxs-lookup"><span data-stu-id="0deb6-127">If you have a scenario that regularly requires a rebuild of balances, we recommend that you contact customer support.</span></span> <span data-ttu-id="0deb6-128">Kundestøtte kan hjelpe deg med å finne ut hvorfor saldoer ikke samsvarer med dataene i økonomimodulen.</span><span class="sxs-lookup"><span data-stu-id="0deb6-128">Customer support can help you determine why balances don't match the data in General ledger.</span></span>

## <a name="clear-balances"></a><span data-ttu-id="0deb6-129">Avstem saldoer</span><span class="sxs-lookup"><span data-stu-id="0deb6-129">Clear balances</span></span>

<span data-ttu-id="0deb6-130">Bruk **Tøm saldoer**-knappen til å tømme saldoene og stoppe flere oppdateringer.</span><span class="sxs-lookup"><span data-stu-id="0deb6-130">Use the **Clear balances** button to remove the balances and stop any further updates.</span></span> <span data-ttu-id="0deb6-131">Dimensjonssettet vil ikke lenger påvirke posteringsaktiviteter i økonomimodulen.</span><span class="sxs-lookup"><span data-stu-id="0deb6-131">The dimension set will no longer have an impact on General ledger posting activities.</span></span>

<span data-ttu-id="0deb6-132">Hvis du vil ha mer informasjon, kan du se [Finansdimensjoner](financial-dimensions.md).</span><span class="sxs-lookup"><span data-stu-id="0deb6-132">For more information, see [Financial dimensions](financial-dimensions.md).</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
