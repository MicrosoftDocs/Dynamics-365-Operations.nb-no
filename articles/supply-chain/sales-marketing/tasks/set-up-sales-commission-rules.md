--- 
title: Definere regler for salgsprovisjon
description: "Denne fremgangsmåten viser hvordan du konfigurerer og aktiverer salgprovisjonsberegning og sporing."
author: omulvad
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CommissionCustomerGroup, CommissionItemGroup, CommissionSalesGroup, CommissionSalesMember, DirPartyLookup, CommissionCalc, InventPosting, CustTable, EcoResProductDetailsExtended
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 8d81765884f741443d1c0f5b0cb8bc545945e1a1
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-sales-commission-rules"></a>Definere regler for salgsprovisjon

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåten viser hvordan du konfigurerer og aktiverer salgprovisjonsberegning og sporing. Fremgangsmåten viser hvordan du oppretter både kunde- og varegrupper for provisjon, og deretter hvordan du kobler en valgt kunde og produktet til de respektive gruppene. Disse gruppene brukes deretter i oppsettet for beregning av provisjon for å opprette kombinasjonen av en kunde, vare og selgere som må samsvare med salgsordren for å kvalifisere selgerne til en provisjon. Det er valgfritt å opprette kunde- og provisjonsgrupper, ettersom beregning av provisjonen også kan gjøres for en individuell kunde og/eller vare. Du kan kjøre denne fremgangsmåten i demonstrasjonsselskapet USMF eller ved hjelp av dine egne data.


## <a name="set-up-commission-groups-and-commission-rates"></a>Definere provisjonsgrupper og provisjonssatser
1. Gå til Salg og markedsføring > Provisjoner > Kundegrupper for provisjon.
2. Klikk Ny.
3. Skriv inn en verdi i feltet Gruppe.
4. Skriv inn en verdi i Navn-feltet.
5. Klikk Lagre.
6. Lukk siden.
7. Gå til Salg og markedsføring > Provisjoner > Varegrupper.
8. Klikk Ny.
9. Skriv inn en verdi i feltet Gruppe.
10. Skriv inn en verdi i Navn-feltet.
11. Lukk siden.
12. Gå til Salg og markedsføring > Provisjoner > Salgsgrupper.
    * En provisjonssalgsgruppe angir de ansatte i selgerroller som er berettiget til å motta en provisjon når en kunde som er knyttet til den relevante salgsgruppen kjøper visse varer.  
    * I USMF-demodatafirmaet er det en salgsgruppe kalt Selgere USA.  
13. Klikk Generelt i handlingsruten.
14. Klikk Selger.
    * Selger-siden viser en liste over firmaets selgere som er knyttet til en bestemt provisjonsgruppe. Du kan tilordne flere selgere til samme gruppe og definere deres respektive del av totale provisjonsgebyret som en prosentverdi. Den totale provisjonsandelen for alle ansatte må ikke overskride 100.  
15. Merk den valgte raden i listen.
16. Klikk Rediger.
17. Angi Provisjonsandel som 50.
18. Klikk Ny.
19. Klikk rullegardinknappen i Navn-feltet for å åpne oppslaget.
20. Bruk hurtigfilteret for å søke etter poster. Du kan for eksempel filtrere på Navn-feltet med verdien Susan Burk.
21. Klikk Velg.
22. Angi Provisjonsandel som 50.
23. Klikk Lagre.
24. Gå til Salg og markedsføring > Provisjoner > Provisjonsberegning.
    * Du kan definere provisjonssatsen som ansatt skal motta for en salgstransaksjon når den inneholder forhåndangitt kombinasjon av kunde og produkt, på siden Provisjonsberegning. Som en del av provisjonssatsoppsettet, må du angi grunnlaget for provisjonsberegning og om den skal inkludere eller ekskludere rabatter. Du kan også angi en gyldighetsperiode for når provisjonssatsen er aktiv.  
25. Klikk Ny.
26. Velg Gruppe i Varekode-feltet.
27. Klikk rullegardinknappen i feltet Varerelasjon for å åpne oppslaget.
28. Finn og velg gruppen du opprettet tidligere, i listen.
29. Klikk koblingen i den valgte raden i listen.
30. Velg Gruppe i Kundekode-feltet.
31. Klikk rullegardinknappen i Kunderelasjon-feltet for å åpne oppslaget.
32. Velg gruppen du definerte tidligere, i listen.
33. I Selger- relasjon-feltet klikker du rullegardinknappen for å åpne oppslaget.
34. Finn og velg ønsket post i listen.
    * Behold alternativet "Før linjerabatt".  
    * Behold alternativet "Omsetning" som grunnlag for beregning av provisjonsverdi.    
35. Angi et tall i feltet Provisjonssats i prosent.
36. Klikk Lagre.

## <a name="setting-up-commission-posting"></a>Definere provisjonspostering
1. Gå til Salg og markedsføring > Provisjoner > Provisjonspostering.
    * Provisjonsgebyrer betales til ansatte, og må derfor defineres til å sikre riktig økonomisk postering til de aktuelle kontoene i økonomimodulen. Dette gjøres på siden Provisjonspostering. Gå gjennom oppsettet som er tilgjengelig for det gjeldende firmaet. Vanligvis posteres provisjonsbeløpene til en dedikert utgiftskonto og motregnes til en egen konto for leverandører. Hvis du ikke har satt opp regler for provisjonspostering, vil systemet ikke kunne fullføre fakturering av en salgsordre som har kvalifiserte provisjoner.  
2. Lukk siden.

## <a name="assign-a-commission-group-to-a-customer-and-a-product"></a>Tilordne en Provisjonsgruppe til en kunde og et produkt
1. Gå til Salg og markedsføring > Kunder > Alle kunder.
2. Finn og velg ønsket post i listen.
3. Klikk koblingen i den valgte raden i listen.
4. Klikk Rediger
5. Utvid delen Standarder for salgsordrer.
6. Klikk rullegardinknappen i feltet Provisjonsgruppe for å åpne oppslaget.
7. Velg gruppen du opprettet tidligere, i listen.
8. Klikk rullegardinknappen i feltet Salgsgruppe for å åpne oppslaget.
9. Finn og velg ønsket post i listen.
10. Klikk Lagre.
11. Gå til Behandling av produktinformasjon > Produkter > Frigitte produkter.
12. Bruk hurtigfilteret for å søke etter poster. Du kan for eksempel filtrere på Varenummer-feltet med verdien T0020.
13. Klikk koblingen i den valgte raden i listen.
14. Klikk Rediger
15. Utvid Selg-delen.
16. Klikk rullegardinknappen i feltet Provisjonsgruppe for å åpne oppslaget.
17. Velg provisjonsgruppen du opprettet tidligere, i listen.


