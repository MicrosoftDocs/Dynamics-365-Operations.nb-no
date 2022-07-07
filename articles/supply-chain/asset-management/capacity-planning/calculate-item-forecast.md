---
title: Beregn vareprognose
description: Denne artikkelen forklarer hvordan du beregner vareprognose i Aktivastyring.
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
ms.openlocfilehash: 25e9b00533fb183b27c1bbe616cf6f414b44b5e7
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/15/2022
ms.locfileid: "9016108"
---
# <a name="calculate-item-forecast"></a>Beregn vareprognose

[!include [banner](../../includes/banner.md)]

 

På samme måte som du kan foreta beregninger av kapasitetsbelastning, som beskrevet i den forrige delen, kan du også foreta beregninger av vareprognoser:

- linjer for vedlikeholdsplan  
- arbeidsordrer som ennå ikke er planlagt  
- planlagte arbeidsordrer

Dette er nyttig hvis du vil ha en oversikt over forventet vareforbruk (reservedeler i tillegg til andre varer som er nødvendige for å fullføre arbeidsordrer) for en bestemt periode. Beregning av vareprognose kan utføres for alle aktiva eller valgte aktiva. Du kan også foreta en beregning av en aktivitet for vedlikeholdsnedetid (**Alle aktiviteter for vedlikeholdsnedetid** eller **Aktive aktiviteter for vedlikeholdsnedetid**), eller en arbeidsordrepulje (**Alle arbeidsordrepuljer** eller **Aktive arbeidsordrepuljer**).

1. Klikk på **Aktivastyring** > **Forespørsler** > **Vareprognose** eller **Aktivastyring** > **Arbeidsordrepuljer** > **Alle arbeidsordrepuljer** / **Aktive arbeidsordrepuljer** > velg arbeidsordrepulje i listen > **Vareprognose**-knappen, eller **Aktivastyring** > **Aktiviteter for vedlikeholdsnedetid** > **Alle aktiviteter for vedlikeholdsnedetid** / **Aktive aktiviteter for vedlikeholdsnedetid** > velg aktiviteter for vedlikeholdsnedetid i listen > **Vareprognose**-knappen.

2. I dialogboksen **Beregn vareprognose** velger du en periode for beregningen i feltene **Start dato/klokkeslett** og **Sluttdato/-klokkeslett**.

3. Velg "Ja" på veksleknappen **Inkluder vedlikeholdsplan** hvis du vil inkludere vedlikeholdsplanlinjer i prognoseberegningen.

4. Velg "Ja" på veksleknappen **Inkluder arbeidsordre** hvis du vil inkludere arbeidsordrejobber i prognoseberegningen.

5. Du kan bruke **Nivå**-feltet til å angi hvor detaljert prognoselinjene skal være når det gjelder funksjonslokasjoner. 

      Hvis du for eksempel setter inn tallet 1 i feltet, og du har en funksjonslokasjonsstruktur med flere nivåer, vises alle vedlikeholdsplanlinjene og arbeidsordrene for en funksjonslokasjon på øverste nivå, og derfor kan det hende at timene på en linje blir lagt til fra funksjonslokasjoner plassert på et lavere nivå. 
  
      Hvis du setter inn tallet 0 i **Nivå**-feltet, vil du se et detaljert resultat som viser alle vedlikeholdsplanlinjene og alle arbeidsordrene på alle funksjonslokasjonsnivåene de er relatert til.

6. Klikk på **OK** for å starte beregningen.

7. I **Grupper etter...**-gruppene klikker du de relevante knappene for å vise det nødvendige detaljnivået for beregningen. I skjermbildet nedenfor er de valgte **Grupper etter**-knappene uthevet med blått. Klikk på en knapp for å aktivere eller deaktivere den.

8. Klikk på **Vis dimensjoner**-knappen hvis du vil se produkt-, lagrings- eller sporingsdimensjonene som er knyttet til varene. Merk av i de aktuelle avmerkingsboksene, og klikk **OK**.

![Figur 1.](media/02-capacity-planning.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]