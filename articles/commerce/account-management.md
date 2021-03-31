---
title: Kontobehandlingssider og -moduler
description: Dette emnet dekker kontobehandlingssider og -moduler i Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 29523d03fb687684dae7d0ce08208905cce702df
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206637"
---
# <a name="account-management-pages-and-modules"></a><span data-ttu-id="690aa-103">Kontobehandlingssider og -moduler</span><span class="sxs-lookup"><span data-stu-id="690aa-103">Account management pages and modules</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="690aa-104">Dette emnet dekker kontobehandlingssider og -moduler i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="690aa-104">This topic covers account management pages and modules in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="690aa-105">Kontobehandling refererer til en gruppe med sider som brukes til å behandle informasjon som er relatert til brukerkontoer i Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="690aa-105">Account management refers to a group of pages that is used to manage user account–related information in Dynamics 365 Commerce.</span></span> <span data-ttu-id="690aa-106">Kontobehandlingssidene inkluderer målsiden for kontostyring, brukerprofilside, brukeradresseside, ordreloggside, ordredetaljerside, loyalitetsside og ønskelisteside.</span><span class="sxs-lookup"><span data-stu-id="690aa-106">Account management pages include the account management landing page, user profile page, user address page, order history page, order details page, loyalty page, and wish list page.</span></span>

### <a name="account-management-landing-page"></a><span data-ttu-id="690aa-107">Målside for kontobehandling</span><span class="sxs-lookup"><span data-stu-id="690aa-107">Account management landing page</span></span>

<span data-ttu-id="690aa-108">Målsiden for kontoadministrasjons bruker følgende moduler:</span><span class="sxs-lookup"><span data-stu-id="690aa-108">The account management landing page uses the following modules:</span></span>

- <span data-ttu-id="690aa-109">**Container** - Alle modulene for målside for kontobehandlings må plasseres i en container.</span><span class="sxs-lookup"><span data-stu-id="690aa-109">**Container** - All account management landing page modules should be placed within a container.</span></span> 
- <span data-ttu-id="690aa-110">**Velkomstflis for konto** – Denne modulen brukes til å gi en velkomstmelding på kontobehandlingssiden.</span><span class="sxs-lookup"><span data-stu-id="690aa-110">**Account welcome tile** – This module is used to provide a welcome message on the account management page.</span></span> <span data-ttu-id="690aa-111">Den inneholder egenskaper for overskriften.</span><span class="sxs-lookup"><span data-stu-id="690aa-111">It includes properties for the heading.</span></span>
- <span data-ttu-id="690aa-112">**Generell flis for konto** – Denne modulen kan brukes til å angi overskrifter og koblinger til kontobehandlingssider, for eksempel sidene Ordrehistorikk og Min profil.</span><span class="sxs-lookup"><span data-stu-id="690aa-112">**Account generic tile** - This module can be used to provide headings and links to account management pages, such as the "Order history" or "My profile" pages.</span></span> <span data-ttu-id="690aa-113">Generell flis-modulen kan brukes til å konfigurere en flis for en side.</span><span class="sxs-lookup"><span data-stu-id="690aa-113">The generic tile module can be used to configure a tile for any page.</span></span> <span data-ttu-id="690aa-114">I Fabrikam brukes denne modulen for koblinger for Ordrehistorikk- og Min profil-siden på målsiden for kontobehandling.</span><span class="sxs-lookup"><span data-stu-id="690aa-114">In Fabrikam, this module is used for "Order history" and "My profile" page links on the account management landing page.</span></span>
- <span data-ttu-id="690aa-115">**Ønskelisteflis for konto** – Denne modulen brukes til å gi et sammendrag av varene i kundens ønskeliste.</span><span class="sxs-lookup"><span data-stu-id="690aa-115">**Account wishlist tile** – This module is used to provide a summary of the items on the customer's wish list.</span></span> <span data-ttu-id="690aa-116">Det kan for eksempel stå "Du har 10 elementer i ønskelisten".</span><span class="sxs-lookup"><span data-stu-id="690aa-116">For example, it might state, "You have 10 items in your wish list."</span></span> <span data-ttu-id="690aa-117">Den inneholder egenskaper for overskriften og koblingen "Vis detaljer".</span><span class="sxs-lookup"><span data-stu-id="690aa-117">It includes properties for the heading and the "View details" link.</span></span> <span data-ttu-id="690aa-118">Vis detaljer-koblingen bør konfigureres til å omdirigere til ønskelistesiden.</span><span class="sxs-lookup"><span data-stu-id="690aa-118">The "View details" link should be configured to redirect to the wish list page.</span></span> 
- <span data-ttu-id="690aa-119">**Kontoadresseflis** – Denne modulen brukes til å gi et sammendrag av brukerens adresse.</span><span class="sxs-lookup"><span data-stu-id="690aa-119">**Account address tile** – This module is used to provide a summary of the user's addresses.</span></span> <span data-ttu-id="690aa-120">Det kan for eksempel stå "Du har lagt til 2 adresser i kontoen din".</span><span class="sxs-lookup"><span data-stu-id="690aa-120">For example, it might state, "You have 2 addresses added to your account."</span></span> <span data-ttu-id="690aa-121">Den inneholder egenskaper for overskriften og koblingen "Vis detaljer".</span><span class="sxs-lookup"><span data-stu-id="690aa-121">It includes properties for the heading and the "View details" link.</span></span> <span data-ttu-id="690aa-122">Vis detaljer-koblingen bør konfigureres til å omdirigere til brukeradressesiden.</span><span class="sxs-lookup"><span data-stu-id="690aa-122">The "View details" link should be configured to redirect to the user address page.</span></span>
- <span data-ttu-id="690aa-123">**Kontofordelsflis** – Denne modulen brukes til å vise og koble til informasjon om fordelsprogrammer.</span><span class="sxs-lookup"><span data-stu-id="690aa-123">**Account loyalty tile** – This module is used to display and link to loyalty program information.</span></span> <span data-ttu-id="690aa-124">Denne flisen har to tilstander: en tilstand viser koblinger til et fordelsprogram hvis brukeren ikke allerede er medlem.</span><span class="sxs-lookup"><span data-stu-id="690aa-124">This tile has two states: one state shows links to join a loyalty progam if the user is not a member already.</span></span> <span data-ttu-id="690aa-125">Den andre tilstanden viser koblinger for å vise siden med fordelsdetaljer når brukeren allerede er medlem.</span><span class="sxs-lookup"><span data-stu-id="690aa-125">The other state shows links to view the loyalty details page when the user is already a member.</span></span> <span data-ttu-id="690aa-126">Egenskaper inkluderer overskriften, Registrering-koblingen og Vis fordel-koblingen.</span><span class="sxs-lookup"><span data-stu-id="690aa-126">Properties include the heading, the "Sign-up" link, and the "View loyalty" link.</span></span> <span data-ttu-id="690aa-127">Vis fordel-koblingen bør konfigureres til å omdirigere til fordelssiden.</span><span class="sxs-lookup"><span data-stu-id="690aa-127">The "View loyalty" link should be configured to redirect to the loyalty page.</span></span> <span data-ttu-id="690aa-128">Registrering-koblingen kan konfigureres til å omadressere til en side der brukere kan bli med i fordelsprogrammet.</span><span class="sxs-lookup"><span data-stu-id="690aa-128">The "Sign-up" link should be configured to redirect to a page where users can join the loyalty program.</span></span> 

### <a name="order-history-page"></a><span data-ttu-id="690aa-129">Siden Ordrehistorikk</span><span class="sxs-lookup"><span data-stu-id="690aa-129">Order history page</span></span>

<span data-ttu-id="690aa-130">Siden for ordrehistorikk bruker ordreloggmodulen til å vise alle de siste ordrene som brukeren har lagt inn.</span><span class="sxs-lookup"><span data-stu-id="690aa-130">The order history page uses the order history module to show all the recent orders that the user has placed.</span></span>

### <a name="order-details-page"></a><span data-ttu-id="690aa-131">Side for ordredetaljer</span><span class="sxs-lookup"><span data-stu-id="690aa-131">Order details page</span></span>

<span data-ttu-id="690aa-132">Ordredetaljer-siden inneholder detaljert informasjon for hver ordre og er tilgjengelig fra ordrehistorikksiden.</span><span class="sxs-lookup"><span data-stu-id="690aa-132">The order details page provides detailed information for each order and is accessed from the order history page.</span></span> <span data-ttu-id="690aa-133">Den bruker ordredetaljermodulen, som krever salgs-IDen eller transaksjons-IDen for å hente ordredetaljene.</span><span class="sxs-lookup"><span data-stu-id="690aa-133">It uses the order details module, which requires the sales ID or transaction ID to retrieve the order details.</span></span>

### <a name="user-profile-page"></a><span data-ttu-id="690aa-134">Brukerprofilside</span><span class="sxs-lookup"><span data-stu-id="690aa-134">User profile page</span></span>

<span data-ttu-id="690aa-135">Siden brukerprofil viser brukerkontodetaljer, for eksempel brukerens navn og e-postadresse.</span><span class="sxs-lookup"><span data-stu-id="690aa-135">The user profile page shows user account details, such as a user's name and email address.</span></span> <span data-ttu-id="690aa-136">Den bruker brukerprofildetaljene og brukerprofilredigeringsmodulene.</span><span class="sxs-lookup"><span data-stu-id="690aa-136">It uses the user profile details and user profile edit modules.</span></span> <span data-ttu-id="690aa-137">Selv om epostadresse ikke kan fjernes, kan den redigeres.</span><span class="sxs-lookup"><span data-stu-id="690aa-137">Although the email address can't be removed, it can be edited.</span></span> <span data-ttu-id="690aa-138">Brukerprofilsiden viser også brukerpreferansene som gjør en bruker i stand til å velge/velge bort bestemte funksjoner, for eksempel tilpassing av anbefalingslister.</span><span class="sxs-lookup"><span data-stu-id="690aa-138">The user profile page also shows user preferences that enable a user to opt in or opt out from certain features, such as personalization of recommendation lists.</span></span> 

### <a name="user-address-page"></a><span data-ttu-id="690aa-139">Brukeradresseside</span><span class="sxs-lookup"><span data-stu-id="690aa-139">User address page</span></span>

<span data-ttu-id="690aa-140">Siden for brukeradresse viser listen over adresser som er knyttet til brukerkontoen.</span><span class="sxs-lookup"><span data-stu-id="690aa-140">The user address page shows the list of addresses that are associated with the user account.</span></span> <span data-ttu-id="690aa-141">Brukeren har enten oppgitt disse adressene under utsjekking eller lagt dem til direkte på denne siden.</span><span class="sxs-lookup"><span data-stu-id="690aa-141">The user either provided these addresses during checkout or added them directly on  this page.</span></span> <span data-ttu-id="690aa-142">Brukeradressemodulen brukes til å legge til og redigere adresser, angi primæradresse og gjengi eksisterende adresser på siden.</span><span class="sxs-lookup"><span data-stu-id="690aa-142">The user address module is used add and edit addresses, set the primary address, and render existing addresses on the page.</span></span>

### <a name="wish-list-page"></a><span data-ttu-id="690aa-143">Ønskelisteside</span><span class="sxs-lookup"><span data-stu-id="690aa-143">Wish list page</span></span>

<span data-ttu-id="690aa-144">Ønskelistesiden viser varene som er lagt til på kundens ønskeliste.</span><span class="sxs-lookup"><span data-stu-id="690aa-144">The wish list page shows the items that have been added to the customer's wish list.</span></span> <span data-ttu-id="690aa-145">Den bruker ønskelistemodulen til å vise ønskelisteelementer.</span><span class="sxs-lookup"><span data-stu-id="690aa-145">It uses the wish list module to render wish list items.</span></span>

### <a name="loyalty-page"></a><span data-ttu-id="690aa-146">Fordelsside</span><span class="sxs-lookup"><span data-stu-id="690aa-146">Loyalty page</span></span>

<span data-ttu-id="690aa-147">Fordelssiden lar kunder vise sine fordelsdetaljer hvis de allerede er medlemmer av fordelsprogrammet.</span><span class="sxs-lookup"><span data-stu-id="690aa-147">The loyalty page lets customers view their loyalty details if they are already loyalty program members.</span></span> <span data-ttu-id="690aa-148">De kan også vise poengene de har tjent opp og løst inn i nylige transaksjoner.</span><span class="sxs-lookup"><span data-stu-id="690aa-148">They can also view the points that they have earned and redeemed in recent transactions.</span></span> <span data-ttu-id="690aa-149">Siden bruker modulen for fordelsdetaljer til å vise fordelsdetaljene.</span><span class="sxs-lookup"><span data-stu-id="690aa-149">The page uses the loyalty details module to showcase the loyalty details.</span></span> 

<span data-ttu-id="690aa-150">For å bli med i et fordelsprogram kan det opprettes en markedsføringsside med moduler for fordelsregistrering og fordelsvilkår.</span><span class="sxs-lookup"><span data-stu-id="690aa-150">To join loyalty program, a marketing page can be created with loyalty sign up and loyalty terms modules.</span></span> <span data-ttu-id="690aa-151">Hvis brukeren ikke er medlem av et fordelsprogram, vil disse modulene gjøre det mulig for brukeren å registrere seg.</span><span class="sxs-lookup"><span data-stu-id="690aa-151">If the user is not a member of a loyalty program, these modules will enable the user to sign up.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="690aa-152">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="690aa-152">Additional resources</span></span>

[<span data-ttu-id="690aa-153">Oversikt over modulbibliotek</span><span class="sxs-lookup"><span data-stu-id="690aa-153">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="690aa-154">Beholdermodul</span><span class="sxs-lookup"><span data-stu-id="690aa-154">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="690aa-155">Kjøpsboksmodul</span><span class="sxs-lookup"><span data-stu-id="690aa-155">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="690aa-156">Handlekurvmodul</span><span class="sxs-lookup"><span data-stu-id="690aa-156">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="690aa-157">Kassemodul</span><span class="sxs-lookup"><span data-stu-id="690aa-157">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="690aa-158">Ordrebekreftelsesmodul</span><span class="sxs-lookup"><span data-stu-id="690aa-158">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="690aa-159">Topptekstmodul</span><span class="sxs-lookup"><span data-stu-id="690aa-159">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="690aa-160">Bunntekstmodul</span><span class="sxs-lookup"><span data-stu-id="690aa-160">Footer module</span></span>](author-footer-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]