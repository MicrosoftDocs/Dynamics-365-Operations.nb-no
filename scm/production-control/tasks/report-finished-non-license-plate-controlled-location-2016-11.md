--- 
title: 'Ferdigmelde til en skiltkontrollert lokasjon '
description: "Denne oppgaveveiledningen viser et eksempel på rapportering som ferdig til en lokasjon som ikke er nummerskiltkontrollert."
author: ChristianRytt
manager: AnnBe
ms.date: 06/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: 9b861d8499db2b7ba362664e271bedda1d392a23
ms.contentlocale: nb-no
ms.lasthandoff: 07/28/2017

---
# <a name="report-as-finished-to-a-plate-controlled-location"></a>Ferdigmelde til en skiltkontrollert lokasjon  

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne oppgaveveiledningen viser et eksempel på rapportering som ferdig til en lokasjon som ikke er nummerskiltkontrollert. En gjeldende arbeidspolicy er en forutsetning for denne oppgaven. En tidligere oppgaveveiledning viste oppsettet av arbeidspolicyen. Denne oppgaveveiledningen krever Dynamics AX 7.0.1 eller senere.




## <a name="set-up-an-output-location"></a>Definere en utleveringslokasjon
1. Gå til Organisasjonsstyring > Ressurser > Ressursgrupper.
2. Velg ressursgruppe 5102 i listen.
3. Klikk Rediger.
4. Angi 51 i feltet Utleveringslager.
5. Angi 001 i feltet Utleveringslokasjon.
    * Lokasjonen 001 er ikke en nummerskiltkontrollert lokasjon. Du kan definere en utleveringslokasjon uten nummerskilt hvis det finnes en gjeldende arbeidspolicy for lokasjonen.  

## <a name="create-a-production-order-and-report-it-as-finished"></a>Opprette en produksjonsordre og rapportere den som avsluttet
1. Lukk siden.
2. Gå til Produksjonskontroll > Produksjonsordrer > Alle produksjonsordrer.
3. Klikk Ny produksjonsordre.
4. Angi L0101 i feltet Varenummer.
5. Klikk Opprett.
6. Klikk Produksjonsordre i handlingsruten.
7. Klikk Estimer.
8. Klikk OK.
9. Klikk Start.
10. Klikk kategorien Generelt.
11. Velg Aldri i feltet Automatisk stykklisteforbruk.
12. Klikk OK.
13. Klikk Rapporter som fullført.
14. Klikk kategorien Generelt.
15. Velg Ja i feltet Godtar feil.
16. Klikk OK.
17. Klikk Lager i handlingsruten.
18. Klikk Arbeidsdetaljer.
    * Når produksjonsordren ble rapportert som fullført, ble det ikke generert arbeid for plassering. Dette skjer fordi en arbeidspolicy er definert som hindrer at arbeidet blir generert når produktet L0101 rapporteres som ferdig til lokasjon 001.  


