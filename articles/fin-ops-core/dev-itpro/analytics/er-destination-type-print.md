---
title: ER-skrivermåltype
description: Dette emnet forklarer hvordan du kan konfigurere et skrivermål for hver MAPPE- eller FIL-komponent i et ER-format (Elektronisk rapportering).
author: NickSelin
ms.date: 02/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 672b1d70607a32d30c703ce39573d7480462fec45739b6e1e49ef27166a50e2c
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6712718"
---
# <a name="printer-destination"></a><a name="PrinterDestinationType"></a>Skrivermål

[!include [banner](../includes/banner.md)]

Du kan sende et generert dokument direkte til en nettverksskriver for direkte utskrift.

## <a name="prerequisites"></a>Forutsetninger

Før du begynner, må du installere og konfigurere Dokumentruting-agenten og deretter registrere nettverksskriverne. Hvis du vil ha mer informasjon, kan du se [Installere dokumentrutingsagenten for å muliggjøre nettverksutskrift](./install-document-routing-agent.md).

## <a name="make-the-printer-destination-available"></a>Gjøre skrivermålet tilgjengelig

Hvis du vil gjøre **Skriver**-målet tilgjengelig i gjeldende forekomst av Microsoft Dynamics 365 Finance, går du til **Funksjonsstyring**-arbeidsområdet og aktiverer følgende funksjoner, i denne rekkefølgen:

1. Konvertere utgående dokumenter for elektronisk rapportering fra Microsoft Office-formater til PDF
2. Dokumentrutingsagent som mål for elektronisk rapportering for utgående dokumenter

[![Aktivere målfunksjonen for ER-skriveren i Funksjonsstyring.](./media/ER_Destinations-EnablePrinterDestinationFeature.png)](./media/ER_Destinations-EnablePrinterDestinationFeature.png)

### <a name="applicability"></a>Relevans

**Skriver**-målet kan bare konfigureres for filkomponenter som brukes til å generere utdata i enten utskrivbart PDF-format (PDF-fusjon eller PDF-filformatelementer) eller Microsoft Office Excel-/Word-format (Excel-fil). Når utdata genereres i PDF-format, sendes de til en skriver. Når utdata genereres i Microsoft Office-format, konverteres de automatisk til PDF-format og sendes deretter til en skriver.

### <a name="limitations"></a>Begrensninger

**Skriver**-målet implementeres bare for skydistribueringer.

### <a name="use-the-printer-destination"></a>Bruke skrivermålet

1. Sett **Aktivert**-alternativet til **Ja** for å sende et generert dokument til en skriver.
2. I **Skrivernavn**-feltet velger du påkrevd nettverksskriver.
3. Sett **Lagre i utskriftsarkiv?**-alternativet til **Ja** for å lagre de genererte utdataene i utskriftsarkivet, slik at de er tilgjengelige for videre utskrift. Hvis du vil ha tilgang til arkiverte utdata senere, går du til **Organisasjonsstyring** \> **Forespørsler og rapporter** \> **Rapportarkiv**.

[![Bruke skrivermålet.](./media/ER_Destinations-PrinterDestination.png)](./media/ER_Destinations-PrinterDestination.png)

> [!NOTE]
> **Konverter til PDF**-alternativet trenger ikke å være aktivert når du konfigurerer **Skriver**-målet. PDF-konverteringen for utskriftsformål vil finne sted selv om alternativet er deaktivert.

Hvis du vil bruke en bestemt [sideretning](electronic-reporting-destinations.md#SelectPdfPageOrientation) når du skriver ut et utgående dokument i Excel-format, må du aktivere alternativet **Konverter til PDF**. Når du setter alternativet **Konverter til PDF** til **Ja**, blir **Sideretning**-feltet tilgjengelig. Du kan velge en sideretning i **Sideretning**-feltet.

## <a name="additional-resources"></a>Tilleggsressurser

- [Oversikt over elektronisk rapportering (ER)](general-electronic-reporting.md)
- [Mål for elektronisk rapportering (ER)](electronic-reporting-destinations.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]