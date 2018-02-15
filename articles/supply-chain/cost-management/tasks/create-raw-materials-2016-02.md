--- 
title: "Opprette råvarer (bare februar 2016)"
description: "Denne oppgaven fokuserer på å opprette komponentene i ferdige produkter og halvfabrikata."
author: YuyuScheller
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: 8ed33e2e80915a80eb4c6de014091f1884799098
ms.contentlocale: nb-no
ms.lasthandoff: 01/17/2018

---
# <a name="create-raw-materials-february-2016-only"></a>Opprette råvarer (bare februar 2016)

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne oppgaven fokuserer på å opprette komponentene i ferdige produkter og halvfabrikata. Det er den trede oppgaven i serien stykklisteberegning. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne oppgaven.


## <a name="create-the-first-material"></a>Opprette det første materialet
1. Gå til Behandling av produktinformasjon > Produkter > Frigitte produkter.
2. Klikk Ny.
3. Skriv inn en verdi i feltet Produktnummer.
    * I dette eksemplet angir du ITEM_A.  
4. Angi eller velg en verdi i Varemodellgruppe-feltet.
    * Velg STD. STD står for standardkostnad, og er den mest brukte modellen når du arbeider med kostnadsberegninger.  
5. Angi eller velg en verdi i Varegruppe-feltet.
    * Velg for eksempel Lyd. Dette har ingen innvirkning på kostnadsberegninger.  
6. Angi eller velg en verdi i lagringsdimensjon-feltet.
    * Velg SiteWH. Bare Område og Lager blir brukt for demonstrasjon.  
7. Angi eller velg en verdi i sporingsdimensjon-feltet.
    * Sporingsdimensjoner vil ikke bli brukt i dette eksemplet. Velg Ingen.  
8. Klikk OK.
9. Klikk Administrer lager i handlingsruten.
10. Klikk Standard ordreinnstillinger.
11. Angi eller velg en verdi i feltet Innkjøpssite.
    * Velg Område 1 for dette eksemplet.  
12. Angi eller velg en verdi i feltet Lagersite.
    * Velg Område 1 for dette eksemplet.  
13. Angi eller velg en verdi i feltet Salgssite.
    * Velg Område 1 for dette eksemplet.  
14. Lukk siden.
15. Lukk siden.
16. Klikk koblingen i den valgte raden i listen.
    * Klikk ITEM_A.  
17. Vis delen Styr kostnader.
18. Skriv inn en verdi i Kostgruppe-feltet.
    * I dette eksemplet skriver du inn M2.  
19. Klikk Styr kostnader i handlingsruten.
20. Klikk Varepris.
21. Klikk Ny.
22. Angi eller velg en verdi i Versjon-feltet.
    * I dette eksemplet velger du 10, som er standard etterkalkuleringstype for kostnad.  
23. Angi eller velg en verdi i Område-feltet.
    * Velg Område 1 for dette eksemplet.  
24. Angi et tall i Pris-feltet
    * I dette eksemplet skriver du inn 10.  
25. Klikk Lagre.
26. Klikk Aktiver ventende pris(er).
27. Lukk siden.
28. Lukk siden.

## <a name="create-the-second-material"></a>Opprette det andre materialet
1. Klikk Ny.
2. Skriv inn en verdi i feltet Produktnummer.
    * I dette eksemplet skriver du inn ITEM_B.  
3. Angi eller velg en verdi i Varemodellgruppe-feltet.
    * Velg STD. STD står for standardkostnad, og er den mest brukte modellen når du arbeider med kostnadsberegninger.  
4. Angi eller velg en verdi i Varegruppe-feltet.
    * Velg for eksempel Lyd. Dette har ingen innvirkning på kostnadsberegninger.  
5. Angi eller velg en verdi i lagringsdimensjon-feltet.
    * Velg SiteWH. Bare Område og Lager blir brukt i dette eksemplet.  
6. Angi eller velg en verdi i sporingsdimensjon-feltet.
    * Sporingsdimensjoner vil ikke bli brukt i dette eksemplet. Velg Ingen.  
7. Klikk OK.
8. Klikk Administrer lager i handlingsruten.
9. Klikk Standard ordreinnstillinger.
10. Angi eller velg en verdi i feltet Innkjøpssite.
    * Velg Område 1 for dette eksemplet.  
11. Angi eller velg en verdi i feltet Lagersite.
    * Velg Område 1 for dette eksemplet.  
12. Angi eller velg en verdi i feltet Salgssite.
    * Velg Område 1 for dette eksemplet.  
13. Lukk siden.
14. Lukk siden.
15. Klikk koblingen i den valgte raden i listen.
    * Klikk ITEM_B.  
16. Vis delen Styr kostnader.
17. Skriv inn en verdi i Kostgruppe-feltet.
    * I dette eksemplet skriver du inn M2.  
18. Klikk Styr kostnader i handlingsruten.
19. Klikk Varepris.
20. Klikk Ny.
21. Angi eller velg en verdi i Versjon-feltet.
    * Velg 10 for dette eksemplet. Dette er standard etterkalkuleringstype for kostnad.  
22. Angi eller velg en verdi i Område-feltet.
    * Velg Område 1 for dette eksemplet.  
23. Angi et tall i Pris-feltet
    * For demonstrasjonen skriver du inn 10.  
24. Klikk Lagre.
25. Klikk Aktiver ventende pris(er).
26. Lukk siden.
27. Lukk siden.

## <a name="create-the-third-material"></a>Opprette det tredje materialet
1. Klikk Ny.
2. Skriv inn en verdi i feltet Produktnummer.
    * For demonstrasjonen skriver du inn ITEM_C.  
3. Angi eller velg en verdi i Varemodellgruppe-feltet.
    * Velg STD. STD står for standardkostnad, og er den mest brukte modellen når du arbeider med kostnadsberegninger.  
4. Angi eller velg en verdi i Varegruppe-feltet.
    * Velg for eksempel Lyd. Dette har ingen innvirkning på kostnadsberegninger.  
5. Angi eller velg en verdi i lagringsdimensjon-feltet.
    * Velg SiteWH. Bare Område og Lager blir brukt for demonstrasjon.  
6. Angi eller velg en verdi i sporingsdimensjon-feltet.
    * Sporingsdimensjoner vil ikke bli brukt i dette eksemplet. Velg Ingen.  
7. Klikk OK.
8. Klikk Administrer lager i handlingsruten.
9. Klikk Standard ordreinnstillinger.
10. Angi eller velg en verdi i feltet Innkjøpssite.
    * Velg Område 1 for dette eksemplet.  
11. Angi eller velg en verdi i feltet Lagersite.
    * Velg Område 1 for dette eksemplet.  
12. Angi eller velg en verdi i feltet Salgssite.
    * Velg Område 1 for dette eksemplet.  
13. Lukk siden.
14. Lukk siden.
15. Klikk koblingen i den valgte raden i listen.
    * Klikk ITEM_C.  
16. Vis delen Styr kostnader.
17. Skriv inn en verdi i Kostgruppe-feltet.
    * I dette eksemplet skriver du inn M1.  
18. Klikk Styr kostnader i handlingsruten.
19. Klikk Varepris.
20. Klikk Ny.
21. Angi eller velg en verdi i Versjon-feltet.
    * Velg 10 for dette eksemplet. Dette er standard etterkalkuleringstype for kostnad.  
22. Angi eller velg en verdi i Område-feltet.
    * Velg Område 1 for dette eksemplet.  
23. Angi et tall i Pris-feltet
    * I dette eksemplet skriver du inn 10.  
24. Klikk Lagre.
25. Klikk Aktiver ventende pris(er).
26. Lukk siden.
27. Lukk siden.


