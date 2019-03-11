---
title: Rapportere som ferdig til en lokasjon som ikke er kontrollert av nummerskilt (program, mai 2016)
description: Denne oppgaveveiledningen viser et eksempel på rapportering som ferdig til en lokasjon som ikke er nummerskiltkontrollert.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WrkCtrResourceGroup, ProdTableListPage, ProdTableCreate, InventItemIdLookupPurchase, ProdParmCostEstimation, ProdParmStartUp, ProdParmReportFinished, WHSWorkTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4da6868a2184a76c435efe824f4670504e1134e7
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "344553"
---
# <a name="report-as-finished-to-a-non-license-plate-controlled-location--application-may-2016"></a>Rapportere som ferdig til en lokasjon som ikke er kontrollert av nummerskilt (program, mai 2016)

[!include [task guide banner](../../includes/task-guide-banner.md)]

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

