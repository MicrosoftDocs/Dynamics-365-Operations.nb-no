---
title: Det skrives bare ut én etikett for flere arbeidshoder i en enkelt kvittering
description: Det skrives bare ut én etikett for flere arbeidshoder i en enkelt kvittering.
author: perlynne
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WHSLicensePlateLabel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 8e11dc918eb3c9085018d15b43819522cc8bebe3
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026778"
---
# <a name="only-one-label-is-printed-for-multiple-work-headers-on-a-single-receipt"></a>Det skrives bare ut én etikett for flere arbeidshoder i en enkelt kvittering

KB-nummer: 4614667

## <a name="symptoms"></a>Symptomer

Flere arbeidshoder opprettes for samme målnummerskilt som del av en enkelt lagerappmottakshendelse. Det skrives imidlertid bare ut én lisensetikett når produktet mottas.

## <a name="resolution"></a>Oppløsning

Systemet fungerer som tiltenkt.

I den gjeldende utformingen genereres det alltid én enkelt lisensetikett, uansett hvor mange arbeidshode- og arbeidslinjekombinasjoner som finnes. Den genererte etiketten inneholder informasjon for bare én kombinasjon.

Du kan omgå dette problemet ved å sørge for at oppretting av arbeidshode alltid er tilordnet til bare én lisensavtale.
