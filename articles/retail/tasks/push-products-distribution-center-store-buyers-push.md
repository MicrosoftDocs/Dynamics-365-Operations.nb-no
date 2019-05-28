---
title: " Overføre produkter fra distribusjonssenter til butikk ved hjelp av sentralt innkjøp"
description: Denne prosedyren hjelper deg gjennom trinnene med å opprette og behandle et sentralt innkjøp ved distribusjon av produkter fra en lokasjon til én eller flere butikker.
author: rubencdelgado
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailBuyersPush, InventLocationIdLookup, InventItemIdLookupSimple, RetailReplenishmentTreeLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 20c2734a8339279e3f13ca9f0a0d5398c87f846f
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1550145"
---
# <a name="push-products-from-distribution-center-to-store-using-buyers-push"></a> Overføre produkter fra distribusjonssenter til butikk ved hjelp av sentralt innkjøp

[!include[task guide banner](../includes/task-guide-banner.md)]

Denne prosedyren hjelper deg gjennom trinnene med å opprette og behandle et sentralt innkjøp ved distribusjon av produkter fra en lokasjon til én eller flere butikker. Brukeren kan definere flere konfigurasjoner og få systemet til å foreslå hvordan produktene skal distribueres, eller manuelt angi hvor produktene skal distribueres og hvor mye som skal distribueres til hver butikk. Denne prosedyren inneholder ikke oppsettet av dataene som skal brukes i det sentrale innkjøpet, for eksempel etterfyllingsregler, organisasjonshierarkier og vekt. Denne prosedyren bruker demonstrasjonsfirmaet USRT.

1. Gå til Kjøp etter ordre.
2. Klikk Ny.
3. Skriv inn en verdi i feltet Beskrivelse.
4. Angi eller velg en verdi i Område-feltet.
5. I Lager-feltet angir eller velger du et lager som har produkter med lagerbeholdningsantall.
6. Klikk Legg til.
7. Merk den valgte raden i listen.
8. Angi eller velg et produkt i Varenummer-feltet.
9. Klikk Legg til.
10. Merk den valgte raden i listen.
11. Angi eller velg et variantprodukt i Varenummer-feltet.
    * Når du angir et variantprodukt, opprettes linjer for hver variant.  
12. Merk en rad i listen.
13. I feltet Antall overførte skriver du inn hvor mye av det valgte produktet du vil distribuere.
14. I feltet Tilleggsantall som skal overføres angir du hvor mange produkter som har tilgjengelig antall for distribusjon.
15. Angi Lokasjonsvekt i feltet Distribusjon.
    * Du kan velge å bruke andre regler for distribusjon for de andre typene.  
16. Angi eller velg en verdi i feltet Etterfyllingshierarki.
17. Velg Ja i feltet Respekter sortimenter.
18. Klikk Beregn antall og se gjennom antallene som legges til i radene, i Lager-delen.
19. Klikk Opprett ordre.
20. Klikk Ja.

