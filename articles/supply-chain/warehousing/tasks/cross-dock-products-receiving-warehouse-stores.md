--- 
title: "Direkteoverføre produkter fra mottakende lager til butikker"
description: "Denne prosedyren hjelper deg gjennom trinnene med å opprette og behandle en direkteoverføring ved distribusjon av produkter fra mottaksstedet for en bestilling til én eller flere butikker."
author: BibiSp
manager: AnnBe
ms.date: 02/17/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: daa42bb83d6b988e8fd18db6ad8386c67fd3e6e5
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="cross-dock-products-from-receiving-warehouse-to-stores"></a>Direkteoverføre produkter fra mottakende lager til butikker

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne prosedyren hjelper deg gjennom trinnene med å opprette og behandle en direkteoverføring ved distribusjon av produkter fra mottaksstedet for en bestilling til én eller flere butikker. Brukeren kan definere flere konfigurasjoner og få systemet til å foreslå hvordan produktene skal distribueres, eller manuelt angi hvor produktene skal distribueres og hvor mye som skal distribueres til hver butikk. Prosedyren inneholder ikke oppsettet av dataene som skal brukes i direkteoverføringen, for eksempel etterfyllingsregler, organisasjonshierarkier og vekt. Prosedyren bruker demonstrasjonsfirmaet USRT.

1. Gå til Alle bestillinger.
2. Velg en bestilling fra listen og klikk koblingen for å åpne den.
3. Klikk Detaljhandel i handlingsruten.
4. Klikk Direkteoverføring.
5. Klikk Rediger.
    * Kategorien kan brukes til å filtrere elementene i Linjer-delen.  
6. Finn og velg ønsket post i listen.
7. Skriv inn en verdi i feltet Direkteoverføringsantall for å angi hvor mye av antallet som kjøpes av det valgte produktet, som skal distribueres.
8. Skriv inn en verdi i feltet Flere direkteoverføringsantall for å angi antallene som skal distribueres av de tilgjengelige produktene som kjøpes.
9. Angi Lokasjonsvekt i feltet Distribusjon.
    * Du kan velge å bruke ulike regler for distribusjon for de andre typene.  
10. Angi eller velg en verdi i feltet Etterfyllingshierarki.
11. Velg Ja i feltet Respekter sortimenter.
12. Klikk Beregn antall.
13. Klikk Opprett ordre.
14. Klikk Ja.
15. Finn og velg et lager som mottok produktene, i listen.
16. Klikk Ordre for å vise ordrer som ble opprettet for det valgte lageret.


