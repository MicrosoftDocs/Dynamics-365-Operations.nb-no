---
title: Vedlikeholde rute for en produktmodell
description: Kjører du denne prosedyren krever det at en eksisterende produktmodellkonfigurasjon finnes.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCRouteOperationDetails, WrkCtrCapabilityLookUp
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 72d1ef253214eae57344417646e9ce2f76ce9200
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844351"
---
# <a name="maintain-route-for-a-product-model"></a>Vedlikeholde rute for en produktmodell

[!include [task guide banner](../../includes/task-guide-banner.md)]

Kjører du denne prosedyren krever det at en eksisterende produktmodellkonfigurasjon finnes. Denne fremgangsmåten bruker modellen for High-end-høyttaler i demofirmaet USMF til å lede deg gjennom prosessen.


## <a name="add-a-route-operation"></a>Legge til en ruteoperasjon
1. Klikk Definisjon av produktvariantmodell.
2. Klikk Produktkonfigurasjonsmodeller.
3. Finn og velg ønsket post i listen.
    * Velg High-end-høyttalermodellen for denne øvelsen.  
4. Klikk koblingen i den valgte raden i listen.
5. Utvid delen Ruteoperasjoner.
6. Klikk Legg til.
7. Skriv inn en verdi i Navn-feltet.
8. Skriv inn en verdi i feltet Beskrivelse.
9. Klikk Lagre.

## <a name="enter-route-operation-details"></a>Angi detaljer om ruteoperasjon
1. Klikk Detaljer om ruteoperasjon.
2. Angi eller velg en verdi i feltet Operasjon.
3. I Oper. Nr. angir du et nummer.
    * Operasjonsnumre fastsetter rutesekvensen.  
    * Hver egenskap for en ruteoperasjon kan få en statisk verdi eller tilordnes til et attributt. Tilordning til et attributt fører til at verdien blir definert som en del av konfigurasjonen.  
4. Angi eller velg en verdi i Rutegruppe-feltet.
    * Rutegruppen bestemmer grunnleggende virkemåte for etterkalkulering, forbruk og oppsett.  
5. Klikk kategorien Oppsett.
6. Klikk kategorien Tider.
7. I feltet Prosessantall angir du et nummer.
    * Bestem hvor mange som skal bli behandlet i løpet av én operasjon.  
8. Angi et tall i feltet Timer/tid.
    * Angi tidsforholdet.  
9. Merk av for Sett.
10. Angi et tall i feltet Kjøretid.
    * Bestem behandlingstiden for antallet som du har angitt.  
11. Klikk kategorien Ressursbehov.
12. Klikk Legg til.
13. Merk den valgte raden i listen.
14. Velg et alternativ i feltet Behovstype.
    * Bestem om du vil angi bestemte ressurser eller egenskaper som de må inneha.  
15. Angi eller velg en verdi i feltet Behov.
16. Klikk OK.

