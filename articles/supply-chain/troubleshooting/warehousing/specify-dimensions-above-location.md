---
title: Kan ikke frigi en belastning for delvis antall med parti over hierarki
description: Når du bruker en vare med parti over reservasjonshierarki, må belastningslinjer angi dimensjoner over lokasjonen for at lageret skal tilordnes.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: eb7e71cc271903cb689c33777b72862246f2dd42
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477175"
---
# <a name="cant-release-a-load-for-partial-quantity-with-batch-above-reservation-hierarchy"></a>Kan ikke frigi en belastning for delvis antall med parti over reservasjonshierarki

## <a name="symptoms"></a>Symptomer

Når du bruker en vare som har et *parti-over*-reservasjonshierarki, fungerer ikke kommandoen **Frigi til lager** på siden **Arbeidsområde for lastplanlegging** hvis du prøver å frigi en last for en delvis mengde. Du får følgende feilmelding:

> For å tilordne bølge må lastlinjer angi dimensjonene over lokasjonen. Hvis du vil tilordne disse dimensjonene, må du reservere og opprette lastlinjen på nytt.

Når du imidlertid bruker en vare som har et *parti-under*-reservasjonshierarki, kan du frigi en last for en delvis mengde fra siden **Arbeidsområde for lastplanlegging**.

## <a name="cause"></a>Årsak

Når en dimensjon er over **Lokasjon**-dimensjonen i reservasjonshierarkiet, må den angis før frigivelse til lageret. Beholdningen kan bare tilordnes hvis det ikke er noen huller i dimensjonene over lokasjonen.

## <a name="resolution"></a>Løsning

Kontroller at alle dimensjoner over **Lokasjon** er tilordnet ved å reservere og opprette belastningslinjen på nytt.
