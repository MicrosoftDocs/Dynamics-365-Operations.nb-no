---
title: Konsernkontogrupper og flere konsernkontoer
description: Dette emnet gir informasjon om konsernkontogrupper og flere konsernkontoer, og forklarer hvordan de brukes i Microsoft Dynamics 365 for operasjoner.
author: RobinARH
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 265544
ms.assetid: 71c31df7-b655-46a8-8844-4f92a8bd71b0
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 9f4d7fdd8cfa7a540fce219f6ae4792e57dfbe44
ms.openlocfilehash: f9c5aaa389c9c2f85d1ab91cbf3d2222cbebef55
ms.lasthandoff: 03/31/2017


---

# <a name="consolidation-account-groups-and-additional-consolidation-accounts"></a>Konsernkontogrupper og flere konsernkontoer

Dette emnet gir informasjon om konsernkontogrupper og flere konsernkontoer, og forklarer hvordan de brukes i Microsoft Dynamics 365 for operasjoner.

<a name="consolidation-account-groups"></a>Konsolideringskontogrupper
----------------------------

Konsernkontogrupper kan du opprette grupper med kontoer som du vil bruke til å konsolidere dataene. Som oftest en konsernkontogruppen representerer en offentlig obligatorisk Kontoplan eller tilordner kontoer til en gruppe som er definert av selskapets hovedkontor. Du kan finne konsolidering kontogrupper i den **oppsett** området i den **konsolideringer** modul. Når du legger til en ny gruppe, angir du en unik ID for kontogruppen og et navn.

## <a name="additional-consolidation-accounts"></a>Flere konsolideringskontoer
Flere konsernkontoer kan du tilordne en konto fra en eksisterende kontoplanen til en konsernkontogruppen. Deretter kan du angi en verdi for konsolidering konto og et navn. 

Finner du ytterligere konsolidering kontoer i den **Setup** området i den **konsolideringer** modul. Når du oppretter en ny konto for konsolidering, må du angi følgende informasjon:

-   **Hovedkontoen** – dette feltet er et oppslagsfelt som viser alle hovedkontoer som er basert på kontoplanen som du valgte på siden. Når du velger en-konto, angis navnet automatisk i den **Main kontonavnet** feltet.
-   **Konsernkontogruppen** – Bruk dette feltet til å angi gruppe hvis du vil tilordne til kontoen. Hvis du konsoliderer på to forskjellige måter, må du legge til samme konto alle fire konsernkontogrupper.
-   **Konsernkonto** – angi verdien for konsolideringskontoen. Denne verdien må ikke være en konto fra en kontoplan. Det kan være en hvilken som helst verdi du trenger.
-   **Navn på konsernkonto** – angi navnet på kontoen som du vil det skal vises i forespørsler og rapporter.
-   **SAT nivå** – dette feltet brukes til å rapportere kontoutdrag til Meksikanske skattemyndighetene. 

Når du er ferdig med å opprette kontogrupper for konsolidering og flere konsernkontoer, velger du gruppen i Konsolider online prosessen.



