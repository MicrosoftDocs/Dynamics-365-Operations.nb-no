---
title: LISTDISTINCT ER-funksjonen
description: Denne artikkelen gir generell informasjon om hvordan du bruker ER-funksjonen LISTDISTINCT.
author: kfend
ms.date: 07/30/2020
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2020-08-01
ms.dyn365.ops.version: AX 10.0.14
ms.custom: ''
ms.assetid: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: cd773f3455af1be1e952cb3852a648436670ce0f
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285283"
---
# <a name="listdistinct-er-function"></a>LISTDISTINCT ER-funksjonen

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

`LISTDISTINCT`-funksjonen beregner det angitte uttrykket som en velger for hver post i den angitte listen. Den returnerer en ny *Postliste*-verdi som inneholder én enkelt post for hver unike velgerverdi.

## <a name="syntax"></a>Syntaks

```
LISTDISTINCT (list, selector)
```

## <a name="arguments"></a>Argumenter

`list`: *Postliste*

Den gyldige banen til en datakilde av *Postliste*-datatypen.

`selector`: *Primitiv datatype*

Et gyldig uttrykk som brukes til å beregne en utvalgsverdi for hver post i den angitte listen.

Følgende datatyper støttes for denne parameteren:

- Boolsk
- Dato
- DateTime
- Guid
- Heltall
- Int64
- Kommatall
- Streng

## <a name="return-values"></a>Returverdier

*Postliste*

Den resulterende listen over oppføringer.

## <a name="usage-notes"></a>Bruksnotater

Strukturen i listen som opprettes, samsvarer med strukturen i den angitte listen.

Den samme velgerverdien kan beregnes for flere poster i den angitte listen. I dette tilfellet er feltverdiene for den tilsvarende posten i den opprettede listen lik verdiene til den første posten fra den angitte listen som velgerverdien beregnes for.

Kjøringen av denne funksjonen utføres på alle datakilder for [elektronisk rapportering (ER)](general-electronic-reporting.md) for *Postliste*-typen som finnes i minnet.

Datakilden **GROUPBY** kan også brukes til å generere listen over poster som velgeren som har distinkte verdier, beregnes for. Fra et ytelses- og minneforbruksperspektiv er det imidlertid bedre å bruke `LISTDISTINCT`-funksjonen enn datakilden **GROUPBY**, fordi kjøringen av funksjonen utføres i minnet.

## <a name="example"></a>Eksempel

Følgende eksempel viser hvordan du kan hente listen over unike kundekontonumre som minst én salgsfaktura eller prosjektfaktura har blitt utstedt til, i løpet av en bestemt periode.

1. Angi **SalesInvoice**-datakilden for `Record list`-typen som refererer til apptabellen **CustInvoiceJour**, og filtrerer salgsfakturaer for bestemte perioder.

    `InvoiceAccount`-feltet i denne datakilden returnerer kontonummeret til en fakturert kunde.

2. Angi **ProjectInvoice**-datakilden for `Record list`-typen som refererer til apptabellen **ProjInvoiceJour**, og filtrerer prosjektfakturaer for bestemte perioder.

    `InvoiceAccount`-feltet i denne datakilden returnerer kontonummeret til en fakturert kunde.

3. Konfigurer datakilden **AllInvoices** for `Calculated field`-typen som inneholder uttrykket `LISTJOIN(SalesInvoice, ProjectInvoice)`.

    Denne datakilden returnerer den sammenføyde listen over salgsfakturaer og prosjektfakturaer.

4. Konfigurer datakilden **InvoicedCustomer** for `Record list`-typen som inneholder uttrykket `LISTDISTINCT(AllInvoices, AllInvoices.InvoiceAccount)`.

    Denne datakilden returnerer en ny liste som inneholder én enkelt post for hver unike kunde som er fakturert i løpet av den definerte perioden. `InvoiceAccount`-feltet i denne listen inneholder et kundekontonummer.

## <a name="additional-resources"></a>Tilleggsressurser

[Listefunksjoner](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
