---
title: Vedlikeholde rute for en produktmodell
description: Kjører du denne prosedyren krever det at en eksisterende produktmodellkonfigurasjon finnes.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCRouteOperationDetails, WrkCtrCapabilityLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 90ea3f65284cc97906002015c715d9f071202bdb
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4966836"
---
# <a name="maintain-route-for-a-product-model"></a>Vedlikeholde rute for en produktmodell

[!include [banner](../../includes/banner.md)]

Kjører du denne prosedyren krever det at en eksisterende produktmodellkonfigurasjon finnes. Denne fremgangsmåten bruker modellen for High-end-høyttaler i demofirmaet USMF til å lede deg gjennom prosessen.


## <a name="add-a-route-operation"></a>Legge til en ruteoperasjon
1. Klikk på Definisjon av produktvariantmodell.
2. Klikk på Produktkonfigurasjonsmodeller.
3. Finn og velg ønsket post i listen.
    * Velg High-end-høyttalermodellen for denne øvelsen.  
4. Klikk på koblingen i den valgte raden i listen.
5. Utvid delen Ruteoperasjoner.
6. Klikk på Legg til.
7. Skriv inn en verdi i Navn-feltet.
8. Skriv inn en verdi i feltet Beskrivelse.
9. Klikk på Lagre.

## <a name="enter-route-operation-details"></a>Angi detaljer om ruteoperasjon
1. Klikk på Detaljer om ruteoperasjon.
2. Angi eller velg en verdi i feltet Operasjon.
3. I Oper. Nei. angir du et nummer.
    * Operasjonsnumre fastsetter rutesekvensen.  
    * Hver egenskap for en ruteoperasjon kan få en statisk verdi eller tilordnes til et attributt. Tilordning til et attributt fører til at verdien blir definert som en del av konfigurasjonen.  
4. Angi eller velg en verdi i Rutegruppe-feltet.
    * Rutegruppen bestemmer grunnleggende virkemåte for etterkalkulering, forbruk og oppsett.  
5. Klikk på fanen Oppsett.
6. Klikk på fanen Tider.
7. I feltet Prosessantall angir du et nummer.
    * Bestem hvor mange som skal bli behandlet i løpet av én operasjon.  
8. Angi et tall i feltet Timer/tid.
    * Angi tidsforholdet.  
9. Merk av for Sett.
10. Angi et tall i feltet Kjøretid.
    * Bestem behandlingstiden for antallet som du har angitt.  
11. Klikk på fanen Ressursbehov.
12. Klikk på Legg til.
13. Merk den valgte raden i listen.
14. Velg et alternativ i feltet Behovstype.
    * Bestem om du vil angi bestemte ressurser eller egenskaper som de må inneha.  
15. Angi eller velg en verdi i feltet Behov.
16. Klikk på OK.

