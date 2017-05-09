---
title: "Mobil område for beholdning på lager for Microsoft Dynamics 365 for Operations-appen"
description: "Beholdningen på lager mobile arbeidsområdet kan du få mobile innsikt i lager, reservert og tilgjengelig når som helst og hvor som helst."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 267094
ms.assetid: 85058f55-e566-40e2-9234-42d3e4fe5ff6
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mirzaab
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 7a0a2af2094e3e5be757d3dd82255769677b96ea
ms.openlocfilehash: 2ad48765528e1d1c6e7c90417b54a248ec79f546
ms.lasthandoff: 03/31/2017


---

# <a name="inventory-on-hand-mobile-workspace-for-microsoft-dynamics-365-for-operations-app"></a>Mobil område for beholdning på lager for Microsoft Dynamics 365 for Operations-appen

Beholdningen på lager mobile arbeidsområdet kan du få mobile innsikt i lager, reservert og tilgjengelig når som helst og hvor som helst. 

<a name="prerequisites"></a>Forutsetninger
-------------

| Forutsetning                                                         | beskrivelse                                                                                                                                        |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Les om Microsoft Dynamics 365 for Operations-mobilplattform | [Dynamics 365 for Operations-mobilplattform](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform)                                   |
| Dynamics 365 for Operations                                          | Et miljø som har Microsoft Dynamics 365 for Operations versjon 1611 og for Microsoft Dynamics for Operations plattformoppdatering 3 (november 2016) |
| Hurtigreparasjon KB 3215650                                                    | Installer hurtigreparasjonen for å aktivere arbeidsområder som finnes i Microsoft Dynamics 365 for Operations.                                       |
| Mobilenhet som har Dynamics 365 for Operations-appen installert | Last ned Dynamics 365 for Operations-appen fra appbutikken for mobilenheten.                                                                           |

## <a name="introduction"></a>Innledning
Selskaper har vanligvis flere leveringer og flere mottak til lager hver dag. Disse flyttingene endrer kontinuerlig lagerbeholdningsstatusen. Beholdningen på lager mobile arbeidsområdet lar deg se status for firmaene i lagerbeholdningen, slik at du kan få den nyeste innsikten i lagerdata på den mobile enheten du velger. Uansett om du arbeider i lager, innkjøp, salg, produksjon eller management, eller har andre roller, kan du få tilgang til dataene i lagerbeholdningen når som helst og hvor som helst. Det mobile arbeidsområdet gir deg øyeblikkelig status på lager på tvers av lokaler, og lar deg vise lagerbeholdning på tvers av lokaler, gjeldende materialereservasjoner og ureservert lagerbeholdning. Du kan også angi varenumrene for å spørre om lagerbeholdning og filtrert søke etter produkter på lager eller varianter. Spesielt inneholder mobil arbeidsområdet disse funksjonene:

-   Du kan søke etter produktnummeret eller produktnavnet for å finne produkter å vise lagerbeholdning status for.
-   For de valgte produktene kan du vise følgende informasjon:
    -   Lagerbeholdning etter område
    -   Lagerbeholdning etter lager
    -   Lagerbeholdning etter lokasjon
    -   Lagerbeholdning etter parti (for partikontrollerte produkter)
    -   Lagerbeholdning etter beholdningsstatus

<!-- -->

-   Lagerbeholdning for produktet vises på følgende måter:
    -   Etter fysisk lager (denne visningen representerer den totale mengden).
    -   Etter fysisk reservert (denne visningen representerer den reserverte mengden).
    -   Etter fysisk tilgjengelig (denne visningen representerer tilgjengelig mengde uten reservasjoner.)

## <a name="get-started"></a>Kom i gang
Å komme i gang på den mobile enheten:

1.  Last ned og installer Microsoft Dynamics 365 for Operations-appen fra appbutikken for mobilenheten.
2.  Start appen på enheten.
3.  Skriv inn URL-adressen for Dynamics 365.
4.  Angi firmaet for å logge på. Skriv for eksempel **USMF**.
5.  Første gang du logger deg på, du blir bedt om brukernavn og passord for din Microsoft Dynamics 365 for Operations-konto. Angi legitimasjon. Når du har logget deg på, kan du se tilgjengelige arbeidsområder for firmaet.

Hvis du vil vise arbeidsområder på mobilappen, må du først publisere ønskede arbeidsområder til Dynamics 365 for Operations-appen.

1.  Start Dynamics 365 for Operations.
2.  Gå til **Systemadministrasjon** &gt; **Oppsett** &gt; **systemparametere**.
3.  Velg **Administrer mobilapp**.
4.  Velg arbeidsområdet for å publisere til den mobile plattformen.
5.  Velg **Publiser arbeidsområde**.
6.  Oppdater enheten for å se de publiserte arbeidsområdene.

## <a name="view-the-onhand-inventory-for-a-product"></a>Vise lagerbeholdning for et produkt
1.  Velg **Lagerbeholdning**-arbeidsområdet på mobilenheten.
2.  Velg **Kontroller lagerbeholdning for en vare**. Du kan se en liste over produkter som er lastet inn i ditt program for frakoblet bruk. 50 varer blir lastet inn som standard, men du kan endre dette antallet. Hvis du vil ha mer informasjon, kan du se før Les håndboken.
3.  Hvis elementet ikke finnes i listen, velger du **Søk mer** for å utføre en online søk i Dynamics 365 for Operations. Søk etter produktnummer, eller bytte til et søk etter produktnavn.
4.  Velg et produkt. Hvis varen har et bilde, vises bildet.
5.  Velg ett av følgende alternativer for å vise lagerbeholdningens status:
    -   Vis lagerbeholdning etter område
    -   Vis lagerbeholdning etter lager
    -   Vis lagerbeholdning etter lokasjon
    -   Vis lagerbeholdning etter parti (for partikontrollerte produkter)
    -   Vis lagerbeholdning per beholdningsstatus

    Lagerbeholdning for produktet vises på følgende måter:
    -   Etter fysisk lager (denne visningen representerer den totale mengden).
    -   Etter fysisk reservert (denne visningen representerer den reserverte mengden).
    -   Etter fysisk tilgjengelig (denne visningen representerer tilgjengelig mengde uten reservasjoner.)




