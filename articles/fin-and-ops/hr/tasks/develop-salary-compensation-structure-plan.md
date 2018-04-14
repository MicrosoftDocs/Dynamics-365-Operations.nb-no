--- 
title: "Utvikle struktur og planer for lønn/kompensasjon"
description: "Denne oppgaveveiledningen veileder deg gjennom prosessen med å opprette en fast kompensasjonsplan og aktivere ansatte som skal registreres i planen gjennom rettighetsregler."
author: kherr75
manager: AnnBe
ms.date: 11/01/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations, Talent
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 63a02a64ff28531bae950f1b61d9167eaa0b0373
ms.openlocfilehash: 7fd32467cfbc8c30b398659d16b268f183b6b3d3
ms.contentlocale: nb-no
ms.lasthandoff: 11/01/2017

---
# <a name="develop-salarycompensation-structure-and-plans"></a>Utvikle struktur og planer for lønn/kompensasjon

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Denne oppgaveveiledningen veileder deg gjennom prosessen med å opprette en fast kompensasjonsplan og aktivere ansatte som skal registreres i planen gjennom rettighetsregler. Demonstrasjonsdataselskapet USMF er brukt til å opprette denne oppgaven, og oppgaven er ment for kompensasjons- og fordelsansvarlig.


## <a name="create-fixed-compensation-plan"></a>Opprette fast kompensasjonsplan
1. Klikk Kompensasjonsstyring.
2. Klikk Faste kompensasjonsplaner.
3. Klikk Ny.
4. Skriv inn en verdi i Plan-feltet.
5. Skriv inn en verdi i feltet Beskrivelse.
6. Angi en dato i feltet Gyldighetsdato.
7. Velg om den faste kompensasjonsplanen er en plan for segment, klasse eller trinn i Type-feltet.
8. Avmerkingsboksen Anbefaling tillatt fungerer som en standardverdi for alle handlinger som er lagt til i denne planen i en prosesshendelse.  Ved å tillate anbefalinger kan du overstyre det beregnede retningslinjebeløpet ved behandling av kompensasjon.
9. Med Utenfor område-toleransen kan du angi hvordan du vil håndtere kompensasjonsbeløp som faller utenfor det angitte kompensasjonsstrukturområdet for det angitte nivået.  En Utenfor område-toleranse på Ingen tillater bruk av et hvilket som helst kompensasjonsbeløp.  En Myk toleranse varsler brukeren hvis kompensasjonsbeløpet er mindre enn det minste referansepunktbeløpet for dette nivået, eller større enn det maksimale beløpet for dette nivået. Brukeren kan ignorere advarselen og fortsette.  En Hard toleranse genererer en feil hvis en ansatts kompensasjon er satt utenfor de minste og største referansepunktene for nivået, og justerer automatisk den ansattes kompensasjon slik at den faller innenfor området.
10. Feltet Ansettelsesregel brukes når en prosesshendelse for kompensasjon kjøres for å beregne den ansattes kompensasjon.  En ansettelsesregel med prosent beregner en økning som er fordelt på hele tiden arbeideren har vært ansatt i syklusen.
11. Skriv inn en verdi i Valuta-feltet.
12. Angi eller velg en verdi i feltet Konverteringer av lønnssats.
13. Vis delen Områdeutnyttelsesmatrise.
    * Du kan også legge til områdeutnyttelsesposter for å få ansatte til midtpunktet raskere og øke tiden det tar å nå det maksimale antallet av området.  
14. Nå må du lagre den faste kompensasjonsplanen for å aktivere knappen Angi kompensasjon og fortsette med å definere kompensasjonsstrukturen for planen.  Klikk Lagre.
15. Klikk Angi kompensasjon.
    * Det finnes tre måter å opprette en kompensasjonsstruktur. 1: Opprette en helt ny struktur ved å velge et sett med referansepunkt og legge til nivåene for å opprette din egen struktur. 2: Kopiere en kompensasjonsstruktur fra en eksisterende plan som utgangspunkt, og endre den for den nye planen. 3: Velge et eksisterende kompensasjonsrutenett. Hvis kompensasjonsrutenettet allerede brukes av en annen plan, gjenspeiles også endringer som gjøres i rutenettet i den andre planen.  
16. Merk av for alternativet Opprett ny fra eksisterende kompensasjonsmatrise.
17. Angi eller velg en verdi i feltet Kopier fra rutenett.
    * Du kan også endre navnet på det nye kompensasjonsrutenettet som opprettes som en kopi av det valgte rutenettet.  
18. Klikk OK.
19. Klikk Masseendring.
    * Ved hjelp av masseendring kan du beholde kompensasjonsmatrisebeløpene ved å bruke en økning i prosent eller et flatt beløp på én eller flere nivåer og/eller referansepunkt.  
20. Angi et tall i Justeringsbeløp-feltet.
21. Merk eller fjern merking for alle rader i listen.
22. Klikk Bruk på rutenett.
23. Lukk siden.
    * Når du har opprettet eller valgt en kompensasjonsstruktur, kan du velge hvilke av referansepunktene som skal brukes som kontrollpunktet for den faste kompensasjonsplanen.  Kontrollpunktet brukes til å beregne den ansattes Komp.grad.  
24. Angi eller velg en verdi i feltet Kontrollpunkt.
25. Lukk siden.

## <a name="create-an-eligibility-rule-for-the-new-fixed-compensation-plan"></a>Opprette en rettighetsregel for den nye kompensasjonsplanen
    * Den nye faste kompensasjonsplanen kan ikke tilordnes til en ansatt før rettighetsregler er definert for planen.  
1. Klikk Rettighetsregler.
2. Klikk Ny.
3. Skriv inn en verdi i Rettighet-feltet.
4. Skriv inn en verdi i feltet Beskrivelse.
5. Angi en dato i feltet Gyldighetsdato.
    * Rettighetsregler brukes for både faste og variable kompensasjonsplaner.  I Type-feltet velger du hvilken type plan dette settet med rettighetsregler gjelder.  
6. Angi eller velg en verdi i Plan-feltet.
    * Velg kriteriene en ansatt må oppfylle for å være kvalifisert for kompensasjonsplanen. Kriterier kan inneholde en avdeling, fagforening, plassering (kompensasjonsområde), jobb, funksjon, jobbtype eller kompensasjonsnivå. Den ansatte må oppfylle alle angitte kriterier for å være kvalifisert for kompensasjonsplanen. Hvis ingen kriterier er angitt, er alle ansatte kvalifisert for kompensasjonsplanen. Hvis en ansatt ikke oppfyller kriteriene angitt i rettighetsregelen, eller en rettighetsregel ikke er angitt for en kompensasjonsplan, vises ikke kompensasjonsplanen i oppslaget når du oppretter en post for fast kompensasjon for en ansatt.  
7. Lukk siden.
8. Lukk siden.


