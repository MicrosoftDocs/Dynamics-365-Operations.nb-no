---
title: Hva er nytt eller endret i Dynamics 365 for Talent Core HR (10. september 2018)
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 for Talent Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 09/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-09-06
ms.dyn365.ops.version: Talent September 10, 2018 update
ms.openlocfilehash: 6682e4d013f006696b45e644b7b4861b34faa9bf
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/19/2019
ms.locfileid: "857413"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-september-10-2018"></a>Hva er nytt eller endret i Dynamics 365 for Talent Core HR (10. september 2018)

[!include [banner](includes/banner.md)]

**Build 8.1.138.0**

Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 for Talent Core HR.

## <a name="allow-specific-time-of-day-on-time-off-requests-half-days"></a>Tillat bestemt tidspunkt på dagen på forespørsler om fritid (halve dager)

Hvis permisjon og fravær er satt opp slik at fritid sendes inn i dager, kan du nå også muliggjøre en halvdagsdefinisjon. Når brukere deretter sender forespørsler om fritid, de kan angi om de vil ber om den første delen eller den andre delen av fridagen.

Dette alternativet deaktivert som standard. For at ansatte skal kunne be om den første eller andre halvdelen av dagen, må du aktivere dette alternativet i området **Permisjon og fravær** i Personale-parameterne.

Sikkerhetsrettigheten for denne funksjonen er Oppretthold parametere for Personale.

## <a name="validation-of-leave-and-absence-entries"></a>Validering av permisjons og fraværsoppføringer

Avhengig av hvordan permisjon er konfigurert, vil ansatte som prøver å sende en forespørsel om fritid som er lengre enn deres virkedag, få en advarsel. De blir med andre ord varslet hvis de prøver å ta mer enn en hel dag fri på en gitt dato.

Denne valideringen er alltid aktivert. Hver gang ansatte overskrider dagsterskelen som er definert, får de en advarsel i fritidsforespørselen.

## <a name="additional-fields-for-conditional-statements-in-workflows"></a>Flere felt for betingelsesuttrykk i arbeidsflyter

Flere felt er lagt til for betingelsesuttrykk og plassholdere for flere arbeidsflyter i Core HR.

Følgende felt er lagt til i arbeidsflytene for kompensasjon, oppsigelse og overføring:

- Ansettelsestype
- Juridisk enhet
- Justert startdato for arbeider
- Oppsigelsesvarsel for arbeidsgiver
- Oppsigelsesenhet for arbeidsgiver
- Overgangsdato
- Oppsigelsesvarsel for arbeider
- Arbeiderens startdato
- Oppsigelsesenhet for arbeider
- Sluttdato for prøvetid
- Posisjon
- Fagforening
- Avdeling
- Stillingstype
- CompLocation
- Stillingstittel
- Jobb
- Jobbtype
- Jobbserie
- Jobbfunksjon

Følgende felt er lagt til i arbeidsflyten for stilling:

- Posisjon
- Fagforening
- Avdeling
- Stillingstype
- CompLocation
- Stillingstittel
- Jobb
- Jobbtype
- Jobbserie
- Jobbfunksjon

Feltene i betingelsesuttrykk og plassholdere er tilgjengelige for alle brukere som har tilgang til å konfigurere arbeidsflytene nevnt ovenfor.

## <a name="navigation-to-attract-from-personnel-management"></a>Gå til Attract fra personaladministrasjon

I personaladministrasjon, hvis Attract ikke er satt opp i delen **Kandidater som skal ansettes**, blir brukerne dirigert til å komme i gang med Attract, i stedet for å vise meldingen "Fant ingenting å vise her".

## <a name="other-changes"></a>Andre endringer

Denne versjonen inneholder flere andre feilrettinger:

- Når en entreprenør ansettes, skal kategorien **Kompensasjon** ikke skal være tilgjengelig på forespørsels-/handlingssiden.
- Under Be om avslutning-prosessen kan du ikke fortsette før alle nødvendige felt inneholder data.
- Problemer med sorteringsrekkefølge og datovisning i analyse av personaladministrasjon er løst.
