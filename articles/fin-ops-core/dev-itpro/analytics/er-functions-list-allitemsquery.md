---
title: ALLITEMSQUERY ER-funksjon
description: Denne artikkelen gir generell informasjon om hvordan du bruker ER-funksjonen ALLITEMSQUERY.
author: kfend
ms.date: 12/12/2019
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: e350dfbe800ddc3e7b1f388fb951d091a283f4e3
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285313"
---
# <a name="allitemsquery-er-function"></a>ALLITEMSQUERY ER-funksjon

[!include [banner](../includes/banner.md)]

`ALLITEMSQUERY`-funksjonen kjøres som en koblet SQL-spørring. Den returnerer en ny *Postliste*-verdi som er flatet ut, og består av en liste over poster som representerer alle elementer som samsvarer med den angitte banen.

## <a name="syntax"></a>Syntaks

```vb
ALLITEMSQUERY (path)
```

## <a name="arguments"></a>Argumenter

`path`: *Postliste*

Den gyldige banen til en datakilde av *Postliste*-datatypen. Den må inneholde minst én relasjon.

## <a name="return-values"></a>Returverdier

*Postliste*

Den resulterende listen over oppføringer.

## <a name="usage-notes"></a>Bruksnotater

Den angitte banen må defineres som en gyldig datakildebane til et datakildeelement av datatypen *Postliste*. Den må også inneholde minst én relasjon. Dataelementer som banens *streng* og *dato* skal føre til en feil i ER-uttrykksverktøyet under utformingen.

Når denne funksjonen brukes på datakilder av datatypen *postliste* som refererer til et programobjekt som kan kalles direkte ved hjelp av SQL (for eksempel en tabell, enhet eller spørring), kjøres den som en sammenkoblet SQL-spørring. Hvis ikke kjører den i minnet som [ALLITEMS](er-functions-list-allitems.md)-funksjonen.

## <a name="example"></a>Eksempel

Du definerer de følgende datakildene i modelltilordningen:

- En **CustInv**-datakilde av *Tabellposter*-typen som refererer til tabellen CustInvoiceTable
- En **FilteredInv**-datakilde av *Beregnet felt*-typen som inneholder uttrykket `FILTER (CustInv, CustInv.InvoiceAccount = "US-001")`
- En **JourLines**-datakilde av *Beregnet felt*-typen som inneholder uttrykket `ALLITEMSQUERY ( FilteredInv.'<Relations'.CustInvoiceJour.'<Relations'.CustInvoiceTrans)`

Når du kjører modelltilordningen for å kalle **JourLines**-datakilden, kjøres følgende SQL-setning:

```sql
SELECT ... FROM CUSTINVOICETABLE T1 CROSS JOIN CUSTINVOICEJOUR T2 CROSS JOIN
CUSTINVOICETRANS T3 WHERE...
```

## <a name="additional-resources"></a>Tilleggsressurser

[Listefunksjoner](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
