---
title: "Skanne strekkoder ved hjelp av et kamera i Dynamics 365 for Finance and Operations – Warehousing"
description: "Dette emnet forklarer hvordan du konfigurerer Dynamics 365 for Finance and Operations – Warehousing for å skanne strekkoder med et kamera på en mobil enhet."
author: MarkusFogelberg
manager: AnnBe
ms.date: 01/03/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSMobileAppField
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2017-01-03
ms.dyn365.ops.version: AX 8.0.0
ms.translationtype: HT
ms.sourcegitcommit: ffbd853c15e479fc4350a19121f2aebcedda9854
ms.openlocfilehash: 31b9d421f3fd5378f26faeee3a83b66861ef5008
ms.contentlocale: nb-no
ms.lasthandoff: 03/02/2018

---

# <a name="scan-bar-codes-using-a-camera-in-dynamics-365-for-finance-and-operations--warehousing"></a><span data-ttu-id="53919-103">Skanne strekkoder ved hjelp av et kamera i Dynamics 365 for Finance and Operations – Warehousing</span><span class="sxs-lookup"><span data-stu-id="53919-103">Scan bar codes using a camera in Dynamics 365 for Finance and Operations – Warehousing</span></span>

<span data-ttu-id="53919-104">Dette emnet forklarer hvordan du konfigurerer Dynamics 365 for Finance and Operations – Warehousing for å skanne strekkoder med et kamera på en mobil enhet.</span><span class="sxs-lookup"><span data-stu-id="53919-104">This topic explains how to set up Dynamics 365 for Finance and Operations – Warehousing to scan bar codes using a camera on a mobile device.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="53919-105">Nødvendig programvare</span><span class="sxs-lookup"><span data-stu-id="53919-105">Prerequisites</span></span>
<span data-ttu-id="53919-106">Hvis du vil bruke denne funksjonen, må du ha versjon 1.2.0.0 av Warehousing installert, og enheten må ha et kamera.</span><span class="sxs-lookup"><span data-stu-id="53919-106">To use this feature, you need to have version 1.2.0.0 of Warehousing installed, and your device must have a camera.</span></span> <span data-ttu-id="53919-107">Når du åpner appen når du har oppdatert, blir du bedt om å tillate at Dynamics 365 for Finance and Operations – Warehousing-programmet kan bruke kameraet.</span><span class="sxs-lookup"><span data-stu-id="53919-107">When you open the app after updating, you will be prompted to allow the Dynamics 365 for Finance and Operations – Warehousing application to use the camera.</span></span> <span data-ttu-id="53919-108">Hvis enheten ikke har kamera, vises ingen ledetekst, og du kan ikke bruke kamera som skanner.</span><span class="sxs-lookup"><span data-stu-id="53919-108">If your device doesn’t have a camera, no prompt will be shown, and you will not be able to use a camera as a scanner.</span></span> 

## <a name="setup"></a><span data-ttu-id="53919-109">Definere</span><span class="sxs-lookup"><span data-stu-id="53919-109">Setup</span></span>
<span data-ttu-id="53919-110">Du kan velge om kameraet skal brukes til å skanne strekkoder, i innstillingene for visning i Warehousing-programmet.</span><span class="sxs-lookup"><span data-stu-id="53919-110">In the Display settings of the Warehousing application, you can select if the camera should be used for bar code scanning.</span></span> <span data-ttu-id="53919-111">Hvis du aktiverer **Bruk kameraet som skanner**, kan du bruke kameraet på alle inndatafelt som har den foretrukne inndatamodusen satt til **Skanning**.</span><span class="sxs-lookup"><span data-stu-id="53919-111">If you enable **Use the camera as scanner**, you can use the camera on every input field that has the preferred input mode set to **Scanning**.</span></span> 

<span data-ttu-id="53919-112">For å kontrollere om inndatafeltet kan skannes, går du til siden **Navn på lagerappfelt** i Dynamics 365 for Finance and Operations og setter **Foretrukket inndatamodus** til **Skanning**.</span><span class="sxs-lookup"><span data-stu-id="53919-112">To control whether an input field should be scannable, on the **Warehouse app field names** page in Dynamics 365 for Finance and Operations, set **Preferred input mode** to **Scanning**.</span></span> <span data-ttu-id="53919-113">Når dette alternativet er valgt, kan kameraet brukes til å skanne i programmet Warehousing.</span><span class="sxs-lookup"><span data-stu-id="53919-113">When this option is selected, a camera can be used for scanning in the Warehousing app.</span></span> <span data-ttu-id="53919-114">Hvis du vil ha informasjon om hvordan du konfigurerer appfeltnavn i Warehousing, kan du se [Konfigurere appfeltnavn i Warehousing-appen](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/warehousing/configure-app-field-names-priorities-warehouse).</span><span class="sxs-lookup"><span data-stu-id="53919-114">For information about how to configure app field names in Warehousing, see [Configure app field names in Warehousing app](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/warehousing/configure-app-field-names-priorities-warehouse).</span></span>

## <a name="supported-bar-code-formats"></a><span data-ttu-id="53919-115">Støttede strekkodeformater</span><span class="sxs-lookup"><span data-stu-id="53919-115">Supported bar code formats</span></span>
<span data-ttu-id="53919-116">De vanligste strekkodeformatene støttes, inkludert Code 128, Code 39, Code 93, EAN-8, EAN-13, UPC-E, UPC-A og QR-koder.</span><span class="sxs-lookup"><span data-stu-id="53919-116">The most common bar code formats are supported, including Code 128, Code 39, Code 93, EAN-8, EAN-13, UPC-E, UPC-A, and QR codes.</span></span> 

## <a name="navigation"></a><span data-ttu-id="53919-117">Navigering</span><span class="sxs-lookup"><span data-stu-id="53919-117">Navigation</span></span>
<span data-ttu-id="53919-118">Kamerasiden startes på hver side der inndatafeltet har den foretrukne inndatamodusen satt til Skanning. Når du er på kamerasiden, bruker du følgende alternativer for å navigere:</span><span class="sxs-lookup"><span data-stu-id="53919-118">The camera page will be initiated on each page where the input field has the preferred input mode set to Scanning, when you are on the Camera page use the following options to navigate:</span></span>
- <span data-ttu-id="53919-119">Klikk tilbakeknappen for å gå tilbake til oppgave- og detaljsiden.</span><span class="sxs-lookup"><span data-stu-id="53919-119">Click the back button to go back to the Task and details page.</span></span> 
- <span data-ttu-id="53919-120">Klikk blyanten på oppgave- og detaljsiden for å gå til siden der du kan skrive inn manuelt.</span><span class="sxs-lookup"><span data-stu-id="53919-120">Click the pencil on the Task and details page to go to the page where you can type input manually.</span></span>
- <span data-ttu-id="53919-121">Klikk kameraet på oppgave- og detaljsiden for å gå tilbake til kamerasiden.</span><span class="sxs-lookup"><span data-stu-id="53919-121">Click the camera on the Task and details page to go back to the Camera page.</span></span> 

| <span data-ttu-id="53919-122">Oppgave- og detaljsiden</span><span class="sxs-lookup"><span data-stu-id="53919-122">Task and details page</span></span> | <span data-ttu-id="53919-123">Kamerasiden</span><span class="sxs-lookup"><span data-stu-id="53919-123">Camera page</span></span> | 
| --------------------- | -------------------- |
| ![camera-scanning-example-task-detail-page](media/camera-scanning-example-task-detail-page.png)          | ![camera-scanning-example-camera-page](media/camera-scanning-example-camera-page.png)          |

<span data-ttu-id="53919-126">På kamerasiden, når du klikker Kamera-knappen, vises den nedtonet ved forsøk på å identifisere en strekkode.</span><span class="sxs-lookup"><span data-stu-id="53919-126">On the camera page, when you click the Camera button, it will appear dimmed while trying to identify a bar code.</span></span> <span data-ttu-id="53919-127">Hvis en strekkode ikke identifiseres innen 5 sekunder, deaktiveres prosessen og Kamera-knappen blir tilgjengelig igjen.</span><span class="sxs-lookup"><span data-stu-id="53919-127">If a bar code is not identified within 5 seconds, the process will time out and the Camera button will become available again.</span></span> <span data-ttu-id="53919-128">Du kan deretter prøve å skanne en strekkode på nytt.</span><span class="sxs-lookup"><span data-stu-id="53919-128">You will then be able to try to scan a bar code again.</span></span>

<span data-ttu-id="53919-129">Når du holder kameraet på en strekkode, må du justere strekkoden innenfor hakeparentesene for best resultat.</span><span class="sxs-lookup"><span data-stu-id="53919-129">When you aim the camera at a bar code, keep the bar code aligned within the brackets for best result.</span></span> <span data-ttu-id="53919-130">Når en strekkode er skannet, blir resultatet behandlet, og du føres til neste trinn.</span><span class="sxs-lookup"><span data-stu-id="53919-130">When a bar code is scanned successfully, the result will be processed, and you will be taken to the next step.</span></span> <span data-ttu-id="53919-131">Hvis det neste trinnet inneholder et annet inndatafelt med den foretrukne inndatamodusen satt til Skanning, startes kamerasiden på nytt.</span><span class="sxs-lookup"><span data-stu-id="53919-131">If the next step contains another input field with the preferred input mode set to Scanning, the camera page will start again.</span></span> <span data-ttu-id="53919-132">Hvis det neste trinnet ikke er et skannefelt, startes ikke kamerasiden.</span><span class="sxs-lookup"><span data-stu-id="53919-132">If the next step is not a scanning field, then the camera page will not be initiated.</span></span>


