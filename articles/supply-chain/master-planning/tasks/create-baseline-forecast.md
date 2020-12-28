---
title: Opprette en basislinjeprognose
description: En produksjonsplanlegger kan opprette en basislinjeprognose ved å bruke tidsserie-prognosemodeller eller ved å kopiere det historiske behovet.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqIntercompanyPlanningGroupSetup, ReqIntercompanyPlanningGroupAllocKeys, ReqDemPlanForecastParameters, ReqDemPlanCreateForecastDialog, SysQueryForm, ReqDemPlanForecastViewer
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 47e26a48cdde3a6996f4c0a4ca85222c402f44e2
ms.sourcegitcommit: 436731d8b3889bebfe6f17922b0a31b1994f6796
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/26/2020
ms.locfileid: "4434848"
---
# <a name="create-a-baseline-forecast"></a>Opprette en basislinjeprognose

[!include [banner](../../includes/banner.md)]

En produksjonsplanlegger kan opprette en basislinjeprognose ved å bruke tidsserie-prognosemodeller eller ved å kopiere det historiske behovet. Denne fremgangsmåten viser hvordan du kopierer det historiske behovet for å opprette en basislinjeprognose for alle produkter som bruker én varetildelingsnøkkel. 


## <a name="set-up-an-item-allocation-key"></a>Definere en nøkkel for varefordeling
1. Gå til Hovedplanlegging > Oppsett > Konserninterne planleggingsgrupper.
2. Bruk hurtigfilteret for å søke etter poster. Du kan for eksempel filtrere på Navn-feltet med verdien 10.
    * Behovsprognose kjører på tvers av juridiske enheter. Derfor må du definere alle selskapene som du vil generere prognoser for, i én konsernintern planleggingsgruppe.  
3. Finn og velg ønsket post i listen.
4. Klikk Varefordelingsnøkler.
    * Velg alle varetildelingsnøklene du vil opprette prognoser for.  
5. Merk den valgte raden i listen.
    * Velg D_Aloc varetildelingsnøkkelen.  
6. Klikk >.
7. Lukk siden.
8. Lukk siden.

## <a name="set-up-the-demand-forecasting-parameters"></a>Definere parameterne for behovsprognose
1. Gå til Hovedplanlegging > Oppsett > Behovsprognose > Parametere for behovsprognose.
2. Utvid delen Prognosealgoritmeparametere.
3. Velg Kopier over historisk behov i feltet Strategi for prognosegenerering.
4. Klikk Lagre.

## <a name="create-a-baseline-forecast"></a>Opprette en basislinjeprognose
1. Gå til Hovedplanlegging > Prognose > Behovsprognose > Generer statistisk basislinjeprognose.
2. Angi en dato i Fra dato-feltet.
    * Angi denne datoen hvis du har salgsordrer fra og med 1. januar 2015. Hvis ikke kan du angi den tidligste datoen for salgsordrene.  
3. Angi en dato i Til dato-feltet.
    * Angi den siste datoen i salgsordrene, for eksempel 2015-03-31.  
4. Angi en dato i Fra dato-feltet.
    * Angi 2015-04-01. Denne datoen beregnes automatisk som startdatoen for den neste prognoseperioden.  
5. Utvid delen Poster som skal inkluderes.
6. Klikk Filter.
7. Merk den valgte raden i listen.
    * Merk raden der feltet = Konsernintern planleggingsgruppe.  
8. Skriv inn en verdi i Kriterier-feltet.
    * Skriv inn den konserninterne planleggingsgruppen, for eksempel 10, som du brukte i den første oppgaven.  
9. Finn og velg ønsket post i listen.
    * Merk raden der feltet = Varetildelingsnøkkel.  
10. Skriv inn en verdi i Kriterier-feltet.
11. Klikk OK.
12. Utvid seksjonen Avanserte parametere.
13. Velg Måned i Prognoseperiode-feltet.
14. Angi 3 i Prognosehorisont-feltet.
15. Angi 1 i feltet Låsningshorisont.
16. Klikk OK.

## <a name="visualize-the-demand-forecast"></a>Visualisere behovsprognosen
1. Gå til Hovedplanlegging > Prognose > Behovsprognose > Justert behovsprognose.
2. Velg cellen i rad 1, kolonne 2 i tabellen for aggregert visning. Dette er den andre måneden du har opprettet prognose.
3. Sett QtyCell til "400".
    * I cellen angir du et annet nummer enn prognoseverdien, for eksempel 400.  
4. Du har gjort en manuell justering av prognosen. Legg merke til den grafiske indikasjonen i neste trinn.
5. Klikk Prognoselinjedetaljer.
    * På denne siden kan du se presisjonsverdier, historisk behov og prognose. Du kan også endre prognosen.  

