---
title: Nedbryting av en stykklisteversjon
description: Denne artikkelen beskriver et scenario som involverer nedbrytingen av en stykklisteversjon (BOM) for hovedplanlegging.
author: roxanadiaconu
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqTransExplosion
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19211
ms.assetid: fe08c2e6-9cc5-4e34-bbb2-cd07843403b5
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 17e5d8638dc02d92a0c67364790353833551250f
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/04/2021
ms.locfileid: "6187416"
---
# <a name="explosion-of-a-bom-version"></a>Nedbryting av en stykklisteversjon

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver et scenario som involverer nedbrytingen av en stykklisteversjon (BOM) for hovedplanlegging.

En vellykket behovsnedbrytning av en stykklisteversjon resulterer i et behov for hver stykklistelinjevare på et bestemte område eller muligens ved et bestemt lager. For en områdespesifikk stykkliste kan det være definert et bestemt lager for hver stykklistelinje. Varens dimensjonsinnstillinger angir dessuten om lageret er påkrevd for hver stykklistelinje. Det resulterende behovet for hver stykklistelinje blir deretter utgangspunktet for en ytterligere behovsnedbrytning. Dette hovedplanleggingsscenariet omfatter følgende betingelser:

-   Områdedimensjonen er obligatorisk, og må angis på behovstransaksjonen.
-   Områdedimensjonen er konsekvent. Området for behovet på lavere nivå, er derfor det samme som området på den innledende behovstransaksjonen.

Illustrasjonen nedenfor viser hvordan behovsnedbrytningen for hovedplanlegging foregår. ![Behovsnedbryting ved hjelp av stykklisteversjon](./media/multisitedemandexplosionscenariousingbomversion.gif)

## <a name="additional-resources"></a>Tilleggsressurser

[Fastslå stykklisteversjonen](master-plan-bom-version-determined.md)

[Oversikt over hovedplanlegging og multisite-funksjonalitet](master-plan-multisite-functionality.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]