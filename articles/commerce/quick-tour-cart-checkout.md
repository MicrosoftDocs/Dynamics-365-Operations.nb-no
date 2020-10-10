---
title: Oversikt over sider for handlekurv og kasse
description: Dette emnet inneholder en oversikt over sider for handlekurv og kasse i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
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
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e932be31a301ef5aacb68fa4e710d8a9137b7263
ms.sourcegitcommit: 8028fbc5b9585e87d3331ea02577ff82ede090af
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/16/2020
ms.locfileid: "3817784"
---
# <a name="cart-and-checkout-pages-overview"></a><span data-ttu-id="1c991-103">Oversikt over sider for handlekurv og kasse</span><span class="sxs-lookup"><span data-stu-id="1c991-103">Cart and checkout pages overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1c991-104">Dette emnet inneholder en oversikt over sider for handlekurv og kasse i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="1c991-104">This topic provides an overview of the cart and checkout pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="1c991-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="1c991-105">Overview</span></span>

<span data-ttu-id="1c991-106">Handlekurvsiden for et e-handelsområde viser alle varene som en kunde har lagt til i handlekurven.</span><span class="sxs-lookup"><span data-stu-id="1c991-106">The cart page of an e-Commerce website shows all items that a customer has added to the cart.</span></span> <span data-ttu-id="1c991-107">Handlekurvsiden bygges ved hjelp av handlemodulen.</span><span class="sxs-lookup"><span data-stu-id="1c991-107">The cart page is built by using the cart module.</span></span> <span data-ttu-id="1c991-108">Handlekurvmodulen er en container som er vert for alle modulene som kreves for å vise varer i handlekurven.</span><span class="sxs-lookup"><span data-stu-id="1c991-108">The cart module is a container that hosts all the modules that are required to showcase items in the cart.</span></span> <span data-ttu-id="1c991-109">Handlekurvmodulen kan også bruke de andre modulene for å vise ordresammendraget og eventuelle kampanjekoder som er brukt på kundeordren.</span><span class="sxs-lookup"><span data-stu-id="1c991-109">The cart module can also use other modules to show the order summary and any promotional codes that have been applied to the customer order.</span></span>

<span data-ttu-id="1c991-110">Kassesiden for et webområde for e-handel viser en trinnvis flyt som kundene følger for å angi all informasjon som kreves for å legge inn en ordre.</span><span class="sxs-lookup"><span data-stu-id="1c991-110">The checkout page of an e-Commerce website presents a step-by-step flow that customers follow to enter all the information that is required to place an order.</span></span> <span data-ttu-id="1c991-111">En kassemodul kan inneholde moduler som håndterer leveringsadressen, leveringsmetoder, faktureringsinformasjon, ordresammendrag og annen informasjon som er knyttet til kundeordrer.</span><span class="sxs-lookup"><span data-stu-id="1c991-111">A checkout module can include modules that handle the shipping address, shipping methods, billing information, order summary, and other information that is related to customer orders.</span></span>

## <a name="cart-page"></a><span data-ttu-id="1c991-112">Handlevognside</span><span class="sxs-lookup"><span data-stu-id="1c991-112">Cart page</span></span>

<span data-ttu-id="1c991-113">Handlekurvsidene fungerer som handlepose og inneholder alle varene som er lagt til i handlekurven.</span><span class="sxs-lookup"><span data-stu-id="1c991-113">The cart page serves as the shopping bag and includes all the items that have been added to the cart.</span></span>

<span data-ttu-id="1c991-114">Illustrasjonen nedenfor viser et eksempel på en handlekurvside som ble bygd ved hjelp av modulbiblioteket og "Fabrikam"-temaet.</span><span class="sxs-lookup"><span data-stu-id="1c991-114">The following illustration show an example of a cart page that was built by using the module library and the "Fabrikam" theme.</span></span>

![Eksempel på en handlekurvside](./media/cart2.PNG)

<span data-ttu-id="1c991-116">Hovedområdet på en handlekurvside viser alle varene som en kunde har lagt til i handlekurven.</span><span class="sxs-lookup"><span data-stu-id="1c991-116">The main body of the cart page shows all the items that the customer has added to the cart.</span></span> <span data-ttu-id="1c991-117">Alle gjeldende rabatter vises.</span><span class="sxs-lookup"><span data-stu-id="1c991-117">All applicable discounts are showcased.</span></span> <span data-ttu-id="1c991-118">Disse rabattene inkluderer komplekse rabatter.</span><span class="sxs-lookup"><span data-stu-id="1c991-118">These discounts include complex discounts.</span></span> <span data-ttu-id="1c991-119">Eksempler inkluderer "Kjøp 3 varer og få 10 % avslag" eller "Kjøp en flaske og en ryggsekk for å få 10 % rabatt".</span><span class="sxs-lookup"><span data-stu-id="1c991-119">Examples include "Buy 3 items and get 10% off" or "Buy a bottle and a backpack to get 10% off."</span></span> <span data-ttu-id="1c991-120">Ordresammendragmodulen viser beløpet som forfaller etter at rabatter, levering, avgifter og så videre er påført.</span><span class="sxs-lookup"><span data-stu-id="1c991-120">The order summary module shows the amount that is due after discounts, shipping, taxes, and so on, have been applied.</span></span> <span data-ttu-id="1c991-121">Det finnes også en promokodemodul som lar kunden bruke eller fjerne kampanjekoder.</span><span class="sxs-lookup"><span data-stu-id="1c991-121">There is also a promo code module that lets the customer apply or remove promotional codes.</span></span>

<span data-ttu-id="1c991-122">En kunde kan handle anonymt eller som en pålogget bruker.</span><span class="sxs-lookup"><span data-stu-id="1c991-122">A customer can shop anonymously or as a signed-in user.</span></span> <span data-ttu-id="1c991-123">Hvis en kunde er pålogget, beholdes varer i handlekurven mellom økter.</span><span class="sxs-lookup"><span data-stu-id="1c991-123">If a customer is signed in, items in the cart are preserved between sessions.</span></span> <span data-ttu-id="1c991-124">På denne måten kan kunden fortsette å handle fra flere enheter.</span><span class="sxs-lookup"><span data-stu-id="1c991-124">In this way, the customer can continue to shop from multiple devices.</span></span>

<span data-ttu-id="1c991-125">Kunden kan gå videre til kassen fra handlekurven.</span><span class="sxs-lookup"><span data-stu-id="1c991-125">From the cart, the customer can proceed to checkout.</span></span> <span data-ttu-id="1c991-126">En kunde kan starte utsjekking som en gjestebruker eller som en pålogget bruker.</span><span class="sxs-lookup"><span data-stu-id="1c991-126">A customer can initiate checkout as a guest user or as a signed-in user.</span></span>

<span data-ttu-id="1c991-127">Hvis du vil ha informasjon om hvordan du redigerer en handlekurv, se [Legge til en handlekurvmodul på en side](add-cart-module.md).</span><span class="sxs-lookup"><span data-stu-id="1c991-127">For information about how to author a cart page, see [Add a cart module to a page](add-cart-module.md).</span></span>

## <a name="checkout-page"></a><span data-ttu-id="1c991-128">Utsjekkingsside</span><span class="sxs-lookup"><span data-stu-id="1c991-128">Checkout page</span></span>

<span data-ttu-id="1c991-129">Utsjekkingssiden er der kunder angir informasjonen som kreves for å legge inn en ordre.</span><span class="sxs-lookup"><span data-stu-id="1c991-129">The checkout page is where customers enter the information that is required to place an order.</span></span>

<span data-ttu-id="1c991-130">Illustrasjonen nedenfor viser et eksempel på en utsjekkingsside som ble bygd ved hjelp av modulbiblioteket.</span><span class="sxs-lookup"><span data-stu-id="1c991-130">The following illustration show an example of a checkout page that was built by using the module library.</span></span>

![Eksempel på en utsjekkingsside](./media/Checkout.PNG)

<span data-ttu-id="1c991-132">Hoveddelen av utsjekkingssiden er der all ordreinformasjon samles inn.</span><span class="sxs-lookup"><span data-stu-id="1c991-132">The main body of the checkout page is where all the order information is collected.</span></span> <span data-ttu-id="1c991-133">Denne informasjonen omfatter leveringsadresse, leveringsalternativer og betalingsinformasjon.</span><span class="sxs-lookup"><span data-stu-id="1c991-133">This information includes the shipping address, delivery options, and payment information.</span></span> <span data-ttu-id="1c991-134">Kassen har en trinnvis flyt, fordi informasjonen må angis i en bestemt rekkefølge for å kunne behandles.</span><span class="sxs-lookup"><span data-stu-id="1c991-134">Checkout has a step-by-step flow, because the information must be entered in a specific order to be processed.</span></span> <span data-ttu-id="1c991-135">Leveringsadressen må for eksempel angis før forsendelseskostnadene kan beregnes og betalingen kan autoriseres.</span><span class="sxs-lookup"><span data-stu-id="1c991-135">For example, the shipping address must be entered before the shipping costs can be calculated and the payment can be authorized.</span></span>

### <a name="shipping-address"></a><span data-ttu-id="1c991-136">Leveringsadresse</span><span class="sxs-lookup"><span data-stu-id="1c991-136">Shipping address</span></span>

<span data-ttu-id="1c991-137">Det kreves en forsendelsesadresse hvis varer må sendes.</span><span class="sxs-lookup"><span data-stu-id="1c991-137">A shipping address is required if items must be shipped.</span></span> <span data-ttu-id="1c991-138">Formatet for forsendelsesadresser for hver nasjonal innstilling kan konfigureres i Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="1c991-138">The format of shipping addresses for each locale can be configured in Dynamics 365 Commerce.</span></span> <span data-ttu-id="1c991-139">Hvis varene for eksempel skal leveres til USA, må leveringsadressen inneholde en gateadresse, stat og postnummer (ZIP).</span><span class="sxs-lookup"><span data-stu-id="1c991-139">For example, if the items will be shipped to the United States, the shipping address must include a street address, state, and ZIP Code.</span></span> <span data-ttu-id="1c991-140">Noe grunnleggende inndatavalidering utføres for felt for leveringsadresse, for eksempel validering for alfanumeriske tegn, maksimumslengde og tall.</span><span class="sxs-lookup"><span data-stu-id="1c991-140">Some basic input validation is done for shipping address fields, such as validation for alphanumeric characters, maximum length, and numbers.</span></span> <span data-ttu-id="1c991-141">Selv om selve adressen ikke er bekreftet, kan denne verifiseringen utføres ved hjelp av tilpassede tredjepartstjenester.</span><span class="sxs-lookup"><span data-stu-id="1c991-141">Although the validity of the address itself isn't verified, this verification can be done by using customized third-party services.</span></span>

<span data-ttu-id="1c991-142">Leveringsadressen brukes for alle varene i handlekurven som "forsendelse"-alternativet er valgt for.</span><span class="sxs-lookup"><span data-stu-id="1c991-142">The shipping address is applied to all items in the cart that the "ship" option is selected for.</span></span> <span data-ttu-id="1c991-143">Hvis du bruker utsjekkingsflyten som er oppgitt i modulbiblioteket, kan ikke individuelle handlekurvvarer sendes til forskjellige adresser.</span><span class="sxs-lookup"><span data-stu-id="1c991-143">If you use the checkout flow that is provided in the module library, individual cart items can't be shipped to different addresses.</span></span> <span data-ttu-id="1c991-144">Hvis du trenger denne funksjonen, kan den implementeres ved hjelp av tilpasning av kassemodulene.</span><span class="sxs-lookup"><span data-stu-id="1c991-144">If you require this capability, it can be implemented through customization of the checkout modules.</span></span>

<span data-ttu-id="1c991-145">Når leveringsadressen er angitt, vises forsendelsesmetodene som er tilgjengelige fra Dynamics 365 Commerce-nettbutikken.</span><span class="sxs-lookup"><span data-stu-id="1c991-145">After the shipping address is provided, the shipping methods that are available from the Dynamics 365 Commerce online store are shown.</span></span> <span data-ttu-id="1c991-146">Forsendelsesmetodene og adressene de støtter, kan konfigureres i Commerce.</span><span class="sxs-lookup"><span data-stu-id="1c991-146">The shipping methods and the addresses that they support can be configured in Commerce.</span></span>

### <a name="payment"></a><span data-ttu-id="1c991-147">Betaling</span><span class="sxs-lookup"><span data-stu-id="1c991-147">Payment</span></span>

<span data-ttu-id="1c991-148">Neste trinn i utsjekkingsflyten er betalingen.</span><span class="sxs-lookup"><span data-stu-id="1c991-148">The next step in the checkout flow is payment.</span></span> <span data-ttu-id="1c991-149">I e-handel kan flere betalingsmåter brukes til å legge inn bestillinger, for eksempel kredittkort, gavekort og fordelspoeng.</span><span class="sxs-lookup"><span data-stu-id="1c991-149">In e-Commerce, multiple methods of payment can be used to place orders, such as credit cards, gift cards, and loyalty points.</span></span> <span data-ttu-id="1c991-150">En kombinasjon av disse betalingsmåtene kan også brukes.</span><span class="sxs-lookup"><span data-stu-id="1c991-150">A combination of these payment methods can also be used.</span></span> <span data-ttu-id="1c991-151">Det kan være nødvendig med mer informasjon, avhengig av betalingsmåtene som brukes.</span><span class="sxs-lookup"><span data-stu-id="1c991-151">Depending on the payment methods that are used, additional information might be required.</span></span> <span data-ttu-id="1c991-152">En kredittkort betaling krever for eksempel en faktureringsadresse.</span><span class="sxs-lookup"><span data-stu-id="1c991-152">For example, a credit card payment requires a billing address.</span></span> <span data-ttu-id="1c991-153">Kredittkortbetalinger behandles ved hjelp av betalingskoblingen Adyen.</span><span class="sxs-lookup"><span data-stu-id="1c991-153">Credit card payments are processed by using the Adyen Payment Connector.</span></span>

#### <a name="loyalty-points"></a><span data-ttu-id="1c991-154">Fordelspoeng</span><span class="sxs-lookup"><span data-stu-id="1c991-154">Loyalty points</span></span>

<span data-ttu-id="1c991-155">Under betalingsflyten kan en kunde som er medlem av et fordelsprogram, og som har påløpte fordelspoeng, løse inn disse fordelspoengene for en ordre.</span><span class="sxs-lookup"><span data-stu-id="1c991-155">During the checkout flow, a customer who is a member of a loyalty program and who has accrued loyalty points can redeem those loyalty points for an order.</span></span> <span data-ttu-id="1c991-156">Fordelspoengmodulen vises bare hvis kunden har et eksisterende fordelsmedlemskap.</span><span class="sxs-lookup"><span data-stu-id="1c991-156">The loyalty points module is shown only if the customer has an existing loyalty membership.</span></span> <span data-ttu-id="1c991-157">For ikke-medlemmer og gjestebrukere er denne modulen skjult.</span><span class="sxs-lookup"><span data-stu-id="1c991-157">For non-members and guest users, this module is hidden.</span></span>

#### <a name="gift-cards"></a><span data-ttu-id="1c991-158">Gavekort</span><span class="sxs-lookup"><span data-stu-id="1c991-158">Gift cards</span></span>

<span data-ttu-id="1c991-159">I modulbiblioteket kan du løse inn interne gavekort for en ordre.</span><span class="sxs-lookup"><span data-stu-id="1c991-159">The module library lets internal gift cards be redeemed for an order.</span></span> <span data-ttu-id="1c991-160">Hvis du vil bruke et internt gavekort, må kunden være pålogget.</span><span class="sxs-lookup"><span data-stu-id="1c991-160">To apply an internal gift card, the customer must be signed in.</span></span> <span data-ttu-id="1c991-161">For ytterligere sikkerhet anbefaler vi at du tilpasser flyten ved hjelp av et personlig ID-nummer (PIN) for interne gavekort.</span><span class="sxs-lookup"><span data-stu-id="1c991-161">For additional security, we recommend that you customize the flow by using a personal identification number (PIN) for internal gift cards.</span></span>

### <a name="signed-in-and-guest-users"></a><span data-ttu-id="1c991-162">Påloggede brukere og gjestebrukere</span><span class="sxs-lookup"><span data-stu-id="1c991-162">Signed-in and guest users</span></span>

<span data-ttu-id="1c991-163">Kunden kan fullføre utsjekkingsprosessen som en gjestebruker eller som en pålogget bruker.</span><span class="sxs-lookup"><span data-stu-id="1c991-163">The customer can complete the checkout process as a guest user or a signed-in user.</span></span> <span data-ttu-id="1c991-164">Hvis kunden logger på, hentes kontoopplysninger som lagrede leveringsadresser og lagrede kredittkortopplysninger automatisk.</span><span class="sxs-lookup"><span data-stu-id="1c991-164">If the customer signs in, account information such as saved shipping addresses and saved credit card details is automatically retrieved.</span></span>

### <a name="order-summary"></a><span data-ttu-id="1c991-165">Ordresammendrag</span><span class="sxs-lookup"><span data-stu-id="1c991-165">Order summary</span></span>

<span data-ttu-id="1c991-166">Utsjekkingen viser et sammendrag av linjevarene i handlekurven, slik at kunden kan kontrollere ordren før han eller hun utfører den.</span><span class="sxs-lookup"><span data-stu-id="1c991-166">Checkout shows a summary of the line items in the cart, so that the customer can verify the order before he or she places it.</span></span> <span data-ttu-id="1c991-167">Linjeelementene kan ikke redigeres i løpet av utsjekkingsflyten.</span><span class="sxs-lookup"><span data-stu-id="1c991-167">The line items can't be edited during the checkout flow.</span></span> <span data-ttu-id="1c991-168">En kobling til handlekurven vises imidlertid i tilfelle brukeren ønsker å gå tilbake og redigere linjeelementer.</span><span class="sxs-lookup"><span data-stu-id="1c991-168">However, a link to the cart is provided in case the user wants to go back and edit line items.</span></span>

<span data-ttu-id="1c991-169">Etter at kunden har gitt leverings- og faktureringsinformasjon, viser ordresammendraget beløpet som forfaller etter fordelspoeng, gavekort og andre betalinger er brukt.</span><span class="sxs-lookup"><span data-stu-id="1c991-169">After the customer provides shipping and billing information, the order summary reflects the amount that is due after loyalty points, gift cards, and other payments have been applied.</span></span>

### <a name="order-confirmation-and-email"></a><span data-ttu-id="1c991-170">Ordrebekreftelse og e-post</span><span class="sxs-lookup"><span data-stu-id="1c991-170">Order confirmation and email</span></span>

<span data-ttu-id="1c991-171">Når kunden legger inn en ordre, blir det oppgitt et bekreftelsesnummer.</span><span class="sxs-lookup"><span data-stu-id="1c991-171">When the customer places an order, a confirmation number is provided.</span></span> <span data-ttu-id="1c991-172">På dette stadiet er betalingen godkjent, men ikke belastet.</span><span class="sxs-lookup"><span data-stu-id="1c991-172">At this point, the payment has been authorized but not charged.</span></span> <span data-ttu-id="1c991-173">Betalingen blir bare belastet når ordren er oppfylt (det vil si når den enten er levert eller plukket opp).</span><span class="sxs-lookup"><span data-stu-id="1c991-173">The payment will be charged only when the order is fulfilled (that is, when it's either shipped or picked up).</span></span>

<span data-ttu-id="1c991-174">Når en ordre er opprettet, sendes det en e-post for ordrebekreftelse til kunden.</span><span class="sxs-lookup"><span data-stu-id="1c991-174">After an order is created, an order confirmation email is sent to the customer.</span></span>

<span data-ttu-id="1c991-175">Hvis du vil ha mer informasjon om hvordan du redigerer en kasseside, se [Legge til en kassemodul på en side](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="1c991-175">For more information about how to author a checkout page, see [Add a checkout module to a page](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1c991-176">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="1c991-176">Additional resources</span></span>

[<span data-ttu-id="1c991-177">Oversikt over startside</span><span class="sxs-lookup"><span data-stu-id="1c991-177">Home page overview</span></span>](quick-tour-home-page.md)

[<span data-ttu-id="1c991-178">Oversikt over produktdetaljsider</span><span class="sxs-lookup"><span data-stu-id="1c991-178">Product details pages overview</span></span>](quick-tour-pdp.md)

[<span data-ttu-id="1c991-179">Oversikt over kontobehandlingssider</span><span class="sxs-lookup"><span data-stu-id="1c991-179">Account management pages overview</span></span>](quick-tour-account-management.md)
