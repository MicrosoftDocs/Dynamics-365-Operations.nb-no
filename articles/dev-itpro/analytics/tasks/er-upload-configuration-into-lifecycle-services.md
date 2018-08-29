--- 
title: Laste opp konfigurasjoner av elektronisk rapportering til Lifecycle Services
description: "De følgende trinnene forklarer hvordan en bruker i rollen systemansvarlig eller utvikler av elektronisk rapportering kan opprette en ny formatkonfigurasjon for elektronisk rapportering (ER) og laste den opp til Microsoft Lifecycle Services (LCS)."
author: NickSelin
manager: AnnBe
ms.date: 05/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 6aa6bf7e08285d18210741ba6618878955009280
ms.contentlocale: nb-no
ms.lasthandoff: 08/09/2018

---
# <a name="upload-electronic-reporting-configurations-into-lifecycle-services"></a>Laste opp konfigurasjoner av elektronisk rapportering til Lifecycle Services

[!include [task guide banner](../../includes/task-guide-banner.md)]

De følgende trinnene forklarer hvordan en bruker i rollen systemansvarlig eller utvikler av elektronisk rapportering kan opprette en ny formatkonfigurasjon for elektronisk rapportering (ER) og laste den opp til Microsoft Lifecycle Services (LCS).

I dette eksemplet skal du opprette en konfigurasjon og laste den opp til LCS for eksempelfirmaet Litware, Inc. Denne fremgangsmåten kan utføres i et hvilket som helst firma ettersom ER-konfigurasjoner deles mellom alle firmaer. For å fullføre disse trinnene må du først fullføre trinnene i fremgangsmåten "Opprette en konfigurasjonsleverandør og merke den som aktiv". Tilgang til LCS kreves også for fullføring av denne fremgangsmåten.

1. Gå til Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering.
2. Velg Litware, Inc. og angi som aktiv.
3. Klikk Konfigurasjoner.

## <a name="create-a-new-data-model-configuration"></a>Opprett en ny datamodellkonfigurasjon
1. Klikk Opprett konfigurasjon for å åpne nedtrekksdialogen.
    * Du vil opprette en konfigurasjon som inneholder en eksempeldatamodell for elektroniske dokumenter. Denne datamodellkonfigurasjonen lastes inn i LCS senere.  
2. Skriv inn Eksempelmodellkonfigurasjon i Navn-feltet.
    * Eksempelmodellkonfigurasjon  
3. Skriv inn Eksempelmodellkonfigurasjon i Beskrivelse-feltet.
    * Eksempelmodellkonfigurasjon  
4. Klikk Opprett konfigurasjon.
5. Velg Modellutforming.
6. Klikk Ny.
7. Skriv inn Inngangspunkt i Navn-feltet.
    * Inngangspunkt  
8. Klikk Legg til.
9. Klikk Lagre.
10. Lukk siden.
11. Klikk Endre status.
12. Klikk Fullført.
13. Klikk OK.

## <a name="register-a-new--repository"></a>Registrere et nytt repositorium
1. Lukk siden.
2. Klikk Repositorier.
    * Denne lar deg åpne listen over repositorier for konfigurasjonsleverandøren Litware, Inc.  
3. Klikk Legg til for å åpne nedtrekksdialogen.
    * Dette lar deg legge til et nytt repositorium.  
4. Velg LCS i feltet Type konfigurasjonsrepositorium.
5. Klikk Opprett repositorium.
6. Angi eller velg en verdi i feltet Prosjekt.
    * Velg ønsket LCS-prosjekt. Du må ha tilgang til prosjektet.  
7. Klikk OK.
    * Fullfør en ny oppføring i repositoriet.  
8. Merk den valgte raden i listen.
    * Velg LCS-repositoriumposten.  
    * Legg merke til at et registrert repositorium er merket med gjeldende leverandør, som betyr at bare konfigurasjoner som eies av denne leverandøren kan settes til dette repositoriet og derfor lastes opp til det valgte LCS-prosjektet.  
9. Klikk Åpne.
    * Åpne repositoriet for å vise listen over ER-konfigurasjoner. Den er tom hvis prosjektet ennå ikke er brukt for deling av ER-konfigurasjoner.  
10. Lukk siden.
11. Lukk siden.

## <a name="upload-configuration-into-lcs"></a>Laste opp konfigurasjon til LCS
1. Klikk Konfigurasjoner.
2. Velg Eksempelmodellkonfigurasjon i treet.
    * Velg en opprettet konfigurasjon som allerede er fullført.  
3. Finn og velg ønsket post i listen.
    * Velg versjonen av den valgte konfigurasjonen med statusen Fullført.  
4. Klikk Endre status.
5. Klikk Del.
    * Konfigurasjonsstatusen endres fra Fullført til Delt når den er publisert i LCS.  
6. Klikk OK.
7. Finn og velg ønsket post i listen.
    * Velg konfigurasjonsversjonen med statusen Delt.  
    * Legg merke til at statusen for den valgte versjonen er endret fra Fullført til Delt.  
8. Lukk siden.
9. Klikk Repositorier.
    * Denne lar deg åpne listen over repositorier for konfigurasjonsleverandøren Litware, Inc.  
10. Klikk Åpne.
    * Velg LCS-repositorium, og åpne det.  
    * Legg merke til at den valgte konfigurasjonen vises som et anleggsmiddel for det valgte LCS-prosjektet.  
    * Åpne LCS ved hjelp av https://lcs.dynamics.com. Åpne et prosjekt som ble brukt tidligere for registrering av repositoriet, åpne Aktivabibliotek for dette prosjektet og vis innholdet i aktivatypen Ger-konfigurasjonstypen – den opplastede ER-konfigurasjonen vil være tilgjengelig. Legg merke til at den opplastede LCS-konfigurasjonen kan importeres til en annen forekomst av Microsoft Dynamics 365 for Finance and Operations hvis leverandører har tilgang til dette LCS-prosjektet.  


