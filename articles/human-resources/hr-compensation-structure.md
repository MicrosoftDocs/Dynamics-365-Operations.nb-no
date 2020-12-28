---
title: Utvikle en kompensasjonsstruktur
description: Denne artikkelen leder deg gjennom prosessen med å opprette en fast kompensasjonsplan og registrere ansatte i planen gjennom rettighetsregler.
author: andreabichsel
manager: AnnBe
ms.date: 02/10/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: DefaultDashboard, HcmCompensationWorkspace, HcmCompFixedPlansPart, HRMCompFixedPlanTable, HRMCompCreateGridDialog, HRCCompGridView, HRMCompEligibility,  HRCCompGrid
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 124d0f7f83feebabf622f00732c25bfa0f6eccdd
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4419922"
---
# <a name="develop-a-compensation-structure"></a>Utvikle en kompensasjonsstruktur

Denne artikkelen leder deg gjennom prosessen med å opprette en fast kompensasjonsplan og registrere ansatte i planen gjennom rettighetsregler. Denne artikkelen bruker USMF-demodataene og gjelder ansvarlige for kompensasjon og fordeler.

## <a name="create-a-fixed-compensation-plan"></a>Opprette en fast kompensasjonsplan

1. Velg **Kompensasjonsstyring**.

2. Velg **Faste kompensasjonsplaner**.

3. Velg **Ny**.

4. Angi en verdi i **Plan**-feltet.

5. Angi en verdi i feltet **Beskrivelse**.

6. Angi en dato i feltet **Gyldighetsdato**.

7. I **Type**-feltet velger du om den faste kompensasjonsplanen er en plan for **segment**, **klasse** eller **trinn**.

8. Avmerkingsboksen **Anbefaling tillatt** fungerer som en standardverdi for alle handlinger som er lagt til i denne planen i en prosesshendelse. Ved å tillate anbefalinger kan du overstyre det beregnede retningslinjebeløpet ved behandling av kompensasjon.

9. Med feltet **Utenfor områdetoleranse** kan du angi hvordan du vil håndtere kompensasjonsbeløp som faller utenfor det angitte kompensasjonsstrukturområdet for det angitte nivået. Hvis du angir feltet **Utenfor område-toleranse** til **Ingenl**, kan du bruke et hvilket som helst kompensasjonsbeløp. **Myk toleranse** varsler brukeren hvis kompensasjonsbeløpet er mindre enn det minste eller større enn det maksimale referansepunktbeløpet for dette nivået. Brukeren kan ignorere advarselen og fortsette. **Hard toleranse** genererer en feil hvis en ansatts kompensasjon er utenfor de minste og største referansepunktene for nivået, og justerer automatisk den ansattes kompensasjon slik at den faller innenfor området.

10. Feltet **Ansettelsesregel** beregner kompensasjonen til en ansatt i løpet av en prosesshendelse. En **ansettelsesregel** med **prosent** beregner en økning som er fordelt på hele tiden arbeideren har vært ansatt i syklusen.

11. Skriv inn en verdi i **Valuta**-feltet.

12. Angi eller velg en verdi i feltet **Konverteringer av lønnssats**.

13. Vis delen **Områdeutnyttelsesmatrise**. Du kan også legge til områdeutnyttelsesposter for å få ansatte til midtpunktet raskere og øke tiden det tar å nå det maksimale antallet av området.

14. Velg **Lagre**. Dermed aktiveres knappen **Angi kompensasjon**, og du kan fortsette å definere kompensasjonsstrukturen for planen.

15. Velg **Angi kompensasjon**. Du kan opprette en kompensasjonsstruktur på en av følgende tre måter:

    - Opprett en helt ny struktur ved å velge et sett med referansepunkt og legge til nivåene for å opprette din egen struktur.
    - Kopier en kompensasjonsstruktur fra en eksisterende plan som utgangspunkt, og endre den for den nye planen.
    - Velg et eksisterende kompensasjonsrutenett. Hvis en annen plan allerede bruker kompensasjonsrutenettet, gjenspeiler den andre planen også endringer du gjør i rutenettet.

16. Velg **Opprett ny fra eksisterende kompensasjonsmatrise**.

17. Angi eller velg en verdi i feltet **Kopier fra rutenett**. Du kan også endre navnet på det nye kompensasjonsrutenettet som du oppretter ved å kopiere det valgte rutenettet.

18. Velg **OK**.

19. Velg **Masseendring**. Ved hjelp av **Masseendring** kan du beholde kompensasjonsmatrisebeløpene ved å bruke en økning i prosent eller et flatt beløp på én eller flere nivåer eller referansepunkt.

20. Angi et tall i **Justeringsbeløp**-feltet.

21. Merk eller fjern merking for alle rader i listen.

22. Klikk **Bruk på rutenett**.

23. Lukk siden. Når du har opprettet kompensasjonsstrukturen, kan du velge hvilke av referansepunktene som skal brukes som kontrollpunktet for den faste kompensasjonsplanen. Kontrollpunktet brukes til å beregne den ansattes Komp.grad.

24. Angi eller velg en verdi i feltet **Kontrollpunkt**.

25. Lukk siden.

## <a name="create-an-eligibility-rule-for-the-fixed-compensation-plan"></a>Opprette en rettighetsregel for den faste kompensasjonsplanen

Du kan ikke tilordne en fast kompensasjonsplan til en ansatt før du definerer rettighetsregler for planen.  

1. Velg **Rettighetsregler**.

2. Velg **Ny**.

3. Angi eller velg en verdi i feltet **Rettighet**.

4. Angi en verdi i feltet **Beskrivelse**.

5. Angi en dato i feltet **Gyldighetsdato**. Både faste og variable kompensasjonsplaner bruker rettighetsregler. Velg plantypen i **Type**-feltet.

6. Angi eller velg en verdi i **Plan**-feltet. Velg kriteriene en ansatt må oppfylle for å være kvalifisert for kompensasjonsplanen. Vilkårene kan omfatte:

    - **Avdeling**
    - **Fagforening**
    - **Sted** (**Kompensasjonsområde**)
    - **Jobb**
    - **Funksjon**
    - **Jobbtype**
    - **Kompensasjonsnivå**
    
    Den ansatte må oppfylle alle angitte kriterier for å være kvalifisert for kompensasjonsplanen. Hvis du ikke angir kriterier, er alle ansatte kvalifisert for kompensasjonsplanen. Hvis en ansatt ikke oppfyller kriteriene angitt i rettighetsregelen, eller en rettighetsregel ikke er angitt for en kompensasjonsplan, vises ikke kompensasjonsplanen i oppslaget når du oppretter en post for fast kompensasjon for en ansatt.

7. Lukk siden.

8. Lukk siden.

