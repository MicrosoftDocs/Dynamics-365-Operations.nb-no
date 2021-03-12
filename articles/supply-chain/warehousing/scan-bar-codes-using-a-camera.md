---
title: Skanne strekkoder ved hjelp av et kamera i lagerappen
description: Dette emnet forklarer hvordan du konfigurerer lagerappen for å skanne strekkoder med et kamera på en mobil enhet.
author: MarkusFogelberg
manager: tfehr
ms.date: 01/03/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSMobileAppField
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2017-01-03
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 71ec15b2568eefd8bea99e64c258a65461a7ad95
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4965649"
---
# <a name="scan-bar-codes-using-a-camera-in-the-warehouse-app"></a><span data-ttu-id="30e1e-103">Skanne strekkoder ved hjelp av et kamera i lagerappen</span><span class="sxs-lookup"><span data-stu-id="30e1e-103">Scan bar codes using a camera in the warehouse app</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="30e1e-104">Dette emnet forklarer hvordan du konfigurerer lagerappen for å skanne strekkoder med et kamera på en mobil enhet.</span><span class="sxs-lookup"><span data-stu-id="30e1e-104">This topic explains how to set up the warehouse app to scan bar codes using a camera on a mobile device.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="30e1e-105">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="30e1e-105">Prerequisites</span></span>
<span data-ttu-id="30e1e-106">Hvis du vil bruke denne funksjonen, må du ha versjon 1.2.0.0 av lagerappen installert, og enheten må ha et kamera.</span><span class="sxs-lookup"><span data-stu-id="30e1e-106">To use this feature, you need to have version 1.2.0.0 of the warehouse app installed, and your device must have a camera.</span></span> <span data-ttu-id="30e1e-107">Når du åpner appen når du har oppdatert, blir du bedt om å tillate at appen kan bruke kameraet.</span><span class="sxs-lookup"><span data-stu-id="30e1e-107">When you open the app after updating, you will be prompted to allow the app to use the camera.</span></span> <span data-ttu-id="30e1e-108">Hvis enheten ikke har kamera, vises ingen ledetekst, og du kan ikke bruke kamera som skanner.</span><span class="sxs-lookup"><span data-stu-id="30e1e-108">If your device doesn’t have a camera, no prompt will be shown, and you will not be able to use a camera as a scanner.</span></span> 

## <a name="setup"></a><span data-ttu-id="30e1e-109">Installasjon</span><span class="sxs-lookup"><span data-stu-id="30e1e-109">Setup</span></span>
<span data-ttu-id="30e1e-110">Du kan velge om kameraet skal brukes til å skanne strekkoder, i innstillingene for visning i lagerappen.</span><span class="sxs-lookup"><span data-stu-id="30e1e-110">In the Display settings of the warehouse application, you can select if the camera should be used for bar code scanning.</span></span> <span data-ttu-id="30e1e-111">Hvis du aktiverer **Bruk kameraet som skanner**, kan du bruke kameraet på alle inndatafelt som har den foretrukne inndatamodusen satt til **Skanning**.</span><span class="sxs-lookup"><span data-stu-id="30e1e-111">If you enable **Use the camera as scanner**, you can use the camera on every input field that has the preferred input mode set to **Scanning**.</span></span> 

<span data-ttu-id="30e1e-112">For å kontrollere om inndatafeltet kan skannes går du til siden **Navn på lagerappfelt** og setter **Foretrukket inndatamodus** til **Skanning**.</span><span class="sxs-lookup"><span data-stu-id="30e1e-112">To control whether an input field should be scannable, on the **Warehouse app field names** page, set **Preferred input mode** to **Scanning**.</span></span> <span data-ttu-id="30e1e-113">Når dette alternativet er valgt, kan kameraet brukes til å skanne i lagerappen.</span><span class="sxs-lookup"><span data-stu-id="30e1e-113">When this option is selected, a camera can be used for scanning in the warehouse app.</span></span> <span data-ttu-id="30e1e-114">Hvis du vil ha informasjon om hvordan du konfigurerer appfeltnavn i Warehousing, kan du se [Konfigurere appfeltnavn i lagerappen](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/warehousing/configure-app-field-names-priorities-warehouse).</span><span class="sxs-lookup"><span data-stu-id="30e1e-114">For information about how to configure app field names in Warehousing, see [Configure app field names in warehouse app](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/warehousing/configure-app-field-names-priorities-warehouse).</span></span>

## <a name="supported-bar-code-formats"></a><span data-ttu-id="30e1e-115">Støttede strekkodeformater</span><span class="sxs-lookup"><span data-stu-id="30e1e-115">Supported bar code formats</span></span>
<span data-ttu-id="30e1e-116">De vanligste strekkodeformatene støttes, inkludert Code 128, Code 39, Code 93, EAN-8, EAN-13, UPC-E, UPC-A og QR-koder.</span><span class="sxs-lookup"><span data-stu-id="30e1e-116">The most common bar code formats are supported, including Code 128, Code 39, Code 93, EAN-8, EAN-13, UPC-E, UPC-A, and QR codes.</span></span> 

## <a name="navigation"></a><span data-ttu-id="30e1e-117">Navigering</span><span class="sxs-lookup"><span data-stu-id="30e1e-117">Navigation</span></span>
<span data-ttu-id="30e1e-118">Kamerasiden startes på hver side der inndatafeltet har den foretrukne inndatamodusen satt til Skanning. Når du er på kamerasiden, bruker du følgende alternativer for å navigere:</span><span class="sxs-lookup"><span data-stu-id="30e1e-118">The camera page will be initiated on each page where the input field has the preferred input mode set to Scanning, when you are on the Camera page use the following options to navigate:</span></span>
- <span data-ttu-id="30e1e-119">Klikk på tilbakeknappen for å gå tilbake til oppgave- og detaljsiden.</span><span class="sxs-lookup"><span data-stu-id="30e1e-119">Click the back button to go back to the Task and details page.</span></span> 
- <span data-ttu-id="30e1e-120">Klikk blyanten på oppgave- og detaljsiden for å gå til siden der du kan skrive inn manuelt.</span><span class="sxs-lookup"><span data-stu-id="30e1e-120">Click the pencil on the Task and details page to go to the page where you can type input manually.</span></span>
- <span data-ttu-id="30e1e-121">Klikk kameraet på oppgave- og detaljsiden for å gå tilbake til kamerasiden.</span><span class="sxs-lookup"><span data-stu-id="30e1e-121">Click the camera on the Task and details page to go back to the Camera page.</span></span> 

| <span data-ttu-id="30e1e-122">Oppgave- og detaljsiden</span><span class="sxs-lookup"><span data-stu-id="30e1e-122">Task and details page</span></span> | <span data-ttu-id="30e1e-123">Kamerasiden</span><span class="sxs-lookup"><span data-stu-id="30e1e-123">Camera page</span></span> | 
| :---------------------: | :--------------------: |
| ![Detaljside med oppgaveeksempel på kameraskanning](./media/camera-scanning-example-task-detail-page50.png)          | ![Mindre kameraside med eksempel på kameraskanning](./media/camera-scanning-example-camera-page50.png)          |

<span data-ttu-id="30e1e-126">På kamerasiden, når du klikker Kamera-knappen, vises den nedtonet ved forsøk på å identifisere en strekkode.</span><span class="sxs-lookup"><span data-stu-id="30e1e-126">On the camera page, when you click the Camera button, it will appear dimmed while trying to identify a bar code.</span></span> <span data-ttu-id="30e1e-127">Hvis en strekkode ikke identifiseres innen 5 sekunder, deaktiveres prosessen og Kamera-knappen blir tilgjengelig igjen.</span><span class="sxs-lookup"><span data-stu-id="30e1e-127">If a bar code is not identified within 5 seconds, the process will time out and the Camera button will become available again.</span></span> <span data-ttu-id="30e1e-128">Du kan deretter prøve å skanne en strekkode på nytt.</span><span class="sxs-lookup"><span data-stu-id="30e1e-128">You will then be able to try to scan a bar code again.</span></span>

<span data-ttu-id="30e1e-129">Når du holder kameraet på en strekkode, må du justere strekkoden innenfor hakeparentesene for best resultat.</span><span class="sxs-lookup"><span data-stu-id="30e1e-129">When you aim the camera at a bar code, keep the bar code aligned within the brackets for best result.</span></span> <span data-ttu-id="30e1e-130">Når en strekkode er skannet, blir resultatet behandlet, og du føres til neste trinn.</span><span class="sxs-lookup"><span data-stu-id="30e1e-130">When a bar code is scanned successfully, the result will be processed, and you will be taken to the next step.</span></span> <span data-ttu-id="30e1e-131">Hvis det neste trinnet inneholder et annet inndatafelt med den foretrukne inndatamodusen satt til Skanning, startes kamerasiden på nytt.</span><span class="sxs-lookup"><span data-stu-id="30e1e-131">If the next step contains another input field with the preferred input mode set to Scanning, the camera page will start again.</span></span> <span data-ttu-id="30e1e-132">Hvis det neste trinnet ikke er et skannefelt, startes ikke kamerasiden.</span><span class="sxs-lookup"><span data-stu-id="30e1e-132">If the next step is not a scanning field, then the camera page will not be initiated.</span></span>

