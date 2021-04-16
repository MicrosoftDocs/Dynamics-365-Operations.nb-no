---
title: Skanne strekkoder ved hjelp av et kamera i mobilappen Lagerstyring
description: Dette emnet forklarer hvordan du konfigurerer mobilappen Lagerstyring for å skanne strekkoder med et kamera på en mobil enhet.
author: MarkusFogelberg
ms.date: 01/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSMobileAppField
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2017-01-03
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 2f61f9c45b95b730a7f1743963658ec00abfbb56
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5831224"
---
# <a name="scan-bar-codes-using-a-camera-in-the-warehouse-management-mobile-app"></a><span data-ttu-id="9b49f-103">Skanne strekkoder ved hjelp av et kamera i mobilappen Lagerstyring</span><span class="sxs-lookup"><span data-stu-id="9b49f-103">Scan bar codes using a camera in the Warehouse Management mobile app</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9b49f-104">Dette emnet forklarer hvordan du konfigurerer mobilappen Lagerstyring for å skanne strekkoder med et kamera på en mobil enhet.</span><span class="sxs-lookup"><span data-stu-id="9b49f-104">This topic explains how to set up the Warehouse Management mobile app to scan bar codes using a camera on a mobile device.</span></span>

## <a name="setup"></a><span data-ttu-id="9b49f-105">Installasjon</span><span class="sxs-lookup"><span data-stu-id="9b49f-105">Setup</span></span>

<span data-ttu-id="9b49f-106">Du kan velge om kameraet skal brukes til å skanne strekkoder, i innstillingene for visning i mobilappen Lagerstyring.</span><span class="sxs-lookup"><span data-stu-id="9b49f-106">In the display settings of the Warehouse Management mobile app, you can select if the camera should be used for bar code scanning.</span></span> <span data-ttu-id="9b49f-107">Hvis du aktiverer **Bruk kameraet som skanner**, kan du bruke kameraet på alle inndatafelt som har den foretrukne inndatamodusen satt til **Skanning**.</span><span class="sxs-lookup"><span data-stu-id="9b49f-107">If you enable **Use the camera as scanner**, you can use the camera on every input field that has the preferred input mode set to **Scanning**.</span></span>

<span data-ttu-id="9b49f-108">For å kontrollere om inndatafeltet kan skannes går du til siden **Navn på lagerappfelt** og setter **Foretrukket inndatamodus** til **Skanning**.</span><span class="sxs-lookup"><span data-stu-id="9b49f-108">To control whether an input field should be scannable, on the **Warehouse app field names** page, set **Preferred input mode** to **Scanning**.</span></span> <span data-ttu-id="9b49f-109">Når dette alternativet er valgt, kan kameraet brukes til å skanne i mobilappen Lagerstyring.</span><span class="sxs-lookup"><span data-stu-id="9b49f-109">When this option is selected, a camera can be used for scanning in the Warehouse Management mobile app.</span></span> <span data-ttu-id="9b49f-110">For mer informasjon, se [Konfigur felter for mobilappen Lagerstyring](configure-app-field-names-priorities-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="9b49f-110">For more information, see [Configure fields for the Warehouse Management mobile app](configure-app-field-names-priorities-warehouse.md).</span></span>

## <a name="supported-bar-code-formats"></a><span data-ttu-id="9b49f-111">Støttede strekkodeformater</span><span class="sxs-lookup"><span data-stu-id="9b49f-111">Supported bar code formats</span></span>

<span data-ttu-id="9b49f-112">De vanligste strekkodeformatene støttes, inkludert Code 128, Code 39, Code 93, EAN-8, EAN-13, UPC-E, UPC-A og QR-koder.</span><span class="sxs-lookup"><span data-stu-id="9b49f-112">The most common bar code formats are supported, including Code 128, Code 39, Code 93, EAN-8, EAN-13, UPC-E, UPC-A, and QR codes.</span></span>

## <a name="navigation"></a><span data-ttu-id="9b49f-113">Navigering</span><span class="sxs-lookup"><span data-stu-id="9b49f-113">Navigation</span></span>

<span data-ttu-id="9b49f-114">Kamerasiden startes på hver side der inndatafeltet har **Foretrukket inndatamodus** satt til *Skanning*. Når du er på kamerasiden, bruker du følgende alternativer for å navigere:</span><span class="sxs-lookup"><span data-stu-id="9b49f-114">The camera page will be initiated on each page where the input field has its **Preferred input mode** set to *Scanning*, when you are on the camera page use the following options to navigate:</span></span>

- <span data-ttu-id="9b49f-115">Klikk på tilbakeknappen for å gå tilbake til siden **Oppgave og detaljer**.</span><span class="sxs-lookup"><span data-stu-id="9b49f-115">Select the back button to go back to the **Task and details** page.</span></span>
- <span data-ttu-id="9b49f-116">Klikk på blyanten på siden **Oppgave og detaljer** for å gå til siden der du kan skrive inn manuelt.</span><span class="sxs-lookup"><span data-stu-id="9b49f-116">Select the pencil on the **Task and details** page to go to the page where you can type input manually.</span></span>
- <span data-ttu-id="9b49f-117">Klikk på kameraet på siden **Oppgave og detaljer** for å gå tilbake til kamerasiden.</span><span class="sxs-lookup"><span data-stu-id="9b49f-117">Select the camera on the **Task and details** page to go back to the camera page.</span></span>

<span data-ttu-id="9b49f-118">På kamerasiden, når du velger Kamera-knappen, vises den nedtonet ved forsøk på å identifisere en strekkode.</span><span class="sxs-lookup"><span data-stu-id="9b49f-118">On the camera page, when you select the camera button, it will appear dimmed while trying to identify a bar code.</span></span> <span data-ttu-id="9b49f-119">Hvis en strekkode ikke identifiseres innen 5 sekunder, deaktiveres prosessen og Kamera-knappen blir tilgjengelig igjen.</span><span class="sxs-lookup"><span data-stu-id="9b49f-119">If a bar code is not identified within 5 seconds, the process will time out and the camera button will become available again.</span></span> <span data-ttu-id="9b49f-120">Du kan deretter prøve å skanne en strekkode på nytt.</span><span class="sxs-lookup"><span data-stu-id="9b49f-120">You will then be able to try to scan a bar code again.</span></span>

<span data-ttu-id="9b49f-121">Når du holder kameraet på en strekkode, må du justere strekkoden innenfor hakeparentesene for best resultat.</span><span class="sxs-lookup"><span data-stu-id="9b49f-121">When you aim the camera at a bar code, keep the bar code aligned within the brackets for best result.</span></span> <span data-ttu-id="9b49f-122">Når en strekkode er skannet, blir resultatet behandlet, og du føres til neste trinn.</span><span class="sxs-lookup"><span data-stu-id="9b49f-122">When a bar code is scanned successfully, the result will be processed, and you will be taken to the next step.</span></span> <span data-ttu-id="9b49f-123">Hvis det neste trinnet inneholder et annet inndatafelt med den foretrukne inndatamodusen satt til Skanning, startes kamerasiden på nytt.</span><span class="sxs-lookup"><span data-stu-id="9b49f-123">If the next step contains another input field with the preferred input mode set to Scanning, the camera page will start again.</span></span> <span data-ttu-id="9b49f-124">Hvis det neste trinnet ikke er et skannefelt, startes ikke kamerasiden.</span><span class="sxs-lookup"><span data-stu-id="9b49f-124">If the next step is not a scanning field, then the camera page will not be initiated.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]