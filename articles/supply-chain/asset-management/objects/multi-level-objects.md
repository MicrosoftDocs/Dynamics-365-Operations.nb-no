---
title: Aktiva på flere nivåer
description: Dette emnet forklarer hvordan du oppretter og sletter aktiva på flere nivåer.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4b7609a85f0315ee5cb5fae62d151b271ef5febe
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4434544"
---
# <a name="multi-level-assets"></a><span data-ttu-id="7950c-103">Aktiva på flere nivåer</span><span class="sxs-lookup"><span data-stu-id="7950c-103">Multi-level assets</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="7950c-104">Dette emnet forklarer hvordan du oppretter og sletter aktiva på flere nivåer.</span><span class="sxs-lookup"><span data-stu-id="7950c-104">This topic explains how to create and delete multi-level assets.</span></span> <span data-ttu-id="7950c-105">Du kan opprette aktiva og relaterte underaktiva i en hierarkisk trestruktur.</span><span class="sxs-lookup"><span data-stu-id="7950c-105">You can create assets and related sub-assets in a hierarchical tree structure.</span></span> <span data-ttu-id="7950c-106">På denne måten kan du vise relasjoner og avhengigheter blant aktiva.</span><span class="sxs-lookup"><span data-stu-id="7950c-106">In this way, you can show relations and dependencies among assets.</span></span> <span data-ttu-id="7950c-107">Vedlikeholdsjobber kan knyttes til alle nivåer i trestrukturen.</span><span class="sxs-lookup"><span data-stu-id="7950c-107">Maintenance jobs can be related to all levels of the tree structure.</span></span> <span data-ttu-id="7950c-108">Statistikk kan også opprettes for et enkeltnivå eller som en sum for alle underaktivanivåer.</span><span class="sxs-lookup"><span data-stu-id="7950c-108">Statistics can also be created for an individual level or as a sum of all sub-asset levels.</span></span>

<span data-ttu-id="7950c-109">På listesiden **Alle aktiva** (**Aktivastyring** \> **Felles** \> **Aktiva** \> **Alle aktiva**) vises aktiva i hierarkisk rekkefølge i kolonnen **Aktiva**.</span><span class="sxs-lookup"><span data-stu-id="7950c-109">On the **All Assets** list page (**Asset management** \> **Common** \> **Assets** \> **All assets**), the **Asset** column lists assets in hierarchical order.</span></span> <span data-ttu-id="7950c-110">Kolonnen **Overordnet** viser det tilknyttede overordnede objektet.</span><span class="sxs-lookup"><span data-stu-id="7950c-110">The **Parent** column shows the related parent.</span></span> <span data-ttu-id="7950c-111">Hvis det allerede er opprettet aktiva og under aktiva, viser i tillegg **Aktivatre**-delen i ruten **Beslektet informasjon** aktivaene i en trestruktur.</span><span class="sxs-lookup"><span data-stu-id="7950c-111">Additionally, if assets and sub-assets have already been created, the **Asset tree** section in the **Related information** pane shows the assets in a tree structure.</span></span>

<span data-ttu-id="7950c-112">Se [Opprette et aktivum](../objects/create-an-object.md) hvis du vil ha mer informasjon om hvordan du oppretter et aktivum.</span><span class="sxs-lookup"><span data-stu-id="7950c-112">For information about how to create an asset, see [Create an asset](../objects/create-an-object.md).</span></span> <span data-ttu-id="7950c-113">Hvis du vil opprette et underordnet aktivum, velger du det overordnede objektet i feltet **Overordnet** på hurtigfanen **Generelt**.</span><span class="sxs-lookup"><span data-stu-id="7950c-113">To create a sub-asset, select the parent asset in the **Parent** field on the **General** FastTab.</span></span>

## <a name="copy-an-asset-or-asset-structure"></a><span data-ttu-id="7950c-114">Kopiere en aktivastruktur</span><span class="sxs-lookup"><span data-stu-id="7950c-114">Copy an asset or asset structure</span></span>

<span data-ttu-id="7950c-115">Hvis firmaet har flere lignende aktivastrukturer, kan du bruke kopieringsfunksjonen i Aktivastyring til å opprette dem raskt.</span><span class="sxs-lookup"><span data-stu-id="7950c-115">If your company has several similar asset structures, you can use the Copy function in Asset Management to quickly create them.</span></span>

1. <span data-ttu-id="7950c-116">Velg **Aktivastyring** \> **Felles** \> **Aktiva** \> **Alle aktiva**.</span><span class="sxs-lookup"><span data-stu-id="7950c-116">Select **Asset management** \> **Common** \> **Assets** \> **All assets**.</span></span>
2. <span data-ttu-id="7950c-117">På listesiden **Alle aktiva** velger du aktivumet du vil kopiere.</span><span class="sxs-lookup"><span data-stu-id="7950c-117">On the **All assets** list page, select the asset to copy.</span></span> <span data-ttu-id="7950c-118">Hvis du for eksempel vil kopiere hele aktivastrukturen, inkludert underordnede aktiva, velger du et overordnet objekt.</span><span class="sxs-lookup"><span data-stu-id="7950c-118">For example, if you want to copy the whole asset structure, including sub-assets, select a parent asset.</span></span>
3. <span data-ttu-id="7950c-119">Velg **Kopier aktivum**.</span><span class="sxs-lookup"><span data-stu-id="7950c-119">Select **Copy asset**.</span></span> <span data-ttu-id="7950c-120">I **Kopier fra**-delen er **Aktivum**-feltet satt til aktivumet du valgte på listesiden.</span><span class="sxs-lookup"><span data-stu-id="7950c-120">In the **Copy from** section, the **Asset** field is set to the asset that you selected on the list page.</span></span>
4. <span data-ttu-id="7950c-121">I **Kopier til**-delen i **Aktiva**-feltet angir du navnet på det nye aktivumet.</span><span class="sxs-lookup"><span data-stu-id="7950c-121">In the **Copy to** section, in the **Asset** field, enter the name of the new asset.</span></span>
5. <span data-ttu-id="7950c-122">Hvis aktivaet du oppretter, skal være en del av en eksisterende aktivastruktur, går du til delen **Overordnet objekt**, **Aktiva**-feltet, og velger en overordnet ID.</span><span class="sxs-lookup"><span data-stu-id="7950c-122">If the asset that you're creating should be part of an existing asset structure, in the **Parent asset** section, in the **Asset** field, select a parent ID.</span></span>
6. <span data-ttu-id="7950c-123">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="7950c-123">Select **OK**.</span></span> <span data-ttu-id="7950c-124">Den nye aktivastrukturen vises på listesiden **Alle aktiva**.</span><span class="sxs-lookup"><span data-stu-id="7950c-124">The new asset structure is shown on the **All assets** list page.</span></span> <span data-ttu-id="7950c-125">Alle aktivaattributter, vedlikeholdsplaner og vedlikeholdsrunder som er relatert til aktivumet du kopierte, overføres til den nye aktivaet eller aktivastrukturen.</span><span class="sxs-lookup"><span data-stu-id="7950c-125">All asset attributes, maintenance plans, and maintenance rounds that are related to the asset that you copied are transferred to the new asset or asset structure.</span></span>

<span data-ttu-id="7950c-126">Når du kopierer en aktivastruktur, har de underordnede aktivaene i den nye strukturen samme navn som de underordnede aktivaene du kopierte.</span><span class="sxs-lookup"><span data-stu-id="7950c-126">When you copy an asset structure, the sub-assets in the new structure have the same name as the sub-assets that you copied.</span></span> <span data-ttu-id="7950c-127">Når kopieringsprosedyren er fullført, kan du enkelt endre navnet og andre innstillinger for et aktivum.</span><span class="sxs-lookup"><span data-stu-id="7950c-127">After the copy procedure is completed, you can easily change the name and other settings for an asset.</span></span> <span data-ttu-id="7950c-128">Velg aktivumet på listesiden **Alle aktiva**, og velg deretter **Rediger**-knappen.</span><span class="sxs-lookup"><span data-stu-id="7950c-128">Select the asset on the **All assets** list page, and then select the **Edit** button.</span></span>

> [!NOTE]
> <span data-ttu-id="7950c-129">Når du kopierer en aktivastruktur, tilbakestilles livsløpstilstanden til de nye aktivaene til uansett status du definerte som start lilvsløpsstatus for aktiva.</span><span class="sxs-lookup"><span data-stu-id="7950c-129">When you copy an asset or asset structure, the lifecycle state of the new assets is reset to whatever state you defined as the initial lifecycle state for assets.</span></span> <span data-ttu-id="7950c-130">Arbeidsstedet tilbakestilles til standard arbeidssted.</span><span class="sxs-lookup"><span data-stu-id="7950c-130">The functional location is reset to the default functional location.</span></span>

## <a name="delete-an-asset-or-asset-structure"></a><span data-ttu-id="7950c-131">Slette et aktivum eller en aktivastruktur</span><span class="sxs-lookup"><span data-stu-id="7950c-131">Delete an asset or asset structure</span></span>

<span data-ttu-id="7950c-132">Hvis et aktivum har relaterte underordnede aktiva, kan du bare slette det hvis det er registrert vedlikeholdsanmodninger, arbeidsordrejobber, feilregistreringer eller betingelsesvurderinger for noen av aktivaene.</span><span class="sxs-lookup"><span data-stu-id="7950c-132">If an asset has related sub-assets, you can delete it only if no maintenance requests, work order jobs, fault registrations, or condition assessments are registered on any of the assets.</span></span>

1. <span data-ttu-id="7950c-133">På listesiden **Alle aktiva** velger du aktivumet du vil slette.</span><span class="sxs-lookup"><span data-stu-id="7950c-133">On the **All assets** list page, select the asset to delete.</span></span>
2. <span data-ttu-id="7950c-134">Velg **Slett**.</span><span class="sxs-lookup"><span data-stu-id="7950c-134">Select **Delete**.</span></span>

> [!NOTE]
> <span data-ttu-id="7950c-135">Hvis du ikke kan slette et aktivum ved hjelp av denne fremgangsmåten, er det en annen måte å håndtere sletting på, ved å definere en livsløpstilstand for et aktivum</span><span class="sxs-lookup"><span data-stu-id="7950c-135">If you can't delete an asset by using this procedure, another way to handle deletion is to set up an asset lifecycle state for this purpose.</span></span> <span data-ttu-id="7950c-136">Du kan for eksempel definere en **kassert** eller **slettet** livsløpstilstand på siden **Livsløpstilstander for aktiva**.</span><span class="sxs-lookup"><span data-stu-id="7950c-136">For example, you can set up a **Scrapped** or **Deleted** lifecycle state on the **Asset lifecycle states** page.</span></span>
