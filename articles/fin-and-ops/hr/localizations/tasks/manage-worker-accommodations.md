--- 
title: Behandle arbeidertilpassinger
description: "Denne fremgangsmåten går gjennom trinnene for å definere tilpasningstyper for arbeidsmiljø, for eksempel ergonomiske stoler eller periodiske pauser."
author: ShielaSogge
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 10d34d0b2eca95034d1f67931ff72a035be9a6b8
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="manage-worker-accommodations"></a>Behandle arbeidertilpassinger

[!include[task guide banner](../../../includes/task-guide-banner.md)]

Denne fremgangsmåten går gjennom trinnene for å definere tilpasningstyper for arbeidsmiljø, for eksempel ergonomiske stoler eller periodiske pauser. Den viser også hvordan du tilordner disse tilpasningstyper til en arbeider, og enten godkjenner eller avviser tilpasningstypen. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.


## <a name="setup-accommodations"></a>Definer tilpasninger
1. Gå til Personale > Oppsett > Tilpasningstyper.
2. Klikk Ny.
3. I Tilpasningstype-feltet angir du et navn på tilpasningen. Eksempel: tastatur.
4. I Beskrivelse-feltet skriver du inn en beskrivelse for tilpasningen. Eksempel: Ergonomisk tastatur.
5. Angi informasjon som hjelper deg med å klargjøre tilpasningen i Merknad-feltet.
6. Klikk Lagre.
7. Lukk siden.

## <a name="assign-accommodations"></a>Tilordne tilpasninger
1. Gå til Personale > Arbeidere > Ansatte.
2. Velg en ansatt fra listen.
3. Klikk navnet på den ansatte for å vise detaljer om ansatt som ber om tilpasningen.
4. Utvid hurtigkategorien Personlig informasjon.
5. Klikk Tilpasninger.
6. Klikk Ny.
7. Velg den aktuelle tilpasningen i feltet Tilpasningstype. Eksempel: tastatur
8. I feltet Jobboppgave angir du arbeidsoppgaven som krever tilpasning.
9. I Status-feltet angir du den aktuelle statusen. Eksempel: rimelig
    * Følgende statuser er tilgjengelige. Forespurt angir at tilpasningen er opprettet, men ennå ikke er gjennomgått. Rimelig angir at tilpasningen er rimelig og skal gis. Med overlast angir at tilpasningen vil plassere en uforholdsmessige belastning på arbeidsgiver og er avslått. I dette eksemplet ble forespørselen umiddelbart godkjent fordi forespørselen om tilpasning var minimal.  
10. I feltet Godkjent velger du personen som godtok forespørselen om tilpasning.
11. Klikk Velg.
12. Angi datoen og klokkeslettet da forespørselen om tilpasning ble godtatt i feltet Dato og klokkeslett for godkjenning.
13. Utvid merknadsdelen.
14. Angi informasjon eller ressurskostnader som bidrar til å klargjøre virkningen av tilpasningen, i feltet Økonomisk.
    * Hvis tilpasning er avslått, kan Svar-feltet brukes til å angi hvorfor en forespørsel ble avvist.  
15. Klikk Lagre.


