---
title: Opprette en produktlivssyklustilstand for å utelukke produkter fra hovedplanlegging
description: Denne prosedyren viser hvordan du oppretter en ny produktlivssyklustilstand som utelukker produktene fra hovedplanlegging og beregning av stykklistenivå.
author: cvocph
manager: AnnBe
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 156972cdbf4ffb02b01b00972cc83d003d941378
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1567751"
---
# <a name="create-a-product-lifecycle-state-to-exclude-products-from-master-planning"></a>Opprette en produktlivssyklustilstand for å utelukke produkter fra hovedplanlegging

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne prosedyren viser hvordan du oppretter en ny produktlivssyklustilstand som utelukker produktene fra hovedplanlegging og beregning av stykklistenivå.


## <a name="create-an-obsolete-state"></a>Opprette en foreldet tilstand
1. Gå til Behandling av produktinformasjon > Oppsett > Livssyklustilstand for produkt.
2. Klikk Ny.
3. Skriv inn en verdi i feltet Tilstand.
4. Velg Nei i Er aktiv for planlegging-feltet.
5. Skriv inn en verdi i feltet Beskrivelse.

## <a name="associate-the-obsolete-state-to-a-released-product"></a>Knytte den utdaterte tilstanden til et frigitt produkt
1. Lukk siden.
2. Gå til Behandling av produktinformasjon > Produkter > Frigitte produkter.
3. Bruk hurtigfilteret for å søke etter poster. Du kan for eksempel filtrere på Søkenavn-feltet med verdien M00.
4. Klikk Rediger.
5. Merk den valgte raden i listen.
6. Angi eller velg en verdi i feltet Livssyklustilstand for produkt.

