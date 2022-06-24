---
title: Dokumentrutingsoppsett for nummerskiltetiketter
description: Denne artikkelen beskriver hvordan du kan bruke formateringsmetoder til å skrive ut verdier på etiketter.
author: perlynne
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLicensePlateLabel, WHSLicensePlateLabelBuildConfig, WHSLicensePlateLabel, WHSDocumentRoutingLayout
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2012-04-01
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: 10e63353cda93d666d7f23f59508b73e5492c3cc
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8847882"
---
# <a name="document-routing-layout-for-license-plate-labels"></a>Dokumentrutingsoppsett for nummerskiltetiketter

[!include [banner](../includes/banner.md)]


Dokumentrutingsoppsettet definerer oppsettet til nummerskiltetiketter og dataene som skrives ut på dem. Du konfigurerer utløsingspunkt for utskrift når du definerer menyelementer og arbeidsmaler for mobilenheter.

I et typisk scenario vil mottaksassistenter på lageret skrive ut nummerskiltetiketter umiddelbart etter at de har registrert innholdet på paller som ankommer mottaksområdet. De fysiske etikettene brukes på pallene. De kan deretter brukes til validering som en del av plasseringsprosessen som følger, og fremtidige utgående plukkoperasjoner.

Du kan skrive ut svært komplekse etiketter, forutsatt at utskriftsenheten kan tolke teksten som sendes til den. Et ZPL-oppsett (Zebra Programming Language) som inneholder en strekkode, kan for eksempel ligne på følgende eksempel.

```dos
^XA~TA000~JSN^LT0^MNW^MTD^PON^PMN^LH0,0^JMA^PR2,2~SD15^JUS^LRN^CI0^XZ
^XA
^MMT
^PW320
^LL0160
^LS0
^FT20,58^A0N,28,28^FH\^FDLabel:^FS
^FT20,81^AAN,18,10^FH\^FD$LicensePlateId$^FS
^BY1,3,17^FT20,106^BCN,,Y,N,N,A
^FD$LicensePlateId$^FS
^PQ1,,,Y^XZ
```

Som en del av etikettutskriftsprosessen vil teksten `$LicensePlateId$` i dette eksemplet erstattes med en dataverdi.

Hvis du vil se hvilke verdier som blir skrevet ut, går du til **Lagerstyring \> Forespørsler og rapporter \> Nummerskiltetiketter**.

Flere generelt tilgjengelige verktøy for etikettgenerering kan hjelpe deg med å formatere teksten for etikettoppsettet. Mange av disse verktøyene støtter formatet `$FieldName$`. I tillegg bruker Microsoft Dynamics 365 Supply Chain Management en spesiell formateringslogikk som en del av felttilordningen for dokumentrutingsoppsettet.

## <a name="turn-on-this-feature-for-your-system"></a>Aktivere denne funksjonen for systemet

Hvis systemet ikke allerede inneholder funksjonene som er beskrevet i denne artikkelen, kan du gå til [Funksjonsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) og aktivere funksjonen *Forbedrede oppsett for nummerskiltetikett*. (Fra og med Supply Chain Management versjon 10.0.21 er denne funksjonen aktivert som standard. Denne funksjonen er obligatorisk fra og med Supply Chain Management 10.0.25 og kan ikke deaktiveres.)

## <a name="custom-number-formats"></a>Egendefinerte tallformater

Du kan tilpasse formateringen av numeriske feltverdier som skrives ut ved å bruke koder som har følgende format.

```dos
$FieldName:FormatString$
```

Her er en forklaring på dette formatet:

- `FieldName` er navnet på datafeltet (for eksempel **Antall**).
- `FormatString` definerer hvordan dataene må skrives ut.

Eksemplene nedenfor viser hvordan du kan tilpasse feltet for arbeidsantall (**Antall**):

- Hvis du alltid vil vise fire sifre (ved å bruke nuller som plassholdere), bruker du `$Qty:0000$`. Hvis for eksempel antallet er 10, vil etiketten vise "0010".
- Hvis du alltid vil vise to desimaler, bruker du `$Qty:0.00$`. Hvis for eksempel antallet er 10, vil etiketten vise "10,00".

Hvis du vil ha en fullstendig liste over de tilgjengelige tallformatstrengene, kan du se [Egendefinerte tallformatstrenger](/dotnet/standard/base-types/custom-numeric-format-strings).

## <a name="custom-string-formats"></a>Egendefinerte strengformater

Du kan fjerne de første tegnene i en streng ved å bruke følgende felt og formatkode.

```dos
$FieldName:#..$
```

Her angir `#` hvor mange tegn det skal hoppes over. Hvis du for eksempel vil skrive ut et SSCC-skiltnummer (Serial Shipping Container Code) som ikke inkluderer de to første tegnene, bruker du `$LicensePlateId:2..$`. I dette tilfellet vil skiltnummeret 0011111111111222221 skrives ut som 11111111111222221.

## <a name="custom-datetime-formats"></a>Egen definerte dato- og klokkeslettformater

Følgende eksempel viser hvordan du kan styre formatet som brukes til å skrive ut datoer.

```dos
$PrintedDate:dd-MM-yyyy$
```

I dette eksemplet vil datoen 30. april 2020 skrives ut som "30-04-2020".

Hvis du vil ha en fullstendig liste over de tilgjengelige dato- og klokkeslettformatene, kan du se [Egendefinerte formatstrenger for dato/klokkeslett](/dotnet/standard/base-types/custom-date-and-time-format-strings).

## <a name="print-individual-lines-from-multiline-data"></a>Skrive ut enkeltlinjer fra flerlinjedata

Hvis et datafelt inneholder flere linjer (det vil si linjer som er atskilt med linjeskift), kan du skrive ut en enkelt linje ved hjelp av følgende format.

```dos
$FieldName[#]$
```

Her er `#` linjenummeret du vil skrive ut. (Bruk 1 for den første linjen.)

Systemet har for eksempel et `AdditionalAddress`-felt som lagrer følgende adresse med flere linjer:

Contoso Inc.  
123 Gatenavn  
By, Stat

Du kan skrive ut denne adressen, én linje om gangen, ved hjelp av følgende koder.

| Kode | Tekst som skrives ut |
|---|---|
| `$AdditionalAddress[1]$` | Contoso Inc. |
| `$AdditionalAddress[2]$` | 123 Gatenavn |
| `$AdditionalAddress[3]$` | By, Stat |

## <a name="print-and-format-from-a-display-method"></a>Skrive ut og formatere fra en visningsmetode

Du kan skrive ut fra en visningsmetode ved å bruke følgende format.

```dos
$DisplayMethod()$
```

Du kan kombinere dette formatet med andre typer som ble beskrevet tidligere i denne artikkelen. Du kan for eksempel ha en visningsmetode kalt `DisplayListOfItemsNumbers()`, og du kan skrive ut det første varenummeret for denne metoden. I dette tilfellet kan du bruke følgende kode.

```dos
$DisplayListOfItemsNumbers()[1]$
```

## <a name="more-information-about-how-to-print-labels"></a>Mer informasjon om hvordan du skriver ut etiketter

Hvis du vil ha mer informasjon om hvordan du definerer og skriver ut etiketter, kan du se [Aktivere utskrift av nummerskiltetikett](tasks/license-plate-label-printing.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]