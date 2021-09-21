---
title: Du kan ikke til å konsolidere flere produktkvitteringer til én bestilling
description: Du kan ikke konsolidere flere produktkvitteringer i én enkelt bestilling hvis de ulike produktkvitteringslinjene har forskjellige regnskapsdatoer.
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
ms.openlocfilehash: 485306279281ceb55a140526f4216af35574af42
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477169"
---
# <a name="you-cant-consolidate-multiple-product-receipts-into-a-single-purchase-order"></a>Du kan ikke til å konsolidere flere produktkvitteringer til én bestilling

## <a name="symptoms"></a>Symptomer

Du kan ikke konsolidere flere produktkvitteringer i én enkelt bestilling hvis de ulike produktkvitteringslinjene har forskjellige regnskapsdatoer.

## <a name="resolution"></a>Løsning

I tidligere versjoner av Dynamics 365 Supply Chain Management var konsolidering tillatt i denne situasjonen. Dette er imidlertid utsatt for feil. Regnskapsdatoen på bestillingslinjene som opprettes, må ikke være forskjellige fra regnskapsdatoen på produktkvitteringslinjene som disse bestillingslinjene ble opprettet fra. (Regnskapsdatoen i bestillingslinjene samsvarer med regnskapsdatoen i bestillingshodet.) Derfor er ikke konsolideringen av flere produktkvitteringer i én enkelt bestillinger tillatt.

Regnskapsdatoen brukes for eksempel for budsjettreservasjoner og disposisjoner. Derfor bør den holdes i løpet av overgangen fra produktkvittering til bestilling.
