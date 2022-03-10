---
title: Definere arbeidsdeling
description: Du kan definere regler for å skille aktiviteter som må utføres av forskjellige brukere.
author: peakerbl
ms.date: 01/04/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1c06ce9325d7b0894ba53d6b9782f495a48280d45e538b048d883ab86f05dabf
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6755754"
---
# <a name="set-up-segregation-of-duties"></a>Definere arbeidsdeling

[!include [banner](../../includes/banner.md)]

Du kan definere regler for å skille aktiviteter som må utføres av forskjellige brukere. Dette konseptet kalles arbeidsdeling. Det kan for eksempel hende at du ikke vil at den samme personen skal bekrefte mottak av varer og behandle betalingen til leverandøren. Arbeidsdeling hjelper deg med å redusere risikoen for bedrageri, og det hjelper deg å oppdage feil eller uregelmessigheter også. Du kan også bruke arbeidsdeling til å følge policyer for intern kontroll. Fullfør fremgangsmåten nedenfor for å opprette en regel. Du må være en systemansvarlig for å fullføre prosedyren.

1. Gå til **Systemadministrasjon** > **Sikkerhet** > **Arbeidsdeling** > **Arbeidsdelingsregler**.
2. Klikk på **Ny**.
3. Skriv inn en verdi i feltet **Navn**.
4. Klikk på rullegardinknappen i feltet **Første plikt** for å åpne oppslaget.
5. Finn og velg ønsket post i listen. Velg den første plikten som kontrolleres av regelen.
6. Klikk på rullegardinknappen i feltet **Andre plikt** for å åpne oppslaget. 
7. Finn og velg ønsket post i listen. Velg den andre plikten som kontrolleres av regelen.
10. Velg et alternativ i feltet **Alvorsgrad**. Velg viktighet for risikoen som oppstår når den samme brukeren eller rollen utfører begge pliktene.  
11. Skriv inn en verdi i feltet **Sikkerhetsrisiko**. Angi en beskrivelse av sikkerhetsrisikoen.  
12. Skriv inn en verdi i feltet **Sikkerhetsreduksjon**. Angi en beskrivelse av handlingene som du gjøre for å redusere sikkerhetsrisikoen. Du kan for eksempel redusere risikoen ved å utføre mer detaljert gjennomgang av prosessen, utføre en månedlig ledergjennomgang eller ved å dele ressurser med andre avdelinger.     
13. Klikk på **Lagre**.

> [!IMPORTANT] 
> Samsvar med reglene for arbeidsdeling kontrolleres ikke når du oppretter en regel. Du kan opprette en regel som skaper en konflikt for eksisterende roller. Eksisterende brukerrolletilordninger kan også være i konflikt med den nye regelen. Du må validere samsvar etter at du har opprettet eller endret en regel. Hvis du vil ha mer informasjon, kan du se [Identifisere og løse konflikter i arbeidsdeling](identify-resolve-conflicts-segregation-duties.md)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]