---
title: Definere ny tildeling av vare for plukking med mangler
description: Denne fremgangsmåten viser hvordan du kan la lagerarbeidere raskt finne alternative lokasjoner hvis ikke det er nok lager på lokasjonen de er sendt til.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkException, WHSWorker
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: eae86b307ac8d8539c3897293c2fc21ea57d2d60
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148245"
---
# <a name="set-up-short-picking-item-reallocation"></a>Definere ny tildeling av vare for plukking med mangler

[!include [banner](../../includes/banner.md)]

Denne fremgangsmåten viser hvordan du kan la lagerarbeidere raskt finne alternative lokasjoner hvis ikke det er nok lager på lokasjonen de er sendt til. Det er mulig å bruke en automatisk prosess for ny tildeling, som bruker lokasjonsdirektiver til å hente varene hvis de er tilgjengelige på en annen lokasjon. Når manuell ny tildeling brukes, vises også en liste over lokasjoner med det tilgjengelige antallet på den mobile enheten, noe som gjør at lagerarbeideren kan velge hvilken lokasjon som skal brukes for beholdningen. Du kan bruke prosedyren i demonstrasjonsdataselskapet USMF. Denne fremgangsmåten gjelder for en funksjon som ble lagt til i Dynamics 365 for Operations versjon 1611.


## <a name="set-up-work-exceptions"></a>Konfigurer arbeidsunntak
1. I **navigasjonsruten** går du til **Lagerstyring > Oppsett > Arbeid > Arbeidsunntak**.
2. Klikk på **Ny**. Det er mulig å definere flere arbeidsunntak med ulike varetildelingspolicyer, slik at lagermedarbeideren kan velge én basert på behovene i forsendelsen de behandler.  
3. Skriv inn en verdi i feltet **Kode for arbeidsunntak**. Gi arbeidsunntaket en tittel for å angi hva den skal brukes til. Eksempel: Plukking med mangler manuelt.  
4. Skriv inn en verdi i **Beskrivelse**-feltet.
5. Velg Plukk med mangler i **Unntakstype**-feltet.
6. Merk av for **Juster beholdning**. Dette alternativet betyr at lageret blir automatisk justert til 0 på lokasjonen med mangler.  
7. Angi eller velg en verdi i feltet **Standard justeringstypekode**. I USMF kan du for eksempel velge Remove Res Adj Out.  
8. Velg Manuell i feltet **Ny fordeling av vare**. Hvis du velger Manuell, eller Automatisk og Manuell, må lagermedarbeideren aktiveres for å bruke manuell ny tildeling.  

## <a name="set-up-a-worker-to-use-manual-item-reallocation"></a>Konfigurere en arbeider til å bruke manuell ny tildeling av vare
1. Lukk siden.
2. I **navigasjonsruten** går du til **Lagerstyring > Oppsett > Arbeider**.
3. Klikk **Rediger**.
4. Velg arbeider 24 i listen.
5. Utvid **Arbeid**-hurtigfanen.
6. Velg Ja i feltet **Tillat manuell ny tildeling av vare**.

