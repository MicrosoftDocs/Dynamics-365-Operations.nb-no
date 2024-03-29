---
title: Utforme et ER-format som holder rader sammen på samme Excel-side
description: Denne artikkelen beskriver hvordan du utformer et ER-format (elektronisk rapportering) som holder rader sammen på samme Microsoft Excel-side.
author: kfend
ms.date: 02/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2022-03-01
ms.dyn365.ops.version: Version 10.0.26
ms.custom: 220314
ms.assetid: ''
ms.search.form: EROperationDesigner
ms.openlocfilehash: 7ecc4358a0d4d9ae9e729393bd3ac4cefbf15ad2
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9287966"
---
# <a name="design-an-er-format-to-keep-rows-together-on-the-same-excel-page"></a>Utforme et ER-format som holder rader sammen på samme Excel-side

[!include [banner](../includes/banner.md)]


Denne artikkelen beskriver hvordan en bruker i rollen som systemadministrator eller funksjonell konsulent for elektronisk rapportering kan konfigurere et [format](er-overview-components.md#format-component) for [elektronisk rapportering (ER)](general-electronic-reporting.md) som genererer utgående dokumenter i Microsoft Excel og behandler dokumentpaginering slik at rader som opprettes, holdes på samme side.

I dette eksemplet skal du endre ER-formatet fra Microsoft som brukes til å skrive ut fritekstfakturaer i Excel. Endringene dine gjør at du kan behandle pagineringen av en generert fritekstfakturarapport slik at alle radene på én fakturalinje, holdes på samme side når det er mulig.

Prosedyrene i denne artikkelen kan fullføres i **USMF**-firmaet. Ingen koding er nødvendig.

I dette eksemplet skal du opprette de nødvendige ER-[konfigurasjonene](general-electronic-reporting.md#Configuration) for eksempelfirmaet **Litware, Inc**. Kontroller at konfigurasjonsleverandøren for eksempelfirmaet **Litware, Inc.** (`http://www.litware.com`) er oppført for ER-rammeverket og at det er merket som **Aktiv**. Hvis denne konfigurasjonsleverandøren ikke er oppført, eller hvis den ikke er merket som **Aktiv**, følger du trinnene i emnet [Opprette en konfigurasjonsleverandør og merke den som aktiv](tasks/er-configuration-provider-mark-it-active-2016-11.md).

## <a name="enter-a-new-free-text-invoice"></a>Registrere en ny fritekstfaktura

1. Følg trinnene i [Opprette en fritekstfaktura](../../../finance/accounts-receivable/create-free-text-invoice-new.md#create-a-free-text-invoice-1) for å legge til en fritekstfaktura.

    1. Legg til én linje på fakturaen.
    2. Legg til fem notater for fakturalinjen.

    ![Gå gjennom fakturalinjenotatene på Vedlegg-siden.](./media/er-keep-excel-rows-together-notes.png)

2. Følg trinnene i [Kopier linjer](../../../finance/accounts-receivable/create-free-text-invoice-new.md#copy-lines) for å opprette fem ekstra fakturalinjer som er kopier av fakturalinjen du la til i det forrige trinnet.

    ![Gå gjennom fritekstfakturalinjene på siden Fritekstfaktura.](./media/er-keep-excel-rows-together-invoice.png)

## <a name="configure-the-er-framework"></a>Konfigurere ER-rammeverket

Følg trinnene i [Konfigurere ER-rammeverket](er-quick-start2-customize-report.md#ConfigureFramework) for å konfigurere minimumssettet med ER-parametere. Du må fullføre dette oppsettet før du begynner å bruke ER-rammeverket til å utforme en egendefinert versjon av et standard ER-format.

## <a name="import-the-standard-er-format-configuration"></a>Importere standard ER-formatkonfigurasjon

Følg trinnene i [Importere standard ER-formatkonfigurasjon](er-quick-start2-customize-report.md#ImportERSolution1) for å legge til standard ER-konfigurasjoner i gjeldende forekomst av Dynamics 365 Finance. Du kan for eksempel importere versjon **252.116** av formatkonfigurasjonen **Fritekstfaktura (Excel)**. Basisversjon **252** av basiskonfigurasjonen for **Fakturamodell** importeres automatisk fra repositoriet sammen med den nødvendige konfigurasjonen for **Fakturamodelltilordning**.

## <a name="set-up-print-management-to-use-the-standard-er-format"></a>Konfigurere utskriftsbehandling slik at standard ER-format brukes

Følg trinnene i [Konfigurere utskriftsbehandling](er-embed-images-header-footer-excel-reports.md#ConfigurePrintManagement1) for å konfigurere utskriftsbehandling for **Kunder**-modulen, slik at standard ER-format brukes til å skrive ut fritekstfakturaer.

## <a name="configure-a-format-destination-for-the-standard-er-format"></a>Konfigurere et formatmål for standard ER-format

Følg trinnene i [Konfigurere et formatmål for forhåndsvisning på skjermen](er-quick-start1-new-solution.md#ConfigureDestination) for å konfigurere ER-målet [Skjerm](er-destination-type-screen.md) for standard ER-format, slik at genererte rapporter konverteres til PDF-format og forhåndsvises i en ny nettleserfane.

## <a name="print-a-free-text-invoice-by-using-the-standard-er-format"></a>Skrive ut en fritekstfaktura ved hjelp av standard ER-format

1. Følg trinnene i [Skriv ut en fritekstfaktura](er-embed-images-header-footer-excel-reports.md#ProcessInvoice1) for å bruke standard ER-format til å generere en fritekstfakturarapport i Excel-format for den tilføyde fakturaen.
2. Last ned den genererte Excel-arbeidsboken, og gå gjennom den i Excel-skrivebordsprogrammet.

    Legg merke til at den sjette linjen på fakturaen starter på første side i rapporten og fortsetter på andre side. Det siste notatet vises på andre side, og det er ikke åpenbart at det hører til på den sjette fakturalinjen. Sideskiftet midt i innholdet for fakturalinjen gjør derfor dokumentet vanskeligere å lese.

    ![Gå gjennom pagineringen av den genererte fritekstfakturaen i Excel-skrivebordsprogrammet.](./media/er-keep-excel-rows-together-invoice1.gif)

De gjenstående fremgangsmåtene i denne artikkelen viser hvordan du kan justere standard ER-format for å forbedre utseendet og lesbarheten til fakturarapporten ved å holde alt innhold for én fakturalinje på samme side.

## <a name="create-a-custom-format"></a>Opprette et egendefinert format

Følg trinnene i [Opprette et egendefinert format](er-embed-images-header-footer-excel-reports.md#DeriveProvidedFormat) for å avlede et format fra det importerte ER-formatet og opprette en ER-konfigurasjon av typen **Egendefinert fritekstfaktura (Excel)** som er tilgjengelig for redigering og endring.

## <a name="edit-the-custom-format"></a>Redigere det tilpassede formatet

1. Følg trinnene i [Opprette et egendefinert format](er-embed-images-header-footer-excel-reports.md#ConfigureDerivedFormat) for å åpne det avledede ER-formatet for redigering i ER-formatutforming.
2. Utvid **Fritekstfaktura \> Ark \> InvoiceLines** i formatkomponenttreet i venstre rute på siden **Formatutforming**, og velg komponenten **InvoiceLines_Values**.
3. Angi **Ja** for **Hold rader sammen** i **Format**-fanen.

    ![Angi alternativet Hold rader sammen for det redigerbare ER-formatet på siden Formatutforming.](./media/er-keep-excel-rows-together-format.png)

4. Velg **Lagre**, og lukk siden.

## <a name="mark-the-custom-format-as-runnable"></a>Merke det egendefinerte formatet som kjørbart

Følg trinnene i [Merke det egendefinerte formatet som kjørbart](er-embed-images-header-footer-excel-reports.md#MarkFormatRunnable) for å gjøre den endrede versjonen av det egendefinerte ER-formatet kjørbart.

## <a name="set-up-print-management-to-use-the-custom-er-format"></a>Konfigurere utskriftsbehandling slik at det egendefinerte ER-formatet brukes

Følg trinnene i [Konfigurere utskriftsbehandling](er-embed-images-header-footer-excel-reports.md#ConfigurePrintManagement2) for å konfigurere utskriftsbehandling for **Kunder**-modulen, slik at det egendefinerte ER-formatet brukes til å skrive ut fritekstfakturaer.

## <a name="configure-a-format-destination-for-the-custom-er-format"></a>Konfigurere et formatmål for det egendefinerte ER-formatet

Følg trinnene i [Konfigurere et formatmål for forhåndsvisning på skjermen](er-quick-start1-new-solution.md#ConfigureDestination) for å konfigurere ER-målet **Skjerm** for det egendefinerte ER-formatet, slik at genererte rapporter konverteres til PDF-format og forhåndsvises i en ny nettleserfane.

## <a name="print-a-free-text-invoice-by-using-the-custom-er-format"></a>Skrive ut en fritekstfaktura ved hjelp av det egendefinerte ER-formatet

1. Følg trinnene i [Skriv ut en fritekstfaktura](er-embed-images-header-footer-excel-reports.md#ProcessInvoice2) for å bruke det egendefinerte ER-formatet til å generere en fritekstfakturarapport i Excel-format for den tilføyde fakturaen.
2. Last ned den genererte Excel-arbeidsboken, og gå gjennom den i Excel-skrivebordsprogrammet.

    Legg merke til at den sjette linjen på fakturaen starter på andre side, og at alle Excel-radene som representerer denne fakturalinjen, vises sammen på denne siden.

    ![Gå gjennom den oppdaterte pagineringen av den genererte fritekstfakturaen i Excel-skrivebordsprogrammet.](./media/er-keep-excel-rows-together-invoice2.gif)

## <a name="additional-resources"></a>Tilleggsressurser

[Utform en konfigurasjon til å generere dokumenter i Excel-format](er-fillable-excel.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
