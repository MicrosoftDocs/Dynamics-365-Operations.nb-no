---
title: Beregne kapasitetsbelastning på planlagte arbeidsordrer
description: Dette emnet forklarer hvordan du beregner kapasitetsbelastning på planlagte arbeidsordrer i Aktivastyring.
author: josaw1
manager: AnnBe
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: d7684d1a4f78c95ebc7fd0a88f1c7dc7fead0303
ms.sourcegitcommit: fb66731f05207094149a6bc7b8549a4dabbb071a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/22/2019
ms.locfileid: "2652109"
---
# <a name="calculate-capacity-load-on-scheduled-work-orders"></a><span data-ttu-id="cb47b-103">Beregne kapasitetsbelastning på planlagte arbeidsordrer</span><span class="sxs-lookup"><span data-stu-id="cb47b-103">Calculate capacity load on scheduled work orders</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="cb47b-104">Du kan beregne kapasitetsbelastning på planlagte arbeidsordrer for å få en oversikt over arbeidsbelastningen på ressurser for en bestemt periode.</span><span class="sxs-lookup"><span data-stu-id="cb47b-104">You can calculate capacity load on scheduled work orders to get an overview of the work load on resources for a specific period.</span></span> <span data-ttu-id="cb47b-105">Beregninger kan gjøres for følgende ressurser: vedlikeholdsarbeidere, arbeidsgrupper, verktøy og aktiva.</span><span class="sxs-lookup"><span data-stu-id="cb47b-105">Calculations can be made for the following resources: Maintenance workers, worker groups, tools, and assets.</span></span>

1. <span data-ttu-id="cb47b-106">Klikk **Aktivastyring** > **Forespørsel** > **Planlegg** > **Kapasitetsbelastning**.</span><span class="sxs-lookup"><span data-stu-id="cb47b-106">Click **Asset management** > **Inquiries** > **Schedule** > **Capacity load**.</span></span>

2. <span data-ttu-id="cb47b-107">I dialogboksen **Beregn kapasitetsbelastning** > **Vis**-feltet velger du hvilken belastningstype du vi vil beregne: **Kapasitet**, **Reservert** eller **Rest**.</span><span class="sxs-lookup"><span data-stu-id="cb47b-107">In the **Calculate capacity load** dialog > **Show** field, select which load type you want to calculate: **Capacity**, **Reserved**, or **Remainder**.</span></span>

3. <span data-ttu-id="cb47b-108">Velg **Ja** på veksleknappen **Hopp over null** hvis du ikke vil vise resultater med null timer.</span><span class="sxs-lookup"><span data-stu-id="cb47b-108">Select **Yes** on the **Skip zero** toggle button if you do not want to show results containing zero.</span></span>

4. <span data-ttu-id="cb47b-109">Velg ressurstypene du vil beregne kapasitetsbelastningen for, ved å velge **Ja** på de aktuelle veksleknappene: **Arbeider**, **Vedlikeholdspersongruppe**, **Verktøy** og **Aktivum**.</span><span class="sxs-lookup"><span data-stu-id="cb47b-109">Select the resource types for which you want to calculate capacity load by selecting **Yes** on the relevant toggle buttons: **Worker**, **Maintenance worker group**, **Tool**, and **Asset**.</span></span>

5. <span data-ttu-id="cb47b-110">Velg startdatoen for beregningen i **Fra dato**-feltet.</span><span class="sxs-lookup"><span data-stu-id="cb47b-110">Select the start date for the calculation in the **From date** field.</span></span>

6. <span data-ttu-id="cb47b-111">I **Intervalltype**-feltet velger du intervallet for beregningen: **Dag**, **Uke**, **Måned** eller **Kvartal**.</span><span class="sxs-lookup"><span data-stu-id="cb47b-111">In the **Interval type** field, select the interval for the calculation: **Day**, **Week**, **Month**, or **Quarter**.</span></span>

7. <span data-ttu-id="cb47b-112">I **Periodefrekvens**-feltet setter du inn antall intervaller du vil beregne.</span><span class="sxs-lookup"><span data-stu-id="cb47b-112">In the **Period frequency** field, insert the number of intervals you want to calculate.</span></span> <span data-ttu-id="cb47b-113">Hvis du for eksempel har valgt **Dag** som intervalltype, og du setter inn tallet "5" i dette feltet, vil det bli opprettet en beregning på fem dager fra startdatoen.</span><span class="sxs-lookup"><span data-stu-id="cb47b-113">For example, if you have selected **Day** as the interval type, and you enter the number "5" in this field, a calculation of five days from the start date will be made.</span></span>

8. <span data-ttu-id="cb47b-114">Klikk på **OK** for å starte beregningen.</span><span class="sxs-lookup"><span data-stu-id="cb47b-114">Click **OK** to start the calculation.</span></span>

<span data-ttu-id="cb47b-115">Figuren nedenfor viser resultatet av en beregning som dekker tre uker for belastningstypen **Reservert**.</span><span class="sxs-lookup"><span data-stu-id="cb47b-115">The figure below shows the result of a calculation covering three weeks for the load type **Reserved**.</span></span>

![Figur 1](media/08-work-order-scheduling.png)

[!NOTE]
<span data-ttu-id="cb47b-117">Hvis du velger belastningstypene **Kapasitet** eller **Rest** for beregningen, vil det samme resultatet vises hvis det ikke er gjort reservasjoner for ressursene i den valgte perioden.</span><span class="sxs-lookup"><span data-stu-id="cb47b-117">If you select the load types **Capacity** or **Remainder** for your calculation, the same result will be displayed if no reservations have been made for the resources in the selected period.</span></span>

<span data-ttu-id="cb47b-118">Se [Beregne kapasitetsbelastning](../capacity-planning/calculate-capacity-load.md) for informasjon om hvordan du beregner kapasitetsbelastning på vedlikeholdsplanlinjer og ikke planlagte arbeidsordrer.</span><span class="sxs-lookup"><span data-stu-id="cb47b-118">For information about how to calculate capacity load on maintenance schedule lines and not scheduled work orders, refer to [Calculate capacity load](../capacity-planning/calculate-capacity-load.md).</span></span>

