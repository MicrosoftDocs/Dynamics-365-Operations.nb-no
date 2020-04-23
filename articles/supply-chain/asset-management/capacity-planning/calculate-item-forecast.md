---
title: Beregn vareprognose
description: Dette emnet forklarer hvordan du beregner vareprognose i Aktivastyring.
author: josaw1
manager: tfehr
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 20f969b68e4e9a9936f377000191ba9db202447f
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/02/2020
ms.locfileid: "3216465"
---
# <a name="calculate-item-forecast"></a>Beregn vareprognose

[!include [banner](../../includes/banner.md)]

 

På samme måte som du kan foreta beregninger av kapasitetsbelastning, som beskrevet i den forrige delen, kan du også foreta beregninger av vareprognoser:

- linjer for vedlikeholdsplan  
- arbeidsordrer som ennå ikke er planlagt  
- planlagte arbeidsordrer

Dette er nyttig hvis du vil ha en oversikt over forventet vareforbruk (reservedeler i tillegg til andre varer som er nødvendige for å fullføre arbeidsordrer) for en bestemt periode. Beregning av vareprognose kan utføres for alle aktiva eller valgte aktiva. Du kan også foreta en beregning av en aktivitet for vedlikeholdsnedetid (**Alle aktiviteter for vedlikeholdsnedetid** eller **Aktive aktiviteter for vedlikeholdsnedetid**), eller en arbeidsordrepulje (**Alle arbeidsordrepuljer** eller **Aktive arbeidsordrepuljer**).

1. Klikk **Aktivastyring** > **Forespørsler** > **Vareprognose** eller **Aktivastyring** > **Felles** > **Arbeidsordrepuljer** > **Alle arbeidsordrepuljer** / **Aktive arbeidsordrepuljer** > velg arbeidsordrepulje i listen > **Vareprognose**-knappen, eller **Aktivastyring** > **Felles** > **Aktiviteter for vedlikeholdsnedetid** > **Alle aktiviteter for vedlikeholdsnedetid** / **Aktive aktiviteter for vedlikeholdsnedetid** > velg aktiviteter for vedlikeholdsnedetid i listen > **Vareprognose**-knappen.

2. I dialogboksen **Beregn vareprognose** velger du en periode for beregningen i feltene **Start dato/klokkeslett** og **Sluttdato/-klokkeslett**.

3. Velg "Ja" på veksleknappen **Inkluder vedlikeholdsplan** hvis du vil inkludere vedlikeholdsplanlinjer i prognoseberegningen.

4. Velg "Ja" på veksleknappen **Inkluder arbeidsordre** hvis du vil inkludere arbeidsordrejobber i prognoseberegningen.

5. Du kan bruke **Nivå**-feltet til å angi hvor detaljert prognoselinjene skal være når det gjelder arbeidssted. 

      Hvis du for eksempel setter inn tallet 1 i feltet, og du har en arbeidsstedsstruktur med flere nivåer, vises alle vedlikeholdsplanlinjene og arbeidsordrene for et arbeidssted på øverste nivå, og derfor kan det hende at timene på en linje blir lagt til fra arbeidssteder plassert på et lavere nivå. 
  
      Hvis du setter inn tallet 0 i **Nivå**-feltet, vil du se et detaljert resultat som viser alle vedlikeholdsplanlinjene og alle arbeidsordrene på alle arbeidsstedsnivåene de er relatert til.

6. Klikk på **OK** for å starte beregningen.

7. I **Grupper etter...**-gruppene klikker du de relevante knappene for å vise det nødvendige detaljnivået for beregningen. I skjermbildet nedenfor er de valgte **Grupper etter**-knappene uthevet med blått. Klikk på en knapp for å aktivere eller deaktivere den.

8. Klikk **Vis dimensjoner**-knappen hvis du vil se produkt-, lagrings- eller sporingsdimensjonene som er knyttet til varene. Merk av i de aktuelle avmerkingsboksene, og klikk **OK**.

![Figur 1](media/02-capacity-planning.png)
