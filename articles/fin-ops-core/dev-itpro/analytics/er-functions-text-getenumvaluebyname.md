---
title: GETENUMVALUEBYNAME ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen GETENUMVALUEBYNAME.
author: NickSelin
ms.date: 09/23/2020
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
ms.openlocfilehash: 72b5831e3d2bc2e839b0a569fb314a8ec074a5a1
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746417"
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

## <a name="example-1"></a>Eksempel 1

I følgende illustrasjon introduseres opplistingen **ReportDirection** i en datamodell. Legg merke til at etiketter er definert for opplistingsverdiene.

![Tilgjengelige verdier for en datamodellopplisting](./media/ER-data-model-enumeration-values.PNG)

Illustrasjonen nedenfor viser disse detaljene:

- Datakilden **$Direction** er konfigurert i en ER-rapport. Denne datakilden er konfigurert basert på **ReportDirection**-modellopplistingen.
- Uttrykket `$IsArrivals` er utformet for å bruke den modellopplistingsbaserte **$Direction**-datakilden som en parameter for denne funksjonen.
- Verdien av denne sammenligningen er **SANN**.

![Eksempel på en datamodellopplisting](./media/ER-data-model-enumeration-usage.PNG)

## <a name="example-2"></a>Eksempel 2

Funksjonene `GETENUMVALUEBYNAME` og [`LISTOFFIELDS`](er-functions-list-listoffields.md) lar deg hente verdier og etiketter for støttede opplistinger som tekstverdier. (De støttede opplistingene er programopplistinger, datamodellopplistinger og formatopplistinger.)

I følgende illustrasjon introduseres datakilden **TransType** i en modelltilordning. Denne datakilden refererer til programopplistingen **LedgerTransType**.

![Datakilde for en modelltilordning som refererer til en programopplisting](./media/er-functions-text-getenumvaluebyname-example2-1.png)

Følgende illustrasjon viser datakilden **TransTypeList** som konfigureres i en modelltilordning. Denne datakilden er konfigurert basert på **TransType**-programopplistingen. Funksjonen `LISTOFFIELDS` brukes til å returnere alle opplistingsverdier som en liste med poster som inneholder felt. På denne måten vises detaljene for hver opplistingsverdi.

> [!NOTE]
> Feltet **EnumValue** er konfigurert for datakilden **TransTypeList** ved hjelp av uttrykket `GETENUMVALUEBYNAME(TransType, TransTypeList.Name)`. Dette feltet returnerer en nummereringsverdi for hver post i denne listen.

![Datakilde for en modelltilordning som returnerer alle opplistingsverdier for en valgt opplisting som en liste med oppføringer](./media/er-functions-text-getenumvaluebyname-example2-2.png)

Følgende illustrasjon viser datakilden **VendTrans** som konfigureres i en modelltilordning. Denne datakilden returnerer leverandørtransaksjonsposter fra **VendTrans**-programtabellen. Finanstypen for hver transaksjon defineres av verdien til **TransType**-feltet.

> [!NOTE]
> Feltet **TransTypeTitle** er konfigurert for datakilden **VendTrans** ved hjelp av uttrykket `FIRSTORNULL(WHERE(TransTypeList, TransTypeList.EnumValue = @.TransType)).Label`. Dette feltet returnerer etiketten for en opplistingsverdi for den gjeldende transaksjonen som tekst, hvis denne opplistingsverdien er tilgjengelig. Ellers returneres en tom strengverdi.
>
> Feltet **TransTypeTitle** er bundet til **LedgerType**-feltet i en datamodell som gjør at denne informasjonen kan brukes i alle ER-format som bruker datamodellen som en datakilde.

![Datakilde for en modelltilordning som returnerer leverandørtransaksjoner](./media/er-functions-text-getenumvaluebyname-example2-3.png)

Illustrasjonen nedenfor viser hvordan du kan bruke [feilsøkingsprogrammet for datakilde](er-debug-data-sources.md) til å teste den konfigurerte modelltilordningen.

![Bruke feilsøkingsprogrammet for datakilde til å teste den konfigurerte modelltilordningen](./media/er-functions-text-getenumvaluebyname-example2-4.gif)

Feltet **LedgerType** i en datamodell viser etiketter med transaksjonstyper som forventet.

Hvis du planlegger å bruke denne fremgangsmåten for en stor mengde transaksjonsdata, må du vurdere utførelsesytelsen. Hvis du vil ha mer informasjon, kan du se [Spore kjøringen av ER-formater for å feilsøke ytelsesproblemer](trace-execution-er-troubleshoot-perf.md).

## <a name="additional-resources"></a>Tilleggsressurser

[Tekstfunksjoner](er-functions-category-text.md)

[Spore kjøringen av ER-formater for å feilsøke ytelsesproblemer](trace-execution-er-troubleshoot-perf.md)

[LISTOFFIELDS ER-funksjonen](er-functions-list-listoffields.md)

[FIRSTORNULL ER-funksjon](er-functions-list-firstornull.md)

[WHERE ER-funksjonen](er-functions-list-where.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]