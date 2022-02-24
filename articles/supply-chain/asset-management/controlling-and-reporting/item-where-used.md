---
title: Brukssted for vare
description: Dette emnet beskriver hvordan du får oversikt over hvor en vare brukes i Aktivastyring.
author: josaw1
manager: tfehr
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetItemWhereUsed, EntAssetItemWhereUsedCalculate
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: db0932c5a52030c1a7f0411163aee120e2173ca0
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/16/2021
ms.locfileid: "5021145"
---
# <a name="item-where-used"></a>Brukssted for vare

[!include [banner](../../includes/banner.md)]

 

Du kan foreta en beregning for en bestemt vare for å få en oversikt over hvor i Aktivastyring varen er brukt. Resultatene viser konteksten som varen ble brukt i, i løpet av varens levetid. Siden **Vare der brukt** kan åpnes fra hovedmenyen for Aktivastyring, og kan også nås fra følgende sider:

- [Stykklister for aktiva](../objects/object-BOM.md)

- [Reservedeler på aktivatypestandarder](../setup-for-objects/object-types.md#spare-parts-on-the-asset-type-setup)

- [Kategorier for vedlikeholdsjobbtype og vedlikeholdsjobbtyper, varianter av vedlikeholdsjobbtype, handel for vedlikeholdsjobb og sjekklister for vedlikehold](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md)

- [Vedlikeholdsprognose](../work-orders/maintenance-forecasts.md)

- [Innkjøp](../work-orders/procurement.md)

- [Innkjøp for arbeidsordre](../work-orders/procurement.md)

## <a name="make-an-item-where-used-calculation"></a>Gjøre en beregning for vare-der-brukt

1. Klikk på **Aktivastyring** > **Forespørsler** > **Vare der brukt**, eller velg **Vare der brukt**-knappen på en av sidene som er nevnt ovenfor.

2. I dialogboksen **Vare der brukt** velger du varen du vil gjøre beregningen for, i **Varenummer**-feltet.

3. Du kan bruke **Nivå**-feltet til å angi hvor detaljert varelinjene skal være når det gjelder arbeidssted. 

    Hvis du for eksempel setter inn tallet 1 i feltet, og du har en flernivås arbeidsstedsstruktur, vises alle varelinjene for et arbeidssted på øverste nivå. Derfor kan relasjon/antall på en linje tilføyes fra arbeidssteder på et lavere nivå. 
    
    Hvis du setter inn tallet 0 i **Nivå**-feltet, vil du se et detaljert resultat som viser alle varelinjene på alle arbeidsstedsnivåene de er relatert til.

4. I **Inkluder**-delen velger du Ja på veksleknappene som du vil ta med i beregningen.

5. Klikk på **OK** for å starte beregningen.

6. I fanen **Vare der brukt** velger du knappene **Grupper etter** for å vise det nødvendige detaljnivået for beregningen. De valgte **Grupper etter**-knappen er uthevet. Klikk på en knapp for å aktivere eller deaktivere den.

7. Hvis du vil vise dimensjoner knyttet til varen, klikker du på **Visningsdimensjoner** og velger dimensjonene som skal vises.

## <a name="example"></a>Eksempel

I skjermbildet nedenfor ser du et eksempel på en beregning for vare-der-brukt for varenummer 1000.

![Eksempel på beregning for vare-der-brukt](media/12-controlling-and-reporting.png)

