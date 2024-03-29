---
title: Fullføre grunnleggende oppsett av en frigitt produktstandard
description: Denne artikkelen viser hvordan du fullfører minimumsoppsettet som kreves før produktstandarden kan brukes i stykklisteversjoner.
author: t-benebo
ms.date: 07/08/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, InventTableInventoryDimensionGroups, InventItemOrderSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a403600bfdc257587441b5b5a907981d5eebaf58
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8844886"
---
# <a name="complete-basic-setup-of-a-released-product-master"></a>Fullføre grunnleggende oppsett av en frigitt produktstandard

[!include [banner](../../includes/banner.md)]

Denne artikkelen viser hvordan du fullfører minimumsoppsettet som kreves før produktstandarden kan brukes i stykklisteversjoner.

Dette er den tredje fremgangsmåten av åtte som forklarer hvordan du bygger kombinasjoner for dimensjonsbasert konfigurasjon. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.

1. Gå til **Navigasjonsrute > Moduler > Behandling av produktinformasjon > Produkter > Frigitte produkter**.
2. Finn og velg ønsket post i listen. Velg produktstandarden du har frigitt i den andre prosedyren. Denne produktstandarden opprettes ved hjelp av dimensjonsbasert konfigurasjon-teknologi.  
3. Klikk på **Produkt** i handlingsruten.
4. Velg **Dimensjonsgrupper** for å åpne nedtrekksdialogen.
5. Klikk på rullegardinknappen i **Lagringsdimensjonsgruppe**-feltet for å åpne oppslaget.
6. Finn og velg ønsket post i listen. Lagringsdimensjonsgruppen bestemmer hvilke lagerdimensjoner som skal brukes for produkttransaksjonen. Velg **Område** for denne prosedyren.  
7. Klikk på rullegardinknappen i **Sporingsdimensjonsgruppe**-feltet for å åpne oppslaget.
8. Finn og velg ønsket post i listen. Sporingsdimensjonsgruppen bestemmer hvilke sporingsdimensjoner som skal brukes for produkttransaksjonen. Velg **Ingen** for denne prosedyren.  
9. Klikk på **OK**.
10. Klikk på **Rediger**.
11. Klikk på rullegardinknappen i feltet **Varemodellgruppe** for å åpne oppslaget.
12. Finn og velg ønsket post i listen. Varemodellgrupper inneholder innstillinger som bestemmer hvordan varer styres og behandles ved varemottak og vareavganger. De bestemmer også hvordan vareforbruk beregnes. Velg **FIFO** for denne prosedyren.  
13. Vis delen **Styr kostnader**.
14. Klikk på rullegardinknappen i feltet **Varegruppe** for å åpne oppslaget.
15. Finn og velg ønsket post i listen. Varegrupper brukes til å styre lager ved å dele inn lagervarer i grupper. Velg **CarAudio** for denne prosedyren.  
16. Velg **Plan** i handlingsruten.
17. Velg **Standard ordreinnstillinger**.
18. Velg et alternativ i feltet **Standard ordretype**. Velg **Produksjon** for å angi at standardforsyningsalternativet for denne produktstandarden skal produsere den.  
19. Velg **Lagre**.
20. Lukk siden.
21. Lukk skjemaet **Detaljer om frigitt produkt**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]