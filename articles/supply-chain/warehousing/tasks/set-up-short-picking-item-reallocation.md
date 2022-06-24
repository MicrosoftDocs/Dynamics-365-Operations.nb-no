---
title: Definere ny tildeling av vare for plukking med mangler
description: Denne artikkelen viser hvordan du kan la lagerarbeidere raskt finne alternative lokasjoner hvis ikke det er nok lager på lokasjonen de er sendt til.
author: Mirzaab
ms.date: 06/29/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWorkException, WHSWorker, WHSLocationWithWorkException
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a4e6d7f9b09434346cb0f3670d10437ef8197822
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8875021"
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
3. Klikk på **Rediger**.
4. Velg arbeider i listen. For eksempel Julia Funderburk.
5. Utvid **Brukere**-hurtigfanen.
6. Velg en **bruker-ID** i listen. For eksempel 24.
7. Utvid **Arbeid**-hurtigfanen.
8. Velg **Ja** i feltet **Tillat manuell ny tildeling av vare**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]