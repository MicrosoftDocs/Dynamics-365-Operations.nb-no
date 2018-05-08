--- 
title: Aktivere utskrift av nummerskiltetikett
description: "Denne fremgangsmåten tillater automatisk utskrift av en SSCC-etikett (Serial Shipping Container Code) etter at den siste varen er plukket fra lageret i en arbeidsprosess for salgsplukk."
author: perlynne
manager: AnnBe
ms.date: 11/03/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 6d186bf7e4aee8cfa97adbd90b9090085e842f9b
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="enable-license-plate-label-printing"></a>Aktivere utskrift av nummerskiltetikett

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåten tillater automatisk utskrift av en SSCC-etikett (Serial Shipping Container Code) etter at den siste varen er plukket fra lageret i en arbeidsprosess for salgsplukk. Du kan kjøre denne prosedyren i demonstrasjonsdataselskapet USMF. Hvis du skal kjøre det på dine egne data, må du ha en nummerserie som er definert for nummerskilt. Du må definere en etikettskriver før du begynner. Gå til Organisasjonsstyring > Oppsett > Nettverksskrivere. I handlingsruten velger du Alternativer, og deretter klikker du Last ned installasjonsprogram for dokumentrutingsagent. Kjør installasjonsprogrammet og kontroller at du har en fungerende skriver satt til Aktiv før du fortsetter med prosedyren.


## <a name="set-up-the-gs1-company-prefix"></a>Angi GS1-firmaprefikset
1. Gå til Lagerstyring > Oppsett > Lagerstyringsparametere.
2. I feltet GS1-firmaprefiks angir du det 7-sifrede GS1-firmanummeret.
3. Klikk Lagre.
4. Lukk siden.

## <a name="setup-the-sscc-license-plate-number-sequence"></a>Konfigurasjon av nummerserien for SSCC-skiltnummeret
1. Gå til Organisasjonsadministrasjon > Nummerserier > Nummerserier.
2. Velg et alternativ i Område-feltet.
3. Velg et alternativ i Referanse-feltet.
4. Skriv inn en verdi i feltet Firma.
5. Merk den valgte raden i listen.
6. Klikk koblingen i den valgte raden i listen.
7. Utvid seksjonen Segmenter.
8. Klikk Rediger.
9. Merk den første raden i tabellen Segmenter
10. Klikk Fjern.
11. Klikk Fjern.
12. Klikk Lagre.
13. Lukk siden.

## <a name="create-the-document-route-layout"></a>Opprett dokumentruteoppsettet
1. Gå til Lagerstyring > Oppsett > Dokumentruting > Dokumentrutingsoppsett.
    * Aktiver SSCC-oppsettet.  
2. Klikk Ny.
3. Skriv inn en verdi i feltet Oppset-ID.
4. Skriv inn en verdi i feltet Beskrivelse.
5. Finn og velg ønsket post i listen.
6. Klikk Sett inn i slutten av teksten.
7. Klikk Lagre.
8. Lukk siden.

## <a name="set-up-the-document-routing"></a>Konfigurer dokumentrutingen
1. Gå til Lagerstyring > Oppsett > Dokumentruting > Dokumentruting.
2. Velg et alternativ i feltet Arbeidsordretype.
3. Klikk Ny.
4. Skriv inn en verdi i Lager-feltet.
5. Skriv inn en verdi i Navn-feltet.
6. Klikk Ny.
7. Angi eller velg en verdi i feltet Oppsett-ID.
8. I Navn-feltet angir du navnet på skriveren du vil bruke.
9. Klikk Lagre.
10. Lukk siden.

## <a name="create-mobile-device-menu"></a>Opprett mobilenhetsmeny
1. Gå til Lagerstyring > Oppsett > Mobilenhet > Menyelementer på mobilenheten.
2. Klikk Ny.
3. Skriv inn en verdi i feltet Menyelementnavn.
4. Skriv inn en verdi i Tittel-feltet.
5. Velg et alternativ i Modus -feltet.
6. Velg Ja i feltet Bruk eksisterende arbeid.
7. Velg Ja i Generer nummerskilt-feltet.
8. Utvid Arbeidsklasser-delen.
9. Klikk Ny.
10. Skriv inn en verdi i feltet Arbeidsklasse-ID.
11. Klikk Lagre.
12. Lukk siden.
13. Gå til Lagerstyring > Oppsett > Mobilenhet > Meny på mobilenheten.
14. Finn og velg ønsket post i listen.
15. I treet velger du menyelementet du har opprettet før.
16. Klikk Rediger
17. Klikk pilen for å legge til menyelementet i menyen.
18. Klikk Lagre.
19. Lukk siden.

## <a name="update-a-work-template"></a>Oppdater en arbeidsmal
1. Gå til Lagerstyring > Oppsett > Arbeid > Arbeidsmaler.
2. Finn og velg ønsket post i listen.
3. Klikk Rediger.
4. Klikk Ny.
5. Merk den valgte raden i listen.
6. Velg Skriv ut i Arbeidstype-feltet.
7. Angi eller velg en verdi i feltet Arbeidsklasse-ID.
8. Klikk koblingen i den valgte raden i listen.
9. Klikk Flytt opp.
10. Klikk Lagre.
11. Lukk siden.


