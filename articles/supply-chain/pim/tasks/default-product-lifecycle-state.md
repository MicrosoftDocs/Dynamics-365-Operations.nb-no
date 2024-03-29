---
title: Opprette en standard livssyklustilstand for produkt
description: Denne fremgangsmåten beskriver hvordan du oppretter en standard produktlivssyklustilstand samt hvordan du knytter standardtilstanden til frigitte produkter.
author: t-benebo
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a628ed2b609f48c22076f409889c212e4d9463ac
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/29/2021
ms.locfileid: "7578206"
---
# <a name="create-a-default-product-lifecycle-state"></a>Opprette en standard livssyklustilstand for produkt

[!include [banner](../../includes/banner.md)]

Denne fremgangsmåten beskriver hvordan du oppretter en standard produktlivssyklustilstand samt hvordan du knytter standardtilstanden til frigitte produkter.


## <a name="create-a-default-lifecycle-state"></a>Opprette en standard livssyklustilstand
1. Gå til Behandling av produktinformasjon > Oppsett > Livssyklustilstand for produkt.
2. Klikk på Ny.
3. Skriv inn en verdi i feltet Tilstand.
4. Velg Ja i Standard når frigitt til juridisk enhet-feltet.
5. Skriv inn en verdi i feltet Beskrivelse.
6. Velg Nei i Er aktiv for planlegging-feltet.

> [!NOTE]
> Hvis et nytt frigitt produkt ikke skal inkluderes i Hovedplanlegging, velger du Nei. Hvis det skal være med i Hovedplanlegging, lar du kontrollen ha standardverdien Ja.  

## <a name="create-a-new-released-product"></a>Opprette et nytt frigitt produkt
1. Lukk siden.
2. Gå til Behandling av produktinformasjon > Produkter > Frigitte produkter.
3. Klikk på Ny.
4. Skriv inn en verdi i feltet Produktnummer.
5. Skriv inn en verdi i feltet Produktnavn.
6. Skriv inn en verdi i Søkenavn-feltet.
7. Angi eller velg en verdi i Varemodellgruppe-feltet.
8. Angi eller velg en verdi i Varegruppe-feltet.
9. Angi eller velg en verdi i lagringsdimensjon-feltet.
10. Angi eller velg en verdi i sporingsdimensjon-feltet.
11. Klikk på OK.

> [!NOTE]
> Standard produktlivssyklustilstand er en global definisjon.  

## <a name="change-the-product-to-an-active-state"></a>Endre produktet til en aktiv tilstand
1. Angi eller velg en verdi i feltet Livssyklustilstand for produkt.

> [!NOTE]
> Anta at du har definert en aktiv tilstand og at du nå kan velge den aktive tilstanden slik at produktet kan brukes i Hovedplanlegging og stykklistenivåberegningen. Åpenbart så gir dette bare mening hvis alle produktdetaljene som kreves for konsekvent planlegging, er angitt.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]