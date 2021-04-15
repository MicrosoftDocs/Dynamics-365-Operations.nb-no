---
title: Registreringsside for kredittkort viser en feil i betalingsprosessen
description: Dette emnet gir feilsøkingsveiledning som kan hjelpe når delen Betalingsmåte ikke er lastet inn og viser en feilmelding.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: d2c5f01d17df79c9b23fd513aaeb5c0605d657e9
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801777"
---
# <a name="credit-card-entry-page-shows-an-error-at-checkout"></a><span data-ttu-id="0cb8b-103">Registreringsside for kredittkort viser en feil i betalingsprosessen</span><span class="sxs-lookup"><span data-stu-id="0cb8b-103">Credit card entry page shows an error at checkout</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0cb8b-104">Dette emnet gir feilsøkingsveiledning som kan hjelpe når delen **Betalingsmåte** ikke er lastet inn og viser en feilmelding.</span><span class="sxs-lookup"><span data-stu-id="0cb8b-104">This topic provides troubleshooting guidance that can help when the **Payment method** section isn't loaded and shows an error message.</span></span>

## <a name="description"></a><span data-ttu-id="0cb8b-105">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="0cb8b-105">Description</span></span>

<span data-ttu-id="0cb8b-106">Når du åpner betalingssiden til en nettbutikk, blir ikke delen **Betalingsmåte** lastet og følgende feilmelding vises: "Noe gikk galt.</span><span class="sxs-lookup"><span data-stu-id="0cb8b-106">When you open the checkout page of an online store, the **Payment method** section isn't loaded, and the following error message is shown: "Something went wrong.</span></span> <span data-ttu-id="0cb8b-107">Prøv på nytt senere."</span><span class="sxs-lookup"><span data-stu-id="0cb8b-107">Please try again later."</span></span>

![Feil i betalingsmodul](media/payment-module-error.jpg)

## <a name="resolution"></a><span data-ttu-id="0cb8b-109">Oppløsning</span><span class="sxs-lookup"><span data-stu-id="0cb8b-109">Resolution</span></span>

### <a name="wait-for-the-commerce-scale-unit-cache-to-expire"></a><span data-ttu-id="0cb8b-110">Vent til bufferen for Commerce Scale Unit utløper</span><span class="sxs-lookup"><span data-stu-id="0cb8b-110">Wait for the Commerce Scale Unit cache to expire</span></span>

<span data-ttu-id="0cb8b-111">Betalingstjenesteinnstillingene på betalingssiden til den elektroniske butikken hurtigbufres på Commerce Scale Unit, og det kan ta opptil 15 minutter å vises på e-handelsområdet.</span><span class="sxs-lookup"><span data-stu-id="0cb8b-111">The payment service settings on the online store's checkout page are cached on the Commerce Scale Unit and can take up to 15 minutes to appear on the e-commerce site.</span></span> <span data-ttu-id="0cb8b-112">Disse innstillingene for betalingstjenesten inkluderer endringer i forretningskonto-IDen, sky-API-nøkkelen og ulike konfigurasjonsinnstillinger som er knyttet til betalingsmåten.</span><span class="sxs-lookup"><span data-stu-id="0cb8b-112">These payment service settings include changes to the merchant account ID, cloud API key, and various configuration settings that are related to the payment method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0cb8b-113">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="0cb8b-113">Additional resources</span></span>

[<span data-ttu-id="0cb8b-114">Konfigurere en nettkanal</span><span class="sxs-lookup"><span data-stu-id="0cb8b-114">Set up an online channel</span></span>](../channel-setup-online.md)
