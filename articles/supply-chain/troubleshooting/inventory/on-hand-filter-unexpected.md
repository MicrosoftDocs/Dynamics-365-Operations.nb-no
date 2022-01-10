---
title: Filterruten på lagerlistesiden fungerer ikke som forventet
description: Filtrene i filterruten på siden Beholdningsliste filtrerer ikke resultater slik du forventer.
author: sherry-zheng
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 2b2b233e22378c8710a63dce83d168bfd89eba7f
ms.sourcegitcommit: 008779c530798f563fe216810d34b2d56f2c8d3c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/14/2021
ms.locfileid: "7920504"
---
# <a name="the-filter-pane-on-the-on-hand-list-page-doesnt-work-as-expected"></a>Filterruten på lagerlistesiden fungerer ikke som forventet

## <a name="symptoms"></a>Symptomer

Filtrene i filterruten på siden **Beholdningsliste** filtrerer ikke resultater slik du forventer.

## <a name="resolution"></a>Løsning

Siden **Beholdningsliste** er satt sammen fra en detaljert lagerbeholdningstabell som inkluderer alle tilgjengelige dimensjoner. Listen på denne siden er imidlertid et sammendrag. Derfor kan den kombinere rader fra kildetabellen ved å samle verdier i henhold til dimensjonene som vises.

Filtre som er definert i filterruten, gjelder for kildetabellen, ikke for den aggregerte listen. Denne virkemåten kan av og til gi uventede resultater, som vist i [disse eksemplene](/dynamics365/supply-chain/inventory/inventory-on-hand-list.md#examples).

[Filtrene som oppgis i rutenettet](/dynamics365/supply-chain/inventory/inventory-on-hand-list.md#grid-filters), *gjelder* imidlertid for den aggregerte listen. Disse filtrene inkluderer både hurtigfilteret øverst i rutenettet og filteret for hver kolonneoverskrift.
