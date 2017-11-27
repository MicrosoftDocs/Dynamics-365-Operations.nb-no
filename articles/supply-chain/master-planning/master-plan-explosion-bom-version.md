---
title: Nedbryting av en stykklisteversjon
description: Denne artikkelen beskriver et scenario som involverer nedbrytingen av en stykklisteversjon (BOM) for hovedplanlegging.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqTransExplosion
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19211
ms.assetid: fe08c2e6-9cc5-4e34-bbb2-cd07843403b5
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 0f852c8d100c91d055e58c4594106aedf6fe5afb
ms.contentlocale: nb-no
ms.lasthandoff: 11/03/2017

---

# <a name="explosion-of-a-bom-version"></a>Nedbryting av en stykklisteversjon

[!include[banner](../includes/banner.md)]


Denne artikkelen beskriver et scenario som involverer nedbrytingen av en stykklisteversjon (BOM) for hovedplanlegging.

En vellykket behovsnedbrytning av en stykklisteversjon resulterer i et behov for hver stykklistelinjevare på et bestemte område eller muligens ved et bestemt lager. For en områdespesifikk stykkliste kan det være definert et bestemt lager for hver stykklistelinje. Varens dimensjonsinnstillinger angir dessuten om lageret er påkrevd for hver stykklistelinje. Det resulterende behovet for hver stykklistelinje blir deretter utgangspunktet for en ytterligere behovsnedbrytning. Dette hovedplanleggingsscenariet omfatter følgende betingelser:

-   Områdedimensjonen er obligatorisk, og må angis på behovstransaksjonen.
-   Områdedimensjonen er konsekvent. Området for behovet på lavere nivå, er derfor det samme som området på den innledende behovstransaksjonen.

Illustrasjonen nedenfor viser hvordan behovsnedbrytningen for hovedplanlegging foregår. ![Behovsnedbryting ved hjelp av stykklisteversjon](./media/multisitedemandexplosionscenariousingbomversion.gif)

<a name="see-also"></a>Se også
--------

[Hovedplanlegging – hvordan stykklisteversjon fastsettes](master-plan-bom-version-determined.md)

[Hovedplanlegging og multisite-funksjonalitet](master-plan-multisite-functionality.md)




