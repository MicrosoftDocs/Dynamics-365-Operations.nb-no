--- 
title: Definere ny tildeling av vare for plukking med mangler
description: "Denne fremgangsmåten viser hvordan du kan la lagerarbeidere raskt finne alternative lokasjoner hvis ikke det er nok lager på lokasjonen de er sendt til."
author: YuyuScheller
manager: AnnBe
ms.date: 10/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: b67965b6c8641b5d91ab3c5b0a7a7fd28a07cba6
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-short-picking-item-reallocation"></a>Definere ny tildeling av vare for plukking med mangler

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåten viser hvordan du kan la lagerarbeidere raskt finne alternative lokasjoner hvis ikke det er nok lager på lokasjonen de er sendt til. Det er mulig å bruke en automatisk prosess for ny tildeling, som bruker lokasjonsdirektiver til å hente varene hvis de er tilgjengelige på en annen lokasjon. Når manuell ny tildeling brukes, vises også en liste over lokasjoner med det tilgjengelige antallet på den mobile enheten, noe som gjør at lagerarbeideren kan velge hvilken lokasjon som skal brukes for beholdningen. Du kan bruke prosedyren i demonstrasjonsdataselskapet USMF. Denne fremgangsmåten gjelder for en funksjon som ble lagt til i Dynamics 365 for Operations, versjon 1611.


## <a name="set-up-work-exceptions"></a>Konfigurer arbeidsunntak
1. Gå til Lagerstyring > Oppsett > Arbeid > Arbeidsunntak.
2. Klikk Ny.
    * Det er mulig å definere flere arbeidsunntak med ulike varetildelingspolicyer, slik at lagermedarbeideren kan velge én basert på behovene i forsendelsen de behandler.  
3. Skriv inn en verdi i feltet Kode for arbeidsunntak.
    * Gi arbeidsunntaket en tittel for å angi hva den skal brukes til. Eksempel: Plukking med mangler manuelt.  
4. Skriv inn en verdi i feltet Beskrivelse.
5. Velg Plukk med mangler i Unntakstype-feltet.
6. Merk av for Juster beholdning.
    * Dette alternativet betyr at lageret blir automatisk justert til 0 på lokasjonen med mangler.  
7. Angi eller velg en verdi i feltet Standard justeringstypekode.
    * I USMF kan du for eksempel velge Remove Res Adj Out.  
8. Velg Manuell i feltet Ny fordeling av vare.
    * Hvis du velger Manuell, eller Automatisk og Manuell, må lagermedarbeideren aktiveres for å bruke manuell ny tildeling.  

## <a name="set-up-a-worker-to-use-manual-item-reallocation"></a>Konfigurere en arbeider til å bruke manuell ny tildeling av vare
1. Lukk siden.
2. Gå til Lagerstyring > Oppsett > Arbeider.
3. Klikk Rediger.
4. Velg arbeider 24 i listen.
5. Utvid seksjonen Arbeid.
6. Velg Ja i feltet Tillat manuell ny tildeling av vare.


