--- 
title: Generere og behandle kunderabatter
description: "Denne fremgangsmåten beskriver hvordan du behandler kunderabatter fra kravgenerering til de overføres som avsetninger til kunder."
author: omulvad
manager: AnnBe
ms.date: 02/17/2016
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
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: fb5053ac5c5f9218b95d14baf4ea78f7a40479ff
ms.contentlocale: nb-no
ms.lasthandoff: 07/27/2017

---
# <a name="generate-and-process-customer-rebates"></a>Generere og behandle kunderabatter

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåten beskriver hvordan du behandler kunderabatter fra kravgenerering til de overføres som avsetninger til kunder. Den hjelper deg gjennom et konkret eksempel for å forklare hvordan forskjellige betingelsene på rabattlinjene påvirker de endelige beløpene som krediteres til kunden. Du må bruke USMF-demodatafirmaet og utføre følgende oppgaver før du starter veiledningen: (1) Gå til siden Kundeparametere, og utvid kategorien Priser og deretter kategorien Prisdetaljer, og kontroller at alternativet Aktiver prisdetaljer er satt til Ja. (2) Gå til siden Rabattavtaler, og velg kunderabattavtalen: USMF-000001. Hvis Arbeidsflytgodkjenningsstatus-feltet ikke er satt til Godkjent, må du klikke Validering i handlingsruten for å godkjenne.


## <a name="review-a-customer-rebate-agreement"></a>Se over en kunderabattavtale
1. Gå til Salg og markedsføring > Kunderabatter > Rabattavtaler.
    * De neste trinnene ser på betingelsene i avtalen USMF-000001. Dette gjør det enklere å forstå hvordan kundekredittverdiene beregnes senere i prosedyren.  
    * Avtalen er for en enkeltkunde, i dette eksemplet kunde US-009.  
    * Rabatter gis til kunden når de kjøper et bestemt produkt. I dette tilfellet har produktet varenummeret T0020.   
    * Kundens salgsytelse, som rabattbeløpene beregnes mot, skal akkumuleres på ukentlig basis.  
    * Innstillingen for Pris fra er Brutto, noe som betyr at denne linjens salgsbeløp, som er grunnlag for beregning av kravet, ikke reduseres av linjerabatten.  
    * Feltet Linjeskifttype for rabatt viser metoden for beregning av rabatter. I dette tilfellet settes salgsmål som rabattene skal beregnet mot, til Antall.   
    * Avtalelinjene angir rabattbeløpstypen, den faktiske rabattverdien og tersklene. I dette eksemplet vil kunden oppnå en rabatt på 20 USD per enhet som er solgt, hvis de ukentlige kjøp av produktet er innenfor 1 til 50 enheter; og en rabatt på 40 USD per enhet som er solgt, hvis de kjøper over 50 enheter.  
2. Lukk siden.

## <a name="generate-rebate-claims"></a>Generere rabattkrav
1. Gå til Salg og markedsføring > Salgsordrer > Alle salgsordrer.
2. Klikk Ny.
    * Hvis du vil etterligne måten som rabattkrav genereres på, er den neste oppgaven til å opprette en salgsordre, der produktet og antallet vil kvalifisere den aktuelle kunden for en rabatt.  
3. Angi eller velg en verdi i Kundekonto-feltet.
4. Klikk OK.
5. Angi eller velg en verdi i Varenummer-feltet.
6. Sett verdien for Antall til 40.
7. Klikk Salgsordrelinje.
8. Klikk Prisdetaljer.
    * Hvis du ikke ser dette alternativet, er det fordi du ikke har angitt alternativet Aktiver prisdetaljer som Ja før du startet veiledningen.  
9. Utvid delen Rabatter.
    * Kategorien Rabatter viser alle rabattavtaler som gjelder for gjeldende ordrelinje, og viser beregnet rabattbeløp. Legg merke til at beløpene som vises er bare indikasjoner på hva fremtidig rabattkrav kan bli. De faktiske rabattbeløpene kan være forskjellig avhengig av: det totale salgsvolumet kunden har oppnådd under en periodisk rabattavtale; om kunden hadde returnert alle eller et delvist antall; og om den aktuelle salgsordren er fakturert.  
10. Lukk siden.
11. Klikk Legg til linje.
12. Angi eller velg en verdi i Varenummer-feltet.
13. Sett verdien for Antall til 60.
14. Klikk Lagre.
15. Klikk Faktura i handlingsruten.
16. Klikk Faktura.
17. Utvid seksjonen Parametere.
18. Velg Alle i feltet Antall.
19. Klikk OK.
20. Klikk OK.

## <a name="process-rebate-claims"></a>Behandle rabattkrav
1. Gå til Salg og markedsføring > Kunderabatter > Rabatter.
    * Siden Rabatter fungerer en arbeidsbenk der kan du gå gjennom, godkjenne og behandle rabattkrav. Nå vil du behandle krav som er opprettet som et resultat av fakturering av en salgsordre for kunden US-009, som rabattavtalen USMF-000001 gjelder for.   
    * Den første linjen representerer et rabattkrav for 800 USD, som er basert på salget av 40 enheter av produkt T0020, beregnet som 20 USD per enhet. Dette tilsvarer betingelsene for det avbruddspunktet for antall i rabattavtalen.  
    * Andre kravet er for USD 2 400, som er basert på salget av 60 enheter av produkt T0020, beregnet på 40 USD per enhet, i henhold til det andre avbruddspunktet for antall i avtalen.  
    * Begge krav er i tilstanden "Som skal beregnes". Dette betyr at de er knyttet til en avtale som sporer kundens salgsytelse periodisk og at de må beregnes på nytt for å ta hensyn til totalvolumet for salg i den aktuelle perioden.   
2. Klikk Summer.
3. Angi eller velg en verdi i feltet Kunde.
4. Velg dagens dato i Startdato-feltet.
5. Klikk OK.
    * Som et resultat av funksjonen Summer, har det estimerte kravbeløpet nå blitt justert for å ta hensyn til at kundens totale salgsvolum i den aktuelle perioden er høyere enn da den første rabatten ble generert. Mer spesifikt, fordi totalt antall kjøpt har nådd 100 enheter, kvalifiserer kunden nå for 40 USD per enhet (i henhold til avtalens andre avbruddspunkt for antall) eller 400 USD av totalt rabattbeløp. Forskjellen er registrert som en ny "justering" av krav for ekstra 800 USD. Statusen for rabattkravet som er inkludert i den oppdaterte summen er nå satt til Beregnet.   
6. Merk alle rader i listen.
7. Klikk Godkjenn.
8. Velg Behandle.
9. Angi eller velg en verdi i feltet Kunde.
10. Klikk OK.
    * En melding viser at rabatten ble behandlet, og statusen for kravene har blitt endret til Merk. Dette betyr at som et resultat av en rabattavsetningsjournal som posteres: a) kravene er nå overført til den midlertidige kundesaldoen som fradrag; b) avsetningskontoen for rabatt er kreditert for å representere den fremtidige gjelden for kunden. og c) utgiftskontoen for rabatten har blitt debitert, for å føre kostnadene påløpt i forbindelse med salg.   

