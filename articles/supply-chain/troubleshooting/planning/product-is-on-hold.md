---
title: Produktet er på vent for transaksjoner
description: Når du har autorisert planleggingsordrer, får du en feilmelding som angir at en vare er sperret for transaksjoner.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 6654e6437a088218db116b955631be4c7e62de5f
ms.sourcegitcommit: f9b145ef4a81cec81f420871b4130b05db4f4500
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/23/2021
ms.locfileid: "6301285"
---
# <a name="product-is-on-hold-for-transactions"></a>Produktet er på vent for transaksjoner

Feilkode: SYS13295

## <a name="symptoms"></a>Symptomer

Når du har autorisert ordrer, mottar du følgende feilmelding:

> Varen %1 er sperret for transaksjoner i %2.

## <a name="cause"></a>Årsak

Når blokkerte varer beskrives, bruker systemet termene *blokkert*, *stoppet* og *på vent* om hverandre. Denne feilen betyr at varen angis som **Stoppet** i standardordreinnstillingene.

Hvis en vare er sperret, og du legger den til i en bestilling eller salgsordrelinje, får du en advarsel. Når en vare er sperret, kan du ikke endre lagertransaksjoner som er knyttet til bestillings- eller salgsordrelinjen når du for eksempel posterer en følgeseddel eller en faktura. Du kan sperre en kjøpt vare og samtidig selge varen. I dette tilfellet er det merket av for **Stoppet** i en bestilling, men varen er ikke sperret på lager eller i en salgsordre.

Her er noen av betingelsene som kan føre til at et varenummer blir blokkert fra å bli solgt:

- Varen er fremdeles er under utvikling eller produksjon. Derfor ønsker du ikke at den skal selges eller reserveres.
- Du har mottatt mange mangelfulle varer, og defektene må korrigeres før varen kan selges.

I slike tilfeller kan du ikke sperre varen før problemet er løst.

Hvis en vare er sperret og du oppretter en returordrelinje, mottar du en melding. Du kan ikke sperre en serie eller et parti av en vare. Hvis deler av en vare må sperres, kan du gjøre det ved å flytte beholdningen eller ved å blokkere hele lagerbeholdningen av varen i dette tidsrommet.

## <a name="resolution"></a>Løsning

- Åpne siden **Standard ordreinnstillinger** for varen, og fjern merket for **Stoppet**.
