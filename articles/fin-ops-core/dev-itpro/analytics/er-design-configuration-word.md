---
title: Utforme en ny ER-konfigurasjon for å generere rapporter i Word-format
description: Dette emnet forklarer hvordan brukere kan konfigurere et nytt ER-format (Elektronisk rapportering) for å generere rapporter som Microsoft Word-dokumenter.
author: NickSelin
ms.date: 12/17/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner,  LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-01-01
ms.dyn365.ops.version: Version 10.0.6
ms.openlocfilehash: 98d28c39b2923afecc851299a07aa3b93ef2edce
ms.sourcegitcommit: ac23a0a1f0cc16409aab629fba97dac281cdfafb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/29/2021
ms.locfileid: "7867300"
---
# <a name="design-a-new-er-configuration-to-generate-reports-in-word-format"></a>Utforme en ny ER-konfigurasjon for å generere rapporter i Word-format

[!include [banner](../includes/banner.md)]

Hvis du vil generere rapporter som Microsoft Word-dokumenter, må du utforme en mal for rapportene, for eksempel ved å bruke skrivebordsversjonen av Word. Illustrasjonen nedenfor viser eksempelmalen for kontrollrapporten som kan genereres for å vise detaljer om behandlede leverandørbetalinger.

![Eksempelmal for kontrollrapporten i skrivebordsversjonen av Word.](./media/er-design-configuration-word-image1.png)

Hvis du vil bruke et Word-dokument som en mal for rapporter i Word-format, kan du konfigurere en ny [løsning](er-quick-start1-new-solution.md) for [Elektronisk rapportering (ER)](general-electronic-reporting.md). Denne løsningen må inneholde en ER-[konfigurasjon](general-electronic-reporting.md#Configuration) som inneholder en komponent for ER-[format](general-electronic-reporting.md#FormatComponentOutbound).

> [!NOTE]
> Når du oppretter en ny ER-formatkonfigurasjon for å generere rapporter i Word-format, må du enten velge **Word** som formattype i rullegardinboksen **Opprett konfigurasjon** eller la **Formattype**-feltet stå tomt.

![Opprette en formatkonfigurasjon på Konfigurasjoner-siden.](./media/er-design-configuration-word-image2.gif)

Er-formatkomponenten for løsningen må inneholde formatelementet **Excel\\Fil**, og dette formatelementet må være koblet til Word-dokumentet som skal brukes som mal for genererte rapporter ved kjøretid. Hvis du vil konfigurere ER-formatkomponenten, må du åpne [utkast](general-electronic-reporting.md#component-versioning)versjonen for den opprettede ER-konfigurasjonen i ER-formatutformingen. Legg deretter til elementet **Excel\\Fil**, knytt Word-malen til det redigerbare ER-formatet, og koble denne malen til elementet **Excel\\Fil** du la til.

> [!NOTE]
> Når du knytter til en mal manuelt, må du bruke en [dokumenttype](../../fin-ops/organization-administration/configure-document-management.md#configure-document-types) som tidligere har blitt [konfigurert](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) for dette formålet, i ER-parameterne for å lagre maler i ER-formater.

![Tilknytte en mal på Formatutforming-siden.](./media/er-design-configuration-word-image3.gif)

Du kan legge til de nestede elementene **Excel\\Område** og **Excel\\Celle** for elementet **Excel\\Fil** for å angi strukturen til dataene som skal registreres i genererte rapporter ved kjøretid. Du må deretter binde disse elementene til datakilder i det redigerbare ER-formatet for å angi de faktiske dataene som skal registreres i genererte rapporter ved kjøretid.

![Legge til nestede elementer på Formatutforming-siden.](./media/er-design-configuration-word-image4.gif)

Når du lagrer endringene i ER-formatet på utformingstidspunktet, lagres den hierarkiske formatstrukturen i den tilknyttede Word-malen som en [egendefinert XML-del](/visualstudio/vsto/custom-xml-parts-overview) med navnet **Rapport**. Du må ha tilgang til den endrede malen, laste den ned fra Finance, lagre den lokalt og åpne den i skrivebordsversjonen av Word. Illustrasjonen nedenfor viser den lokalt lagrede eksempelmalen for kontrollrapporten som inneholder den egendefinerte XML-delen **Rapport**.

![Forhåndsvise eksempelrapportmalen i skrivebordsversjonen av Word.](./media/er-design-configuration-word-image5.gif)

Når bindinger for formatelementene **Excel\\Område** og **Excel\\Celle** kjøres ved kjøretid, kommer dataene som hver binding leverer, inn i det genererte Word-dokumentet som et enkeltfelt i den egendefinerte XML-delen **Rapport**. Hvis du vil angi verdiene fra feltene i den egendefinerte XML-delen i et generert dokument, må du legge til de riktige Word-[innholdskontrollene](/office/client-developer/word/content-controls-in-word) i Word-malen, slik at de kan fungere som plassholdere for data som fylles ut ved kjøretid. Hvis du vil angi hvordan innholdskontroller skal fylles ut, tilordner du hver innholdskontroll til det aktuelle feltet i den egendefinerte XML-delen **Rapport**.

![Legge til og tilordne innholdskontroller i skrivebordsversjonen av Word.](./media/er-design-configuration-word-image6.gif)

Du må deretter erstatte den opprinnelige Word-malen i det redigerbare ER-formatet med den endrede malen som nå inneholder Word-innholdskontroller som ble tilordnet til feltene i den egendefinerte XML-delen **Rapport**.

![Erstatte malen på Formatutforming-siden.](./media/er-design-configuration-word-image7.gif)

Når du kjører det konfigurerte ER-formatet, brukes den tilknyttede Word-malen til å generere en ny rapport. De faktiske dataene lagres i Word-rapporten som en egendefinert XML-del med navnet **Rapport**. Når den genererte rapporten åpnes, fylles Word-innholdskontrollene ut med data fra den egendefinerte XML-delen **Rapport**.

## <a name="frequently-asked-questions"></a>Vanlige spørsmål

**Spørsmål:** Jeg har konfigurert et ER-format slik at det skriver ut et Word-dokument som inneholder en firmaadresse. I Word-malen for dette ER-formatet satte jeg inn en innholdskontroll for rik tekst for å presentere en firmaadresse. I Finance angav jeg firmaadressen som tekst på flere linjer og valgte **Enter** for å legge til en vognretur for hver linje jeg angav. Derfor forventer jeg at firmaadressen skal vises som tekst på flere linjer i genererte dokumenter. Adressen vises imidlertid som én tekstlinje som inneholder spesialsymboler i stedet for vognreturer. Hva er feil med innstillingene?

**Svar:** I stedet for å bruke en innholdskontroll for rik tekst, må du bruke en innholdskontroll for ren tekst og merke av for **Tillat vognreturer (flere avsnitt)** i egenskapene for kontrollen.

## <a name="additional-resources"></a>Tilleggsressurser

- [Bruke ER-konfigurasjoner på nytt med Excel-maler for å generere rapporter i Word-format](./tasks/er-design-configuration-word-2016-11.md)
- [Bygge inn bilder og figurer i dokumenter du genererer ved hjelp av ER](electronic-reporting-embed-images-shapes.md#embed-an-image-in-a-word-document)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
