---
title: "Salgsordrer mobile arbeidsområdet for Microsoft Dynamics 365 for operasjoner app"
description: "Med mobile arbeidsområdet salgsordrer, du kan holde deg oppdatert på salgsordrene hvor som helst og når som helst."
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

# <a name="sales-orders-mobile-workspace-for-microsoft-dynamics-365-for-operations-app"></a>Salgsordrer mobile arbeidsområdet for Microsoft Dynamics 365 for operasjoner app

Med mobile arbeidsområdet salgsordrer, du kan holde deg oppdatert på salgsordrene hvor som helst og når som helst. 

<a name="prerequisites"></a>Forutsetninger
-------------

| Forutsetning                                                         | beskrivelse                                                                                                                                                                   |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Les om Microsoft Dynamics-365 for mobil plattform for operasjoner | [Dynamics 365 for mobil plattform for operasjoner](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform)                                                              |
| Dynamics 365 for operasjoner                                          | Pass på at du bruker et miljø som har Microsoft Dynamics 365 for operasjoner versjon 1611 og for Microsoft Dynamics for operasjoner plattform oppdatere 3 (November 2016). |
| Hurtigreparasjonen KB 3215650                                                    | Installere hurtigreparasjonen for å aktivere arbeidsområder som finnes i Microsoft Dynamics 365 for operasjoner.                                                                       |
| Mobil enhet som Dynamics-365 for operasjoner app installert | Last ned Dynamics-365 for operasjoner app fra din mobile app lager.                                                                                                      |

## <a name="overview"></a>Oversikt
Arbeidsområdet mobile har tilgang til Dynamics-365 for operasjoner program og kan du vise detaljert informasjon om hver salgsordre, for eksempel ordrestatusen, kontaktinformasjon for kunden og rekkefølge taker kontaktinformasjon. Mobile arbeidsområdet inneholder en øyeblikkelig visning av ordrer. Du kan vise ordrer per kunde, eller Vis alle salgsordrer, eller Vis informasjon om en bestemt salgsordre. Mobile arbeidsområdet inneholder to visninger for å analysere salg ordrer i dybden.

### <a name="view-all-sales-orders"></a>Vis alle salgsordrer

Denne visningen viser alle salgsordrer.

-   Bruk en av følgende filtre til velger du salgsordren du vil vise.
    -   Søk etter salgsordren.
    -   Søke etter kundekonto
    -   Søke etter kundenavn
    -   Søke etter status
    -   Søk etter publiseringsstatus
    -   Søk etter dato og klokkeslett

<!-- -->

-   Når du velger ordrer, kan du vise detaljene for bestemte ordrer. Nærmere bestemt kan du vise:
    -   Informasjon om navn og adresse for kunde
    -   Annen salgsordre datoer, for eksempel ønsket forsendelsesdato og bekreftet forsendelsesdato.
    -   Rekkefølge taker kontaktinformasjon
    -   Opplysninger om kundekontakt
    -   Ordrelinjer
    -   Forsendelser som viser hvordan og når en salgsordre er levert

### <a name="view-orders-for-a-customer-"></a>Vis ordrer for kunde ** **

Denne visningen viser ordrer per kunde.

-   Bruk en av følgende filtre for å vise ordrer for en kunde.
    -   Søk etter navn
    -   Søk etter konto

<!-- -->

-   Når du velger en kunde, kan du vise:
    -   Kundenavnet og kundegruppen
    -   Opplysninger om kundekontakt
    -   Kunde-ordrer og detaljer om ordrene:
        -   Informasjon om navn og adresse for kunde
        -   Annen salgsordre datoer
        -   Rekkefølge taker kontaktinformasjon
        -   Opplysninger om kundekontakt
        -   Ordrelinjer
        -   Forsendelser som viser hvordan og når en salgsordre er levert

## <a name="get-started"></a>Kom i gang
Følg disse trinnene for å komme i gang med salgsordrer mobile arbeidsområdet på den mobile enheten.

1.  På din mobile app-butikk, kan du laste ned og installere Microsoft Dynamics 365 for operasjoner app.
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

## <a name="view-information-about-sales-orders-for-a-customer"></a>Visningsinformasjon om salgsordrer for en kunde
1.  På den mobile enheten, velger du **ordrer** arbeidsområde.
2.  Velg **Vis ordrer for kunde**.
3.  Bruk ** konto ** eller ** kundenavn ** informasjon for å finne den aktuelle kunden.
4.  Velg kunden.
5.  Velg **kontaktinformasjon** eller **ordrer**.
6.  Hvis **ordrer** er valgt, vil det skal vises en liste over salgsordrer for kunden.
7.  Velg **ordre**.
8.  Her kan du vise informasjon om salgsordrelinjer, leveringer, kontaktinformasjon for kunden og rekkefølge taker kontaktinformasjon.




