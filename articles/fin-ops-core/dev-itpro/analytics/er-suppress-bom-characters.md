---
title: Utforme ER-konfigurasjoner for å slette BOM-tegn i genererte filer
description: Denne artikkelen beskriver hvordan du konfigurerer et ER-format (Elektronisk rapportering) slik at det genererer rapporter som sletter merker for byterekkefølge (BOM-tegn).
author: kfend
ms.date: 01/04/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2018-01-01
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: EROperationDesigner
ms.openlocfilehash: a2ea132b51f2f451fbe81a9c7869bea84bf4017a
ms.sourcegitcommit: 66d129874635d34a8b29c57762ecf1564e4dc233
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/23/2022
ms.locfileid: "9324027"
---
# <a name="design-er-configurations-to-suppress-bom-characters-in-generated-files"></a>Utforme ER-konfigurasjoner for å slette BOM-tegn i genererte filer

[!include [banner](../includes/banner.md)]

Du kan utforme en [løsning](er-quick-start1-new-solution.md) for [Elektronisk rapportering (ER)](general-electronic-reporting.md) for å generere utgående dokumenter. Hvis du vil generere dokumentene som tekst- eller XML-filer, må løsningen omfatte en ER-[konfigurasjon](general-electronic-reporting.md#Configuration) som inneholder en komponent for ER-format. Hvis du vil angi [tegnkodingen](/windows/win32/intl/character-sets) som representerer tegnsettet i genererte filer, må ER-formatet inneholde formatelementet **Felles\\Fil**. Hvis du vil konfigurere ER-formatkomponenten, åpner du utkastversjonen av ER-konfigurasjonen i ER-formatutformingen og legger til elementet **Felles\\Fil**. I **Koding**-feltet angir du kodingen for utgående filer som genereres ved kjøretid ved hjelp av denne komponenten.

> [!NOTE]
> Hvis formatet inneholder feil kodingsnavn, oppstår det en feil når du lagrer endringene i innstillingene for formatet.

![Legge til et rotelement på Formatutforming-siden.](./media/er-suppress-bom-characters-image1.gif)

Hvis du angir **UTF-8**, **UTF-16** eller **UTF-32** som kodingen, blir alternativet **Slett BOM-tegn** tilgjengelig. Sett dette alternativet til **Ja** for å slette [merker for byterekkefølge (BOM-tegn)](/globalization/encoding/byte-order-mark) i utgående filer som genereres ved kjøretid når det redigerbare ER-formatet kjøres.

> [!NOTE]
> Hvis du lar **Koding**-feltet være tomt, brukes standard **UTF-8**-koding.

![Angi alternativet Slett BOM-tegn på Formatutforming-siden.](./media/er-suppress-bom-characters-image2.gif)

Fullfør den riktige fremgangsmåten for å gå gjennom funksjonaliteten ved kjøretid. Fullfør for eksempel fremgangsmåten i artikkelen [Utsette kjøringen av XML-elementer i ER-formater](er-defer-xml-element.md). Når du har fullført fremgangsmåten i delen [Endre formatet slik at beregningen baseres på genererte utdata](er-defer-xml-element.md#modify-the-format-so-that-the-calculation-is-based-on-generated-output) i denne artikkelen, følger du disse tilleggstrinnene.

1. Angi UTF-kodingen:

    1. Velg **Rapport**-elementet av typen **Felles\\Fil**.
    2. Angi **UTF-8**-kodingen i **Koding**-feltet.

2. Generer en XML-fil som inneholder et BOM-tegn:

    1. Angi **Nei** for alternativet **Slett BOM-tegn** for å ta med BOM-tegn i genererte XML-filer.
    2. Fullfør fremgangsmåten i delen [Utsett kjøringen av XML-elementet Sammendrag slik at beregnet sum brukes](er-defer-xml-element.md#defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used) i artikkelen [Utsette kjøringen av XML-elementer i ER-formater](er-defer-xml-element.md), og lagre den genererte filen som **SampleXmlReport.xml**.

3. Generer en XML-fil som ikke inneholder et BOM-tegn:

    1. Angi **Ja** for alternativet **Slett BOM-tegn** for å slette BOM-tegn i genererte XML-filer.
    2. Fullfør fremgangsmåten i delen [Utsett kjøringen av XML-elementet Sammendrag slik at beregnet sum brukes](er-defer-xml-element.md#defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used) i artikkelen [Utsette kjøringen av XML-elementer i ER-formater](er-defer-xml-element.md), og lagre den genererte filen som **SampleXmlReport (1).xml**.

4. Sammenlign de genererte filene i et verktøy for sammenligning av filer.

    Den første forskjellen du vil legge merke til, er i filhodet. Filen SampleXmlReport.xml inneholder et BOM-tegn, mens filen SampleXmlReport (1).xml ikke gjør det.

    ![Sammenligne genererte filer ved å bruke et verktøy for sammenligning av filer.](./media/er-suppress-bom-characters-image3.png)

## <a name="see-also"></a>Se også

- [Utsette kjøringen av XML-elementer i ER-formater](er-defer-xml-element.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
