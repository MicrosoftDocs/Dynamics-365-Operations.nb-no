---
title: Opprette et purreforløp
description: Bruk denne oppgaveveiledningen til å opprette et purreforløp.
author: mikefalkner
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CollectionLetterCourse
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8cf5612fcd237ebaaede3f8f70da5eb443a94c34
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5842424"
---
# <a name="create-a-collection-letter-sequence"></a>Opprette et purreforløp

[!include [banner](../../includes/banner.md)]

Bruk denne oppgaveveiledningen til å opprette et purreforløp. Denne oppgaven bruker demonstrasjonsfirmaet USMF.

1. I navigasjonsruten går du til **Moduler > Kreditt og innkreving > Oppsett > Definer purreforløp**.
2. Klikk på **Ny**.
3. I **Purreforløp**-feltet angir du en sekvens-ID som representerer rekkefølgen. Den brukes når du oppretter en posteringsprofil.
4. Skriv inn en verdi i **Beskrivelse**-feltet.  Betalingsbetingelsene er valgfrie. Hvis du angir en verdi her, bruker purregebyrfakturaen disse betalingsbetingelsene i stedet for betalingsbetingelsene som er lagret med kunden.  
5. I **Purrekode**-feltet velger du koden for den første purringen du vil sende. Den første purringen opprettes i henhold til forfallsdatoen på fakturaen, verdien du angir for respittperioden i Dager-feltet på denne linjen, og annen informasjon du angir på denne linjen.  
6. Skriv inn en verdi i **Beskrivelse**-feltet. Valutaen for gebyret er som standard kundevalutaen. Denne valutakoden kan være forskjellig fra fakturavalutaen.  
7. Klikk på **Legg til** for å legge til den neste purringen som skal sendes i sekvensen. I mange tilfeller er den første purringen bare en advarsel. Du kan legge til gebyrer om nødvendig.  
8. I Purrekode-feltet velger du koden for den neste purringen som skal sendes i sekvensen.
9. Skriv inn en verdi i **Beskrivelse**-feltet.
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
25. Merk av for **Blokker** for å sperre kunden for videre leveranser og fakturering. Hvis du vil oppheve blokkeringen av kontoen, velger du **Nei** i feltet Fakturering og levering på vent på Kunder-siden.  
26. Utvid **Merknad**-hurtigfanen.
27. Angi teksten som skal vises på purringen for valgt purrekode. Du kan oversette denne teksten til flere språk ved hjelp av Oversettelser-menyen over notat-boksen.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]