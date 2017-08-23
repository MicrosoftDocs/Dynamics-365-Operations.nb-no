--- 
title: 'Definere syklustelling '
description: "Syklustelling er en lagerprosess som du kan bruke til å overvåke varer i lagerbeholdning."
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/23/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bibis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: f0d598bbd13406b27a23dcf349f6c81e758a9e61
ms.contentlocale: nb-no
ms.lasthandoff: 07/27/2017

---
# <a name="define-cycle-counting"></a>Definere syklustelling  

[!include[task guide banner](../../includes/task-guide-banner.md)]

Syklustelling er en lagerprosess som du kan bruke til å overvåke varer i lagerbeholdning. Denne oppgaveregistreringen viser hvordan du gjør følgende: definere standard opptellingsarbeidsprioritet, aktivere et menyelement for mobil enhet for å behandle både plukkings- og opptellingsoperasjoner, aktivere en utløser for opptellingsterskel når en lokasjon blir tom og aktivere en syklustellingsplan for en bestemt vare i et bestemt lager. Disse oppgavene utføres vanligvis av en lagersjef. Du kan gå gjennom denne fremgangsmåten i USMF-demonstrasjonsdataselskapet eller i dine egne data.


## <a name="set-the-priority-of-counting-work"></a>Angi prioritet for opptellingsarbeid
1. Gå til Lagerstyring > Oppsett > Lagerstyringsparametere.
2. Klikk kategorien for Syklustelling.
3. Angi et nummer i feltet Standardprioritet for arbeid for syklustelling.
    * Dette trinnet endrer prioriteten til syklustellingsarbeidet, sammenlignet med andre typer varer i lageret. Ved å skrive inn et tall som er lavere enn tallet for andre typer arbeid, kan du øke prioriteten for syklustellingsarbeidet.  
4. Klikk Lagre.
5. Lukk siden.

## <a name="enable-the-mobile-device"></a>Aktivere mobilenheten
1. Gå til Lagerstyring > Oppsett > Mobilenhet > Menyelementer på mobilenheten.
2. Klikk Ny.
3. Skriv inn en verdi i feltet Menyelementnavn.
4. Skriv inn en verdi i Tittel-feltet.
5. Velg Arbeid i feltet Modus.
6. Angi alternativet Bruk eksisterende arbeid til Ja.
    * Når du setter dette alternativet til Ja, vil systemet se etter eksisterende arbeid når menyelementet for mobilenhet brukes.  
7. Velg Systemstyrt i feltet Styrt av.
    * Når "Systemrettet" er valgt, kommer lagermedarbeideren til å åpne arbeid som er i definerte arbeidsklasser. (Vi vil opprette disse arbeidsklassene etterpå.)  
8. Vis eller skjul delen Arbeidsklasser.
    * Nå skal vi opprette to klasser for arbeid som skal brukes med dette menyelementet for mobil enhet. Når menyelementet brukes, spørres det etter disse arbeidsklassene, og arbeidet med høyest prioritet blir vist for brukeren.  
9. Klikk Ny.
10. Velg en verdi i feltet Arbeidsklasse-ID.
11. Klikk Ny.
12. Velg en verdi i feltet Arbeidsklasse-ID.
13. Klikk Lagre.
14. Lukk siden.
15. Gå til Lagerstyring > Oppsett > Mobilenhet > Meny på mobilenheten.
16. Finn og velg ønsket post i listen.
17. Velg menyelementet du har nettopp opprettet, i treet.
18. Klikk Rediger.
19. Klikk pilen for å legge til menyelementet i menyen.
20. Klikk Lagre.

## <a name="create-a-counting-threshold"></a>Opprette en opptellingsterskel
1. Gå til Lagerstyring > Oppsett > Syklustelling > Terskler for syklustelling.
2. Klikk Ny.
3. Skriv inn en verdi i feltet ID for syklustellingsterskel.
4. Angi alternativet Behandle syklustelling umiddelbart som Ja.
5. Skriv inn en verdi i feltet Beskrivelse.
6. Klikk Lagre.
7. Klikk Velg lokasjoner.
8. Merk den valgte raden i listen.
9. Velg en verdi i feltet Vilkår.
10. Klikk OK.
11. Lukk siden.

## <a name="create-a-cycle-count-plan"></a>Opprette en plan for syklustelling
1. Gå til Lagerstyring > Oppsett > Syklustelling > Planer for syklustelling.
2. Klikk Ny.
3. Skriv inn en verdi i feltet ID for syklustellingsplan.
4. Skriv inn en verdi i Beskrivelse-feltet.
5. Angi et tall i feltet Største antall syklustellinger.
6. Klikk Lagre.
7. Klikk Velg lokasjoner.
8. Merk den valgte raden i listen.
9. Velg en verdi i feltet Vilkår.
10. Klikk OK.
11. Angi et tall i feltet Dager mellom syklustellinger.
    * Hvis for eksempel feltet Dager mellom syklustellinger er angitt til 5, opprettes syklustellingsarbeidet hver femte dag. Hvis syklustellingsarbeid imidlertid behandles på dag tre, opprettes neste syklustellingsarbeid fem dager etter den siste syklustellingen ble behandlet, på dag 8.  
12. Klikk Lagre.
13. Klikk Ny.
14. Angi et nummer i Sekvensnummer-feltet.
    * Sorteringen er fra det laveste tallet til det høyeste tallet. Verdien må være over 0 (null).  
15. Merk den valgte raden i listen.
16. Skriv inn en verdi i feltet Beskrivelse.
17. Klikk Lagre.
18. Klikk Definer produktspørring.
19. Merk den valgte raden i listen.
20. Angi eller velg en verdi i Kriterier-feltet.
21. Klikk OK.
22. Lukk siden.


