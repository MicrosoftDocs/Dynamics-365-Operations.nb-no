---
title: Opprette en mva-betaling
description: Jobbprosedyren Utlign og poster merverdiavgift utligner mva-saldoer på mva-kontoene og forskyver dem til mva-oppgjørskontoen for en gitt periode.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Dialog
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7aec00c2fb657f0b4074063ef7acad5f4372ebca
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/25/2020
ms.locfileid: "4646341"
---
# <a name="create-a-sales-tax-payment"></a>Opprette en mva-betaling

[!include [banner](../../includes/banner.md)]

Jobbprosedyren Utlign og poster merverdiavgift utligner mva-saldoer på mva-kontoene og forskyver dem til mva-oppgjørskontoen for en gitt periode.

1. Gå til **Avgift > Deklareringer > Merverdiavgift > Utlign og poster merverdiavgift**.
2. Klikk på rullegardinknappen i **Utligningsperiode**-feltet for å åpne oppslaget.
3. Klikk koblingen i den valgte raden i listen.
4. Angi en dato i **Fra dato**-feltet.
    * Hvis du ikke velger alternativet **Ta med rettelser** på siden **Parametere for økonomimodul**, kan utligningen behandles for forskjellige versjoner. Original er den første utligningen for et periodeintervall og kan bare behandles én gang for et periodeintervall. De nyeste rettelsene utligner mva-transaksjoner som er postert etter at den opprinnelige versjonen er opprettet.   
5. Angi en dato i feltet **Transaksjonsdato**.
6. Klikk **OK**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]