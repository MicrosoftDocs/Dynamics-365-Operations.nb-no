---
title: CHANGETIMEZONE ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen CHANGETIMEZONE.
author: NickSelin
ms.date: 09/09/2021
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: AX 10.0.23
ms.openlocfilehash: 48e96cfbc19503daf6a20363c4520c765f11a249
ms.sourcegitcommit: 9e8d7536de7e1f01a3a707589f5cd8ca478d657b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/18/2021
ms.locfileid: "7647949"
---
# <a name="changetimezone-er-function"></a>CHANGETIMEZONE ER-funksjon

[!include [banner](../includes/banner.md)]

`CHANGETIMEZONE`-funksjonen returnerer en *[DateTime](er-formula-supported-data-types-primitive.md#datetime)*-verdi i Coordinated Universal Time (Greenwich Mean Time \[GMT\]) som konverteres fra en gitt dato/klokkeslett-verdi i én tidssone til en dato/klokkeslett-verdi i en annen tidssone.

## <a name="syntax"></a>Syntaks

```vb
CHANGETIMEZONE (datetime, base time zone, target time zone)
```

## <a name="arguments"></a>Argumenter

`datetime`: *DateTime*

En dato-/klokkeslettverdi i tidssonen Coordinated Universal Time som representerer dato-/klokkeslettverdien som skal konverteres.

`base time zone`: *[Streng](er-formula-supported-data-types-primitive.md#string)*

Navnet på tidssonen som en angitt dato-/klokkeslettverdi flyttes til før konvertering.

`target time zone`: *Streng*

Navnet på tidssonen som en konvertert dato-/klokkeslettverdi flyttes til under konvertering.

## <a name="return-values"></a>Returverdier

*dato/klokkeslett*

Resultatverdien for dato/klokkeslett i tidssonen Coordinated Universal Time.

## <a name="usage-notes"></a>Bruksnotater

Hvis du vil angi tidssoner for kilde og mål, kan du bruke tidssonenavn som [leveres](https://data.iana.org/time-zones/releases/) av [IANA (Internet Assigned Numbers Authority)](https://www.iana.org/) eller som [støttes](/windows-hardware/manufacture/desktop/default-time-zones) av Microsoft Windows.

Ved kjøretid, hvis unntaket Tidssone \<time zone name\> finnes ikke vises hvis det angitte navnet ikke finnes i IANA-listen eller i Windows-registeret.

For tidssoner med justering for sommertid tar konverteringen høyde for sommertidens tidsforskyvning for Coordinated Universal Time. Den nyeste tilgjengelige informasjonen om denne forskyvningen brukes under konvertering.

## <a name="example-1"></a>Eksempel 1

I dette eksemplet brukes tidssonenavnene for Windows.

Du konfigurerer **DSX**-datakilden for **Beregnet felt**-typen. Det inneholder følgende uttrykk.

```vb
CONCATENATE(
    DATETIMEFORMAT( DSY, "O"), 
    " -> ", 
    DATETIMEFORMAT( CHANGETIMEZONE(DSY, "E. Europe Standard Time", "Hawaiian Standard Time"), "O")
)
```

Hvis du konfigurerer uttrykket til **DSY**-datakilden for **Beregnet felt**-typen som `DATETIMEVALUE ("01-Jun-2021 12:55:00", "dd-MMM-yyyy HH:mm:ss", "EN")`, returnerer datakilden **DSX** teksten **2021-06-01T12:55:00.0000000+00:00 -> 2021-05-31T23:55:00.0000000+00:00**. Denne teksten viser at tidsforskjellen mellom de to angitte tidssonene 1. juni er mer enn 24 timer. Derfor er den konverterte dato-/klokkeslettverdien én dag tidligere enn den angitte dato-/klokkeslettverdien, fordi basistidssonen ligger foran måltidssonen.

Hvis du konfigurerer uttrykket til **DSY**-datakilden for typen **Beregnet felt** som `DATETIMEVALUE ("01-Dec-2021 12:55:00", "dd-MMM-yyyy HH:mm:ss", "EN")`, returnerer datakilden **DSX** teksten **2021-12-01T12:55:00.0000000+00:00 -> 2021-12-01T00:55:00.0000000+00:00**. Denne teksten viser at tidsforskjellen mellom de to angitte tidssonene 1. desember er mindre enn 24 timer. Derfor vil den konverterte dato-/klokkeslettverdien være lik den angitte dato-/klokkeslettverdien.

> [!NOTE]
> Det samme uttrykket returnerer et annet avvik mellom de angitte og konverterte dato-/klokkeslettverdiene for samme tidssonepar, fordi det er observert en annen tidsforskyvning for sommertid for Coordinated Universal Time for angitte tidssonene på en angitt dato/klokkeslett.

## <a name="example-2"></a>Eksempel 2

I dette eksemplet brukes IANA-tidssonenavnene.

Du konfigurerer **DSX**-datakilden for **Beregnet felt**-typen. Det inneholder følgende uttrykk.

```vb
CONCATENATE(
    DATETIMEFORMAT( DSY, "O"), 
    " -> ", 
    DATETIMEFORMAT( CHANGETIMEZONE(DSY, "Europe/Athens", "US/Hawaii"), "O")
)
```

Hvis du konfigurerer uttrykket til **DSY**-datakilden for **Beregnet felt**-typen som `DATETIMEVALUE ("01-Jun-2021 12:55:00", "dd-MMM-yyyy HH:mm:ss", "EN")`, returnerer datakilden **DSX** teksten **2021-06-01T12:55:00.0000000+00:00 -> 2021-05-31T23:55:00.0000000+00:00**. Denne teksten viser at tidsforskjellen mellom de to angitte tidssonene 1. juni er mer enn 24 timer. Derfor er den konverterte dato-/klokkeslettverdien én dag tidligere enn den angitte dato-/klokkeslettverdien, fordi basistidssonen ligger foran måltidssonen.

Hvis du konfigurerer uttrykket til **DSY**-datakilden for typen **Beregnet felt** som `DATETIMEVALUE ("01-Dec-2021 12:55:00", "dd-MMM-yyyy HH:mm:ss", "EN")`, returnerer datakilden **DSX** teksten **2021-12-01T12:55:00.0000000+00:00 -> 2021-12-01T00:55:00.0000000+00:00**. Denne teksten viser at tidsforskjellen mellom de to angitte tidssonene 1. desember er mindre enn 24 timer. Derfor vil den konverterte dato-/klokkeslettverdien være lik den angitte dato-/klokkeslettverdien.

## <a name="example-3"></a>Eksempel 3

Du konfigurerer **DSX**-datakilden for **Beregnet felt**-typen. Det inneholder følgende uttrykk.

```vb
CONCATENATE(
    DATETIMEFORMAT( DSY, "O"), 
    " -> ", 
    DATETIMEFORMAT( CHANGETIMEZONE(DSY, "US/Hawaii", "Europe/Athens"), "O")
)
```

Hvis du konfigurerer uttrykket til **DSY**-datakilden for **Beregnet felt** som `DATETIMEVALUE ("01-Jun-2021 12:55:00", "dd-MMM-yyyy HH:mm:ss", "EN")`, returnerer datakilden **DSX** teksten **2021-06-01T12:55:00.0000000+00:00 -> 2021-06-02T01:55:00.0000000+00:00'**. Denne teksten viser at tidsforskjellen mellom de to angitte tidssonene 1. juni er mer enn 24 timer. Derfor er den konverterte dato-/klokkeslettverdien én dag senere enn den angitte dato-/klokkeslettverdien, fordi måltidssonen ligger foran basistidssonen.

## <a name="example-4"></a>Eksempel 4

Du kan motta en dato-/tidsangivelse fra en ekstern kilde som tekst som ikke inneholder noen tidssoneinformasjon. Du vet imidlertid kanskje tidssonen som kilden opererer i. Du mottar for eksempel dato-/tidsangivelse **01/12/2021 12:55:00** fra en tjeneste som drives i Spania. Hvis du vil lagre denne dato-/klokkeslettverdien riktig i databasen, fullfører du følgende konvertering:

- Konfigurer **DSY**-datakilden for **Beregnet felt**-typen for å konvertere et dato-/tidsangivelse fra tekst til verdien dato-/klokkeslett-verdien Coordinated Universal Time.

    `DATETIMEVALUE ("01/12/2021 12:55:00", "dd/MM/yyyy HH:mm:ss", "ES")`

- Konfigurer **DSX**-datakilden for typen **Beregnet felt** for å forskyve den konverterte dato-/klokkeslettverdien til Coordinated Universal Time som dato-/klokkeslettverdien for tidssonen til den eksterne kilden.

    `CHANGETIMEZONE(DSY, "Romance Standard Time", "GMT Standard Time")`

> [!NOTE]
> Når du bruker `CHANGETIMEZONE`-funksjonen for dato-/klokkeslettkonvertering, må du være oppmerksom på at alle dato-/klokkeslettverdier lagres i databasen som verdien i Coordinated Universal Time-tidssonen. Før denne verdien kan presenteres på applikasjonssider, er den transformert. Transformasjonen vurderer tidssonen som er [angitt](../../fin-ops/organization-administration/tasks/set-users-preferred-time-zone.md) som en foretrukket sone for den påloggede programbrukeren.

## <a name="additional-resources"></a>Tilleggsressurser

[Dato- og klokkeslettfunksjoner](er-functions-category-datetime.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
