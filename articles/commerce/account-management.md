---
title: Kontobehandlingssider og -moduler
description: Dette emnet dekker kontobehandlingssider og -moduler i Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 12/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: f9fc3731cd9d21294b0161e1d419f255096d7790
ms.sourcegitcommit: 96bfc20eb748f4090a2b5e1ff9f54997d5a5d359
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/04/2019
ms.locfileid: "2885815"
---
# <a name="account-management-pages-and-modules"></a><span data-ttu-id="84d81-103">Kontobehandlingssider og -moduler</span><span class="sxs-lookup"><span data-stu-id="84d81-103">Account management pages and modules</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="84d81-104">Dette emnet dekker kontobehandlingssider og -moduler i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="84d81-104">This topic covers account management pages and modules in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="84d81-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="84d81-105">Overview</span></span>

<span data-ttu-id="84d81-106">Kontobehandling refererer til en gruppe med sider som brukes til å behandle informasjon som er relatert til brukerkontoer i Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="84d81-106">Account management refers to a group of pages that is used to manage user account–related information in Dynamics 365 Commerce.</span></span> <span data-ttu-id="84d81-107">Kontobehandlingssidene inkluderer målsiden for kontostyring, brukerprofilside, brukeradresseside, ordreloggside, ordredetaljerside, loyalitetsside og ønskelisteside.</span><span class="sxs-lookup"><span data-stu-id="84d81-107">Account management pages include the account management landing page, user profile page, user address page, order history page, order details page, loyalty page, and wish list page.</span></span>

### <a name="account-management-landing-page"></a><span data-ttu-id="84d81-108">Målside for kontobehandling</span><span class="sxs-lookup"><span data-stu-id="84d81-108">Account management landing page</span></span>

<span data-ttu-id="84d81-109">Målsiden for kontoadministrasjons bruker følgende moduler:</span><span class="sxs-lookup"><span data-stu-id="84d81-109">The account management landing page uses the following modules:</span></span>

- <span data-ttu-id="84d81-110">**Innholdsplassering** – Denne modulen er en containermodul som inneholder alle modulene på målsiden for kontostyring.</span><span class="sxs-lookup"><span data-stu-id="84d81-110">**Content placement** – This module is a container module that holds all the modules on the account management landing page.</span></span>
- <span data-ttu-id="84d81-111">**Velkomstelement for konto** – Denne modulen brukes til å gi en velkomstmelding på kontobehandlingssiden.</span><span class="sxs-lookup"><span data-stu-id="84d81-111">**Account welcome item** – This module is used to provide a welcome message on the account management page.</span></span> <span data-ttu-id="84d81-112">Den inneholder egenskaper for overskriften og flisstørrelsen.</span><span class="sxs-lookup"><span data-stu-id="84d81-112">It includes properties for the heading and the tile size.</span></span> <span data-ttu-id="84d81-113">Egenskapen **Flisstørrelse** angir bredden på modulen i innholdsplasseringsmodulen.</span><span class="sxs-lookup"><span data-stu-id="84d81-113">The **Tile size** property defines the width of the module in the content placement module.</span></span> <span data-ttu-id="84d81-114">Verdiområdet fra **1** til **12**, der **12** representerer den fullstendige bredden på innholdsplasseringscontaineren.</span><span class="sxs-lookup"><span data-stu-id="84d81-114">Values range from **1** through **12**, where **12** represents the full width of the content placement container.</span></span>
- <span data-ttu-id="84d81-115">**Plasseringselement for kontoordre** – Denne modulen brukes til å gi et sammendrag av antall ordrer som er lagt inn av brukerkontoen.</span><span class="sxs-lookup"><span data-stu-id="84d81-115">**Account order placement item** – This module is used to provide a summary of the number of orders that have been placed by the user account.</span></span> <span data-ttu-id="84d81-116">Den inneholder egenskaper for overskriften, flisstørrelsen og koblingen "vis detaljer".</span><span class="sxs-lookup"><span data-stu-id="84d81-116">It includes properties for the heading, the tile size, and the "view details" link.</span></span> <span data-ttu-id="84d81-117">Vis detaljer-koblingen bør konfigureres til å omdirigere til ordreloggsiden.</span><span class="sxs-lookup"><span data-stu-id="84d81-117">The "view details" link should be configured to redirect to the order history page.</span></span>
- <span data-ttu-id="84d81-118">**Plasseringselement for kontoprofil** – Denne modulen brukes til å gi et sammendrag av brukerprofilen.</span><span class="sxs-lookup"><span data-stu-id="84d81-118">**Account profile placement item** – This module is used to provide a summary of the user profile.</span></span> <span data-ttu-id="84d81-119">Den inneholder egenskaper for overskriften, flisstørrelsen og koblingen "vis detaljer".</span><span class="sxs-lookup"><span data-stu-id="84d81-119">It includes properties for the heading, the tile size, and the "view details" link.</span></span> <span data-ttu-id="84d81-120">Vis detaljer-koblingen bør konfigureres til å omdirigere til brukerprofilsiden.</span><span class="sxs-lookup"><span data-stu-id="84d81-120">The "view details" link should be configured to redirect to the user profile page.</span></span>
- <span data-ttu-id="84d81-121">**Ønskelisteelement for konto** – Denne modulen brukes til å gi et sammendrag av varene i kundens ønskeliste.</span><span class="sxs-lookup"><span data-stu-id="84d81-121">**Account wishlist item** – This module is used to provide a summary of the items on the customer's wish list.</span></span> <span data-ttu-id="84d81-122">Det kan for eksempel stå "Du har 10 elementer i ønskelisten".</span><span class="sxs-lookup"><span data-stu-id="84d81-122">For example, it might state, "You have 10 items in your wish list."</span></span> <span data-ttu-id="84d81-123">Den inneholder egenskaper for overskriften, flisstørrelsen og koblingen "vis detaljer".</span><span class="sxs-lookup"><span data-stu-id="84d81-123">It includes properties for the heading, the tile size, and the "view details" link.</span></span> <span data-ttu-id="84d81-124">Vis detaljer-koblingen bør konfigureres til å omdirigere til ønskelistesiden.</span><span class="sxs-lookup"><span data-stu-id="84d81-124">The "view details" link should be configured to redirect to the wish list page.</span></span>
- <span data-ttu-id="84d81-125">**Kontoadresseelement** – Denne modulen brukes til å gi et sammendrag av brukerens adresse.</span><span class="sxs-lookup"><span data-stu-id="84d81-125">**Account address item** – This module is used to provide a summary of the user's addresses.</span></span> <span data-ttu-id="84d81-126">Det kan for eksempel stå "Du har lagt til 2 adresser i kontoen din".</span><span class="sxs-lookup"><span data-stu-id="84d81-126">For example, it might state, "You have 2 addresses added to your account."</span></span> <span data-ttu-id="84d81-127">Den inneholder egenskaper for overskriften, flisstørrelsen og koblingen "vis detaljer".</span><span class="sxs-lookup"><span data-stu-id="84d81-127">It includes properties for the heading, the tile size, and the "view details" link.</span></span> <span data-ttu-id="84d81-128">Vis detaljer-koblingen bør konfigureres til å omdirigere til brukeradressesiden.</span><span class="sxs-lookup"><span data-stu-id="84d81-128">The "view details" link should be configured to redirect to the user address page.</span></span>
- <span data-ttu-id="84d81-129">**Kontofordelselement** – Denne modulen brukes til å vise og koble til informasjon om fordelsprogrammer.</span><span class="sxs-lookup"><span data-stu-id="84d81-129">**Account loyalty item** – This module is used to show and link to loyalty program information.</span></span> <span data-ttu-id="84d81-130">Den inneholder egenskaper for overskriften, flisstørrelsen, koblingen "vis detaljer" og koblingen "bli medlem".</span><span class="sxs-lookup"><span data-stu-id="84d81-130">It includes properties for the heading, the tile size, the "view details" link, and the "become a member" link.</span></span> <span data-ttu-id="84d81-131">"Vis detaljer"-koblingen bør konfigureres til å omdirigere til fordelssiden.</span><span class="sxs-lookup"><span data-stu-id="84d81-131">The "view details" link should be configured to redirect to the loyalty page.</span></span> <span data-ttu-id="84d81-132">Koblingen "bli medlem" kan konfigureres til å omadressere til en side der brukere kan bli med i fordelsprogrammet.</span><span class="sxs-lookup"><span data-stu-id="84d81-132">The "become a member" link should be configured to redirect to a page where users can join the loyalty program.</span></span>

### <a name="order-history-page"></a><span data-ttu-id="84d81-133">Siden Ordrehistorikk</span><span class="sxs-lookup"><span data-stu-id="84d81-133">Order history page</span></span>

<span data-ttu-id="84d81-134">Siden for ordrehistorikk bruker ordreloggmodulen til å vise alle de siste ordrene som brukeren har lagt inn.</span><span class="sxs-lookup"><span data-stu-id="84d81-134">The order history page uses the order history module to show all the recent orders that the user has placed.</span></span>

### <a name="order-details-page"></a><span data-ttu-id="84d81-135">Side for ordredetaljer</span><span class="sxs-lookup"><span data-stu-id="84d81-135">Order details page</span></span>

<span data-ttu-id="84d81-136">Ordredetaljer-siden inneholder detaljert informasjon for hver ordre og er tilgjengelig fra ordrehistorikksiden.</span><span class="sxs-lookup"><span data-stu-id="84d81-136">The order details page provides detailed information for each order and is accessed from the order history page.</span></span> <span data-ttu-id="84d81-137">Den bruker ordredetaljermodulen, som krever salgs-IDen eller transaksjons-IDen for å hente ordredetaljene.</span><span class="sxs-lookup"><span data-stu-id="84d81-137">It uses the order details module, which requires the sales ID or transaction ID to retrieve the order details.</span></span>

### <a name="user-profile-page"></a><span data-ttu-id="84d81-138">Brukerprofilside</span><span class="sxs-lookup"><span data-stu-id="84d81-138">User profile page</span></span>

<span data-ttu-id="84d81-139">Siden brukerprofil viser brukerkontodetaljer, for eksempel brukerens navn og e-postadresse.</span><span class="sxs-lookup"><span data-stu-id="84d81-139">The user profile page shows user account details, such as a user's name and email address.</span></span> <span data-ttu-id="84d81-140">Den bruker brukerprofilmodulen.</span><span class="sxs-lookup"><span data-stu-id="84d81-140">It uses the user profile module.</span></span> <span data-ttu-id="84d81-141">Selv om epostadresse ikke kan fjernes, kan den redigeres.</span><span class="sxs-lookup"><span data-stu-id="84d81-141">Although the email address can't be removed, it can be edited.</span></span> <span data-ttu-id="84d81-142">Brukerprofilsiden viser også brukerpreferansene som gjør en bruker i stand til å velge/velge bort bestemte funksjoner, for eksempel tilpassing av anbefalingslister.</span><span class="sxs-lookup"><span data-stu-id="84d81-142">The user profile page also shows user preferences that enable a user to opt in or opt out from certain features such as personalization of recommendation lists.</span></span> 

### <a name="user-address-page"></a><span data-ttu-id="84d81-143">Brukeradresseside</span><span class="sxs-lookup"><span data-stu-id="84d81-143">User address page</span></span>

<span data-ttu-id="84d81-144">Siden for brukeradresse viser listen over adresser som er knyttet til brukerkontoen.</span><span class="sxs-lookup"><span data-stu-id="84d81-144">The user address page shows the list of addresses that are associated with the user account.</span></span> <span data-ttu-id="84d81-145">Brukeren har enten oppgitt disse adressene under utsjekking eller lagt dem til direkte på denne siden.</span><span class="sxs-lookup"><span data-stu-id="84d81-145">The user either provided these addresses during checkout or added them directly on  this page.</span></span> <span data-ttu-id="84d81-146">Brukeradressemodulen brukes til å legge til og redigere adresser, angi primæradresse og gjengi eksisterende adresser på siden.</span><span class="sxs-lookup"><span data-stu-id="84d81-146">The user address module is used add and edit addresses, set the primary address, and render existing addresses on the page.</span></span>

### <a name="wish-list-page"></a><span data-ttu-id="84d81-147">Ønskelisteside</span><span class="sxs-lookup"><span data-stu-id="84d81-147">Wish list page</span></span>

<span data-ttu-id="84d81-148">Ønskelistesiden viser varene som er lagt til på kundens ønskeliste.</span><span class="sxs-lookup"><span data-stu-id="84d81-148">The wish list page shows the items that have been added to the customer's wish list.</span></span> <span data-ttu-id="84d81-149">Den bruker ønskelistemodulen til å vise ønskelisteelementer.</span><span class="sxs-lookup"><span data-stu-id="84d81-149">It uses the wish list module to render wish list items.</span></span>

### <a name="loyalty-page"></a><span data-ttu-id="84d81-150">Fordelsside</span><span class="sxs-lookup"><span data-stu-id="84d81-150">Loyalty page</span></span>

<span data-ttu-id="84d81-151">Fordelssiden lar kunder bli med i et fordelsprogram eller, hvis de allerede er medlemmer at fordelsprogrammet, vise programdetaljer.</span><span class="sxs-lookup"><span data-stu-id="84d81-151">The loyalty page lets customers join a loyalty program or, if they are already loyalty program members, view their program details.</span></span> <span data-ttu-id="84d81-152">De kan også vise poengene de har tjent opp og løst inn i nylige transaksjoner.</span><span class="sxs-lookup"><span data-stu-id="84d81-152">They can also view the points that they have earned and redeemed in recent transactions.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="84d81-153">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="84d81-153">Additional resources</span></span>

[<span data-ttu-id="84d81-154">Startpakke, oversikt</span><span class="sxs-lookup"><span data-stu-id="84d81-154">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="84d81-155">Containermodul</span><span class="sxs-lookup"><span data-stu-id="84d81-155">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="84d81-156">Kjøpsboksmodul</span><span class="sxs-lookup"><span data-stu-id="84d81-156">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="84d81-157">Handlekurvmodul</span><span class="sxs-lookup"><span data-stu-id="84d81-157">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="84d81-158">Kassemodul</span><span class="sxs-lookup"><span data-stu-id="84d81-158">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="84d81-159">Ordrebekreftelsesmodul</span><span class="sxs-lookup"><span data-stu-id="84d81-159">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="84d81-160">Topptekstmodul</span><span class="sxs-lookup"><span data-stu-id="84d81-160">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="84d81-161">Bunntekstmodul</span><span class="sxs-lookup"><span data-stu-id="84d81-161">Footer module</span></span>](author-footer-module.md)
