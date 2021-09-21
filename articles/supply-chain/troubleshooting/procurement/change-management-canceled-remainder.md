---
title: Hvis du avbryter leveringsresten, flyttes bestillingen til bekreftet status
description: Hvis en leveringsrest blir annullert på en bestilling der endringsstyring er aktivert, går bestillingen til en bekreftet status
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
ms.openlocfilehash: 1d8b331bc5699487dff3491d65daa36293f3212f
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477212"
---
# <a name="cancelling-delivery-remainder-moves-purchase-order-to-a-confirmed-state"></a>Hvis du avbryter leveringsresten, flyttes bestillingen til bekreftet status

## <a name="symptoms"></a>Symptomer

For en bestilling som er underlagt endringsstyring, hvis den eneste endringen som blir forespurt, er annullering av en leveringsrest på én eller flere av linjene, vil bestillingen gå direkte til en *Bekreftet* tilstand når den er godkjent, og det vil ikke bli opprettet noen journal.

## <a name="resolution"></a>Løsning

Annullering av en leveringsrest påvirker ikke innholdet i bekreftelsesjournalen. Denne funksjonaliteten bør brukes når linjen er delvis mottatt, og den gjenværende kvaliteten skal avbrytes i prosesstrinnet etter at bestillingen er bekreftet hos leverandøren.

Hvis dette skal reflekteres på bestillingsbekreftelsen, skal antallet justeres på bestillingslinjen slik at bekreftelsen blir nødvendig. Hvis det ikke er mottatt noe på linjen, kan du eventuelt fjerne antallet. I dette tilfellet kreves det en bekreftelse på nytt.
