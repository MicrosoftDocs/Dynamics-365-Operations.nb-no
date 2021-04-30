---
title: Legge til en QR-kode eller strekkode i e-postmeldinger for transaksjon og kvittering
description: Dette emnet beskriver hvordan du setter inn QR-koder og strekkoder som representerer ordre-IDer, i e-postmeldinger for transaksjoner og kvitteringer i Microsoft Dynamics 365 Commerce.
author: bicyclingfool
ms.date: 03/04/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Commerce, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2021-02-16
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 791b244c867ea4263f08250abf220a1b75784cad
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/16/2021
ms.locfileid: "5907869"
---
# <a name="add-a-qr-code-or-bar-code-to-transactional-and-receipt-emails"></a><span data-ttu-id="b93f7-103">Legge til en QR-kode eller strekkode i e-postmeldinger for transaksjon og kvittering</span><span class="sxs-lookup"><span data-stu-id="b93f7-103">Add a QR code or bar code to transactional and receipt emails</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b93f7-104">Dette emnet beskriver hvordan du setter inn QR-koder og strekkoder som representerer ordre-IDer, i e-postmeldinger for transaksjoner og kvitteringer i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b93f7-104">This topic explains how to insert QR codes and bar codes that represent order IDs into transactional and receipt emails in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="b93f7-105">Du kan lett ta med QR-koder og strekkoder i transaksjons-e-postmeldinger for å gjøre ordreoppslagsprosessen raskere i et detaljhandelsmiljø.</span><span class="sxs-lookup"><span data-stu-id="b93f7-105">You can easily include QR codes and bar codes in transactional emails to help speed up the order lookup process in a retail environment.</span></span> <span data-ttu-id="b93f7-106">Hvis du vil sette inn QR-koder og strekkoder i e-postmeldinger, bruker du en HTML-kode **\<img\>** som ber om en QR-kode eller strekkodebilde fra en genererings- og gjengivelsestjeneste.</span><span class="sxs-lookup"><span data-stu-id="b93f7-106">To insert QR codes and bar codes into emails, you use an HTML **\<img\>** tag that requests a QR code or bar code image from a generation and rendering service.</span></span> <span data-ttu-id="b93f7-107">Microsoft tilbyr ikke denne tjenesten.</span><span class="sxs-lookup"><span data-stu-id="b93f7-107">Microsoft doesn't provide this service.</span></span> <span data-ttu-id="b93f7-108">Det finnes imidlertid mange gratis- eller tilbudstjenester som kan tjene QR-koder eller strekkoder som genereres dynamisk basert på en verdi som sendes i en spørringsstreng.</span><span class="sxs-lookup"><span data-stu-id="b93f7-108">However, there are many free or inexpensive services that can serve QR codes or bar codes that are dynamically generated based on a value that is passed in a query string.</span></span>

## <a name="add-a-qr-code-or-bar-code-to-a-transactional-email"></a><span data-ttu-id="b93f7-109">Legge til en QR-kode eller strekkode i transaksjons-e-post</span><span class="sxs-lookup"><span data-stu-id="b93f7-109">Add a QR code or bar code to a transactional email</span></span>

<span data-ttu-id="b93f7-110">Følg denne fremgangsmåten for å sette inn en QR-kode eller strekkode i en transaksjons-e-post som sendes som en del av et e-commerce-innkjøp.</span><span class="sxs-lookup"><span data-stu-id="b93f7-110">To insert a QR code or bar code into a transactional email that is sent as part of an e-commerce purchase, follow these steps.</span></span>

1. <span data-ttu-id="b93f7-111">Åpne HTML-kilden for den transaksjonsbaserte e-postmalen, og legg til en HTML-kode **\<img\>** som peker til QR-koden eller strekkodetjenesten.</span><span class="sxs-lookup"><span data-stu-id="b93f7-111">Open the source HTML for the transactional email template, and add an HTML **\<img\>** tag that points to your QR code or bar code service.</span></span> <span data-ttu-id="b93f7-112">Her er et eksempel:</span><span class="sxs-lookup"><span data-stu-id="b93f7-112">Here is an example.</span></span>

    ```HTML
    <img src="https://YOUR_QR_CODE_BAR_CODE_SERVICE?data=%salesid%&param1=value1&param2=value2" alt="%salesid%" />
    ```

    <span data-ttu-id="b93f7-113">Her er en forklaring av det forrige eksemplet:</span><span class="sxs-lookup"><span data-stu-id="b93f7-113">Here is an explanation of the preceding example:</span></span>

    - <span data-ttu-id="b93f7-114">**DIN\_QR-\_KODE\_STREK\_KODE\_TJENESTE** representerer domenet for QR-koden eller strekkodetjenesten din.</span><span class="sxs-lookup"><span data-stu-id="b93f7-114">**YOUR\_QR\_CODE\_BAR\_CODE\_SERVICE** represents the domain of your QR code or bar code service.</span></span>
    - <span data-ttu-id="b93f7-115">**dara** representerer parameteren som QR-koden eller strekkodetjenesten bruker til å motta innholdet som skal gjengis som en QR-kode eller strekkode.</span><span class="sxs-lookup"><span data-stu-id="b93f7-115">**data** represents the parameter that the QR code or bar code service uses to receive the content that should be rendered as a QR code or bar code.</span></span>

        <span data-ttu-id="b93f7-116">Verdien **%salesid%** må tilordnes til denne parameteren.</span><span class="sxs-lookup"><span data-stu-id="b93f7-116">The value **%salesid%** must be assigned to this parameter.</span></span> <span data-ttu-id="b93f7-117">I dette eksemplet kan du legge merke til at verdien også brukes som alternativ tekst for bildet.</span><span class="sxs-lookup"><span data-stu-id="b93f7-117">In this example, notice that the value is also used as alt text for the image.</span></span>

    - <span data-ttu-id="b93f7-118">**param1** og **param2** representerer ekstra valgfrie parametere.</span><span class="sxs-lookup"><span data-stu-id="b93f7-118">**param1** and **param2** represent additional optional parameters.</span></span>

1. <span data-ttu-id="b93f7-119">Gå til **Detaljhandel og handel \> Hovedkvarteroppsett \> Parametere \> Maler for e-post til organisasjon**, og last opp den oppdaterte HTML-en til den riktige malen for transaksjons-e-post.</span><span class="sxs-lookup"><span data-stu-id="b93f7-119">Go to **Retail and Commerce \> Headquarters setup \> Parameters \> Organization email templates**, and upload the updated HTML to the appropriate transactional email template.</span></span>

> [!NOTE]
> <span data-ttu-id="b93f7-120">Parametere kan være forskjellige blant leverandørene av QR-kode og strekkodetjeneste.</span><span class="sxs-lookup"><span data-stu-id="b93f7-120">Parameters might differ among QR code and bar code service providers.</span></span> <span data-ttu-id="b93f7-121">Husk derfor å ta kontakt med leverandøren for å bekrefte parameterne du må tilordne verdier til.</span><span class="sxs-lookup"><span data-stu-id="b93f7-121">Therefore, be sure to contact your service provider to confirm the parameters that you must assign values to.</span></span>

## <a name="add-a-qr-code-or-bar-code-to-a-receipt-email"></a><span data-ttu-id="b93f7-122">Legge til en QR-kode eller strekkode i en kvitterings-e-post</span><span class="sxs-lookup"><span data-stu-id="b93f7-122">Add a QR code or bar code to a receipt email</span></span> 

<span data-ttu-id="b93f7-123">Følg denne fremgangsmåten for å sette inn en QR-kode eller strekkode i en kvitterings-e-post som kan sendes etter at et kjøp er foretatt ved salgsstedet (POS).</span><span class="sxs-lookup"><span data-stu-id="b93f7-123">To insert a QR code or bar code into a receipt email that can be sent after a purchase is made at the point of sale (POS), follow these steps.</span></span>

1. <span data-ttu-id="b93f7-124">Åpne HTML-kilden for malen for kvitterings-e-post, og legg til en HTML-kode **\<img\>** som peker til QR-koden eller strekkodetjenesten.</span><span class="sxs-lookup"><span data-stu-id="b93f7-124">Open the source HTML for the receipt email template, and add an HTML **\<img\>** tag that points to your QR code or bar code service.</span></span> <span data-ttu-id="b93f7-125">Nedenfor ser du et eksempel.</span><span class="sxs-lookup"><span data-stu-id="b93f7-125">Here is an example below.</span></span>

    ```HTML
    <img src="https://YOUR_QR_CODE_BAR_CODE_SERVICE?data=%receiptid%&param1=value1&param2=value2" alt="%receiptid%" />
    ```

    <span data-ttu-id="b93f7-126">Her er en forklaring av det forrige eksemplet:</span><span class="sxs-lookup"><span data-stu-id="b93f7-126">Here is an explanation of the preceding example:</span></span>

    - <span data-ttu-id="b93f7-127">**DIN\_QR-\_KODE\_STREK\_KODE\_TJENESTE** representerer domenet for QR-koden eller strekkodetjenesten din.</span><span class="sxs-lookup"><span data-stu-id="b93f7-127">**YOUR\_QR\_CODE\_BAR\_CODE\_SERVICE** represents the domain of your QR code or bar code service.</span></span>
    - <span data-ttu-id="b93f7-128">**dara** representerer parameteren som QR-koden eller strekkodetjenesten bruker til å motta innholdet som skal gjengis som en QR-kode eller strekkode.</span><span class="sxs-lookup"><span data-stu-id="b93f7-128">**data** represents the parameter that the QR code or bar code service uses to receive the content that should be rendered as a QR code or bar code.</span></span>

        <span data-ttu-id="b93f7-129">Verdien **%receiptid%** må tilordnes til denne parameteren.</span><span class="sxs-lookup"><span data-stu-id="b93f7-129">The value **%receiptid%** must be assigned to this parameter.</span></span> <span data-ttu-id="b93f7-130">I dette eksemplet kan du legge merke til at verdien også brukes som alternativ tekst for bildet.</span><span class="sxs-lookup"><span data-stu-id="b93f7-130">In this example, notice that the value is also used as alt text for the image.</span></span>

    - <span data-ttu-id="b93f7-131">**param1** og **param2** representerer ekstra valgfrie parametere.</span><span class="sxs-lookup"><span data-stu-id="b93f7-131">**param1** and **param2** represent additional optional parameters.</span></span>

1. <span data-ttu-id="b93f7-132">Gå til **Detaljhandel og handel \> Hovedkvarteroppsett \> Parametere \> Maler for e-post til organisasjon**, og last opp den oppdaterte HTML-en til e-postmalen som har e-post-ID-en **emailrecpt**.</span><span class="sxs-lookup"><span data-stu-id="b93f7-132">Go to **Retail and Commerce \> Headquarters setup \> Parameters \> Organization email templates**, and upload the updated HTML to the email template that has the email ID **emailrecpt**.</span></span>

> [!NOTE]
> <span data-ttu-id="b93f7-133">Parametere kan være forskjellige blant leverandørene av QR-kode og strekkodetjeneste.</span><span class="sxs-lookup"><span data-stu-id="b93f7-133">Parameters might differ among QR code and bar code service providers.</span></span> <span data-ttu-id="b93f7-134">Husk derfor å ta kontakt med leverandøren for å bekrefte parameterne du må tilordne verdier til.</span><span class="sxs-lookup"><span data-stu-id="b93f7-134">Therefore, be sure to contact your service provider to confirm the parameters that you must assign values to.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b93f7-135">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="b93f7-135">Additional resources</span></span>

[<span data-ttu-id="b93f7-136">Sende e-postkvitteringer fra Modern POS (MPOS)</span><span class="sxs-lookup"><span data-stu-id="b93f7-136">Send email receipts from Modern POS (MPOS)</span></span>](email-receipts.md)

[<span data-ttu-id="b93f7-137">Opprette e-postmaler for transaksjonshendelser</span><span class="sxs-lookup"><span data-stu-id="b93f7-137">Create email templates for transactional events</span></span>](email-templates-transactions.md)
