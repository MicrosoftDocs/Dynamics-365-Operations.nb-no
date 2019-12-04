---
title: Definere sikkerhet for Power BI-innhold for analyse av kostnadsregnskap
description: Dette emnet forklarer hvordan du kan overføre tilgangsnivåsikkerhet i Kostnadsregnskap til radnivåsikkerhet i Microsoft Power BI. Denne funksjonaliteten lar brukere bare se Power BI-data som de har tilgang til.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 270294
ms.assetid: 3a7ba8b0-ac57-4159-9cd8-4308f6021f36
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: d371d35352348b1cfe1dd2a5ba25e1b2b20d7d71
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/06/2019
ms.locfileid: "2769907"
---
# <a name="set-up-security-for-the-cost-accounting-analysis-power-bi-content"></a>Definere sikkerhet for Power BI-innhold for analyse av kostnadsregnskap

[!include [banner](../includes/banner.md)]

Dette emnet forklarer hvordan du kan overføre tilgangsnivåsikkerhet i Kostnadsregnskap til radnivåsikkerhet i Microsoft Power BI. Denne funksjonaliteten lar brukere bare se Power BI-data som de har tilgang til.

## <a name="overview"></a>Oversikt

**Kostregnskapsanalyse**-innholdet for Microsoft Power BI bruker Power BI-radnivåsikkerhet til å begrense brukertilgangen. Sikkerheten er basert på organisasjonshierarkiet for tilgangsnivå som er definert i parametere for kostnadsregnskapet. Hvis du vil ha mer informasjon om **Kostregnskapsanalyse**-innhold for Power BI, kan du se [Kostnadsregnskapsanalyse-innhold for Power BI.](cost-accounting-analysis-content-pack.md)

## <a name="setup"></a>Installasjon
For å overføre tilgangsnivåsikkerhet til Power BI må eieren av Power BI-innholdet følge fremgangsmåten nedenfor.

> [!NOTE]
> Brukeren som publiserer **Kostregnskapsanalyse**-innholdet for Power BI blir automatisk eieren. Bare en eier kan konfigurere sikkerhet for Power BI. Før en eier legger til andre brukere på PowerBI.com kan ingen unntatt eieren se alle dataene i Power BI-innholdet **Kostnadsregnskapsanalyse**.

1. Publisere definisjonsfilen til Power BI.
2. Logg på PowerBI.com.
3. Finn datasettet for **Kostnadsregnskapsanalyse**-innhold for Power BI.
4. Åpne sikkerhetssiden.

    ![Åpne sikkerhetssiden](./media/CA-picture-1.png)

5. Rollen **Kontroller for kostnadsobjekt** er allerede opprettet. Legg til andre medlemmer som er en del av organisasjonshierarkiet for tilgangsnivået for kostnadsregnskap.

    ![Legge til medlemmer](./media/CA-picture-2.png)

Brukere som legges til i rollen **Kontroller for kostnadsobjekt**, kan bare se dataene som de har tillatelse til å se i henhold til definisjonen i organisasjonshierarkiet for tilgangsnivået for kostnadsregnskap.

> [!NOTE]
> Sikkerheten på radnivå gjelder fliser og rapporter som er innebygd fra Power BI.

## <a name="updating-security"></a>Oppdatere sikkerhet
Hvis oppdateringer gjøres i tilgangsnivåsikkerhet i kostnadsregnskapet og du vil at Power BI skal gjenspeile disse oppdateringene, må du oppdatere enhetsbutikken for **Kostnadsregnskapsanalyse**-innholdet for Power BI. Når du har fullført oppdateringen av enhetsbutikken, må du oppdatere artefaktene på PowerBI.com. Hvis du vil ha mer informasjon om hvordan du utfører en oppdatering for enhetsbutikk, kan du se [Power BI-integrering med enhetslager](power-bi-integration-entity-store.md#update-entity-store). Eieren av **Kostnadsregnskapsanalyse**-innholdet for Power BI må også utføre en oppdatering av enhetsbutikken hvis nye brukere gis tilgang til organisasjonshierarkiet. I tillegg må eieren legge til nye brukere i rollen **Kontroller for kostnadsobjekt** på PowerBI.com, slik at radnivåsikkerhet gjelder for dem.

## <a name="disabling-security"></a>Deaktivere sikkerhet
Vi antar at organisasjonen vil begrense tilgang til data. Hvis sikkerhetsparameterene er deaktivert av en eller annen grunn ved kjøring av kostnadsregnskap, må eieren legge brukere til i rollen **Regnskapsfører lager** i Power BI i stedet. Hvis du endrer sikkerhet fra en aktivert tilstand til en deaktivert tilstand, er det en god idé å fjerne brukere fra rollen **Kontroller for kostnadsobjekt**. Utfør dette omvendt hvis du aktiverer sikkerhet på nytt. Brukere kan tilhøre begge rollene. Felles tilgang er foreningen av begge rollene. For **Kostnadsregnskapsanalyse**-innhold for Power BI har brukere med felles tilgang ubegrenset tilgang til data. Hvis målet ditt er å bruke begrenset tilgang, må brukere bare tilordnes til rollen **Kontroller for kostnadsobjekt**. Disse oppdateringene for radnivåsikkerhet trer i kraft umiddelbart. Berørte brukere må oppdatere nettleseren.

## <a name="additional-resources"></a>Tilleggsressurser
Hvis du vil ha mer informasjon om radnivåsikkerhet i Power BI, kan du se [Administrere sikkerhet for modellen i Power BI](https://powerbi.microsoft.com/documentation/powerbi-admin-rls/#manage-security-on-your-model).
