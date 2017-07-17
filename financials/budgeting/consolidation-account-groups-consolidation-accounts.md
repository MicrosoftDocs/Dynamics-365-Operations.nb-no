---
title: Konsolideringskontogrupper og flere konsolideringskontoer
description: Dette emnet gir informasjon om konsolideringskontogrupper og flere konsolideringskontoer, og forklarer hvordan de brukes i Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 265544
ms.assetid: 71c31df7-b655-46a8-8844-4f92a8bd71b0
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 835669de01deb1ba0dcc5752d9d6d8f498e6ff7d
ms.contentlocale: nb-no
ms.lasthandoff: 06/13/2017


---

# Konsolideringskontogrupper og flere konsolideringskontoer
<a id="consolidation-account-groups-and-additional-consolidation-accounts" class="xliff"></a>

[!include[banner](../includes/banner.md)]


Dette emnet gir informasjon om konsolideringskontogrupper og flere konsolideringskontoer, og forklarer hvordan de brukes i Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.

Konsolideringskontogrupper
<a id="consolidation-account-groups" class="xliff"></a>
----------------------------

Med konsolideringskontogrupper kan du opprette grupper med kontoer som du vil bruke til å konsolidere dataene. Som oftest representerer en konsolideringskontogruppe en lovpålagt kontoplan eller tilordner kontoer til en gruppe som er definert av selskapets hovedkontor. Du kan finne konsolideringskontogrupper i **Oppsett**-området i **Konsolideringer**-modulen. Når du legger til en ny gruppe, angir du en unik ID for kontogruppen og et navn.

## Flere konsolideringskontoer
<a id="additional-consolidation-accounts" class="xliff"></a>
Med flere konsolideringskontoer kan du tilordne en konto fra en eksisterende kontoplan til en konsolideringskontogruppe. Deretter kan du angi en verdi og et navn for konsolideringskontoen. 

Du kan finne flere konsolideringskontoer i **Oppsett**-området i **Konsolideringer**-modulen. Når du oppretter en ny konsolideringskonto, må du angi følgende informasjon:

-   **Hovedkonto** – Dette feltet er et oppslagsfelt som viser alle hovedkontoer som er basert på kontoplanen som du valgte på siden. Når du velger en konto, angis navnet automatisk i feltet **Navn på hovedkonto**.
-   **Konsernkontogruppe** – Bruk dette feltet til å angi gruppen du vil tilordne kontoen til. Hvis du konsoliderer på to forskjellige måter, må du legge til samme konto i alle fire konsolideringskontogrupper.
-   **Konsolideringskonto** – Angi verdien for konsolideringskontoen. Denne verdien må ikke være en konto fra en kontoplan. Det kan være en hvilken som helst verdi du trenger.
-   **Navn på konsolideringskonto** – Angi navnet på kontoen slik du vil at det skal vises i forespørsler og rapporter.
-   **SAT-nivå** – Dette feltet brukes til å rapportere kontoutdrag til meksikanske skattemyndigheter. 

Når du er ferdig med å opprette konsolideringskontogruppene og ekstra konsolideringskontoer, kan du velge gruppen i den elektroniske konsolideringsprosessen.





