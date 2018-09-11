--- 
title: Definere arbeidsdeling
description: "Du kan definere regler for å skille aktiviteter som må utføres av forskjellige brukere."
author: maertenm
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 754f28cd2831d8a9a57c408518d240de460b732b
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-segregation-of-duties"></a>Definere arbeidsdeling

[!include [task guide banner](../../includes/task-guide-banner.md)]

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


