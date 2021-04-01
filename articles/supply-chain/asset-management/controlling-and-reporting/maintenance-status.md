---
title: Vedlikeholdsstatus
description: Dette emnet forklarer hvordan du beregner vedlikeholdsstatus i Aktivastyring.
author: josaw1
manager: tfehr
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetStatusCalculate, EntAssetStatus
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 0f65bfc7b5ef9651853a12bab2ed83dbb8562ba6
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5253740"
---
# <a name="maintenance-status"></a>Vedlikeholdsstatus

[!include [banner](../../includes/banner.md)]

 

I Aktivastyring kan du foreta en oversiktsberegning for en spesifikk periode for nye, aktive og fullførte vedlikeholdsforespørsler, arbeidsordrer og aktiviteter for vedlikeholdsnedetid. Du kan også se antall fullførte betingelsesvurderinger for samme periode. Bruk denne beregningen til å få en oversikt over arbeidsbelastningen for innkommende og fullførte vedlikeholdsforespørsler og arbeidsordrer.

## <a name="make-a-maintenance-status-calculation"></a>Foreta en vedlikeholdsstatusberegning

1. Klikk på **Aktivastyring** > **Forespørsler** > **Vedlikeholdsstatus**.

2. I dialogboksen **Beregn status** velger du perioden du vil gjøre beregningen for, i feltene **Fra dato** og **Til dato**.

3. Du kan bruke **Nivå**-feltet til å angi hvor detaljert vedlikeholdslinjene skal være når det gjelder arbeidssted. 

  Hvis du for eksempel setter inn tallet 1 i feltet, og du har en arbeidsstedsstruktur med flere nivåer, vises alle vedlikeholdslinjene for et arbeidssted på øverste nivå, og derfor kan det hende at statusen på en linje blir lagt til fra arbeidssteder plassert på et lavere nivå. 
  
  Hvis du setter inn tallet 0 i **Nivå**-feltet, ser du et detaljert resultat som viser alle vedlikeholdslinjene på alle arbeidsstedsnivåene de er relatert til.

4. Klikk på **OK** for å starte beregningen.

5. Klikk på knappene **Grupper etter** for å vise det nødvendige detaljnivået for beregningen. De valgte **Grupper etter**-knappen er uthevet. Klikk på en knapp for å aktivere eller deaktivere den.

6. Husk å klikke på **Oppdater**-knappen for å oppdatere beregningen hver gang du gjør endringer, ved å aktivere eller deaktivere **Grupper etter**-knappene eller gjøre en beregning for en ny periode.

7. Klikk på **Status** hvis du vil opprette en ny vedlikeholdsstatusberegning.

>[!NOTE]
>Resultatene som vises i **Vedlikeholdsstatus**, inkluderer bare vedlikeholdsforespørsler og arbeidsordrer med faktisk startdato og -klokkeslett. Sluttdato og -klokkeslett kan være tomt.

## <a name="example-1"></a>Eksempel 1

I skjermbildet nedenfor er knappene **År** og **Måned** aktivert. Når alternativene for **Grupper etter** er valgt, får du en generell oversikt på månedlig basis av arbeidsmengde og gjennomstrømning relatert til vedlikeholdsforespørsler og arbeidsordrer. 

![Eksempel på månedlig arbeidsmengde](media/13-controlling-and-reporting.png)

## <a name="example-2"></a>Eksempel 2

I skjermdumpen nedenfor er informasjon om arbeidssteder lagt til. Nå er det mulig å sammenligne arbeidsmengde og gjennomstrømming mellom arbeidssteder, som kan representere geografiske steder, fabrikker eller arbeidsområder. 

![Eksempel på månedlig arbeidsmengde med funksjonsplasseringer](media/14-controlling-and-reporting.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]