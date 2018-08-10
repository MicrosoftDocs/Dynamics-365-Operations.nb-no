--- 
title: Lukke masseregnskapsperiode
description: "Denne fremgangsmåten viser hvordan du setter en periode på vent eller permanent lukker en periode for mer enn en juridisk enhet om gangen."
author: aprilolson
manager: AnnBe
ms.date: 10/25/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ef3cad6538d9efbd1c1881f4b7d771382d9b1ba8
ms.openlocfilehash: 1954bfdf4807e91d275e3a1ba80f959bdf9464a8
ms.contentlocale: nb-no
ms.lasthandoff: 10/26/2017

---
# <a name="mass-financial-period-close"></a>Lukke masseregnskapsperiode

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåten viser hvordan du setter en periode på vent eller permanent lukker en periode for mer enn en juridisk enhet om gangen. I tillegg viser oppgaven hvordan du begrenser brukergruppepostering til spesifikke moduler.

1. Gå til Økonomimodul > Periodeavslutning > Finanskalendere.
    * Vær oppmerksom på at listen over juridiske enheter som vises, er avhengig av regnskapskalenderen som er valgt på siden. Bare juridiske enheter som bruker den valgte regnskapskalenderen, vises.  
2. Klikk Rediger.
3. Velg perioden du vil endre statusen for.
4. Velg de juridiske enhetene du vil oppdatere statusen for.
    * Du kan raskt velge alle juridiske enheter ved merke av øverst til venstre i rutenettet.  
5. Velg Oppdater modultilgang for å definere posteringstilgangen til en valgt modul.
    * Modulstatusen kan også oppdateres en etter en ved å redigere postene i rutenettet. Knappen er nyttig når du vil oppdatere flere poster for juridisk enhet raskt.  
6. I feltet Programmodul velger du modulen som du vil oppdatere statusen for. Klikk Velg.
7. I tilgangsnivået velger du Alle, Ingen eller en bestemt brukergruppe. Klikk Velg.
    * Alle angir at alle brukere med redigeringstilgang til modulen kan postere hvis perioden er åpen. Ingen angir at brukere ikke kan postere til modulen hvis perioden er åpen. En bestemt brukergruppe angir bare brukere i gruppen kan postere til modulen hvis perioden er åpen.  
8. Klikk Oppdater.
9. Velg en annen periode å oppdatere statusen for.
10. Velg de juridiske enhetene du vil oppdatere periodestatusen for.
11. Velg Oppdater periodestatus og sett statusen til På vent, Åpen eller Lukket permanent.
    * Åpen angir perioden det kan posteres til, gitt at brukeren har tilgang. På vent betyr at perioden ikke kan posteres til, men perioden kan åpnes på nytt. Lukket permanent betyr at perioden er lukket og aldri kan åpnes. Justeringer kan ikke posteres. Vi anbefaler ikke å sette en periode til Lukket permanent før alle justeringer og revisjoner er fullført.  
12. Klikk Oppdater.


