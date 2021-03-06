---
title: NUMSEQVALUE ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen NUMSEQVALUE.
author: NickSelin
ms.date: 12/17/2019
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
ms.openlocfilehash: c3351360d0c1afca9f828ba4fc935096ddfd67f2
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744009"
---
# <a name="numseqvalue-er-function"></a>NUMSEQVALUE ER-funksjon

[!include [banner](../includes/banner.md)]

`NUMSEQVALUE`-funksjonen returnerer en *streng*-verdi som representerer den nye genererte verdien av en nummerserie, basert på den angitte nummerserien, omfanget og område-IDen. Område-IDen er lik firmakoden som angis av konteksten som ER-formatet kjøres under.

## <a name="syntax-1"></a>Syntaks 1

```vb
NUMSEQVALUE (number sequence code)
```

## <a name="syntax-2"></a>Syntaks 2

```vb
NUMSEQVALUE (number sequence record ID)
```

## <a name="syntax-3"></a>Syntaks 3

```vb
NUMSEQVALUE (number sequence code, scope type, scope ID)
```

## <a name="arguments"></a>Argumenter

`number sequence code`: *Streng*

En tekstverdi som representerer koden for nummerserien som en ny verdi kreves i.

`number sequence record ID`: *Int64*

En *Int64*-verdi som representerer post-IDen for en post i NumberSequenceTable-tabellen som inneholder definisjonen av nummerserien som en ny verdi kreves i.

`scope type`: *Opplistingsverdi*

En opplistingsverdi for **ERExpressionNumberSequenceScopeType**-opplistingen som definerer omfanget av nummerserien som en ny verdi kreves i. De tilgjengelige omfangstypene er **delt**, **juridisk enhet** og **firma**.

`scope ID`: *Streng*

En *streng*-verdi som identifiserer omfanget, basert på den angitte omfangstypen.

## <a name="return-values"></a>Returverdier

*Streng*

Den resulterende tekstverdien.

## <a name="usage-notes"></a>Bruksnotater

For **Delt**-omfangstypen angir du en tom streng som område-ID.

For omfangstypene **Firma** og **Juridisk enhet** angir du firmakoden som område-ID. Hvis du angir en tom streng som område-ID for disse omfangstypene, brukes den gjeldende firmakoden.

Når syntaks 1 brukes, er nummerserien forespurt for **Firma**-omfangstypen, og firmakoden angis av konteksten som ER-formatet kjøres under.

## <a name="example-1"></a>Eksempel 1

I ER-format definerer du **AskNumSeq**-datakilden for *Inndataparameter*-typen. Denne datakilden refererer til den utvidede datatypen **Beskrivelse** (EDT). Deretter definerer du **NumSeq**-datakilden for *Beregnet felt*-typen. Denne datakilden inneholder uttrykket `NUMSEQVALUE (AskNumSeq)`. Når **NumSeq**-datakilden kalles, returneres den nye genererte verdien av nummerserien som ble angitt under kjøring ved å skrive inn koden i dialogboksen. Nummerserien blir forespurt for **Firma**-omfangstypen. Firmakoden angis av konteksten som ER-formatet kjøres under.

## <a name="example-2"></a>Eksempel 2

Følgende datakilder defineres i modelltilordningen:

- **LedgerParms**-datakilden for *Tabell*-typen. Denne datakilden refererer til LedgerParameters-tabellen.
- **NumSeq**-datakilden for *Beregnet felt*-typen. Denne datakilden inneholder uttrykket `NUMSEQVALUE ( LedgerParameters.'numRefJournalNum()'.NumberSequenceId)`.

Når **NumSeq**-datatypen kalles opp, returneres den nye genererte verdien for nummerserien som er konfigurert i økonomimodul-parameterne for firmaet som leverer konteksten som ER-formatet kjøres under. Denne nummerserien identifiserer journaler unikt og fungerer som et partinummer som kobler sammen transaksjonene.

## <a name="example-3"></a>Eksempel 3

Følgende datakilder defineres i modelltilordningen:

- Datakilden **enumScope** for Microsoft Dynamics 365 Finance *-opplistingstypen*. Denne datakilden refererer til opplistingen **ERExpressionNumberSequenceScopeType**.
- **NumSeq**-datakilden for *Beregnet felt*-typen. Denne datakilden inneholder uttrykket `NUMSEQVALUE ("Gene_1", enumScope.Company, "")`.

Når **NumSeq**-datatypen kalles opp, returneres den nye genererte verdien for **Gene\_1**-nummerserien som er konfigurert for firmaet som levererte konteksten som ER-formatet kjøres under.

## <a name="additional-resources"></a>Tilleggsressurser

[Andre funksjoner (spesifikke for forretningsområder)](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]