---
title: Tilordne dimensjonsmedlemmer for kostnadselement til et felles sett med dimensjonsmedlemmer
description: Ved tilordning av forskjellige medlemmer av kostnadselementdimensjon til et felles sett med medlemmer av kostnadselementdimensjoner, slår du sammen data i et felles format for analyseformål.
author: AndersGirke
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CAMDimension, CAMDimensionMember, CAMDimensionMapping
audience: Application User
ms.reviewer: twheeloc
ms.custom: 223234
ms.assetid: 4c66a231-aed2-48b5-9727-b3eb4fe6e6aa
ms.search.region: global
ms.author: twheeloc
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 7654f748fb0cfc70d76718f03a235c5d4d13a908
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/10/2022
ms.locfileid: "8735471"
---
# <a name="map-cost-element-dimension-members-to-a-common-set-of-dimension-members"></a>Tilordne dimensjonsmedlemmer for kostnadselement til et felles sett med dimensjonsmedlemmer

[!include [banner](../includes/banner.md)]

Ved tilordning av forskjellige medlemmer av kostnadselementdimensjon til et felles sett med medlemmer av kostnadselementdimensjoner, slår du sammen data i et felles format for analyseformål.

Hvis du er et globalt selskap og overholder lovbestemte regnskapsmessige krav, kan du bruke flere kontoplaner. Når du importerer medlemmer av kostnadelementdimensjoner fra ulike kontoplaner, kan du ende opp med en blanding av kontoer. Disse kontoene har imidlertid faktisk samme egenskap, og du vil kanskje analysere og fordele kostnader for dem ved hjelp av et felles format.

## <a name="map-cost-element-dimension-members-to-a-common-format"></a>Tilordne medlemmer av kostnadelementdimensjoner til et vanlig format
Eksemplet nedenfor viser hvordan du, som kostnadskontrollør, kan opprette en ny kostnadselementdimensjon i kostnadsregnskap som tilordner medlemmer av kostnadelementdimensjoner fra den amerikanske og franske kontoplanstrukturen til et felles sett med medlemmer av kostnadelementdimensjoner. Du kan deretter bruke det felles settet med medlemmer av kostnadelementdimensjoner til å analysere kostnadsdata fra de to juridiske enhetene i en finanskonto for kostnadsregnskap.

| Kilde: amerikansk kontoplanstruktur          | Kilde: fransk kontoplanstruktur           | Nytt felles sett med medlemmer av kostnadelementdimensjoner                        |
|------------------------------------|----------------------------------------------|-------------------------------------------------------------------------|
| Importerte medlemmer av kostnadelementdimensjoner fra den amerikanske kontoplanen | Importerte medlemmer av kostnadelementdimensjoner fra den franske kontoplanen | Tilordning av amerikanske og fransk medlemmer av kostnadselementdimensjoner til et felles sett |
| 5001: Salg                   | 5001: Salg og markedsføring                      | 5000: Salg og markedsføring                               |
| 5030: Reklame             | 6390: Lagerinnkjøp\*                          | 7000: Renholdsutgifter                                   |
| 7001: Renholdsutgifter              | 7001: Reiseutgifter                     | 7001: Reiseutgifter                                                   |

\*Lagerinnkjøp for franske medlem av kostnadselementdimensjon er ikke tilordnet.

## <a name="currency-conversion"></a>Valutaomregning
De ulike kontoplanene som du bruker, kan være konfigurert til å bruke ulike valutaer. I så fall må du huske å angi en valutaomregning, slik at kostnadsdata behandles ved hjelp av riktig valuta, som definert i kostnadsregnskapsfinans der medlemmene av kostnadselementdimensjonen er brukt. Hvis Amerikanske dollar (USD) brukes i kostnadsregnskapsfinans i eksemplet ovenfor, må du opprette en valutaomregning fra USD til euro (EUR) for å behandle transaksjoner for de tilordnede medlemmene av kostnadselementdimensjonen.

## <a name="update-mappings-at-any-time"></a>Oppdater tilordninger når som helst
Du kan oppdatere tilordningsdefinisjonene for en kostnadselementdimensjon når som helst. Siden tilordningene ikke er datoeffektive, brukes endringene neste gang du behandler kostnadstransaksjoner eller kjøre kostnadsberegninger.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
