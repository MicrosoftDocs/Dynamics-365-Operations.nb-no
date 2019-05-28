---
title: Fullføre grunnleggende oppsett av en frigitt produktstandard
description: Denne fremgangsmåten viser hvordan du fullfører minimumsoppsett som kreves før produktstandarden kan brukes i stykklisteversjoner.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, InventTableInventoryDimensionGroups, InventItemOrderSetup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0d3a91977c38c0ce0f9fe114bec943c7cb32a5d4
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1568780"
---
# <a name="complete-basic-setup-of-a-released-product-master"></a>Fullføre grunnleggende oppsett av en frigitt produktstandard

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåten viser hvordan du fullfører minimumsoppsett som kreves før produktstandarden kan brukes i stykklisteversjoner.

Dette er den tredje fremgangsmåten av åtte som forklarer hvordan du bygger kombinasjoner for dimensjonsbasert konfigurasjon. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.

1. Gå til Behandling av produktinformasjon > Produkter > Frigitte produkter.
2. Finn og velg ønsket post i listen.
    * Velg produktstandarden du har frigitt i den andre prosedyren. Denne produktstandarden opprettes ved hjelp av dimensjonsbasert konfigurasjon-teknologi.  
3. Klikk Produkt i handlingsruten.
4. Klikk Dimensjonsgrupper for å åpne nedtrekksdialogen.
5. Klikk rullegardinknappen i Lagringsdimensjonsgruppe-feltet for å åpne oppslaget.
6. Finn og velg ønsket post i listen.
    * Lagringsdimensjonsgruppen bestemmer hvilke lagerdimensjoner som skal brukes for produkttransaksjonen. Velg Område for denne prosedyren.  
7. Klikk koblingen i den valgte raden i listen.
8. Klikk rullegardinknappen i Sporingsdimensjonsgruppe-feltet for å åpne oppslaget.
9. Finn og velg ønsket post i listen.
    * Sporingsdimensjonsgruppen bestemmer hvilke sporingsdimensjoner som skal brukes for produkttransaksjonen. Velg Ingen for denne prosedyren.  
10. Klikk koblingen i den valgte raden i listen.
11. Klikk OK.
12. Klikk koblingen i den valgte raden i listen.
13. Klikk Rediger.
    * Åpne skjemaet Detaljer om frigitt produkt for å fortsette oppgaven for oppsettet.  
14. Klikk rullegardinknappen i feltet Varemodellgruppe for å åpne oppslaget.
15. Finn og velg ønsket post i listen.
    * Varemodellgrupper inneholder innstillinger som bestemmer hvordan varer styres og behandles ved varemottak og vareavganger. De bestemmer også hvordan vareforbruk beregnes. Velg FIFO for denne prosedyren.  
16. Klikk koblingen i den valgte raden i listen.
17. Vis eller skjul delen Styr kostnader.
18. Klikk rullegardinknappen i feltet Varegruppe for å åpne oppslaget.
19. Finn og velg ønsket post i listen.
    * Varegrupper brukes til å styre lager ved å dele inn lagervarer i grupper. Velg CarAudio for denne prosedyren.  
20. Klikk koblingen i den valgte raden i listen.
21. Klikk Plan i handlingsruten.
22. Klikk Standard ordreinnstillinger.
23. Velg et alternativ i feltet Standard ordretype.
    * Velg Produksjon for å angi at standardforsyningsalternativet for denne produktstandarden skal produsere den.  
24. Lukk siden.
25. Lukk skjemaet Detaljer om frigitt produkt.

