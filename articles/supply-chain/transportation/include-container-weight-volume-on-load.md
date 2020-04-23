---
title: Inkludere containervekt og -volum for last
description: Dette emnet beskriver hvordan sette opp og bruke funksjonalitet for å inkludere containervekt og -volum for last.
author: pjacobse
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSRateRouteWorkbench, TMSDriverLogListPage, TMSTransportationTender
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: pjacobse
ms.search.validFrom: 2017-09-20
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7e6b29bf2e42ea2df3d36f39fa577078009aa584
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/02/2020
ms.locfileid: "3206294"
---
# <a name="include-container-weight-and-volume-on-load"></a><span data-ttu-id="6ce07-103">Inkludere containervekt og -volum for last</span><span class="sxs-lookup"><span data-stu-id="6ce07-103">Include container weight and volume on load</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6ce07-104">Funksjonaliteten for å inkludere containerverk- og volum for en last gir en klar fremstilling av totalvekt og volum av beholdere og gjenstander som går på en last.</span><span class="sxs-lookup"><span data-stu-id="6ce07-104">The functionality for including the container weight and volume on a load gives a clear representation of the total weight and volume of containers and items that are going on a load.</span></span>

<span data-ttu-id="6ce07-105">En last inneholder en enkelt forsendelse eller flere forsendelser, og disse forsendelsene inneholder forskjellige elementer som tilhører en enkelt salgsordre eller flere salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="6ce07-105">A load contains a single shipment or multiple shipments, and these shipments contain distinct items that belong to a single sales order or multiple sales orders.</span></span> <span data-ttu-id="6ce07-106">Varene er lagret i en container, og containere lastes på en last.</span><span class="sxs-lookup"><span data-stu-id="6ce07-106">The items are stored inside a container, and containers are loaded on a load.</span></span> <span data-ttu-id="6ce07-107">Elementer som er utenfor en container kan også være en del av en last.</span><span class="sxs-lookup"><span data-stu-id="6ce07-107">Items that are outside a container can also be part of a load.</span></span> <span data-ttu-id="6ce07-108">Basert på disse forholdene, beregner systemet verdier for vekt og volum på lasten ved å vurdere vekten og volumet av både beholdere og gjenstander.</span><span class="sxs-lookup"><span data-stu-id="6ce07-108">Based on these conditions, the system calculates values for the weight and volume on the load by considering the weight and volume of both containers and items.</span></span>

<span data-ttu-id="6ce07-109">Hvis de beregnede verdiene ikke er presise, kan du justere dem ved å angi de faktiske verdiene for vekt og volum på lasten.</span><span class="sxs-lookup"><span data-stu-id="6ce07-109">If the calculated values aren’t precise, you can adjust them by entering the actual values for the weight and volume on the load.</span></span> <span data-ttu-id="6ce07-110">Verdiene for vekt og volum brukes i transportstyringsprosesser.</span><span class="sxs-lookup"><span data-stu-id="6ce07-110">The values for the weight and volume are used in transportation management processes.</span></span> <span data-ttu-id="6ce07-111">For eksempel brukes verdiene i arbeidsbenken for rutesats, der de hjelper til med å definere hastigheten og ruten for last, og de brukes også til transportanbud og innsjekking av sjåføren.</span><span class="sxs-lookup"><span data-stu-id="6ce07-111">For example, the values are used in the rate route workbench, where they help define the rate and route for loads, and they are also used for transportation tenders and driver check-in.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="6ce07-112">Der det er aktuelt</span><span class="sxs-lookup"><span data-stu-id="6ce07-112">Where it applies</span></span>

<span data-ttu-id="6ce07-113">Funksjonaliteten for å inkludere containerens vekt og volum på en last gjelder i transporthåndteringsprosesser, som for eksempel arbeidsbenken for rutesats, transportanbud og innsjekking av sjåføren.</span><span class="sxs-lookup"><span data-stu-id="6ce07-113">The functionality for including the container weight and volume on a load applies in transportation management processes, such as the rate route workbench, transportation tenders, and driver check-in.</span></span>

## <a name="how-it-is-set-up"></a><span data-ttu-id="6ce07-114">Hvordan det er satt opp</span><span class="sxs-lookup"><span data-stu-id="6ce07-114">How it is set up</span></span>

<span data-ttu-id="6ce07-115">Antall containere som bør vurderes for en last, beregnes ut fra vekt og volum av containeren, og prosenten av containeren som brukes.</span><span class="sxs-lookup"><span data-stu-id="6ce07-115">The number of containers that should be considered for a load is calculated based on the weight and volume of the container, and on the percentage of the container is used.</span></span>

-   <span data-ttu-id="6ce07-116">For å sette opp vekt og volum for en container, klikk **Lagerstyring** \> **Oppsett** \> **Containere** \> **Containertyper**.</span><span class="sxs-lookup"><span data-stu-id="6ce07-116">To set the weight and volume for a container, click **Warehouse management** \> **Setup** \> **Containers** \> **Container types**.</span></span>

-   <span data-ttu-id="6ce07-117">For å angi containerutnyttelsesprosenten, klikk **Lagerstyring** \> **Oppsett** \> **Containere** \> **Containergrupper**, og skriv inn en verdi i feltet **Utnyttelsesprosent for container**.</span><span class="sxs-lookup"><span data-stu-id="6ce07-117">To set the container utilization percentage, click **Warehouse management** \> **Setup** \> **Containers** \> **Container groups**, and then enter a value in the **Container utilization percentage** field.</span></span>
