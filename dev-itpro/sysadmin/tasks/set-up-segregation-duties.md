--- 
title: Definere arbeidsdeling
description: "Du kan definere regler for å skille aktiviteter som må utføres av forskjellige brukere."
author: maertenm
manager: AnnBe
ms.date: 11/15/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 2ab30f4326b627406f9a39d6c3203b181b67d68f
ms.contentlocale: nb-no
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-segregation-of-duties"></a>Definere arbeidsdeling

[!include[task guide banner](../../includes/task-guide-banner.md)]

Du kan definere regler for å skille aktiviteter som må utføres av forskjellige brukere. Dette konseptet kalles arbeidsdeling. Det kan for eksempel være at du ikke vil at den samme personen både skal bekrefte mottak av varer og til å behandle betalingen til leverandøren. Arbeidsdeling hjelper deg med å redusere risikoen for bedrageri, og det hjelper deg å oppdage feil eller uregelmessigheter også. Du kan også bruke arbeidsdeling til å følge policyer for intern kontroll. Fullfør fremgangsmåten nedenfor for å opprette en regel. Du må være en systemansvarlig for å fullføre prosedyren. Demonstrasjonsdatafirmaet DAT brukes til å opprette denne fremgangsmåten. 

1. Gå til Systemadministrasjon > Sikkerhet > Arbeidsdeling > Arbeidsdelingsregler.
2. Klikk Ny.
3. Skriv inn en verdi i Navn-feltet.
    * Angi et navn for regelen.  
4. Klikk rullegardinknappen i feltet Første plikt for å åpne oppslaget.
5. Finn og velg ønsket post i listen.
    * Velg den første plikten som kontrolleres av regelen.  
6. Klikk koblingen i den valgte raden i listen.
7. Klikk rullegardinknappen i feltet Andre plikt for å åpne oppslaget.
8. Finn og velg ønsket post i listen.
    * Velg den andre plikten som kontrolleres av regelen.  
9. Klikk koblingen i den valgte raden i listen.
10. Velg et alternativ i feltet Alvorlighetsgrad.
    * Velg viktighet for risikoen som oppstår når den samme brukeren eller rollen utfører begge pliktene.  
11. Skriv inn en verdi i feltet Sikkerhetsrisiko.
    * Angi en beskrivelse av sikkerhetsrisikoen.  
12. Skriv inn en verdi i feltet Sikkerhetsreduksjon.
    * Angi en beskrivelse av handlingene som du gjøre for å redusere sikkerhetsrisikoen. Du kan for eksempel redusere risikoen ved å utføre mer detaljert gjennomgang av prosessen, utføre en månedlig ledergjennomgang eller ved å dele ressurser med andre avdelinger.  
13. Klikk Lagre.


