---
title: Støttede sammensatte datatyper for formler i elektronisk rapportering
description: Dette emnet inneholder informasjon om de sammensatte datatypene som støttes i formler i elektronisk rapportering (ER).
author: NickSelin
ms.date: 06/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2593f3128ec103248e109f3c80f48b9d7a035f54
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/06/2021
ms.locfileid: "6355352"
---
# <a name="supported-composite-data-types-for-electronic-reporting-formulas"></a>Støttede sammensatte datatyper for formler i elektronisk rapportering

[!include [banner](../includes/banner.md)]

Dette emnet inneholder informasjon om de sammensatte datatypene som støttes i uttrykk i [Elektronisk rapportering (ER)](general-electronic-reporting.md). De sammensatte datatypene er [klasse](#class), [beholder](#container), [post](#record), [postliste](#record-list) og [objekt](#object).

## <a name="class"></a><a name="class"></a>Klasse

Datatypen *klasse* refererer til en offentlig programklasse. I ER representeres den som en [*post*](#record) som inneholder et eget felt for hver offentlige metode i den refererte klassen. Når oppkallet av metoden er parameterisert, må du også angi de nødvendige argumentene for de aktuelle typene i et ER-uttrykk som er konfigurert slik at det kaller opp metoden.

I komponenter for ER-[tilordning](general-electronic-reporting.md#data-model-and-model-mapping-components) og ER-[format](general-electronic-reporting.md#FormatComponentOutbound) kan du legge til datakilden **Klasse** som presenteres som en datakilde og returnerer en verdi av typen *klasse*. Denne datakilden viser offentlige metoder for klassen som kan kalles ved kjøretid.

> [!NOTE]
> Bare metoder som returnerer en verdi, kan kalles opp fra ER-uttrykk.
>
> Bare metoder som har et område på null til åtte argumenter, kan kalles opp fra ER-uttrykk.

Standardverdien for en *klasse* er **null**.

Illustrasjonen nedenfor viser hvordan datakilden **Systeminformasjon(xInfo)** for **Klasse**-typen legges til for å lage forekomsten av **xInfo**-programklassen og kalle opp **productName()**-metoden for den for å motta navnet på det gjeldende programmet. Navnet på gjeldende program hentes ved kjøretid ved å kjøre bindingen `xInfo.productName`, som ble konfigurert for feltet **Programvarenavn(SoftwareName)** i ER-datamodellen. Denne bindingen kaller opp metoden `productName()` for **xInfo**-programklassen som er representert i den gjeldende modelltilordningen som datakilden **Systeminformasjon(xInfo)**.

[![Konfigurere en Klasse-datakilde i ER-utforming av modelltilordning.](./media/er-formula-supported-data-types-composite-class1.gif)](./media/er-formula-supported-data-types-composite-class1.gif)

Illustrasjonen nedenfor viser hvordan ER-formatet er konfigurert slik at det legger det angitte programnavnet i genererte dokumenter. Feltet **Programvarenavn(SoftwareName)** i den brukte datamodellen var bundet til **Streng**-komponenten som er nestet under XML-elementet **softwareUsed** i ER-formatet. Navnet på det gjeldende programmet legges til ved kjøretid i XML-elementet **softwareUsed** i et generert dokument i XML-format.

[![Konfigurere strukturen for et utgående elektronisk dokument i ER-formatutformingen.](./media/er-formula-supported-data-types-composite-class2.png)](./media/er-formula-supported-data-types-composite-class2.png)

## <a name="container"></a><a name="container"></a>Container

Datatypen *beholder* består av binært innhold. En verdi for *beholder* kan brukes til å sende bestemt informasjon fra et lager til et generert dokument. I ER-rammeverket brukes denne datatypen ofte til å legge til medieinnhold, for eksempel en firmalogo, i genererte dokumenter.

> [!NOTE]
> Selv om ethvert medieelement kan representeres som en verdi for *beholder*, representeres ikke alle verdier for *beholder* som et medieelement. Hvis du konfigurerer et ER-format slik at det bruker en *beholder* til å legge til et bilde i genererte dokumenter, men den refererte *beholderen* ikke returnerer medieinnhold, kan det derfor oppstå et unntak som ligner på følgende eksempel: «Feil under kjøring av kode: Binær (objekt), metoden constructFromContainer ble kalt opp med ugyldige parametere.»

Standardverdien for en *beholder* er **null**.

Følgende illustrasjon viser hvordan feltet **Punktgrafikk(Image)** for typen *Beholder* er bundet til **Logo**-feltet for datamodell av typen **Beholder** i modelltilordningen **Salgsfaktura**. Denne bindingen gjør firmalogoen tilgjengelig for ethvert ER-format som er utformet for rotdefinisjonen **SalesInvoice** og bruker denne modelltilordningen ved kjøretid.

[![Binde et felt av Beholder-typen i ER-utforming av modelltilordning.](./media/er-formula-supported-data-types-composite-container.png)](./media/er-formula-supported-data-types-composite-container.png)

## <a name="record"></a><a name="record"></a>Registrer

En *post* er en samling av navngitte felt, der hvert av dem er knyttet til en verdi av enten en [primitiv](er-formula-supported-data-types-primitive.md) datatype eller en sammensatt datatype. En *post* brukes vanligvis til å representere én post i en postliste. Hvert element representerer i dette tilfellet individuelle felter, metoder og relasjoner.

Standardverdien for en *post* er **tom**.

> [!NOTE]
> Når du henter verdien til et felt i en tom *post*, returneres standardverdien til den aktuelle datatypen.

En *post* kan hentes ved hjelp av følgende funksjoner:

- [FIRST](er-functions-list-first.md)
- [FIRSTORNULL](er-functions-list-firstornull.md)
- [EMPTYRECORD](er-functions-record-emptyrecord.md)
- [NULLCONTAINER](er-functions-record-nullcontainer.md)

Hvis du vil ha mer informasjon om transformasjonen av *post* verdier, kan du se [Liste over ER-funksjoner i listekategorien](er-functions-category-list.md).

## <a name="record-list"></a><a name="record-list"></a>Postliste

En *postliste* er en liste over elementer av typen *post*. En *postliste* brukes vanligvis til å representere listen over poster som er hentet fra en databasetabell.

Tilgang til poster i en *postliste* skjer som standard sekvensielt. Du kan bruke [INDEX](er-functions-list-index.md)-funksjonen og angi indeksen *heltall* for å få tilgang til en bestemt post.

Standardverdien for en *postliste* er **tom**. Du kan bruke [ISEMPTY](/er-functions-list-isempty.md)-funksjonen til å evaluere om en *postliste* er tom.

> [!NOTE]
> Hvis en *postliste* er tom, oppstår det et unntak ved kjøretid ved ethvert forsøk på å hente en feltverdi for en *post*. Hvis du vil vite hvordan du kan bidra til å forhindre kjøretidsunntak av denne typen, kan du se [Vurdering ved saker med tomme lister](er-components-inspections.md#i9).

En *postliste* kan startes ved hjelp av følgende funksjoner:

- [ALLITEMS](er-functions-list-allitems.md)
- [ALLITEMSQUERY](er-functions-list-allitemsquery.md)
- [EMPTYLIST](er-functions-list-emptylist.md)
- [LIST](er-functions-list-list.md)
- [LISTDISTINCT](er-functions-list-listdistinct.md)

Hvis du vil ha mer informasjon om transformasjonen av verdier for *postliste*, kan du se [Liste over ER-funksjoner i listekategorien](er-functions-category-list.md). Hvis du vil vite hvordan du innfører *postliste* elementer, fyller du dem ut med programdata og deretter bruker dataene til å generere forretningsdokumenter, kan du se [Utforme en ny ER-løsning for å skrive ut en egendefinert rapport](er-quick-start1-new-solution.md).

## <a name="object"></a><a name="object"></a>Objekt

Et *objekt* refererer til en tilstandsfull forekomst av en *klasse*. Et *objekt* startes vanligvis i kildekoden. Det sendes deretter til en ER-modelltilordning og gir detaljer om kjøringskonteksten.

Standardverdien for et *objekt* er **null**.

Illustrasjonen nedenfor viser hvordan datakilden **ReportDataContract** for typen *Objekt* legges til for å sende informasjon om en generert faktura fra en kildekode til modelltilordningen **Prosjektfaktura**. Teksten i fakturaforekomsten sendes for eksempel som en del av kjøringskonteksten. Denne teksten tas fra kildekoden ved kjøretid ved å kjøre bindingen `ReportDataContract.parmInvoiceInstanceText`, som ble konfigurert for **Merknad**-feltet i ER-datamodellen. Denne bindingen kaller opp metoden `parmInvoiceInstanceText()` for programklassen **PSAProjInvoiceContract** som er representert i den gjeldende modelltilordningen som datakilden **ReportDataContract**.

[![Konfigurere en Objekt-datakilde i ER-utforming av modelltilordning.](./media/er-formula-supported-data-types-composite-object.gif)](./media/er-formula-supported-data-types-composite-object.gif)

Hvis du vil vite hvordan du sender detaljer om kjøringskonteksten fra kildekode til ER-løsningen som kjører, kan du se [Utarbeide appartefakter for å kalle den utformede rapporten](er-quick-start1-new-solution.md#DevelopCustomCode).

## <a name="additional-resources"></a>Tilleggsressurser

- [Oversikt over elektronisk rapportering](general-electronic-reporting.md)
- [Formelspråk i elektronisk rapportering](er-formula-language.md)
- [Støttede primitive datatyper](er-formula-supported-data-types-primitive.md)
