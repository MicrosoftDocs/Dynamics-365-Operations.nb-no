---
title: Definer kompensasjonsprosess og beregn resultater
description: Kompensasjonsprosesser brukes til å fastslå nye kompensasjonsbeløp og -bonuser for ansatte som er registrert i faste og variable kompensasjonsplaner.
author: twheeloc
ms.date: 08/25/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: HRMCompProcess, HRMCompProcessLine, HRMCompEvent, HRMCompEventEmpl, HcmCompensationWorkspace
audience: Application User
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 196c907521bba5440f12149abcb2fc446c2aa523
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/04/2022
ms.locfileid: "8687058"
---
# <a name="define-compensation-process-and-calculate-results"></a>Definer kompensasjonsprosess og beregn resultater


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Kompensasjonsprosesser brukes til å fastslå nye kompensasjonsbeløp og -bonuser for ansatte som er registrert i faste og variable kompensasjonsplaner. Kompensasjonsprosesser kan kjøres flere ganger for å utføre hva-skjer-hvis-analyse, for å bekrefte at alle endringer og innstillinger er riktige. Dette vil opprette en kompensasjonsprosess, kjøre prosessen og vise resultatene. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.


## <a name="create-a-compensation-process"></a>Opprette en kompensasjonsprosess
1. Gå til **Kompensasjonsstyring** > **Prosess** > **Kompensasjonsprosesser**.
2. Klikk på **Ny kompensasjonsprosess**.
3. Skriv inn en verdi i **Prosess-feltet**.
4. Skriv inn en verdi i **Beskrivelse**-feltet.
5. Velg et alternativ i **Prosesstype**-feltet.
    * En syklus angir hvor lang tid som vurderes for å fastslå kompensasjon. Evalueringen tar hensyn til hvilke stillinger ansatte hadde, hvilke resultatvurderinger som skal tas med, beregningen av prosentandelen av tid den ansatte var ansatt i løpet av syklusen og så videre. Et eksempel på en startdato for syklus kan være den første dagen i det siste regnskapsåret.  
6. Angi en dato i **Syklusstart**-feltet.
    * Syklusens sluttdato er viktig fordi det er datoen som brukes til å fastslå hvilke ansatte som var aktivt ansatt og registrert i én eller flere kompensasjonsplaner.  
7. Angi en dato i **Sykluslutt**-feltet.
    * Aktiveringsdatoen for transaksjonen er datoen de nye kompensasjonssatsene skal tre i kraft. Mange firmaer inkluderer noen måneder mellom slutten på en syklus og tidspunktet de nye kompensasjonssatsene trer i kraft. Den ekstra tiden brukes til å behandle og gjennomgå den nye kompensasjonen.  
8. Angi en dato i feltet **Aktiveringsdato for transaksjon**.
    * Tidspunktdatoen brukes for variable kompensasjonsplaner som bestemmer den ansattes belønningsbeløp basert på kompensasjonssatsen til den ansatte på dette tidspunktet.  
    * Den faste lønnen for klassifisert ansettelsesdato brukes med faste kompensasjonsplaner med en ansettelsesregel med **prosent**. Ansatte som er ansatt mellom syklusens startdato og den klassifiserte ansettelsesdatoen for fast lønn får 100 % av den beregnede kompensasjonsøkningen i stedet for klassifisert prosent.  
9. Angi en dato i feltet **Fast lønn for klassifisert ansettelsesdato**.
    * Tidsfristen for gjennomgang er datoen da alle prosessresultater må være gjennomgått, slik at de kan lastes inn i den ansattes kompensasjonspost før aktiveringsdatoen for transaksjonen. Dette feltet er kun veiledende.  
10. Angi en dato i feltet **Tidsfrist for gjennomgang**.
11. Klikk på **Lagre**.

## <a name="set-up-the-compensation-plans-and-actions-for-a-compensation-process"></a>Konfigurere kompensasjonsplanene og -handlingene for en kompensasjonsprosess
1. Klikk på **Oppsett**.
    * **Oppsett**-siden brukes til å velge hvilke planer som skal behandles i denne kompensasjonsprosessen, og hvilke handlinger som skal utføres mot hver plan.  
2. Angi eller velg en verdi i **Plan**-feltet.
3. Klikk på **Lagre**.
4. Klikk på **Legg til**.
5. Velg en handlingstype for **egenkapital** i **Handling**-feltet.
6. Klikk på **Legg til**.
7. Velg en handlingstype for **personlig tillegg** i **Handling**-feltet.
    * Kompensasjonshandlinger kan kjedes sammen ved hjelp av feltet **Bruk forrige resultat** for å angi om den valgte handlingen skal bruke grunnlønnen til den ansatte eller resultatet av forrige handling som utgangspunkt for handlingens beregning.  
8. Velg **Ja** i feltet **Bruk forrige resultat**.
9. Klikk på **Legg til**.
10. Velg en **generell** handlingstype i **Handling**-feltet.
    * Forskjellige kompensasjonshandlingstyper aktiverer forskjellige felt. For en generell kompensasjonshandlingstype kan en økningsprosent eller et økningsbeløp angis.  
11. Velg alternativet **Velg økningsbeløp**.
12. Angi en verdi i **Økningsbeløp**-feltet.
13. Klikk på **Legg til**.
14. Velg en handlingstype for **forfremmelse** i **Handling**-feltet.
    * Handlingstypene Forfremmelse og Annen nivåendring lar brukerne gjøre manuelle justeringer i ansattkompensasjon. Anbefalinger kan aktiveres for disse handlingstypene samt andre handlingstyper, slik at du kan angi en ny verdi for anbefalt kompensasjon for en ansatt.  
15. Klikk på **Legg til**.
16. Velg et alternativ i **Type**-feltet.
    * Faste og variable kompensasjonsplaner kan kjøres i samme kompensasjonsprosess.  
17. Angi eller velg en verdi i **Plan**-feltet.
    * Bruk avmerkingsboksen **Aktiver betal for ytelse** for å bestemme om faste og variable kompensasjonsbeløp skal justeres basert på den ansattes ytelsesvurdering.  
    * Utnyttelse kan overstyres i variable kompensasjonsplaner.  
18. Klikk på **Lagre**.
19. Klikk på **Legg til**.
20. Lukk siden.

## <a name="run-the-compensation-process"></a>Kjøre kompensasjonsprosessen
1. Klikk **Kjør prosess**.
    * Kontrollen **Vis resultater for hendelsesbehandling** lar deg vise behandlingsmeldinger for den fullstendige kompensasjonsprosessen når behandlingen er fullført.  
2. Velg **Ja** i feltet **Vis resultater for hendelsesbehandling**.
3. Klikk på **OK**.

## <a name="view-the-results"></a>Vise resultatene
1. Klikk **Prosessresultater**.
2. Klikk **Ansattresultater**.
3. Finn og velg ønsket post i listen.
4. Utvid delen for **fast kompensasjon**.
    * Utvid hurtigfanene for å vise resultatene av prosessen. Hvis **Aktiver anbefalinger** ble avmerket for en kompensasjonshandling, aktiveres **Anbefaling**-feltene for denne handlingen.  
5. Finn og velg ønsket post i listen.
    * Resultatene for én enkelt ansatt kan vises ved å klikke **Vis resultater**.  
    * Du kan overskrive det beregnede kompensasjonsbeløpet ved å justere prosenten eller økningsbeløpet i **Anbefaling**-feltene.  
6. Angi en verdi i feltet for **anbefalt prosent**.
7. Finn og velg ønsket post i listen.
8. Angi en verdi i feltet for **anbefalt prosent**.
    * Omberegn kan brukes til å ignorere eventuelle endringer i den eksisterende posten og generere et nytt kompensasjonsresultat for den valgte ansatte.  
    * Når alle endringene er fullført for en ansatt, kan du endre statusen til **Godkjent**.  
9. Klikk på **Endre status**.
10. Klikk **Godkjent**.
    * Etter at posten er godkjent, kan den lastes til den ansattes offisielle kompensasjonspost. Den nye kompensasjonen trer i kraft på transaksjonsdatoen som er angitt i kompensasjonsprosessen.  



[!INCLUDE[footer-include](../includes/footer-banner.md)]
