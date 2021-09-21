---
title: Kan ikke velge endring i lagerstatus som Arbeidstype
description: Du kan ikke opprette en arbeidsmallinje for lagerstatusendring, fordi arbeidstypen bare brukes av systemprosesser. Velg en annen arbeidstype.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: ad7f26f3235d15779583f9cdadeb4e6dca16242a
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477234"
---
# <a name="cant-select-inventory-status-change-in-the-work-type-column"></a>Kan ikke velge endring i lagerstatus i kolonnen Arbeidstype

## <a name="symptoms"></a>Symptomer

Når du konfigurerer Microsoft Dynamics 365 Supply Chain Management, kan du få følgende feilmelding:

> Du kan ikke opprette en arbeidsmallinje for lagerstatusendring, fordi arbeidstypen ikke er gyldig. Velg en annen arbeidstype.

## <a name="resolution"></a>Løsning

Denne virkemåten er standard. Arbeidstypen *Lagerstatusendring* brukes bare av systemprosesser. Den kan ikke konfigureres. Fordi listen over arbeidstyper er fast som en opplisting, kan ikke de ekstra postene filtreres ut fra rullegardinmenyen **Arbeidstype**.
