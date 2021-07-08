---
title: Produktet er på vent for transaksjoner
description: Når du har autorisert planleggingsordrer, får du en feilmelding som angir at en vare er sperret for transaksjoner.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 6654e6437a088218db116b955631be4c7e62de5f
ms.sourcegitcommit: f9b145ef4a81cec81f420871b4130b05db4f4500
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/23/2021
ms.locfileid: "6301285"
---
# <a name="product-is-on-hold-for-transactions"></a><span data-ttu-id="7f388-103">Produktet er på vent for transaksjoner</span><span class="sxs-lookup"><span data-stu-id="7f388-103">Product is on hold for transactions</span></span>

<span data-ttu-id="7f388-104">Feilkode: SYS13295</span><span class="sxs-lookup"><span data-stu-id="7f388-104">Error code: SYS13295</span></span>

## <a name="symptoms"></a><span data-ttu-id="7f388-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="7f388-105">Symptoms</span></span>

<span data-ttu-id="7f388-106">Når du har autorisert ordrer, mottar du følgende feilmelding:</span><span class="sxs-lookup"><span data-stu-id="7f388-106">After you firm planned orders, you receive the following error message:</span></span>

> <span data-ttu-id="7f388-107">Varen %1 er sperret for transaksjoner i %2.</span><span class="sxs-lookup"><span data-stu-id="7f388-107">Item %1 is on hold for transactions in %2.</span></span>

## <a name="cause"></a><span data-ttu-id="7f388-108">Årsak</span><span class="sxs-lookup"><span data-stu-id="7f388-108">Cause</span></span>

<span data-ttu-id="7f388-109">Når blokkerte varer beskrives, bruker systemet termene *blokkert*, *stoppet* og *på vent* om hverandre.</span><span class="sxs-lookup"><span data-stu-id="7f388-109">When describing blocked items, system uses the terms *blocked*, *stopped*, and *on hold* interchangeably.</span></span> <span data-ttu-id="7f388-110">Denne feilen betyr at varen angis som **Stoppet** i standardordreinnstillingene.</span><span class="sxs-lookup"><span data-stu-id="7f388-110">This error means that the item is set as **Stopped** in its default order settings.</span></span>

<span data-ttu-id="7f388-111">Hvis en vare er sperret, og du legger den til i en bestilling eller salgsordrelinje, får du en advarsel.</span><span class="sxs-lookup"><span data-stu-id="7f388-111">If an item is blocked, and you add it to a purchase order or sales order line, you receive a warning message.</span></span> <span data-ttu-id="7f388-112">Når en vare er sperret, kan du ikke endre lagertransaksjoner som er knyttet til bestillings- eller salgsordrelinjen når du for eksempel posterer en følgeseddel eller en faktura.</span><span class="sxs-lookup"><span data-stu-id="7f388-112">When an item is blocked, inventory transactions that are related to the purchase order or sales order line can't be modified (for example, when you post a packing slip or an invoice).</span></span> <span data-ttu-id="7f388-113">Du kan sperre en kjøpt vare og samtidig selge varen.</span><span class="sxs-lookup"><span data-stu-id="7f388-113">You can block a purchased item, and, at the same time, sell the item.</span></span> <span data-ttu-id="7f388-114">I dette tilfellet er det merket av for **Stoppet** i en bestilling, men varen er ikke sperret på lager eller i en salgsordre.</span><span class="sxs-lookup"><span data-stu-id="7f388-114">In this case, the **Stopped** check box is selected on a purchase order, but the item isn't blocked in inventory or on a sales order.</span></span>

<span data-ttu-id="7f388-115">Her er noen av betingelsene som kan føre til at et varenummer blir blokkert fra å bli solgt:</span><span class="sxs-lookup"><span data-stu-id="7f388-115">Here are some of the conditions that can cause an item number to be blocked from being sold:</span></span>

- <span data-ttu-id="7f388-116">Varen er fremdeles er under utvikling eller produksjon.</span><span class="sxs-lookup"><span data-stu-id="7f388-116">The item is still under development or manufacture.</span></span> <span data-ttu-id="7f388-117">Derfor ønsker du ikke at den skal selges eller reserveres.</span><span class="sxs-lookup"><span data-stu-id="7f388-117">Therefore, you don't want it to be sold or reserved.</span></span>
- <span data-ttu-id="7f388-118">Du har mottatt mange mangelfulle varer, og defektene må korrigeres før varen kan selges.</span><span class="sxs-lookup"><span data-stu-id="7f388-118">You've received many defective items, and the defects must be corrected before the item can be sold.</span></span>

<span data-ttu-id="7f388-119">I slike tilfeller kan du ikke sperre varen før problemet er løst.</span><span class="sxs-lookup"><span data-stu-id="7f388-119">In cases of this type, you can block the item until the issue is resolved.</span></span>

<span data-ttu-id="7f388-120">Hvis en vare er sperret og du oppretter en returordrelinje, mottar du en melding.</span><span class="sxs-lookup"><span data-stu-id="7f388-120">If an item is blocked, and you create a return order line, you receive a message.</span></span> <span data-ttu-id="7f388-121">Du kan ikke sperre en serie eller et parti av en vare.</span><span class="sxs-lookup"><span data-stu-id="7f388-121">You can't block a series or a lot of an item.</span></span> <span data-ttu-id="7f388-122">Hvis deler av en vare må sperres, kan du gjøre det ved å flytte beholdningen eller ved å blokkere hele lagerbeholdningen av varen i dette tidsrommet.</span><span class="sxs-lookup"><span data-stu-id="7f388-122">If parts of an item must be blocked, you can block them by moving inventory or by blocking the full stock of the item for that period.</span></span>

## <a name="resolution"></a><span data-ttu-id="7f388-123">Løsning</span><span class="sxs-lookup"><span data-stu-id="7f388-123">Resolution</span></span>

- <span data-ttu-id="7f388-124">Åpne siden **Standard ordreinnstillinger** for varen, og fjern merket for **Stoppet**.</span><span class="sxs-lookup"><span data-stu-id="7f388-124">Open the **Default order settings** page for the item, and clear the **Stopped** checkbox.</span></span>
