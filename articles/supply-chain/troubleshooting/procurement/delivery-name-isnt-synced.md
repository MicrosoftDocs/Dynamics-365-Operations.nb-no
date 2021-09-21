---
title: Etter å ha endret en leveringsadresse for en bestilling, blir ikke leveringsnavnet synkronisert
description: Etter at du endret leveringsadressen i et bestillingshode, blir ikke leveringsnavnet synkronisert
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 588d1ef6250d249aa4fc9da4f5125e9a34c0255f
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477168"
---
# <a name="the-delivery-name-isnt-synced-after-changing-a-purchase-order-delivery-address"></a>Etter å ha endret en leveringsadresse for en bestilling, blir ikke leveringsnavnet synkronisert

## <a name="symptoms"></a>Symptomer

Adressen på hodet til en bestilling oppdateres til en adresse som ikke er en leveringsadresse. Selv om adressen oppdateres på bestillingen, oppdateres ikke leveringsnavnet basert på den oppdaterte adressen.

## <a name="resolution"></a>Løsning

Denne virkemåten er standard. Den valgte adressen må klassifiseres som leveringsadresse. Hvis ikke oppdateres ikke leveringsnavnet basert på den valgte adressen.
