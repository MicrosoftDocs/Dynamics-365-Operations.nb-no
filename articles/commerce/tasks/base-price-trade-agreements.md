---
title: " Basispris og forretningsavtaler"
description: Denne prosedyren hjelper med å opprette kanalspesifikke salgsprisforretningsavtaler.
author: josaw1
manager: AnnBe
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PriceDiscGroup, RetailStoreTable, RetailChannelPriceGroup, EcoResProductDetailsExtended, PriceDiscAdmTable, PriceDiscAdm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 022db9365f25c1d3e387870dd9d173077d864b3d
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141528"
---
# <a name="base-price-and-trade-agreements"></a> Basispris og forretningsavtaler

[!include [banner](../includes/banner.md)]

Denne prosedyren hjelper med å opprette kanalspesifikke salgsprisforretningsavtaler. Denne prosedyren bruker demonstrasjonsdatafirmaet USRT.

1. I **navigasjonsruten** går du til **Moduler > Retail og Commerce > Prissetting og rabattstyring > Prisgrupper > Alle prisgrupper**. Prisgrupper er måten forretningsavtaler tilordnes til bestemte kanaler på. Kanalspesifikke priser blir mulig ved å bruke prisgrupper for å tilordne forretningsavtaler til en kanal.  
2. Klikk på **Ny**.
3. Skriv inn en verdi i feltet **Prisgrupper**.
4. Skriv inn en verdi i **Navn**-feltet.
5. Klikk **Lagre**.
6. Lukk siden.
7. I **navigasjonsruten** går du til **Moduler > Retail og Commerce > Kanaler > Butikker > Alle butikker**.
8. Velg New York i listen.
9. Klikk **Butikk** i handlingsruten.
10. Klikk **Prisgrupper**.
11. Klikk på **Ny**.
12. Klikk rullegardinknappen i **Prisgrupper**-feltet for å åpne oppslaget.
13. Finn og velg ønsket post i listen.
14. Klikk **Lagre**.
15. Lukk siden.
16. Lukk siden.
17. I **navigasjonsruten** går du til **Moduler > Retail og Commerce > Produkter og kategorier > Frigitte produkter etter kategori**.
18. Klikk koblingen i den valgte raden i listen.
19. Klikk **Rediger**.
20. Utvid **Selg**-hurtigfanen.
21. Angi et tall i **Pris**-feltet Denne prisen brukes hvis det ikke blir funnet en gjeldende forretningsavtale.  
22. Klikk **Lagre**.
23. I **Handlingsrute** klikker du på **Selg**.
24. Klikk **Opprett forretningsavtaler**.
25. Klikk på **Ny**.
26. Klikk på rullegardinknappen i **Navn**-feltet for å åpne oppslaget.
27. Velg **Commerce** i listen. I demonstrasjonsdataene har journalnavnet **Commerce** standardrelasjonen **Pris (salg)**. Det betyr at alle nye linjer som opprettes, bruker salgsprisforretningsavtaler som standard.  
28. Klikk på **Linjer** i **handlingsruten**.
29. Velg Gruppe i **Kontokode**-feltet.
30. Klikk på rullegardinknappen i **Kontovalg**-feltet for å åpne oppslaget.
31. Finn og velg ønsket post i listen. Dette fullfører koblingen fra kanal til prisgruppe til forretningsavtale.  
32. Skriv inn en verdi i **Varerelasjon**-feltet.
33. Angi en verdi i feltet **Beløp i valuta**.
34. Merk av eller fjern merket for **Søk etter neste** i hurtigfanen **Detaljer**. Når **Søk etter neste** settes til Ja, fortsetter prissettingsmotoren å søke etter gjeldende forretningsavtaler med en lavere salgspris. Når **Søk etter neste** settes til Nei, slutter motoren å søke og bruker forretningsavtalen.  
35. Klikk **Poster**.
36. Klikk **OK**.
37. Lukk siden.
38. Klikk Selg i **handlingsruten.**
39. Klikk **Salgspris**.

