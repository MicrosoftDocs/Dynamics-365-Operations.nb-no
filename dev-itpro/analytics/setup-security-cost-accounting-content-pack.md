---
title: "Konfigurere sikkerhet for kostnadsregnskap analysen strømmen BI-innhold"
description: "Dette emnet forklarer hvordan du kan overføre tilgang til brukersikkerhet i kostnadsregnskap radnivå sikkerhet i Microsoft Power BI. Denne funksjonaliteten hjelper med å garantere at brukere bare se strømmen BI data som de har tilgang til."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations
ms.custom: 270294
ms.assetid: 3a7ba8b0-ac57-4159-9cd8-4308f6021f36
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 1e42622e7621c645d7eda3299f78c34c7e41a251
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-security-for-the-cost-accounting-analysis-power-bi-content"></a>Konfigurere sikkerhet for kostnadsregnskap analysen strømmen BI-innhold

Dette emnet forklarer hvordan du kan overføre tilgang til brukersikkerhet i kostnadsregnskap radnivå sikkerhet i Microsoft Power BI. Denne funksjonaliteten hjelper med å garantere at brukere bare se strømmen BI data som de har tilgang til.

<a name="overview"></a>Oversikt
--------

Den **Kostregnskapsanalyse** Microsoft Power BI-innhold bruker strøm BI radnivå sikkerhet til å begrense tilgangen til en bruker. Sikkerhet er basert på tilgangsnivå organisasjonshierarkiet som er definert i parametere for kostnadsregnskap. For mer informasjon om den **Kostregnskapsanalyse** strømmen BI innhold, se [Kostregnskapsanalyse strømmen BI-innhold](cost-accounting-analysis-content-pack.md).

## <a name="setup"></a>Konfigurer
Hvis du vil overføre access brukersikkerhet til strøm BI, må eieren av strømmen BI-innhold følger du denne fremgangsmåten. **Merk:** brukeren som publiserer den **Kostregnskapsanalyse** strømmen BI-innhold blir automatisk eieren. Bare en eier kan konfigurere sikkerhet for strøm BI. I tillegg til en eier legger til andre brukere på PowerBI.com, ingen unntatt eieren kan se alle dataene i den **Kostregnskapsanalyse** strømmen BI-innhold.

1.  Publisere definisjonsfilen til strøm BI.
2.  Logg på PowerBI.com.
3.  Finne datasettet for den **Kostregnskapsanalyse** strømmen BI-innhold.
4.  Åpne sikkerhetssiden. 

    [![Åpne sikkerhetssiden](https://msdynamics.blob.core.windows.net/media/2017/02/CA-picture-1.png)](https://msdynamics.blob.core.windows.net/media/2017/02/CA-picture-1.png)

5.  Den **kostnader objekt Kontroller** rolle er allerede opprettet. Legge til andre medlemmer som er en del av organisasjonshierarkiet for kostnadsregnskap-tilgangsnivå. 

    [![Legge til medlemmer](https://msdynamics.blob.core.windows.net/media/2017/02/CA-picture-2.png)](https://msdynamics.blob.core.windows.net/media/2017/02/CA-picture-2.png)

Brukere som er lagt til i **kostnader objekt Kontroller** rolle vil bare se dataene de har lov til å se, i henhold til definisjonen i kostnadsregnskap-tilgangsnivå organisasjonshierarkiet. **Merk:** rad brukersikkerhet gjelder brikker og rapporter i Microsoft Dynamics 365 for operasjoner som er innebygd fra strømmen BI.

## <a name="updating-security"></a>Oppdatering sikkerhetsoppdatering
Hvis oppdateringer gjøres i access brukersikkerhet i kostnadsregnskapet, og du vil strømmen BI skal gjenspeile oppdateringer, må du oppdatere enheten butikken for den **Kostregnskapsanalyse** strømmen BI-innhold. Når du har fullført enhet butikken oppdateringen fra Dynamics 365 for operasjoner, må du oppdatere artefakter i PowerBI.com. Hvis du vil ha mer informasjon om hvordan du gjør en enhet butikk-oppdatering, kan du se [oppdatering enhet butikken](power-bi-integration-entity-store.md#update-entity-store). Eieren av den **Kostregnskapsanalyse** strømmen BI-innhold må også gjøre en enhet butikken oppdatering hvis nye brukere får tilgang til organisasjonshierarkiet. I tillegg eieren må legge til nye brukere til den **kostnader objekt Kontroller** rolle i PowerBI.com, slik at sikkerheten på radnivå er brukt for dem.

## <a name="disabling-security"></a>Deaktivering av sikkerhet
Vi antar at organisasjonen ønsker å begrense tilgang til data. Hvis en eller annen grunn sikkerhetsparameterene er deaktivert når du kjører kostnadsregnskap, eieren må legge til brukere i den **regnskapsfører** rolle i BI strøm i stedet. Hvis du endrer sikkerhet fra en aktivert tilstand til en deaktivert, er det en god idé å fjerne brukere fra den **kostnader objekt Kontroller** rolle. Og omvendt Hvis du reaktivere sikkerhet. Brukere kan tilhøre begge rollene. Felles tilgang er union av begge rollene. Med den **Kostregnskapsanalyse** strømmen BI innhold, og brukere som har felles tilgang har ubegrenset tilgang til data. Hvis målet ditt er å bruke begrenset tilgang, brukere må tilordnes bare til de **kostnader objekt Kontroller** rolle. Disse sikkerhetsoppdateringene på radnivå trer i kraft umiddelbart. Berørte brukere bør oppdatere sine lesere.

## <a name="additional-resources"></a>Tilleggsressurser
Hvis du vil vite mer om strøm Annenhver rad for brukersikkerhet, kan du se [administrere sikkerhet på modellen i strømmen BI](https://powerbi.microsoft.com/en-us/documentation/powerbi-admin-rls/#manage-security-on-your-model).


