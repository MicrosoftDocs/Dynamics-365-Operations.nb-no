---
title: Metoder for utsettelsespostering
description: Denne artikkelen beskriver forskjellen på metodene for utsettelsespostering for inntekts- og utgiftsutsettelse i abonnementsfakturering.
author: JodiChristiansen
ms.date: 6/10/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: c66ed1c38251140dd798c39797873ceb5f7121a4
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/15/2022
ms.locfileid: "9019100"
---
# <a name="deferral-posting-methods"></a>Metoder for utsettelsespostering

Denne artikkelen beskriver forskjellen på metodene for utsettelsespostering for inntekts- og utgiftsutsettelse i abonnementsfakturering.

Alternativene for metoder for utsettelsespostering på siden **Parametere for inntekts- og utgiftsutsettelse** er **Balanse** og **Resultat**. Eksemplet i denne artikkelen bidrar til å forklare forskjellen på de to metodene og grunnene til å velge den ene eller andre metoden.

Metoden **Balanse** bruker bare to kontoer. Mindre konfigurasjon er derfor involvert. Metoden **Resultat** har to ytterligere kontoer, **Opprinnelig føring** og **Motkonto for føring**, for inntekt, rabatter og kostnader, avhengig av transaksjonstypen. Disse kontoene konfigureres på siden **Standarder for utsettelse** (**Abonnementsfakturering \> Inntekts- og utgiftsutsettelser \> Oppsett**). Selv om eksemplet fokuserer på utsatt inntekt, kan det samme konseptet brukes på utsatte rabatter og utsatte kostnader.

## <a name="example"></a>Eksempel

Salgsfaktura 1 har et totalbeløp på USD 3000 og utsatt inntekt. Tabellene nedenfor viser distribusjonene når denne salgsfakturaen posteres.

**Metoden Balanse**

| Type | Konto | Debet | Kreditt|
|---|---|---|---|
| Debet | Kundereskontro | 3,000.00 | |
| Kreditt | Utsatt inntekt | | 3,000.00 |

**Metoden Resultat**

| Type | Konto | Debet | Kreditt |
|---|---|---|---|
| Debet | Kundereskontro | 3,000.00 | |
| Debet | Motregnet inntektsføring | 3,000.00 | |
| Kreditt | Utsatt inntekt | | 3,000.00 |
| Kreditt | Opprinnelig inntektsføring | | 3,000.00 |

Salgsfaktura 2 har et totalbeløp på USD 2000 og ikke utsatt inntekt.

| Type | Konto | Beløp |
|---|---|---|
| Debet | Kundereskontro | 3,000.00 |
| Kreditt | Inntekt | 3,000.00 |

**Totalbeløpene for metoden Balanse for salgsfaktura 1 og 2 kombinert**

| Konto | Debet | Kreditt |
|---|---|---|
| Kundereskontro | 5 000,00 | |
| Inntekt | | 2,000.00 |
| Utsatt inntekt | | 3,000.00 |

Når metoden **Balanse** brukes, er det ikke enkelt å se bruttoinntektene for en periode. Noe av inntekten posteres i kontoen **Utsatt inntekt**. Husk at når inntekten føres i hver periode, forekommer det flere debiteringer og krediteringer på kontoen **Utsatt inntekt**. Bruttoinntekten for en gitt periode blandes med inn-/utgående inntektsføring.

**Totalbeløpene for metoden Resultat for salgsfaktura 1 og 2 kombinert**

| Konto | Debet | Kreditt |
|---|---|---|
| Kundereskontro | 5 000,00 | |
| Inntekt | | 5 000,00 |
| Inntektsmotkonto | 3,000.00 | |
| Utsatt inntekt | | 3,000.00 |

All inntekt går til resultatkontoen **Inntekt**. Deretter flyttes den utsatte inntekten fra resultatregnskapet til balansen. Du kan lett se bruttoinntekten siden alt posteres på **Inntekt**-kontoen. En del av denne bruttoinntekten blir imidlertid utsatt. Den flyttes derfor til kontoen **Utsatt inntekt** og føres senere.

Du kan se på kontoene **Inntekt** og **Inntektsmotkonto** i metoden **Resultat** for å se bruttoinntekten på USD 5000 og nettoinntekten (netto av utsatt) på USD 2000. Selv om metoden **Resultat** kan gjøre rapporteringen enklere, er det flere kontoer å konfigurere.
