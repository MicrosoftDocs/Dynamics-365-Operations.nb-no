---
title: Oversikt over livssyklus for produksjonsordre
description: Når en produksjonsordre opprettes, startes en forespørsel om å starte produksjonen av en vare. Produksjonsordren inneholder informasjon om hva som skal produseres, antallet som skal produseres og den planlagte sluttdatoen. Den inneholder også informasjon om hvilke materialer som skal brukes og prosessen som skal følges for å produsere varen.
author: johanhoffmann
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTable, ProdTableCreate
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19741
ms.assetid: bbb6e69d-479c-45fc-a0a8-66da5df16c7f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 68758f4ddf39b4b8f7f0758f9e59e17c3411723a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5246315"
---
# <a name="production-order-lifecycle-overview"></a><span data-ttu-id="38a83-105">Oversikt over livssyklus for produksjonsordre</span><span class="sxs-lookup"><span data-stu-id="38a83-105">Production order lifecycle overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="38a83-106">Når en produksjonsordre opprettes, startes en forespørsel om å starte produksjonen av en vare.</span><span class="sxs-lookup"><span data-stu-id="38a83-106">When a production order is created, a request is initiated to start producing an item.</span></span> <span data-ttu-id="38a83-107">Produksjonsordren inneholder informasjon om hva som skal produseres, antallet som skal produseres og den planlagte sluttdatoen.</span><span class="sxs-lookup"><span data-stu-id="38a83-107">The production order contains information about what will be produced, the quantity to produce, and the planned finish date.</span></span> <span data-ttu-id="38a83-108">Den inneholder også informasjon om hvilke materialer som skal brukes og prosessen som skal følges for å produsere varen.</span><span class="sxs-lookup"><span data-stu-id="38a83-108">It also contains information about which materials to consume and which process to follow to produce the item.</span></span>

<span data-ttu-id="38a83-109">En produksjonsordre går gjennom stadiene i livssyklusen til produksjonen.</span><span class="sxs-lookup"><span data-stu-id="38a83-109">A production order passes through stages of the production life cycle.</span></span> <span data-ttu-id="38a83-110">Når en ordre opprettes, tilordnes statusen **Opprettet**.</span><span class="sxs-lookup"><span data-stu-id="38a83-110">When an order is created, it is assigned the status **Created**.</span></span> <span data-ttu-id="38a83-111">Når en ordre avsluttes, tilordnes statusen **Avsluttet**.</span><span class="sxs-lookup"><span data-stu-id="38a83-111">When an order is finished, it is assigned the status **Ended**.</span></span> <span data-ttu-id="38a83-112">En parameterinnstilling i hvert trinn tillater en bruker å konfigurere hvert trinn.</span><span class="sxs-lookup"><span data-stu-id="38a83-112">A parameter setting in each stage allows a user to configure each step.</span></span> <span data-ttu-id="38a83-113">Innstillingen kan defineres for en enkeltbruker eller for alle brukere.</span><span class="sxs-lookup"><span data-stu-id="38a83-113">The setting can be set up for a single user or for all users.</span></span>

<span data-ttu-id="38a83-114">Produksjonsstykklisten og produksjonsruten er primærenhetene i produksjonsordren.</span><span class="sxs-lookup"><span data-stu-id="38a83-114">The production bill of material and the production route are the main entities of the production order.</span></span> <span data-ttu-id="38a83-115">De er kopiert til produksjonsordren basert på den valgte varen og antallet som skal produseres.</span><span class="sxs-lookup"><span data-stu-id="38a83-115">They are copied to the production order based on the selected item and quantity that are going to be produced.</span></span> <span data-ttu-id="38a83-116">Før produksjonsordren startes kan du redigere produksjonsstykklisten og ruten.</span><span class="sxs-lookup"><span data-stu-id="38a83-116">Before the production order is started, the production bill of material and route can be edited.</span></span>

<span data-ttu-id="38a83-117">En produksjonsordre kan opprettes i følgende scenarier:</span><span class="sxs-lookup"><span data-stu-id="38a83-117">A production order can be created in the following scenarios:</span></span>

-   <span data-ttu-id="38a83-118">Opprettet av hovedplanleggingsutførelse basert på materialbehov.</span><span class="sxs-lookup"><span data-stu-id="38a83-118">Created by master planning execution based on material demand.</span></span>
-   <span data-ttu-id="38a83-119">Opprettet direkte fra en salgsordrelinje eller når en overordnet produksjonsordre er opprettet og estimert (tilknyttet forsyning).</span><span class="sxs-lookup"><span data-stu-id="38a83-119">Created directly from a sales order line or when a higher-level production order is created and estimated (pegged supply).</span></span>
-   <span data-ttu-id="38a83-120">Opprettet manuelt.</span><span class="sxs-lookup"><span data-stu-id="38a83-120">Created manually.</span></span>






[!INCLUDE[footer-include](../../includes/footer-banner.md)]