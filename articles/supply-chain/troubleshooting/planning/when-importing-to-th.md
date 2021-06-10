---
title: Du blir bedt om å lagre varedekningsinnstillinger selv om du ikke har gjort noen endringer
description: Du blir bedt om å lagre varedekningsinnstillinger selv om du ikke har gjort noen endringer.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: DataManagementWorkspace_
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: angarmas
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 3dfa974740420433af1e1b37630b22509510c91b
ms.sourcegitcommit: 3c15a26e9708adc9a75082dc551f0a3a0a7d89f4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/17/2021
ms.locfileid: "6049482"
---
# <a name="youre-prompted-to-save-item-coverage-settings-even-though-you-made-no-changes"></a>Du blir bedt om å lagre varedekningsinnstillinger selv om du ikke har gjort noen endringer

KB-nummer: 4615588

## <a name="symptoms"></a>Symptomer

I noen scenarier kan det hende at du får følgende melding når du åpner siden **Varedekning** etter at du har importert varer via enheten *Varedekning V2*:

> Vil du lagre endringer før du lukker?

Du får denne meldingen selv om du ikke har gjort noen endringer.

## <a name="resolution"></a>Løsning

**Varedekning**-siden inneholder kompleks standardlogikk som kan føre til at meldingen vises etter at det nylig er gjort direkte endringer i databasen, for eksempel gjennom enhetsimport. Enhetsfeltet `AREGENERALSETTINGSOVERRIDDEN` er for eksempel satt til *Nei*, men du importerer en fil som inneholder nye eller endrede verdier for felt som for eksempel `PRODUCTCOVERAGEGROUPID` og/eller `VENDORACCOUNTNUMBER`. I dette tilfellet, fordi feltet `AREGENERALSETTINGSOVERRIDDEN` er satt til *Nei*, tømmes verdiene automatisk fra feltene når du åpner **Varedekning**-siden for første gang etter importen. Hvis du lagrer endringene som meldingsboksledetekst, lagres de i databasen. Ellers får du samme melding neste gang du åpner siden.

Hvis du vil hindre denne virkemåten, men også ta med verdier for felt som `PRODUCTCOVERAGEGROUPID` gjennom enhetsimport, kan du sette `AREGENERALSETTINGSOVERRIDDEN` til *Ja* når du importerer.
