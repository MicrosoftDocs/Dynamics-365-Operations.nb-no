---
title: Dokumentere statuser og livssyklus
description: Dette emnet dekker de ulike dokumenttilstandene for sideelementer i Microsoft Dynamics 365 Commerce.
author: phinneyridge
manager: annbe
ms.date: 04/13/2020
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
ms.openlocfilehash: 4a00f1c363e5ecb0e3e64637a8f487c48df2df72
ms.sourcegitcommit: ac966ea3a6c557fb5f9634b187b0e788d3e82d4d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/14/2020
ms.locfileid: "3261519"
---
# <a name="document-states-and-lifecycle"></a><span data-ttu-id="40446-103">Dokumentere statuser og livssyklus</span><span class="sxs-lookup"><span data-stu-id="40446-103">Document states and lifecycle</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="40446-104">Dette emnet dekker de ulike dokumenttilstandene for sideelementer i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="40446-104">This topic covers the various document states of page elements in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="document-state-descriptions"></a><span data-ttu-id="40446-105">Beskrivelse av dokumenttilstand</span><span class="sxs-lookup"><span data-stu-id="40446-105">Document state descriptions</span></span>

<span data-ttu-id="40446-106">Emnet [Sideelementer](page-elements-overview.md) viser ulike dokumenttyper i innholdsbehandlingssystemet (CMS).</span><span class="sxs-lookup"><span data-stu-id="40446-106">The [Page elements](page-elements-overview.md) topic lists various documents types in the content management system (CMS).</span></span> <span data-ttu-id="40446-107">Disse dokumenttypene kan ha flere tilstander i redigeringsverktøyet.</span><span class="sxs-lookup"><span data-stu-id="40446-107">These document types can have several states in the authoring tool.</span></span> <span data-ttu-id="40446-108">Dokumentstatusen bidrar til å hindre datakonflikter og bruk av versjonskontroll.</span><span class="sxs-lookup"><span data-stu-id="40446-108">The document states help prevent data conflicts and enforce version control.</span></span> <span data-ttu-id="40446-109">De bestemmer hvem som kan endre dokumentene, når dokumentene kan endres, og når endringer kan vises av andre personer.</span><span class="sxs-lookup"><span data-stu-id="40446-109">They determine who can change the documents, when the documents can be changed, and when changes can be viewed by other people.</span></span>

<span data-ttu-id="40446-110">Følgende tabell viser mulige dokumenttilstander for sideelementer i Commerce.</span><span class="sxs-lookup"><span data-stu-id="40446-110">The following table shows the possible document states of page elements in Commerce.</span></span>

| <span data-ttu-id="40446-111">Dokumenttilstand</span><span class="sxs-lookup"><span data-stu-id="40446-111">Document state</span></span>      | <span data-ttu-id="40446-112">Handling i områdebygger</span><span class="sxs-lookup"><span data-stu-id="40446-112">Site builder action</span></span>        | <span data-ttu-id="40446-113">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="40446-113">Description</span></span>                                                  |
| ------------------- | -------------------------- | ------------------------------------------------------------ |
| <span data-ttu-id="40446-114">Sjekket ut</span><span class="sxs-lookup"><span data-stu-id="40446-114">Checked out</span></span>         | <span data-ttu-id="40446-115">Velg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="40446-115">Select **Edit**.</span></span>           | <span data-ttu-id="40446-116">Det aktuelle dokumentet er sjekket ut til deg.</span><span class="sxs-lookup"><span data-stu-id="40446-116">The applicable document is checked out to you.</span></span> <span data-ttu-id="40446-117">Mens et dokument er i denne tilstanden, kan det ikke endres av andre godkjente systembrukere, og endringer du utfører i dokumentet, er bare synlige for deg.</span><span class="sxs-lookup"><span data-stu-id="40446-117">While a document is in this state, it can't be changed by other authenticated system users, and any changes that you make to the document are visible only to you.</span></span> |
| <span data-ttu-id="40446-118">Lagret</span><span class="sxs-lookup"><span data-stu-id="40446-118">Saved</span></span>               | <span data-ttu-id="40446-119">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="40446-119">Select **Save**.</span></span>           | <span data-ttu-id="40446-120">Endringer som er gjort i et utsjekket dokument, blir lagret i databasen, men dokumentet er ennå ikke sjekket inn eller publisert.</span><span class="sxs-lookup"><span data-stu-id="40446-120">Changes that have been made to a checked-out document are saved to the database, but the document isn't yet checked in or published.</span></span> <span data-ttu-id="40446-121">De lagrede endringene er ikke synlige for andre godkjente systembrukere før forfatteren velger **Fullfør redigering**.</span><span class="sxs-lookup"><span data-stu-id="40446-121">The saved changes aren't visible to other authenticated system users until the author selects **Finish editing**.</span></span> <span data-ttu-id="40446-122">De er ikke synlige for eksterne brukere før elementet er publisert.</span><span class="sxs-lookup"><span data-stu-id="40446-122">They aren't visible to external users until the item is published.</span></span> |
| <span data-ttu-id="40446-123">Forkastet utsjekking</span><span class="sxs-lookup"><span data-stu-id="40446-123">Discarded check out</span></span> | <span data-ttu-id="40446-124">Velg **Forkast redigeringer**.</span><span class="sxs-lookup"><span data-stu-id="40446-124">Select **Discard edits**.</span></span>  | <span data-ttu-id="40446-125">Alle endringer i det utsjekkede dokumentet forkastes, og varen tilbakestilles til den siste versjonen som ble sjekket inn.</span><span class="sxs-lookup"><span data-stu-id="40446-125">All changes to the checked-out document are discarded, and the item reverts to the last version that was checked in.</span></span> |
| <span data-ttu-id="40446-126">Sjekket inn</span><span class="sxs-lookup"><span data-stu-id="40446-126">Checked in</span></span>          | <span data-ttu-id="40446-127">Velg **Fullfør redigering**.</span><span class="sxs-lookup"><span data-stu-id="40446-127">Select **Finish editing**.</span></span> | <span data-ttu-id="40446-128">Det redigerte dokumentet sjekkes inn.</span><span class="sxs-lookup"><span data-stu-id="40446-128">The edited document is checked in.</span></span> <span data-ttu-id="40446-129">Alle endringer er synlige for andre godkjente systembrukere, og disse brukerne kan deretter redigere dokumentet.</span><span class="sxs-lookup"><span data-stu-id="40446-129">All changes are visible to other authenticated system users, and those users can then edit the document.</span></span> <span data-ttu-id="40446-130">Hver innsjekking oppretter en dokumentversjonsregistrering i elementloggen.</span><span class="sxs-lookup"><span data-stu-id="40446-130">Each check-in creates a document version record in the item's history.</span></span> |
| <span data-ttu-id="40446-131">Publisert</span><span class="sxs-lookup"><span data-stu-id="40446-131">Published</span></span>           | <span data-ttu-id="40446-132">Velg **Publiser**.</span><span class="sxs-lookup"><span data-stu-id="40446-132">Select **Publish**.</span></span>        | <span data-ttu-id="40446-133">Dokumentet publiseres, og endringene sendes ut på det aktive området og blir synlige for eksterne brukere.</span><span class="sxs-lookup"><span data-stu-id="40446-133">The document is published, and the changes are pushed to your live site and become discoverable by external users.</span></span> <span data-ttu-id="40446-134">Varer kan bare publiseres hvis de først har blitt sjekket inn ved å velge **Fullfør redigering**.</span><span class="sxs-lookup"><span data-stu-id="40446-134">Items can be published only if they have first been checked in by selecting **Finish editing**.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="40446-135">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="40446-135">Additional resources</span></span>

[<span data-ttu-id="40446-136">Måter å legge til innhold på</span><span class="sxs-lookup"><span data-stu-id="40446-136">Ways to add content</span></span>](add-manage-content.md)

[<span data-ttu-id="40446-137">Ordliste for sidemodell</span><span class="sxs-lookup"><span data-stu-id="40446-137">Page model glossary</span></span>](page-elements-overview.md)

[<span data-ttu-id="40446-138">Arbeide med publiseringsgrupper</span><span class="sxs-lookup"><span data-stu-id="40446-138">Work with publish groups</span></span>](publish-groups.md)

[<span data-ttu-id="40446-139">Arbeide med moduler</span><span class="sxs-lookup"><span data-stu-id="40446-139">Work with modules</span></span>](work-with-modules.md)

[<span data-ttu-id="40446-140">Arbeide med fragmenter</span><span class="sxs-lookup"><span data-stu-id="40446-140">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="40446-141">Oversikt over maler og oppsett</span><span class="sxs-lookup"><span data-stu-id="40446-141">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="40446-142">Tilpasse områdenavigering</span><span class="sxs-lookup"><span data-stu-id="40446-142">Customize site navigation</span></span>](customize-site-navigation.md)
