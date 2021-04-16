---
title: Refusjon på en returordre avvises
description: Dette emnet inneholder feilsøkingsveiledning som kan hjelpe deg når en refusjon på en returordre avvises, fordi kredittkortet som brukes til fakturering, er forskjellig fra kortet som ble brukt under den opprinnelige betalingsautorisasjonen.
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
ms.openlocfilehash: 5961e77de1de5dc23454fc1a6e16f8c0b4e7cc6a
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801561"
---
# <a name="refund-on-a-return-order-is-declined"></a><span data-ttu-id="ed5da-103">Refusjon på en returordre avvises</span><span class="sxs-lookup"><span data-stu-id="ed5da-103">Refund on a return order is declined</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ed5da-104">Dette emnet inneholder feilsøkingsveiledning som kan hjelpe deg når en refusjon på en returordre avvises, fordi kredittkortet som brukes til fakturering, er forskjellig fra kortet som ble brukt under den opprinnelige betalingsautorisasjonen.</span><span class="sxs-lookup"><span data-stu-id="ed5da-104">This topic provides troubleshooting guidance that can help when a refund on a return order is declined because the credit card that is used for invoicing differs from the card that was used during the original payment authorization.</span></span>

## <a name="description"></a><span data-ttu-id="ed5da-105">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="ed5da-105">Description</span></span>

<span data-ttu-id="ed5da-106">En tilbakebetaling avvises når kredittkortet som brukes til å fakturere en returordre, er forskjellig fra kortet som ble brukt under den opprinnelige betalingsautorisasjonen.</span><span class="sxs-lookup"><span data-stu-id="ed5da-106">A refund is declined when the credit card that is used to invoice a return order differs from the card that was used during the original payment authorization.</span></span> <span data-ttu-id="ed5da-107">Du får følgende feilmelding: Noen betalinger har ikke riktig status for postering.</span><span class="sxs-lookup"><span data-stu-id="ed5da-107">You receive the following error message: "Some payments are not in the correct status for posting.</span></span> <span data-ttu-id="ed5da-108">Valider statusen for alle betalinger før fakturering på nytt.</span><span class="sxs-lookup"><span data-stu-id="ed5da-108">Please re-validate the status of all payments prior to invoicing."</span></span>

<span data-ttu-id="ed5da-109">Detaljene for betalingsautorisasjon vil inneholde følgende feilmelding: Adyen-gatewayen SendRequest() mislyktes med statusen InternalServerError.22144; Tomt svar returnert fra Adyen. (22001);</span><span class="sxs-lookup"><span data-stu-id="ed5da-109">The payment authorization details will include the following error message: "Adyen gateway SendRequest() failed with status 'InternalServerError'.22144; Empty response returned from Adyen.(22001);"</span></span>

![Feilmeldingen Refusjon på en returordre avvises](media/refund-order-decline.jpg)

## <a name="resolution"></a><span data-ttu-id="ed5da-111">Oppløsning</span><span class="sxs-lookup"><span data-stu-id="ed5da-111">Resolution</span></span>

### <a name="enable-blind-returns-in-adyen"></a><span data-ttu-id="ed5da-112">Aktivere blinde returer i Adyen</span><span class="sxs-lookup"><span data-stu-id="ed5da-112">Enable blind returns in Adyen</span></span>

<span data-ttu-id="ed5da-113">Hvis du vil aktivere blinde returer, følger du trinnene i [Feilsøke problemer med Dynamics 365 Payment Connector for Adyen](adyen-support.md) for å kontakte Adyen-kundestøttegruppen og be om at blinde returer skal aktiveres på Adyen-forretningsenheten.</span><span class="sxs-lookup"><span data-stu-id="ed5da-113">To enable blind returns, follow the steps in [Troubleshoot Dynamics 365 Payment Connector for Adyen issues](adyen-support.md) to contact the Adyen support team and request that blind returns be enabled on your Adyen merchant account.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ed5da-114">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="ed5da-114">Additional resources</span></span>

[<span data-ttu-id="ed5da-115">Dynamics 365 Payment Connector for Adyen</span><span class="sxs-lookup"><span data-stu-id="ed5da-115">Dynamics 365 Payment Connector for Adyen</span></span>](../dev-itpro/adyen-connector.md)

[<span data-ttu-id="ed5da-116">Konfigurere Adyen-betalingskobling for Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="ed5da-116">Set up the Adyen payment connector for Dynamics 365</span></span>](https://docs.adyen.com/plugins/microsoft-dynamics)
