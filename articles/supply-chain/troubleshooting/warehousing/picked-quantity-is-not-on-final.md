---
title: Du kan ikke bekrefte en forsendelse fordi varer ikke har blitt plukket
description: Du kan ikke bekrefte en forsendelse fordi varer ikke har blitt plukket
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 23a517e7769dc86ebec30e4f17c62172a6ad8801
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938525"
---
# <a name="you-cant-confirm-a-shipment-because-items-havent-been-picked"></a><span data-ttu-id="4a267-103">Du kan ikke bekrefte en forsendelse fordi varer ikke har blitt plukket</span><span class="sxs-lookup"><span data-stu-id="4a267-103">You can't confirm a shipment because items haven't been picked</span></span>

<span data-ttu-id="4a267-104">Feilkode: LoadNotPickedAndMovedToFinalShippingLocation</span><span class="sxs-lookup"><span data-stu-id="4a267-104">Error code: LoadNotPickedAndMovedToFinalShippingLocation</span></span>

## <a name="symptoms"></a><span data-ttu-id="4a267-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="4a267-105">Symptoms</span></span>

<span data-ttu-id="4a267-106">Når du prøver å bekrefte en forsendelse, viser systemet følgende feilmelding:</span><span class="sxs-lookup"><span data-stu-id="4a267-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="4a267-107">Noen av varene som trengs for lasten %1, har ennå ikke blitt plukket og flyttet til den endelige forsendelseslokasjonen.</span><span class="sxs-lookup"><span data-stu-id="4a267-107">Some of the items that are needed for load %1 have not yet been picked and moved to the final shipping location.</span></span>

<span data-ttu-id="4a267-108">Derfor kan du ikke bekrefte forsendelsen for belastningen.</span><span class="sxs-lookup"><span data-stu-id="4a267-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="4a267-109">Årsak</span><span class="sxs-lookup"><span data-stu-id="4a267-109">Cause</span></span>

<span data-ttu-id="4a267-110">Belastningen eller forsendelsen kan ikke bekreftes i gjeldende tilstand, fordi det kan hende at én av følgende betingelser finnes:</span><span class="sxs-lookup"><span data-stu-id="4a267-110">The load or shipment can't be confirmed in its current state because one of the following conditions might exist:</span></span>

- <span data-ttu-id="4a267-111">Det relaterte arbeidet er ennå ikke plukket og flyttet til den endelige forsendelseslokasjonen.</span><span class="sxs-lookup"><span data-stu-id="4a267-111">The related work hasn't yet been picked and moved to the final shipping location.</span></span>
- <span data-ttu-id="4a267-112">Det plukkede arbeidsantallet samsvarer ikke med det opprettede arbeidsantallet på belastningslinjen.</span><span class="sxs-lookup"><span data-stu-id="4a267-112">The picked work quantity doesn't match the created work quantity on the load line.</span></span>

## <a name="resolution"></a><span data-ttu-id="4a267-113">Oppløsning</span><span class="sxs-lookup"><span data-stu-id="4a267-113">Resolution</span></span>

<span data-ttu-id="4a267-114">Kontroller de tilknyttede salgsordrene eller overføringsordrene for belastningen eller forsendelsen.</span><span class="sxs-lookup"><span data-stu-id="4a267-114">Check the related sales orders or transfer orders for the load or shipment.</span></span> <span data-ttu-id="4a267-115">Kontroller at alt tilknyttet arbeid er fullført på den endelige forsendelseslokasjonen, og at antallet samsvarer.</span><span class="sxs-lookup"><span data-stu-id="4a267-115">Make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>

1. <span data-ttu-id="4a267-116">Gå til **Lagerstyring \> Laster \> Alle laster**.</span><span class="sxs-lookup"><span data-stu-id="4a267-116">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="4a267-117">Velg belastningen som forsendelsen ikke kan bekreftes for.</span><span class="sxs-lookup"><span data-stu-id="4a267-117">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="4a267-118">I hurtigfanen **Lastlinjer** velger du lastlinjen.</span><span class="sxs-lookup"><span data-stu-id="4a267-118">On the **Load lines** FastTab, select the load line.</span></span>
1. <span data-ttu-id="4a267-119">Legg merke til verdien i feltet **Antall for arbeid opprettet**.</span><span class="sxs-lookup"><span data-stu-id="4a267-119">Make a note of the value of the **Work created quantity** field.</span></span>
1. <span data-ttu-id="4a267-120">I handlingsruten, i fanen **Laster** i gruppen **Relatert informasjon**, velger du **Arbeid**.</span><span class="sxs-lookup"><span data-stu-id="4a267-120">On the Action Pane, on the **Loads** tab, in the **Related information** group, select **Work**.</span></span>
1. <span data-ttu-id="4a267-121">Kontroller at arbeidet er fullført på det endelige forsendelsesstedet, og at det plukkede arbeidsantallet samsvarer med det opprettede arbeidsantallet på belastningslinjen.</span><span class="sxs-lookup"><span data-stu-id="4a267-121">Verify that the work has been completed at the final shipping location, and that the picked work quantity matches the created work quantity on the load line.</span></span>
1. <span data-ttu-id="4a267-122">Gjenta denne fremgangsmåten for alle belastningslinjer for å være sikker på at alle kriteriene er oppfylt.</span><span class="sxs-lookup"><span data-stu-id="4a267-122">Repeat this procedure for all load lines to make sure that all criteria are met.</span></span>
