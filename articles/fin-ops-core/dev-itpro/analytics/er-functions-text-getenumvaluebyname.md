---
title: GETENUMVALUEBYNAME ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen GETENUMVALUEBYNAME.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 33ccf358dc5355cd00d5ff41ebd8148a334cba38
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743861"
---
# <a name="getenumvaluebyname-er-function"></a>GETENUMVALUEBYNAME ER-funksjonen

[!include [banner](../includes/banner.md)]

`GETENUMVALUEBYNAME`-funksjonen søker etter en bestemt *opplistings*-verdi i den angitte opplistingsdatakilden ved hjelp av opplistingsnavnet som er angitt som en *Streng*-verdi. Hvis *opplistings*-verdien blir funnet, returnerer funksjonen den. Hvis ikke returnerer funksjonen opplistingsverdien **null**.

## <a name="syntax"></a>Syntaks

```vb
GETENUMVALUEBYNAME (enumeration data source path, enumeration value text)
```

## <a name="arguments"></a>Argumenter

`enumeration data source path`: *Opplisting*

Den gyldige referansebanen til en datakilde for en av følgende opplistingstyper:

- ER-modellopplisting
- ER-formatopplisting
- Microsoft Dynamics 365 Finance-opplisting

`enumeration value text`: *Streng*

En strengverdi som representerer navnet på en enkelt opplistingsverdi.

## <a name="return-values"></a>Returverdier

*Opplisting* som kan nullstilles

Den resulterende opplistingsverdien.

## <a name="usage-notes"></a>Bruksnotater

Det blir ikke registrert noe unntak hvis en *opplisting*-verdi ikke blir funnet ved å bruke navnet på opplistingsverdien som er angitt som en *streng*-verdi.

## <a name="example"></a>Eksempel

I følgende illustrasjon introduseres opplistingen **ReportDirection** i en datamodell. Legg merke til at etiketter er definert for opplistingsverdiene.

<p><a href="./media/ER-data-model-enumeration-values.PNG"><img src="./media/ER-data-model-enumeration-values.PNG" alt="Available values for a data model enumeration" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

Illustrasjonen nedenfor viser disse detaljene:

- Datakilden **$Direction** er konfigurert i en ER-rapport. Denne datakilden er konfigurert basert på **ReportDirection**-modellopplistingen.
- Uttrykket `$IsArrivals` er utformet for å bruke den modellopplistingsbaserte **$Direction**-datakilden som en parameter for denne funksjonen.
- Verdien av denne sammenligningen er **SANN**.

<a href="./media/ER-data-model-enumeration-usage.PNG"><img src="./media/ER-data-model-enumeration-usage.PNG" alt="Example of data model enumeration" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

## <a name="additional-resources"></a>Tilleggsressurser

[Tekstfunksjoner](er-functions-category-text.md)
