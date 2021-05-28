---
title: Ordresynkroniseringsfeil relatert til den standard betalingstjenesten
description: Dette emnet gir feilsøkingsveiledning som kan hjelpe deg med å reparere en feil som kan oppstå når en nettordre synkroniseres.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
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
ms.openlocfilehash: fa174bbb257379f6ce906dd21180bbcb19f8bc3f
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021133"
---
# <a name="order-synchronization-error-related-to-the-default-payment-service"></a><span data-ttu-id="37411-103">Ordresynkroniseringsfeil relatert til den standard betalingstjenesten</span><span class="sxs-lookup"><span data-stu-id="37411-103">Order synchronization error related to the default payment service</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="37411-104">Dette emnet gir feilsøkingsveiledning som kan hjelpe deg med å reparere en feil som kan oppstå når en nettordre synkroniseres.</span><span class="sxs-lookup"><span data-stu-id="37411-104">This topic provides troubleshooting guidance that can help fix an error that might occur when an online order is synced.</span></span>

## <a name="description"></a><span data-ttu-id="37411-105">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="37411-105">Description</span></span>

<span data-ttu-id="37411-106">Når du synkroniserer en nettordre, får du følgende feilmelding: Det må være en standard betalingstjeneste for å behandle kredittkorttransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="37411-106">When you sync an online order, you receive the following error message: "There must be a default payment service to process credit card transactions."</span></span>

![Feilen Manglende standard betalingstjeneste](media/default-payment-method-error.jpg)

## <a name="resolution"></a><span data-ttu-id="37411-108">Oppløsning</span><span class="sxs-lookup"><span data-stu-id="37411-108">Resolution</span></span>

### <a name="confirm-or-set-the-default-payment-service-in-commerce-headquarters"></a><span data-ttu-id="37411-109">Bekreft eller angi standard betalingstjeneste i Commerce Headquarters</span><span class="sxs-lookup"><span data-stu-id="37411-109">Confirm or set the default payment service in Commerce headquarters</span></span>

<span data-ttu-id="37411-110">Hvis du vil bekrefte eller angi standard betalingstjeneste i Commerce Headquarters, gjør du følgende.</span><span class="sxs-lookup"><span data-stu-id="37411-110">To confirm or set the default payment service in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="37411-111">Gå til **Kunder \> Betalingsoppsett \> Betalingstjenester**.</span><span class="sxs-lookup"><span data-stu-id="37411-111">Go to **Accounts receivable \> Payment setup \> Payment services**.</span></span>
1. <span data-ttu-id="37411-112">Kontroller at alternativet **Standardbehandler for nye kredittkort** er satt til **Ja** for én betalingstjeneste.</span><span class="sxs-lookup"><span data-stu-id="37411-112">Make sure that the **Default processor for new credit cards** option is set to **Yes** for one payment service.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="37411-113">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="37411-113">Additional resources</span></span>

[<span data-ttu-id="37411-114">Kredittkortoppsett, godkjenning og registrering</span><span class="sxs-lookup"><span data-stu-id="37411-114">Credit card setup, authorization, and capture</span></span>](../../finance/accounts-receivable/credit-card-authorizations.md)