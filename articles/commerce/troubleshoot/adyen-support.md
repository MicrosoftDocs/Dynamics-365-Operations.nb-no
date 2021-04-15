---
title: Feilsøke problemer med Dynamics 365 Payment Connector for Adyen
description: Dette emnet gir feilsøkingsveiledning som kan hjelpe deg med å få støtte når du har problemer med Microsoft Dynamics 365 Payment Connector for Adyen.
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
ms.openlocfilehash: c779997d530d60f945bee19ee09bdabbff121fa6
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801825"
---
# <a name="troubleshoot-dynamics-365-payment-connector-for-adyen-issues"></a><span data-ttu-id="d9291-103">Feilsøke problemer med Dynamics 365 Payment Connector for Adyen</span><span class="sxs-lookup"><span data-stu-id="d9291-103">Troubleshoot Dynamics 365 Payment Connector for Adyen issues</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d9291-104">Dette emnet gir feilsøkingsveiledning som kan hjelpe deg med å få støtte når du har problemer med Microsoft Dynamics 365 Payment Connector for Adyen.</span><span class="sxs-lookup"><span data-stu-id="d9291-104">This topic provides troubleshooting guidance that can help you get support when you have issues with the Microsoft Dynamics 365 Payment Connector for Adyen.</span></span>

## <a name="description"></a><span data-ttu-id="d9291-105">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="d9291-105">Description</span></span>

<span data-ttu-id="d9291-106">Du har problemer med Dynamics 365 Payment Connector for Adyen på følgende områder, og du trenger støtte fra Adyen-teamet:</span><span class="sxs-lookup"><span data-stu-id="d9291-106">You have issues with the Dynamics 365 Payment Connector for Adyen in the following areas, and you require support from the Adyen team:</span></span>

- <span data-ttu-id="d9291-107">Konfigurasjon av salgssted (POS), moderne salgssted for detaljhandel (MPOS), telefonsenter eller Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="d9291-107">Configuration of Point of sale (POS), Modern point of sale (MPOS), call center, or Dynamics 365 Commerce</span></span>
- <span data-ttu-id="d9291-108">Referansenummeret til Adyen-betalingstjenesten (PSP) (for eksempel hvis du har spørsmål om avvisninger, inkludert \[MKE\]-avslag for manuell nøkkelregistrering)</span><span class="sxs-lookup"><span data-stu-id="d9291-108">The Adyen payment service provider (PSP) reference number (for example, if you have questions about refusals, including manual key entry \[MKE\] refusals)</span></span>
- <span data-ttu-id="d9291-109">Alt som ikke fungerer i test- eller forretningsmiljøer</span><span class="sxs-lookup"><span data-stu-id="d9291-109">Anything that isn't working in test or live merchant environments</span></span>

## <a name="resolution"></a><span data-ttu-id="d9291-110">Oppløsning</span><span class="sxs-lookup"><span data-stu-id="d9291-110">Resolution</span></span>

<span data-ttu-id="d9291-111">Bruk e-postmalen nedenfor til å starte støtteprosessen med Adyen-teamet.</span><span class="sxs-lookup"><span data-stu-id="d9291-111">Use the following email template to start the support process with the Adyen team.</span></span> <span data-ttu-id="d9291-112">Hvis du vil fremskynde feilsøking, må du sørge for at e-posten inneholder alle de nødvendige detaljene.</span><span class="sxs-lookup"><span data-stu-id="d9291-112">To expedite troubleshooting, make sure that the email contains all the required details.</span></span>

| <span data-ttu-id="d9291-113">Felt</span><span class="sxs-lookup"><span data-stu-id="d9291-113">Field</span></span>        | <span data-ttu-id="d9291-114">Verdi</span><span class="sxs-lookup"><span data-stu-id="d9291-114">Value</span></span> |
|--------------|-------|
| <span data-ttu-id="d9291-115">Til</span><span class="sxs-lookup"><span data-stu-id="d9291-115">To</span></span>           | `support@adyen.com` |
| <span data-ttu-id="d9291-116">Kopi</span><span class="sxs-lookup"><span data-stu-id="d9291-116">Cc</span></span>           | |
| <span data-ttu-id="d9291-117">Emnelinje</span><span class="sxs-lookup"><span data-stu-id="d9291-117">Subject line</span></span> | <span data-ttu-id="d9291-118">Kundestøtteforespørsel for Microsoft Dynamics</span><span class="sxs-lookup"><span data-stu-id="d9291-118">Microsoft Dynamics Support Request</span></span> |
| <span data-ttu-id="d9291-119">Meldingstekst</span><span class="sxs-lookup"><span data-stu-id="d9291-119">Body</span></span>         | <p><span data-ttu-id="d9291-120">Hei, Kundestøtte,</span><span class="sxs-lookup"><span data-stu-id="d9291-120">Hi Support,</span></span></p><p><span data-ttu-id="d9291-121">Formidle støtte for følgende problem:</span><span class="sxs-lookup"><span data-stu-id="d9291-121">Please provide support for the following issue:</span></span></p><ul><li><span data-ttu-id="d9291-122">Forhandlerkonto</span><span class="sxs-lookup"><span data-stu-id="d9291-122">Merchant account</span></span></li><li><span data-ttu-id="d9291-123">Miljø (test/prod)</span><span class="sxs-lookup"><span data-stu-id="d9291-123">Environment (Test/Prod)</span></span></li><li><span data-ttu-id="d9291-124">Kanal (salgssted/telefonsenter/Commerce e-commerce)</span><span class="sxs-lookup"><span data-stu-id="d9291-124">Channel (POS/call center/Commerce e-commerce)</span></span></li><li><span data-ttu-id="d9291-125">PSP-referansenummeret, hvis avgangen gjelder en bestemt transaksjon (Du kan finne PSP-referansenummeret på mottaket, i Adyen-kundeområdet eller på transaksjonsmenyen på POS-terminalen.)</span><span class="sxs-lookup"><span data-stu-id="d9291-125">PSP reference number, if the issue involved a specific transaction (You can find the PSP reference number on the receipt, in the Adyen Customer Area, or on the transactions menu on the POS terminal.)</span></span></li><li><span data-ttu-id="d9291-126">Skjermbilde eller bilde av feilmeldingen, hvis det er aktuelt</span><span class="sxs-lookup"><span data-stu-id="d9291-126">Screenshot or photo of the error message, if applicable</span></span></li><li><span data-ttu-id="d9291-127">Hendelseslistelogger (i .txt-format)</span><span class="sxs-lookup"><span data-stu-id="d9291-127">Event Viewer logs (in .txt format)</span></span></li><li><span data-ttu-id="d9291-128">Beskrivelse av problemet og feilsøkingstrinnene du har forsøkt</span><span class="sxs-lookup"><span data-stu-id="d9291-128">Description of the issue and troubleshooting steps that you've tried</span></span></li></ul> |

## <a name="additional-resources"></a><span data-ttu-id="d9291-129">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="d9291-129">Additional resources</span></span>

[<span data-ttu-id="d9291-130">Godta betalinger med Adyen-kontakten for Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="d9291-130">Accept payments with the Adyen connector for Dynamics 365 Commerce</span></span>](https://www.adyen.com/partners/dynamics-365-commerce)

[<span data-ttu-id="d9291-131">Dynamics 365 Payment Connector for Adyen</span><span class="sxs-lookup"><span data-stu-id="d9291-131">Dynamics 365 Payment Connector for Adyen</span></span>](../dev-itpro/adyen-connector.md)

[<span data-ttu-id="d9291-132">Konfigurere Adyen-betalingskobling for Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="d9291-132">Set up the Adyen payment connector for Dynamics 365</span></span>](https://docs.adyen.com/plugins/microsoft-dynamics)
