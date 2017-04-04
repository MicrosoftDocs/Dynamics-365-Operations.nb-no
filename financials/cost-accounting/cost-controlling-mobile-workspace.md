---
title: "Kostnad kontrollerende mobile arbeidsområdet for Microsoft Dynamics 365 for operasjoner app"
description: "Med kostnaden kan styre mobile arbeidsområde, cost center ledere se center kostnadsresultater når som helst og hvor som helst."
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

# <a name="cost-controlling-mobile-workspace-for-microsoft-dynamics-365-for-operations-app"></a>Kostnad kontrollerende mobile arbeidsområdet for Microsoft Dynamics 365 for operasjoner app

Med kostnaden kan styre mobile arbeidsområde, cost center ledere se center kostnadsresultater når som helst og hvor som helst. 

<a name="prerequisites"></a>Forutsetninger
-------------

| Forutsetning                                                         | beskrivelse                                                                                                                                                                   |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Les om Microsoft Dynamics-365 for mobil plattform for operasjoner | [Dynamics 365 for mobil plattform for operasjoner](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform)                                                              |
| Dynamics 365 for operasjoner                                          | Pass på at du bruker et miljø som har Microsoft Dynamics 365 for operasjoner versjon 1611 og for Microsoft Dynamics for operasjoner plattform oppdatere 3 (November 2016). |
| Hurtigreparasjonen KB 3215650                                                    | Installere hurtigreparasjonen for å aktivere arbeidsområder som finnes i Microsoft Dynamics 365 for operasjoner.                                                                       |
| Mobil enhet som Dynamics-365 for operasjoner app installert | Last ned Dynamics-365 for operasjoner app fra din mobile app lager.                                                                                                      |

## <a name="introduction"></a>Innledning
Kostnaden styre mobile arbeidsområdet gir en gang se gjeldende ytelsen til kostsentre ved å sammenligne faktiske kostnader mot de budsjetterte kostnadene. Du kan gå nedover statusene for individuelle kostnadselementer.

### <a name="example"></a>Eksempel

En ansatt mottar en invitasjon til en internasjonal konferanse. Organisasjonen må dekke alle reiseutgifter. Ansatt som ber om hans manger hvis han kan delta på konferansen. Prosjektlederen åpner kostnaden styre mobile arbeidsområde på hans mobiltelefon til å se om han har budsjettet for ansatt til å delta på konferansen.

### <a name="data-security"></a>Datasikkerhet

Dataene i kostnaden kontrollere arbeidsområdet er sikret av legitimasjonsbeskrivelser for bruker. En kostnad center manager er bare tillatt å se data for sin egen kostsenter. Sikkerhet på brukernivå i access behandles i kostnadsregnskapsmodulen. Kostnaden regnskapsførere definere kostnaden kontrollere konfigurasjonen for mobile arbeidsområdet i kostnadsregnskapsmodulen. Når arbeidsområdet er publisert på Microsoft Dynamics-365 for operasjoner app, er funksjonen tilgjengelig i Dynamics-365 for operasjoner mobile app. Dette sikrer at alle kostnader center ledere i organisasjonen titt på dataene i det samme formatet.

### <a name="actions-views-and-links"></a>Handlinger, visninger og koblinger

Kostnaden styre mobile arbeidsområde for Dynamics 365 for operasjoner app gir følgende handlinger, visninger og koblinger:

-   Handlinger 
    -   Velg **konfigurasjoner** til å velge et oppsett.
    -   Velg **kostobjekter** å plukke kostsentre som du vil filtrere data. **Merk:** listen vises i henhold til tilgangen som gis i kostnadsregnskapsmodulen.

<!-- -->

-   Basert på hva som er valgt **handlinger** og hva er konfigurert i kostnadsregnskapsmodulen, kan du vise følgende informasjon i kortene. Vær oppmerksom på at beløpet som vises i samme format: faktisk, budsjett, avvik og varians %. 
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

Når du velger en av koblingene, vises et kort per element for kost. Beløpet i kortene vises i følgende format: faktisk, budsjett, Budsjettavvik, budsjett avviks-%, revidert budsjett, revidert Budsjettavvik og revidert budsjett avviks-%.  [![kontroll av kostnader](./media/cost-controlling.png)](./media/cost-controlling.png)

## <a name="get-started"></a>Kom i gang
Følg disse trinnene for å komme i gang med kostnader kontroll mobile app på den mobile enheten.

1.  På din mobile app-butikk, kan du laste ned og installere Microsoft Dynamics 365 for operasjoner app.
2.  Start programmet på enheten.
3.  Skriv inn URL-adressen Dynamics 365.
4.  Angi firmaet å logge på. Angi for eksempel **USMF**.
5.  Første gang du logger deg på, du blir bedt om brukernavn og passord for din Microsoft Dynamics-365 for kontoen for operasjoner. Angi legitimasjonen. Når du logger deg på, kan du se tilgjengelige arbeidsområder for firmaet.

Hvis du vil vise arbeidsområder på din mobile app, må du først publisere ønsket arbeidsområder til Dynamics-365 for operasjoner app.

1.  Starte Dynamics 365 for operasjoner.
2.  Gå til **systemadministrasjon**&gt;**Setup**&gt;**systemparametere**.
3.  Velg **behandle mobile app**.
4.  Velg arbeidsområdet ** koster kontrollere ** å publisere til mobil plattform.
5.  Velg **publisere arbeidsområde for**.
6.  Oppdatere enheten for å se de publiserte delte arbeidsområdene.

## <a name="view-the-performance-of-your-cost-center"></a>Vise ytelsen til din kostsenter
1.  På den mobile enheten, velger du den **koster kontroll av** arbeidsområde.
2.  Velg **koster objektet styrer**.
3.  Klikk **handlinger**.
4.  Klikk **Select configuration** til å velge en kostnad som kontrollerer oppsettet.
5.  Klikk **gjort**.
6.  Klikk **handlinger**.
7.  Klikk **velger kostobjekt** til å velge kostsentre som du har fått tilgang.
8.  Klikk **gjort**.
9.  Vis den generelle ytelsen til din kostsenter.
10. Klikk **detaljer for gjeldende periode**.
11. Vise ytelsen til individuelle kostnadselementer.
12. Du kan også søke etter bestemte kostnadselementer.



