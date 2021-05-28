---
title: Standardbeskrivelser for økonomimodulen
description: Standardbeskrivelser kan brukes til å oppdatere feltet Beskrivelse i bilagsposteringer til økonomimodulen.
author: sherry-zheng
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TransactionTexts
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 25dd72c86b22b50eccef22a5d2cbcfcf04280684
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021618"
---
# <a name="default-descriptions-for-the-general-ledger"></a><span data-ttu-id="25d35-103">Standardbeskrivelser for økonomimodulen</span><span class="sxs-lookup"><span data-stu-id="25d35-103">Default descriptions for the general ledger</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="25d35-104">Standardbeskrivelser kan brukes til å oppdatere feltet **Beskrivelse** i bilagsposteringer til økonomimodulen.</span><span class="sxs-lookup"><span data-stu-id="25d35-104">Default descriptions can be used to update the **Description** field in voucher postings to the general ledger.</span></span> <span data-ttu-id="25d35-105">Denne funksjonaliteten er utvidet for å arbeide med Netto innkjøpspris.</span><span class="sxs-lookup"><span data-stu-id="25d35-105">This functionality has been enhanced to work with Landed cost.</span></span>

<span data-ttu-id="25d35-106">Hvis du vil definere standardbeskrivelser for finansposteringer, kan du gå til **Organisasjonsstyring \> Oppsett \> Standardbeskrivelser**.</span><span class="sxs-lookup"><span data-stu-id="25d35-106">To set up default descriptions for ledger postings, go to **Organizational administration \> Setup \> Default descriptions**.</span></span>

<span data-ttu-id="25d35-107">Følgende tabell viser de nye verdiene som er lagt til for feltet **Beskrivelse** på siden **Standardbeskrivelser** for å støtte Netto innkjøpspris.</span><span class="sxs-lookup"><span data-stu-id="25d35-107">The following table lists the new values that have been added for the **Description** field on the **Default descriptions** page to support Landed cost.</span></span>

| <span data-ttu-id="25d35-108">Beskrivelsestype</span><span class="sxs-lookup"><span data-stu-id="25d35-108">Description type</span></span> | <span data-ttu-id="25d35-109">Notater</span><span class="sxs-lookup"><span data-stu-id="25d35-109">Notes</span></span> |
|---|---|
| <span data-ttu-id="25d35-110">Importer etterkalkulering – Kostnadsforløp</span><span class="sxs-lookup"><span data-stu-id="25d35-110">Import costing – Cost accrual</span></span> | <span data-ttu-id="25d35-111">Når en bestillingsfaktura posteres, behandles en kostnadsavsetning for estimerte sjøreisekostnader.</span><span class="sxs-lookup"><span data-stu-id="25d35-111">When a purchase order invoice is posted, a cost accrual is processed for estimate voyage costs.</span></span> <span data-ttu-id="25d35-112">Standardbeskrivelser kan angis for å legge til sjøreisenummeret i beskrivelsen.</span><span class="sxs-lookup"><span data-stu-id="25d35-112">Default descriptions can be specified to add the voyage number to the description.</span></span> <span data-ttu-id="25d35-113">Bruk *%4* for forsendelsesnummeret.</span><span class="sxs-lookup"><span data-stu-id="25d35-113">Use *%4* for the shipment number.</span></span> |
| <span data-ttu-id="25d35-114">Importer etterkalkulering – Varer i transittordre</span><span class="sxs-lookup"><span data-stu-id="25d35-114">Import costing – Goods in transit order</span></span> | <span data-ttu-id="25d35-115">Hvis du bruker behandling i transitt, posteres bestillingsfakturaen, og varene posteres til en vare i transittkonto.</span><span class="sxs-lookup"><span data-stu-id="25d35-115">If you're using in-transit processing, the purchase order invoice is posted, and the goods are posted to a goods in transit account.</span></span> <span data-ttu-id="25d35-116">Standardbeskrivelser kan angis for å legge til ordrenummeret i transitt i beskrivelsen.</span><span class="sxs-lookup"><span data-stu-id="25d35-116">Default descriptions can be specified to add the in-transit order number to the description.</span></span> <span data-ttu-id="25d35-117">Bruk *%4* for ordrenummeret i transitt.</span><span class="sxs-lookup"><span data-stu-id="25d35-117">Use *%4* for the in-transit order number.</span></span> |
| <span data-ttu-id="25d35-118">Beholdning – lukking – justering</span><span class="sxs-lookup"><span data-stu-id="25d35-118">Inventory – close – adjustment</span></span> | <span data-ttu-id="25d35-119">Når AP-fakturaen behandles for en sjøreisekostnad, behandles en lagerjustering for å estimere sjøreisekostnader.</span><span class="sxs-lookup"><span data-stu-id="25d35-119">When the accounts payable (AP) invoice is processed for a voyage cost, an inventory adjustment is processed to estimate voyage costs.</span></span> <span data-ttu-id="25d35-120">Standardbeskrivelser kan angis for å legge til sjøreisenummeret i beskrivelsen.</span><span class="sxs-lookup"><span data-stu-id="25d35-120">Default descriptions can be specified to add the voyage number to the description.</span></span> <span data-ttu-id="25d35-121">Bruk *%4* for forsendelsesnummeret.</span><span class="sxs-lookup"><span data-stu-id="25d35-121">Use *%4* for the shipment number.</span></span> |

<span data-ttu-id="25d35-122">Hvis du vil ha mer informasjon om hvordan du arbeider med siden **Standardbeskrivelser**, kan du se [Definere standardbeskrivelser for automatisk postering](../../finance/general-ledger/set-up-default-descriptions-for-automatic-posting.md).</span><span class="sxs-lookup"><span data-stu-id="25d35-122">For more information about how to work with the **Default descriptions** page, see [Set up default descriptions for automatic posting](../../finance/general-ledger/set-up-default-descriptions-for-automatic-posting.md).</span></span>
