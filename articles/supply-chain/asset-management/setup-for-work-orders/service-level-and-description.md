---
title: Servicenivå og -beskrivelse
description: Dette emnet beskriver servicenivå og -beskrivelse i Aktivastyring.
author: josaw1
manager: tfehr
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetObjectServiceLevel, EntAssetWorkOrderStandardDescription, EntAssetWorkOrderServiceLevel, EntAssetServiceLevelLookup
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8bb56e5103bd9e18e88c164cd308e55d48e64823
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/16/2021
ms.locfileid: "5019385"
---
# <a name="service-level-and-description"></a>Servicenivå og -beskrivelse

[!include [banner](../../includes/banner.md)]

 

Når du oppretter en arbeidsordre, vil du kanskje definere servicenivåene og legge til en generell beskrivelse for den. Du kan opprette servicenivåer for arbeidsordrer på siden **Servicenivåer for arbeidsordrer** og beskrivelser på siden **Arbeidsordrebeskrivelse**.

## <a name="create-a-service-level"></a>Opprette et servicenivå

1. Velg **Aktivastyring** \> **Oppsett** \> **Arbeidsordrer** \> **Servicenivå**.
2. Velg **Ny**.
3. I **Servicenivå**-feltet angir du servicenivået (for eksempel et tall).
4. Angi et navn i **Navn**-feltet.

    I hurtigfanen **Arbeidsordrer** kan du definere forventede start- og sluttdatoer og -klokkeslett. Feltene i denne hurtigfanen definerer perioden som arbeidsordrer skal startes og avsluttes i. De brukes for arbeidsordrer som opprettes manuelt, og arbeidsordrer som opprettes basert på vedlikeholdsforespørsler. 

5. I feltet **Startdag** angir du et antall dager for å definere perioden som arbeidsordren skal starte i. Antallet dager beregnes fra opprettelsesdatoen for arbeidsordren. Hvis for eksempel arbeidsordren skal starte når den opprettes, skriver du inn **0**. Hvis arbeidsordren skal starte innen én uke etter den opprettes, skriver du inn **7**.
6. Hvis du vil angi et starttidspunkt for arbeidsordren, i tillegg til en startdato, setter du alternativet **Angi starttidspunkt** til **Ja**. Deretter angir du starttidspunktet i **Starttidspunkt**-feltet. Hvis du setter alternativet til **Nei**, brukes gjeldende tidspunkt på dagen.
7. I feltet **Sluttdag** angir du et antall dager for å definere perioden som arbeidsordren skal avsluttes i. Antallet dager beregnes fra startdatoen for arbeidsordren. Hvis for eksempel arbeidsordren skal slutte innen én uke fra startdatoen, skriver du inn **7**.
8. Hvis du vil angi et sluttidspunkt for arbeidsordren, i tillegg til en sluttdato, setter du alternativet **Angi sluttidspunkt** til **Ja**. Deretter angir du sluttidspunktet i **Sluttidspunkt**-feltet. Hvis du setter alternativet til **Nei**, brukes gjeldende tidspunkt på dagen.
9. Velg **Lagre**.

![Siden Servicenivå for arbeidsordre](media/19-setup-for-work-orders.png)

## <a name="create-a-description"></a>Opprett en beskrivelse

1. Velg **Aktivastyring** \> **Oppsett** \> **Arbeidsordrer** \> **Beskrivelser**.
2. Velg **Ny**.
3. Angi beskrivelsen i **Beskrivelse**-feltet.
4. Velg **Lagre**.
