---
title: Nedbryting av en stykklisteversjon
description: Denne artikkelen beskriver et scenario som involverer nedbrytingen av en stykklisteversjon (BOM) for hovedplanlegging.
author: roxanadiaconu
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransExplosion
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19211
ms.assetid: fe08c2e6-9cc5-4e34-bbb2-cd07843403b5
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 482c036294f525be5db1dc6efefe76a9ba5b3ce5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4434645"
---
# <a name="explosion-of-a-bom-version"></a>Nedbryting av en stykklisteversjon

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver et scenario som involverer nedbrytingen av en stykklisteversjon (BOM) for hovedplanlegging.

En vellykket behovsnedbrytning av en stykklisteversjon resulterer i et behov for hver stykklistelinjevare på et bestemte område eller muligens ved et bestemt lager. For en områdespesifikk stykkliste kan det være definert et bestemt lager for hver stykklistelinje. Varens dimensjonsinnstillinger angir dessuten om lageret er påkrevd for hver stykklistelinje. Det resulterende behovet for hver stykklistelinje blir deretter utgangspunktet for en ytterligere behovsnedbrytning. Dette hovedplanleggingsscenariet omfatter følgende betingelser:

-   Områdedimensjonen er obligatorisk, og må angis på behovstransaksjonen.
-   Områdedimensjonen er konsekvent. Området for behovet på lavere nivå, er derfor det samme som området på den innledende behovstransaksjonen.

Illustrasjonen nedenfor viser hvordan behovsnedbrytningen for hovedplanlegging foregår. ![Behovsnedbryting ved hjelp av stykklisteversjon](./media/multisitedemandexplosionscenariousingbomversion.gif)

<a name="additional-resources"></a>Tilleggsressurser
--------

[Fastslå stykklisteversjonen](master-plan-bom-version-determined.md)

[Oversikt over hovedplanlegging og multisite-funksjonalitet](master-plan-multisite-functionality.md)



