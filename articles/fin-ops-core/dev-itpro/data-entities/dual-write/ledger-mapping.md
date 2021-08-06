---
title: Integrert finans
description: Dette emnet beskriver integreringen av finansdata mellom Finance and Operations og andre Dynamics 365-programmer ved bruk av Dataverse.
author: robinarh
ms.date: 09/06/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: rhaertle
ms.openlocfilehash: 9e6e65b2b8ec8241bc2082b30ae641692c31afdd
ms.sourcegitcommit: f65bde9ab0bf4c12a3250e7c9b2abb1555cd7931
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/13/2021
ms.locfileid: "6542667"
---
# <a name="integrated-ledger"></a>Integrert finans

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

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
