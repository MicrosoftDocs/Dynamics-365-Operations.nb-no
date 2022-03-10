---
title: Integrert finans
description: Dette emnet beskriver integreringen av finansdata mellom Finance and Operations og andre Dynamics 365-programmer ved bruk av Dataverse.
author: tonyafehr
ms.date: 09/06/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: tfehr
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 0deb4198acb59b90bf06e4050889d028df2223e3
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/31/2022
ms.locfileid: "8063653"
---
# <a name="integrated-ledger"></a>Integrert finans

[!include [banner](../../includes/banner.md)]



I et forretningsprogram definerer finansdata kjerneoppsettet for hvordan et firma gjør forretninger. Finansdata beskriver for eksempel regnskapsåret firmaet følger, transaksjonsvalutaene og kontoene det bruker. Dette emnet beskriver integreringen av disse finansielle dataene.

## <a name="templates"></a>Maler

Finansdata inkluderer en samling tabelltilordninger for viktige finansområder som fungerer sammen under datasamhandling, som vist i følgende tabell.

Finance and Operations-apper | Kundeengasjementsapper     | beskrivelse
---------------------------------|----------------------------------|------------
[Valutakurser for CDS](mapping-reference.md#123) | msdyn_currencyexchangerates |
[Kontoplan](mapping-reference.md#121) | msdyn_chartofaccountses |
[Valutaer](mapping-reference.md#218) | transactioncurrencies |
[Valutapar for valutakurs](mapping-reference.md#122) | msdyn_currencyexchangeratepairs |
[Valutakurstype](mapping-reference.md#129) | msdyn_exchangeratetypes |
[Format for finansdimensjon](mapping-reference.md#130) | msdyn_financialdimensionformats |
[Finansdimensjoner](mapping-reference.md#128) | msdyn_dimensionattributes |
[Enhet for integrering av regnskapskalender](mapping-reference.md#132) | msdyn_fiscalcalendars |
[Økonomisk kalenderperiode](mapping-reference.md#131) | msdyn_fiscalcalendarperiods |
[Enhet for årsintegrering av regnskapskalender](mapping-reference.md#133) | msdyn_fiscalcalendaryears |
[Ledger](mapping-reference.md#148) | msdyn_ledgers |
[Hovedkonto](mapping-reference.md#152) | msdyn_mainaccounts |
[Hovedkontokategorier](mapping-reference.md#151) | msdyn_mainaccountcategories |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
