--- 
title: Definere en arbeidsmal for bestillinger
description: "Denne prosedyren fokuserer på oppsettet for enkel arbeidsmal for som skal brukes når du plasserer mottatte varer."
author: BibiSp
manager: AnnBe
ms.date: 11/14/2016
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
ms.openlocfilehash: fbbe019bdca2d5182466a20370418a14032fe63d
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-a-work-template-for-purchase-orders"></a>Definere en arbeidsmal for bestillinger

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Denne prosedyren fokuserer på oppsettet for enkel arbeidsmal for som skal brukes når du plasserer mottatte varer. Arbeidsmaler bestemmer settet med instruksjoner som presenteres for lagermedarbeideren på en mobil enhet når de flytter varer fra mottaksområdet. Du kan bruke denne fremgangsmåten med data som er nevnt i demonstrasjonsdataselskapet USMF. Før du starter denne veiledningen kan du opprette en arbeidspulje-ID. I dette eksemplet brukes en arbeidpulje-ID kalt Innkommende. Denne fremgangsmåten er ment for lagersjef.

1. Gå til Lagerstyring > Oppsett > Arbeid > Arbeidsmaler.
2. Velg Bestillinger i feltet Arbeidsordretype.

## <a name="create-a-work-template-header"></a>Opprette et arbeidsmalhode
1. Klikk Ny.
2. Angi et nummer i Sekvensnummer-feltet.
    * Dette er sekvensen der arbeidsmalene blir evaluert. Du kan endre rekkefølgen om nødvendig.  
3. Angi en verdi i feltet Arbeidsmal.
    * Dette er den unike identifikatoren for denne malen.  
4. Skriv inn en verdi i feltet Beskrivelse av arbeidsmal.
    * Alternativet gyldig kontrolleres ikke før du har fullført all informasjonen som kreves av malen og deretter har klikket Lagre.  
    * En arbeidsordre av typen Bestilling kan ikke kan behandles automatisk, så la alternativet Behandle automatisk være satt til Nei.  
5. Skriv inn en verdi i feltet ID for arbeidsutvalg.
    * Arbeidspulje-ID-er gir deg muligheten til å organisere arbeidet i grupper. Verdien du angir her, blir standardverdien for arbeid som opprettes med denne malen.  
6. I Arbeidsprioritet-feltet angir du '1'.
    * Dette indikerer viktigheten av arbeidet, og verdien du angir her, blir standard for alt arbeid som er opprettet ved hjelp av denne malen.  
7. Klikk Lagre.
    * Du må lagre arbeidsmalhodet før knappen Rediger spørring blir tilgjengelig.  

## <a name="set-up-the-query-for-the-work-template"></a>Konfigurere spørringen for arbeidsmalen
1. Klikk Rediger spørring.
    * Vi vil angi en begrensning slik at malen bare kan brukes i et bestemt lager.  
2. Klikk Legg til.
3. Merk den valgte raden i listen.
4. Skriv lager i Felt-feltet.
5. Skriv inn en verdi i Kriterier-feltet.
6. Klikk OK.
7. Klikk Ja.

## <a name="set-work-template-details"></a>Angi arbeidsmaldetaljer
1. Klikk Ny.
2. Velg Plukk i Arbeidstype-feltet.
3. Skriv inn innkjøp i feltet Arbeidsklasse-ID.
    * Arbeidsklassen som du angir her, blir standard på alle arbeidslinjer av typen Plukk som opprettes ved hjelp av denne malen. Arbeidsklassen kan ikke overskrives fra arbeidsordrelinjene. Arbeidsklasser brukes til å styre og/eller begrense typen arbeidsordrelinjer som en lagermedarbeider kan behandle på en mobilenhet.  
4. Klikk Ny.
5. Velg Plasser i Arbeidstype-feltet.
6. Skriv inn en verdi i feltet Arbeidsklasse-ID.
    * Instruksjoner for plukking og plassering er et sett. Hvert plukk/plasser-sett må ha samme arbeidsklasse. Bruk samme arbeidsklasse som du har angitt for plukkinstruksjonen.  
7. Klikk Lagre.
    * Legg merke til at det nå merket av for Gyldig.  


