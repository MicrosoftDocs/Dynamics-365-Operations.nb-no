---
title: Definere arbeidsdeling
description: Du kan definere regler for å skille aktiviteter som må utføres av forskjellige brukere.
author: maertenm
manager: AnnBe
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 47747cba7f83d0b43a284750cff232824e00053a
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/10/2020
ms.locfileid: "3982412"
---
# <a name="set-up-segregation-of-duties"></a>Definere arbeidsdeling

[!include [banner](../../includes/banner.md)]

Du kan definere regler for å skille aktiviteter som må utføres av forskjellige brukere. Dette konseptet kalles arbeidsdeling. Det kan for eksempel være at du ikke vil at den samme personen både skal bekrefte mottak av varer og til å behandle betalingen til leverandøren. Arbeidsdeling hjelper deg med å redusere risikoen for bedrageri, og det hjelper deg å oppdage feil eller uregelmessigheter også. Du kan også bruke arbeidsdeling til å følge policyer for intern kontroll. Fullfør fremgangsmåten nedenfor for å opprette en regel. Du må være en systemansvarlig for å fullføre prosedyren. Demonstrasjonsdatafirmaet DAT brukes til å opprette denne fremgangsmåten. 

1. Gå til **Navigasjonsrute > Moduler > Systemadministrasjon > Sikkerhet > Arbeidsdeling > Arbeidsdelingsregler.**
2. Klikk på **Ny** .
3. Skriv inn en verdi i feltet **Navn** .
4. Klikk på rullegardinknappen i feltet **Første plikt** for å åpne oppslaget.
5. Finn og velg ønsket post i listen. Velg den første plikten som kontrolleres av regelen.
6. Klikk på rullegardinknappen i feltet **Andre plikt** for å åpne oppslaget. 
7. Finn og velg ønsket post i listen. Velg den andre plikten som kontrolleres av regelen.
10. Velg et alternativ i feltet **Alvorsgrad** . Velg viktighet for risikoen som oppstår når den samme brukeren eller rollen utfører begge pliktene.  
11. Skriv inn en verdi i feltet **Sikkerhetsrisiko** . Angi en beskrivelse av sikkerhetsrisikoen.  
12. Skriv inn en verdi i feltet **Sikkerhetsreduksjon** . Angi en beskrivelse av handlingene som du gjøre for å redusere sikkerhetsrisikoen. Du kan for eksempel redusere risikoen ved å utføre mer detaljert gjennomgang av prosessen, utføre en månedlig ledergjennomgang eller ved å dele ressurser med andre avdelinger.     
13. Klikk **Lagre** .

