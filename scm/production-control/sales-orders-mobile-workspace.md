---
title: "Mobilt område for salgsordrer for Microsoft Dynamics 365 for Operations-appen"
description: "Med det mobile arbeidsområdet for salgsordrer, du kan holde deg oppdatert på salgsordrene hvor som helst og når som helst."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 267134
ms.assetid: dbc6dc39-b535-42d3-9fbd-4724597388ad
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mirzaab
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 7a0a2af2094e3e5be757d3dd82255769677b96ea
ms.openlocfilehash: 851c53e1c53fb37488ed86e25e3ede83ca0541db
ms.lasthandoff: 03/31/2017


---

# <a name="sales-orders-mobile-workspace-for-microsoft-dynamics-365-for-operations-app"></a>Mobilt område for salgsordrer for Microsoft Dynamics 365 for Operations-appen

Med det mobile arbeidsområdet for salgsordrer, du kan holde deg oppdatert på salgsordrene hvor som helst og når som helst. 

<a name="prerequisites"></a>Forutsetninger
-------------

| Forutsetning                                                         | beskrivelse                                                                                                                                                                   |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Les om Microsoft Dynamics 365 for Operations-mobilplattform | [Dynamics 365 for Operations-mobilplattform](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform)                                                              |
| Dynamics 365 for Operations                                          | Pass på at du bruker et miljø som har Microsoft Dynamics 365 for Operations versjon 1611 og for Microsoft Dynamics for Operations plattformoppdatering 3 (november 2016). |
| Hurtigreparasjon KB 3215650                                                    | Installer hurtigreparasjonen for å aktivere arbeidsområder som finnes i Microsoft Dynamics 365 for Operations.                                                                       |
| Mobilenhet som har Dynamics 365 for Operations-appen installert | Last ned Dynamics 365 for Operations-appen fra appbutikken for mobilenheten.                                                                                                      |

## <a name="overview"></a>Oversikt
Dette mobile arbeidsområdet har tilgang til Dynamics 365 for Operations-appen, og lar deg vise detaljert informasjon om hver salgsordre, for eksempel ordrestatus, kontaktinformasjon for kunde og kontaktinformasjon for ordremottaker. Det mobile arbeidsområdet inneholder en øyeblikkelig visning av salgsordrer. Du kan vise salgsordrer etter kunde, vis alle salgsordrer eller vise informasjon om en bestemt salgsordre. Det mobile arbeidsområdet inneholder to visninger som lar deg analysere salgsordrer i dybden.

### <a name="view-all-sales-orders"></a>Vis alle salgsordrer

Denne visningen viser alle salgsordrer.

-   Bruk ett av filtrene nedenfor for velger du salgsordren du vil vise.
    -   Søk etter salgsordre
    -   Søk etter kundekonto
    -   Søk etter kundenavn
    -   Søk etter status
    -   Søk etter frigivelsesstatus
    -   Søk etter opprettingsdato og -klokkeslett

<!-- -->

-   Når du har valgt salgsordrene, kan du vise detaljene for bestemte ordrer. Du kan for eksempel vise:
    -   Informasjon om navn og adresse for kunde
    -   Ulike salgsordredatoer, for eksempel ønsket forsendelsesdato og bekreftet forsendelsesdato.
    -   Kontaktinformasjon for ordremottaker
    -   Kontaktinformasjon for kunde
    -   Ordrelinjer
    -   Forsendelser som viser hvordan og når en salgsordre er levert

### <a name="view-orders-for-a-customer-"></a>Vis ordrer for en kunde

Denne visningen viser salgsordrer per kunde.

-   Bruk et av filtrene nedenfor for å vise ordrer for en kunde.
    -   Søk etter navn
    -   Søk etter konto

<!-- -->

-   Når du velger en kunde, kan du vise:
    -   Navn på kunde og gruppe
    -   Kontaktinformasjon for kunde
    -   Kundesalgsordrer og detaljer om salgsordrene:
        -   Informasjon om navn og adresse for kunde
        -   Andre salgsordredatoer
        -   Kontaktinformasjon for ordremottaker
        -   Kontaktinformasjon for kunde
        -   Ordrelinjer
        -   Forsendelser som viser hvordan og når salgsordrer er levert

## <a name="get-started"></a>Kom i gang
Følg fremgangsmåten nedenfor for å komme i gang med det mobile arbeidsområdet for salgsordrer på mobilenheten.

1.  Last ned og installer Microsoft Dynamics 365 for Operations-appen fra appbutikken for mobilenheten.
2.  Start appen på enheten.
3.  Skriv inn URL-adressen for Dynamics 365.
4.  Angi firmaet for å logge på. Skriv for eksempel **USMF**.
5.  Første gang du logger deg på, blir du bedt om brukernavn og passord for din Microsoft Dynamics 365 for Operations-konto. Angi legitimasjon. Når du har logget deg på, kan du se tilgjengelige arbeidsområder for firmaet.

Hvis du vil vise arbeidsområder på mobilappen, må du først publisere ønskede arbeidsområder til Dynamics 365 for Operations-appen.

1.  Start Dynamics 365 for Operations.
2.  Gå til **Systemadministrasjon** &gt; **Oppsett** &gt; **systemparametere**.
3.  Velg **Administrer mobilapp**.
4.  Velg arbeidsområdet for å publisere til den mobile plattformen.
5.  Velg **Publiser arbeidsområde**.
6.  Oppdater enheten for å se de publiserte arbeidsområdene.

## <a name="view-information-about-sales-orders-for-a-customer"></a>Viser informasjon om salgsordrer for en kunde.
1.  Velg **Salgsordrer**-arbeidsområdet på mobilenheten.
2.  Velg **Vis ordrer for en kunde**.
3.  Bruk informasjonen **Konto** eller **Kundenavn** for å finne den aktuelle kunden.
4.  Velg kunden.
5.  Velg **Kontaktinformasjon** eller **Salgsordrer**.
6.  Hvis **Salgsordrer** er valgt, vises en liste over salgsordrer for kunden.
7.  Velg **Salgsordre**.
8.  Her kan du vise informasjon om salgsordrelinjer, leveringer, kontaktinformasjon for kunden og kontaktinformasjon for ordremottaker.




