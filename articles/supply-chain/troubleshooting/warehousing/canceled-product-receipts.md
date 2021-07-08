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
ms.openlocfilehash: 9c86457d50a7a9ac2a699a0e0a9c7bdf4cd7c67b
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294144"
---
# <a name="canceled-product-receipts-dont-update-transaction-status-to-registered"></a>Annullerte produktmottak oppdaterer ikke transaksjonsstatusen til Registrert

## <a name="symptoms"></a>Symptomer

Når du har kjørt handlingen **Avbryt produktmottak** for en innkommende last, oppdaterer systemet automatisk lagertransaksjonsstatusen fra *Mottatt* til *Bestilt*.

## <a name="resolution"></a>Løsning

Når følgesedler annulleres for utgående belastninger, forblir statusen for lagertransaksjoner *Plukket*. Når produktmottak fra en innkommende last annulleres, vil imidlertid statusen for lagertransaksjoner som gjenopprettes, ikke gjenopprettes til *Registrert*. Når et produktmottak fra en innkommende last er annullert, må derfor lagerarbeideren registrere vareantallet på nytt for lasten.

Hvis du vil ha mer informasjon, kan du se [Registrere vareantall som ankommer for en innkommende last](/dynamics365/supply-chain/warehousing/inbound-load-handling#register-item-quantities-arriving).
