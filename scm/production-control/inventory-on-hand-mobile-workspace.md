---
title: "Lager beholdning mobile arbeidsområdet for Microsoft Dynamics 365 for operasjoner app"
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

# <a name="inventory-on-hand-mobile-workspace-for-microsoft-dynamics-365-for-operations-app"></a>Lager beholdning mobile arbeidsområdet for Microsoft Dynamics 365 for operasjoner app

Beholdningen på lager mobile arbeidsområdet kan du få mobile innsikt i lager, reservert og tilgjengelig når som helst og hvor som helst. 

<a name="prerequisites"></a>Forutsetninger
-------------

| Forutsetning                                                         | beskrivelse                                                                                                                                        |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Les om Microsoft Dynamics-365 for mobil plattform for operasjoner | [Dynamics 365 for mobil plattform for operasjoner](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform)                                   |
| Dynamics 365 for operasjoner                                          | Et miljø som har Microsoft Dynamics 365 for operasjoner versjon 1611 og Microsoft Dynamics for operasjoner plattform oppdatere 3 (November 2016) |
| Hurtigreparasjonen KB 3215650                                                    | Installere hurtigreparasjonen for å aktivere arbeidsområder som finnes i din Microsoft Dynamics-365 for operasjoner.                                       |
| Mobil enhet som Dynamics-365 for operasjoner app installert | Last ned Dynamics-365 for operasjoner app fra din mobile app lager.                                                                           |

## <a name="introduction"></a>Innledning
Selskaper har vanligvis flere leveringer og flere mottak til lager hver dag. Disse flyttingene endre kontinuerlig lagerbeholdning-status. Beholdningen på lager mobile arbeidsområdet lar deg se status for firmaene i lagerbeholdningen slik at du kan få de nyeste innsikt i lagerdata på den mobile enheten du velger. Uansett om du arbeider i lager, innkjøp, salg, produksjon eller management, eller har andre roller, kan du få tilgang til dataene i lagerbeholdningen når som helst og hvor som helst. Mobile arbeidsområdet gir en gang se status på lager på tvers av lokaler, og lar deg vise lagerbeholdning på tvers av lokaler, gjeldende regning reservasjoner og ureserverte lagerbeholdning. Du kan også angi varenumrene til spørringen lagerbeholdning og filtrert søke etter produkter på lager eller varianter. Spesielt inneholder mobil arbeidsområdet disse funksjonene:

-   Du kan søke etter produktnummeret eller produktnavnet for å finne produkter å vise lagerbeholdning status for.
-   For de valgte produktene, kan du vise følgende informasjon:
    -   Lagerbeholdning per område
    -   Lagerbeholdning per lager
    -   Lagerbeholdning per lokasjon
    -   Lagerbeholdning per parti (for partikontrollert produkter)
    -   Lagerbeholdning per lagerstatus

<!-- -->

-   Lagerbeholdning for produktet vises på følgende måter:
    -   Ved fysisk lager (denne visningen representerer det totale beløpet).
    -   Ved fysisk reservert (denne visningen representerer det reserverte beløpet).
    -   Ved fysisk tilgjengelig (denne visningen representerer tilgjengelig beløp som har ingen reservasjoner.)

## <a name="get-started"></a>Kom i gang
Å komme i gang på den mobile enheten:

1.  Fra din mobile app-butikk, kan du laste ned og installere Microsoft Dynamics 365 for operasjoner app.
2.  Start programmet på enheten.
3.  Skriv inn URL-adressen Dynamics 365.
4.  Angi firmaet å logge på. Angi for eksempel **USMF**.
5.  Første gang du logger deg på, du blir bedt om brukernavn og passord for din Microsoft Dynamics-365 for kontoen for operasjoner. Angi legitimasjonen. Når du logger deg på, kan du se tilgjengelige arbeidsområder for firmaet.

Hvis du vil vise arbeidsområder på din mobile app, må du først publisere ønsket arbeidsområder til Dynamics-365 for operasjoner app.

1.  Starte Dynamics 365 for operasjoner.
2.  Gå til **systemadministrasjon**&gt;**Setup**&gt;**systemparametere**.
3.  Velg **behandle mobile app**.
4.  Velg arbeidsområde til å publisere til mobil plattform.
5.  Velg **publisere arbeidsområde for**.
6.  Oppdatere enheten for å se de publiserte delte arbeidsområdene.

## <a name="view-the-onhand-inventory-for-a-product"></a>Vis lageret onhand for et produkt
1.  På den mobile enheten, velger du **lagerbeholdning** arbeidsområde.
2.  Velg **kontrollere beholdningen for en vare**. Du kan se en liste over produkter som er lastet inn i ditt program for frakoblet bruk. 50 varer blir lastet inn som standard, men du kan endre dette nummeret. Hvis du vil ha mer informasjon, kan du se før Les håndboken.
3.  Hvis elementet ikke finnes i listen, velger du **søke mer** til å utføre en online søk i Dynamics 365 for operasjoner. Søk etter produktnummer, eller bytte til et søk etter produktnavn.
4.  Velg et produkt. Hvis varen har et bilde, vises bildet.
5.  Velg ett av følgende alternativer for å vise lagerbeholdningen status:
    -   Vis lagerbeholdning per område
    -   Vis lagerbeholdning per lager
    -   Vis lagerbeholdning per lokasjon
    -   Vis lagerbeholdning per parti (for partikontrollert produkter)
    -   Vis lagerbeholdning per lagerstatus

    Lagerbeholdning for produktet vises på følgende måter:
    -   Ved fysisk lager (denne visningen representerer det totale beløpet).
    -   Ved fysisk reservert (denne visningen representerer det reserverte beløpet).
    -   Ved fysisk tilgjengelig (denne visningen representerer vises tilgjengelig beløp som har ingen reservasjoner).




