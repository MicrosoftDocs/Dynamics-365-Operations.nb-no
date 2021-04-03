---
title: Henteinformasjonsmodul
description: Dette emnet dekker henteinformasjonsmodulen og beskriver hvordan du legger den til på utsjekkingssider i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 11/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-09021
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 222e8ad79b30e5197f7140958309d442b284f286
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5263186"
---
# <a name="pickup-information-module"></a><span data-ttu-id="92707-103">Hente informasjonsmodul</span><span class="sxs-lookup"><span data-stu-id="92707-103">Pickup information module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="92707-104">Dette emnet dekker henteinformasjonsmodulen og beskriver hvordan du legger den til på utsjekkingssider i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="92707-104">This topic covers the pickup information module and describes how to add it to checkout pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="92707-105">Henteinformasjonsmodulen kan brukes i en kassemodulen til å vise henteinformasjon for ordre.</span><span class="sxs-lookup"><span data-stu-id="92707-105">The pickup information module can be used in a checkout module to show order pickup information.</span></span> <span data-ttu-id="92707-106">Kunder kan se tilgjengelige hentedatoer og -tidspunkter, og deretter velge en passende tid for å hente ordren.</span><span class="sxs-lookup"><span data-stu-id="92707-106">Customers can view available pickup dates and time slots, and then select a suitable time to pick up their order.</span></span> <span data-ttu-id="92707-107">En kunde kan for eksempel velge å hente en ordre klokken 15:00 den 21. mars fra San Francisco-butikken.</span><span class="sxs-lookup"><span data-stu-id="92707-107">For example, a customer can choose to pick up an order at 3 PM on March 21 from the San Francisco store.</span></span>

<span data-ttu-id="92707-108">Hentetidspunkter for de aktuelle butikkene må konfigureres i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="92707-108">Pickup time slots for the appropriate stores must be configured in Commerce headquarters.</span></span> <span data-ttu-id="92707-109">Hvis du vil ha mer informasjon, kan du se [Opprette og oppdatere tidspunkter for kundehenting](dev-itpro/pickup-timeslots.md).</span><span class="sxs-lookup"><span data-stu-id="92707-109">For more information, see [Create and update time slots for customer pickup](dev-itpro/pickup-timeslots.md).</span></span>

<span data-ttu-id="92707-110">Hvis en henteinformasjonsmodul opprettes på en utsjekkingsside, men det ikke er definert noen tidspunkter for butikken som er valgt for henting, vil modulen vise informasjon, men brukeren vil ikke kunne velge noen tidspunkter.</span><span class="sxs-lookup"><span data-stu-id="92707-110">If a pickup information module is created on a checkout page, but no time slots are defined for the store that is selected for pickup, the module will show information, but the user won't be able to select any time slots.</span></span> <span data-ttu-id="92707-111">Tidspunkter er valgfrie og kreves ikke for å legge inn en ordre.</span><span class="sxs-lookup"><span data-stu-id="92707-111">Time slots are optional and aren't required to place an order.</span></span>

<span data-ttu-id="92707-112">Hvis flere varer er valgt for henting på tvers av flere butikker, last henteinformasjonsmodulen brukeren velge et tidspunkt for hver butikk, forutsatt at tidspunktene er tilgjengelige for den.</span><span class="sxs-lookup"><span data-stu-id="92707-112">If multiple items are selected for pickup across multiple stores, the pickup information module will let the user select a time slot for each store, provided that time slots are available for it.</span></span>

> [!NOTE]
> <span data-ttu-id="92707-113">Støtte for henteinformasjonsmodulen for tidspunkter og utsjekking er tilgjengelig i Dynamics 365 Commerce, versjon 10.0.15 og nyere.</span><span class="sxs-lookup"><span data-stu-id="92707-113">Support for time slots and the checkout pickup information module is available in Dynamics 365 Commerce version 10.0.15 and later.</span></span>

<span data-ttu-id="92707-114">Følgende illustrasjon viser et eksempel på valg av tidspunkt ved hjelp av henteinformasjonsmodulen på en utsjekkingsside.</span><span class="sxs-lookup"><span data-stu-id="92707-114">The following illustration shows an example of time slot selection through the pickup information module on a checkout page.</span></span>

![Eksempel på en henteinformasjonsmodul på en utsjekkingsside](./dev-itpro/media/Curbside_timeslot_eCommerce.PNG)

## <a name="module-properties"></a><span data-ttu-id="92707-116">Modulegenskaper</span><span class="sxs-lookup"><span data-stu-id="92707-116">Module properties</span></span>

- <span data-ttu-id="92707-117">**Overskrift** – Angi en overskrift for modulen.</span><span class="sxs-lookup"><span data-stu-id="92707-117">**Heading** – Enter a heading for the module.</span></span>

## <a name="show-time-slot-information-after-an-order-is-placed"></a><span data-ttu-id="92707-118">Vis informasjon om tidspunkt etter at en ordre er bestilt</span><span class="sxs-lookup"><span data-stu-id="92707-118">Show time slot information after an order is placed</span></span>

<span data-ttu-id="92707-119">Etter at en ordre er bestilt, kan informasjon om det valgte tidspunktet vises i [ordrebekreftelsesmodulen](order-confirmation-module.md) og [ordredetaljmodulen](account-management.md#order-details-page).</span><span class="sxs-lookup"><span data-stu-id="92707-119">After an order is placed, information about the selected time slot can be viewed in the [order confirmation module](order-confirmation-module.md) and the [order details module](account-management.md#order-details-page).</span></span> <span data-ttu-id="92707-120">Begge disse modulene har en egenskap for **Vis tidspunktinformasjon**.</span><span class="sxs-lookup"><span data-stu-id="92707-120">Both these modules have a **Show timeslot information** property.</span></span> <span data-ttu-id="92707-121">Før de kan vise det valgte tidspunktet i løpet av ordreprosessen, må denne egenskapen settes til **sann**.</span><span class="sxs-lookup"><span data-stu-id="92707-121">Before they can show the selected time slot during the order process, this property must be set to **True**.</span></span>

## <a name="add-a-checkout-pickup-information-module-to-a-page"></a><span data-ttu-id="92707-122">Legg til en henteinformasjonsmodul for utsjekking på en side</span><span class="sxs-lookup"><span data-stu-id="92707-122">Add a checkout pickup information module to a page</span></span>

<span data-ttu-id="92707-123">Hvis du vil ha informasjon om hvordan du legger til en henteinformasjonsmodul på en kasseside og angir de nødvendige egenskapene, kan du se [Kassemodul](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="92707-123">For instructions about how to add a pickup information module to a checkout page and set the required properties, see [Checkout module](add-checkout-module.md).</span></span>

<span data-ttu-id="92707-124">Følgende illustrasjon viser et eksempel på en betalingsside for e-handel som inkluderer tidspunkter for hentelinjevarer.</span><span class="sxs-lookup"><span data-stu-id="92707-124">The following illustration shows an example of an e-Commerce checkout page that includes time slots for pickup line items.</span></span>

![Eksempel på en betalingsside for e-handel som inkluderer tidspunkter for hentelinjevarer](./dev-itpro/media/Curbside_timeslot_eCommerce_checkoutsummary.PNG)

## <a name="additional-resources"></a><span data-ttu-id="92707-126">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="92707-126">Additional resources</span></span>

[<span data-ttu-id="92707-127">Opprett og oppdater tidspunkter for kundehenting</span><span class="sxs-lookup"><span data-stu-id="92707-127">Create and update time slots for customer pickup</span></span>](dev-itpro/pickup-timeslots.md)

[<span data-ttu-id="92707-128">Kassemodul</span><span class="sxs-lookup"><span data-stu-id="92707-128">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="92707-129">Ordrebekreftelsesmodul</span><span class="sxs-lookup"><span data-stu-id="92707-129">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="92707-130">Ordredetaljermodul</span><span class="sxs-lookup"><span data-stu-id="92707-130">Order details module</span></span>](account-management.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]