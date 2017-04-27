---
title: "Mobilt arbeidsområde for kostnadskontroll for Microsoft Dynamics 365 for Operations-appen"
description: "Med mobilt arbeidsområde for kostnadskontroll kan kostsenterledere se kostsenterresultater når som helst og hvor som helst."
author: YuyuScheller
manager: AnnBe
ms.date: 2017-01-12 16 - 53 - 04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 267114
ms.assetid: 84740472-494f-444c-9b74-f83b7342fd25
ms.search.region: global
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: c8c96dc9705688308dd4a5c720700ddc17657d75
ms.openlocfilehash: 8136efb1d2669c39fcc0f80b60e80ecae983d5d8
ms.lasthandoff: 03/31/2017


---

# <a name="cost-controlling-mobile-workspace-for-microsoft-dynamics-365-for-operations-app"></a>Mobilt arbeidsområde for kostnadskontroll for Microsoft Dynamics 365 for Operations-appen

Med mobilt arbeidsområde for kostnadskontroll kan kostsenterledere se kostsenterresultater når som helst og hvor som helst. 

<a name="prerequisites"></a>Forutsetninger
-------------

| Forutsetning                                                         | beskrivelse                                                                                                                                                                   |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Les om Microsoft Dynamics 365 for Operations-mobilplattform | [Dynamics 365 for Operations-mobilplattform](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform)                                                              |
| Dynamics 365 for Operations                                          | Pass på at du bruker et miljø som har Microsoft Dynamics 365 for Operations versjon 1611 og for Microsoft Dynamics for Operations plattformoppdatering 3 (november 2016). |
| Hurtigreparasjon KB 3215650                                                    | Installer hurtigreparasjonen for å aktivere arbeidsområder som finnes i Microsoft Dynamics 365 for Operations.                                                                       |
| Mobilenhet som har Dynamics 365 for Operations-appen installert | Last ned Dynamics 365 for Operations-appen fra appbutikken for mobilenheten.                                                                                                      |

## <a name="introduction"></a>Innledning
Mobilt arbeidsområde for kostnadskontroll gir en øyeblikkelig visning av den gjeldende ytelsen til kostsentre ved å sammenligne faktiske kostnader med de budsjetterte kostnadene. Du kan drille ned til statusene for individuelle kostnadselementer.

### <a name="example"></a>Eksempel

En ansatt mottar en invitasjon til en internasjonal konferanse. Organisasjonen må dekke alle reiseutgifter. Den ansatte ber om lederen om tillatelse til å delta på konferansen. Lederen åpner raskt det mobile arbeidsområdet for kostnadskontroll på mobiltelefonen for å se om han har budsjettert for at den ansatte kan delta på konferansen.

### <a name="data-security"></a>Datasikkerhet

Dataene i arbeidsområdet for kostnadskontroll er sikret gjennom brukerlegitimasjon. En kostsenterleder kan bare se data for sitt eget kostsenter. Tilgangsnivåsikkerhet behandles i kostnadsregnskapsmodulen. Regnskapsførere definerer konfigurasjonen av det mobile arbeidsområdet for kostnadskontroll i kostnadsregnskapsmodulen. Når arbeidsområdet er publisert til Microsoft Dynamics-365 for Operations-appen, er det tilgjengelig i Dynamics 365 for Operations-mobilappen. Dette sikrer at alle kostsenterledere i organisasjonen ser dataene i det samme formatet.

### <a name="actions-views-and-links"></a>Handlinger, visninger og koblinger

Mobilt arbeidsområde for kostnadskontroll for Dynamics 365 for Operations-appen gir følgende handlinger, visninger og koblinger:

-   Handlinger 
    -   Velg **Konfigurasjoner** for å velge et oppsett.
    -   Velg **Kostnadsobjekter** for å velge kostsentre der du vil filtrere data. **Merk:** Listen vises i henhold til tilgangen som gis i kostnadsregnskapsmodulen.

<!-- -->

-   Basert på hva som er valgt **Handlinger** og hva som er konfigurert i kostnadsregnskapsmodulen, kan du vise følgende informasjon i kortene. Vær oppmerksom på at beløpet vises i samme format: faktisk, budsjett, avvik og varians %. 
    -   Faktisk i forhold til budsjett (gjeldende periode)
    -   Faktisk i forhold til revidert budsjett (gjeldende periode)
    -   Faktisk i forhold til budsjett (forrige periode)
    -   Faktisk i forhold til revidert budsjett (forrige periode)
    -   Faktisk i forhold til budsjett (hittil i år)
    -   Faktisk i forhold til revidert budsjett (hittil i år)

<!-- -->

-   Koblinger
    -   Detaljer for gjeldende periode.
    -   Detaljer for forrige periode.
    -   Detaljer for hittil i år.

Når du velger en av koblingene, vises et kort per kostnadselement. Beløpet i kortene vises i følgende format: faktisk, budsjett, budsjettavvik, budsjettavviks-%, revidert budsjett, revidert budsjettavvik og revidert budsjettavviks-%.  [![kostnad-kontroll](./media/cost-controlling.png)](./media/cost-controlling.png)

## <a name="get-started"></a>Kom i gang
Følg fremgangsmåten nedenfor for å komme i gang med mobilappen for kostnadskontroll på mobilenheten.

1.  Last ned og installer Microsoft Dynamics 365 for Operations-appen fra appbutikken for mobilenheten.
2.  Start appen på enheten.
3.  Skriv inn URL-adressen for Dynamics 365.
4.  Angi firmaet for å logge på. Skriv for eksempel **USMF**.
5.  Første gang du logger deg på, blir du bedt om brukernavn og passord for din Microsoft Dynamics 365 for Operations-konto. Angi legitimasjon. Når du har logget deg på, kan du se tilgjengelige arbeidsområder for firmaet.

Hvis du vil vise arbeidsområder på mobilappen, må du først publisere ønskede arbeidsområder til Dynamics 365 for Operations-appen.

1.  Start Dynamics 365 for Operations.
2.  Gå til **Systemadministrasjon** &gt; **Oppsett** &gt; **systemparametere**.
3.  Velg **Administrer mobilapp**.
4.  Velg arbeidsområdet **Kostnadskontroll **for å publisere til den mobile plattformen.
5.  Velg **Publiser arbeidsområde**.
6.  Oppdater enheten for å se de publiserte arbeidsområdene.

## <a name="view-the-performance-of-your-cost-center"></a>Vise ytelsen til kostsenteret
1.  Velg **Kostnadskontroll**-arbeidsområdet på mobilenheten.
2.  Velg **Kostnadsobjektobjekt**.
3.  Klikk **Handlinger**.
4.  Klikk **Velg konfigurasjon** for å velge et kostnadskontrolloppsett.
5.  Klikk **Ferdig**.
6.  Klikk **Handlinger**.
7.  Klikk **Velg kostnadsobjekt** for å velge kostsentrene du har fått tilgang til.
8.  Klikk **Ferdig**.
9.  Vis den totale ytelsen til kostsenteret.
10. Klikk **Detaljer for gjeldende periode**.
11. Vise ytelsen til individuelle kostnadselementer.
12. Du kan også søke etter bestemte kostnadselementer.



