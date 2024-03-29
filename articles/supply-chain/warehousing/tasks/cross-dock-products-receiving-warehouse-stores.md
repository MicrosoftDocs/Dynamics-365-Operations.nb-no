---
title: Direkteoverføre produkter fra mottakende lager til butikker
description: Denne prosedyren hjelper deg gjennom trinnene med å opprette og behandle en direkteoverføring ved distribusjon av produkter fra mottaksstedet for en bestilling til én eller flere butikker.
author: Mirzaab
ms.date: 02/17/2016
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: RetailBuyersPushPerPackage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6e65535a1879eab229f185e0e97d81a304fd292d
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/29/2021
ms.locfileid: "7572967"
---
# <a name="cross-dock-products-from-receiving-warehouse-to-stores"></a>Direkteoverføre produkter fra mottakende lager til butikker

[!include [banner](../../includes/banner.md)]

Denne prosedyren hjelper deg gjennom trinnene med å opprette og behandle en direkteoverføring ved distribusjon av produkter fra mottaksstedet for en bestilling til én eller flere butikker. Brukeren kan definere flere konfigurasjoner og få systemet til å foreslå hvordan produktene skal distribueres, eller manuelt angi hvor produktene skal distribueres og hvor mye som skal distribueres til hver butikk. Prosedyren inneholder ikke oppsettet av dataene som skal brukes i direkteoverføringen, for eksempel etterfyllingsregler, organisasjonshierarkier og vekt. Prosedyren bruker demonstrasjonsfirmaet USRT.

1. Gå til Alle bestillinger.
2. Velg en bestilling fra listen og klikk koblingen for å åpne den.
3. Klikk på Retail og Commerce i handlingsruten.
4. Klikk på Direkteoverføring.
5. Klikk på Rediger
    * Kategorien kan brukes til å filtrere elementene i Linjer-delen.  
6. Finn og velg ønsket post i listen.
7. Skriv inn en verdi i feltet Direkteoverføringsantall for å angi hvor mye av antallet som kjøpes av det valgte produktet, som skal distribueres.
8. Skriv inn en verdi i feltet Flere direkteoverføringsantall for å angi antallene som skal distribueres av de tilgjengelige produktene som kjøpes.
9. Angi Lokasjonsvekt i feltet Distribusjon.
    * Du kan velge å bruke ulike regler for distribusjon for de andre typene.  
10. Angi eller velg en verdi i feltet Etterfyllingshierarki.
11. Velg Ja i feltet Respekter sortimenter.
12. Klikk på Beregn antall.
13. Klikk på Opprett ordre.
14. Klikk på Ja.
15. Finn og velg et lager som mottok produktene, i listen.
16. Klikk på Ordre for å vise ordrer som ble opprettet for det valgte lageret.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]