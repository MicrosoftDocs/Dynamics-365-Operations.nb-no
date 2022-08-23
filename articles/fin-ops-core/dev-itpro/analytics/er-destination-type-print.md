---
title: ER-skrivermåltype
description: Denne artikkelen forklarer hvordan du kan konfigurere et skrivermål for hver MAPPE- eller FIL-komponent i et ER-format (Elektronisk rapportering).
author: kfend
ms.date: 02/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 10.0.9
ms.custom: 97423
ms.assetid: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
ms.openlocfilehash: 7e01476b85c6c35d7c36c90db4d64ab2a2930fec
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9271742"
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

#### <a name="pdf-printing"></a>PDF-utskrift

I versjoner av Finance før versjon 10.0.18 kunne **Skriver**-målet bare konfigureres for filkomponenter som ble brukt til å generere utdata i utskrivbart PDF-format (formatelementet **PDF-sammenslåing** eller **PDF-fil**) eller Microsoft Office Excel- og Word-format (formatelementet **Excel-fil**). Når utdataene genereres i PDF-format, sendes de til en skriver. Når utdataene genereres i Office-format ved hjelp av formatelementet **Excel-fil**, konverteres de automatisk til PDF-format og sendes deretter til en skriver.

Fra og med versjon 10.0.18 kan du imidlertid konfigurere **Skriver**-målet for formatelementet **Felles fil**. Dette formatelementet brukes som oftest til å generere utdata i TXT- eller XML-format. Du kan konfigurere et ER-format som inneholder formatelementet **Felles fil** som rotformatelementet og formatelementet **Binært innhold** som det eneste nestede elementet under det. I dette tilfellet gir formatelementet **Felles fil** gi utdata i formatet som er angitt av bindingen du konfigurerer for formatelementet **Binært innhold**. Du kan for eksempel konfigurere denne bindingen for å [fylle ut](tasks/er-document-management-files-5.md#modify-the-format-to-populate-attachments-into-generating-messages-in-binary-format) dette elementet med innholdet i et vedlegg for [Dokumentstyring](../../fin-ops/organization-administration/configure-document-management.md) i PDF- eller Office-format (Excel eller Word). Du kan skrive ut utdataene ved å bruke det konfigurerte **Skriver**-målet. 

> [!NOTE]
> Når du velger formatelementet **Felles\\Fil** for å konfigurere **Skriver**-målet, går det ikke an å garantere på utformingstidspunktet at det valgte elementet gir utdata i PDF-format eller utdata som kan konverteres til PDF-format. Du får derfor den følgende advarselen: «Kontroller at utdataene som genereres av den valgte formatkomponenten, kan konverteres til PDF. Ellers fjerner du merket for Konverter til PDF.» Du må iverksette tiltak for å forhindre kjøretidsproblemer når utdata som ikke er i PDF-format eller ikke kan konverteres til PDF-format, sendes til utskrift ved kjøretid. Hvis du forventer å motta utdata i Office-format (Excel eller Word), må du velge alternativet **Konverter til PDF**.
>
> I versjon 10.0.26 må du velge **PDF** for parameteren **Dokumentrutingstype** for det konfigurerte **Skriver**-målet for å kunne bruke alternativet **Konverter til PDF**.

#### <a name="zpl-printing"></a>ZPL-utskrift

I versjon 10.0.26 og senere kan du konfigurere **Skriver**-målet for formatelementet **Felles\\Fil** ved å velge **ZPL** for parameteren **Dokumentrutingstype**. I dette tilfellet ignoreres alternativet **Konverter til PDF** ved kjøretid, og TXT- eller XML-utdataene sendes direkte til en valgt skriver ved hjelp av ZPL-kontrakten (Zebra Programming Language) i [dokumentrutingsagenten](install-document-routing-agent.md). Bruk denne funksjonen for et ER-format som representerer et ZPL II-etikettoppsett, til å skrive ut ulike etiketter.

[![Angi parameteren Dokumentrutingstype i dialogboksen Innstillinger for mål.](./media/ER_Destinations-SetDocumentRoutingType.png)](./media/ER_Destinations-SetDocumentRoutingType.png)

Hvis du vil ha mer informasjon om denne funksjonen, kan du se [Utforme en ny ER-løsning for å skrive ut ZPL-etiketter](er-design-zpl-labels.md).

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
