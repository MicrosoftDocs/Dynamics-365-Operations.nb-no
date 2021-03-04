---
title: FORMAT ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen FORMAT.
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8b347a7209ee543f6bd687c2864203eb632d6a4a
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/05/2020
ms.locfileid: "4688419"
---
# <a name="format-er-function"></a>FORMAT ER-funksjonen

[!include [banner](../includes/banner.md)]

`FORMAT`-funksjonen returnerer den angitte strengen som en *streng*-verdi etter at den er formatert ved å erstatte forekomster av **%N** med *N*-te argumentet.

## <a name="syntax"></a>Syntaks

```vb
FORMAT (string, argument 1[, argument 2, …, argument N])
```

## <a name="arguments"></a>Argumenter

`string`: *Streng*

En referanse til en datakilde for *Streng*-datatypen som må formateres. Dette argumentet er obligatorisk.

`argument 1`: *Streng*

Det første argumentet, som brukes til å erstatte forekomster av **%1**. Dette argumentet er obligatorisk.

`argument N`: *Streng*

Det *N*-te argumentet, som brukes til å erstatte forekomster av **%2**, **%3**, osv. Disse tilleggsargumentene er valgfrie.

## <a name="return-values"></a>Returverdier

*Streng*

Den resulterende tekstverdien.

## <a name="usage-notes"></a>Bruksnotater

Hvis et argument ikke er angitt for en parameter, returneres parameteren som **"%N"** i strengen. For verdier for *reell*-typen begrenses standard strengkonverteringen til to desimalplasser.

## <a name="example"></a>Eksempel

I illustrasjonen nedenfor returnerer **PaymentModel**-datakilden en liste over kundeposter ved hjelp av **Kunde**-komponenten. Den returnerer behandlingsdatoverdien ved hjelp av **ProcessingDate**-feltet.

<a href="./media/picture-format-datasource.jpg"><img src="./media/picture-format-datasource.jpg" alt="PaymentModel data source" class="alignnone wp-image-290751 size-full" width="293" height="143" /></a>

I ER-formatet som er utformet for å generere en elektronisk fil for utvalgte kunder, velges **PaymentModel** som en datakilde og styrer prosessflyten. Et unntak for å informere brukeren iverksettes hvis en valgt kunde stoppes for datoen da rapporten behandles. Formelen som er utviklet for denne typen behandlingskontroll kan bruke følgende ressurser:

- Etiketten SYS70894, som har følgende tekst:

    - **For EN-US språk:** "Nothing to print"
    - **For DE-språk:** "Nichts zu drucken"

- Etiketten SYS18389, som har følgende tekst:

    - **For EN-US-språk:** "Customer %1 is stopped for %2."
    - **For DE-språk:** "Debitor '%1' wird für %2 gesperrt."

Her er uttrykket som kan utformes.

```vb
FORMAT (CONCATENATE (@"SYS70894", ". ", @"SYS18389"), model.Customer.Name, DATETIMEFORMAT (model.ProcessingDate, "d"))
```

Hvis en rapport behandles for **Litware Retail**-kunden 17. desember 2015 i **EN-US**-kulturen og **EN-US**-språket, returnerer denne formelen teksten nedenfor, som kan vises for brukeren som en unntaksmelding:

*Nothing to print. Customer Litware Retail is stopped for 12/17/2015.*

Hvis den samme rapporten behandles for **Litware Retail**-kunden 17. desember 2015, i **DE**-kulturen og **DE**-språket, returnerer formelen følgende tekst som bruker et annet datoformat:

*Nichts zu drucken. Debitor 'Litware Retail' wird für 17.12.2015 gesperrt.*

>[!NOTE]
> Følgende syntaks brukes i ER-formler for etiketter:
>
> - **For etiketter fra ressurser i Microsoft Dynamics 365 Finance-appen:** **\@X**, der **X** er etikett-ID-en i applikasjonsobjekttreet (AOT)
> - **For etiketter som ligger i ER-konfigurasjoner:** **@"GER_LABEL:X"**, der **X** er etikett-ID-en i ER-konfigurasjonen

## <a name="additional-resources"></a>Tilleggsressurser

[Tekstfunksjoner](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]