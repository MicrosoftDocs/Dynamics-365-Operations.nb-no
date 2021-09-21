---
title: Mottak av kombinerte nummerskilter virker ikke for alle disposisjonskoder
description: Når Handling-feltet for en disposisjonskode er satt til Kredit eller Svinn, kan du bare bruke menyelementet Mottak av kombinerte nummerskilter til å behandle returnerte varer.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: b762255bc5ef6a1e15688a9c635940e92e67db3c
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477225"
---
# <a name="mixed-license-plate-receiving-doesnt-work-for-any-disposition-code-but-credit"></a>Mottak av kombinerte nummerskilter virker ikke for noen disposisjonskode, bortsett fra Kreditt

## <a name="symptoms"></a>Symptomer

Når **Handling**-feltet for en disposisjonskode er satt til *Kredit* eller *Svinn*, kan du bare bruke menyelementet [Mottak av kombinerte nummerskilter](/dynamics365/supply-chain/warehousing/mixed-license-plate-receiving) til å behandle returnerte varer.

## <a name="resolution"></a>Løsning

Microsoft har evaluert dette problemet og har funnet ut at det er en funksjonsbegrensning. For øyeblikket er det bare [disposisjonskoder](/dynamics365/supply-chain/service-management/set-up-disposition-codes) der **Handling**-feltet er satt til *Kredit* eller *Svinn*, som støttes for mottak av kombinerte nummerskilter.
