---
title: Integrert finans
description: Denne artikkelen beskriver integreringen av finansdata mellom Finance and Operations og andre Dynamics 365-programmer ved bruk av Dataverse.
author: RamaKrishnamoorthy
ms.date: 09/06/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 728c131c260586e7f1f787f22ccf02ed81c94c01
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289156"
---
# <a name="integrated-ledger"></a>Integrert finans

[!include [banner](../../includes/banner.md)]



I et forretningsprogram definerer finansdata kjerneoppsettet for hvordan et firma gjør forretninger. Finansdata beskriver for eksempel regnskapsåret firmaet følger, transaksjonsvalutaene og kontoene det bruker. Denne artikkelen beskriver integreringen av disse finansielle dataene.

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

