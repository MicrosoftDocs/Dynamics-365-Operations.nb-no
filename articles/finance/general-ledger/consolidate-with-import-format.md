---
title: Importformat for konsolidering
description: Dette emnet gir detaljert informasjon om importformatet som brukes når du konsoliderer økonomiske data fra flere juridiske enheter.
author: jinniew
manager: AnnBe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2018-5-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: a8ba65ecc27bb152b1b368e870b15544d9599968
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4978542"
---
# <a name="import-format-for-consolidation"></a>Importformat for konsolidering

[!include [banner](../includes/banner.md)]

Dette emnet gir detaljert informasjon om importformatet som brukes når du konsoliderer økonomiske data fra flere juridiske enheter. Importformatet må lagres som en tekstfil (.txt).

## <a name="import-format"></a>Importformat

Tabellen nedenfor viser et importformat du bør bruke når du gjør en konsolidering under en import.

| Posttabell | Format | Notater |
|--------------|---------|-------|
| 1            | 170150, Goodwill, 4 | <ul><li>Posttabellen</li><li>Hovedkonto-IDen for kilden</li><li>Hovedkontolinjen</li><li>Hovedkontotypen</li></ul> |
| 2            | 110130, 2015/01/01, 1, USD, 0,0,80699.39,0,1 | <ul><li>Hovedkonto-IDen</li><li>Transaksjonsdatoen</li><li>Regnskapsperiodetypen (**0** = Åpning, **1** = Drift og **2** = Lukking)</li><li>Transaksjonsvalutaen</li><li>Debet eller kredit (**0** = debet og **1** = kredit)</li><li>Posteringslaget</li><li>Transaksjonsbeløp</li><li>Antall</li><li>Lokal RecID (tvetydig, unik int64-verdi for transaksjonen)</li></ul> |
| 3            | USMF0000009, 2017/01/01, FY2017, 1, 2017,01,01, 602200, USD, 6053.6.0 | <ul><li>Oppføringsnummeret (budsjethodetransaksjonsnummer)</li><li>Standarddatoen for budsjetthodet</li><li>Budsjettmodell-IDen</li><li>Heltallsverdien for opplisting for transaksjonstypen (tom, opprinnelig budsjett og så videre)</li><li>Datoen for linjen</li><li>Hovedkonto-IDen for linjen</li><li>Valutakoden for linjen</li><li>Beløpet for linjen, i transaksjonsvalutaen</li><li>Heltallsverdien for opplisting for budsjetttypen for linjen (utgift eller inntekt)</li></ul> |
| 4            | DEMF | RecordCompany er den juridiske kildeenheten. |
| 5            | 110130, 2015/01/01, 1, USD, 0,0,80699.39,0,1 | RecordCompany er den juridiske kildeenheten. |
| 6            | BusinessUnit, 1 Avdeling, 2 | Finansdimensjonsattributtene som er definert i segmentrekkefølgen.<p>Du kan bruke **Eksport**-sidenn til å kontrollere hvordan attributtene er definert.</p> |
| 7            | 002,1,658 | <ul><li>Finansdimensjonsverdien</li><li>Finansdimensjonen, som indeksen som angis i RecordDimensions</li><li>En tvetydig, unik post-ID som er knyttet til den unike post-IDen fra RecordTrans eller RecordTrans2</li></ul> |
| 8            | 002,1,1 | <ul><li>Dimensjonsverdier som er knyttet til transaksjonen fra RecordBudget</li><li>Finansdimensjonen, som indeksen som angis i RecordDimensions</li><li>En tvetydig linjepost-ID som justeres etter rekkefølgen til transaksjonslinjene i filen</li></ul> |
