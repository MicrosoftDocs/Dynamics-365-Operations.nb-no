---
title: Glidende gjennomsnitt, sekvens for kostnad for tilbakefall
description: Dette emnet inneholder informasjon om sekvenser for kostnad for tilbakefall for glidende gjennomsnitt av beregninger i Microsoft Dynamics 365 Supply Chain Management.
author: AndersGirke
manager: AnnBe
ms.date: 03/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-03-25
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: b2172dfbec0a7f0fa25a081e4d92635a09f00e46
ms.sourcegitcommit: 3a823444005d316bd95fc663e2dbc8252ac7d93a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/14/2020
ms.locfileid: "3261361"
---
# <a name="moving-average-fallback-cost-sequence"></a><span data-ttu-id="6952f-103">Glidende gjennomsnitt, sekvens for kostnad for tilbakefall</span><span class="sxs-lookup"><span data-stu-id="6952f-103">Moving average fallback cost sequence</span></span>

<span data-ttu-id="6952f-104">En måte du kan beregne lagerkostnadene på, er ved hjelp av et _glidende gjennomsnitt_.</span><span class="sxs-lookup"><span data-stu-id="6952f-104">One way that you can calculate the cost of your inventory is by using a _moving average_.</span></span> <span data-ttu-id="6952f-105">Opptil tre kostnadsverdier kan knyttes til hver lagervare:</span><span class="sxs-lookup"><span data-stu-id="6952f-105">Up to three cost values can be associated with each inventory item:</span></span>

- <span data-ttu-id="6952f-106">**Siste avgang** – Den siste avgangskostnaden som ble tilordnet før beholdningen ble negativ</span><span class="sxs-lookup"><span data-stu-id="6952f-106">**Last issue** – The last issue cost that was assigned before inventory went negative</span></span>
- <span data-ttu-id="6952f-107">**Aktiv kostnad** – Den siste kostnaden som ble aktivert i en etterkalkuleringsversjon</span><span class="sxs-lookup"><span data-stu-id="6952f-107">**Active cost** – The latest cost that was activated in a costing version</span></span>
- <span data-ttu-id="6952f-108">**Varepris** – Kostnaden som er angitt for det frigitte produktet</span><span class="sxs-lookup"><span data-stu-id="6952f-108">**Item price** – The cost that is specified for the released product</span></span>

<span data-ttu-id="6952f-109">For å bestemme hvilke av disse kostverdiene som skal brukes ved beregning av glidende gjennomsnitt, bruker systemet en _sekvens for kostnad for tilbakefall_ for å etablere preferanserekkefølgen for verdiene.</span><span class="sxs-lookup"><span data-stu-id="6952f-109">To determine which of these cost values should be used in moving average calculations, the system uses a _fallback cost sequence_ to establish the order of preference for the values.</span></span> <span data-ttu-id="6952f-110">Hvis den foretrukne kostnadsverdien ikke er tilgjengelig, bruker systemet den neste foretrukne verdien, og så videre.</span><span class="sxs-lookup"><span data-stu-id="6952f-110">If the preferred cost value isn't available, the system uses the next-preferred value, and so on.</span></span>

<span data-ttu-id="6952f-111">I tidligere versjoner av Microsoft Dynamics 365 Supply Chain Management brukte systemet en fast sekvens for kostnad for tilbakefall (_siste avgang – aktiv kostnad – varepris_).</span><span class="sxs-lookup"><span data-stu-id="6952f-111">In previous versions of Microsoft Dynamics 365 Supply Chain Management, the system used a fixed fallback cost sequence (_Last issue – Active cost – Item price_).</span></span> <span data-ttu-id="6952f-112">I versjon 10.0.11 er denne sekvensen fremdeles standardsekvensen.</span><span class="sxs-lookup"><span data-stu-id="6952f-112">In version 10.0.11, this sequence is still the default sequence.</span></span> <span data-ttu-id="6952f-113">Du kan imidlertid også aktivere en funksjon som lar deg velge mellom tre tilgjengelige sekvenser for kostnad for tilbakefall.</span><span class="sxs-lookup"><span data-stu-id="6952f-113">However, you can also turn on a feature that lets you select among three available fallback cost sequences.</span></span> <span data-ttu-id="6952f-114">Denne funksjonen kan være spesielt nyttig for organisasjoner som regelmessig bruker negative beholdningsverdier.</span><span class="sxs-lookup"><span data-stu-id="6952f-114">This feature can be especially useful for organizations that regularly use negative inventory values.</span></span>

<span data-ttu-id="6952f-115">Hvis du vil gjøre velgeren for tilbakefallskostnadene tilgjengelig, må du (eller en administrator) bruke [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til å aktivere funksjonen med navnet _Glidende gjennomsnitt, sekvens for kostnad for tilbakefall_.</span><span class="sxs-lookup"><span data-stu-id="6952f-115">To make the selector for the fallback cost sequence available, you (or an admin) must use [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn on the feature that is named _Moving average fallback cost sequence_.</span></span>

<span data-ttu-id="6952f-116">Følg denne fremgangsmåten for å velge sekvensen for kostnad for tilbakefall for beregning av glidende gjennomsnitt.</span><span class="sxs-lookup"><span data-stu-id="6952f-116">To select the fallback cost sequence for moving average calculations, follow these steps.</span></span>

1. <span data-ttu-id="6952f-117">Åpne **Parametere**-siden.</span><span class="sxs-lookup"><span data-stu-id="6952f-117">Open the **Parameters** page.</span></span>
2. <span data-ttu-id="6952f-118">I kategorien **Lagerregnskap**, i delen **Glidende gjennomsnitt**, setter du feltet **Sekvens for kostnad for tilbakefall** til en av følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="6952f-118">On the **Inventory accounting** tab, in the **Moving average** section, set the **Fallback cost sequence** field to one of the following values:</span></span>

    - <span data-ttu-id="6952f-119">**Siste avgang – Aktiv kostnad – varepris** – Denne sekvensen er standardsekvensen.</span><span class="sxs-lookup"><span data-stu-id="6952f-119">**Last issue – Active cost – Item price** – This sequence is the default sequence.</span></span> <span data-ttu-id="6952f-120">Det er samme sekvens som brukes hvis funksjonen _Glidende gjennomsnitt, sekvens for kostnad for tilbakefall_ ikke er aktivert.</span><span class="sxs-lookup"><span data-stu-id="6952f-120">It's the same sequence that is used if the _Moving average fallback cost sequence_ feature isn't turned on.</span></span>
    - <span data-ttu-id="6952f-121">**Aktiv kostnad – Siste avgang**</span><span class="sxs-lookup"><span data-stu-id="6952f-121">**Active cost – Last issue**</span></span>
    - <span data-ttu-id="6952f-122">**Aktiv kostnad – Varepris** – Organisasjoner kan oppleve ytelsesproblemer hvis de bruker forretningsprosesser der lageret regelmessig blir negativ, og samtidig har et høyt transaksjonsvolum.</span><span class="sxs-lookup"><span data-stu-id="6952f-122">**Active cost – Item price** – Organizations might experience performance issues if they use business processes where inventory regularly goes negative and, at the same time, the transaction volume is high.</span></span> <span data-ttu-id="6952f-123">Denne innstillingen kan bidra til å redusere disse ytelsesproblemene.</span><span class="sxs-lookup"><span data-stu-id="6952f-123">This setting can help mitigate those performance issues.</span></span>

<span data-ttu-id="6952f-124">![Parametere for lagerregnskap](media/inventory-accounting-parameters.png "Parametere for lagerregnskap")</span><span class="sxs-lookup"><span data-stu-id="6952f-124">![Inventory accounting parameters](media/inventory-accounting-parameters.png "Inventory accounting parameters")</span></span>
