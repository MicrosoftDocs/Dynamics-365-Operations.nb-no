---
title: Ordresynkroniseringsfeil relatert til den standard betalingstjenesten
description: Dette emnet gir feilsøkingsveiledning som kan hjelpe deg med å reparere en feil som kan oppstå når en nettordre synkroniseres.
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
ms.openlocfilehash: dd7c400f26b6fc7fbe1d4fec43a52295eb363333
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585459"
---
# <a name="order-synchronization-error-related-to-the-default-payment-service"></a><span data-ttu-id="07eb9-103">Ordresynkroniseringsfeil relatert til den standard betalingstjenesten</span><span class="sxs-lookup"><span data-stu-id="07eb9-103">Order synchronization error related to the default payment service</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="07eb9-104">Dette emnet gir feilsøkingsveiledning som kan hjelpe deg med å reparere en feil som kan oppstå når en nettordre synkroniseres.</span><span class="sxs-lookup"><span data-stu-id="07eb9-104">This topic provides troubleshooting guidance that can help fix an error that might occur when an online order is synced.</span></span>

## <a name="description"></a><span data-ttu-id="07eb9-105">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="07eb9-105">Description</span></span>

<span data-ttu-id="07eb9-106">Når du synkroniserer en nettordre, får du følgende feilmelding: Det må være en standard betalingstjeneste for å behandle kredittkorttransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="07eb9-106">When you sync an online order, you receive the following error message: "There must be a default payment service to process credit card transactions."</span></span>

![Feilen Manglende standard betalingstjeneste](media/default-payment-method-error.jpg)

## <a name="resolution"></a><span data-ttu-id="07eb9-108">Oppløsning</span><span class="sxs-lookup"><span data-stu-id="07eb9-108">Resolution</span></span>

### <a name="confirm-or-set-the-default-payment-service-in-commerce-headquarters"></a><span data-ttu-id="07eb9-109">Bekreft eller angi standard betalingstjeneste i Commerce Headquarters</span><span class="sxs-lookup"><span data-stu-id="07eb9-109">Confirm or set the default payment service in Commerce headquarters</span></span>

<span data-ttu-id="07eb9-110">Hvis du vil bekrefte eller angi standard betalingstjeneste i Commerce Headquarters, gjør du følgende.</span><span class="sxs-lookup"><span data-stu-id="07eb9-110">To confirm or set the default payment service in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="07eb9-111">Gå til **Kunder \> Betalingsoppsett \> Betalingstjenester**.</span><span class="sxs-lookup"><span data-stu-id="07eb9-111">Go to **Accounts receivable \> Payment setup \> Payment services**.</span></span>
1. <span data-ttu-id="07eb9-112">Kontroller at alternativet **Standardbehandler for nye kredittkort** er satt til **Ja** for én betalingstjeneste.</span><span class="sxs-lookup"><span data-stu-id="07eb9-112">Make sure that the **Default processor for new credit cards** option is set to **Yes** for one payment service.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="07eb9-113">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="07eb9-113">Additional resources</span></span>

[<span data-ttu-id="07eb9-114">Kredittkortoppsett, godkjenning og registrering</span><span class="sxs-lookup"><span data-stu-id="07eb9-114">Credit card setup, authorization, and capture</span></span>](https://docs.microsoft.com/dynamics365/finance/accounts-receivable/credit-card-authorizations)
