--- 
title: Behandle ordresperrer
description: "Denne fremgangsmåten forklarer hvordan du plasserer salgsordrer for kunden på vent, hvordan du arbeider med ordresperreutsjekkinger og fjerner ordresperrer."
author: omulvad
manager: AnnBe
ms.date: 01/09/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: 6a9487567620b7b7d6d15015f7f0b7675e227c8a
ms.contentlocale: nb-no
ms.lasthandoff: 07/28/2017

---
# <a name="manage-order-holds"></a>Behandle ordresperrer

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåten forklarer hvordan du plasserer salgsordrer for kunden på vent, hvordan du arbeider med ordresperreutsjekkinger og fjerner ordresperrer. En ordre kan settes på vent av en rekke ulike årsaker. Du kan for eksempel sperre en ordre til kundens adresse eller betalingsmetode kan bekreftes, eller til en leder kan gå gjennom kundens kredittgrense. Mens ordren er på vent, kan den ikke behandles av lageret for forsendelse. 

Du kan kjøre denne fremgangsmåten i demonstrasjonsselskapet USMF eller ved hjelp av dine egne data.


## <a name="set-up-order-holds"></a>Definer ordresperrer
1. Gå til Salg og markedsføring > Oppsett > Salgsordrer > Ordresperrekoder.
2. Klikk Ny.
3. Skriv inn en verdi i Sperrekode-feltet.
    * Skriv for eksempel Ring tilbake.  
4. Skriv inn en verdi i feltet Beskrivelse.
    * For eksempel Ordre sperret i påvente av at kunden ringer tilbake.  
    * Eventuelt kan du merke av for Fjernede reservasjoner for å fjerne fysiske reservasjoner fra ordren når denne sperrekoden legges til.  
5. Klikk Lagre.

## <a name="place-order-on-hold"></a>Sett ordre på vent
1. Gå til Salg og markedsføring > Salgsordrer > Alle salgsordrer.
2. Klikk Ny.
3. Angi eller velg en verdi i Kundekonto-feltet.
4. Klikk OK.
5. Angi eller velg en verdi i Varenummer-feltet.
6. Angi et tall i feltet Antall.
7. Klikk Salgsordre i handlingsruten.
8. Klikk Ordresperrer.
9. Klikk Ny.
10. Velg koden du har opprettet i den forrige underoppgaven, i Sperrekode-feltet.
11. Klikk Lagre.
12. Lukk siden.
13. Gå til Salg og markedsføring > Salgsordrer > Alle salgsordrer.
14. Merk den valgte raden i listen.
    * Ordrer som er på vent, har feltene "Ikke behandle" og "Vent" merket av.    
15. Klikk Plukk og pakk i handlingsruten.

## <a name="manage-order-holds"></a>Behandle ordresperrer
1. Gå til Salg og markedsføring > Salgsordrer > Åpne ordrer > Ordresperrer.
    * Siden Ordresperrer fungerer som et arbeidsområde der du kan få en oversikt over alle gjeldende og behandlede sperrer, og behandle dem og tilknyttede salgsordrer.      
2. Merk den valgte raden i listen.
3. Klikk Sperre - utsjekking i handlingsruten.
4. Klikk Sjekk ut.
5. Fjern merket for den valgte raden i listen.
    * Feltet Sjekk ut til viser nå bruker-IDen din.   
6. Klikk Fjern utsjekking.
7. Klikk Fjern sperre i handlingsruten.
    * Når du er klar til å fjerne sperren og la ordren gå videre til neste trinn i fullføringen, må du fjerne sperren. Hvis ordren ikke krever noen endringer, kan du kjøre Fjern sperrer-handlingen. Du kan imidlertid bruke Fjern og endre-handlingen hvis ordren må oppdateres når du fjerner en sperre.      
    * Fjern og send-handlingen gjelder bare når du bruker Telefonsenterfunksjonalitet.  
8. Klikk Fjern sperrer.
    * Sperringen er nå fjernet fra ordren og fjernet fra listen over aktive sperringer. Hvis du vil se alle sperringene eller delsettet i henhold til en bestemt status, kan du endre verdien i Vis-feltet.     


