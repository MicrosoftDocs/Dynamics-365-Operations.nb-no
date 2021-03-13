---
title: Definere regler for salgsprovisjon
description: Denne fremgangsmåten viser hvordan du konfigurerer og aktiverer salgprovisjonsberegning og sporing.
author: omulvad
manager: tfehr
ms.date: 06/21/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CommissionCustomerGroup, CommissionItemGroup, CommissionSalesGroup, CommissionSalesMember, DirPartyLookup, CommissionCalc, InventPosting, CustTable, EcoResProductDetailsExtended, CommissionEmplSalesGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b49865cf9d4073c2da7aa6ccc610b92055c711c1
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010727"
---
# <a name="set-up-sales-commission-rules"></a>Definere regler for salgsprovisjon

[!include [banner](../../includes/banner.md)]

Denne fremgangsmåten viser hvordan du konfigurerer og aktiverer salgprovisjonsberegning og sporing. Fremgangsmåten viser hvordan du oppretter både kunde- og varegrupper for provisjon, og deretter hvordan du kobler en valgt kunde og produktet til de respektive gruppene. Disse gruppene brukes deretter i oppsettet for beregning av provisjon for å opprette kombinasjonen av en kunde, vare og selgere som må samsvare med salgsordren for å kvalifisere selgerne til en provisjon. Det er valgfritt å opprette kunde- og provisjonsgrupper, ettersom beregning av provisjonen også kan gjøres for en individuell kunde og/eller vare. Du kan kjøre denne fremgangsmåten i demonstrasjonsselskapet USMF eller ved hjelp av dine egne data.


## <a name="set-up-commission-groups-and-commission-rates"></a>Definere provisjonsgrupper og provisjonssatser
1. Gå til **Navigasjonsrute > Moduler > Salg og markedsføring > Provisjoner > Kundegrupper for provisjon**.
2. Velg **Ny**.
3. Skriv inn en verdi i feltet **Gruppe**.
4. Skriv inn en verdi i **Navn**-feltet.
5. Velg **Lagre**.
6. Lukk siden.
7. Gå til **Navigasjonsrute > Moduler > Salg og markedsføring > Provisjoner > Varegrupper**.
8. Velg **Ny**.
9. Skriv inn en verdi i feltet **Gruppe**.
10. Skriv inn en verdi i **Navn**-feltet.
11. Velg **Lagre**.
12. Lukk siden.
13. Gå til **Salg og markedsføring > Provisjoner > Salgsgrupper**.
    - En provisjonssalgsgruppe angir de ansatte i selgerroller som er berettiget til å motta en provisjon når en kunde som er knyttet til den relevante salgsgruppen kjøper visse varer.  
    - I USMF-demodatafirmaet er det en salgsgruppe kalt Selgere USA.  
14. Klikk på **Generelt** i **handlingsruten**.
15. Klikk på **Selger**. Selger-siden viser en liste over firmaets selgere som er knyttet til en bestemt provisjonsgruppe. Du kan tilordne flere selgere til samme gruppe og definere deres respektive del av totale provisjonsgebyret som en prosentverdi. Den totale provisjonsandelen for alle ansatte må ikke overskride 100. 
16. Merk den valgte raden i listen.
17. Velg **Rediger**.
18. Sett **Provisjonsandel** til 50.
19. Klikk på **Ny**.
20. Klikk på rullegardinknappen i **Navn**-feltet for å åpne oppslaget.
21. Bruk **hurtigfilteret** for å søke etter poster. Du kan for eksempel filtrere på Navn-feltet med verdien Susan Burk.
22. Klikk på **Velg**.
23. Sett **Provisjonsandel** til 50.
24. Klikk på **Lagre**.
25. Gå til **Salg og markedsføring > Provisjoner > Provisjonsberegning**. Du kan definere provisjonssatsen som ansatt skal motta for en salgstransaksjon når den inneholder forhåndangitt kombinasjon av kunde og produkt, på siden **Provisjonsberegning**. Som en del av provisjonssatsoppsettet, må du angi grunnlaget for provisjonsberegning og om den skal inkludere eller ekskludere rabatter. Du kan også angi en gyldighetsperiode for når provisjonssatsen er aktiv.  
26. Klikk på **Ny**.
27. Velg Gruppe i **Varekode**-feltet.
28. Klikk på rullegardinknappen i **Varerelasjon**-feltet for å åpne oppslaget.
29. Finn og velg gruppen du opprettet tidligere, i listen.
30. Velg Gruppe i **Kundekode**-feltet.
31. Klikk på rullegardinknappen i **Kunderelasjon**-feltet for å åpne oppslaget.
32. Velg gruppen du definerte tidligere, i listen.
33. I **Selgerrelasjon**-feltet klikker du på rullegardinknappen for å åpne oppslaget.
34. Finn og velg ønsket post i listen.
    - Behold alternativet "Før linjerabatt".  
    - Behold alternativet "Omsetning" som grunnlag for beregning av provisjonsverdi.    
35. Angi et tall i feltet Provisjonssats i prosent.
36. Klikk på **Lagre**.

## <a name="setting-up-commission-posting"></a>Definere provisjonspostering
1. Gå til **Navigasjonsrute > Salg og markedsføring > Provisjoner > Provisjonspostering**. Provisjonsgebyrer betales til ansatte, og må derfor defineres til å sikre riktig økonomisk postering til de aktuelle kontoene i **økonomimodulen**. Dette gjøres på siden **Provisjonspostering**. Gå gjennom oppsettet som er tilgjengelig for det gjeldende firmaet. Vanligvis posteres provisjonsbeløpene til en dedikert utgiftskonto og motregnes til en egen konto for leverandører. Hvis du ikke har satt opp regler for provisjonspostering, vil systemet ikke kunne fullføre fakturering av en salgsordre som har kvalifiserte provisjoner.  
2. Lukk siden.

## <a name="assign-a-commission-group-to-a-customer-and-a-product"></a>Tilordne en Provisjonsgruppe til en kunde og et produkt
1. Gå til **Navigasjonsrute > Moduler > Salg og markedsføring > Kunder > Alle kunder**.
2. Finn og velg ønsket post i listen.
3. Klikk på koblingen i den valgte raden i listen.
4. Klikk på **Rediger**.
5. Vis delen **Standarder for salgsordrer**.
6. Klikk på rullegardinknappen i feltet **Provisjonsgruppe** for å åpne oppslaget.
7. Velg gruppen du opprettet tidligere, i listen.
8. Klikk på rullegardinknappen i feltet **Salgsgruppe** for å åpne oppslaget.
9. Finn og velg ønsket post i listen.
10. Klikk på **Lagre**.
11. Gå til **Navigasjonsrute > Moduler > Behandling av produktinformasjon > Produkter > Frigitte produkter**.
12. Bruk **filteret** for å søke etter poster. Du kan for eksempel filtrere på Varenummer-feltet med verdien T0020.
13. Klikk på koblingen i den valgte raden i listen.
14. Klikk på **Rediger**.
15. Vis **Selg**-delen.
16. Klikk på rullegardinknappen i feltet **Provisjonsgruppe** for å åpne oppslaget.
17. Velg provisjonsgruppen du opprettet tidligere, i listen.
18. Velg **Lagre**.

