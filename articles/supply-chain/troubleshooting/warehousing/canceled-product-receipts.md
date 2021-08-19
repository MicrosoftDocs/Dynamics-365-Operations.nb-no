---
title: Annullerte produktmottak oppdaterer ikke transaksjonsstatusen til Registrert
description: Når du har annullert produktmottak for en innkommende last, oppdaterer systemet automatisk lagertransaksjonsstatusen fra Mottatt til Bestilt.
author: GalynaFedorova
ms.date: 06/11/2021
ms.topic: troubleshooting
ms.search.form: WMSPickingRegistration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-06-11
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: eae703ce0b2c981518b18c4badd4f90031b902ece62f3ca0837427b306d618b1
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6731109"
---
# <a name="canceled-product-receipts-dont-update-transaction-status-to-registered"></a>Annullerte produktmottak oppdaterer ikke transaksjonsstatusen til Registrert

## <a name="symptoms"></a>Symptomer

Når du har kjørt handlingen **Avbryt produktmottak** for en innkommende last, oppdaterer systemet automatisk lagertransaksjonsstatusen fra *Mottatt* til *Bestilt*.

## <a name="resolution"></a>Løsning

Når følgesedler annulleres for utgående belastninger, forblir statusen for lagertransaksjoner *Plukket*. Når produktmottak fra en innkommende last annulleres, vil imidlertid statusen for lagertransaksjoner som gjenopprettes, ikke gjenopprettes til *Registrert*. Når et produktmottak fra en innkommende last er annullert, må derfor lagerarbeideren registrere vareantallet på nytt for lasten.

Hvis du vil ha mer informasjon, kan du se [Registrere vareantall som ankommer for en innkommende last](/dynamics365/supply-chain/warehousing/inbound-load-handling#register-item-quantities-arriving).
