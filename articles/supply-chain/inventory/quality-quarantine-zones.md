---
title: Karantenesoner for avvik
description: Dette emnet beskriver hvordan du oppretter og bruker karantenesoner for avvik.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventQuarantineZone
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 93ca74ec4586fffa3b9156aadab887629283b98a
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956778"
---
# <a name="quarantine-zones-for-nonconformances"></a><span data-ttu-id="09007-103">Karantenesoner for avvik</span><span class="sxs-lookup"><span data-stu-id="09007-103">Quarantine zones for nonconformances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="09007-104">Dette emnet beskriver hvordan du oppretter og bruker karantenesoner for avvik.</span><span class="sxs-lookup"><span data-stu-id="09007-104">This topic describes how to create and use quarantine zones for nonconformances.</span></span>

<span data-ttu-id="09007-105">Du kan bruke **Karantenesoner**-siden til å definere soner som kan tilordnes til et avvik.</span><span class="sxs-lookup"><span data-stu-id="09007-105">You use the **Quarantine zones** page to define zones that can be assigned to nonconformances.</span></span> <span data-ttu-id="09007-106">Når du oppretter et avvik, kan du definere feltene **Karantenesone** og **Karantenetype** i kategorien **Generelt** på **Avvik**-siden.</span><span class="sxs-lookup"><span data-stu-id="09007-106">When you create a nonconformance, you can set the **Quarantine zone** and **Quarantine type** fields on the **General** tab of the **Non conformances** page.</span></span> <span data-ttu-id="09007-107">Feltet **Karantenesone** angir vanligvis området eller lokasjonen der varen finnes.</span><span class="sxs-lookup"><span data-stu-id="09007-107">The **Quarantine zone** field typically indicates the area or location where the item is located.</span></span> <span data-ttu-id="09007-108">**Karantenetype**-feltet definerer varen som enten *Begrenset bruk* eller *Kan ikke brukes*.</span><span class="sxs-lookup"><span data-stu-id="09007-108">The **Quarantine type** field defines the item as either *Restricted usage* or *Unusable*.</span></span>

<span data-ttu-id="09007-109">Når du skriver ut en avviks- eller rettelsesrapport for et avvik, kan du vise karantenesonen der varen finnes.</span><span class="sxs-lookup"><span data-stu-id="09007-109">When you print a nonconformance or corrections report for a nonconformance, you can view the quarantine zone where the item is located.</span></span>

<span data-ttu-id="09007-110">Du kan også skrive ut en avviksbrikke for et avvik.</span><span class="sxs-lookup"><span data-stu-id="09007-110">You can also print a nonconformance tag for a nonconformance.</span></span> <span data-ttu-id="09007-111">Denne rapporten viser den tilordnede karantenesonen og informasjon om bruk, for å gi veiledning om hvordan materialer med defekter skal håndteres.</span><span class="sxs-lookup"><span data-stu-id="09007-111">This report shows the assigned quarantine zone and information about usage to provide guidance about how defective material should be handled.</span></span> <span data-ttu-id="09007-112">Karantenesonene kan tilsvare lagerlokasjoner eller operasjonsressurser.</span><span class="sxs-lookup"><span data-stu-id="09007-112">The quarantine zones might correspond to inventory locations or operations resources.</span></span>

## <a name="examples-of-quarantine-zones"></a><span data-ttu-id="09007-113">Eksempler på karantenesoner</span><span class="sxs-lookup"><span data-stu-id="09007-113">Examples of quarantine zones</span></span>

### <a name="example-1"></a><span data-ttu-id="09007-114">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="09007-114">Example 1</span></span>

<span data-ttu-id="09007-115">Du jobber i et produksjonsfirma for elektronikk, som produserer og distribuerer TV-er, høyttalere og mediespillere.</span><span class="sxs-lookup"><span data-stu-id="09007-115">You work at an electronics manufacturing company that produces and distributes televisions, speakers, and media players.</span></span> <span data-ttu-id="09007-116">I dette tilfellet kan du konfigurere en karantenesone til å representere hver produkttype.</span><span class="sxs-lookup"><span data-stu-id="09007-116">In this case, you can configure a quarantine zone to represent each type of product.</span></span>

### <a name="example-2"></a><span data-ttu-id="09007-117">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="09007-117">Example 2</span></span>

<span data-ttu-id="09007-118">Tre bokser og to reoler brukes til å lagre varer som er avvik.</span><span class="sxs-lookup"><span data-stu-id="09007-118">Three bins and two racks are used to store items that are nonconforming.</span></span> <span data-ttu-id="09007-119">I dette tilfellet kan du konfigurere fem karantenesoner, én for hver boks og hver reol.</span><span class="sxs-lookup"><span data-stu-id="09007-119">In this case, you can configure five quarantine zones, one for each bin and each rack.</span></span>

## <a name="create-a-quarantine-zone"></a><span data-ttu-id="09007-120">Opprette en karantenesone</span><span class="sxs-lookup"><span data-stu-id="09007-120">Create a quarantine zone</span></span>

1. <span data-ttu-id="09007-121">Gå til **Lagerstyring \> Oppsett \> Kvalitetsstyring \> Karantenesoner**.</span><span class="sxs-lookup"><span data-stu-id="09007-121">Go to **Inventory management \> Setup \> Quality management \> Quarantine zones**.</span></span>
1. <span data-ttu-id="09007-122">I handlingsruten velger du **Ny** for å legge til en rad i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="09007-122">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="09007-123">Angi deretter følgende felter for den nye raden:</span><span class="sxs-lookup"><span data-stu-id="09007-123">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="09007-124">**Karantenesone** – Angi en unik ID eller et navn for karantenesonen.</span><span class="sxs-lookup"><span data-stu-id="09007-124">**Quarantine zone** – Enter a unique ID or name for the quarantine zone.</span></span>
    - <span data-ttu-id="09007-125">**Beskrivelse** – Angi en detaljert beskrivelse av karantenesonen.</span><span class="sxs-lookup"><span data-stu-id="09007-125">**Description** – Enter a detailed description of the quarantine zone.</span></span>

1. <span data-ttu-id="09007-126">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="09007-126">Close the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="09007-127">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="09007-127">Additional resources</span></span>

- [<span data-ttu-id="09007-128">Oversikt over kvalitetsstyring</span><span class="sxs-lookup"><span data-stu-id="09007-128">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="09007-129">Aktivere kvalitets- og avviksstyring</span><span class="sxs-lookup"><span data-stu-id="09007-129">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="09007-130">Arbeidere som er ansvarlige for å godkjenne avvik</span><span class="sxs-lookup"><span data-stu-id="09007-130">Workers responsible for approving nonconformances</span></span>](quality-responsible-workers.md)
- [<span data-ttu-id="09007-131">Problemtyper for avvik</span><span class="sxs-lookup"><span data-stu-id="09007-131">Problem types for nonconformances</span></span>](quality-quarantine-zones.md)
- [<span data-ttu-id="09007-132">Diagnosetyper for avvik</span><span class="sxs-lookup"><span data-stu-id="09007-132">Diagnostic types for nonconformances</span></span>](quality-diagnostic-types.md)
- [<span data-ttu-id="09007-133">Kvalitetsendringer for avvik</span><span class="sxs-lookup"><span data-stu-id="09007-133">Quality charges for nonconformances</span></span>](quality-charges.md)
- [<span data-ttu-id="09007-134">Operasjoner for avvik</span><span class="sxs-lookup"><span data-stu-id="09007-134">Operations for nonconformances</span></span>](quality-operations.md)
- [<span data-ttu-id="09007-135">Kvalitetsstyring for lagerprosesser</span><span class="sxs-lookup"><span data-stu-id="09007-135">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]