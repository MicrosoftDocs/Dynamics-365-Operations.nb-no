---
title: Beregn kapasitetsbelastning
description: Denne artikkelen forklarer hvordan du beregner kapasitetsbelastning i Aktivastyring.
author: johanhoffmann
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetCapacityLoad, EntAssetWorkOrderCapacityLoadCalculate, EntAssetWorkOrderCapacityLoad
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 95d1e38db8e4658a57f36139836264b87d525e61
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/15/2022
ms.locfileid: "9016137"
---
# <a name="calculate-capacity-load"></a>Beregn kapasitetsbelastning

[!include [banner](../../includes/banner.md)]


I Aktivastyring kan du beregne kapasitetsbelastning på:

- linjer for vedlikeholdsplan  
- arbeidsordrer som ennå ikke er planlagt  
- planlagte arbeidsordrer

Dette er nyttig hvis du vil ha en oversikt over forventet kapasitetsbelastning for en bestemt periode. Beregning av kapasitetsbelastning kan utføres for alle aktiva eller valgte aktiva. Du kan også foreta en beregning av aktiviteter for vedlikeholdsnedetid eller arbeidsordrepuljer.

1. Klikk på **Aktivastyring** > **Forespørsler** > **Kapasitetsbelastning** eller **Aktivastyring** > **Arbeidsordrepuljer** > **Alle arbeidsordrepuljer** / **Aktive arbeidsordrepuljer** > velg arbeidsordrepulje i listen > **Kapasitetsbelastning**-knappen, eller **Aktivastyring** > **Aktiviteter for vedlikeholdsnedetid** > **Alle aktiviteter for vedlikeholdsnedetid** / **Aktive aktiviteter for vedlikeholdsnedetid** > velg vedlikeholdsaktivitet i listen > **Kapasitetsbelastning**-knappen.

2. I dialogboksen **Beregn kapasitetsbelastning** velger du en periode for beregningen i feltene **Start dato/klokkeslett** og **Sluttdato/-klokkeslett**.

3. Velg "Ja" på veksleknappen **Inkluder vedlikeholdsplan** hvis du vil inkludere vedlikeholdsplanlinjer i beregningen.

4. Velg "Ja" på veksleknappen **Inkluder arbeidsordre** hvis du vil inkludere arbeidsordrejobber i beregningen.

5. Du kan bruke **Nivå**-feltet til å angi hvor detaljerte kapasitetsbelastningslinjene skal være når det gjelder funksjonslokasjoner. 

    Hvis du for eksempel setter inn tallet 1 i feltet, og du har en funksjonslokasjonsstruktur med flere nivåer, vises alle vedlikeholdsplanlinjene og arbeidsordrene for en funksjonslokasjon på øverste nivå, og derfor kan det hende at timene på en linje blir lagt til fra funksjonslokasjoner plassert på et lavere nivå. 
    
    Hvis du setter inn tallet 0 i **Nivå**-feltet, vil du se et detaljert resultat som viser alle vedlikeholdsplanlinjene og alle arbeidsordrene på alle funksjonslokasjonsnivåene de er relatert til.

6. Klikk på **OK** for å starte beregningen.

7. I **Grupper etter...**-gruppene klikker du de relevante knappene for å vise det nødvendige detaljnivået for beregningen. I skjermbildet nedenfor er de valgte **Grupper etter**-knappene uthevet med blått. Klikk på en knapp for å aktivere eller deaktivere den.

    ![Figur 1.](media/01-capacity-planning.png)

>[!NOTE]
>Hvis du bare vil fokusere på kapasitetsplanlegging i forbindelse med planlagte arbeidsordrer, kan du se [Beregne kapasitetsbelastning på planlagte arbeidsordrer](../work-order-scheduling/calculate-capacity-load-on-scheduled-work-orders.md).



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]