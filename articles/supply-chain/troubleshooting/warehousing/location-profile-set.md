---
title: Lokasjonsprofilen sperrer negativ beholdning, men negativ lagerbeholdning er tillatt
description: Alternativet Tillat negativ beholdning for lokasjonsprofilen er satt til Nei, men systemet tillater likevel negativ lagerbeholdning.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WHSLocationProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: shawan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 2a7345281301ee70a512dfadcd553cb4eb33003904d0dddf6967659b693f60d7
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6742614"
---
# <a name="location-profile-disallows-negative-inventory-but-negative-on-hand-inventory-is-permitted"></a>Lokasjonsprofilen sperrer negativ beholdning, men negativ lagerbeholdning er tillatt

KB-nummer: 4613622

## <a name="symptoms"></a>Symptomer

Alternativet **Tillat negativ beholdning** for lokasjonsprofilen er satt til *Nei*, men systemet tillater likevel negativ lagerbeholdning.

## <a name="example-scenario"></a>Eksempelscenario

For transaksjoner som er regulert av offentlige myndigheter, må systemet kunne registrere negativ beholdning for bokført tap. Du vil at en vare skal kunne vise negativ beholdning, men bare på angitte lokasjoner, for eksempel tanker. Hvis imidlertid varemodellgruppen tillater negativ beholdning, finner du ut at det ikke har noen betydning om lokasjonen er angitt til å tillate negativ beholdning. Hvis varen er konfigurert slik at negativ beholdning ikke er tillatt, har det ingen betydning hvordan lokasjonsprofilen er satt opp.

## <a name="resolution"></a>Oppløsning

Innstillingen **Tillat negativt lager** fra lokasjonsprofilen gjelder bare for lagerprosesser, for eksempel plukking. Men varemodellgrupper som er angitt for å tillate negativ beholdning, påvirker alle prosesser fra lagerstyrings- og lagerstyringsmodulene, og lokasjonsprofilen vil ikke overstyre innstillingen.

Du kan styre om et lager kan tillate negativt beholdning. Angi at varemodellgruppene skal sperre negativ fysisk beholdning, og angi bare relevant lager, slik at negativ beholdning tillates.
