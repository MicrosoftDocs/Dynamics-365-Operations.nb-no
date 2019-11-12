---
title: Brukssted for vare
description: Dette emnet beskriver hvordan du får oversikt over hvor en vare brukes i Aktivastyring.
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 511108e689c10e27a42253d95b02e5394f9eb713
ms.sourcegitcommit: fb66731f05207094149a6bc7b8549a4dabbb071a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/22/2019
ms.locfileid: "2652362"
---
# <a name="item-where-used"></a>Brukssted for vare

[!include [banner](../../includes/banner.md)]

 

Du kan foreta en beregning for en bestemt vare for å få en oversikt over hvor i Aktivastyring varen er brukt. Resultatene viser konteksten som varen ble brukt i, i løpet av varens levetid. Siden **Vare der brukt** kan åpnes fra hovedmenyen for Aktivastyring, og kan også nås fra følgende sider:

- [Stykkliste for aktiva](../objects/object-BOM.md)

- [Reservedeler på aktivatypestandarder](../setup-for-objects/object-types.md)

- [Vareprognose i prognose for vedlikeholdsjobbtypestandarder](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md)

- [Prognose for vedlikehold av arbeidsordre](../work-orders/maintenance-forecasts.md)

- [Innkjøpsrekvisisjon for arbeidsordre](../work-orders/procurement.md)

- [Innkjøp for arbeidsordre](../work-orders/procurement.md)

## <a name="make-an-item-where-used-calculation"></a>Gjøre en beregning for vare-der-brukt

1. Klikk på **Aktivastyring** > **Forespørsler** > **Vare der brukt**, eller velg **Vare der brukt**-knappen på en av sidene som er nevnt ovenfor.

2. I dialogboksen **Vare der brukt** velger du varen du vil gjøre beregningen for, i **Varenummer**-feltet.

3. Du kan bruke **Nivå**-feltet til å angi hvor detaljert varelinjene skal være når det gjelder arbeidssted. 

    Hvis du for eksempel setter inn tallet 1 i feltet, og du har en flernivås arbeidsstedsstruktur, vises alle varelinjene for et arbeidssted på øverste nivå. Derfor kan relasjon/antall på en linje tilføyes fra arbeidssteder på et lavere nivå. 
    
    Hvis du setter inn tallet 0 i **Nivå**-feltet, vil du se et detaljert resultat som viser alle varelinjene på alle arbeidsstedsnivåene de er relatert til.

4. I **Inkluder**-delen velger du Ja på veksleknappene som du vil ta med i beregningen.

5. Klikk på **OK** for å starte beregningen.

6. I kategorien **Vare der brukt** velger du knappene **Grupper etter** for å vise det nødvendige detaljnivået for beregningen. De valgte **Grupper etter**-knappen er uthevet. Klikk på en knapp for å aktivere eller deaktivere den.

7. Hvis du vil vise dimensjoner knyttet til varen, klikker du på **Visningsdimensjoner** og velger dimensjonene som skal vises.

## <a name="example"></a>Eksempel

I skjermbildet nedenfor ser du et eksempel på en beregning for vare-der-brukt for varenummer 1000.

![Eksempel på beregning for vare-der-brukt](media/12-controlling-and-reporting.png)

