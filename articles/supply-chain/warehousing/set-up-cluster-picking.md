---
title: Definere gruppeplukking
description: Dette emnet beskriver hvordan du konfigurerer gruppeplukking og hvordan du bruker varebekreftelse med gruppeplukking.
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSClusterProfile, WHSRFAutoConfirm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 84b6d3c3caa09b9601701ca4ac1992b151c0b8d4
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/30/2019
ms.locfileid: "2249756"
---
[!include[banner](../includes/banner.md)]

# <a name="set-up-cluster-picking"></a>Definere gruppeplukking

Dette emnet beskriver hvordan du gir arbeiderne mulighet til å bruke mobile enheter til å gruppere plukkarbeid til klynger, slik at de kan plukke varer fra ett sted for flere arbeidsordrer samtidig. Dette kalles *gruppeplukking*.

## <a name="about-cluster-picking"></a>Om gruppeplukking

Etter at arbeidsordrer er frigitt til lageret, kan arbeideren bruke en mobilenhet til å tilordne ordrene til en gruppe. Gruppen organiserer plukkarbeidet for arbeideren. Når en arbeidsordre tilordnes til en gruppe, må arbeideren bruke gruppeplukking for å utføre plukkarbeidet for ordren. Arbeideren kan ikke bruke andre metoder for plukking. Hvis en arbeidsordre tilordnes en gruppe ved en feiltakelse, må arbeideren bryte gruppen og deretter opprette den på nytt.

Om nødvendig kan en arbeider sende en gruppe til en annen arbeider. Dette endrer gruppestatusen Sendt. Når arbeideren bruker en mobilenhet til å angi at plukk- og plasseringsarbeidet er fullført, må forsendelsen eller lasten bekreftes i klienten.

## <a name="set-up-cluster-picking"></a>Definere gruppeplukking

Hvis du vil aktivere gruppeplukking, må du konfigurere følgende:

-   **Gruppeprofiler** – Angi om du vil generere gruppe-IDer, antall stillinger som skal brukes, når du skal bryte grupper, og hvordan du deler opp og kontrollerer plukkarbeidet, automatisk.

-   **Arbeidsmaler** – Definer hvordan du oppretter plukkarbeidet for gruppeplukking.

-   **Lokasjonsdirektiver** – Angi hvor du vil plukke varer fra, og hvor du vil plassere dem.

-   **Menyelementer på mobilenheten** – Konfigurer et menyelement for mobilenhet til å bruke eksisterende arbeid styrt av gruppeplukking. Deretter må du legge til menyelementet på en mobilenhetsmeny slik at det blir vist på mobile enheter.

-   **Lagerstyringsparametere** – Angi nummerserien du vil bruke hvis du vil generere identifikatorer for grupper.

## <a name="set-up-a-cluster-profile"></a>Definere en gruppeprofil

Hvis du vil konfigurere en gruppeprofil, gjør du følgende:

1.  Klikk **Lagerstyring** \> **Oppsett** \> **Mobilenhet** \> **Gruppeprofiler**.

2.  Klikk **Ny** for å opprette en ny profil.

3.  Klikk **Opprett gruppe** og deretter, under **Gruppesortering**, klikker du **Ny** for å definere sorteringskriteriene for gruppen. Sorteringskriteriene bestemmer i hvilken rekkefølge arbeideren vil utføre plukkarbeidet. Du kan legge til så mange kriterier som nødvendig.

4.  I **Serienummer**-feltet angir du et tall for å definere rekkefølgen som sorteringskriteriene behandles i.

5.  I **feltnavn**-feltet velger du feltet som bestemmer sorteringen. Hvis du for eksempel velger **WMSLocationId**-feltet, blir arbeidet sorteret etter lokasjon.

6.  I **Sortering**-feltet velger du ett av følgende alternativer.

| **Alternativ**     | **Beskrivelse**                                                                                                                                                                                                                    |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Stigende**  | Plukkarbeid er delt inn i en stigende rekkefølge basert på sorteringskriteriene. Hvis du for eksempel bruker **WMSLocationId**-feltet som sorteringskriterium, og lokasjons-IDene 1, 2, 3 og 4, plukker du først fra lokasjon 4. |
| **Synkende** | Plukkarbeid er delt inn i en synkende rekkefølge basert på sorteringskriteriene. Hvis du for eksempel bruker **WMSLocationId**-feltet som sorteringskriterium, og lokasjons-IDene 1, 2, 3 og 4, plukker du først fra lokasjon 1. |

## <a name="item-confirmation"></a>Varebekreftelse

Når gruppeplukking brukes, er varebekreftelse avgjørende for å bekrefte varene som legges til i grupper. Du kan bekrefte varer i gruppeplukking mens gruppeplukkingen utføres. Oppsettet er basert på strekkodeoppsettet for produkt.

### <a name="set-up-item-verification-with-cluster-picking"></a>Definere varebekreftelse med gruppeplukking

1.  Åpne oppsettskjemaet for arbeidsbekreftelse på et menyelement for mobilenhet: **Lagerstyring** \> **Lagerstyring** \> **Oppsett** \> **Mobilenhet** \> **Menyelementer på mobilenheten**.

2.  Åpne **Arbeidsbekreftelsesoppsett** fra menyelementet på mobilenheten. Med alternativet **Produktbekreftelse** kan du bekrefte hver del av beholdningen fra den mobile enheten når den skannes.
