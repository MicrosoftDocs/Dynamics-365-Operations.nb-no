---
title: Lagerantallet kan ikke oppdateres på grunn av utilstrekkelige transaksjoner
description: Lagerantall -1 % kan ikke oppdateres fordi det ikke finnes nok lagertransaksjoner for vare %2 som har de angitte dimensjonene.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 88130a969039dd741c8ea4fbaabe81acf0e6fb6a
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477151"
---
# <a name="system-cant-update-inventory-quantity-because-of-insufficient-transactions"></a>Systemet kan ikke oppdatere lagerantall på grunn av utilstrekkelige transaksjoner

## <a name="symptoms"></a>Symptomer

Dette problemet kan oppstå hvis systemet ikke kan oppdatere et lagerantall, fordi det ikke finnes nok lagertransaksjoner som har de angitte dimensjonene. Du får følgende feilmelding:

> Lagerantall -%1 kan ikke oppdateres på grunn av utilstrekkelige lagertransaksjoner for varen %2 med dimensjonsstørrelse = %3, farge = %4, tillegg = %5, område = %6, lager = %7, lokasjon = %8, lagerstatus = tilgjengelig, nummerskilt = %9, partinummer = %10 for referanse-ID %11 på parti-ID %12.

## <a name="resolution"></a>Løsning

Kontroller at ingen lagertransaksjoner fysisk reserverer antallet. Disse transaksjonene kan for eksempel åpne kvalitetsordrer, lagerblokkeringsposter eller ordrer.
