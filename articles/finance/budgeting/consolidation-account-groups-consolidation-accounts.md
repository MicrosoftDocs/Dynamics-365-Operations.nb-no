---
title: Konsolideringskontogrupper og flere konsolideringskontoer
description: Dette emnet gir informasjon om konsolideringskontogrupper og flere konsolideringskontoer, og forklarer hvordan de brukes i Microsoft Dynamics 365 Finance.
author: aprilolson
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerConsolidateAccountGroup
audience: Application User
ms.reviewer: roschlom
ms.custom: 265544
ms.assetid: 71c31df7-b655-46a8-8844-4f92a8bd71b0
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 245b61c8cb85ab1282a921ac99b9ac7c2efbadc5
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/04/2021
ms.locfileid: "6189427"
---
# <a name="consolidation-account-groups-and-additional-consolidation-accounts"></a>Konsolideringskontogrupper og flere konsolideringskontoer

[!include [banner](../includes/banner.md)]

Dette emnet gir informasjon om konsolideringskontogrupper og flere konsolideringskontoer, og forklarer hvordan de brukes i Microsoft Dynamics 365 Finance.

## <a name="consolidation-account-groups"></a>Konsolideringskontogrupper

Med konsolideringskontogrupper kan du opprette grupper med kontoer som du vil bruke til å konsolidere dataene. Som oftest representerer en konsolideringskontogruppe en lovpålagt kontoplan eller tilordner kontoer til en gruppe som er definert av selskapets hovedkontor. Du kan finne konsolideringskontogrupper i **Oppsett**-området i **Konsolideringer**-modulen. Når du legger til en ny gruppe, angir du en unik ID for kontogruppen og et navn.

## <a name="additional-consolidation-accounts"></a>Flere konsolideringskontoer
Med flere konsolideringskontoer kan du tilordne en konto fra en eksisterende kontoplan til en konsolideringskontogruppe. Deretter kan du angi en verdi og et navn for konsolideringskontoen. 

Du kan finne flere konsolideringskontoer i **Oppsett**-området i **Konsolideringer**-modulen. Når du oppretter en ny konsolideringskonto, må du angi følgende informasjon:

-   **Hovedkonto** – Dette feltet er et oppslagsfelt som viser alle hovedkontoer som er basert på kontoplanen som du valgte på siden. Når du velger en konto, angis navnet automatisk i feltet **Navn på hovedkonto**.
-   **Konsernkontogruppe** – Bruk dette feltet til å angi gruppen du vil tilordne kontoen til. Hvis du konsoliderer på to forskjellige måter, må du legge til samme konto i alle fire konsolideringskontogrupper.
-   **Konsolideringskonto** – Angi verdien for konsolideringskontoen. Denne verdien må ikke være en konto fra en kontoplan. Det kan være en hvilken som helst verdi du trenger.
-   **Navn på konsolideringskonto** – Angi navnet på kontoen slik du vil at det skal vises i forespørsler og rapporter.
-   **SAT-nivå** – Dette feltet brukes til å rapportere kontoutdrag til meksikanske skattemyndigheter. 

Når du er ferdig med å opprette konsolideringskontogruppene og ekstra konsolideringskontoer, kan du velge gruppen i den elektroniske konsolideringsprosessen.


Hvis du vil ha mer informasjon, kan du se [Opprette konsolideringsgrupper og flere konsolideringskontoer](../general-ledger/tasks/create-consolidation-groups.md) 





[!INCLUDE[footer-include](../../includes/footer-banner.md)]