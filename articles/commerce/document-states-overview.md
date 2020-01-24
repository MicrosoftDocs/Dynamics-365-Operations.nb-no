---
title: Dokumentere statuser og livssyklus
description: Dette emnet dekker de ulike dokumenttilstandene for sideelementer i Microsoft Dynamics 365 Commerce.
author: phinneyridge
manager: annbe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: edb81efc45fc5e7eed32cb7d9b8fda5ade987dd4
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914893"
---
# <a name="document-states-and-lifecycle"></a><span data-ttu-id="d0113-103">Dokumentere statuser og livssyklus</span><span class="sxs-lookup"><span data-stu-id="d0113-103">Document states and lifecycle</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="d0113-104">Dette emnet dekker de ulike dokumenttilstandene for sideelementer i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="d0113-104">This topic covers the various document states of page elements in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="document-state-descriptions"></a><span data-ttu-id="d0113-105">Beskrivelse av dokumenttilstand</span><span class="sxs-lookup"><span data-stu-id="d0113-105">Document state descriptions</span></span>

<span data-ttu-id="d0113-106">Emnet [Sideelementer](page-elements-overview.md) viser ulike dokumenttyper i innholdsbehandlingssystemet (CMS).</span><span class="sxs-lookup"><span data-stu-id="d0113-106">The [Page elements](page-elements-overview.md) topic lists various documents types in the content management system (CMS).</span></span> <span data-ttu-id="d0113-107">Disse dokumenttypene kan ha flere tilstander i redigeringsverktøyet.</span><span class="sxs-lookup"><span data-stu-id="d0113-107">These document types can have several states in the authoring tool.</span></span> <span data-ttu-id="d0113-108">Dokumentstatusen bidrar til å hindre datakonflikter og bruk av versjonskontroll.</span><span class="sxs-lookup"><span data-stu-id="d0113-108">The document states help prevent data conflicts and enforce version control.</span></span> <span data-ttu-id="d0113-109">De bestemmer hvem som kan endre dokumentene, når dokumentene kan endres, og når endringer kan vises av andre personer.</span><span class="sxs-lookup"><span data-stu-id="d0113-109">They determine who can change the documents, when the documents can be changed, and when changes can be viewed by other people.</span></span>

<span data-ttu-id="d0113-110">Følgende tabell viser mulige dokumenttilstander for sideelementer i Commerce.</span><span class="sxs-lookup"><span data-stu-id="d0113-110">The following table shows the possible document states of page elements in Commerce.</span></span>

| <span data-ttu-id="d0113-111">Dokumenttilstand</span><span class="sxs-lookup"><span data-stu-id="d0113-111">Document state</span></span> | <span data-ttu-id="d0113-112">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="d0113-112">Description</span></span> |
|---|---|
| <span data-ttu-id="d0113-113">Sjekket ut</span><span class="sxs-lookup"><span data-stu-id="d0113-113">Checked out</span></span> | <span data-ttu-id="d0113-114">Når en CMS-vare er sjekket ut til deg, kan den ikke redigeres av andre godkjente systembrukere.</span><span class="sxs-lookup"><span data-stu-id="d0113-114">When a CMS item is checked out to you, it can't be edited by any other authenticated system users.</span></span> <span data-ttu-id="d0113-115">Endringer du utfører i elementet, er bare synlige for deg.</span><span class="sxs-lookup"><span data-stu-id="d0113-115">Any changes that you make to the item are visible only to you.</span></span> |
| <span data-ttu-id="d0113-116">Sjekket inn</span><span class="sxs-lookup"><span data-stu-id="d0113-116">Checked in</span></span> | <span data-ttu-id="d0113-117">Når en CMS-vare sjekkes inn, er alle endringer synlige for andre godkjente systembrukere, og disse brukerne kan deretter sjekke ut elementet og redigere det.</span><span class="sxs-lookup"><span data-stu-id="d0113-117">When a CMS item is checked in, all changes are visible to other authenticated system users, and those users can then check out the item and edit it.</span></span> <span data-ttu-id="d0113-118">Hver innsjekking oppretter en dokumentversjonsregistrering i elementloggen.</span><span class="sxs-lookup"><span data-stu-id="d0113-118">Each check-in creates a document version record in the item's history.</span></span> |
| <span data-ttu-id="d0113-119">Publisert</span><span class="sxs-lookup"><span data-stu-id="d0113-119">Published</span></span> | <span data-ttu-id="d0113-120">Når en CMS-vare publiseres, skyves den til det aktive området ditt og blir synlig på Internett for ikke-godkjente eksterne brukere.</span><span class="sxs-lookup"><span data-stu-id="d0113-120">When a CMS item is published, it's pushed to your live site and becomes discoverable on the internet by non-authenticated external users.</span></span> <span data-ttu-id="d0113-121">Elementer kan bare publiseres hvis de er sjekket inn.</span><span class="sxs-lookup"><span data-stu-id="d0113-121">Items can be published only if they have been checked in.</span></span> |
| <span data-ttu-id="d0113-122">Lagret</span><span class="sxs-lookup"><span data-stu-id="d0113-122">Saved</span></span> | <span data-ttu-id="d0113-123">Endringer som er gjort i en utsjekket CMS-vare, kan lagres i CMS før varen sjekkes inn eller publiseres.</span><span class="sxs-lookup"><span data-stu-id="d0113-123">Changes that have been made to a checked-out CMS item can be saved to the CMS before the item is checked in or published.</span></span> <span data-ttu-id="d0113-124">Disse lagrede endringene er ikke synlige for andre godkjente systembrukere før varen sjekkes inn.</span><span class="sxs-lookup"><span data-stu-id="d0113-124">These saved changes aren't visible to other authenticated system users until the item is checked in.</span></span> <span data-ttu-id="d0113-125">De er ikke synlige for eksterne brukere før elementet er publisert.</span><span class="sxs-lookup"><span data-stu-id="d0113-125">They aren't visible to external users until the item is published.</span></span> |
| <span data-ttu-id="d0113-126">Forkastet utsjekking</span><span class="sxs-lookup"><span data-stu-id="d0113-126">Discarded check out</span></span> | <span data-ttu-id="d0113-127">Når en utsjekket CMS-vare forkastes, slettes alle lagrede endringer, og varen tilbakestilles til den versjonen som sist ble sjekket inn.</span><span class="sxs-lookup"><span data-stu-id="d0113-127">When a checked-out CMS item is discarded, all saved changes are deleted, and the item reverts to the version that was most recently checked in.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="d0113-128">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="d0113-128">Additional resources</span></span>

[<span data-ttu-id="d0113-129">Måter å legge til innhold på</span><span class="sxs-lookup"><span data-stu-id="d0113-129">Ways to add content</span></span>](add-manage-content.md)

[<span data-ttu-id="d0113-130">Ordliste for sidemodell</span><span class="sxs-lookup"><span data-stu-id="d0113-130">Page model glossary</span></span>](page-elements-overview.md)

[<span data-ttu-id="d0113-131">Arbeide med publiseringsgrupper</span><span class="sxs-lookup"><span data-stu-id="d0113-131">Work with publish groups</span></span>](publish-groups.md)

[<span data-ttu-id="d0113-132">Arbeide med moduler</span><span class="sxs-lookup"><span data-stu-id="d0113-132">Work with modules</span></span>](work-with-modules.md)

[<span data-ttu-id="d0113-133">Arbeide med fragmenter</span><span class="sxs-lookup"><span data-stu-id="d0113-133">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="d0113-134">Oversikt over maler og oppsett</span><span class="sxs-lookup"><span data-stu-id="d0113-134">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="d0113-135">Tilpasse områdenavigering</span><span class="sxs-lookup"><span data-stu-id="d0113-135">Customize site navigation</span></span>](customize-site-navigation.md)
