---
title: Nedbryting av en stykklisteversjon
description: Denne artikkelen beskriver et scenario som involverer nedbrytingen av en stykklisteversjon (BOM) for hovedplanlegging.
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ReqTransExplosion
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19211
ms.assetid: fe08c2e6-9cc5-4e34-bbb2-cd07843403b5
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 6461a07f8c8f02f584e5ef70b21ebaf04f29b57b
ms.lasthandoff: 03/31/2017


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



