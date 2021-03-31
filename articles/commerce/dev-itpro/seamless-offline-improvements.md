---
title: Sømløs bryter for frakoblet modus for gavekort- og kreditnotaoperasjoner
description: Dette emnet gir en oversikt over forbedringer som gir en sømløs bryter i frakoblet modus for bestemte betalingstyper.
author: rubendel
manager: AnnBe
ms.date: 02/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: 141393
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 20120-02-28
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 1ea46ae90dedcc3ad3c3b305bddeb4d98827353a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5230675"
---
# <a name="seamless-offline-switch-for-gift-card-and-credit-memo-operations"></a><span data-ttu-id="295c1-103">Sømløs bryter for frakoblet modus for gavekort- og kreditnotaoperasjoner</span><span class="sxs-lookup"><span data-stu-id="295c1-103">Seamless offline switch for gift card and credit memo operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="295c1-104">Hvis en salgsstedsenhet (POS) mister tilkoblingen til kanaldatabasen, kan de fleste de fleste POS-operasjoner og -transaksjoner som var i gang, fortsette etter at kassereren får en advarsel om tap av tilkobling.</span><span class="sxs-lookup"><span data-stu-id="295c1-104">If a point of sale (POS) device loses its connection to the channel database, most POS operations and transactions that were in progress can proceed after the cashier receives a warning message about the loss of connectivity.</span></span> <span data-ttu-id="295c1-105">I noen tilfeller har transaksjoner imidlertid elementer som er avhengige av service i sanntid, og disse elementene støttes ikke når POS er frakoblet.</span><span class="sxs-lookup"><span data-stu-id="295c1-105">However, in some cases, transactions have elements that rely on the real-time service, and those elements aren't supported when the POS is offline.</span></span> <span data-ttu-id="295c1-106">Dette emnet beskriver noe funksjonalitet som bidrar til å redusere virkningen av tapt tilkobling i disse scenariene.</span><span class="sxs-lookup"><span data-stu-id="295c1-106">This topic describes some functionality that helps reduce the impact of lost connectivity in these scenarios.</span></span>

## <a name="completing-gift-card-transactions-in-offline-mode"></a><span data-ttu-id="295c1-107">Fullføring av gavekorttransaksjoner i frakoblet modus</span><span class="sxs-lookup"><span data-stu-id="295c1-107">Completing gift card transactions in offline mode</span></span>

<span data-ttu-id="295c1-108">Interne gavekort er avhengige av service i sanntid, fordi saldoen for gavekortene må vedlikeholdes sentralt i Microsoft Dynamics 365 Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="295c1-108">Internal gift cards depend on the real-time service, because the balance for the gift cards must be centrally maintained in Microsoft Dynamics 365 Commerce Headquarters.</span></span> <span data-ttu-id="295c1-109">For å hindre svindel eller andre synkroniseringsproblemer låses gavekort så snart de er lagt til i en transaksjon.</span><span class="sxs-lookup"><span data-stu-id="295c1-109">To help prevent fraud or other synchronization issues, gift cards are locked as soon as they are added to a transaction.</span></span> <span data-ttu-id="295c1-110">Låsefunksjonen sikrer at et gavekort ikke kan brukes på flere terminaler samtidig.</span><span class="sxs-lookup"><span data-stu-id="295c1-110">The locking function ensures that a gift card can't be used on multiple terminals at the same time.</span></span> <span data-ttu-id="295c1-111">Når en transaksjon er fullført, blir gavekortet oppdatert og låst opp.</span><span class="sxs-lookup"><span data-stu-id="295c1-111">When a transaction is completed, the gift card is updated and unlocked.</span></span>

<span data-ttu-id="295c1-112">Hvis tilkoblingen til salgsstedet forsvinner etter at et gavekort er lagt til i en transaksjon, kan gavekortet imidlertid bli ubrukelig.</span><span class="sxs-lookup"><span data-stu-id="295c1-112">However, if the POS loses connectivity after a gift card has been added to a transaction, the gift card can become unusable.</span></span> <span data-ttu-id="295c1-113">For å hindre denne situasjonen har Dynamics 365 Commerce en parameter som gjør det mulig å fullføre transaksjoner som inneholder en gavekortlinje mens POS er frakoblet.</span><span class="sxs-lookup"><span data-stu-id="295c1-113">To help prevent this situation, Dynamics 365 Commerce has a parameter that enables transactions that include a gift card line to be completed while the POS is offline.</span></span> <span data-ttu-id="295c1-114">Når denne parameteren er aktivert, vil gavekorttransaksjoner som fremtvinges frakoblet, lagres sammen med frakoblede transaksjoner, og de blir synkronisert til Commerce Headquarters når de frakoblede transaksjonene er synkronisert.</span><span class="sxs-lookup"><span data-stu-id="295c1-114">When this parameter is turned on, gift card transactions that are forced offline will be saved together with offline transactions, and they will be synced to Commerce Headquarters when the offline transactions are synced.</span></span> <span data-ttu-id="295c1-115">Synkroniseringen vil også låse opp gavekortet slik at det kan brukes ved en annen terminal.</span><span class="sxs-lookup"><span data-stu-id="295c1-115">The synchronization will also unlock the gift card so that it can be used at another terminal.</span></span>

<span data-ttu-id="295c1-116">Hvis du vil aktivere funksjonaliteten for å fullføre gavekorttransaksjoner etter at du har byttet til frakoblet modus, kan du gå til kategorien **Postering** på siden **Parametere for Commerce**.</span><span class="sxs-lookup"><span data-stu-id="295c1-116">To enable the functionality to conclude gift card transactions after switching to offline mode, go to the **Posting** tab on the **Commerce parameters** page.</span></span> <span data-ttu-id="295c1-117">I denne kategorien finner du hurtigfanen **Gavekort**, og angi **Tillat avslutning av gavekorttransaksjoner i frakoblet modus** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="295c1-117">On that tab, locate the **Gift card** fasttab and set **Allow concluding gift card transactions in offline mode** to **Yes**.</span></span>

![Frakoblet innstilling for gavekort](../media/gift.png)

<span data-ttu-id="295c1-119">Commerce-parametere bufres vanligvis.</span><span class="sxs-lookup"><span data-stu-id="295c1-119">Commerce parameters are typically cached.</span></span> <span data-ttu-id="295c1-120">Etter at innstillingen for denne parameteren er oppdatert og distribusjonsplanen startes for å synkronisere endringen til kanalen, kan det derfor ta opptil 24 timer før endringen trer i kraft.</span><span class="sxs-lookup"><span data-stu-id="295c1-120">Therefore, after the setting of this parameter is updated, and the distribution schedule is initiated to sync the change to the channel, the change can take up to 24 hours to take effect.</span></span> <span data-ttu-id="295c1-121">Hvis du vil gjøre endringene gjeldende umiddelbart, tilbakestiller du Microsoft Internet Information Services (IIS).</span><span class="sxs-lookup"><span data-stu-id="295c1-121">To make the change effective immediately, reset Microsoft Internet Information Services (IIS).</span></span>

## <a name="completing-credit-memo-transactions-in-offline-mode"></a><span data-ttu-id="295c1-122">Fullføring av kreditnotatransaksjoner i frakoblet modus</span><span class="sxs-lookup"><span data-stu-id="295c1-122">Completing credit memo transactions in offline mode</span></span>

<span data-ttu-id="295c1-123">På samme måte som interne gavekort vedlikeholdes kreditnotaer sentralt i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="295c1-123">Like internal gift cards, credit memos are centrally maintained in Commerce Headquarters.</span></span> <span data-ttu-id="295c1-124">Commerce har en parameter som gjør at kreditnotatransaksjoner kan fullføres mens salgsstedet er frakoblet.</span><span class="sxs-lookup"><span data-stu-id="295c1-124">Commerce has a parameter that enables credit memo transactions to be completed while the POS is offline.</span></span> <span data-ttu-id="295c1-125">Denne parameteren fungerer som gavekortparameteren som ble nevnt i forrige del.</span><span class="sxs-lookup"><span data-stu-id="295c1-125">This parameter works like the gift card parameter that was mentioned in the previous section.</span></span> <span data-ttu-id="295c1-126">Når parameteren er aktivert, vil kreditnotatransaksjoner som fremtvinges frakoblet, synkroniseres tilbake til kanaldatabasen sammen med andre transaksjoner som ble utført mens salgsstedet var frakoblet.</span><span class="sxs-lookup"><span data-stu-id="295c1-126">When the parameter is turned on, credit memo transactions that are forced offline will be synced back to the channel database, together with other transactions that were performed while the POS was offline.</span></span>

<span data-ttu-id="295c1-127">Hvis du vil aktivere funksjonaliteten for å fullføre kreditnotatransaksjoner etter at du har byttet til frakoblet modus, kan du gå til kategorien **Postering** på siden **Parametere for Commerce**.</span><span class="sxs-lookup"><span data-stu-id="295c1-127">To enable the functionality to conclude credit memo transactions after switching to offline mode, go to the **Posting** tab on the **Commerce parameters** page.</span></span> <span data-ttu-id="295c1-128">I denne kategorien finner du hurtigfanen **Kreditnota**, og angi **Tillat avslutning av kreditnotatransaksjoner i frakoblet modus** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="295c1-128">On that tab, locate the **Credit memo** fasttab and set **Allow concluding credit memo transactions in offline mode** to **Yes**.</span></span>

![Frakoblet innstilling for kreditnota](../media/creditmemo.png)

<span data-ttu-id="295c1-130">Commerce-parametere bufres vanligvis.</span><span class="sxs-lookup"><span data-stu-id="295c1-130">Commerce parameters are typically cached.</span></span> <span data-ttu-id="295c1-131">Etter at innstillingen for denne parameteren er oppdatert og distribusjonsplanen startes for å synkronisere endringen til kanalen, kan det derfor ta opptil 24 timer før endringen trer i kraft.</span><span class="sxs-lookup"><span data-stu-id="295c1-131">Therefore, after the setting of this parameter is updated, and the distribution schedule is initiated to sync the change to the channel, the change can take up to 24 hours to take effect.</span></span> <span data-ttu-id="295c1-132">Hvis du vil gjøre endringene gjeldende umiddelbart, tilbakestiller du IIS.</span><span class="sxs-lookup"><span data-stu-id="295c1-132">To make the change effective immediately, reset IIS.</span></span>

## <a name="related-topics"></a><span data-ttu-id="295c1-133">Relaterte emner</span><span class="sxs-lookup"><span data-stu-id="295c1-133">Related topics</span></span>

- [<span data-ttu-id="295c1-134">Frakoblet salgsstedsfunksjonalitet</span><span class="sxs-lookup"><span data-stu-id="295c1-134">Offline point of sale (POS) functionality</span></span>](https://docs.microsoft.com/dynamics365/retail/pos-offline-functionality)
- [<span data-ttu-id="295c1-135">Tilkoblede og frakoblede salgsstedsoperasjoner (POS)</span><span class="sxs-lookup"><span data-stu-id="295c1-135">Online and offline point of sale (POS) operations</span></span>](https://docs.microsoft.com/dynamics365/retail/pos-operations)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]