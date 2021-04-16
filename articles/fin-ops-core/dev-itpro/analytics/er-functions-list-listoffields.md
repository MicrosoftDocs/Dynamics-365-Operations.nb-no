---
title: LISTOFFIELDS ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen LISTOFFIELDS.
author: NickSelin
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4f394a557beaeb558f5c7065eefe16f4aadce6ac
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5743781"
---
# <a name="listoffields-er-function"></a>LISTOFFIELDS ER-funksjonen

[!include [banner](../includes/banner.md)]

`LISTOFFIELDS`-funksjonen returnerer en *postliste*-verdi som opprettes basert på strukturen til det angitte argumentet for typen *Opplisting* eller *Container (post)*.

## <a name="syntax-1"></a>Syntaks 1

```vb
LISTOFFIELDS (path)
```

## <a name="syntax-2"></a>Syntaks 2

```vb
LISTOFFIELDS (path, language)
```

## <a name="arguments"></a>Argumenter

`path`: Datakildereferanse

Den gyldige referansebanen til en datakilde for en av følgende datatyper:

- Modellopplisting
- Formatopplisting
- Opplisting av programmer
- Container (post)

`language`: *Streng*

Tekst som representerer en språkkode.

## <a name="return-values"></a>Returverdier

*Postliste*

Den resulterende listen over oppføringer.

## <a name="usage-notes"></a>Bruksnotater

Listen som opprettes, består av poster med følgende felt:

- **Navn** (*Streng*-datatype)
- **Etikett** (*Streng*-datatype)
- **Beskrivelse** (*Streng*-datatype)
- **IsTranslated** (*boolsk* datatype)

Hvis `path`-argumentet refererer til en datakilde av typen *Container (post)*, legges det til en ny post i listen som opprettes, for hvert felt i container-posten det refereres til. For hver post som opprettes, vil **navn**-feltet returnere navnet på feltet i den refererte container-posten som gjeldende post ble opprettet for.

Hvis `path`-argumentet refererer til en datakilde for en av *Opplisting*-typene, legges det til en ny post i listen som opprettes, for hver opplistingsverdi i opplistingsposten det refereres til. For hver post som opprettes, returnerer **Navn**-feltet verdien for den refererte opplistingen som gjeldende post ble opprettet for. **Beskrivelse**-feltet returnerer beskrivelsen av denne opplistingen, og **Etikett**-feltet returnerer etiketten for denne opplistingen.

Når syntaks 1 brukes i kjøretid, må **Etikett**- og **Beskrivelse**-feltene returnere verdier som er basert på språkinnstillingene for ER-formatet som kjører:

- Hvis etikettene og beskrivelsene for det forespurte språket er tilgjengelige, returnerer **Etikett**- og **Beskrivelse**-feltene verdier som er basert på dette språket, og **IsTranslated**-feltet returnerer **Sann**.
- Hvis etikettene og beskrivelsene for det forespurte språket ikke er tilgjengelige, returnerer **Etikett**- og **Beskrivelse**-feltene verdier som er basert på standard **EN-US**-språket, og **IsTranslated**-feltet returnerer **Usann**.

Når syntaks 2 brukes i kjøretid, må **Etikett**- og **Beskrivelse**-feltene returnere verdier som er basert på språket som er definert som det andre argumentet for den kalte funksjonen:

- Hvis etikettene og beskrivelsene for det forespurte språket er tilgjengelige, returnerer **Etikett**- og **Beskrivelse**-feltene verdier som er basert på dette språket, og **IsTranslated**-feltet returnerer **Sann**.
- Hvis etikettene og beskrivelsene for det forespurte språket ikke er tilgjengelige, returnerer **Etikett**- og **Beskrivelse**-feltene verdier som er basert på **EN-US**-språket, og **IsTranslated**-feltet returnerer **Usann**.

## <a name="example-1"></a>Eksempel 1

I følgende illustrasjon introduseres en opplisting i en ER-datamodell.

<a href="./media/ger-listoffields-function-model-enumeration.png"><img src="./media/ger-listoffields-function-model-enumeration-e1474545790761.png" alt="Enumeration in a model" class="alignnone wp-image-1203943 size-full" width="514" height="155" /></a>

Illustrasjonen nedenfor viser disse detaljene:

- Modellopplistingen settes inn i en rapport som en datakilde.
- Et ER-uttrykk bruker modellopplistingen som en parameter i `LISTOFFIELDS`-funksjonen.
- En datakilde av *Postliste*-typen settes inn i en rapport ved hjelp av det opprettede ER-uttrykket.

<a href="./media/ger-listoffields-function-in-format-expression.png"><img src="./media/ger-listoffields-function-in-format-expression-e1474546110395.png" alt="Format" class="alignnone wp-image-1204033 size-full" width="549" height="318" /></a>

Eksemplet nedenfor viser elementene i ER-formatet som er bundet til datakilden for *Postliste*-typen som ble opprettet ved hjelp av funksjonen `LISTOFFIELDS`.

<a href="./media/ger-listoffields-function-format-design.png"><img src="./media/ger-listoffields-function-format-design.png" alt="Format design" class="alignnone size-full wp-image-1204043" width="466" height="221" /></a>

Følgende illustrasjon viser resultatet når det utformede formatet kjøres.

<a href="./media/ger-listoffields-function-format-output.png"><img src="./media/ger-listoffields-function-format-output.png" alt="Format output" class="alignnone size-full wp-image-1204053" width="585" height="158" /></a>

> [!NOTE] 
> Basert på språkinnstillingene for de overordnede **FILE** og **FOLDER**-formatelementene, angis oversatt tekst for etiketter og beskrivelser i utdataene i ER-formatet.

## <a name="example-2"></a>Eksempel 2

Du bruker *Beregnet felt*-datakildetypen til å konfigurere **enumType\_de** og **enumType\_deCH**-datakildene for **enumType**-datamodellopplistingen:

- **enumType\_de** = `LISTOFFIELDS (enumType, "de")`
- **enumType\_deCH** = `LISTOFFIELDS (enumType, "de-CH")`

I dette tilfellet kan du bruke følgende uttrykk til å hente etiketten for opplistingsverdien på sveitsisk (tysk) hvis denne oversettelsen er tilgjengelig. Hvis sveitsisk (tysk) oversettelse ikke er tilgjengelig, er etiketten på tysk.

```vb
IF (NOT (enumType_deCH.IsTranslated), enumType_de.Label, enumType_deCH.Label)
```

## <a name="additional-resources"></a>Tilleggsressurser

[Listefunksjoner](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]