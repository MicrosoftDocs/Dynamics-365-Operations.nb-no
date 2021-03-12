---
title: Lagermerking med planleggingsoptimalisering
description: Dette emnet inneholder informasjon om alternativene som er tilgjengelige for merking av lager i autoriserte ordrer når du bruker planleggingsoptimalisering.
author: ChristianRytt
manager: tfehr
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MpsIntegrationParameters, MpsFitAnalysis
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 236e1955dd80564e748aab1c595b017cb78e9418
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4983497"
---
# <a name="inventory-marking-with-planning-optimization"></a><span data-ttu-id="11ffd-103">Lagermerking med planleggingsoptimalisering</span><span class="sxs-lookup"><span data-stu-id="11ffd-103">Inventory marking with Planning Optimization</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="11ffd-104">Dette emnet inneholder informasjon om alternativene som er tilgjengelige for merking av lager i autoriserte ordrer når du bruker planleggingsoptimalisering.</span><span class="sxs-lookup"><span data-stu-id="11ffd-104">This topic provides information about the options that are available for marking inventory in firmed orders when you use Planning Optimization.</span></span>

<span data-ttu-id="11ffd-105">*Merking* brukes til å koble til forsyning og behov.</span><span class="sxs-lookup"><span data-stu-id="11ffd-105">*Marking* is used to link supply and demand.</span></span> <span data-ttu-id="11ffd-106">Det ligner på *utligning*, som indikerer hvordan hovedplanleggingen forventes å dekke behov.</span><span class="sxs-lookup"><span data-stu-id="11ffd-106">It resembles *pegging*, which indicates how master planning expects to cover demand.</span></span> <span data-ttu-id="11ffd-107">Fra et planleggingssynspunkt er hovedforskjellen at merking er mer permanent enn utligning.</span><span class="sxs-lookup"><span data-stu-id="11ffd-107">From a planning point of view, the main difference is that marking is more permanent than pegging.</span></span>

<span data-ttu-id="11ffd-108">Merking ble innført for å støtte spesielle etterkalkuleringsscenarioer for først inn, først ut (FIFO) og sist inn, først ut (LIFO).</span><span class="sxs-lookup"><span data-stu-id="11ffd-108">Marking was introduced to support special costing scenarios for first in, first out (FIFO) and last in, first out (LIFO).</span></span> <span data-ttu-id="11ffd-109">Den brukes imidlertid også for noen ikke-etterkalkuleringsscenarioer.</span><span class="sxs-lookup"><span data-stu-id="11ffd-109">However, it's now also used for some non-costing scenarios.</span></span> <span data-ttu-id="11ffd-110">Merking mellom forsyning og behov er valgfritt og nesten permanent.</span><span class="sxs-lookup"><span data-stu-id="11ffd-110">Marking between supply and demand is optional and almost permanent.</span></span> <span data-ttu-id="11ffd-111">Merking kan fjernes manuelt av en bruker, eller den kan fjernes ved å kjøre en nedbryting av salgsordrelinjen der alternativet **Fjern merking** er valgt.</span><span class="sxs-lookup"><span data-stu-id="11ffd-111">Marking can be removed manually by a user, or it can be removed by running a sales order line explosion where the **Remove marking** option is selected.</span></span>

<span data-ttu-id="11ffd-112">Utligning kontrolleres av hovedplanleggingen under dekning for å koble behov med den påkrevde forsyningen.</span><span class="sxs-lookup"><span data-stu-id="11ffd-112">Pegging is controlled by master planning during coverage to link demand with the required supply.</span></span> <span data-ttu-id="11ffd-113">Utligning kan oppdateres for hver planleggingskjøring for å optimalisere forsyningen som kreves for å dekke behovet.</span><span class="sxs-lookup"><span data-stu-id="11ffd-113">Pegging can be updated for each planning run to optimize the supply that is required to cover demand.</span></span> <span data-ttu-id="11ffd-114">Når hovedplanleggingen oppdaterer utligningsinformasjon, respekterer den eksisterende merking.</span><span class="sxs-lookup"><span data-stu-id="11ffd-114">When master planning updates pegging information, it respects any existing marking.</span></span>

<span data-ttu-id="11ffd-115">Utligning starter ved å inkludere relevante merking, lagerreservasjoner og ordrereservasjoner i følgende rekkefølge:</span><span class="sxs-lookup"><span data-stu-id="11ffd-115">Pegging starts by including relevant marking, on-hand reservations, and on-order reservations, in the following sequence:</span></span>

1. <span data-ttu-id="11ffd-116">Merking mellom behov og forsyning</span><span class="sxs-lookup"><span data-stu-id="11ffd-116">Marking between demand and supply</span></span>
1. <span data-ttu-id="11ffd-117">Lagerreservasjoner</span><span class="sxs-lookup"><span data-stu-id="11ffd-117">On-hand reservations</span></span>
1. <span data-ttu-id="11ffd-118">Ordrereservasjoner</span><span class="sxs-lookup"><span data-stu-id="11ffd-118">On-order reservations</span></span>

<span data-ttu-id="11ffd-119">Når du autoriserer en planlagt bestilling, inneholder dialogboksen **Autorisering** et **Oppdater merking**-felt som du kan bruke til å angi merkingsalternativer for ordrene som opprettes under autorisering.</span><span class="sxs-lookup"><span data-stu-id="11ffd-119">When you firm a planned order, the **Firming** dialog box provides an **Update marking** field that you use to set marking options for the orders that are created during firming.</span></span> <span data-ttu-id="11ffd-120">Velg én av følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="11ffd-120">Select one of the following values:</span></span>

- <span data-ttu-id="11ffd-121">**Nei** – Det brukes ingen lagermerking.</span><span class="sxs-lookup"><span data-stu-id="11ffd-121">**No** – No inventory marking is applied.</span></span>
- <span data-ttu-id="11ffd-122">**Standard** – Lagermerking oppdateres i forhold til utligningen.</span><span class="sxs-lookup"><span data-stu-id="11ffd-122">**Standard** – Inventory marking is updated according to the pegging.</span></span> <span data-ttu-id="11ffd-123">En kravordre (behov) merkes mot en innfrielsesordre (forsyning).</span><span class="sxs-lookup"><span data-stu-id="11ffd-123">A requirement order (demand) is marked against a fulfillment order (supply).</span></span> <span data-ttu-id="11ffd-124">Hvis det gjenstår varer på innfrielsesordren, blir den ikke merket, og referanseinformasjonen er tom.</span><span class="sxs-lookup"><span data-stu-id="11ffd-124">If some quantity remains on the fulfillment order, it isn't marked, and the reference information is left blank.</span></span> <span data-ttu-id="11ffd-125">Hvis for eksempel en salgsordre for 100 ea utlignes mot en bestilling for 150 ea, vil referanseinformasjon bare bli tilordnet salgsordren.</span><span class="sxs-lookup"><span data-stu-id="11ffd-125">For example, if a sales order for 100 ea is pegged against a purchase order for 150 ea, reference information will be assigned only to the sales order.</span></span>
- <span data-ttu-id="11ffd-126">**Utvidet** – Både kravordren (behov) og innfrielsesordren (forsyning) merkes, uansett om det gjenstår kvanta på innfrielsesordren.</span><span class="sxs-lookup"><span data-stu-id="11ffd-126">**Extended** – Both the requirement order (demand) and the fulfillment order (supply) are marked, regardless of any quantity that remains on the fulfillment order.</span></span> <span data-ttu-id="11ffd-127">Hvis for eksempel en salgsordre for 100 ea utlignes mot en bestilling for 150 ea, vil referanseinformasjon bli tilordnet både salgsordren og bestillingen.</span><span class="sxs-lookup"><span data-stu-id="11ffd-127">For example, if a sales order for 100 ea is pegged against a purchase order for 150 ea, reference information will be assigned to both the sales order and the purchase order.</span></span>
