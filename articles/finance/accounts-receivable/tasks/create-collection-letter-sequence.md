---
title: Opprette et purreforløp
description: Bruk denne prosedyren til å opprette et purreforløp.
author: JodiChristiansen
ms.date: 12/07/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CollectionLetterCourse
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: af5d0a001fbe705834e116516933be67f2de8826
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/10/2022
ms.locfileid: "8734165"
---
# <a name="create-a-collection-letter-sequence"></a>Opprette et purreforløp

[!include [banner](../../includes/banner.md)]

Bruk denne prosedyren til å opprette et purreforløp. Denne oppgaven bruker demonstrasjonsfirmaet USMF.

1. Gå til **Kreditt og innkreving > Oppsett > Definer purreforløp**.
2. Klikk på **Ny**.
3. I **Purreforløp**-feltet angir du en sekvens-ID som representerer rekkefølgen. Den brukes når du oppretter en posteringsprofil.
4. Skriv inn en verdi i **Beskrivelse**-feltet. Betalingsbetingelsene er valgfrie. Hvis du angir en verdi her, bruker purregebyrfakturaen disse betalingsbetingelsene i stedet for betalingsbetingelsene som er lagret med kunden.  
5. I **Purrekode**-feltet velger du koden for den første purringen du vil sende. Den første purringen opprettes i henhold til forfallsdatoen på fakturaen, verdien du angir for respittperioden i Dager-feltet på denne linjen, og annen informasjon du angir på denne linjen.  
6. Skriv inn en verdi i **Beskrivelse**-feltet. 
7. Standardvalutaen for gebyret er standard for juridisk enhet. Denne valutakoden kan være forskjellig fra fakturavalutaen.   
8. Klikk på **Legg til** for å legge til den neste purringen som skal sendes i sekvensen. I mange tilfeller er den første purringen bare en advarsel. Du kan legge til gebyrer om nødvendig.  
9. I **Purrekode**-feltet velger du koden for den neste purringen som skal sendes i sekvensen.
10. Velg inntektskontoen som skal brukes for gebyrer, i **Hovedkonto**-feltet.
11. Angi gebyret som skal belastes når denne purringen posteres.
12. Klikk rullegardinknappen i feltet **Merverdiavgiftsgruppe for vare** for å åpne oppslaget. Velg en mva-gruppe for vare hvis merverdiavgift må beregnes på gebyret.  
13. Klikk koblingen i den valgte raden i listen.
14. I feltet **Minste forfalte saldo** angir du den minste forfalte saldoen som kreves før en purring sendes.
15. I **Dager**-feltet angir du antall respittdager du vil tillate. Dette er antall dager etter forfallsdatoen som en purring kan genereres. Forfallsdatoen som brukes i beregningen, avhenger av plasseringen av purringen i purreforløpet:
    - Respittperioden for purring 1 er relativ til forfallsdatoen på fakturaen.
    - Respittperioden for purringer 2 og høyere er relativ til datoen da forrige purring posteres eller skrives ut, avhengig av valget i feltet Oppdatere purrekode på siden Kundeparametere.  
16. Klikk **Legg til** for å legge til den siste purringen i sekvensen. Du kan legge til opptil fem purrekoder for et purreforløp.  
17. I **Purrekode**-feltet velger du koden for den neste purringen som skal sendes i sekvensen.
18. Skriv inn en verdi i **Beskrivelse**-feltet.
19. Angi de ønskede verdiene i **Hovedkonto**-feltet.
20. Angi et tall i feltet **Gebyr i valuta**.
21. Klikk rullegardinknappen i feltet **Merverdiavgiftsgruppe for vare** for å åpne oppslaget.
22. Klikk koblingen i den valgte raden i listen.
23. Angi et nummer i feltet **Minste forfalte saldo**.
24. Angi et tall i **Dager**-feltet.
25. Merk av for **Blokker** for å sperre kunden for videre leveranser og fakturering. Hvis du vil oppheve blokkeringen av kontoen, velger du **Nei** i feltet **Fakturering og levering på vent** på **Kunder**-siden.  
26. Utvid **Merknad**-hurtigfanen.
27. Angi teksten som skal vises på purringen for valgt purrekode. Du kan oversette denne teksten til flere språk ved hjelp av **Oversettelser**-menyen ovenfor notatboksen.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
