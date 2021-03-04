---
title: Lukke masseregnskapsperiode
description: Dette emnet viser hvordan du setter en periode på vent eller permanent lukker en periode for mer enn en juridisk enhet om gangen.
author: aprilolson
manager: AnnBe
ms.date: 08/16/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerCalendar, LedgerPeriodModuleAccessControlUpdate, SysLookupPicklist, LedgerFiscalCalendarPeriodStatus
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a149b35c6964166207effc799a02cd4c59bbb843
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4446323"
---
# <a name="mass-financial-period-close"></a>Lukke masseregnskapsperiode

[!include [banner](../../includes/banner.md)]

Dette emnet viser hvordan du setter en periode på vent eller permanent lukker en periode for mer enn en juridisk enhet om gangen. I tillegg viser oppgaven hvordan du begrenser brukergruppepostering til spesifikke moduler.

1. Gå til **Moduler > Økonomimodul > Lukket periode > Finanskalendere** i navigasjonsruten. Vær oppmerksom på at listen over juridiske enheter som vises, er avhengig av regnskapskalenderen som er valgt på siden. Bare juridiske enheter som bruker den valgte regnskapskalenderen, vises.
2. Velg **Rediger**.
3. Velg perioden du vil endre statusen for.
4. Velg de juridiske enhetene du vil oppdatere statusen for. Du kan raskt velge alle juridiske enheter ved merke av øverst til venstre i rutenettet.  
5. Velg **Oppdater modultilgang** for å definere posteringstilgangen til en valgt modul. Modulstatusen kan også oppdateres en etter en ved å redigere postene i rutenettet. Knappen er nyttig når du vil oppdatere flere poster for juridisk enhet raskt.  
6. I feltet **Programmodul** velger du modulen som du vil oppdatere statusen for. Klikk **Velg**.
7. I **tilgangsnivået** velger du **Alle**, **Ingen** eller en bestemt brukergruppe. Klikk **Velg**. Alle angir at alle brukere med redigeringstilgang til modulen kan postere hvis perioden er åpen. Ingen angir at brukere ikke kan postere til modulen hvis perioden er åpen. En bestemt brukergruppe angir bare brukere i gruppen kan postere til modulen hvis perioden er åpen.  
8. Velg **Oppdater**.
9. Velg en annen periode å oppdatere statusen for.
10. Velg de juridiske enhetene du vil oppdatere periodestatusen for.
11. Velg **Oppdater periodestatus** og sett statusen til **På vent**, **Åpen** eller **Lukket permanent**. **Åpen** angir perioden det kan posteres til, gitt at brukeren har tilgang. **På vent** betyr at perioden ikke kan posteres til, men perioden kan åpnes på nytt. **Lukket permanent** betyr at perioden er lukket og aldri kan åpnes. Justeringer kan ikke posteres. Vi anbefaler ikke å sette en periode til **Lukket permanent** før alle justeringer og revisjoner er fullført.  
12. Velg **Oppdater**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]