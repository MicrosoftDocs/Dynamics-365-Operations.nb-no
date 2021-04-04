---
title: Registreringsside for kredittkort viser en feil i betalingsprosessen
description: Dette emnet gir feilsøkingsveiledning som kan hjelpe når delen Betalingsmåte ikke er lastet inn og viser en feilmelding.
author: Reza-Assadi
manager: AnnBe
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
ms.openlocfilehash: f0751fc76e6eb4320f766886b4c1efcb1042e996
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585460"
---
# <a name="credit-card-entry-page-shows-an-error-at-checkout"></a><span data-ttu-id="cb386-103">Registreringsside for kredittkort viser en feil i betalingsprosessen</span><span class="sxs-lookup"><span data-stu-id="cb386-103">Credit card entry page shows an error at checkout</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="cb386-104">Dette emnet gir feilsøkingsveiledning som kan hjelpe når delen **Betalingsmåte** ikke er lastet inn og viser en feilmelding.</span><span class="sxs-lookup"><span data-stu-id="cb386-104">This topic provides troubleshooting guidance that can help when the **Payment method** section isn't loaded and shows an error message.</span></span>

## <a name="description"></a><span data-ttu-id="cb386-105">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="cb386-105">Description</span></span>

<span data-ttu-id="cb386-106">Når du åpner betalingssiden til en nettbutikk, blir ikke delen **Betalingsmåte** lastet og følgende feilmelding vises: "Noe gikk galt.</span><span class="sxs-lookup"><span data-stu-id="cb386-106">When you open the checkout page of an online store, the **Payment method** section isn't loaded, and the following error message is shown: "Something went wrong.</span></span> <span data-ttu-id="cb386-107">Prøv på nytt senere."</span><span class="sxs-lookup"><span data-stu-id="cb386-107">Please try again later."</span></span>

![Feil i betalingsmodul](media/payment-module-error.jpg)

## <a name="resolution"></a><span data-ttu-id="cb386-109">Oppløsning</span><span class="sxs-lookup"><span data-stu-id="cb386-109">Resolution</span></span>

### <a name="wait-for-the-commerce-scale-unit-cache-to-expire"></a><span data-ttu-id="cb386-110">Vent til bufferen for Commerce Scale Unit utløper</span><span class="sxs-lookup"><span data-stu-id="cb386-110">Wait for the Commerce Scale Unit cache to expire</span></span>

<span data-ttu-id="cb386-111">Betalingstjenesteinnstillingene på betalingssiden til den elektroniske butikken hurtigbufres på Commerce Scale Unit, og det kan ta opptil 15 minutter å vises på e-handelsområdet.</span><span class="sxs-lookup"><span data-stu-id="cb386-111">The payment service settings on the online store's checkout page are cached on the Commerce Scale Unit and can take up to 15 minutes to appear on the e-commerce site.</span></span> <span data-ttu-id="cb386-112">Disse innstillingene for betalingstjenesten inkluderer endringer i forretningskonto-IDen, sky-API-nøkkelen og ulike konfigurasjonsinnstillinger som er knyttet til betalingsmåten.</span><span class="sxs-lookup"><span data-stu-id="cb386-112">These payment service settings include changes to the merchant account ID, cloud API key, and various configuration settings that are related to the payment method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cb386-113">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="cb386-113">Additional resources</span></span>

[<span data-ttu-id="cb386-114">Konfigurere en nettkanal</span><span class="sxs-lookup"><span data-stu-id="cb386-114">Set up an online channel</span></span>](../channel-setup-online.md)
