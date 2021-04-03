---
title: Komprimere store dokumenter som genereres i Elektronisk rapportering
description: Dette emnet forklarer hvordan du komprimerer store dokumenter som genereres av formatet Elektronisk rapportering (ER).
author: NickSelin
manager: kfend
ms.date: 09/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EROperationDesigner, ERFormatDestinationTable
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-01-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 8a8f55b33624b057a6abf9af5084209ac6a0c778
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562340"
---
# <a name="compress-large-documents-that-are-generated-in-electronic-reporting"></a>Komprimere store dokumenter som genereres i Elektronisk rapportering 

[!include [banner](../includes/banner.md)]

Du kan bruke [rammeverket for Elektroniske Rapportering (ER)](general-electronic-reporting.md) til å konfigurere en løsning som henter transaksjonsdata for å generere et utgående dokument. Dette genererte dokumentet kan være ganske stort. Når denne dokumenttypen genereres, brukes [AOS (Application Object Server)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/access-instances#location-of-packages-source-code-and-other-aos-configurations)-minnet til å oppbevare det. På et eller annen tidspunkt må dokumentet lastes ned fra Microsoft Dynamics 365 Finance-programmet. For øyeblikket er maksimumsstørrelsen for ett enkelt dokument som genereres i ER, begrenset til 2 gigabyte (GB). I tillegg [begrenser](https://fix.lcs.dynamics.com/Issue/Details?kb=4569432&bugId=453907&dbType=3) Finance for øyeblikket størrelsen på en nedlastet fil til 1 GB. Derfor må du konfigurere en ER-løsning som reduserer sannsynligheten for at disse begrensningene vil bli overskredet, og at du vil motta et unntak om at **dataflyten er for lang** eller **overflyt eller underflyt i aritmetisk operasjon**.

Når du konfigurerer en løsning, kan du endre ER-formatet i Operasjonsutforming ved å legge til et rotelement av **Mappe**-typen for å komprimere innholdet som genereres av noen av de nestede elementene. Komprimering fungerer "til riktig tid", slik at maksimal minnebruk og størrelsen på filen som lastes ned, kan reduseres.

> [!NOTE]
> Filkomprimering tar en ekstra prosentandel av CPU-bruken.

Hvis du vil vite mer om denne tilnærmingen, kan du fullføre eksemplet i dette emnet.

## <a name="example-compress-an-outbound-document"></a>Eksempel: Komprimere et utgående dokument

Dette eksemplet viser hvordan en bruker som er tilordnet rollen **Systemansvarlig** eller **Funksjonell konsulent for elektronisk rapportering**, kan konfigurere et ER-format for å komprimere et generert dokument.

### <a name="prerequisites"></a>Forutsetninger

Før du kan fullføre fremgangsmåten i dette emnet, må du fullføre følgende trinn:

1. [Aktivere en konfigurasjonsleverandør](er-defer-xml-element.md#activate-a-configuration-provider).
2. [Importere ER-eksempelkonfigurasjonene](er-defer-xml-element.md#import-the-sample-er-configurations).
3. [Gå gjennom det importerte formatet](er-defer-xml-element.md#review-the-imported-format).

> [!NOTE]
> For øyeblikket starter formatstrukturen fra **Rapport**-elementet for typen **Fil** og inneholder XML-elementer. Derfor vil et utgående dokument bli generert i XML-format, og ingen komprimering vil bli brukt.

### <a name="generate-an-er-format-to-get-an-uncompressed-document"></a>Generere et ER-format for å få et ukomprimert dokument

1. [Kjør det importerte formatet](er-defer-xml-element.md#run-the-imported-format).
2. Legg merke til at størrelsen på det genererte dokumentet i XML-format er 3 kilobyte (KB).

    ![Forhåndsvisning av det ikke-komprimerte utgående dokumentet](./media/er-compress-outbound-files1.png)

### <a name="modify-the-format-to-compress-the-generated-output"></a>Endre formatet for å komprimere det genererte resultatet

1. Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Konfigurasjoner**.
2. På **Konfigurasjoner**-siden, i konfigurasjonstreet, utvider du **Modell for å lære utsatte elementer**.
3. Velg **Format for å lære utsatte XML-elementer**-konfigurasjonen.
4. Velg **Utforming** for å endre formatstrukturen.
5. På **Formatutforming**-siden, i **Format**-fanen, velger du **Legg til rot** for å legge til rotformatelement.
6. I dialogboksen **Legg til** velger du **Felles\\Mappe**.
7. Velg **OK** for å bekrefte tillegget av det nye rotelementet.
8. Velg **Lagre**.

> [!NOTE]
> Formatstrukturen starter fra elementet til **Mappe**-typen. Dette elementet vil generere utdata som en komprimert (zip) fil. Når et dokument som genereres av **Rapport**-elementet, plasseres i en utgående zip-fil, komprimeres innholdet for å redusere størrelsen på den utgående filen.

### <a name="generate-an-er-format-to-get-a-compressed-document"></a>Generere et ER-format for å få et komprimert dokument

1. På **Formatutforming**-siden velger du **Kjør**.
2. Last ned zip-filen som nettleseren tilbyr, og åpne den for gjennomgang.
3. Legg merke til at størrelsen på det genererte dokumentet i ZIP-format er 1 KB.

    > [!NOTE] 
    > Komprimeringsforholdet i XML-filen som denne zip-filen inneholder, er 87 prosent. Komprimeringsforholdet avhenger av hvilke data som komprimeres.

    ![Forhåndsvisning av det komprimerte utgående dokumentet](./media/er-compress-outbound-files2.png)

> [!NOTE]
> Hvis ER-[målet](electronic-reporting-destinations.md) er konfigurert for formatelementet som genererer utdata (**Rapport**-elementet i dette eksemplet), vil komprimering av utdataene hoppes over.

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over elektronisk rapportering (ER)](general-electronic-reporting.md)

[Mål for elektronisk rapportering (ER)](electronic-reporting-destinations.md)

[Utsette kjøringen av XML-elementer i ER-formater](er-defer-xml-element.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]