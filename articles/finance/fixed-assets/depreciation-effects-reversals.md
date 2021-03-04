---
title: Avskrivningseffekter av tilbakeføringer
description: Denne artikkelen beskriver potensielle konsekvenser av å tilbakeføre en anleggsmiddeltransaksjon.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTrans
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 2961
ms.assetid: 63a3ac92-c321-4379-a86a-b1b14915f340
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dd4c4a9e7e89b34b1311b38310877b45e4d95b22
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4446281"
---
# <a name="depreciation-effects-with-reversals"></a>Avskrivningseffekter av tilbakeføringer

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver potensielle konsekvenser av å tilbakeføre en anleggsmiddeltransaksjon. 

Du kan tilbakeføre anleggsmiddeltransaksjoner, og transaksjoner som er tilknyttet et anleggsmiddel. Du kan også oppheve en tilbakeført transaksjon. 

Du kan tilbakeføre eller oppheve en transaksjon som ikke har den nyeste transaksjonen postert til tablået for anleggsmiddelet. Først må du bestemme om det er postert avskrivningstransaksjoner etter transaksjonen du tilbakefører. Dette er fordi avskrivning ikke omberegnes når du tilbakefører en transaksjon. Derfor er avskrivning ofte overvurdert eller undervurdert etter tilbakeføringen, som vist i eksemplene. 

For å sikre at avskrivningen er riktig når du tilbakefører en transaksjon, må du ikke gå videre med tilbakeføringen hvis du får en melding som sier at avskrivningen ikke blir omberegnet. Da må du i stedet tilbakeføre den avskrivningstransaksjonen som ble postert etter den transaksjonen du forsøkte å tilbakeføre, og deretter gå videre med tilbakeføringen. Du vil ikke få noen advarsel om avskrivningsomberegning, og du kan gå videre med tilbakeføringen. 

Eksemplene nedenfor viser beregningene som skjer hvis du fortsetter etter meldingen uten å tilbakeføre avskrivningstransaksjonene først.

## <a name="example-1-depreciation-is-overstated"></a> Eksempel 1: Avskrivning overvurdert
Et anleggsmiddelet er definert med 5 års levetid og lineær avskrivning (60 avskrivningsperioder). I dette eksemplet er avskrivningen overvurdert.
#### <a name="asset-transaction-history"></a>Transaksjonshistorikk for anleggsmiddel

| Dato       | Transaksjonstype                                                          | Beløp                                    |
|------------|---------------------------------------------------------------------------|-------------------------------------------|
| 1. januar  | Anskaffelse                                                               | 59 000,00                                 |
| 1. januar  | Anskaffelsesjustering                                                    | 1 000,00                                  |
| 31. januar | Avskrivning (opprettet ved bruk av forslag for én avskrivningsperiode) | 1 000,00Beregning: Bokført verdi (59 000 + 1 000) / Antall gjenværende avskrivningsperioder (60) |

#### <a name="reversal-action"></a>Tilbakeføringshandling

| Dato      | transaksjonstype                | Beløp    |
|-----------|---------------------------------|-----------|
| 1. januar | Tilbakeføring av anskaffelsesjustering | -1 000,00 |

#### <a name="depreciation-effect"></a>Avskrivningseffekt

| Dato        | transaksjonstype        | Beløp                                                                                |
|-------------|-------------------------|---------------------------------------------------------------------------------------|
| 28. februar | Avskrivning (forslag) | 983,05Beregning: Bokført verdi (59 000 - 1 000 avskrivning) / Antall gjenværende avskrivningsperioder (59) |

Avskrivningen er overvurdert med 16,95 (1 000 - 983,05).

## <a name="example-2-depreciation-is-understated"></a> Eksempel 2: Avskrivning undervurdert
Et anleggsmiddelet er definert med 5 års levetid og lineær avskrivning (60 avskrivningsperioder). I dette eksemplet er avskrivningen undervurdert.
#### <a name="asset-transaction-history"></a>Transaksjonshistorikk for anleggsmiddel

| Dato       | transaksjonstype                                                          | Beløp                                      |
|------------|---------------------------------------------------------------------------|---------------------------------------------|
| 1. januar  | Anskaffelse                                                               | 59 000,00                                   |
| 1. januar  | Skriv ned justering                                                     | 1 000,00                                    |
| 31. januar | Avskrivning (opprettet ved bruk av forslag for én avskrivningsperiode) | 966,67Beregning: Bokført verdi (59 000 - 1 000) / Antall gjenværende avskrivningsperioder (60) |

#### <a name="reversal-action"></a>Tilbakeføringshandling

| Dato      | transaksjonstype               | Beløp    |
|-----------|--------------------------------|-----------|
| 1. januar | Tilbakeføring av nedskrivingsjustering | -1 000,00 |

#### <a name="depreciation-effect"></a>Avskrivningseffekt

| Dato        | transaksjonstype        | Beløp                                                                                       |
|-------------|-------------------------|----------------------------------------------------------------------------------------------|
| 28. februar | Avskrivning (forslag) | 983,62Beregning: Bokført verdi (59 000 - 966,67 avskrivning) / Antall gjenværende avskrivningsperioder (59) |

Avskrivningen er undervurdert med 16,95 (983,62 - 966,67).



<a name="additional-resources"></a>Tilleggsressurser
--------

[Avskrivning av anleggsmiddel](fixed-asset-depreciation.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]