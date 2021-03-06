---
title: Beregn vareprognose
description: Dette emnet forklarer hvordan du beregner vareprognose i Aktivastyring.
author: johanhoffmann
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetItemForecast
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 9392245abe5858b03b8324dcb471f5652aed7cd6
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5813899"
---
# <a name="calculate-item-forecast"></a>Beregn vareprognose

[!include [banner](../../includes/banner.md)]

 

På samme måte som du kan foreta beregninger av kapasitetsbelastning, som beskrevet i den forrige delen, kan du også foreta beregninger av vareprognoser:

- linjer for vedlikeholdsplan  
- arbeidsordrer som ennå ikke er planlagt  
- planlagte arbeidsordrer

Dette er nyttig hvis du vil ha en oversikt over forventet vareforbruk (reservedeler i tillegg til andre varer som er nødvendige for å fullføre arbeidsordrer) for en bestemt periode. Beregning av vareprognose kan utføres for alle aktiva eller valgte aktiva. Du kan også foreta en beregning av en aktivitet for vedlikeholdsnedetid (**Alle aktiviteter for vedlikeholdsnedetid** eller **Aktive aktiviteter for vedlikeholdsnedetid**), eller en arbeidsordrepulje (**Alle arbeidsordrepuljer** eller **Aktive arbeidsordrepuljer**).

1. Klikk på **Aktivastyring** > **Forespørsler** > **Vareprognose** eller **Aktivastyring** > **Felles** > **Arbeidsordrepuljer** > **Alle arbeidsordrepuljer** / **Aktive arbeidsordrepuljer** > velg arbeidsordrepulje i listen > **Vareprognose**-knappen, eller **Aktivastyring** > **Felles** > **Aktiviteter for vedlikeholdsnedetid** > **Alle aktiviteter for vedlikeholdsnedetid** / **Aktive aktiviteter for vedlikeholdsnedetid** > velg aktiviteter for vedlikeholdsnedetid i listen > **Vareprognose**-knappen.

2. I dialogboksen **Beregn vareprognose** velger du en periode for beregningen i feltene **Start dato/klokkeslett** og **Sluttdato/-klokkeslett**.

3. Velg "Ja" på veksleknappen **Inkluder vedlikeholdsplan** hvis du vil inkludere vedlikeholdsplanlinjer i prognoseberegningen.

4. Velg "Ja" på veksleknappen **Inkluder arbeidsordre** hvis du vil inkludere arbeidsordrejobber i prognoseberegningen.

5. Du kan bruke **Nivå**-feltet til å angi hvor detaljert prognoselinjene skal være når det gjelder arbeidssted. 

      Hvis du for eksempel setter inn tallet 1 i feltet, og du har en arbeidsstedsstruktur med flere nivåer, vises alle vedlikeholdsplanlinjene og arbeidsordrene for et arbeidssted på øverste nivå, og derfor kan det hende at timene på en linje blir lagt til fra arbeidssteder plassert på et lavere nivå. 
  
      Hvis du setter inn tallet 0 i **Nivå**-feltet, vil du se et detaljert resultat som viser alle vedlikeholdsplanlinjene og alle arbeidsordrene på alle arbeidsstedsnivåene de er relatert til.

6. Klikk på **OK** for å starte beregningen.

7. I **Grupper etter...**-gruppene klikker du de relevante knappene for å vise det nødvendige detaljnivået for beregningen. I skjermbildet nedenfor er de valgte **Grupper etter**-knappene uthevet med blått. Klikk på en knapp for å aktivere eller deaktivere den.

8. Klikk på **Vis dimensjoner**-knappen hvis du vil se produkt-, lagrings- eller sporingsdimensjonene som er knyttet til varene. Merk av i de aktuelle avmerkingsboksene, og klikk **OK**.

![Figur 1](media/02-capacity-planning.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]