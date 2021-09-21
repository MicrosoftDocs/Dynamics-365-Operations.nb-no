---
title: Stykklistenedbrytning fungerer ulikt for autoriserte og estimerte produksjonsordrer
description: Stykklistenedbrytning er forskjellig for autoriserte produksjonsordrer og for estimerte produksjonsordrer for manuelt opprettet arbeid
author: ChristianRytt
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 94d4b00ea30396923a61b2748cf1aaeedc0af8af
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477197"
---
# <a name="bom-explosion-behaves-differently-for-firmed-and-estimated-production-orders"></a>Stykklistenedbrytning fungerer ulikt for autoriserte og estimerte produksjonsordrer

## <a name="symptoms"></a>Symptomer

Når en produksjonsordre blir autorisert, blir ikke varene nedbrutt når du deler opp stykklisten. Når du oppretter en arbeidsordre manuelt og deretter estimerer produksjonsordren, deles imidlertid varene opp.

### <a name="resolution"></a>Løsning

Nedbrytingen som skjer når produksjonsordren autoriseres, vil peke mot den planlagte ordren, men den viser ikke at den planlagte ordren for øyeblikket er autorisert i dette tilfellet. Hvis imidlertid produksjonsordren er estimert, utløses nedbrytingen fra den frigitte produksjonsordren der det ikke finnes noen planlagt ordre.
