---
title: Definere ny tildeling av vare for plukking med mangler
description: Dette emnet viser hvordan du kan la lagerarbeidere raskt finne alternative lokasjoner hvis ikke det er nok lager på lokasjonen de er sendt til.
author: ShylaThompson
manager: tfehr
ms.date: 06/29/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkException, WHSWorker, WHSLocationWithWorkException
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4e8f5c23f82e96145f411ec993f766a90137b5b8
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4434763"
---
# <a name="set-up-short-picking-item-reallocation"></a>Definere ny tildeling av vare for plukking med mangler

[!include [banner](../../includes/banner.md)]

Denne fremgangsmåten viser hvordan du kan la lagerarbeidere raskt finne alternative lokasjoner hvis ikke det er nok lager på lokasjonen de er sendt til. 

Den nye tildelingsprosessen styres av et **arbeidsunntak** og brukes av **lagermedarbeideren.**

Det er mulig å bruke automatisk, manuell eller begge prosessene for ny tildeling:

- Automatisk ny tildeling – lokasjonsdirektiver brukes til å fastslå om varene er tilgjengelige på en annen lokasjon. Hvis det er mulig, oppdateres arbeidet og lagerbrukeren blir dirigert til den alternative lokasjonen.
- Manuell ny tildeling – gjør at lagerbrukeren kan velge blant én eller flere lokasjoner med ikke-reservert antall varer. 
- Automatisk og manuell – hvis systemet ikke klarer å utføre automatisk ny tildeling, og lokasjoner er tilgjengelige med ikke-reservert antall, blir brukeren bedt om å velge en lokasjon.

## <a name="set-up-work-exceptions"></a>Konfigurer arbeidsunntak
Det er mulig å definere flere arbeidsunntak med ulike varetildelingspolicyer, slik at lagermedarbeideren kan velge én basert på behovene i forsendelsen de behandler.

Demonstrasjonsdatafirmaet USMF ble brukt til å opprette denne fremgangsmåten.

1. I **navigasjonsruten** går du til **Lagerstyring > Oppsett > Arbeid > Arbeidsunntak**.
2. Klikk på **Ny** 
3. Skriv inn en verdi i feltet **Kode for arbeidsunntak**. Dette er tittelen på dette unntaket. Eksempel: Plukking med mangler manuelt.
4. Skriv inn en verdi i **Beskrivelse**-feltet. Dette vil være en kort beskrivelse av bruken av dette unntaket. For eksempel Plukk med mangler – vare ikke tilgjengelig.
5. Velg **Plukk med mangler** i **Unntakstype**-feltet.
6. Merk av for **Juster beholdning**. Hvis valg betyr det at lageret blir automatisk justert til 0 på lokasjonen med mangler.
7. Angi eller velg en verdi i feltet **Standard justeringstypekode**. I USMF kan du for eksempel velge **Remove Res Adj Out**. Hver justeringstypekode inneholder fire karakteristikker: navn, beskrivelse, navn på lagerjournal og **Fjern reservasjoner**. Hvis **Fjern reservasjoner** er aktivert, vil reservasjonene for ordrelinjen med plukk med mangler.  
8. I **Ny tildeling av vare**-feltet velger du en verdi, som Manuell. Hvis du velger Manuell, eller Automatisk og Manuell, må lagermedarbeideren aktiveres for å bruke manuell ny tildeling.

## <a name="set-up-a-worker-to-use-manual-item-reallocation"></a>Konfigurere en arbeider til å bruke manuell ny tildeling av vare

Demonstrasjonsdatafirmaet USMF ble brukt til å opprette denne fremgangsmåten.

1. Lukk siden.
2. I **navigasjonsruten** går du til **Lagerstyring > Oppsett > Arbeider**.
3. Klikk **Rediger**.
4. Velg arbeider i listen. For eksempel Julia Funderburk.
5. Utvid **Brukere**-hurtigfanen.
6. Velg en **bruker-ID** i listen. For eksempel 24.
7. Utvid **Arbeid**-hurtigfanen.
8. Velg **Ja** i feltet **Tillat manuell ny tildeling av vare**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]