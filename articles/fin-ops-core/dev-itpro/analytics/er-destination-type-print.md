---
title: ER-skrivermåltype
description: Dette emnet forklarer hvordan du kan konfigurere et skrivermål for hver MAPPE- eller FIL-komponent i et elektronisk rapporteringsformat (ER) som er konfigurert til å generere utgående dokumenter i enten PDF- eller Microsoft Office-formater (Excel\Word).
author: NickSelin
manager: AnnBe
ms.date: 01/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 58e067baa130458e3a8e788d978604f208140a03
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019927"
---
# <a name="PrinterDestinationType"></a><span data-ttu-id="b074e-103">Skrivermål</span><span class="sxs-lookup"><span data-stu-id="b074e-103">Printer destination</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b074e-104">Du kan sende et generert dokument direkte til en nettverksskriver for direkte utskrift.</span><span class="sxs-lookup"><span data-stu-id="b074e-104">You can send a generated document directly to a network printer for direct printing.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="b074e-105">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="b074e-105">Prerequisites</span></span>

<span data-ttu-id="b074e-106">Før du begynner, må du installere og konfigurere Dokumentruting-agenten og deretter registrere nettverksskriverne.</span><span class="sxs-lookup"><span data-stu-id="b074e-106">Before you begin, you must install and configure the Document Routing Agent, and then register the network printers.</span></span> <span data-ttu-id="b074e-107">Hvis du vil ha mer informasjon, kan du se [Installere dokumentrutingsagenten for å muliggjøre nettverksutskrift](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/install-document-routing-agent).</span><span class="sxs-lookup"><span data-stu-id="b074e-107">For more information, see [Install the Document Routing Agent to enable network printing](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/install-document-routing-agent).</span></span>

## <a name="make-the-printer-destination-available"></a><span data-ttu-id="b074e-108">Gjøre skrivermålet tilgjengelig</span><span class="sxs-lookup"><span data-stu-id="b074e-108">Make the Printer destination available</span></span>

<span data-ttu-id="b074e-109">Hvis du vil gjøre **Skriver**-målet tilgjengelig i gjeldende forekomst av Microsoft Dynamics 365 Finance, går du til **Funksjonsstyring**-arbeidsområdet og aktiverer følgende funksjoner, i denne rekkefølgen:</span><span class="sxs-lookup"><span data-stu-id="b074e-109">To make the **Printer** destination available in the current instance of Microsoft Dynamics 365 Finance, go to the **Feature management** workspace, and turn on the following features, in this order:</span></span>

1. <span data-ttu-id="b074e-110">Konvertere utgående dokumenter for elektronisk rapportering fra Microsoft Office-formater til PDF</span><span class="sxs-lookup"><span data-stu-id="b074e-110">Convert Electronic Reporting outbound documents from Microsoft Office formats to PDF</span></span>
2. <span data-ttu-id="b074e-111">Dokumentrutingsagent som mål for elektronisk rapportering for utgående dokumenter</span><span class="sxs-lookup"><span data-stu-id="b074e-111">Document Routing Agent as Electronic Reporting destination for outbound documents</span></span>

<span data-ttu-id="b074e-112">[![Aktivere målfunksjonen for ER-skriveren i Funksjonsstyring](./media/ER_Destinations-EnablePrinterDestinationFeature.png)](./media/ER_Destinations-EnablePrinterDestinationFeature.png)</span><span class="sxs-lookup"><span data-stu-id="b074e-112">[![Turning on the ER printer destination feature in Feature management](./media/ER_Destinations-EnablePrinterDestinationFeature.png)](./media/ER_Destinations-EnablePrinterDestinationFeature.png)</span></span>

### <a name="applicability"></a><span data-ttu-id="b074e-113">Relevans</span><span class="sxs-lookup"><span data-stu-id="b074e-113">Applicability</span></span>

<span data-ttu-id="b074e-114">**Skriver**-målet kan bare konfigureres for filkomponenter som brukes til å generere utdata i enten utskrivbart PDF-format (PDF-fusjon eller PDF-filformatelementer) eller Microsoft Office Excel-/Word-format (Excel-fil).</span><span class="sxs-lookup"><span data-stu-id="b074e-114">The **Printer** destination can be configured only for file components that are used to generate output in either printable PDF format (PDF Merger or PDF file format elements) or Microsoft Office Excel/Word format (Excel file).</span></span> <span data-ttu-id="b074e-115">Når utdata genereres i PDF-format, sendes de til en skriver.</span><span class="sxs-lookup"><span data-stu-id="b074e-115">When output is generated in PDF format, it's sent to a printer.</span></span> <span data-ttu-id="b074e-116">Når utdata genereres i Microsoft Office-format, konverteres de automatisk til PDF-format og sendes deretter til en skriver.</span><span class="sxs-lookup"><span data-stu-id="b074e-116">When output is generated in Microsoft Office format, it's automatically converted to PDF format and then sent to a printer.</span></span>

### <a name="limitations"></a><span data-ttu-id="b074e-117">Begrensninger</span><span class="sxs-lookup"><span data-stu-id="b074e-117">Limitations</span></span>

<span data-ttu-id="b074e-118">Denne funksjonen er en forhåndsvisningsfunksjon, og den er underlagt vilkårene for bruk beskrevet i [Ekstra vilkår for bruk for Microsoft Dynamics 365-forhåndsvisninger](https://go.microsoft.com/fwlink/?linkid=2105274).</span><span class="sxs-lookup"><span data-stu-id="b074e-118">This feature is a preview feature and is subject to the terms of use that are described in [Supplemental Terms of Use for Microsoft Dynamics 365 Previews](https://go.microsoft.com/fwlink/?linkid=2105274).</span></span>

<span data-ttu-id="b074e-119">**Skriver**-målet implementeres bare for skydistribueringer.</span><span class="sxs-lookup"><span data-stu-id="b074e-119">The **Printer** destination is implemented only for cloud deployments.</span></span>

### <a name="use-the-printer-destination"></a><span data-ttu-id="b074e-120">Bruke skrivermålet</span><span class="sxs-lookup"><span data-stu-id="b074e-120">Use the Printer destination</span></span>

1. <span data-ttu-id="b074e-121">Sett **Aktivert**-alternativet til **Ja** for å sende et generert dokument til en skriver.</span><span class="sxs-lookup"><span data-stu-id="b074e-121">Set the **Enabled** option to **Yes** to send a generated document to a printer.</span></span>
2. <span data-ttu-id="b074e-122">I **Skrivernavn**-feltet velger du påkrevd nettverksskriver.</span><span class="sxs-lookup"><span data-stu-id="b074e-122">In the **Printer name** field, select the required network printer.</span></span>
3. <span data-ttu-id="b074e-123">Sett **Lagre i utskriftsarkiv?**-alternativet til **Ja** for å lagre de genererte utdataene i utskriftsarkivet, slik at de er tilgjengelige for videre utskrift.</span><span class="sxs-lookup"><span data-stu-id="b074e-123">Set the **Save in print archive?** option to **Yes** to store the generated output in the print archive, so that it's available for further printing.</span></span> <span data-ttu-id="b074e-124">Hvis du vil ha tilgang til arkiverte utdata senere, går du til **Organisasjonsstyring** \> **Forespørsler og rapporter** \> **Rapportarkiv**.</span><span class="sxs-lookup"><span data-stu-id="b074e-124">To access archived output later, go to **Organization administration** \> **Inquiries and reports** \> **Report archive**.</span></span>

<span data-ttu-id="b074e-125">[![Bruke skrivermålet](./media/ER_Destinations-PrinterDestination.png)](./media/ER_Destinations-PrinterDestination.png)</span><span class="sxs-lookup"><span data-stu-id="b074e-125">[![Using the Printer destination](./media/ER_Destinations-PrinterDestination.png)](./media/ER_Destinations-PrinterDestination.png)</span></span>

> [!NOTE]
> <span data-ttu-id="b074e-126">**Konverter til PDF**-alternativet trenger ikke å være aktivert når du konfigurerer **Skriver**-målet.</span><span class="sxs-lookup"><span data-stu-id="b074e-126">The **Convert to PDF** option doesn't have to be turned on when you configure the **Printer** destination.</span></span> <span data-ttu-id="b074e-127">PDF-konverteringen for utskriftsformål vil finne sted selv om alternativet er deaktivert.</span><span class="sxs-lookup"><span data-stu-id="b074e-127">The PDF conversion for printing purposes will occur even if the option is turned off.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b074e-128">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="b074e-128">Additional resources</span></span>

- [<span data-ttu-id="b074e-129">Oversikt over elektronisk rapportering (ER)</span><span class="sxs-lookup"><span data-stu-id="b074e-129">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="b074e-130">Mål for elektronisk rapportering (ER)</span><span class="sxs-lookup"><span data-stu-id="b074e-130">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)
