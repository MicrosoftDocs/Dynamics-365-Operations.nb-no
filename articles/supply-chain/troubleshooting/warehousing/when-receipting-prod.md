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
ms.openlocfilehash: cf307964a07c2b69eb5e4ef2cf9dc094482736d0970e333e84f674c9be6331c7
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6740533"
---
# <a name="only-one-label-is-printed-for-multiple-work-headers-on-a-single-receipt"></a>Det skrives bare ut én etikett for flere arbeidshoder i en enkelt kvittering

KB-nummer: 4614667

## <a name="symptoms"></a>Symptomer

Flere arbeidshoder opprettes for samme målnummerskilt som del av en enkelt lagerappmottakshendelse. Det skrives imidlertid bare ut én lisensetikett når produktet mottas.

## <a name="resolution"></a>Oppløsning

Systemet fungerer som tiltenkt.

I den gjeldende utformingen genereres det alltid én enkelt lisensetikett, uansett hvor mange arbeidshode- og arbeidslinjekombinasjoner som finnes. Den genererte etiketten inneholder informasjon for bare én kombinasjon.

Du kan omgå dette problemet ved å sørge for at oppretting av arbeidshode alltid er tilordnet til bare én lisensavtale.
