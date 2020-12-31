---
title: Opprette en leiegruppe
description: Dette emnet forklarer hvordan du konfigurerer leiegrupper. Leiegrupper kreves for å opprette nye leieavtaler.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: f8512a59d0e9935090f97a0f0237bfefc8473955
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/28/2020
ms.locfileid: "4446595"
---
# <a name="create-a-lease-group"></a><span data-ttu-id="324ef-104">Opprette en leiegruppe</span><span class="sxs-lookup"><span data-stu-id="324ef-104">Create a lease group</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="324ef-105">Dette emnet forklarer hvordan du konfigurerer leiegrupper.</span><span class="sxs-lookup"><span data-stu-id="324ef-105">This topic explains how to set up lease groups.</span></span> <span data-ttu-id="324ef-106">Leiegrupper kreves for å opprette nye leieavtaler.</span><span class="sxs-lookup"><span data-stu-id="324ef-106">Lease groups are required to create new leases.</span></span> <span data-ttu-id="324ef-107">Leietablåer er knyttet til hver leiegruppe.</span><span class="sxs-lookup"><span data-stu-id="324ef-107">Lease books are associated with each lease group.</span></span> <span data-ttu-id="324ef-108">Leietablåer fastsetter standardtablåene som må opprettes for hver leieavtale.</span><span class="sxs-lookup"><span data-stu-id="324ef-108">Lease books determine the default books that must be created for each lease.</span></span> <span data-ttu-id="324ef-109">Du kan tilordne bestemte kontoer til en leiegruppe på siden **Parametere for leiepostering**.</span><span class="sxs-lookup"><span data-stu-id="324ef-109">You can assign specific accounts to a lease group on the **Lease posting parameters** page.</span></span>

## <a name="create-a-lease-book-and-add-a-lease-group"></a><span data-ttu-id="324ef-110">Opprette et leietablå og legge til en leiegruppe</span><span class="sxs-lookup"><span data-stu-id="324ef-110">Create a lease book and add a lease group</span></span>

1. <span data-ttu-id="324ef-111">Gå til **Aktivaleie \> Oppsett \> Leiegrupper**.</span><span class="sxs-lookup"><span data-stu-id="324ef-111">Go to **Asset leasing \> Setup \> Lease groups**.</span></span>
2. <span data-ttu-id="324ef-112">I handlingsruten velger du **Ny** for legge til en leiegruppe.</span><span class="sxs-lookup"><span data-stu-id="324ef-112">On the Action Pane, select **New** to add a lease group.</span></span> <span data-ttu-id="324ef-113">Det blir lagt til en linje i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="324ef-113">A line is added to the grid.</span></span>
3. <span data-ttu-id="324ef-114">Angi en verdi i feltet **Leiegruppe** på den nye linjen.</span><span class="sxs-lookup"><span data-stu-id="324ef-114">On the new line, in the **Lease group** field, enter a value.</span></span>
4. <span data-ttu-id="324ef-115">Angi en verdi i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="324ef-115">In the **Description** field, enter a value.</span></span>

<span data-ttu-id="324ef-116">Informasjonen du nettopp har registrert, legges til i feltet **Leiegruppe** på siden **Legg til leieavtale**.</span><span class="sxs-lookup"><span data-stu-id="324ef-116">The information that you just entered is added to the **Lease group** field on the **Add lease** page.</span></span>

## <a name="associate-a-book-with-a-lease-group"></a><span data-ttu-id="324ef-117">Knytte et tablå til en leiegruppe</span><span class="sxs-lookup"><span data-stu-id="324ef-117">Associate a book with a lease group</span></span>

<span data-ttu-id="324ef-118">Etter at du har opprettet leiegrupper, kan du tilordne tablåer til hver gruppe.</span><span class="sxs-lookup"><span data-stu-id="324ef-118">After you create lease groups, you can assign books to each group.</span></span> <span data-ttu-id="324ef-119">Når du oppretter en leieavtale og tilordner den til en leiegruppe, oppretter systemet et sett med tidsplaner for hvert tablå som er tilknyttet denne leiegruppen.</span><span class="sxs-lookup"><span data-stu-id="324ef-119">When you create a lease and assign it to a lease group, the system creates a set of schedules for each book that is associated with that lease group.</span></span>

> [!NOTE]
> <span data-ttu-id="324ef-120">Tablåer må konfigureres før de kan tilordnes til en leiegruppe.</span><span class="sxs-lookup"><span data-stu-id="324ef-120">Books must be set up before they can be assigned to a lease group.</span></span>

1. <span data-ttu-id="324ef-121">Gå til **Aktivaleie \> Oppsett \> Leiegruppe**.</span><span class="sxs-lookup"><span data-stu-id="324ef-121">Go to **Asset leasing \> Setup \> Lease group**.</span></span>
2. <span data-ttu-id="324ef-122">Velg en leiegruppe, og velg deretter **Tablåer**.</span><span class="sxs-lookup"><span data-stu-id="324ef-122">Select a lease group, and then select **Books**.</span></span>
3. <span data-ttu-id="324ef-123">Velg **Nytt**, og velg deretter tablået som skal tilordnes til leiegruppen, i feltet **Tablåtype**.</span><span class="sxs-lookup"><span data-stu-id="324ef-123">Select **New**, and then, in the **Book type** field, select the book to assign to the lease group.</span></span> <span data-ttu-id="324ef-124">Du kan tilordne flere tablåer til en leiegruppe hvis en leieavtale må gjøres rede for på forskjellige måter.</span><span class="sxs-lookup"><span data-stu-id="324ef-124">You can assign multiple books to a lease group if a lease must be accounted for in different ways.</span></span>
