---
title: Produkteiere
description: Dette emnet inneholder informasjon om produkteiere. En produkteier er en gruppe brukere som har ansvaret for bestemte produkter. Bare medlemmer av gruppen kan frigi disse produktene. Produkteieren kan også brukes i godkjenningsarbeidsflyten.
author: t-benebo
manager: tfehr
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EngChgProductOwner
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 4308020d66995d857e547be47216cb82caacf035
ms.sourcegitcommit: 5f21cfde36c43887ec209bba4a12b830a1746fcf
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/29/2020
ms.locfileid: "4434857"
---
# <a name="product-owners"></a><span data-ttu-id="11c05-106">Produkteiere</span><span class="sxs-lookup"><span data-stu-id="11c05-106">Product owners</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="11c05-107">Produkteieren er en gruppe brukere som har ansvaret for bestemte produkter.</span><span class="sxs-lookup"><span data-stu-id="11c05-107">The product owner is a group of users who are responsible for specific products.</span></span> <span data-ttu-id="11c05-108">Når en produkteiergruppe tilordnes til et produkt, kan bare medlemmene av denne gruppen frigi produktet.</span><span class="sxs-lookup"><span data-stu-id="11c05-108">When a product owner group is assigned to a product, only the members of that group can release the product.</span></span> <span data-ttu-id="11c05-109">Produkteieren kan også brukes i godkjenningsarbeidsflyten i behandling av teknisk endring.</span><span class="sxs-lookup"><span data-stu-id="11c05-109">The product owner can also be used in the approval workflow in engineering change management.</span></span>

<span data-ttu-id="11c05-110">Produkteiere er globale innstillinger.</span><span class="sxs-lookup"><span data-stu-id="11c05-110">Product owners are global settings.</span></span> <span data-ttu-id="11c05-111">De er derfor tilgjengelige for alle juridiske enheter.</span><span class="sxs-lookup"><span data-stu-id="11c05-111">Therefore, they are available to all legal entities.</span></span>

## <a name="create-a-product-owner-group"></a><span data-ttu-id="11c05-112">Opprett en produkteiergruppe</span><span class="sxs-lookup"><span data-stu-id="11c05-112">Create a product owner group</span></span>

<span data-ttu-id="11c05-113">Følg denne fremgangsmåten for å opprette en produkteiergruppe og legge til medlemmer i den:</span><span class="sxs-lookup"><span data-stu-id="11c05-113">To create a product owner group and add members to it, follow these steps.</span></span>

1. <span data-ttu-id="11c05-114">Gå til **Behandling av teknisk endring \> Oppsett \> Produkteiere**.</span><span class="sxs-lookup"><span data-stu-id="11c05-114">Go to **Engineering change management \> Setup \> Product owners**.</span></span>
2. <span data-ttu-id="11c05-115">Velg **Ny** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="11c05-115">On the Action Pane, select **New**.</span></span>
3. <span data-ttu-id="11c05-116">I **Produkteier**-feltet angir du et navn på gruppen.</span><span class="sxs-lookup"><span data-stu-id="11c05-116">In the **Product owner** field, enter a name for the group.</span></span>
4. <span data-ttu-id="11c05-117">I **Navn**-feltet skriver du inn en beskrivelse av gruppen.</span><span class="sxs-lookup"><span data-stu-id="11c05-117">In the **Name** field, enter a description of the group.</span></span>
5. <span data-ttu-id="11c05-118">På hurtigfanen **Medlemmer** legger du til arbeiderne som skal være medlemmer av gruppen.</span><span class="sxs-lookup"><span data-stu-id="11c05-118">On the **Members** FastTab, add the workers who should be members of the group.</span></span>

## <a name="assign-a-product-owner-to-a-product"></a><span data-ttu-id="11c05-119">Tilordne en produkteier til et produkt</span><span class="sxs-lookup"><span data-stu-id="11c05-119">Assign a product owner to a product</span></span>

<span data-ttu-id="11c05-120">Hvis du vil tilordne en produkteier til et produkt, gjør du følgende.</span><span class="sxs-lookup"><span data-stu-id="11c05-120">To assign a product owner to a product, follow these steps.</span></span>

1. <span data-ttu-id="11c05-121">Åpne siden **Produktdetaljer** for det relevante produkt eller produktstandarden.</span><span class="sxs-lookup"><span data-stu-id="11c05-121">Open the **Product details** page for the relevant product or product master.</span></span>
1. <span data-ttu-id="11c05-122">I hurtigfanen **Generelt** setter du **Produkteier**-feltet til navnet på den aktuelle produkteiergruppen.</span><span class="sxs-lookup"><span data-stu-id="11c05-122">On the **General** FastTab, set the **Product owner** field to the name of the relevant product owner group.</span></span>

<span data-ttu-id="11c05-123">Mens en produkteier er tilordnet et produkt, kan bare medlemmene av produkteiergruppen redigere **Produkteier**-innstillingen.</span><span class="sxs-lookup"><span data-stu-id="11c05-123">While a product owner is assigned to a product, only the members of the product owner group can edit the **Product owner** setting.</span></span>

<span data-ttu-id="11c05-124">Produkteieren vises også på siden **Frigitte produkter**.</span><span class="sxs-lookup"><span data-stu-id="11c05-124">The product owner is also visible on the **Released products** page.</span></span>

## <a name="product-owners-and-product-releases"></a><span data-ttu-id="11c05-125">Produkteiere og produktfrigivelser</span><span class="sxs-lookup"><span data-stu-id="11c05-125">Product owners and product releases</span></span>

<span data-ttu-id="11c05-126">Bare brukere fra et produkts produkteiergruppe kan frigi produktet.</span><span class="sxs-lookup"><span data-stu-id="11c05-126">Only users from a product's product owner group can release that product.</span></span> <span data-ttu-id="11c05-127">Det er imidlertid et unntak når produktet er en underordnet vare, og det overordnede frigis av eieren av det overordnede.</span><span class="sxs-lookup"><span data-stu-id="11c05-127">However, there is an exception when the product is a child item, and its parent is released by the parent's owner.</span></span> <span data-ttu-id="11c05-128">Med andre ord, hvis produktet er en del av stykklisten til et annet produkt, sjekker ikke systemet produkteieren av hver vare i stykklisten.</span><span class="sxs-lookup"><span data-stu-id="11c05-128">In other words, if the product is part of the BOM of another product, the system doesn't check the product owner of each item in the BOM.</span></span> <span data-ttu-id="11c05-129">Den kontrollerer bare produkteieren av den overordnede varen.</span><span class="sxs-lookup"><span data-stu-id="11c05-129">It checks only the product owner of the parent item.</span></span>

<span data-ttu-id="11c05-130">Produkt X er for eksempel tilordnet til produkteiergruppen *Designkabinetter*.</span><span class="sxs-lookup"><span data-stu-id="11c05-130">For example, product X is assigned to the *Design cabinets* product owner group.</span></span> <span data-ttu-id="11c05-131">Produkt X er også en del av stykklisten for produkt Y, som er tilordnet til produkteiergruppen *Designhøyttalere*.</span><span class="sxs-lookup"><span data-stu-id="11c05-131">Product X is also part of the BOM of product Y, which is assigned to the *Design Speakers* product owner group.</span></span> <span data-ttu-id="11c05-132">Hvis en bruker fra produkteiergruppen *Designhøyttalere* frigir produkt Y og stykklisten, blir produkt X frigitt sammen med produkt Y.</span><span class="sxs-lookup"><span data-stu-id="11c05-132">If a user from the *Design Speakers* product owner group releases product Y and its BOM, product X will be released together with product Y.</span></span>

## <a name="product-owners-and-approvals"></a><span data-ttu-id="11c05-133">Produkteiere og godkjenninger</span><span class="sxs-lookup"><span data-stu-id="11c05-133">Product owners and approvals</span></span>

<span data-ttu-id="11c05-134">Fordi produkteiere vet om bestemte tekniske endringer som vil dra nytte av produktene deres, er det ofte fornuftig å ta dem med som en del av godkjenningsprosessen under behandling av teknisk endring.</span><span class="sxs-lookup"><span data-stu-id="11c05-134">Because product owners know whether specific engineering changes will benefit their products, it often makes sense to include them as part of the approval process in engineering change management.</span></span> <span data-ttu-id="11c05-135">Du kan implementere denne fremgangsmåten ved å definere produkteierne som deltakerleverandører i arbeidsflytene som brukes til behandling av teknisk endring.</span><span class="sxs-lookup"><span data-stu-id="11c05-135">You can implement this approach by setting up the product owners as participant providers in the workflows that are used for engineering change management.</span></span> <span data-ttu-id="11c05-136">Systemet vil deretter tilordne godkjenningsoppgaver i arbeidsflytene, basert på produktene som er i forespørsler og ordrer om teknisk endring.</span><span class="sxs-lookup"><span data-stu-id="11c05-136">The system will then assign approval tasks in the workflows, based on the products that are in engineering change requests and engineering change orders.</span></span> <span data-ttu-id="11c05-137">Hvis du vil ha mer informasjon, kan du se [Behandle endringer i tekniske produkter](engineering-change-management.md).</span><span class="sxs-lookup"><span data-stu-id="11c05-137">For more information, see [Manage changes to engineering products](engineering-change-management.md).</span></span>
