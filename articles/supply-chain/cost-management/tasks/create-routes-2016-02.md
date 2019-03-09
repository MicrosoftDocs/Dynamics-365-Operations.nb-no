---
title: Opprette ruter (bare februar 2016)
description: Denne oppgaven fokuserer på å opprette produksjonsruter for et ferdig produkt og et halvfabrikata.
author: ShylaThompson
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 63ad2cc0c41a5931750dffbfc64bc7ce965a1da4
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "316470"
---
# <a name="create-routes-february-2016-only"></a>Opprette ruter (bare februar 2016)

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne oppgaven fokuserer på å opprette produksjonsruter for et ferdig produkt og et halvfabrikata. Det er den femte oppgaven i serien stykklisteberegning. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne oppgaven.


## <a name="create-a-route-for-a-semi-finished-product"></a>Opprette en rute for et halvfabrikata
1. Gå til Behandling av produktinformasjon > Produkter > Frigitte produkter.
2. Klikk koblingen i den valgte raden i listen.
    * Velg varenummeret BOM_2.  
3. Klikk Utvikling i handlingsruten.
4. Klikk Rute.
5. Klikk Ny.
6. Klikk Rute og ruteversjon.
7. Skriv inn en verdi i feltet Beskrivelse.
    * I dette eksemplet skriver du inn ROUTE_2.  
8. Angi eller velg en verdi i Område-feltet.
    * I dette eksemplet angir eller velger du Område 1.  
9. Klikk OK.
10. Klikk Ny.
11. Angi eller velg en verdi i feltet Operasjon.
    * I dette eksemplet velger du Samling.  
12. Angi et tall i feltet Kjøretid.
    * Skriv for eksempel 1. Operasjonstid inngår ofte i prisen som er beregnet for en vare.  
13. Angi eller velg en verdi i Rutegruppe-feltet.
    * Velg Std. for dette eksemplet.  
14. Klikk kategorien Oppsett.
15. Angi eller velg en verdi i Oppsettkategori-feltet.
    * I dette eksemplet velger du Samling.  
16. Klikk kategorien Tider.
17. Angi et tall i feltet Oppstillingstid.
    * I dette eksemplet skriver du inn 1. Oppstillingstider inngår ofte i prisen som er beregnet for en vare.  
18. Klikk Ruteversjon i handlingsruten.
19. Klikk Godkjenn.
20. Velg Ja under Vil du også godkjenne ruten? .
21. Klikk OK.
22. Klikk Ruteversjon i handlingsruten.
23. Klikk Aktiver.
24. Lukk siden.
25. Lukk siden.

## <a name="create-a-route-for-a-finished-product"></a>Opprette en rute for et ferdig produkt
1. Klikk koblingen i den valgte raden i listen.
    * Velg varenummeret BOM_1.  
2. Klikk Utvikling i handlingsruten.
3. Klikk Rute.
4. Klikk Ny.
5. Klikk Rute og ruteversjon.
6. Skriv inn en verdi i feltet Beskrivelse.
    * I dette eksemplet skriver du inn ROUTE_1.  
7. Angi eller velg en verdi i Område-feltet.
    * I dette eksemplet angir eller velger du Område 1.  
8. Klikk OK.
9. Klikk Ny.
10. Angi eller velg en verdi i feltet Operasjon.
    * I dette eksemplet velger du Emballasje.  
11. Angi et tall i feltet Kjøretid.
    * I dette eksemplet skriver du inn 1.  
12. Angi eller velg en verdi i Rutegruppe-feltet.
    * Velg Std. for dette eksemplet.  
13. Klikk kategorien Oppsett.
14. Angi eller velg en verdi i Oppsettkategori-feltet.
    * I dette eksemplet velger du Emballasje.  
15. Klikk kategorien Tider.
16. Angi et tall i feltet Oppstillingstid.
    * I dette eksemplet skriver du inn 1.  
17. Klikk Ruteversjon i handlingsruten.
18. Klikk Godkjenn.
19. Klikk OK.
20. Klikk Ruteversjon i handlingsruten.
21. Klikk Aktiver.
22. Lukk siden.
23. Lukk siden.

## <a name="enable-automatic-consumption-of-setup-time"></a>Aktiver automatisk forbruk av oppstillingstid
1. Gå til Produksjonskontroll > Oppsett > Ruter > Rutegrupper.
2. Finn og velg ønsket post i listen.
    * Velg Std i listen.  
3. Klikk Rediger.
4. Velg Ja i feltet Oppstillingstid.
    * Oppstillingstider inngår ofte i prisen som er beregnet for en vare.  
5. Klikk Lagre.
6. Lukk siden.

