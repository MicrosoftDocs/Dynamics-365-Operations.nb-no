---
title: Støttede primitive datatyper for formler i elektronisk rapportering
description: Dette emnet inneholder informasjon om de primitive datatypene som støttes i formler i elektronisk rapportering (ER).
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
ms.openlocfilehash: 9d5e6bb5e070ebbcdb7e99b1b70010acd5fca5ac
ms.sourcegitcommit: 15aacd0e109b05c7281407b5bba4e6cd99116c28
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/10/2021
ms.locfileid: "6224107"
---
# <a name="supported-primitive-data-types-for-electronic-reporting-formulas"></a>Støttede primitive datatyper for formler i elektronisk rapportering

[!include [banner](../includes/banner.md)]

Dette emnet inneholder informasjon om de primitive datatypene som støttes i uttrykk i [Elektronisk rapportering (ER)](general-electronic-reporting.md). Her er en liste over de primitive datatypene:

- [boolsk](#boolean)
- [dato](#date)
- [dato/klokkeslett](#datetime)
- [opplisting](#enumeration)
- [guid](#guid)
- [heltall](#integer)
- [int64](#int64)
- [kommatall](#real)
- [streng](#string)

## <a name="boolean"></a><a name="boolean"></a>Boolsk

Den primitive datatypen *boolsk* inneholder en verdi som evalueres som *sann* eller *usann*. Du kan bruke de reserverte litterale nøkkelordene **Sann** og **Usann** der det forventes et *boolsk* uttrykk. Standardverdien er *usann*.

Den interne representasjonen av en *boolsk* er et *heltall*. *Heltall* sverdien 0 (null) evalueres som *usann*, og alle andre *heltall* sverdier evalueres som *sann*. Når du [validerer](general-electronic-reporting-formula-designer.md#TestFormula) et konfigurert uttrykk som returnerer en *boolsk* i [ER-formeldesigneren](er-advanced-formula-editor.md), viser testresultatruten *0* (null) når et uttrykk returnerer *usann*. Ellers viser testresultatruten *1*.

En *boolsk* har ingen implisitte konverteringer. Du kan imidlertid bruke [TEXT](er-functions-text-text.md)-funksjonen til eksplisitt å konvertere en *boolsk* til en *streng*:

- Den *usanne* verdien konverteres til tekststrengen **Usann**.
- Den *sanne* verdien konverteres til tekststrengen **Sann**.

> [!NOTE]
> Denne konverteringen er ikke avhengig av den gitte [konteksten](er-design-multilingual-reports.md) for språk og kultur.

Sammenlignings [operatorer](er-formula-language.md#Operators) er den eneste typen operator som kan brukes med den *boolske* datatypen. Følgende operatorer kan brukes til å sammenligne to *boolske* verdier: \<\> og =.

## <a name="date"></a><a name="date"></a>Dato

Den primitive datatypen *dato* inneholder dag, måned og år. Datoer kan startes ved hjelp av følgende funksjoner:

- [DATEVALUE](er-functions-datetime-datevalue.md)
- [NULLDATE](er-functions-datetime-nulldate.md)
- [SESSIONTODAY](er-functions-datetime-sessiontoday.md)
- [TODAY](er-functions-datetime-today.md)

Datatypen *dato* kan inneholde datoer mellom 1. januar 1900 og 31. desember 2154. Standardverdien er **null**, og den interne representasjonen er datoen 1. januar 1900.

En *dato* har ingen implisitte konverteringer. Du kan imidlertid bruke følgende eksplisitte konverteringsfunksjoner:

- [DATEFORMAT](er-functions-datetime-dateformat.md)
- [DATETODATETIME](er-functions-datetime-datetodatetime.md)
- [TEXT](er-functions-text-text.md)

Med [ADDDAYS](er-functions-datetime-adddays.md)-funksjonen kan du legge til og trekke fra dager i datoer. På denne måten kan du flytte datoen et bestemt antall dager inn i fremtiden og fortiden. [DAYS](er-functions-datetime-days.md)-funksjonen lar deg trekke datoer fra andre datoer og beregne differansen i dager. Hvis du vil ha mer informasjon om transformasjonen av *dato* verdier, kan du se [Liste over ER-funksjoner i kategorien Dato og klokkeslett](er-functions-category-datetime.md).

Sammenlignings [operatorer](er-formula-language.md#Operators) er den eneste typen operator som kan brukes med datatypen *dato*. Følgende operatorer kan brukes til å sammenligne to verdier for *dato*: \<\>, \<, \<=, =, \> og \>=.

## <a name="datetime"></a><a name="datetime"></a>Dato/klokkeslett

Den primitive datatypen *dato/klokkeslett* kombinerer typen *dato* og en verdi som representerer tiden som er gått siden midnatt. Tiden uttrykkes i timer, minutter, sekunder og brøkdeler av et sekund. En verdi for *dato/klokkeslett* inneholder også informasjon om tidssonen.

Datatypen *dato/klokkeslett* kan inneholde datoer mellom 1. januar 1900 (1900-01-01T00:00:00.0000000+00:00 i [formatet](/dotnet/standard/base-types/standard-date-and-time-format-strings)) rundtur og 31. desember 2154 (2154/12/31T11:59:59.9999999+00:00 i formatet rundtur). Den minste tidsenheten i *dato/klokkeslett* er ti milliondeler av et sekund.

> [!NOTE]
> Når [angivelsen](/dotnet/standard/base-types/standard-date-and-time-format-strings) **tt** brukes for timer, kan ikke tidsverdier over 12:59:59:9999999 tolkes som gyldige tider.
>
> Når angivelsen **TT** brukes for timer, kan ikke tidsverdier over 23:59:59:9999999 tolkes som gyldige tider.

Standardverdien er **null**, og den interne representasjonen er datoen 1. januar 1900 (1900-01-01T00:00:00.0000000+00:00 i formatet rundtur).

Datoer/klokkeslett kan startes ved hjelp av følgende funksjoner:

- [DATETIMEVALUE](er-functions-datetime-datetimevalue.md)
- [NULNULLDATETIMELDATE](er-functions-datetime-nulldatetime.md)
- [SESSIONNOW](er-functions-datetime-sessionnow.md)
- [NOW](er-functions-datetime-now.md)

En forekomst av *dato/klokkeslett* har ingen implisitte konverteringer. Du kan imidlertid bruke følgende eksplisitte konverteringsfunksjoner:

- [DATETIMEFORMAT](er-functions-datetime-datetimeformat.md)
- [TEXT](er-functions-text-text.md)

Hvis du vil ha mer informasjon om transformasjonen av verdier for *dato/klokkeslett*, kan du se [Liste over ER-funksjoner i kategorien Dato og klokkeslett](er-functions-category-datetime.md).

Sammenlignings [operatorer](er-formula-language.md#Operators) er den eneste typen operator som kan brukes med datatypen *dato/klokkeslett*. Følgende operatorer kan brukes til å sammenligne to verdier for *dato/klokkeslett*: \<\>, \<, \<=, =, \> og \>=.

## <a name="enumeration"></a><a name="enumeration"></a>Opplisting

Den primitive datatypen *opplisting* er en liste over litteraler. Du kan bruke opplistinger som er definert i [kildekoden](../dev-ref/xpp-data-primitive.md#enum) for programmet. Du kan også innføre dine egne opplistinger i ER-[datamodellen](general-electronic-reporting.md#data-model-and-model-mapping-components) og ER-[format](general-electronic-reporting.md#FormatComponentOutbound)komponentene.

En *opplisting* for program kan brukes i uttrykk i enhver ER-modelltilordning og ethvert ER-format.

Illustrasjonen nedenfor viser hvordan du kan legge til modellopplistingen **CustVendCorrectiveReasonCode** i den redigerbare ER-datamodellen.

[![Konfigurere en modellopplisting i ER-datamodellutformingen](./media/er-formula-supported-data-types-primitive-enum1.gif)](./media/er-formula-supported-data-types-primitive-enum1.gif)

En modell *opplisting* kan brukes i uttrykk i enhver ER-modelltilordning og ethvert ER-format som ble opprettet under en datamodell der *opplistingen* ble innført.

Illustrasjonen nedenfor viser hvordan du kan legge til formatopplistingen **Liste over underkategorier for snudd avregning for Natura** i det redigerbare ER-formatet.

[![Konfigurere en formatopplisting i ER-formatutformingen](./media/er-formula-supported-data-types-primitive-enum2.gif)](./media/er-formula-supported-data-types-primitive-enum2.gif)

En format *opplisting* kan bare brukes i uttrykk av ER-formatet der *opplistingen* ble innført.

Du må bruke riktig type ER-datakilder til å overføre en bestemt opplisting til en konfigurert ER-komponent som en konstant eller som en verdi som brukeren som kjører en ER-løsning, definerte i dialogboksen ved kjøretid.

- Du får tilgang til programopplistinger ved hjelp av datakildene **Dynamics 365 for Operations \ Opplisting** og **Generelt \ Inndataparametere for brukere**. Illustrasjonen nedenfor viser hvordan du kan legge til det redigerbare ER-formatet i datakildene **appenumNoYes** og **uipNoYes** som refererer til programopplistingen **NoYes**.

    [![Legge til datakilder for programopplisting i ER-formatutforming](./media/er-formula-supported-data-types-primitive-enum3a.gif)](./media/er-formula-supported-data-types-primitive-enum3a.gif)

- Du kan få tilgang til datamodellopplistinger ved hjelp av datakildene **Datamodell \ Opplisting** og **Datamodell \ Inndataparametere for brukere for opplisting**. Illustrasjonen nedenfor viser hvordan du kan legge til det redigerbare ER-formatet i datakilden **CustVendCorrectiveReasonCode** som henviser til datamodellopplistingen **CustVendCorrectiveReasonCode**.

    [![Legge til datakilder for modellopplisting i ER-formatutforming](./media/er-formula-supported-data-types-primitive-enum3b.gif)](./media/er-formula-supported-data-types-primitive-enum3b.gif)

- Du får tilgang til formatopplistinger ved hjelp av datakildene **Format \ Opplisting** og **Format \ Inndataparametere for brukere for opplisting**. Illustrasjonen nedenfor viser hvordan du kan legge til det redigerbare ER-formatet i datakilden **NaturaReverseCharge** som henviser til formatopplistingen **Underkategorier for snudd avregning for Natura**.

    [![Legge til datakilder for formatopplisting i ER-formatutforming](./media/er-formula-supported-data-types-primitive-enum3c.gif)](./media/er-formula-supported-data-types-primitive-enum3c.gif)

En *opplisting* har ingen implisitte konverteringer. Du kan imidlertid bruke konverteringsfunksjonen [TEXT](er-functions-text-text.md) til å konvertere en *opplisting* til en tekststreng. Denne konverteringen er ikke språkavhengig. Hvis du vil vite hvordan du kan knytte en *opplisting* sverdi til de aktuelle språkspesifikke etikettene, kan du se brukseksemplene for funksjonene [LISTOFFIELDS](er-functions-list-listoffields.md) og [GETENUMVALUEBYNAME](er-functions-text-getenumvaluebyname.md).

Sammenlignings [operatorer](er-formula-language.md#Operators) er den eneste typen operator som kan brukes med datatypen *opplisting*. Følgende operatorer kan brukes til å sammenligne to verdier for *opplisting*: \<\> og =.

## <a name="guid"></a><a name="guid"></a>Guid

Den primitive datatypen *guid* inneholder en GUID-verdi (globalt unik identifikator). En GUID er en verdi som kan brukes på tvers av alle datamaskiner og nettverk, der en unik identifikator kreves. Det er usannsynlig at nummeret dupliseres. En gyldig GUID oppfyller alle følgende spesifikasjoner:

- Den må bestå av 32 heksadesimale sifre.
- Det må i tillegg finnes fire bindestreker på følgende steder: 8-4-4-4-12.
- Du kan i tillegg legge til valgfrie klammeparenteser \{\} i begynnelsen og på slutten strengen. Både **\{2CDB0FE7-D7B3-4938-A0F0-FE28FB8FE212\}** og **2CDB0FE7-D7B3-4938-A0F0-FE28FB8FE212** er eksempler på gyldige GUID-strenger.
- De må derfor bestå av totalt 36 eller 38 tegn, avhengig av om klammeparenteser er lagt til.
- Bokstavene som brukes som heksadesimale sifre, kan være store bokstaver (A–F), små bokstaver (a–f) eller blandet.

Følgende eksplisitte konverteringsfunksjoner kan brukes:

- [GUIDVALUE](er-functions-text-guidvalue.md)
- [TEXT](er-functions-text-text.md)

Sammenlignings [operatorer](er-formula-language.md#Operators) er den eneste typen operator som kan brukes med datatypen *guid*. Følgende operatorer kan brukes til å sammenligne to *guid*-verdier: \<\> og =.

## <a name="integer"></a><a name="integer"></a>Heltall

Den primitive datatypen *heltall* representerer et tall uten desimaler. Heltall brukes som kontrollvariabler i gjentagende setninger eller som indekser i postlister.

En *heltall* slitteral er heltallet slik det angis direkte i et ER-[uttrykk](general-electronic-reporting-formula-designer.md#formula-designer-overview) (formel), for eksempel **12345**. Et *heltall* har en bitbredde på 32. Standardverdien er **0**, og den interne representasjonen er et langt tall. Et *heltall* konverteres automatisk til et *kommatall*.

I tillegg kan følgende eksplisitte konverteringsfunksjoner brukes:

- [INTVALUE](er-functions-conversion-intvalue.md)
- [NUMBERFORMAT](er-functions-text-numberformat.md)
- [TEXT](er-functions-text-text.md)

Intervallet til et *heltall* er \[–2 147 483 647 : 2 147 483 647\]. Alle heltall i dette intervallet kan brukes som litteraler.

Alle sammenligningsoperatorer og matematiske [operatorer](er-formula-language.md#Operators) kan brukes med datatypen *heltall*.

## <a name="int64"></a><a name="int64"></a>Int64

Den primitive datatypen *int64* representerer et tall uten desimaler. *Int64*-verdier brukes som kontrollvariabler i gjentagende setninger eller som postidentifikatorer.

Et *int64* har en bitbredde på 64. Standardverdien er **0**, og den interne representasjonen er et langt tall. Et *int64* konverteres automatisk til et *kommatall*.

I tillegg kan følgende eksplisitte konverteringsfunksjoner brukes:

- [INT64VALUE](er-functions-conversion-int64value.md)
- [NUMBERFORMAT](er-functions-text-numberformat.md)
- [TEXT](er-functions-text-text.md)

Intervallet til et *int64* er \[–9 223 372 036 854 775 807 : 9 223 372 036 854 775 807\].

Alle sammenligningsoperatorer og matematiske [operatorer](er-formula-language.md#Operators) kan brukes med datatypen *int64*.

## <a name="real"></a><a name="real"></a>Kommatall

Den primitive datatypen *kommatall* kan inneholde desimalverdier i tillegg til heltall. Du kan bruke desimallitteraler hvor som helst der et *kommatall* forventes. En desimalliteral er desimalen slik den angis direkte i koden, for eksempel **2.19**.

> [!NOTE]
> I ER-uttrykk brukes alltid et punktum (.) som desimalskilletegn.

Kommatall kan brukes i alle uttrykk, og de kan brukes med både sammenligningsoperatorer og aritmetiske operatorer. Et *kommatall* har en presisjon på 16 signifikante sifre. Standardverdien for et *kommatall* er **0.0**, og den interne representasjonen er en binærkodet desimal (BCD). BCD-kodingen muliggjør nøyaktige representasjoner av verdier som er multiplum av 0.1. Intervallet til en *kommatall* variabel er –(10)<sup>127</sup> til og med (10)<sup>127</sup>. Alle kommatall i dette intervallet kan brukes som litteraler i ER-uttrykk.

Et *kommatall* har ingen implisitte konverteringer. Du kan imidlertid bruke følgende funksjoner til eksplisitt å konvertere et *kommatall* til andre datatyper og andre datatyper til et *kommatall*:

- [INTVALUE](er-functions-conversion-intvalue.md)
- [INT64VALUE](er-functions-conversion-int64value.md)
- [NUMBERFORMAT](er-functions-text-numberformat.md)
- [TEXT](er-functions-text-text.md)
- [VALUE](er-functions-conversion-value.md)

Alle sammenligningsoperatorer og matematiske [operatorer](er-formula-language.md#Operators) kan brukes med datatypen *kommatall*.

## <a name="string"></a><a name="string"></a>Streng

Den primitive datatypen *streng* representerer en serie med tegn som brukes som tekst, kontonumre, adresser og telefonnumre.

*Streng* litteraler er tegn som står i anførselstegn (""). *Streng* litteraler kan brukes der *streng* verdier forventes i ER-uttrykk. Du kan bruke strenger i logiske uttrykk, for eksempel sammenligninger. Du kan også sette sammen *streng* verdier ved hjelp av operatoren **\&** eller [CONCATENATE](er-functions-text-concatenate.md)-funksjonen.

> [!NOTE]
> Hvis du setter sammen to *streng* verdier og vil at den resulterende *strengen* skal strekke seg over flere linjer, bruker du linjeskiftskilletegnet mellom verdiene. Når det gjelder TEXT-utdataene, kan dette skilletegnet være et tegn som genereres ved hjelp av uttrykket [CHAR](er-functions-text-char.md)(10) eller CHAR(13). Når det gjelder HTML, kan det være koden **\<br\>**.

Standardverdien for en *streng* er en tom tekststreng som ikke har noen tegn, og den interne representasjonen er en liste over tegn.

Det finnes ingen automatiske konverteringer for strenger. Følgende eksplisitte konverteringsfunksjoner kan imidlertid brukes:

- [CHAR](er-functions-text-char.md)
- [FORMAT](er-functions-text-format.md)
- [LEFT](er-functions-text-left.md)
- [LEN](er-functions-text-len.md)
- [MID](er-functions-text-mid.md)
- [PADLEFT](er-functions-text-padleft.md)
- [REPLACE](er-functions-text-replace.md)
- [RIGHT](er-functions-text-right.md)
- [TEXT](er-functions-text-text.md)
- [TRANSLATE](er-functions-text-translate.md)
- [TRIM](er-functions-text-trim.md)
- [UPPER](er-functions-text-upper.md)

Hvis du vil ha mer informasjon om transformasjonen av *streng* verdier, kan du se [Liste over ER-funksjoner for tekstkategorien](er-functions-category-text.md).

En *streng* kan inneholde et ubestemt antall tegn.

Alle sammenlignings [operatorer](er-formula-language.md#Operators) kan brukes med datatypen *streng*.

## <a name="additional-resources"></a>Tilleggsressurser

- [Oversikt over elektronisk rapportering](general-electronic-reporting.md)
- [Formelspråk i elektronisk rapportering](er-formula-language.md)
- [Sammensatte datatyper som støttes](er-formula-supported-data-types-composite.md)
