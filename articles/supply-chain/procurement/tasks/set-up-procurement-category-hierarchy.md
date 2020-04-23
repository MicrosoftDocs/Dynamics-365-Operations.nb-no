---
title: Definere et innkjøpskategorihierarki
description: Denne prosedyren viser deg hvordan du oppretter nye noder i et innkjøpskategorihierarki og hvordan du konfigurerer en innkjøpskategori som skal brukes i en innkjøpsprosess.
author: mkirknel
manager: tfehr
ms.date: 06/21/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: eaab2093eb2531b63f27717d828f7064a8f9ed1d
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/02/2020
ms.locfileid: "3207514"
---
# <a name="set-up-a-procurement-category-hierarchy"></a><span data-ttu-id="f7a7a-103">Definere et innkjøpskategorihierarki</span><span class="sxs-lookup"><span data-stu-id="f7a7a-103">Set up a procurement category hierarchy</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f7a7a-104">Denne prosedyren viser deg hvordan du oppretter nye noder i et innkjøpskategorihierarki og hvordan du konfigurerer en innkjøpskategori som skal brukes i en innkjøpsprosess.</span><span class="sxs-lookup"><span data-stu-id="f7a7a-104">This procedure shows you how to create new nodes in a procurement category hierarchy and how to configure a procurement category to be used in a procurement process.</span></span> <span data-ttu-id="f7a7a-105">Disse oppgavene vil vanligvis utføres av en innkjøpssjef.</span><span class="sxs-lookup"><span data-stu-id="f7a7a-105">These tasks would typically be carried out by a Purchasing manager.</span></span> <span data-ttu-id="f7a7a-106">Før du starter denne fremgangsmåten, må det være et kategorihierarki av typen Innkjøp.</span><span class="sxs-lookup"><span data-stu-id="f7a7a-106">Before you can start this procedure, there must be a category hierarchy of type Procurement.</span></span> <span data-ttu-id="f7a7a-107">Hvis du bruker en demonstrasjonsdataselskap, kan du kjøre denne prosedyren i firmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="f7a7a-107">If you're using a demo data company, you can run this procedure in the USMF company.</span></span>


## <a name="add-a-new-procurement-category"></a><span data-ttu-id="f7a7a-108">Legge til en ny innkjøpskategori</span><span class="sxs-lookup"><span data-stu-id="f7a7a-108">Add a new procurement category</span></span>
1. <span data-ttu-id="f7a7a-109">Gå til **navigasjonsruten > Moduler > Innkjøp og leverandører > Forsendelse > Innkjøpskategorier**.</span><span class="sxs-lookup"><span data-stu-id="f7a7a-109">Go to **Navigation pane > Modules > Procurement and sourcing > Consignment > Procurement categories**.</span></span>
2. <span data-ttu-id="f7a7a-110">I handlingsruten velger du **Rediger kategorihierarki**.</span><span class="sxs-lookup"><span data-stu-id="f7a7a-110">On the action pane, select **Edit category hierarchy**.</span></span> <span data-ttu-id="f7a7a-111">Gjeldende innkjøpskategorihierarki vises til venstre på siden.</span><span class="sxs-lookup"><span data-stu-id="f7a7a-111">The current procurement category hierarchy is displayed in the left side of the page.</span></span> <span data-ttu-id="f7a7a-112">Du er i ferd med å endre hierarkiet.</span><span class="sxs-lookup"><span data-stu-id="f7a7a-112">You  are about to modify the hierarchy.</span></span>  
3. <span data-ttu-id="f7a7a-113">I handlingsruten velger du **Ny kategorinode**.</span><span class="sxs-lookup"><span data-stu-id="f7a7a-113">On the action pane, select **New category node**.</span></span> <span data-ttu-id="f7a7a-114">Den øverste noden velges som standard.</span><span class="sxs-lookup"><span data-stu-id="f7a7a-114">The system selects the top node by default.</span></span> <span data-ttu-id="f7a7a-115">Hvis du bruker denne fremgangsmåten som oppgaveveiledning, kan du klikke knappen Lås opp og velge en annen overordnet node som du vil sette inn den ny noden i.</span><span class="sxs-lookup"><span data-stu-id="f7a7a-115">If you are running this procedure as a task guide, you can click the Unlock button and select another parent node to insert your new node into.</span></span> <span data-ttu-id="f7a7a-116">Når det er gjort, låser du oppgaveveiledningen på nytt, og klikker deretter Ny kategorinode.</span><span class="sxs-lookup"><span data-stu-id="f7a7a-116">Once that is done, lock the task guide again and then click New category node.</span></span>  
4. <span data-ttu-id="f7a7a-117">Skriv inn en verdi i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="f7a7a-117">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="f7a7a-118">Skriv inn en verdi i **Beskrivelse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="f7a7a-118">In the **Description** field, type a value.</span></span>
6. <span data-ttu-id="f7a7a-119">Skriv inn en verdi i feltet **Egendefinert navn**.</span><span class="sxs-lookup"><span data-stu-id="f7a7a-119">In the **Friendly name** field, type a value.</span></span> <span data-ttu-id="f7a7a-120">Det egendefinerte navnet er valgfritt.</span><span class="sxs-lookup"><span data-stu-id="f7a7a-120">The friendly name is optional.</span></span> <span data-ttu-id="f7a7a-121">Det vises i kategorioppslag sammen med navnet på kategorien.</span><span class="sxs-lookup"><span data-stu-id="f7a7a-121">It will be displayed in category lookups together with the category name.</span></span>  
7. <span data-ttu-id="f7a7a-122">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="f7a7a-122">Select **Save**.</span></span>

## <a name="add-products-to-your-new-procurement-category"></a><span data-ttu-id="f7a7a-123">Legge til produkter i den nye innkjøpskategorien</span><span class="sxs-lookup"><span data-stu-id="f7a7a-123">Add products to your new procurement category</span></span>
1. <span data-ttu-id="f7a7a-124">Gå til **Innkjøp og leverandører > Forsendelse > Innkjøpskategorier**.</span><span class="sxs-lookup"><span data-stu-id="f7a7a-124">Go to **Procurement and sourcing > Consignment > Procurement categories**.</span></span> <span data-ttu-id="f7a7a-125">Merk noden du nettopp la til.</span><span class="sxs-lookup"><span data-stu-id="f7a7a-125">Select the node you just added.</span></span> <span data-ttu-id="f7a7a-126">Hvis du kjører denne prosedyren som en oppgaveveiledning, må du kanskje låse opp i oppgaveveiledningen for å velge noden.</span><span class="sxs-lookup"><span data-stu-id="f7a7a-126">If you're running this procedure as a task guide you might need to unlock the task guide to select the node.</span></span>  
2. <span data-ttu-id="f7a7a-127">Aktiver/deaktiver visning av delen **Produkter**.</span><span class="sxs-lookup"><span data-stu-id="f7a7a-127">Toggle the expansion of the **Products** section.</span></span>
3. <span data-ttu-id="f7a7a-128">Velg **Legg til** for å knytte produkter til innkjøpskategorien.</span><span class="sxs-lookup"><span data-stu-id="f7a7a-128">Select **Add** to associate products with the procurement category.</span></span>
4. <span data-ttu-id="f7a7a-129">Velg produktene du vil legge til i innkjøpskategorien.</span><span class="sxs-lookup"><span data-stu-id="f7a7a-129">Select the products you want to add to the procurement category.</span></span>
5. <span data-ttu-id="f7a7a-130">Velg pilen for å legge til produktene i **Valgt**-tabellen.</span><span class="sxs-lookup"><span data-stu-id="f7a7a-130">Select the arrow to add the products to the **Selected** table.</span></span>
6. <span data-ttu-id="f7a7a-131">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="f7a7a-131">Select **OK**.</span></span>
